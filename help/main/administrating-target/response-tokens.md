---
keywords: 응답 토큰;토큰;플러그인;플러그인;at.js;응답;platform web sdk;google analytics
description: 디버깅하고 타사 도구와 통합하기 위해  [!DNL Adobe Target] 에서 응답 토큰을 사용하여 특정 정보를 출력하는 방법에 대해 알아봅니다.
title: 응답 토큰이란 무엇이며 어떻게 사용해야 합니까?
feature: Administration & Configuration
role: Admin
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 24%

---

# 응답 토큰

응답 토큰을 사용하면 [!DNL Adobe Target]과(와) 관련된 정보를 브랜드 웹 페이지에 자동으로 출력할 수 있습니다. 이 정보에는 활동, 오퍼, 경험, 사용자 프로필, 지역 정보 등에 대한 세부 사항이 포함될 수 있습니다. 이러한 세부 정보는 내부 또는 타사 도구와 공유하거나 디버깅에 사용할 추가 응답 데이터를 제공합니다.

응답 토큰을 사용하면 사용할 변수(키 값 쌍)를 선택한 다음 [!DNL Target] 응답의 일부로 전송할 수 있습니다. 스위치를 사용하여 변수를 활성화하면 [!DNL Target] 응답이 있는 상태로 변수가 전송되며, 이 응답은 네트워크 호출에서 확인할 수 있습니다. 응답 토큰은 [!UICONTROL Preview] 모드에서도 작동합니다.

플러그인과 응답 토큰 간의 주요 차이점은 플러그인이 전달 시 실행되는 페이지에 JavaScript을 전달한다는 것입니다. 그러나 응답 토큰은 이벤트 리스너를 사용할 때 읽고 작용할 수 있는 개체를 전달합니다. 응답 토큰 접근 방식은 더 안전하며 타사 통합을 보다 쉽게 개발하고 유지 관리할 수 있도록 해줍니다.

{{permissions-update}}

>[!NOTE]
>
>응답 토큰은 at.js 버전 1.1 이상에서 사용할 수 있습니다.

| Target SDK | 제안된 작업 |
|--- |--- |
| [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} | Platform Web SDK 버전 2.6.0 이상을 사용 중인지 확인하십시오. 최신 버전의 Platform Web SDK을 다운로드하는 방법에 대한 자세한 내용은 [Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html){target=_blank} 안내서에서 *SDK 설치*&#x200B;를 참조하십시오. Platform Web SDK의 각 버전에 대한 새로운 기능은 [Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html) 안내서의 *릴리스 정보*&#x200B;를 참조하십시오. |
| [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} | at.js 버전 1.1 이상을 사용 중인지 확인하십시오. 최신 버전의 at.js를 다운로드하는 방법에 대해서는 [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=en){target=_blank}를 참조하십시오. 각 at.js 버전의 새로운 기능에 대한 내용은 [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}을 참조하십시오.<br>at.js를 사용하는 고객은 응답 토큰을 사용하고 플러그인을 사용하지 않는 것이 좋습니다. mbox.js(사용 중단됨)에는 존재했지만 at.js에는 존재하지 않는 내부 메서드에 의존하는 일부 플러그인은 전달되지만 실패합니다. |

## 응답 토큰 사용 {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Platform Web SDK 버전 2.6.0 이상 또는 at.js 버전 1.1 이상을 사용 중인지 확인하십시오.

   추가 정보:

   * **Platform Web SDK**: [Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) 안내서의 *SDK 설치*&#x200B;를 참조하십시오.
   * **at.js**: [at.js 다운로드](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html){target=_blank}를 참조하십시오.

1. [!DNL Target]에서 **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**&#x200B;을(를) 클릭합니다.

