---
keywords: 응답 토큰;토큰;플러그인;플러그인;at.js;응답
description: '디버깅 및 타사 시스템(예: Clicktale)과의 통합에 사용하기 위해 Adobe [!DNL Target] 출력 관련 정보에 응답 토큰을 사용하는 방법을 알아봅니다.'
title: 응답 토큰이란 무엇이며 어떻게 사용합니까?
feature: 관리 및 구성
role: Administrator
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: d1579a56e46b806c3e4a0cb1748e5682b0900d11
workflow-type: tm+mt
source-wordcount: '1598'
ht-degree: 27%

---

# 응답 토큰

응답 토큰을 사용하면 [!DNL Adobe Target]에 관련된 정보를 브랜드의 웹 페이지에 자동으로 출력할 수 있습니다. 이 정보에는 활동, 오퍼, 경험, 사용자 프로필, 지역 정보 등에 대한 세부 사항이 포함될 수 있습니다. 이러한 세부 사항은 내부 또는 타사 도구와 공유하거나 디버깅에 사용할 추가 응답 데이터를 제공합니다.

응답 토큰을 사용하면 사용할 변수(키 값 쌍)를 선택한 다음 [!DNL Target] 응답의 일부로 전송할 수 있습니다. 스위치를 사용하여 변수를 활성화하면 [!DNL Target] 응답으로 변수가 전송되며, 이 응답은 네트워크 호출에서 확인할 수 있습니다. 응답 토큰은 [!UICONTROL 미리 보기] 모드에서도 작동합니다.

플러그인과 응답 토큰 간의 주요 차이점은 플러그인이 전달 시 실행되는 페이지에 JavaScript를 전달한다는 것입니다. 그러나 응답 토큰은 이벤트 리스너를 사용하여 읽고 작업할 수 있는 개체를 전달합니다. 응답 토큰 접근 방식은 더 안전하며 타사 통합을 보다 쉽게 개발하고 유지 관리할 수 있도록 해줍니다.

>[!NOTE]
>
>응답 토큰은 [!DNL Adobe Experience Platform Web SDK] 버전 2.5.0 이상(2021년 6월 1일에 릴리스됨)과 at.js 버전 1.1 이상에서 사용할 수 있습니다.

