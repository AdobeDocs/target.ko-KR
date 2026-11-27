---
keywords: 시각적 경험 작성기;시각적 경험 작성기 우수 사례;시각적 경험 작성기 제한 사항;시각적 경험 작성기 주의 사항;vec 우수 사례;vec
description: '[!UICONTROL 시각적 경험 작성기] (VEC)를 사용할 때 경험이 예상대로 작동하도록 하는 모범 사례에 대해 알아봅니다.'
title: '[!UICONTROL 시각적 경험 작성기] 모범 사례 및 제한 사항은 무엇입니까?'
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
TQID: 'https://experienceleague.adobe.com/upZDSyuS9VqUmYskNXrlYazhwRHmZGBpSR-cR-qliRs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '2420'
ht-degree: 8%
---
# [!UICONTROL 시각적 경험 작성기] 모범 사례 및 제한 사항 {#vec-best-practices}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 경험을 만들 때 알아 두어야 할 모범 사례, 주의 사항 및 제한 사항에 대해 알아봅니다.

>[!ENDSHADEBOX]

다음은 [!DNL Adobe Target] **[!UICONTROL 시각적 경험 작성기]**(VEC) 함수에서 만들어진 경험이 의도한 대로 작동하는 데 도움이 되는 방법입니다. 주의 사항과 제한 사항에서는 일반적인 문제를 일으킬 수 있는 행동을 설명하므로 이를 아는 것이 문제를 방지하고 성능을 유지하는 데 도움이 됩니다.

## 모범 사례 {#best-practices}

VEC를 사용할 때는 다음 방법이 적용됩니다.

### [!UICONTROL 향상된 경험 작성기] 사용 {#enable-eec}

**[!UICONTROL 향상된 경험 작성기]**&#x200B;는 계정 수준 또는 개별 활동 수준에서 사용할 수 있습니다.

* **계정 수준:** **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**&#x200B;를 클릭한 다음 **[!UICONTROL 향상된 경험 작성기 사용]** 스위치를 켜짐 위치로 전환합니다.
* **활동 수준:** **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 활동을 만드는 동안 **[!UICONTROL 구성]** > **[!UICONTROL 페이지 전달]**&#x200B;을 클릭한 다음 **[!UICONTROL 향상된 경험 작성기 사용]** 스위치를 [켜짐] 위치로 전환하십시오.

### 페이지 설정 및 로드

+++ at.js 참조를 페이지의 `<head>` 섹션 맨 위에 놓습니다.

**[!UICONTROL 방문자 API 서비스]**&#x200B;도 사용하는 경우 at.js 위에 방문자 API 스크립트를 배치하십시오.

+++

+++ [!UICONTROL 향상된 경험 작성기]가 사이트의 보안 페이지에 로드되지 않는 경우 IP 주소 추가