1. `activity.id` 및 `offer.id`과(와) 같이 원하는 응답 토큰을 활성화합니다.

   기본적으로 다음 매개 변수를 사용할 수 있습니다.

   | 유형 | 매개 변수 | 참고 |
   |--- |--- |--- |
   | 기본 제공 프로필 | `profile.activeActivities` | 방문자가 자격을 갖는 일련의 `activityIds`를 반환합니다. 사용자가 자격을 갖게 됨에 따라 증가합니다. 예를 들어, 두 개의 서로 다른 활동을 전달하는 두 개의 [!DNL Target] 요청이 있는 페이지에서 두 번째 요청에는 두 활동이 모두 포함됩니다. |
   |  | `profile.isFirstSession` | &quot;true&quot; 또는 &quot;false&quot;를 반환합니다. |
   |  | `profile.isNewSession` | &quot;true&quot; 또는 &quot;false&quot;를 반환합니다. |
   |  | `profile.daysSinceLastVisit` | 방문자가 마지막으로 방문한 이후 경과한 일수를 반환합니다. |
   |  | `profile.tntId` | 방문자의 tntID를 반환합니다. |
   |  | `profile.marketingCloudVisitorId` | 방문자의 Experience Cloud 방문자 ID를 반환합니다. |
   |  | `profile.thirdPartyId` | 방문자의 타사 ID를 반환합니다. |
   |  | `profile.categoryAffinity` | 방문자가 즐겨 찾는 카테고리를 반환합니다. |
   |  | `profile.categoryAffinities` | 방문자의 상위 5개 카테고리의 배열을 문자열로 반환합니다. |
   | 활동 | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`offer.name`<br>`offer.id` | 현재 활동의 세부 정보.<br> 오퍼 매개 변수의 값은 경험 수준에서 평가됩니다. |
   | 지역 | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | 활동에서 지역 기반의 타깃팅을 사용하는 방법에 대한 자세한 내용은 [지역](/help/main/c-target/c-audiences/c-target-rules/geo.md)을 참조하십시오. |
   | 트래픽 할당 메서드 <br>([!UICONTROL Auto-Target] 및 [!UICONTROL Automated Personalization] 활동에만 적용) | `experience.trafficAllocationId` | 방문자가 &quot;제어&quot; 트래픽에서 경험을 받은 경우 0을 반환하고, 방문자가 &quot;대상&quot; 트래픽 분배에서 경험을 받은 경우 1을 반환합니다. |
   |  | `experience.trafficAllocationType` | &quot;제어&quot; 또는 &quot;타깃팅&quot;을 반환합니다. |

   사용자 프로필 속성 및 고객 속성도 목록에 표시됩니다.

   >[!NOTE]
   >
   >특수 문자가 있는 매개 변수는 목록에 표시되지 않습니다. 영숫자 문자 및 밑줄만 지원됩니다.

1. (조건부) 프로필 매개 변수를 응답 토큰으로 사용하지만 매개 변수가 [!DNL Target] 요청을 통해 전달되지 않아 [!DNL Target] UI에 로드되지 않은 경우 [!UICONTROL Add Response Token] 단추를 사용하여 프로필을 UI에 추가할 수 있습니다.

   **[!UICONTROL Add Response Token]**&#x200B;을(를) 클릭하고 토큰 이름을 입력한 다음 **[!UICONTROL Activate]**&#x200B;을(를) 클릭합니다.

1. 활동을 만듭니다.

## 응답 수신 및 응답 토큰 읽기

[!DNL Target] 응답을 수신하고 응답 토큰을 읽는 데 사용하는 프로세스는 [!DNL Platform Web SDK] 또는 at.js 구현의 여부에 따라 다릅니다.

### Handle 개체 클래스를 사용하는 ![Adobe Experience Platform Web SDK 배지](/help/main/assets/platform.png) [!DNL Platform Web SDK] {#platform-web-sdk}

메타데이터 개체와 데이터 개체가 있는 Handle 개체 클래스를 사용하여 [!DNL Target] 응답을 수신하고 응답 토큰을 읽습니다.

다음 응답 예제에서는 [!DNL Platform Web SDK] 사용자 지정 이벤트 처리기를 HTML 페이지에 바로 추가합니다(표에서는 코드에 사용되는 개체에 대해 설명합니다).

| 개체 | 정보 |
| --- | --- |
| 유형 - Personalization.decision | [!DNL Target] 또는 Offer Decisioning 공급자가 결정했는지 여부. |
| DecisionProvider - TGT | TGT-[!DNL Target]. [!DNL Target]이(가) 응답 토큰 메타데이터와 값을 페이지에 제공합니다. |
| 메타 | 페이지에 전달되는 메타데이터입니다. |
| 데이터 | 페이지에 전달된 메타데이터의 값입니다. |

