---
keywords: at.js;브라우저 사용자 에이전트;사용자 에이전트;클라이언트 힌트;사용자 에이전트
description: 방법 알아보기 [!DNL Adobe Target] 은 사용자 에이전트 및 클라이언트 힌트를 사용하여 방문자에게 세그멘테이션 및 개인화에 대한 자격을 부여합니다.
title: 사용자 에이전트 및 클라이언트 힌트
feature: at.js
role: Developer
source-git-commit: 2527608fc781913024d5d6ffee49aff9eb6c2f42
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 3%

---

# 사용자 에이전트 및 클라이언트 힌트

[!DNL Adobe Target] 사용자 에이전트를 사용하여 방문자의 세그먼테이션 및 개인화에 대한 자격을 부여합니다.

웹 브라우저가 서버에 요청을 할 때마다, 요청 헤더에 포함된 는 브라우저와 브라우저가 실행되는 환경에 대한 정보입니다. 인터넷 초기 이후 이 데이터는 사용자-에이전트라는 단일 문자열로 집계되었습니다.

다음 텍스트는 Safari 브라우저를 사용하는 Mac OS X 기반 컴퓨터의 샘플 사용자 에이전트입니다.

```
Mozilla/5.0 (Linux; Android 12; SM-S908E) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.41 Mobile Safari/537.36 
```

이 사용자-에이전트로부터 요청을 받는 서버는 브라우저 및 운영 체제에 대한 다음 정보를 인식할 수 있습니다.

| 정보 | 세부 사항 |
| --- | --- |
| 소프트웨어 이름 | Chrome |
| 소프트웨어 버전 | 101 |
| 전체 소프트웨어 버전 | 101.0.4951.41 |
| 레이아웃 엔진 이름 | AppleWebKit |
| 레이아웃 엔진 버전 | 537.36 |
| 운영 체제 | Android |
| 운영 체제 버전 | Android 12(스노우 콘) |
| 장치 | SM-S908E(삼성 갤럭시 S22 Ultra) |

수년 동안 사용자 에이전트 문자열에 포함된 브라우저 및 장치 정보의 양이 증가했습니다.

## 사용자 에이전트 사용 사례

사용자 에이전트는 오랫동안 마케팅 및 개발자 팀에게 브라우저, 운영 체제에 대한 중요한 통찰력을 제공하는 데 사용되어 왔습니다. 및 장치에는 사이트 컨텐츠와 사용자가 웹 사이트와 상호 작용하는 방법 등이 표시됩니다. 사용자 에이전트는 또한 다양한 추가 목적으로 사이트를 크롤링하는 스팸을 차단하고 보트를 필터링하는 데 사용됩니다.

그러나 최근 몇 년 동안 일부 사이트 소유자 및 마케팅 공급업체는 사용자-에이전트를 요청 헤더에 포함된 다른 정보와 함께 사용하여 사용자-에이전트를 알지 못하고 사용자를 식별하는 수단으로 사용할 수 있는 디지털 지문을 만들었습니다. 사용자 에이전트가 사이트 소유자를 위해 제공하는 중요한 목적에도 불구하고 브라우저 개발자는 사이트 방문자에 대한 잠재적인 개인 정보 보호 문제를 제한하는 사용자 에이전트의 작동 방식을 변경하기로 결정했습니다.

사용자 에이전트 클라이언트 힌트는 솔루션 브라우저 개발자가 개발한 것입니다. 클라이언트 힌트를 사용하면 사이트에서 필요한 브라우저, 운영 체제 및 장치 정보를 수집할 수 있을 뿐만 아니라 핑거와 같은 기밀 추적 방법으로부터 더욱 강력한 보호를 제공할 수 있습니다.

## 클라이언트 힌트

사용자-에이전트 클라이언트 힌트는 웹 사이트 소유자에게 사용자 에이전트에서 사용할 수 있는 동일한 정보의 대부분을 개인 정보 보호 방식으로 액세스할 수 있는 기능을 제공합니다. 최신 브라우저가 사용자-에이전트를 웹 서버에 보낼 때 필요 여부에 관계없이 모든 요청 시 전체 사용자-에이전트가 전송됩니다. 반면 클라이언트 힌트는 서버가 브라우저에 클라이언트에 대해 알고 싶은 추가 정보를 요청해야 하는 모델을 적용합니다. 이 요청을 받으면 브라우저가 자체 정책 또는 사용자 구성을 적용하여 반환되는 데이터를 확인할 수 있습니다. 이제 모든 요청에 대해 기본적으로 전체 사용자-에이전트를 노출하는 대신, 액세스를 명시적 및 감사 가능한 방식으로 관리합니다.

