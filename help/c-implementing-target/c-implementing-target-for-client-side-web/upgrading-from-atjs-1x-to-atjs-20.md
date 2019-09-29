---
description: at.js 1.*x*에서 at.js 2.*x*로 업그레이드
keywords: at.js 릴리스;at.js 버전;단일 페이지 앱;스파;크로스 도메인;크로스 도메인
seo-description: Adobe Target at.js 1.*x*에서 at.js 버전 2.0.0으로 업그레이드하는 방법에 대한 자세한 정보
seo-title: Adobe Target at.js 버전 1에서 업그레이드*x*에서 at.js 버전 2로 이동합니다.*x*
solution: Target
subtopic: 시작하기
title: at.js 1.*x*에서 at.js 2.*x*로 업그레이드
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Upgrading from at.js 1.*x* to at.js 2.*x* {#upgrading-from-atjs-1x-to-atjs-200}

[!DNL Adobe Target]의 최신 at.js 버전에서는 차세대 클라이언트측 기술에 대한 개인화를 실행하도록 기업을 지원하는 다양한 기능을 제공합니다. 이 새로운 버전은 단일 페이지 애플리케이션(SPA)과 조화로운 상호 작용을 하도록 at.js를 업그레이드하는 데 주력하고 있습니다.

Here are some benefits of using at.js 2.*x* that are not available in previous versions:

* 페이지 로드 시 모든 오퍼를 캐시하여 여러 서버 호출을 하나의 서버 호출로 줄일 수 있습니다.
* 오퍼가 기존 서버 호출로 인해 초래되는 지연 없이 캐시를 통해 즉시 표시되므로 사이트에서 최종 사용자의 경험을 크게 향상시킬 수 있습니다.
* 간단한 1줄의 코드 및 일회용 개발자 설정으로 마케터가 SPA에서 VEC를 통해 A/B 및 XT 활동을 만들고 실행할 수 있도록 할 수 습니다.

## at.js 2.*x* 시스템 다이어그램

The following diagrams help you understand the workflow of at.js 2.*x* with Views and how this enhances the SPA integration. To get a better introduction of the concepts used in at.js 2.*x*, see [Single Page Application implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![at.js 2.*파섹*](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| 호출 | 세부 사항 |
| --- | --- |
| 1 | 사용자가 인증되면 호출에서 [!DNL Experience Cloud ID]를 반환합니다. 다른 호출은 고객 ID를 동기화합니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js는 페이지에 구현된 코드 조각을 미리 숨기는 선택 사항을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | 모든 구성된 매개 변수(MCID, SDID 및 고객 ID)를 포함하는 페이지 로드 요청이 이루어집니다. |
| 4 | 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다. 저장소는 대상 라이브러리의 적절한 대상(예: Adobe Analytics, Audience Management 등에서 공유되는 대상)을 요청합니다.<br>고객 속성은 묶음 프로세스를 통해 프로필 저장소로 전송됩니다. |
| 5 | [!DNL Target]에서는 URL 요청 매개 변수 및 프로필 데이터를 기반으로 현재 페이지 및 미래 보기를 위해 방문자에게 반환할 활동 및 경험을 결정합니다. |
| 6 | 타깃팅된 콘텐츠는 다시 페이지로 전송되며, 원할 경우 추가적인 개인화를 위한 프로필 값을 포함할 수 있습니다.<br>현재 페이지의 타깃팅된 콘텐츠는 기본 콘텐츠의 플리커 없이 가능한 한 빨리 나타납니다.<br>`triggerView()`를 통해 보기를 트리거할 때 추가적인 서버 호출 없이 즉시 적용할 수 있도록 브라우저에서 캐시된 SPA의 사용자 동작에 대한 결과로서 표시되는 보기를 위한 타깃팅된 콘텐츠입니다. |
| 7 | Analytics 데이터가 데이터 수집 서버로 전송됩니다. |
| 8 | 타깃팅된 데이터는 SDID를 통해 Analytics 데이터에 대응되며 Analytics 보고 저장소로 처리됩니다.그런 다음 <br>Analytics 데이터는 Analytics for Target (A4T) 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다. |

이제 SPA에서 `triggerView()`가 구현될 때 그곳이 어디든, 보기 및 작업은 캐시에서 검색되고 서버 호출 없이 사용자에게 표시됩니다. `triggerView()`는 또한 노출 수를 증가시키고 기록하기 위해 [!DNL Target] 백엔드에 알림을 요청합니다.

![target flow at.js 2.*x* triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| 호출 | 세부 사항 |
| --- | --- |
| 1 | 보기를 렌더링하고 작업을 적용하여 시각적 요소를 수정하기 위해 SPA에서 `triggerView()`가 호출됩니다. |
| 2 | 보기용으로 타깃팅된 콘텐츠를 캐시에서 읽습니다. |
| 3 | 타깃팅된 콘텐츠는 기본 콘텐츠의 플리커 없이 가능한 한 빨리 나타납니다. |
| 4 | 활동 및 증분 지표에서 방문자를 계산하기 위해 알림 요청이 [!DNL Target] 프로필 스토어에 전송됩니다. |
| 5 | Analytics 데이터가 데이터 수집 서버로 전송됩니다. |
| 6 | Target 데이터는 SDID를 통해 Analytics 데이터에 대응되며 Analytics 보고 저장소로 처리됩니다. 그런 다음 Analytics 데이터는 A4T 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다. |

## at.js 2 배포.*x* {#deploy-atjs-200}

1. at.js 2 배포.*x* . Adobe [Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) 확장

   >[!NOTE]
   >
   > Adobe Launch를 사용하여 at.js를 배포하는 것이 가장 좋습니다.

   또는

   Manually download at.js 2.*x* using the Target UI and deploy it using the [method of your choice](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

## 사용 중단된 at.js 함수

There are several functions that have been deprecated in at.js 2.*x*.

>[!IMPORTANT]
>
>If these deprecated functions are still used on your site when at.js 2.*x* is deployed, you will see console warnings. The recommended approach when upgrading is to test the deployment of at.js 2.*x* in a staging environment and make sure to go through each and every warning that has been logged in the console and translate the deprecated functions to new functions introduced in at.js 2.*x*.

아래에는 사용이 중단된 함수와 그에 해당하는 새로운 함수가 있습니다. 전체 함수 목록이 필요하면 [at.js 함수](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md)를 참조하십시오.

>[!NOTE]
>at.js 2.** x는 `mboxDefault` 표시 요소를 더 이상 자동으로 사전에 숨기지 않습니다. 따라서 고객은 사이트에서 수동으로 또는 태그 관리자를 통해 사전 숨김 로직을 수용해야 합니다.

### mboxCreate(mbox,params)

**설명**:

요청을 실행하고 `mboxDefault` 클래스 이름을 사용하는 가장 가까운 DIV에 오퍼를 적용합니다.

**예**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**at.js 2.*x*동급**

`mboxCreate(mbox, params)`의 대체 함수는 `getOffer()`와 `applyOffer()`입니다.

**예**:

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  var el = document.currentScript.previousElementSibling;
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2"
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: el,
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      el.style.visibility = "visible";
    }
  });
</script> 
```

### mboxDefine() 및 mboxUpdate()

**설명**:

요소와 mbox 이름 사이에 내부 매핑을 만들되, 요청을 실행하지 마십시오. 요청을 실행하고 `mboxDefine()`에서 nodeId로 식별되는 요소에 오퍼를 적용하는 `mboxUpdate()`와 함께 사용됩니다. `mboxCreate`로 시작된 mbox를 업데이트하는 데도 사용할 수 있습니다. 

**예**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**at.js 2.*x*equivalent**:

`mboxDefine()`과 `mboxUpdate`의 대체 함수는 `getOffer()`와 `applyOffer()`이며 `applyOffer()`에서는 선택기 선택 사항이 사용됩니다. 이 접근 방식에서는 ID가 있는 선택기뿐만 아니라 CSS 선택기를 사용하여 오퍼를 요소에 매핑할 수 있습니다.

**예**:

```
<div id="someId" class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2",
      param3: "value3",
      param4: "value4" 
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: "#someId",
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      var el = document.getElementById("someId");
      el.style.visibility = "visible";
    }
  });
