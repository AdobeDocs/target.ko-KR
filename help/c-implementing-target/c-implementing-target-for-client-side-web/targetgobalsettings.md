---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;global settings;at.js;functions;function;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;selectorsPollingTimeout;dataProviders;Hybrid Personalization
description: Adobe Target at.js JavaScript 라이브러리에 대한 targetGlobalSettings() 함수 정보입니다.
title: Adobe Target at.js JavaScript 라이브러리에 대한 targetGlobalSettings() 함수 정보입니다.
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a24d932f02d49ff11da6299eb46d73f4f385b866
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 63%

---


# targetGlobalSettings()

[!DNL Target] Standard/Premium UI에서 설정을 구성하거나 REST API를 사용하는 대신 `targetGlobalSettings()`를 사용하여 at.js 라이브러리의 설정을 무시할 수 있습니다.

사용 사례로 일부 설정을 재정의하려는 경우, 특히 at.js가 DTM([!DNL Dynamic Tag Management])을 통해 전달되는 경우를 들 수 있습니다.

## 설정{#section_42C759AE9B524A43B8659018677224B8}의 지침을 완료하여 이 설정을 변경할 수 있습니다 

다음 설정을 재정의할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 유형 | 기본값 | 설명 |
|--- |--- |--- |--- |
| serverState | 아래의 &quot;하이브리드 개인화&quot;를 참조하십시오. | 아래의 &quot;하이브리드 개인화&quot;를 참조하십시오. | 아래의 &quot;하이브리드 개인화&quot;를 참조하십시오. |
| clientCode | 문자열 | UI를 통해 설정된 값 | 클라이언트 코드를 나타냅니다. |
| serverDomain | 문자열 | UI를 통해 설정된 값 | Target 에지 서버를 나타냅니다. |
| cookieDomain | 문자열 | 가능한 경우 최상위 수준 도메인으로 설정하십시오. | 쿠키를 저장할 때 사용되는 도메인을 나타냅니다. |
| crossDomain | 문자열 | UI를 통해 설정된 값 | 교차 도메인 추적이 활성화되어 있는지를 나타냅니다.<br>허용되는 값은 다음과 같습니다.<ul><li>비활성화됨</li><li>활성화됨</li><li>x-전용</li></ul> |
| timeout | 숫자 | UI를 통해 설정된 값 | Target 에지 요청 시간 제한을 나타냅니다. |
| globalMboxAutoCreate | 부울 | UI를 통해 설정된 값 | 전역 mbox 요청을 실행해야 하는지를 나타냅니다. |
| visitorApiTimeout | 숫자 | 2000ms = 2s | 방문자 API 요청 시간 제한을 나타냅니다. |
| 활성화됨 | 부울 | true | 활성화되면 경험을 렌더링하기 위한 타겟 요청과 DOM 조작 등이 자동으로 실행됩니다. 또한 Target 호출은 /를 통해 수동으로 실행할 수 있습니다. `getOffer(s)` 비활성화되면 Target `applyOffer(s)`<br>요청이 자동으로 또는 수동으로 실행되지 않습니다 |
| pageLoadEnabled | 부울 | true | 활성화되면 페이지 로드 시 반환해야 하는 경험을 자동으로 검색합니다. |
| viewsEnabled | 부울 | true | 활성화되면 페이지 로드 시 반환해야 하는 뷰를 자동으로 검색합니다. 보기는 at.js 2에서 지원됩니다.*x*&#x200B;에만 사용할 수 있습니다 |
| defaultContentHiddenStyle | 문자열 | 가시성: 숨김 | 기본 컨텐츠를 숨기기 위해 DIV를 클래스 이름 &quot;mboxDefault&quot;와 함께 사용하고 `mboxCreate()`, `mboxUpdate()` 또는 `mboxDefine()`을 통해 실행되는 mbox를 래핑하는 데만 사용됩니다. |
| defaultContentVisibleStyle | 문자열 | 가시성: 표시 | 적용된 오퍼(있는 경우) 또는 기본 컨텐츠를 표시하기 위해 DIV를 클래스 이름 &quot;mboxDefault&quot;와 함께 사용하고 `mboxCreate()`, `mboxUpdate()` 또는 `mboxDefine()`을 통해 실행되는 mbox를 래핑하는 데만 사용됩니다. |
| bodyHiddenStyle | 문자열 | body { opacity: 0 } | 깜박임 가능성을 최소화하기 위해 `globalMboxAutocreate === true`일 때만 사용됩니다.<br>자세한 내용은 [at.js에서 플리커를 관리하는 방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md)을 참조하십시오. |
| bodyHidingEnabled | 부울 | true | `target-global-mbox` 가 시각적 오퍼로도 알려진 시각적 경험 작성기에서 만든 오퍼를 전달하는 데 사용될 때 깜박임을 제어하는 데 사용됩니다. |
| imsOrgId | 문자열 | IMS ORG ID | IMS ORG ID를 나타냅니다. |
| secureOnly | 부울 | false | at.js에서 HTTPS만 사용되는지 또는 페이지 프로토콜을 기준으로 HTTP와 HTTPS 간을 전환할 수 있는지를 나타냅니다. |
| overrideMboxEdgeServer | 부울 | true(at.js 버전 1.6.2부터 true) | `<clientCode>.tt.omtrdc.net` 도메인과 `mboxedge<clusterNumber>.tt.omtrdc.net` 도메인 중에서 어떤 도메인을 사용해야 하는지를 나타냅니다.<br>이 값이 true면 `mboxedge<clusterNumber>.tt.omtrdc.net` 도메인이 쿠키에 저장됩니다.. 현재 CNAME에서 작동하지 [않음](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) |
| overrideMboxEdgeServerTimeout | 숫자 | 1860000 => 31분 | `mboxedge<clusterNumber>.tt.omtrdc.net` 값을 포함하는 쿠키 라이프타임을 나타냅니다. |
| optoutEnabled | 부울 | false | Target이 방문자 API `isOptedOut()` 함수를 호출해야 하는지를 나타냅니다. Device Graph 지원의 일부입니다. |
| selectorsPollingTimeout | 숫자 | 5000ms = 5s | at.js 0.9.6에서 Target은 `targetGlobalSettings`를 통해 재정의할 수 있는 이 새 설정을 도입했습니다.<br>`selectorsPollingTimeout`은 선택기로 식별된 모든 요소가 페이지에 표시되도록 하기 위해 클라이언트가 대기하는 시간을 나타냅니다.<br>VEC(시각적 경험 작성기)를 통해 작성된 활동에는 선택기를 포함하는 오퍼가 있습니다. |
| dataProviders | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. |
| cspScriptNonce | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. |
| cspStyleNonce | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. | 아래의 &quot;콘텐츠 보안 정책&quot;을 참조하십시오. |

