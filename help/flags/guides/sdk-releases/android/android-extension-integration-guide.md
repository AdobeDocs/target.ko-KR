---
title: Android 통합 안내서의 플래그 확장
description: Flags 확장을 Android의 Adobe Experience Platform Mobile SDK과 통합하는 방법을 알아봅니다.
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 4%

---

# Android용 플래그 확장 {#android-extension-integration-guide}

이 안내서에서는 Android에서 Adobe Experience Platform Mobile SDK과 플래그 확장을 통합하는 방법을 설명합니다.

## 사전 요구 사항 {#prerequisites}

Flags 확장을 구현하기 전에 다음을 확인하십시오.

* [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 구성된 모바일 속성
* 모바일 속성에 설치되고 구성된 플래그 확장
* Adobe Experience Cloud 조직 ID
* 최소 SDK: API 21(Android 5.0 Lollipop)

## 확장 종속성 {#extension-dependencies}

Flags 확장을 사용하려면 다음 Adobe Experience Platform 확장이 필요합니다.

| 확장 | 설명 | 필수 여부 |
|---|---|---|
| 모바일 코어 | 구성 및 이벤트 처리를 포함한 핵심 기능 제공 | 예 |
| 라이프사이클 | 모바일 SDK에 대한 애플리케이션 라이프사이클 및 세션 데이터를 수집합니다. | 예 |
| Edge Network | Adobe Experience Platform Edge Network과의 통신 활성화 | 예 |
| EDGE ID | Edge Network 확장을 사용할 때 모바일 앱에서 ID 관리를 활성화합니다 | 예 |

이러한 확장이 데이터 수집 모바일 속성에 설치되고 앱 종속성에 포함되어 있는지 확인합니다.

## 데이터 수집에서 플래그 확장 구성 {#configure}

### 확장 설치 {#install-extension}

1. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 로그인합니다.
1. **태그** 탭을 선택하고 모바일 속성을 선택합니다.
1. **확장** > **카탈로그**(으)로 이동합니다.
1. **플래그 확장**&#x200B;을(를) 검색하고 **설치**&#x200B;을(를) 선택하십시오.
1. 확장 설정을 구성합니다.

   | 설정 | 설명 |
   |---|---|
   | 애플리케이션 ID | 플래그의 애플리케이션 고유 식별자 |

1. **저장**&#x200B;을 선택합니다.
1. 구성을 업데이트하려면 [게시 프로세스](https://experienceleague.adobe.com/ko/docs/experience-platform/tags/publish/overview)를 따르십시오.

### 환경 파일 ID 가져오기 {#environment-file-id}

1. 모바일 속성에서 **환경**(으)로 이동합니다.
1. 환경에 대한 **설치** 열 아래의 상자 아이콘을 선택합니다.
1. **모바일 설치 지침** 대화 상자에서 **환경 파일 ID**&#x200B;를 복사합니다.

## 앱에 플래그 확장 추가 {#add-to-app}

### 종속성 추가 {#add-dependencies}

Mobile SDK 종속성을 프로젝트에 추가합니다. Flags 확장을 사용하려면 아래에 나열된 Mobile Core 및 Edge 관련 확장이 필요합니다.

#### BOM과 함께 Gradle 사용(권장) {#gradle-bom}

앱의 `build.gradle.kts` 파일에 다음 종속성을 추가하십시오.

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation(platform("com.adobe.marketing.mobile:sdkbom:3.+"))

    // Required extensions
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")
}
```

#### Gradle(Groovy) 사용 {#gradle-groovy}

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation platform('com.adobe.marketing.mobile:sdkbom:3.+')

    // Required extensions
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'
}
```

>[!IMPORTANT]
>
>프로덕션 애플리케이션의 경우 Adobe에서는 동적 버전 대신 명시적 버전 번호를 사용하는 것이 좋습니다. 자세한 내용은 [Gradle 종속성 관리](https://docs.gradle.org/current/userguide/dependency_management.html)를 참조하십시오.

### 플래그 종속성 추가 {#add-flags-dependency}

#### 호스팅된 Maven 저장소 사용(권장) {#hosted-maven}

`settings.gradle.kts`의 `repositories` 블록에 Flags Maven 저장소 추가:

```kotlin
maven {
    url = uri("<HTTPS Flags Maven repository URL>")
}
```

Groovy `settings.gradle` 파일의 경우:

```groovy
maven {
    url = uri('<HTTPS Flags Maven repository URL>')
}
```

`<HTTPS Flags Maven repository URL>`을(를) 플래그 확장에 대해 제공된 보안 저장소 URL로 바꾸십시오.

그런 다음 버전이 지정된 플래그 종속성을 앱의 `build.gradle.kts`에 추가합니다.

```kotlin
implementation("com.adobe.marketing.mobile:flags:<version>")
```

Groovy `build.gradle` 파일의 경우:

```groovy
implementation 'com.adobe.marketing.mobile:flags:<version>'
```

`<version>`을(를) 릴리스에 제공된 정확한 플래그 확장 버전으로 바꾸십시오.

#### Flags 배포 패키지 사용 {#distribution-package}

Flags 확장 배포 패키지는 다음을 포함합니다.

* `flags-3.x.aar`
* `flags-3.x.module`
* `flags-3.x.pom`

다음 방법 중 하나를 사용하여 Android 프로젝트에서 확장을 사용할 수 있도록 합니다.

* 배포 패키지의 모든 파일을 로컬 또는 개인 Maven 저장소에 게시하고 해당 저장소를 사용하도록 프로젝트를 구성합니다.
* `flags-3.x.aar`을(를) 프로젝트에 직접 추가하고 `flags-3.x.pom`에 지정된 전이적 종속성을 선언합니다.

### 권한 추가 {#add-permissions}

`AndroidManifest.xml` 파일에 다음 권한을 추가합니다.

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### SDK 초기화 {#initialize-sdk}

Flags 확장 API를 호출하기 전에 `Application` 클래스에서 Mobile SDK을 초기화하십시오. 모바일 속성의 환경 파일 ID를 `MobileCore.initialize`과(와) 함께 사용하면 앱이 데이터 수집에 게시한 플래그 설정을 선택하게 됩니다.

#### MobileCore.initialize 사용 {#mobile-core-initialize}

Android BOM 버전 3.8.0부터 사용할 수 있는 이 API는 데이터 수집 환경 파일로 SDK을 초기화합니다.

>[!IMPORTANT]
>
>프로덕션 앱의 경우 `LoggingMode.ERROR`만 사용하십시오. 릴리스 빌드에 `DEBUG` 또는 `VERBOSE`을(를) 사용하지 마십시오.

**Kotlin**

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

**Java**

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID", null);
    }
}
```

### 응용 프로그램 클래스 등록 {#register-application}

`AndroidManifest.xml`에서 `Application` 클래스 등록:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

## 평가 컨텍스트 {#evaluation-context}

`FeatureEvaluationContext` 클래스에 타겟팅 특성이 포함되어 있습니다(플래그 규칙 일치에 사용됨).

| 방법 | 필수 | 설명 |
|---|---|---|
| `withAttributes(map)` | 아니요 | `Map<String, List<String>>`. 키는 플래그 규칙에 사용되는 컨텍스트 특성 이름입니다(예: `locale`, `platform`, `appVersion`, `deviceType`). 값은 현재 사용자/세션에 대한 해당 키의 후보 특성 값 목록입니다(예: `["en_US"]` 또는 `["phone"]`). |

**Kotlin**

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val attrs = mapOf(
    "locale" to listOf("en_US"),
    "platform" to listOf("ANDROID")
)

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Java**

```java
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext;
import java.util.Arrays;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