</script>
```

### adobe.target.registerExtension()

**설명**:

특정 확장 기능을 등록하는 표준 방법을 제공합니다.

이 함수는 더 이상 지원되지 않으므로 사용해서는 안 됩니다.

## 2.0에서 사용이 중단된 함수, 새로운 함수 및 지원되는 at.js 함수에 대한 요약

| 메서드 | 지원됨? | 신규? | 삭제 예정?<br>(기본 콘텐츠가 표시됩니다.) |
| --- | --- | --- | --- |
| `getOffer()` | 예 |  |  |
| `getOffers()` |  | 예 |  |
| `applyOffer()` | 예 |  |  |
| `applyOffers()` |  | 예 |  |
| `triggerView()` |  | 예 |  |
| `trackEvent()` | 예 |  |  |
| `mboxCreate()` |  |  | 예 |
| `mboxDefine()`<br>`mboxUpdate()` |  |  | 예 |
| `targetGlobalSettings()` | 예 |  |  |
| `Data Providers` | 예 |  |  |
| `targetPageParams()` | 예 |  |  |
| `targetPageParamsAll()` | 예 |  |  |
| `registerExtension()` |  |  | 예 |
| `At.js Custom Events` | 예 |  |  |

## 제한 사항 및 콜아웃

다음 제한 사항 및 콜아웃을 알아 두십시오.

### 전환 추적

전환 추적에 `mboxCreate()`을 사용하는 고객은 `trackEvent()`나 `getOffer()`를 사용해야 합니다.

### 오퍼 게재

`mboxCreate()`을 `getOffer()`나 `applyOffer()`로 대체하지 않는 고객의 경우 오퍼가 게재되지 않을 수 있습니다.

### Can at.js 2.*x는* at.js 1 동안 일부 페이지에서 사용됩니다.*x*&#x200B;나 mbox.js와 다른 페이지에 있을 때 사용할 수 있습니까?

예. 방문자 프로필은 서로 다른 버전 및 라이브러리를 사용하는 여러 페이지 간에 보존됩니다. 쿠키 형식은 동일합니다.

### New API use in at.js 2.*x*

at.js 2.*x에서는 배달 API라고 하는 새 API를 사용합니다.* at.js가 [!DNL Target] Edge Server를 올바로 호출하는지를 디버깅하기 위해 브라우저의 개발자 도구에 있는 네트워크 탭을 "게재", "`tt.omtrdc.net`" 또는 클라이언트 코드로 필터링할 수 있습니다. 또한 [!DNL Target]에서 키-값 쌍 대신 JSON 페이로드를 전송하는 것을 보게 됩니다.

### Target 글로벌 mbox가 더 이상 사용되지 않음

at.js 2.*x*, 네트워크 호출에서 더 이상 "`target-global-mbox`"가 보이지 않습니다. 대신, 아래에서 보듯이 [!DNL Target] 서버에 전송된 JSON 페이로드에서 "`target-global-mbox`" 구문을 "`execute > pageLoad`"로 대체했습니다.

```
{
  "id": {
    // ...
  },
  "context": {
    "channel": "web",
    // ...
  },
  "execute": {
    "pageLoad": {}
  }
}
```

기본적으로 글로벌 mbox 개념은 페이지 로드 시 오퍼와 콘텐츠를 검색할지 여부를 [!DNL Target]에서 알 수 있도록 하기 위해 도입되었습니다. 따라서 최신 버전에서는 이 기능을 더욱 명확하게 했습니다.

### at.js에서 글로벌 mbox 이름이 문제가 됩니까?

고객은 [!UICONTROL Target &gt; 설정 &gt; 구현 &gt; at.js 설정 편집]을 통해 글로벌 mbox 이름을 지정할 수 있습니다. 이 설정은 [!DNL Target] Edge Server에서 execute &gt; pageLoad를 [!DNL Target] UI에 나타나는 글로벌 mbox 이름으로 변환하는 데 사용됩니다. 이렇게 변환하면 고객은 계속해서 서버 측 API, 양식 기반 작성기, 프로필 스크립트를 사용할 수 있으며 글로벌 mbox 이름을 사용하여 대상을 만들 수 있습니다. 또한 다음 그림에서 보듯이, at.js 1 *x*&#x200B;나 mbox.js를 사용한 페이지가 여전히 있는 경우 동일한 글로벌 mbox 이름이 [!UICONTROL 설정 &gt; 환경 설정] 페이지에도 구성되도록 하는 것이 좋습니다.

![at.js 수정 대화 상자](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

및

![사용자 지정 글로벌 mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

### Does the auto-create global mbox setting need to be turned on for at.js 2.*x*?

대부분의 경우, 그렇습니다. This setting tells at.js 2.*x* to fire a request to the [!DNL Target] edge servers upon page load. 글로벌 mbox가 execute &gt; pageLoad로 변환되므로 페이지 로드 시 요청을 개시하려면 이 설정이 켜져 있어야 합니다.

### Will existing VEC activities continue to work, even though the target global mbox name is not specified from at.js 2.*x*?

예. execute &gt; pageLoad는 `target-global-mbox`처럼 [!DNL Target] 백엔드에서 처리됩니다.

### 양식 기반 활동을 `target-global-mbox`에 타깃팅하는 경우 이러한 활동이 계속 작동합니까?

예. execute &gt; pageLoad는 [!DNL Target]처럼 `target-global-mbox` Edge Server에서 처리됩니다.

### Supported and non-supported at.js 2.*x* Settings

| 설정 | 지원됨? |
| --- | --- |
| X-Domain | 아니오 |
| 글로벌 mbox를 자동으로 만들기 | 예 |
| 글로벌 mbox 이름 | 예 |

### at.js 2.x에서 크로스 도메인 추적 지원 {#cross-domain}

도메인 간 추적을 사용하면 여러 도메인 간에 방문자를 연결할 수 있습니다. 각 도메인에 대해 새 쿠키를 만들어야 하므로 도메인 간을 이동할 때 방문자를 추적하기가 어렵습니다. 도메인 간 추적을 수행하려면 [!DNL Target] 타사 쿠키를 사용하여 도메인 간 방문자를 추적합니다. 이렇게 하면 `siteA.com` 및 방문자가 고유 도메인을 탐색할 때 동일한 경험에 남아 있는 타겟 활동을 만들 `siteB.com` 수 있습니다. 이 기능은 Target의 타사 및 퍼스트 파티 쿠키 동작에 연결되어 있습니다.

>[!NOTE]
>
>at.js 2에서는 도메인 간 추적이 지원되지 않습니다.*x*&#x200B;에는 사용할 수 없습니다. 크로스 도메인 추적은 at.js 2에서 지원됩니다.*x* (Experience Cloud ID(ECID) 라이브러리 v4.3.0+를 통해).

Target에서 타사 쿠키는 에 저장됩니다 `<CLIENTCODE>.tt.omtrdc.net`. 퍼스트 파티 쿠키는 에 저장됩니다 `clientdomain.com`. 첫 번째 요청은 `mboxSession` 및 `mboxPC`라는 타사 쿠키를 설정하는 HTTP 응답 헤더를 반환하는 반면, 리디렉션 요청이 추가 매개 변수(`mboxXDomainCheck=true`)를 사용하여 다시 전송됩니다. 브라우저가 타사 쿠키를 수락하면 리디렉션 요청에 해당 쿠키가 포함되고 경험이 반환됩니다. 여기서는 HTTP GET 메서드를 사용하므로 이 워크플로우가 가능합니다.

However, in at.js 2.*x*, HTTP GET is no longer used and instead we use HTTP POST. 이제 HTTP POST가 at.js 2를 통해 사용됩니다.*x* to send JSON payloads to Target Edge server. 이것은 브라우저가 타사 쿠키를 지원하는지 여부를 확인하는 리디렉션 요청이 이제 중단됨을 의미합니다. 이는 HTTP GET 요청이 idempose 트랜잭션인 반면 HTTP POST는 비idempose이며 임의의 반복되어서는 안 되기 때문입니다. 따라서 at.js 2에서 크로스 도메인 추적이 가능합니다.*x* is no longer supported out of the box. at.js 1만.*x* 는 도메인 간 추적을 기본적으로 지원합니다.

크로스 도메인 추적을 사용하려면 at.js 2와 함께 [ECID 라이브러리 v4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) 을 설치해야 합니다.*x*&#x200B;에는 사용할 수 없습니다. ECID 라이브러리는 여러 도메인에서도 방문자를 식별하는 데 사용되는 영구 ID를 관리하기 위해 존재합니다. ECID 라이브러리 v4.3.0+ 및 at.js 2를 설치한 후&#x200B;*x*, 고유한 도메인을 포괄하는 활동을 만들고 사용자를 추적할 수 있습니다.

### 글로벌 mbox 자동 만들기가 지원됨

This setting tells at.js 2.*x* to fire a request to the [!DNL Target] edge servers on page-load. 글로벌 mbox가 execute &gt; pageLoad로 변환되고, [!DNL Target] Edge Server가 이를 해석하므로 고객은 페이지 로드 시 요청을 개시하려면 이 설정을 켜야 합니다.

### 글로벌 mbox 이름이 지원됨

고객은 [!UICONTROL Target &gt; 설정 &gt; 구현 &gt; at.js 설정 편집]을 통해 글로벌 mbox 이름을 지정할 수 있습니다. 이 설정은 [!DNL Target] Edge Server에서 execute &gt; pageLoad를 입력된 글로벌 mbox 이름으로 변환하는 데 사용됩니다. 이렇게 변환하면 고객은 계속해서 서버 측 API, 양식 기반 작성기, 프로필 스크립트를 사용할 수 있으며 글로벌 mbox를 타깃팅하는 대상을 만들 수 있습니다.

### 아래의 at.js 사용자 지정 이벤트는 `triggerView()`에 적용할 수 있습니까? 아니면 `applyOffer()`나 `applyOffers()`에만 적용할 수 있습니까?

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

at.js 사용자 지정 이벤트는 `triggerView()`에도 적용할 수 있습니다.

### `triggerView()`인 `{“page” : “true”}`를 호출하면 [!DNL Target] 백엔드에 알림이 전송되고 노출이 증가합니다. 이렇게 되면 프로필 스크립트도 실행됩니까?

[!DNL Target] 백엔드에 미리 가져오기 호출이 수행되면 프로필 스크립트가 실행됩니다. 그런 다음 영향을 받은 프로필 데이터가 암호화되어 클라이언트측으로 다시 전달됩니다. `{"page": "true"}`인 `triggerView()`를 호출하면 암호화된 프로필 데이터와 함께 알림이 전송됩니다. 이때 [!DNL Target] 백엔드가 프로필 데이터를 해독하고 데이터베이스에 저장합니다.

### 플리커를 관리하기 위해 `triggerView()`를 호출하기 전에 사전 숨김 코드를 추가해야 합니까?

아니요. `triggerView()`를 호출하기 전에 사전 숨김(pre-hiding) 코드를 추가할 필요는 없습니다. at.js 2.*x에서는 보기가 표시되고 적용되기 전에 사전 숨김 및 플리커(깜박임) 로직을 관리합니다.*

## at.js 호환성

다음 표에서는 다양한 활동 유형, 통합, 기능 및 at.js 함수와의 at.js 2.0.0 호환성에 대해 설명합니다.

### 활동 유형 {#types}

| 유형 | 지원됨? |
| --- | --- |
| A/B 테스트 | 예 |
| 자동 할당 | 예 |
| 자동 타겟 | 예 |
| 경험 타깃팅 | 예 |
| 다변량 테스트 | 예 |
| 자동화된 개인화 | 예 |
| 권장 사항 | 예 |

>[!NOTE]
>
>Auto-Target activities are supported through at.js 2.*x* and the VEC when all modifications are applied to the `Page Load Event`. 수정 사항이 특정 보기에 추가되면 A/B 테스트, 자동 할당 및 XT(경험 타깃팅) 활동만 지원됩니다.

### 통합 {#integrations}

| 유형 | 지원됨? |
| --- | --- |
| Analytics for Target (A4T) | 예 |
| 대상자 | 예 |
| 고객 속성 | 예 |
| AEM 경험 구성요소 | 예 |
| Adobe Launch 확장 프로그램 | [예](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) |
| 디버거 | 예 |
| Auditor | Rules have not yet been updated for at.js 2.*x* |
| DTM(다이내믹 태그 관리자) | 예 |
| 옵트인 | 아니오. [GDPR](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)에 대한 옵트인 지원은 [at.js 버전 2.1.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)에서 지원됩니다. |
| Adobe Target에서 제공하는 AEM 고급 개인화 | 아니오 |

### 기능

| 기능 | 지원됨? |
| --- | --- |
| X-Domain | 아니오 |
| 속성/작업 공간 | 예 |
| QA 링크 | 예 |
| 양식 기반 경험 작성기 | 예 |
| 시각적 경험 작성기(VEC) | 예 |
| 사용자 지정 코드 | 예 |
| 응답 토큰 | [예](#response-tokens) |
| 클릭 추적 | 예 |
| 여러 활동 전달 | 예 |
| targetGlobalSettings | 예(하지만 x-domain은 아님) |
| at.js 메서드 | 기본 콘텐츠를 표시하는<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>을 제외하고 모든 메서드가 지원됩니다. |

### 쿼리 문자열 매개 변수

| 매개 변수 | 지원됨? |
| --- | --- |
| `?mboxDisable` | 예 |
| `?mboxDisable` | 예 |
| `?mboxTrace` | 예 |
| `?mboxSession` | 아니오 |
| `?mboxOverride.browserIp` | 아니오 |

## 응답 토큰 {#response-tokens}

at.js 2.*x*&#x200B;는 at.js 1.*x*&#x200B;와 마찬가지로 사용자 지정 이벤트 `at-request-succeeded`를 사용하여 응답 토큰을 표시합니다. `at-request-succeeded` 사용자 지정 이벤트를 사용한 코드 예에 대해서는 [응답 토큰](/help/administrating-target/response-tokens.md)을 참조하십시오.

## at.js 1.*x* 매개 변수를 at.js 2에 연결합니다.*x* 페이로드 매핑 {#payload-mapping}

이 섹션에서는 at.js 1.*x* 및 at.js 2.*x*.

매개 변수 매핑을 찾기 전에 이러한 라이브러리 버전에서 사용 중인 엔드포인트가 다음과 같이 변경되었습니다.

* at.js 1.*x* - `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* at.js 2.*x* - `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

또 다른 중요한 차이점은 다음과 같습니다.

* at.js 1.*x* - 클라이언트 코드가 경로의 일부입니다.
* at.js 2.*x* - Client code is sent as a query string parameter, such as:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

다음 섹션에는 at.js 1.*x* 매개 변수, 설명 및 해당 2.0.0 JSON 페이로드(해당되는 경우)가 각각 나열되어 있습니다.

### at_property

(at.js 1.*x* 매개 변수)

[엔터프라이즈 사용자 권한](/help/administrating-target/c-user-management/property-channel/property-channel.md)에 사용됩니다.

```
{
  ....
  "property": {
    "token": "1213213123122313121"
  }
  ....
}
```

### browserHeight

(at.js 1.*x* 매개 변수)

방문자의 브라우저 창 높이입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "window": {
       "height": 200
    }
  }
}
```