```html
<html>

<head>
 ...
 <script src="alloy.js"></script>
 <script>
  {
   "requestId": "4d0a7cfd-952c-408c-b3b8-438edc38250a",
   "handle": [{
    "type": "personalization:decisions",
    "payload": [{
     "id": "....",
     "scope": "__view__",
     "scopeDetails": {
      "decisionProvider": "TGT",
      "activity": {
       "id": "..."
      },
      "experience": {
       "id": "...."
      }
     },
     "items": [{
      "id": "123",
      "schema": "https://ns.adobe.com/personalization/dom-action",
      "meta": {
       "activity.id": "...",
       "activity.name": "...",
       "profile.foo": "...",
       "profile.bar": "..."
      },
      "data": {
       "id": "123",
       "type": "setHtml",
       "selector": "#foo",
       "prehidingSelector": "#foo",
       "content": "<div>Hello world</div>"
      }
     }]
    }]
   }]
  }
  });
 </script>
</head>

<body>
 ...
</body>

</html>
```

### 사용자 지정 이벤트를 사용하는 ![at.js 배지](/help/main/assets/atjs.png) at.js

[at.js 사용자 지정 이벤트](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-custom-events.html?lang=en){target=_blank}를 사용하여 [!DNL Target] 응답을 수신하고 응답 토큰을 읽습니다.

다음 코드 샘플은 [!DNL at.js] 사용자 지정 이벤트 핸들러를 HTML 페이지에 바로 추가합니다.

```html
<html> 
  <head> 
    .... 
    <script src="at.js"></script> 
    <script> 
      document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
        console.log("Request succeeded", e.detail); 
      }); 
    </script> 
  <head> 
  <body> 
  ... 
  </body> 
</html>
```

## 응답 토큰 FAQ {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**응답 토큰을 활성화하거나 비활성화하는 데 필요한 역할은 무엇입니까?**

[!DNL Target] [!UICONTROL Administrator] 역할을 가진 사용자만 응답 토큰을 활성화하거나 비활성화할 수 있습니다.

**실행 중인 [!DNL Platform Web SDK] 2.6.0(또는 이전 버전)의 경우 어떻게 됩니까?**

응답 토큰에 대한 액세스 권한이 없습니다.

**at.js 1.0(또는 이전 버전)을 실행하는 경우 어떻게 됩니까?**

응답 토큰이 표시되지만 at.js는 이를 사용할 수 없습니다.

**[!DNL Target Classic] 플러그인과 응답 토큰을 동시에 활성화할 수 있습니까?**

플러그인과 응답 토큰을 동시에 사용할 수 있습니다. 그러나 플러그인은 향후 더 이상 사용되지 않습니다.

**모든 [!DNL Target] 응답을 통해 응답 토큰이 전달됩니까? 아니면 [!DNL Target] 응답에서만 활동을 전달합니까?**

응답 토큰은 활동을 전달하는 [!DNL Target]개의 응답을 통해서만 전달됩니다.

**내 [!DNL Target Classic] 플러그 인에 JavaScript이 포함되었습니다. 응답 토큰을 사용하여 해당 기능을 복제하려면 어떻게 해야 합니까?**

응답 토큰으로 마이그레이션할 때 이러한 유형의 JavaScript은 코드 베이스 또는 태그 관리 솔루션에 유지되어야 합니다. [!DNL Platform Web SDK] 또는 [!DNL at.js] 사용자 지정 이벤트를 사용하여 이 코드를 트리거하고 응답 토큰 값을 JavaScript 함수에 전달할 수 있습니다.

**내 프로필/고객 속성 매개 변수가 응답 토큰 목록에 표시되지 않는 이유는 무엇입니까?**

[!DNL Target]은(는) 일반적으로 15분마다 매개 변수를 새로 고칩니다. 이 새로 고침은 사용자 작업에 따라 다르며 응답 토큰 페이지를 볼 때만 데이터가 새로 고쳐집니다. 매개 변수가 응답 토큰 목록에 표시되지 않으면 [!DNL Target]에서 데이터를 아직 새로 고치지 않았습니다.

