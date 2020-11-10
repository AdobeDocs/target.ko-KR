---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;global settings;at.js;functions;function;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;selectorsPollingTimeout;dataProviders;Hybrid Personalization;deviceIdLifetime
description: Adobe Target at.js JavaScript 라이브러리에 대한 targetGlobalSettings() 함수 정보입니다.
title: targetGlobalSettings()
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 38%

---


# targetGlobalSettings()

[!DNL Target] Standard/Premium UI에서 설정을 구성하거나 REST API를 사용하는 대신 `targetGlobalSettings()`를 사용하여 at.js 라이브러리의 설정을 무시할 수 있습니다.

사용 사례로 일부 설정을 재정의하려는 경우, 특히 at.js가 DTM([!DNL Dynamic Tag Management])을 통해 전달되는 경우를 들 수 있습니다.

## 설정{#section_42C759AE9B524A43B8659018677224B8}의 지침을 완료하여 이 설정을 변경할 수 있습니다 

다음 설정을 재정의할 수 있습니다.

### bodyHiddenStyle

* **유형**: 문자열
* **기본값**:body { opacity:0 }
* **설명**:깜박임 `globalMboxAutocreate === true` 을 최소화할 경우에만 사용됩니다.

   자세한 내용은 [at.js에서 플리커를 관리하는 방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md)을 참조하십시오.

### bodyHidingEnabled

* **유형**:부울
* **기본값**:true
* **설명**:시각적 오퍼라고도 하는 Visual Experience Composer `target-global-mbox` 에서 만든 오퍼를 전달하는 데 사용될 때 깜박임을 제어하는 데 사용됩니다.

### clientCode

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:클라이언트 코드를 나타냅니다.

### cookieDomain

* **유형**: 문자열
* **기본값**:가능한 경우 최상위 도메인에 설정합니다.
* **설명**:쿠키를 저장할 때 사용되는 도메인을 나타냅니다.

### crossDomain

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:도메인 간 추적이 활성화되었는지 여부를 나타냅니다. 허용되는 값은 다음과 같습니다.비활성화, 활성화 또는 x-only.

### cspScriptNonce

* **유형**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.
* **기본값**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.
* **설명**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.

### cspStyleNonce