### browserWidth

(at.js 1.*x* 매개 변수)

방문자의 브라우저 창 폭입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "window": {
       "width": 200
    }
  }
}
```

### browserTimeOffset

(at.js 1.*x* 매개 변수)

시간대 오프셋입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "timeOffsetInMinutes": -480
  }
}
```

### screenHeight

(at.js 1.*x* 매개 변수)

방문자의 화면 높이입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "screen": {
       "height": 200
    }
  }
}
```

### screenWidth

(at.js 1.*x* 매개 변수)

방문자의 화면 폭입니다.

at.js 2.*x* JSON payload:

```
{
  "context": {
    "screen": {
       "width": 200
    }
  }
}
```

### colorDepth

(at.js 1.*x* 매개 변수)

방문자의 화면 색상 깊이입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "screen": {
       "colorDepth": 24
    }
  }
}
```

### mboxHost

(at.js 1.*x* 매개 변수)

Target 라이브러리가 실행되는 페이지의 도메인입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "browser": {
       "host": "test.com"
    }
  }
}
```

### webGLRenderer

(at.js 1.*x* 매개 변수)

브라우저의 WEB GL 렌더러 기능입니다. 장치 탐지 메커니즘에서 방문자의 장치가 데스크탑, iPhone, Android 장치 등인지 판별하는 데 사용됩니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "browser": {
       "webGLRenderer": "AMD Radeon Pro 560X OpenGL Engine"
    }
  }
}
```

