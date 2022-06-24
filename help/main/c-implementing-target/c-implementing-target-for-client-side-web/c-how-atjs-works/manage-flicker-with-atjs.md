---
keywords: 플리커;at.js;구현;비동기적;비동기적;동기
description: at.js 및 Adobe 방법 알아보기 [!DNL Target] 페이지 또는 앱을 로드하는 동안 깜박임(기본 콘텐츠가 활동 콘텐츠로 대체되기 전에 일시적으로 표시)을 방지합니다.
title: at.js는 플리커를 어떻게 관리합니까?
feature: at.js
role: Developer
exl-id: f6c26973-e046-42ed-91db-95c8a4210a9d
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 58%

---

# at.js에서 플리커를 관리하는 방법

페이지 또는 앱 로드 중 Target at.js JavaScript 라이브러리가 어떻게 플리커를 방지하는지에 대한 정보입니다.

플리커는 기본 컨텐츠가 활동 컨텐츠로 대체되기 전에 방문자에게 순간적으로 표시될 때 발생합니다. 플리커는 방문자에게 혼란을 야기할 수 있으므로 달갑지 않습니다.

## 자동 생성된 글로벌 mbox 사용 {#section_C502170D551C4F52AAFD8E82C41BB63A}

를 활성화하는 경우 [글로벌 mbox를 자동으로 만들기](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/global-mbox-overview/)at.js 구성 시 {target=_blank} 설정을 지정하면 at.js가 페이지 로드 시 불투명도 설정을 변경하여 플리커를 관리합니다. at.js가 로드되면 at.js는 요소의 불투명도 설정을 `<body>` &quot;0&quot;으로 변경하여 방문자가 처음에 페이지를 볼 수 있도록 합니다. Target에서 응답을 받은 후 또는 Target 요청에 오류가 감지되면 at.js가 불투명도를 &quot;1&quot;로 재설정합니다. 이렇게 하면 활동의 컨텐츠가 적용된 후에만 방문자에게 페이지가 표시됩니다.

at.js 구성 시 이 설정을 활성화할 경우 at.js가 HTML BODY 스타일 불투명도를 0으로 설정합니다. Target의 응답을 받은 후 at.js는 HTML BODY 불투명도를 1로 재설정합니다.

0으로 설정된 불투명도는 깜박임을 방지하기 위해 페이지 컨텐츠를 숨기지만, 브라우저가 여전히 페이지를 렌더링하고 CSS, 이미지 등과 같은 필요한 모든 자산을 로드합니다.

구현에서 불투명도 0이 작동하지 않는 경우 `bodyHiddenStyle`을 사용자 지정하여 깜박임을 관리하고 `body {visibility:hidden !important}`로 설정할 수도 있습니다. 두 값 body를 사용할 수 있습니다 `{opacity:0 !important}` 또는 `body {visibility:hidden !important}`- 특정 환경에 가장 적합한 항목

다음 그림에서는 at.js 1.*x*&#x200B;와 at.js 2.x의 본문 숨기기와 본문 표시 호출을 보여줍니다.

**at.js 2.x**

![Target 흐름: at.js 페이지 로드 요청](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-flow-page-load-request.png)

**at.js 1.*x***

![](assets/target-flow2.png)