사용자-에이전트 클라이언트 힌트는 버전 89 이후 Chrome에서 사용할 수 있습니다. Microsoft Edge, Opera, Brave, Chrome Android, Opera Android 및 Samsung Internet과 같은 최신 Chromium 기반 브라우저 버전은 클라이언트 힌트 API를 지원합니다.

브라우저가 웹 서버에 대해 수행하는 첫 번째 요청의 헤더에 포함된 클라이언트 힌트는 브라우저 브랜드, 브라우저의 주요 버전 및 클라이언트가 모바일 장치인지 여부에 대한 표시자를 포함합니다. 각 데이터 조각은 다음 샘플에서와 같이 단일 사용자 에이전트 문자열로 그룹화되지 않고 고유한 헤더 값을 갖습니다.

```
Sec-CH-UA: "Chromium";v="101", "Google Chrome";v="101", " Not;A Brand";v="99" 
Sec-CH-UA-Mobile: ?0 
Sec-CH-UA-Platform: "macOS"
```

다음 샘플은 동일한 브라우저의 사용자 에이전트입니다.

```
Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.54 Safari/537.36 
```

정보가 유사하지만 서버에 대한 첫 번째 요청에는 사용자 에이전트 문자열에 사용할 수 있는 항목의 하위 집합만 포함하는 클라이언트 힌트가 포함됩니다. 요청에서 누락된 항목은 OS 아키텍처, 전체 OS 버전, 레이아웃 엔진 이름, 레이아웃 엔진 버전 및 전체 브라우저 버전입니다. 그러나 후속 요청 시 클라이언트 힌트 API를 사용하면 웹 서버에서 장치에 대한 높은 엔트로피 세부 정보를 추가로 요청할 수 있습니다. 이러한 높은 엔트로피 값이 요청될 때 브라우저 정책이나 사용자 설정에 따라 브라우저 응답에 해당 정보가 포함될 수 있습니다.

다음 예는 높은 엔트로피 값을 요청할 때 클라이언트 힌트 API에서 반환되는 JSON 개체입니다.

```
{ 

    "architecture":"x86", 
    "bitness":"64", 
    "brands":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100" 
        } 
    ], 
    "fullVersionList":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99.0.0.0" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100.0.4896.127" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100.0.4896.127" 
        } 
    ], 
    "mobile":false, 
    "model":"", 
    "platformVersion":"12.2.1" 
} 
```

높은 엔트로피 값에는 기본 클라이언트 힌트 정보에서 사용할 수 없는 몇 가지 추가 정보가 포함됩니다. 다음 표에는 기본 요청에서 사용할 수 있는 데이터와 높은 엔트로피 사용자 에이전트 클라이언트 힌트 정보에 대한 세부 정보가 포함되어 있습니다.

| HTTP 헤더 | JavaScript | User-agent | 클라이언트 힌트 | 높은 엔트로피 클라이언트 힌트 |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | 브랜드 | 예 | 예 | 아니오 |
| Sec-CH-UA-Platform | 플랫폼 | 예 | 예 | 아니오 |
| Sec-CH-UA-Mobile | mobile | 예 | 예 | 아니오 |
| Sec-CH-UA-Platform-Version | platformVersion | 예 | 아니오 | 예 |
| Sec-CH-UA-Arch | 아키텍처 | 예 | 아니오 | 예 |
| Sec-CH-UA-Model | model | 예 | 아니오 | 예 |
| Sec-CH-UA-Bitness | 비트 | 예 | 아니오 | 예 |
| Sec-CH-UA-Full-Version-List | fullVersionList | 예 | 아니오 | 예 |

## 클라이언트 힌트로 마이그레이션

현재 Chromium 기반 브라우저는 웹 서버에 수행된 요청 헤더에 있는 클라이언트 힌트와 함께 사용자 에이전트를 계속 보냅니다. 그러나 2022년 4월부터 2023년 2월까지 계속되며 사용자-에이전트 문자열에 포함된 데이터의 양이 줄어듭니다. Safari 및 Firefox와 같은 다른 브라우저는 사용자-에이전트 문자열을 계속 활용합니다. 그러나, 또한 그에 포함된 정보의 양을 줄일 것입니다.