| Target SDK | 제안된 작업 |
|--- |--- |
| [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) | Platform Web SDK 버전 2.5.0 이상을 사용 중인지 확인하십시오. 최신 버전의 Platform Web SDK를 다운로드하는 방법에 대한 자세한 내용은 *Platform Web SDK 개요* 안내서의 [SDK 설치](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html)를 참조하십시오. 각 Platform Web SDK 버전의 새로운 기능에 대한 내용은 *Platform Web SDK 개요* 안내서의 [릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html)를 참조하십시오. |
| [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | at.js 버전 1.1 이상을 사용 중인지 확인하십시오. 최신 버전의 at.js를 다운로드하는 방법에 대해서는 [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)를 참조하십시오. 각 at.js 버전의 새로운 기능에 대한 내용은 [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 참조하십시오.<br>at.js를 사용하는 고객은 응답 토큰을 사용하고 플러그인을 사용하지 않는 것이 좋습니다. mbox.js에는 존재하지만 at.js에는 존재하지 않는 내부 메서드에 의존하는 일부 플러그인이 전달되지만 실패합니다. 자세한 내용은 [at.js 제한 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md)을 참조하십시오. |

## 응답 토큰 사용 {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Platform Web SDK 버전 2.5.0 이상 또는 at.js 버전 1.1 이상을 사용 중인지 확인하십시오.

   자세한 내용을 확인하십시오:

   * **Platform 웹 SDK**:플랫폼  [웹 SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) 개요 안내서에서  *SDK* 설치 를 참조하십시오.
   * **at.js**:at. [js 다운로드](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2)를 참조하십시오 .

1. [!DNL Target]에서 **[!UICONTROL 관리]** > **[!UICONTROL 응답 토큰]**&#x200B;을 클릭합니다.

   ![](assets/response_tokens-new.png)

1. `activity.id` 및 `option.id` 등의 원하는 응답 토큰을 활성화합니다.

   기본적으로 다음 매개 변수를 사용할 수 있습니다.

   | 유형 | 매개 변수 | 참고 |
   |--- |--- |--- |
   | 내장 프로필 | `profile.activeActivities` | 방문자가 자격을 갖는 일련의 `activityIds`를 반환합니다. 사용자가 자격을 갖게 됨에 따라 증가합니다. 예를 들어, 두 개의 [!DNL Target] 요청이 있는 페이지에서 두 번째 요청에는 두 개의 활동이 모두 포함됩니다. |
   |  | `profile.isFirstSession` | &quot;true&quot; 또는 &quot;false&quot;를 반환합니다. |
   |  | `profile.isNewSession` | &quot;true&quot; 또는 &quot;false&quot;를 반환합니다. |
   |  | `profile.daysSinceLastVisit` | 방문자가 마지막으로 방문한 이후 경과한 일수를 반환합니다. |
   |  | `profile.tntId` | 방문자의 tntID를 반환합니다. |
   |  | `profile.marketingCloudVisitorId` | 방문자의 Experience Cloud 방문자 ID를 반환합니다. |
   |  | `profile.thirdPartyId` | 방문자의 타사 ID를 반환합니다. |
   |  | `profile.categoryAffinity` | 방문자가 즐겨 찾는 카테고리를 반환합니다. |
   |  | `profile.categoryAffinities` | 방문자의 상위 5개 카테고리의 배열을 문자열로 반환합니다. |
   | 활동 | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`option.name`<br>`option.id` | 현재 활동의 세부 사항입니다. &quot;option&quot;은 &quot;offer&quot;와 같습니다. |
   | 지역 | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | 활동에서 지역 기반의 타깃팅을 사용하는 방법에 대한 자세한 내용은 [지역](/help/c-target/c-audiences/c-target-rules/geo.md)을 참조하십시오. |
   | 트래픽 할당 방법<br>([!UICONTROL 자동 Target] 및 [!UICONTROL Automated Personalization] 활동에만 적용) | `experience.trafficAllocationId` | 방문자가 &quot;제어&quot; 트래픽에서 경험을 받은 경우 0을 반환하고, 방문자가 &quot;타깃팅된&quot; 트래픽 배포에서 경험을 받은 경우 1을 반환합니다. |
   |  | `experience.trafficAllocationType` | &quot;control&quot; 또는 &quot;targeted&quot;를 반환합니다. |

   사용자 프로필 속성 및 고객 속성도 목록에 표시됩니다.

   >[!NOTE]
   >
   >특수 문자가 있는 매개 변수는 목록에 표시되지 않습니다. 영숫자 문자 및 밑줄만 지원됩니다.

1. (조건부) 프로필 매개 변수를 응답 토큰으로 사용하려면 매개 변수가 [!DNL Target] 요청을 통해 전달되지 않았으므로 [!DNL Target] UI에 로드되지 않았으므로 [!UICONTROL 응답 토큰 추가] 단추를 사용하여 프로필을 UI에 추가할 수 있습니다.

   **[!UICONTROL 응답 토큰 추가]**&#x200B;를 클릭하고 토큰 이름을 제공한 다음 **[!UICONTROL 활성화]**&#x200B;를 클릭하십시오.

   ![](assets/response_token_create.png)

1. 활동을 만듭니다.

## 응답 수신 및 응답 토큰 읽기

[!DNL Target] 응답을 수신하는 데 사용하는 프로세스와 응답 토큰 읽기 프로세스는 [!DNL Platform Web SDK] 구현이 있는지 여부에 따라 다릅니다.

### ![Handle 개체 클래스](/help/assets/platform.png) [!DNL Platform Web SDK] 를 사용하는 Adobe Experience Platform Web SDK 배지

메타데이터 개체와 데이터 개체가 있는 Handle 개체 클래스를 사용하여 [!DNL Target] 응답을 수신하고 응답 토큰을 읽습니다.

다음 코드 샘플은 [!DNL Platform Web SDK] 사용자 지정 이벤트 핸들러를 HTML 페이지에 바로 추가합니다.

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

| 개체 | 정보 |
| --- | --- |
| 유형 - Personalization.decision | [!DNL Target] 그리고 Offer decisioning 데이터가 여기에 전달됩니다. |
| 의사 결정 공급자 - TGT | TGT-[!DNL Target]. [!DNL Target] 페이지에 응답 토큰 메타데이터 및 값을 제공합니다. |
| 메타 | 페이지에 전달되는 메타데이터. |
| 데이터 | 페이지에 전달된 메타 데이터 값입니다. |

### ![사용자 지정 ](/help/assets/atjs.png) 이벤트를 사용하는 at.js badgeat.js

[at.js 사용자 지정 이벤트](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md)를 사용하여 응답을 수신하고 응답 토큰을 읽습니다.[!DNL Target]

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

응답 토큰은 [!DNL Target] [!UICONTROL 관리자] 역할을 가진 사용자만 활성화하거나 비활성화할 수 있습니다.

**[!DNL Platform Web SDK] 2.5.0(또는 이전 버전)을 실행 중이면 어떻게 됩니까?

응답 토큰에 액세스할 수 없습니다.

**at.js 1.0(또는 이전 버전)을 실행 중이면 어떻게 됩니까?**

응답 토큰이 표시되지만 at.js는 응답 토큰을 사용할 수 없습니다.

**[!DNL Target Classic] 플러그인과 응답 토큰이 동시에 활성화될 수 있습니까?**

플러그인 및 응답 토큰을 동시에 사용할 수 있습니다.그러나 플러그인은 향후에 더 이상 사용되지 않습니다.

**응답 토큰이 모든  [!DNL Target] 응답을 통해 전달됩니까, 아니면 활동을  [!DNL Target] 전달하는 응답만 통해 전달됩니까?**

응답 토큰은 활동을 전달하는 [!DNL Target] 응답을 통해서만 전달됩니다.

**내  [!DNL Target Classic] 플러그인이 JavaScript를 포함했습니다. 응답 토큰을 사용하여 해당 기능을 복제하려면 어떻게 해야 합니까?**

응답 토큰으로 마이그레이션할 때 이러한 유형의 JavaScript를 코드 베이스 또는 태그 관리 솔루션에 유지해야 합니다. [!DNL Platform Web SDK] 또는 [!DNL at.js] 사용자 지정 이벤트를 사용하여 이 코드를 트리거하고 응답 토큰 값을 JavaScript 함수에 전달할 수 있습니다.

**내 프로필/고객 속성 매개 변수가 응답 토큰 목록에 표시되지 않는 이유는 무엇입니까?**

[!DNL Target] 일반적으로 매개 변수는 15분마다 새로 고침됩니다. 이 새로 고침은 사용자 작업에 따라 달라지며 응답 토큰 페이지를 볼 때만 데이터가 새로 고쳐집니다. 매개 변수가 응답 토큰 목록에 표시되지 않으면 [!DNL Target]에서 아직 데이터를 새로 고치지 않았습니다.

또한 매개 변수에 영숫자가 아닌 문자 또는 밑줄이 아닌 기호가 포함되어 있는 경우 매개 변수가 목록에 표시되지 않습니다. 현재 영숫자와 밑줄 문자만 지원됩니다.

**삭제된 프로필 스크립트나 프로필 매개 변수를 사용하는 경우 응답 토큰이 여전히 콘텐츠를 전달합니까?**

응답 토큰은 사용자 프로필에서 정보를 추출한 후에 전달합니다. 프로필 스크립트 또는 매개 변수를 삭제해도 사용자 프로필에서 해당 정보가 제거되지 않습니다. 사용자 프로필에는 여전히 프로필 스크립트에 해당하는 데이터가 있습니다. 응답 토큰은 컨텐츠를 계속 전달합니다. 프로필에 해당 정보가 저장되지 않은 사용자 또는 새 방문자의 경우 데이터가 프로필에 없으므로 해당 토큰이 전달되지 않습니다.

[!DNL Target] 은 토큰을 자동으로 끄지 않습니다. 프로필 스크립트를 삭제하고 토큰을 더 이상 전달하지 않으려면 토큰을 직접 해제해야 합니다.

**프로필 스크립트의 이름을 바꾸었는데 해당 스크립트를 사용하는 토큰이 여전히 이전 이름으로 활성 상태인 이유는 무엇입니까?**

위에서 언급한 대로 응답 토큰은 사용자에 따라 저장된 프로필 정보에 적용됩니다. 프로필 스크립트 이름을 변경했지만 웹 사이트를 방문한 사용자는 이전 프로필 스크립트 값이 프로필에 저장됩니다. 토큰은 사용자 프로필에 이미 저장된 이전 값을 계속 선택합니다. 이제 새 이름으로 컨텐츠를 전달하려면 이전 토큰을 해제하고 새 토큰을 설정해야 합니다.

**내 특성이 변경된 경우 언제 목록에서 제거됩니까?**

[!DNL Target] 정기적으로 속성 새로 고침을 수행합니다. 전환되지 않은 속성은 다음 새로 고침 중에 제거됩니다. 그러나 이 설정되고 제거된 속성이 있는 경우 이 스크립트를 해제하기 전까지 해당 스크립트가 속성 목록에서 제거되지 않습니다. 예를 들어 토큰으로 사용된 프로필 스크립트를 제거했습니다. [!DNL Target] 가 삭제되거나 이름이 바뀐 경우 목록에서 전환된 속성만 제거합니다.

## Google Analytics으로 데이터 보내기

다음 섹션에서는 [!DNL Target] 데이터를 Google Analytics에게 전송하는 방법에 대해 설명합니다.

### ![AEP ](/help/assets/platform.png) 배지: Platform Web SDK를 통해 Google Analytics에 데이터 보내기

Google Analytics은 HTML 페이지에 다음 코드를 추가하여 Platform Web SDK 버전 2.5.0 이상을 통해 데이터를 전송할 수 있습니다.

(코드 입력)

### ![at.js ](/help/assets/atjs.png) 배지: at.js를 통해 Google Analytics에 데이터 보내기 {#section_04AA830826D94D4EBEC741B7C4F86156}

at.js를 통해 HTML 페이지에 다음 코드를 추가하여 Google 애널리틱스에 데이터를 전송할 수 있습니다.

```javascript
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
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
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
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

다음 섹션에서는 디버깅 응답 토큰에 대한 정보를 제공합니다.

### ![at.js ](/help/assets/atjs.png) 배지Google Analytics 및 디버깅

다음 코드를 사용하면 Google Analytics을 사용하여 디버깅할 수 있습니다.

```javascript
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
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
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
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
        'OfferId': token["option.id"], 
        'OfferName': token["option.name"], 
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

## ![at.](/help/assets/atjs.png) js 교육 비디오:응답 토큰 및 at.js 사용자 지정 이벤트 {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

다음 비디오에서는 응답 토큰 및 at.js 사용자 지정 이벤트를 사용하여 [!DNL Target]에서 타사 시스템으로 프로필 정보를 공유하는 방법을 설명합니다.

>[!NOTE]
>
>[!DNL Target] [!UICONTROL 관리] 메뉴 UI(이전의 [!UICONTROL 설정])가 향상된 성능을 제공하고, 새 기능을 릴리스할 때 필요한 유지 관리 시간을 줄이고, 제품 전반에서 사용자 경험을 개선하기 위해 다시 디자인되었습니다. 다음 비디오의 정보가 올바릅니다.그러나 옵션은 약간 다른 위치에 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