또한 매개 변수에 영숫자가 아닌 문자나 밑줄 이외의 기호가 포함되어 있으면 매개 변수가 목록에 표시되지 않습니다. 현재 영숫자와 밑줄 문자만 지원됩니다.

**응답 토큰이 삭제된 프로필 스크립트나 프로필 매개 변수를 사용하는 경우에도 콘텐츠를 전달합니까?**

응답 토큰은 사용자 프로필에서 정보를 추출한 후에 전달합니다. 프로필 스크립트 또는 매개 변수를 삭제해도 사용자 프로필에서 해당 정보가 제거되지 않습니다. 사용자 프로필에는 프로필 스크립트에 해당하는 데이터가 여전히 있습니다. 응답 토큰은 콘텐츠를 계속 전달합니다. 프로필에 해당 정보가 저장되어 있지 않은 사용자 또는 새 방문자의 경우 데이터가 프로필에 없으므로 해당 토큰이 전달되지 않습니다.

[!DNL Target]은(는) 토큰을 자동으로 해제하지 않습니다. 프로필 스크립트를 삭제하고 토큰을 더 이상 전달하지 않으려면 토큰을 직접 해제해야 합니다.

**프로필 스크립트의 이름을 바꾸었는데 해당 스크립트를 사용하는 토큰이 여전히 이전 이름으로 활성 상태인 이유는 무엇입니까?**

위에서 언급한 대로 응답 토큰은 사용자에 따라 저장된 프로필 정보에 적용됩니다. 프로필 스크립트의 이름을 변경했지만 웹 사이트를 방문한 사용자의 프로필에 이전 프로필 스크립트 값이 저장됩니다. 토큰은 사용자 프로필에 이미 저장된 이전 값을 계속 선택합니다. 이제 새 이름으로 컨텐츠를 전달하려면 이전 토큰을 해제하고 새 토큰을 설정해야 합니다.

**내 특성이 변경된 경우 해당 특성은 언제 목록에서 제거됩니까?**

[!DNL Target]은(는) 정기적으로 특성을 새로 고칩니다. 켜지지 않는 속성은 다음 새로 고침 중에 제거됩니다. 그러나 전환된 속성이 제거되어 있는 경우 해당 스크립트를 해제할 때까지 속성 목록에서 제거되지 않습니다. 예를 들어 토큰으로 사용된 프로필 스크립트를 제거했습니다. [!DNL Target]은(는) 삭제되거나 이름이 바뀌는 경우 목록에서 전환된 속성만 제거합니다.

## Google Analytics으로 데이터 보내기

다음 섹션에서는 [!DNL Target] 데이터를 Google Analytics 4로 보내는 방법을 설명합니다. 응답 토큰으로 전송된 데이터를 다른 타사 통합으로 전송할 수도 있습니다.

### ![AEP 배지](/help/main/assets/platform.png) Platform Web SDK을 통해 Google Analytics으로 데이터 전송

Google Analytics은 HTML 페이지에 다음 코드를 추가하여 Platform Web SDK 버전 2.6.0 이상을 통해 데이터를 보낼 수 있습니다.

>[!NOTE]
>
>응답 토큰 키 값 쌍이 `alloy("sendEvent"` 개체 아래에 있는지 확인하십시오.

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
<script type="text/javascript">
    alloy("sendEvent", {
 
 
    })
    .then(({ renderedPropositions, nonRenderedPropositions }) => {
        // concatenate all the propositions
        const propositions = [...renderedPropositions, ...nonRenderedPropositions];
        // extractResponseTokens() extract the meta from item -> meta
        const tokens = extractResponseTokens(propositions);
        const activityNames = [];
        const experienceNames = [];
        const uniqueTokens = distinct(tokens);
    
    
        uniqueTokens.forEach(token => {
            activityNames.push(token["activity.name"]);
            experienceNames.push(token["experience.name"]);
        });
 
        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
        });
    });