### mboxURL

(at.js 1.*x* 매개 변수)

페이지 URL입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "address": {
       "url": "http://test.com"
    }
  }
}
```

### mboxReferrer

(at.js 1.*x* 매개 변수)

페이지 레퍼러입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "context": {
    "address": {
       "referringUrl": "http://google.com"
    }
  }
}
```

### mbox (the name) equals to global mbox

(at.js 1.*x* 매개 변수)

배달 API에는 더 이상 글로벌 mbox 개념이 없습니다. JSON 페이로드에서 `execute > pageLoad`를 사용해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "execute": {
    "pageLoad": {
       "parameters": ....
       "profileParameters": ...
       .....
    }
  }
}
```

### mbox (the name) is *not* equal to global mbox

(at.js 1.*x* 매개 변수)

mbox 이름을 사용하려면 `execute > mboxes`에 전달합니다. mbox에는 인덱스와 이름이 필요합니다.

at.js 2.*x* JSON payload:

```
{
  "execute": {
    "mboxes": [{
       "index": 0,
       "name": "some-mbox",
       "parameters": ....
       "profileParameters": ...
       .....
    }]
  }
}
```

### mboxId

(at.js 1.*x* 매개 변수)

더 이상 사용되지 않습니다.

### mboxCount

(at.js 1.*x* 매개 변수)

더 이상 사용되지 않습니다.

### mboxRid

(at.js 1.*x* 매개 변수)

디버깅을 지원하기 위해 다운스트림 시스템에서 사용한 요청 ID입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "requestId": "2412234442342"
  ....
}
```