## [!DNL Target] 클라이언트 힌트가 필요한 사용 사례

Target에서 다음 사용 사례에는 클라이언트 힌트가 필요합니다.

### 대상 속성

만약 [!DNL Target] 대상 및 다음 대상 속성 중 하나를 사용하십시오. [!DNL Target] 올바른 세분화를 수행하려면 클라이언트 힌트가 필요합니다.

* 브라우저
* 운영 체제
* 모바일

### 프로필 스크립트

프로필 스크립트를 사용하고 `user.browser` 속성(사용자-에이전트를 참조하는), 프로필 스크립트를 업데이트하여 하나 이상의 클라이언트 힌트를 확인해야 할 수 있습니다. 함수를 사용하여 클라이언트 힌트에 액세스할 수 있습니다 `user.clientHint('sec-ch-ua-xxxxx')`. Client Hint 헤더 이름은 모두 소문자여야 합니다.

다음 예제에서는 프로필 스크립트에서 Windows OS를 올바르게 검색하는 방법을 보여 줍니다.

```
"return (((user.browser != null) && (user.browser.indexOf(\"Windows\") > -1)) || " + 
      "((user.clientHint('sec-ch-ua-platform') != null) && 
(user.clientHint('sec-ch-ua-platform') === 'Windows')));" 
```

다음 섹션에서는 클라이언트 힌트 헤더 및 해당 프로필 스크립트 사용 의미 체계를 보여줍니다.

#### Sec-CH-UA

엔트로피: 낮은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA){target=_blank} 대상 특성: 브라우저 프로필 스크립트 사용: `user.clientHint('sec-ch-ua')`

#### Sec-CH-UA-Arch

엔트로피: 높은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch){target=_blank} 대상 특성: 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-arch')`

#### Sec-CH-UA-Bitness

엔트로피: 높은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness){target=_blank} 대상 특성: 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-bitness')`

#### Sec-CH-UA-Full-Version-List

엔트로피: 높은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List){target=_blank} 대상 특성: 브라우저 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-full-version-list')`

#### Sec-CH-UA-Mobile

엔트로피: 낮은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile){target=_blank} 대상 특성: 모바일 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-mobile')`

#### Sec-CH-UA-Model

엔트로피: 높은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model){target=_blank} 대상 특성: 모바일 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-model')`

#### Sec-CH-UA-Platform

엔트로피: 낮은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform){target=_blank} 대상 특성: 운영 체제 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-platform')`

#### Sec-CH-UA-Platform-Version

엔트로피: 높은 설명서: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version){target=_blank} 대상 특성: 프로필 스크립트 사용: `user.clientHint('sec-ch-ua-platform-version')`

## 클라이언트 힌트를 로 전달하는 방법 [!DNL Adobe Target]

다음 섹션에는 다음에 따라 클라이언트 힌트를 전달하는 방법에 대한 자세한 정보가 포함되어 있습니다 [!DNL Target] 구현 을 참조하십시오.

### at.js 버전 2.9.0 이상

at.js 2.9.0부터 사용자 에이전트 클라이언트 힌트는 브라우저에서 자동으로 수집되어 로 전송됩니다 [!DNL Target] when `getOffer/getOffers()` 가 호출됩니다. 기본적으로 at.js는 &quot;낮은 엔트로피&quot; 클라이언트 힌트만 수집합니다. 대상 세그멘테이션을 수행하거나 이전 섹션에서 &quot;높은 엔트로피&quot;로 분류된 데이터를 기반으로 프로필 스크립트를 사용하는 경우, 를 통해 브라우저에서 &quot;높은 엔트로피&quot; 클라이언트 힌트를 수집하도록 at.js를 구성해야 합니다 `targetGlobalSettings`.

`window.targetGlobalSettings = { allowHighEntropyClientHints: true };`

### 서버측 SDK

서버측 SDK를 통해 클라이언트 힌트를 전달하는 방법에 대한 자세한 내용은 [클라이언트 힌트](https://adobetarget-sdks.gitbook.io/docs/core-principles/audience-targeting#client-hints)의 {target=_blank} *Adobe Target SDK* 설명서.