## 사용 {#section_9AD6FA3690364F7480C872CB55567FB0}

이 함수는 at.js가 로드되기 전에 또는 **[!UICONTROL 설정]** > **[!UICONTROL 구현]** > **[!UICONTROL at.js 설정 편집]** > **[!UICONTROL 코드 설정]** > **[!UICONTROL 라이브러리 헤더]**&#x200B;에서 정의할 수 있습니다.

라이브러리 헤더 필드에는 자유 형식 JavaScript를 입력할 수 있습니다. 사용자 지정 코드는 다음 예제와 유사해야 합니다.

```
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## 데이터 공급자 {#data-providers}

이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 서드 파티 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다. 비동기 및 동기 요청을 통해 여러 공급자로부터 데이터를 수집하도록 지원합니다. 이 접근 방식을 사용하면 각 공급자에 대해 독립적인 시간 제한을 포함하여 페이지 성능에 미치는 영향을 제한하면서, 기본 페이지 콘텐츠의 깜박임을 쉽게 관리할 수 있습니다

>[!NOTE]
>
>데이터 공급자는 [!DNL at.js] 1.3 이상이 필요합니다.

다음 비디오에는 추가 정보가 포함되어 있습니다.

| 비디오 | 설명 |
|--- |--- |
| [Adobe Target에서 데이터 공급자 사용](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-feature-video-use.html) | 데이터 공급자는 타사의 데이터를 Target에 쉽게 전달할 수 있는 기능입니다. 타사는 기상 서비스, DMP 또는 자체 웹 서비스일 수 있습니다. 그런 다음, 이 데이터를 사용하여 대상, Target 콘텐츠를 작성하고 방문자 프로필을 보강할 수 있습니다. |
| [Adobe Target에서 데이터 공급자 구현](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Adobe Target의 dataProviders 기능을 사용하여 타사 데이터 공급자로부터 데이터를 검색하고 이를 Target 요청에 전달하는 방법에 대한 자세한 내용과 예제에 대한 구현입니다. |

`window.targetGlobalSettings.dataProviders` 설정은 데이터 공급자의 배열입니다.

각 데이터 공급자의 구조는 다음과 같습니다.

| 키 | 유형 | 설명 |
|--- |--- |--- |
| 이름 | 문자열 | 공급자의 이름입니다. |
| version | 문자열 | 공급자 버전입니다. 이 키는 공급자 발전에 사용됩니다. |
| timeout | 숫자 | 네트워크 요청인 경우 공급자 시간 제한을 나타냅니다.  이 키는 선택 사항입니다. |
| provider | 함수 | 공급자 데이터 가져오기 로직을 포함하는 함수입니다.<br>이 함수에는 단일 필수 매개 변수인 `callback`이 있습니다. callback 매개 변수는 데이터를 성공적으로 가져왔거나 오류가 있는 경우에만 호출되어야 하는 함수입니다.<br>콜백에는 다음 두 매개 변수가 필요합니다.<ul><li>error: 오류가 발생했는지를 나타냅니다. 모든 것이 정상이면 이 매개 변수를 null로 설정해야 합니다.</li><li>params: Target 요청에서 보낼 매개 변수를 나타내는 JSON 개체입니다.</li></ul> |

다음 예제에서는 데이터 공급자가 동기화 실행을 사용하는 위치를 보여 줍니다.

```
var syncDataProvider = { 
  name: "simpleDataProvider", 
  version: "1.0.0", 
  provider: function(callback) { 
    callback(null, {t1: 1}); 
  } 
}; 
  
