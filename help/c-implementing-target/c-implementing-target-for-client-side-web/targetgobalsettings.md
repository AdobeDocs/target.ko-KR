---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;전역 설정;at.js;functions;clientCode;serverDomain;cookiedomain;cookieddomain;cookiedomain;crossDomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenSettings 스타일;defaultContentVisibleStyle;bodyHiddenStyle;bodyHiddenEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServer;optoutEnabled;optout;optout;selectorsPollingTimeout;dataProviders;Providers 하이브리드 개인화;deviceIdLifetime
description: Adobe [!DNL Target] at.js JavaScript library to override settings instead of using the [!DNL Target] UI 또는 REST API에 targetGlobalSettings() 함수를 사용합니다.
title: targetGlobalSettings() 함수를 사용하려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 14080cf6-6a15-4829-b95d-62c068898564
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '2200'
ht-degree: 31%

---

# targetGlobalSettings()

[!DNL Target] Standard/Premium UI에서 설정을 구성하거나 REST API를 사용하는 대신 `targetGlobalSettings()`를 사용하여 at.js 라이브러리의 설정을 무시할 수 있습니다.

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
* **설명**:시각적 오퍼라고도  `target-global-mbox` 하는 Visual Experience Composer에서 만든 오퍼를 제공하는 데 사용되는 깜박임을 제어하는 데 사용됩니다.

### clientCode

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:클라이언트 코드를 나타냅니다.

### cookieDomain

* **유형**: 문자열
* **기본값**:가능한 경우 최상위 도메인으로 설정합니다.
* **설명**:쿠키를 저장할 때 사용되는 도메인을 나타냅니다.

### crossDomain

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:크로스 도메인 추적이 활성화되었는지 여부를 나타냅니다. 허용되는 값은 다음과 같습니다.비활성화됨, 활성화됨 또는 x-only.

### cspScriptNonce

* **유형**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.
* **기본값**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.
* **설명**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.

### cspStyleNonce

