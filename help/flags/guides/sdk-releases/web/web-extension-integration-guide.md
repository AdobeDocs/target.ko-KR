---
title: 웹 통합 안내서에 대한 플래그 확장
description: 웹 애플리케이션용 Adobe Experience Platform 웹 SDK(Alloy)와 Flags 확장을 통합하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
hide: true
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 7%

---

# 웹용 플래그 확장 {#web-extension-integration-guide}

이 안내서에서는 웹 애플리케이션용 Adobe Experience Platform 웹 SDK(Alloy)와 Flags 확장을 통합하는 방법을 설명합니다. 플래그 확장을 사용하면 웹 경험에 대한 기능 플래그 관리 및 제어된 롤아웃을 사용할 수 있습니다.

## 사전 요구 사항 {#prerequisites}

Flags 확장을 구현하기 전에 다음을 확인하십시오.

* [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 구성된 웹 속성
* Adobe Experience Platform Web SDK 확장 설치
* Adobe Experience Cloud 조직 ID
* 조직의 플래그에 액세스

### 필요한 권한 {#required-permissions}

다음 속성 권한이 있는지 확인합니다.

* 개발
* 확장 관리

## 확장 종속성 {#extension-dependencies}

플래그 확장을 사용하려면 다음 Adobe Experience Platform 확장이 필요합니다.

| 확장 | 설명 | 필수 여부 |
|---|---|---|
| Adobe Experience Platform 웹 SDK | Edge Network 통신 및 ID 관리를 포함한 핵심 기능 제공 | 예 |

Flags 확장을 설치하기 전에 이 확장이 데이터 수집 웹 속성에 설치되어 있는지 확인하십시오.

## 데이터 수집에서 플래그 확장 구성 {#configure}

### 확장 설치 {#install-extension}

1. Adobe ID 자격 증명을 사용하여 [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
1. **데이터 수집** > **태그**(으)로 이동합니다.
1. 원하는 태그 속성을 선택합니다.
1. **확장** > **카탈로그**(으)로 이동합니다.
1. **플래그**&#x200B;를 검색하고 확장 카드를 선택하십시오.
1. **설치**&#x200B;를 선택합니다.

### 확장 설정 구성 {#configure-settings}

Flags 확장을 설치하면 구성 페이지로 이동합니다. 다음 설정을 구성합니다.

| 설정 | 설명 | 필수 여부 |
|---|---|---|
| 클라이언트 ID | 플래그의 애플리케이션 고유 식별자입니다. | 예 |

### 저장 및 게시 {#save-publish}

1. 확장 구성을 저장하려면 **저장**&#x200B;을 선택합니다.
1. 게시 플로우에 따라 변경 사항을 배포합니다.
   1. 라이브러리에 확장을 추가합니다.
   1. 개발 환경에 빌드합니다.
   1. Adobe Experience Platform Debugger을 사용하여 확인합니다.
   1. 스테이징 및 프로덕션으로 승격합니다.

## 웹 사이트에 태그 포함 코드 추가 {#embed-code}

태그 라이브러리를 게시한 후에는 웹 사이트에 포함 코드를 추가해야 합니다. 포함 코드는 Tags 라이브러리 및 Flags 확장을 포함하여 구성된 모든 확장을 로드하는 `<script>` 태그입니다.

### 포함 코드 복사 {#copy-embed-code}

1. 데이터 수집에서 웹 속성으로 이동합니다.
1. 왼쪽 탐색에서 **환경**&#x200B;을 선택합니다.
1. 대상 환경(개발, 스테이징 또는 프로덕션)의 행에서 **설치** 열 아래의 상자 아이콘을 선택합니다.
1. **웹 설치 지침** 대화 상자에서 Tags는 기본적으로 비동기 포함 코드로 설정됩니다.
1. **복사** 아이콘을 선택하여 포함 코드를 클립보드에 복사합니다.
1. **닫기**&#x200B;를 선택하여 모달을 닫습니다.

>[!NOTE]
>
>각 환경에는 고유한 포함 코드 URL이 있습니다. 자세한 내용은 환경 을 참조하십시오.

### 포함 코드 구현 {#implement-embed-code}

HTML 페이지의 `<head>` 요소에 포함 코드를 추가합니다. 포함 코드는 태그 라이브러리에 의존하는 다른 스크립트 앞에 배치해야 합니다.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>

  <!-- Adobe Experience Platform Tags embed code -->
  <script src="https://assets.adobedtm.com/yourcompany/your-property/launchENxxxxxxxxxxx.min.js" async></script>
</head>
<body>
  <!-- Your page content -->
</body>
</html>
```

>[!NOTE]
>
>`src` URL을 환경 페이지에서 실제 포함 코드로 바꿉니다. URL에는 회사 식별자, 속성 식별자 및 환경 식별자(예: `launch-EN123456789abcdef.min.js`)가 포함되어 있습니다.

### 태그 구성 요소로 플래그 평가 {#tags-components}

Flags 확장은 태그 기반의 평가 표면을 제공합니다.

| 구성 요소 | 유형 | 설명 |
|---|---|---|
| 기능이 활성화되었습니다. | 조건 | 현재 사용자/컨텍스트에 대해 기능이 활성화되어 있는지 여부를 반환합니다. |
| 기능 플래그 | 데이터 요소 | 부울 또는 전체 기능 개체 반환 |

## SDK 초기화 {#initialize-sdk}

플래그 확장은 태그 라이브러리가 로드될 때 자동으로 초기화됩니다. 확장은 다음 위치에 클라이언트를 노출합니다.

```javascript
window._flagClient
```

### 클라이언트 준비 대기 {#client-readiness}

태그는 비동기적으로 로드됩니다. 사용자 지정 코드에서 SDK 메서드를 호출하기 전에 클라이언트가 초기화될 때까지 기다리십시오.

```javascript
window.flagClientReady
  .then(function () {
    const enabled = window._flagClient.isFeatureEnabled('my-feature', context);
    // Use enabled to select the feature or fallback behavior.
  })
  .catch(function (error) {
    console.error('Flags initialization failed:', error);
  });
```

## 평가 컨텍스트 {#evaluation-context}

`FeatureEvaluationContext`에는 id(평가, A/B 버킷팅 및 분석에 필요) 및 선택적 타깃팅 특성(규칙 일치에 사용됨)이 포함되어 있습니다.

| 속성 | 필수 | 설명 |
|---|---|---|
| `identityNamespace` | 예 | Id 네임스페이스([Adobe Identity 네임스페이스](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces) 참조). 일반적인 값: `ECID`, `Email`, `CRMId`. |
| `identityId` | 예 | 현재 사용자의 ID 값입니다. |
| `attributes` | 아니요 | `Record<string, string[]>`. 키는 플래그 규칙에 사용되는 컨텍스트 특성 이름입니다(예: `locale`, `platform`). 값은 해당 키에 대한 후보 속성 값 목록입니다. |

태그 구성 요소에서 조건 또는 데이터 요소 UI에 ID 기본값을 설정합니다. 두 번째 인수가 플랫 특성 맵인 경우 기능 플래그 데이터 요소는 `getVar(name, attributes)`을(를) 통해 런타임 특성도 허용합니다.

### 사용 {#usage}

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: 'your-visitor-ecid',
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};
```

## API 참조 {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled`은(는) 특정 컨텍스트에 대해 플래그 기능이 설정되어 있는지 여부를 반환합니다. `featureKey` 및 `FeatureEvaluationContext`을(를) 전달합니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오. **기능이 활성화됨** 태그 조건을 사용하거나 초기화 후 사용자 지정 코드에서 `window._flagClient.isFeatureEnabled(...)`을(를) 호출하십시오.

**서명**

```javascript
isFeatureEnabled(featureKey: string, context: FeatureEvaluationContext): boolean
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | string | 플래그에서 평가할 기능 키 |
| `context` | 기능 평가 컨텍스트 | ID(필수) 및 선택적 타깃팅 속성입니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |

### 기능 플래그 데이터 요소 만들기 {#create-data-element}

규칙 또는 사용자 지정 코드에서 `%Data Element Name%`(으)로 사용할 수 있는 플래그 값이 필요한 경우 데이터 요소를 사용하십시오.

**단계**

1. 속성에서 **데이터 요소**(으)로 이동하여 **데이터 요소 추가**&#x200B;를 선택합니다.
1. **데이터 요소 만들기** 화면에서 태그 필드를 구성합니다.

   | 필드 | 값 |
   |---|---|
   | 이름 | 수사적 이름(예: `checkout flag`) |
   | 확장 | 플래그 |
   | 데이터 요소 유형 | 기능 플래그 |

1. **플래그** 확장 필드를 구성합니다.

   | 필드 | 필수 | 설명 |
   |---|---|---|
   | 기능 키 | 예 | 고유 플래그 키(예: `checkout_flag`) |
   | 반환 유형 | 예 | **부울(true/false)** — 활성화/비활성화 또는 **기능 개체(전체 세부 정보)** — `meta`을(를) 포함하는 전체 페이로드 |

1. **저장**&#x200B;을 선택합니다.

**반환 형식**

| 반환 유형 | 다음으로 해결: |
|---|---|
| 부울(true/false) | `true`(활성화된 경우), 그렇지 않은 경우 `false` |
| 기능 개체(전체 세부 정보) | 전체 평가된 기능 페이로드 또는 규칙을 만족하지 않는 경우 `null` |

### 데이터 요소 사용 {#use-data-element}

규칙에서 이름 참조(예: `%Test Flag%`).

사용자 지정 코드에서 — `_satellite.getVar`을(를) 사용합니다. 런타임 속성을 사용하여 플랫 속성 맵을 두 번째 인수로 전달하여 다음을 평가합니다.

```javascript
var isEnabled = _satellite.getVar('Test Flag', {
  locale: ['en-US'],
  platform: ['web']
});

if (isEnabled) {
  // your custom code
} else {
  // your default code
}
```

### getFeature {#get-feature}

사용/사용 안 함 이상의 메타데이터가 필요한 경우 `getFeature`에서 평가된 기능 페이로드를 반환합니다.

**기능 플래그** 데이터 요소를 **반환 형식: 기능 개체(전체 세부 정보)** — [기능 플래그 데이터 요소 만들기](#create-data-element) 참조 또는 `flagClientReady`이(가) 해결된 후 사용자 지정 코드에서 `window._flagClient.getFeature(...)`을(를) 호출하십시오.

**서명**

```javascript
getFeature(featureKey: string, context: FeatureEvaluationContext): FeatureResult | null
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | string | 플래그에서 평가할 기능 키 |
| `context` | 기능 평가 컨텍스트 | ID(필수) 및 타깃팅 속성. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |

**응답**

*FeatureResult*

| 필드 | 유형 | 설명 |
|---|---|---|
| `id` | 수 | 숫자 기능 식별자. 기능 수준 컨트롤 표시에 대한 `-1`. |
| `key` | 문자열 \| null | 기능 키. 기능 수준 컨트롤 표시에 대한 `null`. |
| `featureGroupKey` | 문자열 \| null | 사용 가능한 경우 기능 그룹 키 |
| `meta` | 문자열 \| null | 사용 가능한 경우 기능 메타데이터 |
| `analyticsParam` | AnalyticsParam \| null | 평가된 기능에 대한 Analytics 세부 정보 |

*AnalyticsParam*

| 필드 | 유형 | 설명 |
|---|---|---|
| `featureGroupId` | 수 | 숫자 기능 그룹 식별자 |
| `featureId` | 수 | 숫자 기능 식별자 |
| `variantId` | 숫자 \| null | 변형 식별자(`0`(제어용) |

**컨트롤 그룹 동작**

| 시나리오 | isFeatureEnabled | getFeature | 분석 이벤트 isFeatureEnabled | Analytics 이벤트 getFeature |
|---|---|---|---|---|
| 처리 | `true` | 정상 결과 | 예 | 예 |
| 기능 수준 제어 | `false` | 센티넬(`id: -1`, `key: null`) | 예(`variantId: 0`) | 예 |
| 기준 불일치 / 찾을 수 없음 | `false` | `null` | 아니요 | 아니오 |

**예**

```javascript
var feature = _flagClient.getFeature('new-testflag', {
  identityNamespace: 'ECID',
  identityId: visitorEcid,
  attributes: {
    locale: ['en-US']
  }
});

var meta = feature && feature.meta;
if (meta) {
  // your custom code
} else {
  // your default code
}
```

### extensionVersion {#extension-version}

Flags 확장의 버전 문자열을 반환합니다.

**서명**

```javascript
_flagClient.extensionVersion(): string
```

**예**

```javascript
const version = _flagClient.extensionVersion();
console.log(`Flags extension version: ${version}`);
```

## API 요약 {#api-summary}

| API | 반환 |
|---|---|
| 기능 플래그(태그 데이터 요소, 부울) | 부울 |
| 기능 플래그(태그 데이터 요소, 개체) | 기능 개체 또는 `null` |
| `window.flagClientReady` | 약속 — 확장 초기화를 기다립니다. |
| `window._flagClient.isFeatureEnabled(featureKey, context)` | 부울 |
| `window._flagClient.getFeature(featureKey, context)` | 기능 개체 또는 `null` |
| `window._flagClient.extensionVersion()` | 확장 버전 문자열 |

## 오류 처리 {#error-handling}

확장은 오류를 정상적으로 처리합니다.

| 시나리오 | 비헤이비어 |
|---|---|
| 초기화 시 네트워크를 사용할 수 없음 | SDK이 백오프를 통해 초기 가져오기를 3번 다시 시도하고 초기화에 실패합니다. `window.flagClientReady` 및 `_satellite.getVar(...)`이(가) `Failed to initialize Flag`(으)로 거부되고 `window._flagClient`은(는) `undefined` 상태로 유지됩니다. |
| 컨텍스트에 ID 누락 | 평가에서 오류가 발생합니다. `identityNamespace`과(와) `identityId`을(를) 모두 입력하십시오. |
| 기능을 찾을 수 없음 | `getFeature`이(가) `null`을(를) 반환하고 `isFeatureEnabled`이(가) `false`을(를) 반환합니다. |

```javascript
try {
  const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
} catch (error) {
  console.error('Evaluation failed:', error.message);
  // Use default value
}
```

## 모범 사례 {#best-practices}

### 일관된 ID 제공 {#consistent-identity}

롤아웃 비율에서 일관된 버킷팅을 위해 평가 간에 동일한 ID 네임스페이스 및 ID를 사용합니다.

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: identity,
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};

const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
```

### 누락된 기능을 우아하게 처리 {#handle-missing}

기능을 찾을 수 없거나 평가에 실패할 경우 항상 폴백 동작을 제공합니다.

```javascript
const feature = _flagClient.getFeature('new-testflag', context);

if (feature && feature.meta) {
  // your custom code
} else {
  // Feature not enabled - use default code
}
```

### 페이지 로드 후 평가 {#evaluate-after-load}

API를 호출하기 전에 태그 라이브러리 및 플래그 확장이 초기화되었는지 확인하십시오. 규칙에 **Library Loaded** 이벤트, **기능 플래그** 데이터 요소를 사용하거나 `flagClientReady`을(를) 기다립니다.

```javascript
window.flagClientReady.then(function () {
  var isEnabled = window._flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
});
```

## 참조: {#see-also}

* [첫 번째 기능 플래그 만들기](../../feature-flags/create-your-first-feature-flag.md)
* [기능 플래그 및 기능 그룹의 대상자](../../audience/audience-in-feature-flags-and-feature-groups.md)
* [보고](../../feature-flags/reporting.md)

<!-- -->