</script>
```

### ![at.js 배지](/help/main/assets/atjs.png) at.js를 통해 Google Analytics에 데이터 전송 {#section_04AA830826D94D4EBEC741B7C4F86156}

at.js를 통해 HTML 페이지에 다음 코드를 추가하여 Google 애널리틱스에 데이터를 전송할 수 있습니다.

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>

<script type="text/javascript">
    document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) {
        var tokens = e.detail.responseTokens;

        if (isEmpty(tokens)) {
            return;
        }

        var activityNames = [];
        var experienceNames = [];
        var uniqueTokens = distinct(tokens);

        uniqueTokens.forEach(function(token) {
            activityNames.push(token["activity.name"]);
            experienceNames.push(token["experience.name"]);
        });

        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
        });
    });

    function isEmpty(val) {
        return (val === undefined || val == null || val.length <= 0) ? true : false;
    }

    function key(obj) {
        return Object.keys(obj)
        .map(function(k) { return k + "" + obj[k]; })
        .join("");
    }

    function distinct(arr) {
        var result = arr.reduce(function(acc, e) {
            acc[key(e)] = e;
            return acc;
        }, {});

        return Object.keys(result)
        .map(function(k) { return result[k]; });
    }
</script>
```

## 디버깅

다음 섹션에서는 응답 토큰 디버깅에 대한 정보를 제공합니다.

### ![at.js 배지](/help/main/assets/atjs.png) Google Analytics 및 디버깅

다음 코드를 사용하면 Google Analytics을 사용하여 디버그할 수 있습니다.

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
  
<script type="text/javascript">
    document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) {
      var tokens = e.detail.responseTokens;
  
      if (isEmpty(tokens)) {
        return;
      }
  
      var activityNames = [];
      var experienceNames = [];
      var uniqueTokens = distinct(tokens);
  
      uniqueTokens.forEach(function(token) {
        activityNames.push(token["activity.name"]);
        experienceNames.push(token["experience.name"]);
      });
  
      gtag('config', 'TAG_ID');
      gtag('event', 'action_name', {'eventCategory': 'target',
          'eventAction': experienceNames, 'eventLabel': activityNames
      });
    });
  
    function isEmpty(val) {
      return (val === undefined || val == null || val.length <= 0) ? true : false;
    }
  
    function key(obj) {
       return Object.keys(obj)
      .map(function(k) { return k + "" + obj[k]; })
      .join("");
    }
  
    function distinct(arr) {
      var result = arr.reduce(function(acc, e) {
        acc[key(e)] = e;
        return acc;
      }, {});
  
      return Object.keys(result)
      .map(function(k) { return result[k]; });
    }
</script>
```

### ttMeta 플러그인과 동등한 기능을 사용하여 디버깅

디버깅 목적의 ttMeta 플러그인과 동등한 기능은 HTML 페이지에 다음 코드를 추가하여 만들 수 있습니다.

```javascript
<script type="text/javascript" > 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function (e) { 
    window.ttMETA= typeof(window.ttMETA)!="undefined" ? window.ttMETA : []; 
 
    var tokens=e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
     
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      window.ttMETA.push({ 
        'CampaignName': token["activity.name"], 
        'CampaignId' : token["activity.id"], 
        'RecipeName': token["experience.name"], 
        'RecipeId': token["experience.id"], 
        'OfferId': token["offer.id"], 
        'OfferName': token["offer.name"], 
        'MboxName': e.detail.mbox}); 
      console.log(ttMETA); 
    }); 
  }); 
 
  function isEmpty(val){ 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## ![at.js](/help/main/assets/atjs.png) 교육 비디오: 응답 토큰 및 at.js 사용자 지정 이벤트 {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

다음 비디오에서는 응답 토큰 및 at.js 사용자 지정 이벤트를 사용하여 [!DNL Target]에서 타사 시스템으로 프로필 정보를 공유하는 방법을 설명합니다.

>[!NOTE]
>
>[!DNL Target] [!UICONTROL Administration] 메뉴 UI(이전 [!UICONTROL Setup])는 향상된 성능을 제공하고, 새로운 기능을 출시할 때 필요한 유지 관리 시간을 줄이고, 제품 전반에 걸쳐 사용자 경험을 개선할 수 있도록 새롭게 디자인되었습니다. 다음 비디오의 정보는 정확하지만 옵션이 약간 다른 위치에 있습니다.
>
>비디오에는 각각 `option.name` 및 `option.id`(으)로 바뀐 `offer.name` 및 `offer.id`이(가) 언급되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