Map<String, List<String>> attrs = new HashMap<>();
attrs.put("locale", Arrays.asList("en_US"));
attrs.put("platform", Arrays.asList("ANDROID"));

FeatureEvaluationContext ctx = FeatureEvaluationContext.builder()
        .withAttributes(attrs)
        .build();
```

### 사용자 정의 ID {#custom-identity}

플래그 확장은 ID 확인을 위해 Edge Network용 ID 확장을 사용합니다. 기능 플래그는 사용자 지정 ID(예: CRM ID 또는 로열티 ID)에 코호트되어 변형 분할 및 분석이 애플리케이션에 중요한 ID에 연결될 수 있습니다.

기능 플래그가 작성되면 플래그 UI에서 사용자 지정 ID 네임스페이스를 선택해야 합니다. 해당 ID에 대해 플래그를 평가하려면 일치하는 네임스페이스를 사용하여 장치의 Edge ID `identityMap`에 동일한 ID가 있어야 합니다. 런타임 시 Edge Network `updateIdentities` API에 대한 ID를 제공합니다.

#### ID 맵에 사용자 지정 ID 추가 {#add-identity}

기능 플래그에 구성된 동일한 네임스페이스 아래에 ID를 추가합니다.

**Kotlin**

```kotlin
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.edge.identity.IdentityItem
import com.adobe.marketing.mobile.edge.identity.IdentityMap