* **유형**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.
* **기본값**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.
* **설명**:아래의 [콘텐츠 보안 정책을](#content-security) 참조하십시오.

### dataProviders

* **유형**:아래의 [데이터 공급자를](#data-providers) 참조하십시오.
* **기본값**:아래의 [데이터 공급자를](#data-providers) 참조하십시오.
* **설명**:아래의 [데이터 공급자를](#data-providers) 참조하십시오.

### defaultContentHiddenStyle

* **유형**: 문자열
* **기본값**:가시성:숨김
* **설명**:클래스 이름이 &quot;mboxDefault&quot;인 DIV를 사용하고 기본 컨텐츠를 통해 `mboxCreate()`, `mboxUpdate()`또는 `mboxDefine()` 숨기도록 실행되는 mbox를 래핑하는 경우에만 사용됩니다.

### defaultContentVisibleStyle

* **유형**: 문자열
* **기본값**:가시성:visible
* **설명**:클래스 이름이 &quot;mboxDefault&quot;인 DIV를 사용하고 `mboxCreate()`있거나 기본 컨텐츠가 있는 경우 적용된 오퍼를 통해 `mboxUpdate()`실행되거나 `mboxDefine()` 표시하는 mbox를 래핑하는 경우에만 사용됩니다.

### deviceIdLifetime

* **유형**:숫자
* **기본값**:63244800000ms = 2년
* **설명**:쿠키에 `deviceId` 남아 있는 시간입니다.

>[!NOTE]
>
>deviceIdLifetime 설정은 at.js 버전 2.3.1 이상에서 사용할 수 있습니다.

### 활성화됨

* **유형**:부울
* **기본값**:true
* **설명**:활성화되면 경험을 렌더링하기 위한 경험 및 DOM 조작 [!DNL Target] 요청이 자동으로 실행됩니다. 또한 [!DNL Target] 호출은 /를 통해 수동으로 실행할 `getOffer(s)` 수 `applyOffer(s)`있습니다.

   비활성화되면 요청은 자동으로 또는 수동으로 [!DNL Target] 실행되지 않습니다.

### globalMboxAutoCreate

* **유형**:숫자
* **기본값**:UI를 통해 설정된 값.
* **설명**:글로벌 mbox 요청을 실행할지 여부를 나타냅니다.

### imsOrgId

* **유형**:스팅
* **기본값**:true
* **설명**:IMS ORG ID를 나타냅니다.

### optoutEnabled

* **유형**:부울
* **기본값**:false
* **설명**:Target이 방문자 API 함수를 호출해야 하는지 여부를 `isOptedOut()` 나타냅니다. Device Graph 지원의 일부입니다.

### overrideMboxEdgeServer

* **유형**:부울
* **기본값**:true(at.js 버전 1.6.2부터 시작)
* **설명**:도메인 또는 `<clientCode>.tt.omtrdc.net` 도메인을 사용해야 하는지 여부를 `mboxedge<clusterNumber>.tt.omtrdc.net` 나타냅니다.

   If this value is true, `mboxedge<clusterNumber>.tt.omtrdc.net` domain will be saved to a cookie. 현재 at.js 1.8.2 및 at.js 2.3.1 이전의 at.js 버전을 사용할 때 [CNAME에서](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) 작동하지 않습니다. 문제가 되는 경우 at.js [](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) 를 최신 지원 버전으로 업데이트하는 것이 좋습니다.

### overrideMboxEdgeServerTimeout

* **유형**:숫자
* **기본값**:1860000 => 31분
* **설명**:값이 포함된 쿠키 수명을 `mboxedge<clusterNumber>.tt.omtrdc.net` 나타냅니다.

### pageLoadEnabled

* **유형**:부울
* **기본값**:true
* **설명**:활성화되면 페이지 로드 시 반환해야 하는 경험을 자동으로 검색합니다.

### secureOnly

* **유형**:부울
* **기본값**:false
* **설명**:at.js가 HTTPS만 사용하는지 또는 페이지 프로토콜을 기반으로 HTTP와 HTTPS 간을 전환할 수 있는지 여부를 나타냅니다.

### selectorsPollingTimeout

* **유형**:숫자
* **기본값**:5000ms = 5s
* **설명**:at.js 0.9.6에서는 [!DNL Target] 이 새로운 설정을 도입하여 이 설정을 통해 재정의할 수 있습니다 `targetGlobalSettings`.

   The `selectorsPollingTimeout` setting represents how long the client is willing to wait for all the elements identified by selectors to appear on the page.

   VEC(시각적 경험 작성기)를 통해 작성된 활동에는 선택기를 포함하는 오퍼가 있습니다.

### serverDomain

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:Target Edge Server를 나타냅니다.

### serverState

* **유형**:아래의 [하이브리드 개인화를](#server-state) 참조하십시오.
* **기본값**:아래의 [하이브리드 개인화를](#server-state) 참조하십시오.
* **설명**:아래의 [하이브리드 개인화를](#server-state) 참조하십시오.

### timeout

* **유형**:숫자
* **기본값**:UI를 통해 설정된 값.
* **설명**:에지 요청 시간 초과를 [!DNL Target] 나타냅니다.

### viewsEnabled

* **유형**:부울
* **기본값**:true
* **설명**:활성화되면 페이지 로드 시 반환해야 하는 뷰를 자동으로 검색합니다. 보기는 at.js 2에서 지원됩니다.*x*&#x200B;에만 사용할 수 있습니다.

### visitorApiTimeout

* **유형**:숫자
* **기본값**:2000ms = 2s
* **설명**:방문자 [!UICONTROL API] 요청 시간 초과를 나타냅니다.

## 사용 {#section_9AD6FA3690364F7480C872CB55567FB0}

This function can be defined before at.js is loaded or in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit at.js Settings]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

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

at.js 2.3.0+는 배달된 Target 오퍼을 적용할 때 페이지 DOM에 첨부된 SCRIPT 및 STYLE 태그의 Content Security 정책 원본을 설정할 수 있도록 지원합니다.

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

이후 `cspScriptNonce` 및 `cspStyleNonce` 설정이 지정되면 at.js 2.3.0+은 이러한 속성을 Target 오퍼을 적용할 때 DOM에 추가되는 모든 SCRIPT 및 STYLE 태그의 한 번 속성으로 설정합니다.

## 하이브리드 개인화 {#server-state}

`serverState` 은 Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있는 at.js v2.2+에서 사용할 수 있는 설정입니다. 하이브리드 통합이란 클라이언트측에서 at.js v2.2+를 사용하고 서버측에서 제공 API 또는 Target SDK를 모두 사용하여 경험을 전달하는 것을 의미합니다. `serverState` 는 at.js v2.2+를 제공하여 서버 측에서 가져온 컨텐츠에서 직접 경험을 적용하고 제공되는 페이지의 일부로 클라이언트로 돌아오는 기능을 제공합니다.

### 전제 조건

하이브리드 통합 [!DNL Target]이 필요합니다.

* **서버측**: 새 [배달 API](https://developers.adobetarget.com/api/delivery-api/) 또는 [Target SDK를 사용해야 합니다](https://developers.adobetarget.com/api/delivery-api/#section/SDKs).
* **클라이언트측**:at.js 버전 [2.2 이상을 사용해야 합니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### 코드 샘플

이 작동 방식을 보다 잘 이해하려면 아래 코드 예제를 통해 서버에 게시해 주십시오. 이 코드에서는 사용자가 [Target Node.js SDK를 사용하고 있다고 가정합니다](https://github.com/adobe/target-nodejs-sdk).

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

      보기 및 at.js API [!DNL Target] `triggerView()` `triggerView()`를 사용하는 SPA의 경우 at.js v2.2는 서버측에서 프리페치된 모든 뷰에 대한 컨텐츠를 캐시하고 각 보기가 트리거되는 즉시 Target에 대한 추가 컨텐츠 페치 호출을 실행하지 않고 적용합니다.

   * **참고**: 현재, 서버측에서 검색한 mbox는 에서 지원되지 않습니다 `serverState`.

* 오퍼를 `serverState `적용할 때 at.js는 고려 `pageLoadEnabled` 및 `viewsEnabled` 설정(예: 설정이 false인 경우 페이지 로드 오퍼가 적용되지 `pageLoadEnabled` 않습니다.

   이 설정을 활성화하려면 [관리] > [ **[!UICONTROL 구현] ] > [ [!UICONTROL 편집] ]  > [!UICONTROL 페이지 로드]**&#x200B;활성화에서 전환을 활성화합니다.

   ![페이지 로드 활성화 설정](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* 반환된 컨텐츠에서 `serverState` 태그를 사용하고 사용하는 경우 HTML 컨텐츠가 `<script>` 대신 사용되는지 확인하십시오 `<\/script>` `</script>`. 사용하는 경우, 브라우저 `</script>`는 인라인 SCRIPT의 끝 `</script>` 으로 해석되며 HTML 페이지가 중단될 수 있습니다.

### 추가 리소스

작동 방법에 대한 자세한 내용 `serverState` 은 다음 리소스를 참조하십시오.

* [샘플 코드](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [단일 페이지 애플리케이션(SPA) 샘플 앱 `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