### mboxTime

(at.js 1.*x* 매개 변수)

더 이상 사용되지 않습니다.

### mboxSession

(at.js 1.*x* 매개 변수)

세션 ID가 배달 API 엔드포인트에 쿼리 문자열 매개 변수(`sessionId`)로 전송됩니다.

### mboxPC

(at.js 1.*x* 매개 변수)

TNT ID가 `id > tntId`에 전달됩니다.

at.js 2.*x* JSON 페이로드:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(at.js 1.*x* 매개 변수)

Marketing Cloud 방문자 ID가 `id > marketingCloudVisitorId`에 전달됩니다.

at.js 2.*x* JSON 페이로드:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### `vst.aaaa.id` 및 `vst.aaaa.authState`

(at.js 1.*x* 매개 변수)

고객 ID를 `id > customerIds`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "id": {
    "customerIds": [{
       "id": "1232131",
       "integrationCode": "aaaa",
       "authenticatedState": "....."
     }]
  }
  ....
}
```

### mbox3rdPartyId

(at.js 1.*x* 매개 변수)

다른 Target ID를 연결하는 데 사용된 고객 타사 ID입니다.

at.js 2.*x* JSON 페이로드:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### mboxMCSDID

(at.js 1.*x* 매개 변수)

SDID(보충 데이터 ID)라고도 합니다. `experienceCloud > analytics > supplementalDataId`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "experienceCloud": {
    "analytics": {
      "supplementalDataId": "1212321132123131"
    }
  }
  ....
}
```