val identityMap = IdentityMap()
identityMap.addItem(
    IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
    "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(identityMap)
```

**Java**

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

final IdentityItem item = new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true);
final IdentityMap identityMap = new IdentityMap();
identityMap.addItem(item, "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

## API 참조 {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled`은(는) 특정 컨텍스트에 대해 플래그 기능이 설정되어 있는지 여부를 반환합니다. `featureKey`, `FeatureEvaluationContext`(선택적 타깃팅 특성) 및 콜백을 전달합니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오.

**서명**

*Kotlin*

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

*Java*

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `callback` | AdobeCallback&lt;부울> | 기능이 활성화된 경우 `true`(으)로 호출되고 그렇지 않은 경우 `false`로 호출됩니다. `AdobeCallbackWithError<Boolean>`을(를) 전달하여 `fail(...)`을(를) 처리할 수도 있습니다. |

**예**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    object : AdobeCallback<Boolean> {
        override fun call(isEnabled: Boolean?) {
            if (isEnabled == true) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    new AdobeCallback<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            if (Boolean.TRUE.equals(isEnabled)) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
);
```

### getFeature {#get-feature}

`getFeature`이(가) 제공된 컨텍스트에 대해 평가된 기능 페이로드를 반환합니다. 활성화/비활성화보다 더 필요하고 기능 메타데이터 또는 값을 원하는 경우 이 API를 사용하십시오.

**서명**

*Kotlin*

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

*Java*

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult> | 평가된 기능 페이로드와 함께 호출됩니다. 기능을 찾을 수 없으면 `null`일 수 있습니다. `AdobeCallbackWithError<FeatureEvaluationResult>`을(를) 전달하여 `fail(...)`을(를) 처리할 수도 있습니다. |

**응답**

*FeatureEvaluationResult*

| 필드 | 유형 | 설명 |
|---|---|---|
| `id` | 정수 | 숫자 기능 식별자 |
| `key` | 문자열 | 기능 키 |
| `featureGroupKey` | 문자열? | 사용 가능한 경우 기능 그룹 키 |
| `meta` | 문자열? | 사용 가능한 경우 기능 메타데이터를 JSON 문자열로 |
| `analyticsParam` | AnalyticsParam? | 평가된 기능에 대한 Analytics 세부 정보 |

*AnalyticsParam*

| 필드 | 유형 | 설명 |
|---|---|---|
| `featureGroupId` | 정수 | 숫자 기능 그룹 식별자 |
| `featureId` | 정수 | 숫자 기능 식별자 |
| `variantId` | 문자열? | 변형 식별자 |

**예**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-flag",
    ctx,
    object : AdobeCallback<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            if (!meta.isNullOrEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-flag",
    ctx,
    new AdobeCallback<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            String meta = feature != null ? feature.getMeta() : null;
            if (meta != null && !meta.isEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
);
```

### extensionVersion {#extension-version}

Flags 확장의 버전 문자열을 반환합니다.

**구문**

```kotlin
Flag.extensionVersion(): String
```

**예**

*Kotlin*

```kotlin
val version = Flag.extensionVersion()
```

*Java*

```java
String version = Flag.extensionVersion();
```

## API 요약 {#api-summary}

| API | 반환 |
|---|---|
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. `FeatureEvaluationContext`은(는) 규칙에 대한 타깃팅 특성을 전달합니다. [기능 평가](#is-feature-enabled)를 참조하세요. | 콜백을 통한 부울 |
| `getFeature(featureKey, evaluationContext, callback)`. 특정 컨텍스트에 대해 평가된 기능 페이로드를 반환합니다. [getFeature](#get-feature)을(를) 참조하십시오. | 콜백을 통한 FeatureEvaluationResult |
| `extensionVersion()` | 문자열 |

## 참조: {#see-also}

* [모바일 애플리케이션](../../integrate/mobile-applications.md)
* [SDK](../../integrate/sdks.md)

<!-- -->