* **유형**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.
* **기본값**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.
* **설명**:아래의  [컨텐츠 보안 정책](#content-security) 을 참조하십시오.

### dataProviders

* **유형**:아래의  [데이터 공급자](#data-providers) 를 참조하십시오.
* **기본값**:아래의  [데이터 공급자](#data-providers) 를 참조하십시오.
* **설명**:아래의  [데이터 공급자](#data-providers) 를 참조하십시오.

### decisionMethod {#on-device-decisioning}

* **유형**: 문자열
* **기본값**:서버측
* **기타 값**:장치 내, 하이브리드
* **설명**:아래의 의사 결정 방법을 참조하십시오.

**의사 결정 방법**

장치에서 직접 의사 결정을 할 때, Target은 at.js가 경험을 전달하는 방법을 지시하는 [!UICONTROL 의사 결정 방법]이라는 새로운 설정을 소개합니다. `decisioningMethod`에는 다음 값이 3개 있습니다.서버측 전용, 장치 전용 및 하이브리드 `decisioningMethod`이(가) `targetGlobalSettings()`에서 설정되면 모든 [!DNL Target] 결정에 대한 기본 의사 결정 방식 역할을 합니다.

[!UICONTROL 서버측 전용]:

[!UICONTROL 서버측 전용] 은 at.js 2.5+가 구현되어 웹 속성에 배포될 때 기본적으로 설정되어 있는 기본 의사 결정 방식입니다.

기본 구성으로 [!UICONTROL 서버측 전용]을 사용하는 것은 차단 서버 호출을 포함하는 [!DNL Target] 에지 네트워크에서 모든 결정을 한다는 것을 의미합니다. 이 접근 방식에서는 증분 지연을 도입할 수 있지만, [Recommendations](/help/c-recommendations/recommendations.md), [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md)(AP) 및 [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md) 활동을 포함하는 Target의 기계 학습 기능을 적용할 수 있는 등 상당한 이점을 제공합니다.

또한 다양한 세션과 채널에서 지속되는 Target의 사용자 프로필을 사용하여 개인화된 경험을 강화하면 비즈니스에 강력한 결과를 제공할 수 있습니다.

마지막으로 [!UICONTROL 서버측 전용]을 사용하면 Adobe Experience Cloud을 사용하고 Audience Manager 및 Adobe Analytics 세그먼트를 통해 타깃팅할 수 있는 대상을 미세 조정할 수 있습니다.

[!UICONTROL 온디바이스 전용]:

[!UICONTROL 온디바이스는 ] 온디바이드 의사 결정이 웹 페이지 전체에서 사용되어야 하는 경우 at.js 2.5+에서 설정해야 하는 의사 결정 방식입니다.

디바이스에서 의사 결정을 내릴 수 있는 모든 활동을 포함하는 캐시된 규칙 아티팩트로 의사 결정을 내림으로써 경험 및 개인화 활동을 빠른 속도로 전달할 수 있습니다.

장치에서 의사 결정을 할 수 있는 활동에 대한 자세한 내용은 지원되는 기능 섹션을 참조하십시오.

이 의사 결정 방법은 [!DNL Target]의 결정이 필요한 모든 페이지에서 성능이 매우 중요한 경우에만 사용해야 합니다. 또한 이 의사 결정 방법을 선택하면 장치에서 의사 결정을 할 수 없는 [!DNL Target] 활동이 전달되거나 실행되지 않습니다. at.js 라이브러리 2.5+는 결정을 내릴 캐시된 규칙 아티팩트만 찾도록 구성되어 있습니다.

하이브리드:

[!UICONTROL Adobe Target Edge 네트워크에 대한 네트워크 호출이 필요한 ] 장치 내 의사 결정 및 활동을 모두 실행할 때 at.js 2.5+에서 설정해야 하는 의사 결정 방법을 하이브리드합니다.

장치 내 의사 결정 활동과 서버측 활동을 모두 관리하는 경우 페이지에 [!DNL Target]을(를) 배포하고 프로비저닝하는 방법을 생각하면 다소 복잡하고 지루할 수 있습니다. 의사 결정 방법으로 하이브리드 경우 [!DNL Target]은 서버측 실행이 필요한 작업과 장치 내 의사 결정만 실행할 시기를 Adobe Target Edge 네트워크에 서버 호출을 지정해야 하는 시기를 알고 있습니다.

JSON 규칙 아티팩에는 at.js에 mbox가 실행 중인 서버측 활동 또는 장치 내 의사 결정 활동을 가지고 있는지 알리는 메타데이터가 포함되어 있습니다. 이 의사 결정 방법을 사용하면 신속하게 전달하려는 활동이 장치 내 의사 결정을 통해 이루어지며 보다 강력한 ML 기반의 개인화가 필요한 활동에 대해 이러한 활동이 Adobe Target Edge 네트워크를 통해 이루어집니다.

### defaultContentHiddenStyle

* **유형**: 문자열
* **기본값**:가시성:숨김
* **설명**:클래스 이름이 &quot;mboxDefault&quot;인 DIV를 사용하고 기본 컨텐츠를 통해  `mboxCreate()`실행되거나 기본 컨텐츠를 숨기기 `mboxUpdate()`에 사용되는 mbox `mboxDefine()` 를 래핑하는 경우에만 사용됩니다.

### defaultContentVisibleStyle

* **유형**: 문자열
* **기본값**:가시성:visible
* **설명**:클래스 이름이 &quot;mboxDefault&quot;인 DIV를 사용하고 있거나 기본 컨텐츠가 있는 경우 적용된 오퍼 `mboxCreate()`를 통해  `mboxUpdate()`실행되거나  `mboxDefine()` 표시되는 mbox를 래핑하는 경우에만 사용됩니다.

### deviceIdLifetime

* **유형**:숫자
* **기본값**:63244800000 ms = 2년
* **설명**:쿠키에  `deviceId` 남아 있는 시간입니다.

>[!NOTE]
>
>deviceIdLifetime 설정은 at.js 버전 2.3.1 이상에서 사용할 수 있습니다.

### 활성화됨

* **유형**:부울
* **기본값**:true
* **설명**:활성화되면 경험  [!DNL Target] 검색과 경험을 렌더링하기 위한 DOM 조작 요청이 자동으로 실행됩니다. 또한 [!DNL Target] 호출은 `getOffer(s)` / `applyOffer(s)`를 통해 수동으로 실행할 수 있습니다.

   비활성화하면 [!DNL Target] 요청이 자동으로 또는 수동으로 실행되지 않습니다.

### globalMboxAutoCreate

* **유형**:숫자
* **기본값**:UI를 통해 설정된 값.
* **설명**:글로벌 mbox 요청을 실행할지 여부를 나타냅니다.

### imsOrgId

* **유형**:스팅
* **기본값**:true
* **설명**:IMS 조직 ID를 나타냅니다.

### optoutEnabled

* **유형**:부울
* **기본값**:false
* **설명**:Target이 방문자 API 함수를 호출해야 하는지 여부를  `isOptedOut()` 나타냅니다. Device Graph 지원의 일부입니다.

### overrideMboxEdgeServer

* **유형**:부울
* **기본값**:true(at.js 버전 1.6.2부터 true)
* **설명**:도메인 또는  `<clientCode>.tt.omtrdc.net` 도메인을 사용해야 하는지  `mboxedge<clusterNumber>.tt.omtrdc.net` 나타냅니다.

   이 값이 true이면 `mboxedge<clusterNumber>.tt.omtrdc.net` 도메인이 쿠키에 저장됩니다. 현재 at.js 1.8.2 및 at.js 2.3.1 이전 at.js 버전을 사용할 때 [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)에서 작동하지 않습니다. 문제가 되는 경우 [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)에서 지원되는 최신 버전으로 업데이트하는 것이 좋습니다.

### overrideMboxEdgeServerTimeout

* **유형**:숫자
* **기본값**:1860000 => 31분
* **설명**:값이 포함된 쿠키 수명을  `mboxedge<clusterNumber>.tt.omtrdc.net` 나타냅니다.

### pageLoadEnabled

* **유형**:부울
* **기본값**:true
* **설명**:활성화되면 페이지 로드 시 반환해야 하는 경험을 자동으로 검색합니다.

### secureOnly

* **유형**:부울
* **기본값**:false
* **설명**:at.js가 HTTPS만 사용해야 하는지 또는 페이지 프로토콜을 기반으로 HTTP와 HTTPS 간을 전환할 수 있도록 허용되어야 하는지를 나타냅니다.

### selectorsPollingTimeout

* **유형**:숫자
* **기본값**:5000ms = 5s
* **설명**:at.js 0.9.6에서는 을 통해 재정의할 수 있는 이 새로운 설정을  [!DNL Target] 도입했습니다 `targetGlobalSettings`.

   `selectorsPollingTimeout` 설정은 클라이언트가 선택기로 식별된 모든 요소가 페이지에 표시될 때까지 기다리는 시간을 나타냅니다.

   VEC(시각적 경험 작성기)를 통해 작성된 활동에는 선택기를 포함하는 오퍼가 있습니다.

### serverDomain

* **유형**: 문자열
* **기본값**:UI를 통해 설정된 값.
* **설명**:Target Edge Server를 나타냅니다.

### serverState

* **유형**:아래의  [하이브리드 ](#server-state) 개인화를 참조하십시오.
* **기본값**:아래의  [하이브리드 ](#server-state) 개인화를 참조하십시오.
* **설명**:아래의  [하이브리드 ](#server-state) 개인화를 참조하십시오.

### timeout

* **유형**:숫자
* **기본값**:UI를 통해 설정된 값.
* **설명**:가장자리  [!DNL Target] 요청 시간 초과를 나타냅니다.

### viewsEnabled

* **유형**:부울
* **기본값**:true
* **설명**:이 옵션이 활성화되면 페이지 로드 시 반환해야 하는 보기를 자동으로 검색합니다. 보기는 at.js 2에서 지원됩니다.*x* 에만 사용할 수 있습니다.

### visitorApiTimeout

* **유형**:숫자
* **기본값**:2000ms = 2s
* **설명**:방문자  [!UICONTROL API ] 요청 시간 초과를 나타냅니다.

## 사용 {#section_9AD6FA3690364F7480C872CB55567FB0}

이 함수는 at.js를 로드하기 전에 정의하거나 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 편집 at.js 설정]** > **[!UICONTROL 코드 설정]** > **[!UICONTROL 라이브러리 헤더]**&#x200B;에서 정의할 수 있습니다.

라이브러리 헤더 필드에는 자유 형식 JavaScript를 입력할 수 있습니다. 사용자 지정 코드는 다음 예제와 유사해야 합니다.

```javascript
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

```javascript
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

```javascript
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

```javascript
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

## 콘텐츠 보안 정책 {#content-security}

at.js 2.3.0+은 제공된 Target 오퍼을 적용할 때 DOM 페이지에 첨부된 SCRIPT 및 STYLE 태그에서 Content Security 정책 원본을 설정할 수 있도록 지원합니다.

SCRIPT 및 STYLE 논리는 at.js 2.3.0+ 로드 전에 `targetGlobalSettings.cspScriptNonce` 및 `targetGlobalSettings.cspStyleNonce`에 적절히 설정해야 합니다. 아래 예를 참조하십시오.

```javascript
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

`cspScriptNonce` 및 `cspStyleNonce` 설정이 지정되면 at.js 2.3.0+은 Target 오퍼을 적용할 때 DOM에 추가되는 모든 SCRIPT 및 STYLE 태그의 경우 이러한 속성을 nonce 특성으로 설정합니다.

## 하이브리드 개인화 {#server-state}

`serverState` 은 Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있는 at.js v2.2+에서 사용할 수 있는 설정입니다. 하이브리드 통합은 클라이언트측에서 at.js v2.2+를 사용하고 있으며, 서버측에서 배달 API 또는 Target SDK를 모두 사용하고 있음을 의미합니다. `serverState` 는 at.js v2.2+에서 서버측에서 가져온 콘텐츠에서 직접 경험을 적용하고 서비스되는 페이지의 일부로 클라이언트에 반환할 수 있는 기능을 제공합니다.

### 전제 조건

[!DNL Target]의 하이브리드 통합이 있어야 합니다.

* **서버측**:새  [배달 ](https://developers.adobetarget.com/api/delivery-api/) API 또는  [Target SDK를 사용해야 합니다](https://developers.adobetarget.com/api/delivery-api/#section/SDKs).
* **클라이언트측**:at.js 버전  [2.2 이상을 사용해야 합니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### 코드 샘플

이 작동 방식을 보다 잘 이해하려면 서버에서 사용할 코드 예제를 참조하십시오. 이 코드에서는 사용자가 [Target Node.js SDK](https://github.com/adobe/target-nodejs-sdk)를 사용하고 있다고 가정합니다.

```javascript
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

페이지가 브라우저에 로드되면 at.js는 [!DNL Target] 가장자리에 대한 네트워크 호출을 실행하지 않고 `serverState`에서 모든 [!DNL Target] 오퍼를 즉시 적용합니다. 또한 at.js는 컨텐츠 제공 서버측에서 [!DNL Target] 오퍼를 사용할 수 있는 DOM 요소만 미리 숨겨 페이지 로드 성능 및 최종 사용자 경험에 긍정적인 영향을 줍니다.

### 중요 정보

`serverState`을(를) 사용할 때는 다음 사항을 고려하십시오.

* 현재 at.js v2.2는 serverState를 통해 다음을 위한 경험만 전달하는 것을 지원합니다.

   * 페이지 로드 시 실행되는 VEC 생성 활동.
   * 사전 반입된 뷰.

      at.js API에서 [!DNL Target] 보기 및 `triggerView()`를 사용하는 SPA의 경우 at.js v2.2는 서버측에서 프리페치된 모든 뷰에 대한 컨텐츠를 캐시하고 `triggerView()`를 통해 각 보기가 트리거되는 즉시 해당 내용을 적용하여 Target에 대한 추가 컨텐츠 가져오기 호출을 실행하지 않고 다시 적용합니다.

   * **참고**:현재, 서버측에서 검색된 mbox는 에서 지원되지 않습니다 `serverState`.

* `serverState `오퍼를 적용할 때 at.js는 `pageLoadEnabled` 및 `viewsEnabled` 설정을 고려합니다. 예를 들어 `pageLoadEnabled` 설정이 false이면 페이지 로드 오퍼가 적용되지 않습니다.

   이러한 설정을 켜려면 **[!UICONTROL 관리] > [!UICONTROL 구현] > [!UICONTROL 편집] > [!UICONTROL 페이지 로드 활성화]**&#x200B;에서 전환을 활성화합니다.

   ![페이지 로드 사용 설정](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* `serverState`을(를) 사용하고 반환되는 컨텐츠에서 `<script>` 태그를 사용하는 경우 HTML 컨텐츠에 `</script>` 대신 `<\/script>`가 사용되는지 확인하십시오. `</script>`을(를) 사용하는 경우 브라우저가 `</script>`을(를) 인라인 SCRIPT의 끝으로 해석하고 HTML 페이지를 중단할 수 있습니다.

### 추가 리소스

`serverState`의 작동 방법에 대해 자세히 알아보려면 다음 리소스를 확인하십시오.

* [샘플 코드](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [단일 페이지 애플리케이션(SPA) 샘플 앱 `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo)을