window.targetGlobalSettings = { 
  dataProviders: [ 
    syncDataProvider 
  ] 
};
```

at.js가 `window.targetGlobalSettings.dataProviders`를 처리하면 Target 요청에 새 매개 변수인 `t1=1`이 포함됩니다.

다음은 Target 요청에 추가하려는 매개 변수를 Bluekai, Demandbase 등과 같은 서드 파티 서비스에서 가져오는 경우의 예입니다.

```
var blueKaiDataProvider = { 
   name: "blueKai", 
   version: "1.0.0", 
   provider: function(callback) { 
      // simulating network request 
     setTimeout(function() { 
       callback(null, {t1: 1, t2: 2, t3: 3}); 
     }, 1000); 
   } 
} 
  
window.targetGlobalSettings = { 
   dataProviders: [ 
      blueKaiDataProvider 
   ] 
};
```

at.js가 `window.targetGlobalSettings.dataProviders`를 처리한 후에 Target 요청에는 추가 매개 변수인 `t1=1`, `t2=2` 및 `t3=3`이 포함됩니다.

다음 예제에서는 데이터 공급자를 사용하여 날씨 API 데이터를 수집하고 Target 요청에 매개 변수로 전송합니다. Target 요청에는 `country` 및 `weatherCondition`과 같은 추가 매개 변수가 사용됩니다.

```
var weatherProvider = { 
      name: "weather-api", 
      version: "1.0.0", 
      timeout: 2000, 
      provider: function(callback) { 
        var API_KEY = "caa84fc6f5dc77b6372d2570458b8699"; 
        var lat = 44.426767399999996; 
        var lon = 26.1025384; 
        var url = "//api.openweathermap.org/data/2.5/weather?lang=en"; 
        var data = { 
          lat: lat, 
          lon: lon, 
          appId: API_KEY 
        } 
 
        $.ajax({ 
          type: "GET", 
                url: url, 
          dataType: "json", 
          data: data, 
          success: function(data) { 
            console.log("Weather data", data); 
            callback(null, { 
              country: data.sys.country, 
              weatherCondition: data.weather[0].main 
            }); 
          }, 
          error: function(err) { 
            console.log("Error", err); 
            callback(err); 
          } 
        });         
      } 
    }; 
 
    window.targetGlobalSettings = { 
      dataProviders: [weatherProvider] 
    };