### vst.trk

(at.js 1.*x* 매개 변수)

Analytics 추적 서버입니다. `experienceCloud > analytics > trackingServer`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServer": "analytics.test.com"
    }
  }
  ....
}
```

### vst.trks

(at.js 1.*x* 매개 변수)

Analytics 추적 서버가 안전합니다. `experienceCloud > analytics > trackingServerSecure`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServerSecure": "secure-analytics.test.com"
    }
  }
  ....
}
```

### mboxMCGLH

(at.js 1.*x* 매개 변수)

Audience Manager 위치 힌트입니다. `experienceCloud > audienceManager > locationHint`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "experienceCloud": {
    "audienceManager": {
      "locationHint": 9
    }
  }
  ....
}
```

### mboxAAMB

(at.js 1.*x* 매개 변수)

Audience Manager Blob입니다. `experienceCloud > audienceManager > blob`에 전달해야 합니다.

at.js 2.*x* JSON 페이로드:

```
{
  "experienceCloud": {
    "audienceManager": {
      "blob": "2142342343242342"
    }
  }
  ....
}
```

### mboxVersion

(at.js 1.*x* 매개 변수)

버전은 버전 매개 변수를 통해 쿼리 문자열 매개 변수로 전송됩니다.

## Training video: at.js 2.*x* architectural diagram

at.js 2.*x는 SPA에 대한 Adobe Target의 지원을 개선하고 다른 Experience Cloud 솔루션과 통합됩니다.* 다음 비디오에서는 모든 것이 어떻게 합쳐지는지 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/26250?captions=kor)

at. [js 2의 사용 방법 이해를 참조하십시오.*x는* 자세한 정보를 위해 작동합니다](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) .