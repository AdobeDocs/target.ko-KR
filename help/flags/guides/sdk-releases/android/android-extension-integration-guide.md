---
title: Android 통합 안내서의 플래그 확장
description: Flags 확장을 Android의 Adobe Experience Platform Mobile SDK과 통합하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1379'
ht-degree: 4%
---
# Android용 플래그 확장 {#android-extension-integration-guide}

이 안내서에서는 Android에서 Adobe Experience Platform Mobile SDK과 플래그 확장을 통합하는 방법을 설명합니다.

## 사전 요구 사항 {#prerequisites}

Flags 확장을 구현하기 전에 다음을 확인하십시오.

* [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 구성된 모바일 속성
* 모바일 속성에 설치되고 구성된 Adobe 플래그 확장
* Adobe Experience Cloud 조직 ID
* 노출 분석을 수신하기 위해 모바일 속성에 구성된 Edge Network 데이터스트림
* Android API 21(Android 5.0 Lollipop) 이상
* Mobile Core 3.6.0 이상(`sdk-bom` 3.17.0 이상에 포함됨)

## 확장 종속성 {#extension-dependencies}

Flags 확장을 사용하려면 다음 Adobe Experience Platform 확장이 필요합니다.

| 확장 | 설명 | 필수 여부 |
|---|---|---|
| [모바일 코어](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | 구성, 이벤트 처리 및 SDK 초기화 제공 | 예 |
| [라이프사이클](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | 앱이 전경이나 배경으로 이동할 때 보고합니다. | 예 |
| [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Adobe Experience Platform에 노출 분석을 보냅니다. | 예 |
| Edge Network의 [ID](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | 변형에 사용자를 할당하는 데 사용되는 ID를 제공합니다. | 예 |

이러한 확장이 데이터 수집 모바일 속성에 설치되고 앱 종속성에 포함되어 있는지 확인합니다.

## 데이터 수집에서 플래그 확장 구성 {#configure}

### 확장 설치 {#install-extension}

1. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 로그인합니다.

1. **[!UICONTROL 태그]** 메뉴를 선택하고 모바일 속성을 선택합니다.

1. **[!UICONTROL 확장]** > **[!UICONTROL 카탈로그]**(으)로 이동합니다.

1. **[!DNL Adobe Flags]**&#x200B;을(를) 검색하고 **[!UICONTROL 설치]**&#x200B;를 선택합니다.

   ![](../assets/extension-install.png)

1. 확장 설정을 구성합니다.

   * **[!UICONTROL 샌드박스]**: Flags 구성이 포함된 Adobe Experience Platform 샌드박스.
   * **[!UICONTROL 응용 프로그램 ID]**: 플래그에 있는 응용 프로그램의 식별자입니다.

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

1. 구성을 업데이트하려면 [게시 프로세스](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview)를 따르십시오.

### 환경 파일 ID 가져오기 {#environment-file-id}

1. 모바일 속성에서 **[!UICONTROL 환경]**(으)로 이동합니다.

1. 선택한 환경의 **[!UICONTROL 설치]** 열에서 상자 아이콘을 선택합니다.

   ![](../assets/extension-install-2.png)

1. **[!UICONTROL 모바일 설치 지침]** 대화 상자에서 **[!UICONTROL 환경 파일 ID]**&#x200B;를 복사합니다.

   ![](../assets/extension-install-3.png)

## 앱에 플래그 확장 추가 {#add-to-app}

### 종속성 추가 {#add-dependencies}

>[!IMPORTANT]
>
>플래그 확장은 모바일 SDK BOM의 일부가 아닙니다. `<latest-version>`을(를) Maven Central의 최신 버전으로 바꾸십시오. 버전이 없으면 Gradle이 종속성을 해결할 수 없습니다.
>
></br>
&gt;프로덕션 애플리케이션의 경우 Adobe에서는 '3.+'와 같은 동적 버전 대신 명시적 버전 번호를 사용하는 것이 좋습니다. 자세한 내용은 [Managing Gradle dependencies](https://docs.gradle.org/current/userguide/dependency_management.html)를 참조하십시오.

앱의 `build.gradle.kts`(Kotlin) 또는 `build.gradle`(Groovy) 파일에 다음 종속성을 추가하십시오.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation(platform("com.adobe.marketing.mobile:sdk-bom:3.+"))

    // Required extensions (versions managed by the BOM)
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")

    // Flags extension (not managed by the BOM; specify the version)
    implementation("com.adobe.marketing.mobile:flags:<latest-version>")
}
```

>[!TAB Groovy]

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation platform('com.adobe.marketing.mobile:sdk-bom:3.+')

    // Required extensions (versions managed by the BOM)
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'

    // Flags extension (not managed by the BOM; specify the version)
    implementation 'com.adobe.marketing.mobile:flags:<latest-version>'
}
```

>[!ENDTABS]

### SDK 초기화 {#initialize-sdk}

>[!IMPORTANT]
>
>프로덕션 앱의 경우 `LoggingMode.ERROR`만 사용합니다. 릴리스 빌드에 `DEBUG` 또는 `VERBOSE`을(를) 사용하지 마십시오.

Flags 확장 API를 호출하기 전에 `Application` 클래스에서 Mobile SDK을 초기화하십시오. 모바일 속성의 환경 파일 ID를 사용하면 앱이 데이터 수집에 게시한 플래그 설정을 선택하게 됩니다.

`MobileCore.initialize`은(는) Flags 확장을 포함하여 Gradle 종속성에 포함된 모든 Adobe 확장을 등록합니다.

`MobileCore.initialize`을(를) 사용하는 경우 `MobileCore.registerExtensions`, `MobileCore.lifecycleStart` 또는 `MobileCore.lifecyclePause`도 호출하지 마십시오. 이 작업은 자동으로 처리됩니다.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

>[!TAB Java]

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID");
    }
}
```

>[!ENDTABS]

### 응용 프로그램 클래스 등록 {#register-application}

`AndroidManifest.xml`에서 `Application` 클래스 등록:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

### 확장을 수동으로 등록하는 경우 {#register-manually}

앱에서 `MobileCore.initialize`을(를) 사용할 수 없고 확장을 `MobileCore.registerExtensions`에 등록하는 경우 `Flag.EXTENSION`을(를) 목록에 추가하십시오. 기존 `com.adobe.marketing.mobile.Identity`이(가) 아닌 Edge Network 클래스 `com.adobe.marketing.mobile.edge.identity.Identity`의 ID를 사용합니다.

```kotlin
import com.adobe.marketing.mobile.Edge
import com.adobe.marketing.mobile.Lifecycle
import com.adobe.marketing.mobile.MobileCore
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.flags.Flag

MobileCore.setApplication(this)
MobileCore.configureWithAppID("YOUR_ENVIRONMENT_FILE_ID")
MobileCore.registerExtensions(
    listOf(Lifecycle.EXTENSION, Identity.EXTENSION, Edge.EXTENSION, Flag.EXTENSION)
) { }
```

이 설정에서는 라이프사이클이 자동으로 추적되지 않습니다. 모든 활동의 `onResume` 및 `onPause`에서 `MobileCore.lifecyclePause()`을(를) 호출합니다. `MobileCore.lifecycleStart(null)`이러한 호출이 없으면 확장 프로그램은 앱이 백그라운드에 있을 때 플래그를 계속 새로 고치고 노출 분석이 나중에 전송됩니다.

## 평가 컨텍스트 {#evaluation-context}

`FeatureEvaluationContext`은(는) 플래그 규칙에서 사용하는 타깃팅 특성을 보유합니다. ID를 전달하지 않음: 확장이 모든 평가에서 Edge Network용 ID에서 읽습니다. [사용자 지정 ID](#custom-identity)를 참조하십시오.

| 방법 | 필수 | 설명 |
|---|---|---|
| `withAttributes(map)` | 아니요 | `Map<String, List<String>>`. 각 키는 플래그 규칙에 사용되는 특성 이름입니다(예: `locale` 또는 `appVersion`). 각 값은 현재 사용자의 값 목록입니다(예: `["en_US"]`). |

* 모든 평가에 컨텍스트가 필요합니다. 특성이 없으면 `FeatureEvaluationContext.builder().build()`을(를) 전달하십시오.
* 빌더당 최대 한 번까지 `withAttributes`을(를) 호출합니다.
* 빌드된 컨텍스트는 변경할 수 없으므로 평가 간에 재사용할 수 있습니다.

### 사용 {#evaluation-context-usage}

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(
        mapOf(
            "locale" to listOf("en_US"),
            "platform" to listOf("ANDROID")
        )
    )
    .build()
```

>[!TAB Java]

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

>[!ENDTABS]

### 샘플 타깃팅 속성 {#sample-attributes}

| 특성 | 설명 | 값 예 |
|---|---|---|
| `locale` | 사용자의 로케일 | `["en_US"]`, `["fr_FR"]` |
| `platform` | 플랫폼 | `["ANDROID"]` |
| `appVersion` | 앱 버전 | `["3.0.0"]` |
| `deviceType` | 디바이스 유형 | `["phone"]`, `["tablet"]` |

속성 이름 및 값은 플래그 규칙에 사용된 이름과 일치해야 합니다.

## 사용자 정의 ID {#custom-identity}

Flags 확장은 ID 확인을 위해 [Edge Network 확장](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/)에 대한 ID를 사용합니다. 기능 플래그는 사용자 정의 ID(예: CRM ID 또는 로열티 ID)에 코호트될 수 있으므로 변형 분할 및 분석이 애플리케이션에 중요한 ID에 연결됩니다.

기능 플래그가 작성되면 플래그 UI에서 사용자 지정 ID 네임스페이스를 선택해야 합니다. 해당 ID에 대해 플래그를 평가하려면 일치하는 네임스페이스를 사용하여 장치의 Edge ID `identityMap`에 동일한 ID가 있어야 합니다. 런타임 시 Edge Network `updateIdentities` API에 대한 ID를 제공합니다.

### ID 맵에 사용자 지정 ID 추가 {#add-identity}

플래그를 평가하기 전에 기능 플래그에 구성된 동일한 네임스페이스 아래에 ID를 추가합니다.

ID를 추가할 때는 다음 사항에 유의하십시오.

* 네임스페이스는 대/소문자를 포함하여 정확히 일치해야 합니다.
* 네임스페이스에 둘 이상의 ID가 있는 경우 기본으로 표시된 ID가 사용됩니다. 그렇지 않으면 첫 번째 가 사용됩니다.
* 플래그가 평가될 때 ID가 누락되면 앱이 시작될 때마다 변경되는 임시 ID에 의해 사용자가 할당됩니다. 그러면 앱 실행 간에 사용자의 변형이 변경될 수 있습니다. ID를 사용하는 플래그를 평가하기 전에 항상 ID를 설정하십시오.

>[!BEGINTABS]

>[!TAB Kotlin]

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

>[!TAB Java]

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

IdentityMap identityMap = new IdentityMap();
identityMap.addItem(
        new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
        "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

>[!ENDTABS]

## API 참조 {#api-reference}

### 콜백 및 오류 처리 {#callbacks-errors}

이러한 규칙은 `isFeatureEnabled` 및 `getFeature`에 적용됩니다.

* 항상 기본 경험을 제공하십시오. `AdobeCallbackWithError`을(를) 전달하고 `fail`에서 기본 환경을 표시합니다. 일반 `AdobeCallback`을(를) 사용하면 오류가 발생할 때 호출되는 항목이 없습니다.

* 확장은 앱이 시작될 때 플래그 정의를 미리 로드합니다. 그런 다음 플래그는 장치에서 평가됩니다.

* 다른 오류: 다음과 같은 경우 `fail`이(가) `AdobeError.UNEXPECTED_ERROR`(으)로 호출됩니다.

  * 기능 키가 비어 있습니다.
  * 플래그 설정 또는 Experience Cloud 조직 ID가 게시된 구성에서 누락되었거나
  * 앱이 시작될 때(예: 장치가 오프라인 상태임) 플래그 정의를 다운로드할 수 없습니다. 확장은 다음 구성 업데이트(일반적으로 다음 앱 실행)에서 다시 시도합니다.

### isFeatureEnabled {#is-feature-enabled}

현재 사용자에 대해 기능이 활성화되어 있는지 여부를 반환합니다.

**서명**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

>[!TAB Java]

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

>[!ENDTABS]

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 평가할 기능의 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 타깃팅 속성입니다. 항목이 없으면 `FeatureEvaluationContext.builder().build()`을(를) 사용합니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `callback` | AdobeCallback&lt;부울> | 이 기능이 사용자에 대해 활성화되어 있으면 `true`(으)로 호출됩니다. 기능을 찾을 수 없거나 타깃팅 규칙이 일치하지 않거나 사용자가 컨트롤 그룹에 있는 경우 `false`을(를) 사용하여 호출됩니다. 오류도 받으려면 `AdobeCallbackWithError<Boolean>`을(를) 전달하십시오. |

**예**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<Boolean> {
        override fun call(isEnabled: Boolean?) {
            runOnUiThread {
                if (isEnabled == true) showNewCheckout() else showDefaultCheckout()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultCheckout() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            runOnUiThread(() -> {
                if (Boolean.TRUE.equals(isEnabled)) {
                    showNewCheckout();
                } else {
                    showDefaultCheckout();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultCheckout());
        }
    }
);
```

>[!ENDTABS]

### getFeature {#get-feature}

메타데이터를 포함하여 현재 사용자에 대해 평가된 기능을 반환합니다. 활성화하거나 비활성화해야 할 때 이 API를 사용하십시오.

**서명**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

>[!TAB Java]

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

>[!ENDTABS]

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 평가할 기능의 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 타깃팅 속성입니다. 항목이 없으면 `FeatureEvaluationContext.builder().build()`을(를) 사용합니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult> | 평가된 기능을 사용하여 호출되거나, 키가 알 수 없거나, 타깃팅 기준이 충족되지 않거나, 사용자가 제어 집단에 있는 경우 해당 기능이 사용자에게 제공되지 않으면 `null`과(와) 함께 호출됩니다. `null`은(는) 오류가 아닌 일반적인 결과입니다. 통제 집단 노출은 여전히 분석에 보고됩니다. `AdobeCallbackWithError<FeatureEvaluationResult>`을(를) 전달하여 시간 초과와 같은 실제 실패에 대해 `fail(...)`을(를) 받습니다. |

`null` 결과를 &quot;기능 끄기&quot;로 취급하고 기본 환경을 표시합니다. `fail`이(가) 호출될 때 시간 초과와 같은 실제 오류에서만 발생하는 기본 경험도 표시합니다.

**응답**

*FeatureEvaluationResult*

| 필드 | 유형 | 설명 |
|---|---|---|
| `id` | 정수 | 기능 ID |
| `key` | 문자열 | 기능 키 |
| `featureGroupKey` | 문자열? | 피쳐가 그룹에 속하는 경우 피쳐 그룹 키 |
| `meta` | 문자열? | 기능에 대해 구성된 메타데이터입니다(일반 텍스트로 설정됨). 또는 `null`(설정되지 않은 경우)입니다. JSON을 저장한 경우 앱의 문자열을 구문 분석합니다. |
| `analyticsParam` | AnalyticsParam? | 평가를 위한 Analytics 세부 정보 |

*AnalyticsParam*

| 필드 | 유형 | 설명 |
|---|---|---|
| `featureGroupId` | 정수 | 기능 그룹 ID |
| `featureId` | 정수 | 기능 ID |
| `variantId` | 문자열? | 사용자가 할당된 변형의 ID |

**예**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            runOnUiThread {
                if (!meta.isNullOrEmpty()) applyExperience(meta) else showDefaultExperience()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultExperience() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            final String meta = feature != null ? feature.getMeta() : null;
            runOnUiThread(() -> {
                if (meta != null && !meta.isEmpty()) {
                    applyExperience(meta);
                } else {
                    showDefaultExperience();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultExperience());
        }
    }
);
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Flags 확장 버전을 반환합니다.

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
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. [isFeatureEnabled](#is-feature-enabled)을(를) 참조하십시오. | 콜백을 통한 부울 |
| `getFeature(featureKey, evaluationContext, callback)`. [getFeature](#get-feature)을(를) 참조하십시오. | 콜백을 통한 FeatureEvaluationResult |
| `extensionVersion()` | 문자열 |

## 디버깅 {#debugging}

디버그하려면 디버그 빌드에 `MobileCore.setLogLevel(LoggingMode.DEBUG)`을(를) 설정하고 Logcat을 `Flags`(으)로 필터링합니다. `com.adobe.marketing.mobile.flags.FlagExtension`에 대한 MobileCore에서 `Discovered extension` 메시지가 표시됩니다.


