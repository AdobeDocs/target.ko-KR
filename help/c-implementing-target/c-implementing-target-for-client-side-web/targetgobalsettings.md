---
description: 'at.js에 대한 targetGlobalSettings() 함수 정보입니다. '
keywords: adobe.target.notification;요소;선택기;알림;확장 프로그램
seo-description: Adobe Target at.js JavaScript 라이브러리에 대한 targetGlobalSettings() 함수 정보입니다.
seo-title: Adobe Target at.js JavaScript 라이브러리에 대한 targetGlobalSettings() 함수 정보입니다.
solution: Target
subtopic: 시작하기
title: targetGlobalSettings()
topic: Standard
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# targetGlobalSettings()

[!DNL Target] Standard/Premium UI에서 설정을 구성하거나 REST API를 사용하는 대신 `targetGlobalSettings()`를 사용하여 at.js 라이브러리의 설정을 무시할 수 있습니다.

사용 사례로 일부 설정을 재정의하려는 경우, 특히 at.js가 DTM([!DNL Dynamic Tag Management])을 통해 전달되는 경우를 들 수 있습니다.

## 설정{#section_42C759AE9B524A43B8659018677224B8}의 지침을 완료하여 이 설정을 변경할 수 있습니다 

다음 설정을 재정의할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 유형 | 기본값 | 설명 |
|--- |--- |--- |--- |
| clientCode | 문자열 | UI를 통해 설정된 값 | 클라이언트 코드를 나타냅니다. |
| serverDomain | 문자열 | UI를 통해 설정된 값 | Target 에지 서버를 나타냅니다. |
| cookieDomain | 문자열 | 가능한 경우 최상위 수준 도메인으로 설정하십시오. | 쿠키를 저장할 때 사용되는 도메인을 나타냅니다. |
| crossDomain | 문자열 | UI를 통해 설정된 값 | 교차 도메인 추적이 활성화되어 있는지를 나타냅니다.<br>허용되는 값은 다음과 같습니다.<ul><li>비활성화됨</li><li>활성화됨</li><li>x-전용</li></ul> |
| timeout | 숫자 | UI를 통해 설정된 값 | Target 에지 요청 시간 제한을 나타냅니다. |
| globalMboxAutoCreate | 부울 | UI를 통해 설정된 값 | 전역 mbox 요청을 실행해야 하는지를 나타냅니다. |
| visitorApiTimeout | 숫자 | 2000ms = 2s | 방문자 API 요청 시간 제한을 나타냅니다. |
| 활성화됨 | 부울 | true | 라이브러리로서의 at.js가 활성화되어 있는지, 즉 어떤 항목이라도 실행해야 하는지를 나타냅니다. 이 설정에 대한 기본 사용 사례는 옵트아웃 쿠키 또는 at.js 기능을 비활성화하는 기타 사용자 지정 의사 결정입니다. |
| defaultContentHiddenStyle | 문자열 | 가시성: 숨김 | 기본 컨텐츠를 숨기기 위해 DIV를 클래스 이름 &quot;mboxDefault&quot;와 함께 사용하고 `mboxCreate()`, `mboxUpdate()` 또는 `mboxDefine()`을 통해 실행되는 mbox를 래핑하는 데만 사용됩니다. |
| defaultContentVisibleStyle | 문자열 | 가시성: 표시 | 적용된 오퍼(있는 경우) 또는 기본 컨텐츠를 표시하기 위해 DIV를 클래스 이름 &quot;mboxDefault&quot;와 함께 사용하고 `mboxCreate()`, `mboxUpdate()` 또는 `mboxDefine()`을 통해 실행되는 mbox를 래핑하는 데만 사용됩니다. |
| bodyHiddenStyle | 문자열 | body { opacity: 0 } | 깜박임 가능성을 최소화하기 위해 `globalMboxAutocreate === true`일 때만 사용됩니다.<br>자세한 내용은 [at.js에서 플리커를 관리하는 방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md)을 참조하십시오. |
| bodyHidingEnabled | 부울 | true | `target-global-mbox` 가 시각적 오퍼로도 알려진 시각적 경험 작성기에서 만든 오퍼를 전달하는 데 사용될 때 깜박임을 제어하는 데 사용됩니다. |
| imsOrgId | 문자열 | IMS ORG ID | IMS ORG ID를 나타냅니다. |
| secureOnly | 부울 | false | at.js에서 HTTPS만 사용되는지 또는 페이지 프로토콜을 기준으로 HTTP와 HTTPS 간을 전환할 수 있는지를 나타냅니다. |
| overrideMboxEdgeServer | 부울 | true(at.js 버전 1.6.2부터 true) | `<clientCode>.tt.omtrdc.net` 도메인과 `mboxedge<clusterNumber>.tt.omtrdc.net` 도메인 중에서 어떤 도메인을 사용해야 하는지를 나타냅니다.<br>이 값이 true면 `mboxedge<clusterNumber>.tt.omtrdc.net` 도메인이 쿠키에 저장됩니다. |
| overrideMboxEdgeServerTimeout | 숫자 | 1860000 =&gt; 31분 | `mboxedge<clusterNumber>.tt.omtrdc.net` 값을 포함하는 쿠키 라이프타임을 나타냅니다. |
| optoutEnabled | 부울 | false | Target이 방문자 API `isOptedOut()` 함수를 호출해야 하는지를 나타냅니다. Device Graph 지원의 일부입니다. |
| selectorsPollingTimeout | 숫자 | 5000ms = 5s | at.js 0.9.6에서 Target은 `targetGlobalSettings`를 통해 재정의할 수 있는 이 새 설정을 도입했습니다.<br>`selectorsPollingTimeout`은 선택기로 식별된 모든 요소가 페이지에 표시되도록 하기 위해 클라이언트가 대기하는 시간을 나타냅니다.<br>VEC(시각적 경험 작성기)를 통해 작성된 활동에는 선택기를 포함하는 오퍼가 있습니다. |
| dataProviders | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. | 아래의 &quot;데이터 공급자&quot;를 참조하십시오. |