에 대한 자세한 정보 `bodyHiddenStyle` 무시: [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

## at.js를 비동기식으로 로드할 때 플리커 관리

at.js를 비동기식으로 로드하는 것은 브라우저 렌더링이 차단되지 않도록 하는 좋은 방법입니다. 그러나 이 기법은 웹 페이지에서 플리커를 유발할 수 있습니다.

관련 HTML 요소가 [!DNL Target]에 의해 개인화된 후 표시되는 사전에 숨기는(pre-hiding) 코드 조각을 사용하여 플리커(깜박임)를 방지할 수 있습니다. 

at.js는 페이지에 직접 포함되거나 태그 관리자(예: [!DNL Adobe Experience Platform Launch]).

at.js가 페이지에 포함된 경우 at.js를 로드하기 전에 코드 조각을 추가해야 합니다. 비동기식으로 로드되는 태그 관리자를 통해 at.js를 로드하는 경우 태그 관리자를 로드하기 전에 코드 조각을 추가해야 합니다. 태그 관리자가 동기식으로 로드되는 경우 스크립트는 at.js 앞에 태그 관리자 내에 포함될 수 있습니다.

사전에 숨기는 코드 조각은 다음과 같습니다.

```
;(function(win, doc, style, timeout) {
  var STYLE_ID = 'at-body-style';

  function getParent() {
    return doc.getElementsByTagName('head')[0];
  }

  function addStyle(parent, id, def) {
    if (!parent) {
      return;
    }

    var style = doc.createElement('style');
    style.id = id;
    style.innerHTML = def;
    parent.appendChild(style);
  }

  function removeStyle(parent, id) {
    if (!parent) {
      return;
    }

    var style = doc.getElementById(id);

    if (!style) {
      return;
    }

    parent.removeChild(style);
  }

  addStyle(getParent(), STYLE_ID, style);
  setTimeout(function() {
    removeStyle(getParent(), STYLE_ID);
  }, timeout);
}(window, document, "body {opacity: 0 !important}", 3000));
```

기본적으로 이 코드 조각은 전체 HTML BODY를 사전에 숨깁니다. 일부 경우, 전체 페이지가 아닌 특정 HTML 요소만 사전에 숨길 수 있습니다. 이 작업은 스타일 매개 변수를 사용자 지정하여 수행할 수 있습니다. 이것은 페이지의 특정 영역만을 사전에 숨기는 어떤 것으로 대체할 수 있습니다.

예를 들어, ID별로 식별되는 두 개의 영역인 container-1 및 container-2가 있으면 이 스타일을 기본값 대신 다음과 같이 바꿀 수 있습니다.

```
#container-1, #container-2 {opacity: 0 !important}
```

기본값:

```
body {opacity: 0 !important}
```

## at.js 2.x에서 triggerView()에 대한 플리커를 관리합니다

DOM 사전 숨김은 초기 페이지 로드에만 적용됩니다. SPA의 경우 DOM은 `triggerView()` 가 호출됩니다. SPA에서 DOM으로 컨텐츠를 렌더링하는 시간과 at.js 업데이트 사이에 잠깐의 깜박임이 있을 수 있습니다 [!DNL Target] 오퍼.  깜박임을 최소화하기 위해 `triggerView` 페이지 로드 컨텐츠를 수정하려면 페이지가 렌더링되는 즉시 &#39;triggerView&#39;를 호출해야 합니다.

## getOffer() 및 applyOffer()를 사용하여 플리커 관리

`getOffer()`와 `applyOffer()`는 모두 낮은 수준의 API이므로 기본으로 제공되는 플리커 제어 기능이 없습니다. `applyOffer()`에 선택기 또는 HTML 요소를 선택 사항으로 전달할 수 있습니다. 이 경우 `applyOffer()`는 활동 컨텐츠를 이 특정 요소에 추가하게 됩니다. 하지만, `getOffer()`와 `applyOffer()`를 호출하기 전에 해당 요소가 제대로 미리 숨겨져 있는지 확인해야 합니다.

```
document.documentElement.style.opacity = "0";
 
adobe.target.getOffer({
    mbox: 'target-global-mbox',
    success: function(offer) {
        adobe.target.applyOffer({
            mbox: 'target-global-mbox',
            offer: offer
        });
 
        document.documentElement.style.opacity = "1";
    },
    error: function() {
        document.documentElement.style.opacity = "1";        
    }
});
```

## at.js 1.x에서 mboxCreate()과 함께 지역 mbox 사용(at.js 2.x에서는 지원되지 않음)

지역 mbox 구현을 사용하는 경우 다음 샘플 코드와 유사하게 공급된 페이지에 `mboxCreate()`을 사용할 수 있습니다.

```
<div class="mboxDefault">
Some default content
</div>
<script>
mboxCreate('some-mbox');
</script>
```

페이지가 적절하게 공급되면 at.js는 mboxDefault 클래스를 사용하여 요소의 CSS &quot;가시성&quot; 속성을 적절하게 전환하여 플리커를 관리합니다.