```

`dataProviders` 설정을 사용할 때는 다음 사항을 고려하십시오.

* `window.targetGlobalSettings.dataProviders`에 추가된 데이터 공급자가 비동기 상태인 경우 병렬로 실행됩니다. 방문자 API 요청은 최소 대기 시간을 허용하기 위해 `window.targetGlobalSettings.dataProviders`에 추가된 함수와 함께 실행됩니다.
* at.js는 데이터를 캐시하려고 하지 않습니다. 데이터 공급자는 데이터를 한 번만 가져오는 경우 데이터가 캐시되는지 확인해야 하고, 공급자 함수가 호출될 때 두 번째 호출을 위해 캐시 데이터를 제공해야 합니다.

## Content Security Policy {#content-security}

at.js 2.3.0+는 제공된 Target 오퍼를 적용할 때 페이지 DOM에 첨부된 SCRIPT 및 STYLE 태그에서 Content Security 정책 논점 설정을 지원합니다.

at.js 2.3.0+ 로딩 전에 SCRIPT 및 STYLE 원본을 `targetGlobalSettings.cspScriptNonce` in `targetGlobalSettings.cspStyleNonce` 과 이에 따라 설정해야 합니다. 아래 예를 참조하십시오.

```
...
<head>
 <script nonce="<script_nonce_value>">
window.targetGlobalSettings = {
  cspScriptNonce: "<csp_script_nonce_value>",
  cspStyleNonce: "<csp_style_nonce_value>"
};
 </script>
 <script nonce="<script_nonce_value>" src="at.js"></script>