## 사용 {#section_9AD6FA3690364F7480C872CB55567FB0}

이 함수는 at.js가 로드되기 전에 또는 **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]** &gt; **[!UICONTROL at.js 설정 편집]** &gt; **[!UICONTROL 코드 설정]** &gt; **[!UICONTROL 라이브러리 헤더]** 에서 정의할 수 있습니다.

라이브러리 헤더 필드에는 자유 형식 JavaScript를 입력할 수 있습니다. 사용자 지정 코드는 다음 예제와 유사해야 합니다.

```
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## 데이터 공급자 {#data-providers}

이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 서드 파티 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다. 비동기 및 동기 요청을 통해 여러 공급자로부터 데이터를 수집하도록 지원합니다. 이 접근 방식을 사용하면 각 공급자에 대해 독립적인 시간 제한을 포함하여 페이지 성능에 미치는 영향을 제한하면서, 기본 페이지 컨텐츠의 깜박임을 쉽게 관리할 수 있습니다

>[!NOTE]
>
>데이터 공급자는 [!DNL at.js] 1.3 이상이 필요합니다.

다음 비디오에는 추가 정보가 포함되어 있습니다.

| 비디오 | 설명 |
|--- |--- |
| [Adobe Target에서 데이터 공급자 사용](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-feature-video-use.html) | 데이터 공급자는 타사의 데이터를 Target에 쉽게 전달할 수 있는 기능입니다. 타사는 기상 서비스, DMP 또는 자체 웹 서비스일 수 있습니다. 그런 다음, 이 데이터를 사용하여 대상, Target 컨텐츠를 작성하고 방문자 프로필을 보강할 수 있습니다. |
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