**[!UICONTROL 고급 경험 작성기]** 프록시에 사용되는 [!DNL Adobe] 서버의 IP 주소 허용 목록에 추가로 로드 문제가 해결되었습니다. 이러한 IP 주소는 활동 편집에만 필요합니다. 사이트 방문자는 허용 목록에추가된으로 이용할 필요가 없습니다. IP 주소가 [EEC가 공용 IP에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다.](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#eec-ip-addresses)(*고급 경험 작성기 관련 문제 해결*).

+++

+++ 웹 사이트에서 base 태그를 사용하여 URL 및 링크를 확인하지 마십시오.

**[!UICONTROL 향상된 경험 작성기]**&#x200B;를 포함한 VEC는 모든 링크 URL을 업데이트하는 프록시 서버를 통해 웹 사이트를 백그라운드로 조작하여 프록시에서 작동하게 합니다. 기본 태그가 추가되면 브라우저가 이러한 URL을 다시 확인하므로 손상된 것으로 표시됩니다.

+++

+++ JavaScript 코드에서는 `top` 또는 `self` 변수를 사용하지 마십시오.

**[!UICONTROL 향상된 경험 작성기]**&#x200B;를 사용하도록 설정하면 `top` 및 `self` 변수의 값이 업데이트되어 iframe 버스팅을 사용하지 않도록 설정됩니다. X-Frame-Options 헤더를 사용하여 사용자 지정 JavaScript 코드 대신 iframe 버스팅을 추가하십시오.

+++

+++ 페이지가 로드될 때 매개 변수가 추가되면 항상 웹 사이트를 테스트하십시오.

예를 들어 다음 URL 매개 변수는 iframe에서 편집할 `www.abc.com`을(를) 여는 데 사용됩니다.

`www.abc.com?mboxEdit=1&mboxDisable=1`

이러한 매개 변수를 추가한 후 웹 사이트가 예상대로 로드되는지 확인하십시오.

+++

+++ 페이지가 iframe에서 예상대로 열리는지 확인하십시오.

웹 사이트에서 iframe 버스팅 기술을 끄고 웹 사이트가 더미 페이지의 iframe에서 예상대로 열리는지 확인합니다. 예:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <iframe src="https://www.homedepot.com"</iframe>
</body>
</html>
```

+++

### 페이지 마크업

+++ 최상위 수준 요소 및 올바른 테스트 또는 타기팅 후보인 기타 모든 요소에 고유 ID를 사용하십시오.

본문 요소 바로 내부에 있는 모든 항목에는 고유한 ID가 있어야 합니다. 그러면 새 요소가 본문에 삽입되고 코드가 이동할 때 부모 요소를 쉽게 인식할 수 있습니다.

[!DNL Target]에는 ID가 필요하지 않지만 ID는 경험 작성기로 만든 경험의 안정성을 증가시킵니다. [!DNL Target]은(는) 경험이 전달될 때 CSS 선택기를 사용하여 콘텐츠를 수정합니다. 경험을 편집하면 **[!UICONTROL 시각적 경험 작성기]**&#x200B;가 선택기를 null이 아닌 ID 특성이 있는 수정된 HTML 요소의 가장 가까운 상위 요소에 고정합니다. 따라서 JavaScript 라이브러리를 포함하여 HTML ID 속성을 설정하거나 수정하는 메커니즘을 사용하는 것은 권장되지 않습니다. 이러한 ID는 활동을 만들 때 경험 작성기에서 사용할 수 있지만, JavaScript에서 이를 수정하는 경우 경험이 실행될 때 만들 때 사용되는 ID를 사용할 수 없을 수 있습니다. ID를 사용할 수 없는 경우 해당 ID에 고정된 선택기가 실패합니다.

+++

+++ 수사적 CSS 클래스 이름을 사용합니다.

설명 클래스 이름을 사용하면 **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 CSS 클래스를 편집할 때 클래스를 쉽게 식별할 수 있습니다. 이렇게 하면 올바른 CSS 클래스가 편집되고, 페이지가 예상대로 표시되도록 하는 데 도움이 됩니다.

+++

+++ 요소를 숨기거나 제거할 때 `!important` CSS 속성을 사용하지 마십시오.

`!important` CSS 속성이 있으면 사이트의 CSS 규칙이 `target.js`이(가) 게재 중에 변경한 내용을 재정의합니다.

+++

+++ 페이지 레이아웃은 HTML 표를 사용하지 마십시오.

[!DNL Target]은(는) JavaScript을 사용하여 페이지 서식을 지정하며, 표 기반 레이아웃은 JavaScript으로 수정하기 어렵습니다. 표 기반 레이아웃은 모든 브라우저에서 동일한 방식으로 표시되지 않을 수도 있습니다. 최상의 결과를 얻으려면 CSS를 사용하여 페이지 레이아웃을 작성하십시오.

+++

+++ iFrame의 사용을 최소화하십시오.

iFrame을 최소화하면 페이지 및 테스트 관리가 간소화됩니다. **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 iFrame 내의 일부 작업을 적용할 수 있지만 크기 조정과 같은 일부 작업이 제대로 작동하지 않습니다. 여러 iFrame을 사용하는 페이지는 관리하고 크기를 조정하기가 어렵기 때문에 iFrame이 많은 페이지를 테스트하면 문제가 발생할 수 있습니다.

+++

+++ 앵커 요소에서는 일반 텍스트나 이미지 태그만 사용하십시오.

앵커 요소에는 일반 텍스트 중 하나가 포함되어 있습니다.

`<a>Anchor Text</a>`

또는 이미지 태그:

`<a href=""> <img src=""> </img> </a>`

+++

+++ 인라인 요소 내부에는 블록 수준 요소를 사용하지 마십시오.

블록 수준 요소는 앵커 및 span 요소와 같은 인라인 요소 내에서 사용할 수 없습니다. 이렇게 하면 인라인 요소의 높이와 너비가 손실되므로 **[!UICONTROL 시각적 경험 작성기]**&#x200B;의 오버레이 도구가 예상대로 작동하지 않을 수 있습니다.

+++

+++ 양식 필드를 제거할 때 주의하십시오.

특정 양식 필드를 제출해야 하므로 삭제하면 제출에 영향을 줄 수 있습니다.

+++

+++ HTML 코드의 타깃팅에 사용할 수 있는 중요한 텍스트를 요소 내에 보관하십시오.

예를 들어 코드가 다음과 같은 경우 장바구니 텍스트를 VEC에서 타깃팅할 수 없습니다.

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart">
   <img alt="Shopping Cart" src="/images/ico-cart.gif"></img>
   Shopping Cart:
   <span id="HeaderCartQtyTotal">
      0
  </span>
  Items
  <span id="HeaderCartPriceTotal"></span>
</a>
```

이 예에서는 VEC에서 전체 앵커 요소가 선택되어 타깃팅이 수행될 경우 다른 요소에 부정적인 영향을 줍니다.

+++

### 편집 및 게재

+++ DOM이 준비된 후 가능한 한 빨리 모든 동적 DOM 수정 사항을 조정합니다.

`target.js`이(가) 경험을 적용하기 전에 수정 사항을 적용하지 못하면 콘텐츠 전달이 중단될 수 있습니다. 이런 일은 타깃팅된 요소의 계층 구조에 DOM 변경 사항이 있는 경우에만 발생합니다.

+++

+++ HTML 편집을 사용하여 DOM 구조를 조작하면 선택기가 손상될 수 있습니다.

예를 들어 다음 두 가지 작업이 수행됩니다.

* 클래스가 요소 1에 추가됩니다.
* 요소 1의 HTML이 편집됩니다.

각 변경 사항은 VEC에 새 요소를 만듭니다. 두 번째 작업은 요소 1을 수정하므로, 요소 1이 삭제되면 두 번째 작업에는 더 이상 수정할 사항이 없고 변경 사항이 더 이상 작동하지 않습니다.

같은 방식으로 요소가 텍스트와 함께 추가된 다음 별도의 작업을 통해 해당 요소를 다른 텍스트로 편집하는 경우 코드 편집기는 두 작업을 모두 별도의 요소로 표시합니다. 편집하면 원래 요소를 수정하고 편집된 텍스트를 포함하는 새 요소가 만들어집니다. 원래 요소가 삭제되면 편집된 텍스트가 수정할 요소를 찾을 수 없고 표시되지 않습니다. 두 번째 요소는 요소 목록에 남아 있지만, 변경되는 요소가 더 이상 존재하지 않으므로 페이지에 영향을 주지 않습니다.

**[[!UICONTROL 시각적 경험 작성기에 사용된 [요소 선택기]**]](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#vec-selectors)를 참조하십시오.

+++

+++ 서식 있는 텍스트 편집기로 텍스트 요소에 스타일을 지정할 때 `<b>` 및 `<i>` 태그를 사용하십시오.

* 굵은 텍스트를 표시하려면 `<strong>`보다는 `<b>`를 사용하십시오.
* 기울임체 텍스트를 표시하려면 `<em>`보다는 `<i>`를 사용하십시오.

`<strong>` 및 `<em>` 태그로 인해 예기치 않은 결과가 발생할 수 있습니다.

+++

+++ 스크립트 내에 `mboxCreate`을(를) 포함하지 마십시오.

`mboxCreate`이(가) `document.write`을(를) 사용하므로 스크립트에 포함시키지 않는 것이 좋습니다. 같은 목적으로 `mboxDefine` 및 `mboxUpdate`을(를) 사용합니다.

+++

+++ 코드 조각에 초기화에 HTML 코드가 필요한 경우 [!DNL Target]&#x200B;(으)로 JavaScript 코드 조각을 업데이트하지 마십시오.

슬라이더와 회전 메뉴 등 페이지 구성 요소에서 작업(HTML 편집)을 수행하면 게재가 손상된 것으로 표시될 수 있습니다. VEC는 JavaScript이 페이지 구성 요소를 인스턴스화한 후 작업을 수행합니다. 하지만 페이지 콘텐츠가 방문자에게 전달되면 구성 요소가 인스턴스화되기 전에 작업이 적용됩니다. 따라서 페이지의 구성 요소를 정의하는 스크립트에 따라 구성 요소의 기능이 전달 시 중단되거나 중단되지 않을 수 있습니다.

처음 작동하는 게재 테스트는 다음과 같은 경합 조건이 존재할 수 있으므로 게재가 계속 작동한다고 보장하지 않습니다.

* 경합 조건이 있는 경우 게재가 간헐적으로 작동합니다.
* 경합 조건이 없으면 항상 배달이 작동합니다.

페이지를 여러 번 테스트하여 게재가 예상대로 작동하는지 확인하십시오.

+++

## 주의 사항 {#caveats}

**[!UICONTROL 시각적 경험 작성기]**&#x200B;를 사용하여 활동을 디자인할 때 다음 주의 사항이 적용됩니다.

+++ [!UICONTROL 이동] 기능은 z-색인을 지원하지 않습니다.

z-색인 기능이 없으면 이동된 요소를 다른 요소의 맨 위에 배치할 수 없습니다. 자세한 내용은 [제한 사항](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721)을 참조하십시오.

+++

+++ 요소를 다시 정렬하는 것은 클릭 추적에 영향을 줍니다.

클릭 추적으로 표시된 요소가 재배열되면 재배열된 요소의 경로가 변경됩니다. 그 결과 원래 요소가 재배열되기 전에 있었던 위치에 있는 요소에 대한 클릭 수가 추적됩니다.

이는 활동 콘텐츠를 전달하는 코드와 클릭을 추적하는 코드가 페이지에 전달되는 하나의 코드에 포함되기 때문에 발생합니다. 다른 페이지로으로 이동하고 클릭 추적이 설정되어 있는 경우 두 코드 조각이 모두 해당 페이지로 전달됩니다. 클릭 추적 페이지의 페이지 구조가 테스트가 실행되는 페이지의 구조와 유사한 경우 테스트 콘텐츠가 클릭 추적 페이지에도 표시될 수 있습니다.

+++

+++ mbox인 `<div>`에서는 요소 삽입이 작동하지 않을 수 있습니다.

mbox에 오퍼가 포함되어 있고 mbox가 잘못 구현되면 삽입된 요소가 `insertAfter`이(가) 아닌 `insertBefore`(으)로 나타날 수 있습니다.

+++

+++ 상위 요소와 하위 요소를 모두 편집할 때 상위를 먼저 편집하십시오.

요소에서 이미지 작업을 스왑한 다음 해당 상위 요소의 텍스트 또는 HTML을 편집하면 게재 문제가 발생할 수 있습니다. 가장 좋은 워크플로우는 하위 요소의 이미지를 교체하기 전에 상위 요소를 편집하는 것입니다.

+++

+++ mbox를 하위 요소로 포함하는 페이지 요소는 선택하지 마십시오.

예를 들어 페이지에 다음 코드가 포함되어 있는 경우:

```html
<div>
  <div class="mboxDefault" >
  </div>
  <script>mboxCreate('myMbox');
</script>
</div>
```

페이지에서 하드코딩된 mbox가 여전히 [!DNL Target]을(를) 호출하고 응답을 수신하므로 경험에서 외부 div를 선택하면 안 됩니다. 이 응답은 더 큰 페이지 요소용으로 수행되는 응답을 방해합니다.

+++

+++ 프록시 IP 주소는 고객의 환경에서 차단될 수 있습니다.

스테이징 환경과 같이 라이브가 아닌 사이트에서 **[!UICONTROL 향상된 경험 작성기]**&#x200B;를 사용하는 경우 사이트에서 프록시 IP 주소를 차단하면 시간 초과 및 액세스 거부 오류가 발생할 수 있습니다.

+++

## 제한 {#section_F33C2EA27F2E417AA036BC199DD6C721}

VEC를 사용하여 작업할 때는 다음 제한 사항이 적용됩니다.

### 페이지 요구 사항

+++ [!DNL Chrome] 확장 정책 변경 내용과의 VEC 호환성을 처리합니다.

Google Chrome[&#128279;](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}의 업데이트된 V3 매니페스트 정책에서 확장은 브라우저가 DOM을 구문 분석하기 전에 더 이상 원본 DOM을 수정할 수 없습니다. 따라서 iframe 버스팅 구현과 같은 특정 보안 스크립트는 VEC에서 페이지가 로드되지 않도록 차단할 수 있습니다.

호환성을 보장하려면 페이지가 [!DNL Target] iframe 내부에 로드될 때 이러한 스크립트를 조건부로 비활성화하십시오. 이 작업은 VEC가 로드되는 동안 [!DNL Target]에서 주입하는 `window.adobeVecExtension` 개체가 있는지 확인하여 안전하게 수행할 수 있습니다.

다음 코드 조각은 웹 페이지가 VEC에 로드되지 않도록 하는 iframe 버스팅 코드의 예입니다.

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

웹 페이지가 [!DNL Target] 내에 포함된 경우 간단한 검사를 통해 확인할 수 있습니다. 코드 조각은 다음과 같습니다.

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

+++ VEC가 작동하려면 페이지가 URL 매개 변수를 허용해야 합니다.

일부 사이트는 페이지에서 URL 매개 변수를 모두 삭제하지만 VEC에는 이러한 매개 변수가 필요합니다.

+++

+++ 스크립트가 HTML의 일부로 사용되는 경우 창 네임스페이스 아래에 외부에서 액세스하는 모든 변수 및 함수를 선언합니다.

스크립트가 페이지가 로드된 후 `target.js`의 범위 내에서 실행되므로 로컬로 선언된 변수 또는 함수는 스크립트 블록 외부에서 액세스할 수 없습니다.

*잘못된 코드:*

```html
<script>
  var myVar = 123;
  function myFunc() {
    //
  }
</script>
```

*올바른 코드:*

```html
<script>
  window.myVar = 123;
  window.myFunc = function() {
    //
  };
</script>
```

+++

+++ VEC의 `customCode` 작업이 [!DNL Internet Explorer] 8에서 작동하지 않습니다.

스크립트 콘텐츠를 처리할 때 IE8 제한 사항으로 인해 `target.js`은(는) IE8에서 이 작업을 지원하지 않습니다. 해결 방법으로, 페이지에 jQuery가 있고 jQuery가 창 개체에 전역적으로 노출되는 경우 `target.js`은(는) `customCode` 작업을 전달할 수 있습니다. `window.jQuery` 및 `window.jQuery.fn.prepend`이(가) 정의되어 있는지 확인하십시오.

+++

### 재배열 및 mbox

**CSS 속성이 뒤에 오는 컨테이너 외부로 요소를 이동할 수 없습니다.**

+++ 다시 정렬하기 위해 [!UICONTROL Button] 요소를 선택할 수 없습니다.

**[!UICONTROL Button]** 요소를 다시 정렬하기 위해 직접 선택할 수 없습니다. 재배치를 활성화하려면 버튼을 더 큰 컨테이너에 배치합니다.

+++

+++ 동일한 요소를 재배열하고 이동하지 마십시오.

요소를 다른 위치로 이동한 다음 상위 컨테이너를 선택하여 하위 요소를 다시 정렬하면 이동된 요소는 영향을 받지 않고 그대로 유지됩니다. 재배열이 원하는 대로 표시되지 않을 수 있습니다.

+++

+++ 교체 오퍼만 mbox에서 사용할 수 있습니다.

**[!UICONTROL 클래스 편집]** 및 **[!UICONTROL 다시 정렬]**&#x200B;과 같은 작업은 mbox 내에서 허용되지 않습니다.

+++

### 이미지

+++ [!UICONTROL 이미지 변경] 작업은 회전 메뉴에 있는 이미지에 작동하지 않습니다.

예를 들어 페이지에 6개의 이미지가 있는 회전 메뉴가 포함되어 있고 이미지가 회전 메뉴의 두 번째 이미지와 교환되는 경우 **[!UICONTROL 이미지 변경]** 작업이 작동하지 않습니다.

해결 방법으로 상위 컨테이너를 선택하고 **[!UICONTROL HTML 편집]** 작업을 사용하여 회전판의 HTML을 편집하고 원하는 이미지의 이미지 소스를 업데이트합니다.

+++

+++ mbox에서 이미지 크기를 조정할 수 없습니다.

이미지가 mbox 요소에서 교체된 다음 mbox 요소의 크기에 따라 크기가 조정되는 경우 크기 조정이 허용되지 않습니다.

+++

+++ 이미지를 교체한 후에는 [!UICONTROL 편집] 작업을 선택할 수 없습니다.

이미지를 교체한 후에는 Scene7 URL을 편집할 수 없습니다.

+++

+++ [!UICONTROL 컨텐츠] 라이브러리(Scene7)에서 이미지를 삽입하고 HTML을 편집하면 이미지 URL이 손상됩니다.

일부 더미 텍스트를 사용하여 `customHeaderMessage` div 내부에 앵커 요소를 추가합니다.

```html
<a href="#">
<span> Dummy text </span>
</a>
```

**[!UICONTROL 요소 삽입]** 작업을 사용하여 이 div를 선택하여 이미지를 더미 텍스트의 형제 이미지로 삽입합니다.

이미지가 삽입되면 코드는 다음과 같이 표시됩니다.

```html
<a href="#">
<span> Dummy text </span>
<img src=""> This is inserted Image. </img>
</a>
```

더미 텍스트 span을 제거합니다.

+++

### 클릭 추적 및 외부 콘텐츠

+++ 일반 텍스트나 이미지 태그 이외의 항목을 포함하는 앵커 요소에 대해서는 클릭 추적이 작동하지 않습니다.

예를 들어 요소에 JavaScript가 포함되어 있으면 클릭 추적이 작동하지 않습니다.

+++

+++ 클릭 추적은 경험이 만들어진 페이지나 리디렉션된 페이지에서만 지원됩니다.

VEC에서 클릭 추적에 **[!UICONTROL 찾아보기]** 모드를 사용할 수 있지만 **[!UICONTROL 찾아보기]** 모드는 페이지에서 클릭 추적을 추가하는 데 사용할 수 없습니다.

+++

+++ 외부 소스가 있는 HTML 요소는 편집할 수 없습니다.

예: 비디오, 오디오 태그, embed, iFrames 및 프레임

+++