...
</head>
...
```

이후 `cspScriptNonce` 및 `cspStyleNonce` 설정이 지정되면 at.js 2.3.0+은 이러한 속성을 Target 오퍼를 적용할 때 DOM에 추가되는 모든 SCRIPT 및 STYLE 태그의 한 번 속성으로 설정합니다.

## 하이브리드 개인화 {#server-state}

`serverState` 은 at.js v2.2+에서 사용할 수 있는 설정으로, Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있습니다. 하이브리드 통합은 경험을 제공하기 위해 클라이언트측에서 at.js v2.2+를 사용하고 서버측에서 제공 API 또는 Target SDK를 모두 사용하고 있음을 의미합니다. `serverState` 는 at.js v2.2+를 제공하여 서버 측에서 가져온 컨텐츠에서 직접 경험을 적용하고 제공되는 페이지의 일부로 클라이언트로 돌아오는 기능을 제공합니다.

### 전제 조건

하이브리드 통합 [!DNL Target]이 필요합니다.

* **서버측**:  새 [배달 API](https://developers.adobetarget.com/api/delivery-api/) 또는 [Target SDK를 사용해야 합니다](https://developers.adobetarget.com/api/delivery-api/#section/SDKs).
* **클라이언트측**: at.js 버전 [2.2 이상을 사용해야 합니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### 코드 샘플

이 작동 방식을 보다 잘 이해하려면 아래 코드 예제를 통해 서버에 게시해 주십시오. 이 코드는 사용자가 [Target Node.js SDK를 사용하고 있다고 가정합니다](https://github.com/adobe/target-nodejs-sdk).

```
// First, we fetch the offers via Target Node.js SDK API, as usual
const targetResponse = await targetClient.getOffers(options);
// A successfull response will contain Target Delivery API request and response objects, which we need to set as serverState
const serverState = {
  request: targetResponse.request,
  response: targetResponse.response
};
// Finally, we should set window.targetGlobalSettings.serverState in the returned page, by replacing it in a page template, for example
const PAGE_TEMPLATE = `
<!doctype html>
<html>
<head>
  ...
  <script>
    window.targetGlobalSettings = {
      overrideMboxEdgeServer: true,
      serverState: ${JSON.stringify(serverState, null, " ")}
    };
  </script>
  <script src="at.js"></script>
</head>
...
</html>
`;
// Return PAGE_TEMPLATE to the client ...
```

프리페치 보기를 위한 샘플 `serverState` 개체 JSON은 다음과 같습니다.

```
{
 "request": {
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "context": {
   "channel": "web",
   "timeOffsetInMinutes": 0
  },
  "experienceCloud": {
   "analytics": {
    "logging": "server_side",
    "supplementalDataId": "7D3AA246CC99FD7F-1B3DD2E75595498E"
   }
  },
  "prefetch": {
   "views": [
    {
     "address": {
      "url": "my.testsite.com/"
     }
    }
   ]
  }
 },
 "response": {
  "status": 200,
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "client": "testclient",
  "edgeHost": "mboxedge21.tt.omtrdc.net",
  "prefetch": {
   "views": [
    {
     "name": "home",
     "key": "home",
     "options": [
      {
       "type": "actions",
       "content": [
        {
         "type": "setHtml",
         "selector": "#app > DIV.app-container:eq(0) > DIV.page-container:eq(0) > DIV:nth-of-type(2) > SECTION.section:eq(0) > DIV.container:eq(1) > DIV.heading:eq(0) > H1.title:eq(0)",
         "cssSelector": "#app > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(2) > SECTION:nth-of-type(1) > DIV:nth-of-type(2) > DIV:nth-of-type(1) > H1:nth-of-type(1)",
         "content": "<span style=\"color:#FF0000;\">Latest</span> Products for 2020"
        }
       ],
       "eventToken": "t0FRvoWosOqHmYL5G18QCZNWHtnQtQrJfmRrQugEa2qCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
       "responseTokens": {
        "profile.memberlevel": "0",
        "geo.city": "dublin",
        "activity.id": "302740",
        "experience.name": "Experience B",
        "geo.country": "ireland"
       }
      }
     ],
     "state": "J+W1Fq18hxliDDJonTPfV0S+mzxapAO3d14M43EsM9f12A6QaqL+E3XKkRFlmq9U"
    }
   ]
  }
 }
}
```

페이지가 브라우저에 로드되면 at.js는 가장자리에서 네트워크 호출을 실행하지 않고 [!DNL Target] 즉시 모든 오퍼를 `serverState` [!DNL Target] 적용합니다. 또한 at.js는 컨텐츠 제공 서버측에서 오퍼를 사용할 수 있는 DOM 요소만 미리 숨겨 페이지 로드 성능 및 최종 사용자 경험에 긍정적인 영향을 줍니다. [!DNL Target]

### 중요 정보

Consider the following when using `serverState`:

* 현재 at.js v2.2는 serverState를 통해 다음을 수행할 수 있는 경험만 지원합니다.

   * 페이지 로드 시 실행되는 VEC 생성 활동
   * 미리 반입된 뷰

      보기 및 at.js API를 사용하는 SPA [!DNL Target] 의 경우 at.js v2.2는 서버측에서 프리페치된 모든 뷰에 대한 컨텐츠를 캐시하고 각 보기가 트리거되는 즉시 Target에 대한 추가 컨텐츠 페치 호출을 실행하지 않고 `triggerView()` `triggerView()`다시 적용합니다.

   * **참고**:  현재, 서버측에서 검색한 mbox는 에서 지원되지 않습니다 `serverState`.

* 오퍼를 `serverState `적용할 때 at.js는 고려 `pageLoadEnabled` 및 `viewsEnabled` 설정(예: 설정이 false인 경우 페이지 로드 오퍼가 적용되지 `pageLoadEnabled` 않습니다.

   이 설정을 활성화하려면 UICONTROL 설정 > 구현 > **[설정 편집 > 페이지 로드 활성화에서 전환을 활성화합니다]**.

   ![페이지 로드 활성화 설정](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

### 추가 리소스

작동 방법에 대한 자세한 내용 `serverState` 은 다음 리소스를 참조하십시오.

* [샘플 코드](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [단일 페이지 애플리케이션(SPA) 샘플 앱 `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
