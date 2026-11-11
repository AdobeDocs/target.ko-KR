---
title: iOS 통합 안내서의 플래그 확장
description: Flags 확장을 iOS의 Adobe Experience Platform Mobile SDK과 통합하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
hide: true
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 3%
---
# iOS용 플래그 확장 {#ios-extension-integration-guide}

이 안내서에서는 iOS에서 Adobe Experience Platform Mobile SDK과 플래그 확장을 통합하는 방법을 설명합니다. 소스 코드는 [aepsdk-flags-ios](https://github.com/adobe/aepsdk-flags-ios) 리포지토리에서 사용할 수 있습니다.

## 사전 요구 사항 {#prerequisites}

시작하기 전에 다음을 확인하십시오.

* iOS 12.0 이상 및 Swift 5.7 이상
* [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)의 모바일 속성
* 이러한 확장은 모바일 속성에 설치되고 구성됩니다.

  | 확장 | 설명 | 최소 SDK 버전 |
  |---|---|---|
  | [모바일 코어](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | 구성 및 이벤트 처리 | AEPCore 5.8.0 |
  | [라이프사이클](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | 애플리케이션 라이프사이클 데이터 | AEPCore와 동일 |
  | [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Adobe Experience Platform Edge Network과의 통신. 데이터 스트림이 필요합니다. | AEPEdge 5.0.2 |
  | Edge Network의 [ID](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Edge Network용 ID 관리 | AEPEdgeIdentity 5.0.0 |
  | [플래그](https://experienceleague.adobe.com/ko/docs/target/flags/home) | 기능 플래그 평가 | [설치](#installation) 참조 |

## 데이터 수집에서 플래그 구성 {#configure}

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

1. 구성을 업데이트하려면 [게시 프로세스](https://experienceleague.adobe.com/ko/docs/experience-platform/tags/publish/overview)를 따르십시오.

### 환경 파일 ID 가져오기 {#environment-file-id}

1. 모바일 속성에서 **[!UICONTROL 환경]**(으)로 이동합니다.

1. 선택한 환경의 **[!UICONTROL 설치]** 열에서 상자 아이콘을 선택합니다.

   ![](../assets/extension-install-2.png)

1. **[!UICONTROL 모바일 설치 지침]** 대화 상자에서 **[!UICONTROL 환경 파일 ID]**&#x200B;를 복사합니다.

   ![](../assets/extension-install-3.png)

## 설치 {#installation}

Swift 패키지 관리자 또는 XCFramework를 사용하여 확장을 추가합니다. 앱 대상당 하나의 메서드를 사용합니다.

### Swift 패키지 관리자 {#swift-package-manager}

Xcode에서:

1. **파일** > **패키지 종속성 추가**&#x200B;를 선택합니다.

1. 패키지 URL 입력: `https://github.com/adobe/aepsdk-flags-ios.git`

1. 버전 규칙을 사용하려면 **정확한 버전**&#x200B;을 선택하고 [릴리스 페이지](https://github.com/adobe/aepsdk-flags-ios/releases)에서 최신 버전을 입력하십시오.

1. 앱 대상에 `AEPFlags` 라이브러리를 추가합니다.

1. 확장이 의존하는 Adobe 패키지를 추가하고 해당 라이브러리를 앱 타겟에 추가합니다.

   * `https://github.com/adobe/aepsdk-core-ios.git`: `AEPCore`, `AEPLifecycle` 및 `AEPServices`
   * `https://github.com/adobe/aepsdk-edge-ios.git`: `AEPEdge`
   * `https://github.com/adobe/aepsdk-edgeidentity-ios.git`: `AEPEdgeIdentity`

프로젝트에서 `Package.swift` 파일을 사용하는 경우 종속성을 대신 추가하십시오. 릴리스 페이지에서 `<latest-version>`을(를) 최신 버전으로 바꾸십시오.

```swift
dependencies: [
    .package(url: "https://github.com/adobe/aepsdk-flags-ios.git", exact: "<latest-version>"),
    .package(url: "https://github.com/adobe/aepsdk-core-ios.git", .upToNextMajor(from: "5.8.0")),
    .package(url: "https://github.com/adobe/aepsdk-edge-ios.git", .upToNextMajor(from: "5.0.2")),
    .package(url: "https://github.com/adobe/aepsdk-edgeidentity-ios.git", .upToNextMajor(from: "5.0.0"))
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AEPFlags", package: "aepsdk-flags-ios"),
            .product(name: "AEPCore", package: "aepsdk-core-ios"),
            .product(name: "AEPLifecycle", package: "aepsdk-core-ios"),
            .product(name: "AEPServices", package: "aepsdk-core-ios"),
            .product(name: "AEPEdge", package: "aepsdk-edge-ios"),
            .product(name: "AEPEdgeIdentity", package: "aepsdk-edgeidentity-ios")
        ]
    )
]
```

### XCFramework {#xcframework}

1. [릴리스 페이지](https://github.com/adobe/aepsdk-flags-ios/releases)에서 `AEPFlags-<version>.xcframework.zip`을(를) 다운로드하고 압축을 풉니다.

1. 확장이 각 저장소의 릴리스 페이지에서 의존하는 XCFrameworks를 다운로드합니다.

   * [aepsdk-core-ios 릴리스](https://github.com/adobe/aepsdk-core-ios/releases): `AEPCore`, `AEPServices`, `AEPLifecycle` 및 `AEPRulesEngine`
   * [aepsdk-edge-ios 릴리스](https://github.com/adobe/aepsdk-edge-ios/releases): `AEPEdge`
   * [aepsdk-edgeidentity-ios 릴리스](https://github.com/adobe/aepsdk-edgeidentity-ios/releases): `AEPEdgeIdentity`

1. Xcode에서 앱 대상을 선택한 다음 **일반** > **프레임워크, 라이브러리 및 포함된 콘텐츠**&#x200B;를 엽니다.

1. `AEPFlags.xcframework` 및 모든 종속 XCFrameworks를 추가합니다.

1. 각 프레임워크를 **포함 및 서명**(으)로 설정합니다.

## SDK 초기화 {#initialize-sdk}

Flags 확장을 등록한 다음 모바일 속성에서 환경 파일 ID로 SDK을 초기화합니다. `MobileCore.initialize`이(가) Flags 확장을 등록하지 않으므로 먼저 등록하십시오.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPFlags
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([Flag.self])
        MobileCore.initialize(appId: "<your-environment-file-id>")
        return true
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPFlags;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[AEPMobileFlag.class] completion:nil];
    [AEPMobileCore initializeWithAppId:@"<your-environment-file-id>" completion:nil];
    return YES;
}
```

>[!ENDTABS]

### 수동으로 확장 등록 {#register-manually}

확장을 직접 등록하는 경우 모든 확장을 등록합니다. 앱이 전경에 들어가면 `MobileCore.lifecycleStart`을(를) 호출하고, 배경에 들어가면 `MobileCore.lifecyclePause`을(를) 호출합니다.

앱이 장면을 사용하는 경우 대신 `sceneWillEnterForeground(_:)` 및 `sceneDidEnterBackground(_:)`에서 이 호출을 수행합니다.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import AEPLifecycle
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([
            Lifecycle.self,
            Edge.self,
            AEPEdgeIdentity.Identity.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "<your-environment-file-id>")
            DispatchQueue.main.async {
                if application.applicationState != .background {
                    MobileCore.lifecycleStart(additionalContextData: nil)
                }
            }
        }
        return true
    }

    func applicationWillEnterForeground(_ application: UIApplication) {
        MobileCore.lifecycleStart(additionalContextData: nil)
    }

    func applicationDidEnterBackground(_ application: UIApplication) {
        MobileCore.lifecyclePause()
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;
@import AEPLifecycle;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[
        AEPMobileLifecycle.class,
        AEPMobileEdge.class,
        AEPMobileEdgeIdentity.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"<your-environment-file-id>"];
        dispatch_async(dispatch_get_main_queue(), ^{
            if (application.applicationState != UIApplicationStateBackground) {
                [AEPMobileCore lifecycleStart:nil];
            }
        });
    }];
    return YES;
}

- (void)applicationWillEnterForeground:(UIApplication *)application {
    [AEPMobileCore lifecycleStart:nil];
}

- (void)applicationDidEnterBackground:(UIApplication *)application {
    [AEPMobileCore lifecyclePause];
}
```

>[!ENDTABS]

## 평가 컨텍스트 {#evaluation-context}

모든 평가 호출에는 `FeatureEvaluationContext`이(가) 필요합니다. 플래그의 타겟팅 규칙이 사용하는 속성을 보유합니다.

| 매개 변수 | 필수 여부 | 설명 |
|---|---|---|
| `attributes` | 아니요 | `[String: [String]]`. 각 키는 플래그 타겟팅 규칙에 사용되는 속성 이름입니다. 각 값은 현재 사용자의 값 목록입니다. |

* 플래그에 정의한 타겟팅 규칙과 일치하는 속성 이름 및 값을 사용합니다.
* 빌더당 최대 한 번까지 `withAttributes`을(를) 호출합니다. 두 번째 호출은 앱을 종료합니다.
* 특성 없이 평가하려면 `withAttributes`을(를) 호출하지 않고 `build()`을(를) 호출하십시오.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPFlags

let context = FeatureEvaluationContext.builder()
    .withAttributes([
        "locale": ["en_US"],
        "appVersion": ["3.0.0"]
    ])
    .build()
```

>[!TAB Objective-C]

```objc
@import AEPFlags;

AEPFeatureEvaluationContext *context = [[[AEPFeatureEvaluationContext builder]
    withAttributes:@{
        @"locale": @[@"en_US"],
        @"appVersion": @[@"3.0.0"]
    }]
    build];
```

>[!ENDTABS]

## 사용자 정의 ID {#custom-identity}

플래그 확장은 ID 확인을 위해 Edge Network용 ID 확장을 사용합니다. 기능 플래그는 사용자 지정 ID(예: CRM ID 또는 로열티 ID)에 코호트되어 변형 분할 및 분석이 애플리케이션에 중요한 ID에 연결될 수 있습니다.

기능 플래그가 작성되면 플래그 UI에서 사용자 지정 ID 네임스페이스를 선택해야 합니다. 해당 ID에 대해 플래그를 평가하려면 일치하는 네임스페이스를 사용하여 장치의 Edge ID `identityMap`에 동일한 ID가 있어야 합니다. 런타임 시 Edge Network `updateIdentities` API에 대한 ID를 제공합니다.

### ID 맵에 사용자 지정 ID 추가 {#add-identity}

기능 플래그에 구성된 동일한 네임스페이스 아래에 ID를 추가합니다.

다음 동작을 참고하십시오.

* 네임스페이스는 대문자와 소문자를 포함하여 플래그에 구성된 네임스페이스와 정확히 일치해야 합니다.
* 네임스페이스에 여러 ID가 있는 경우 기본으로 표시된 ID가 사용됩니다. 기본 항목으로 표시된 항목이 없으면 첫 번째 항목이 사용됩니다.
* ID가 누락된 경우 호출이 실패하지 않습니다. 사용자는 현재 앱 세션에 대해서만 임의로 변형에 할당되며, 앱이 다시 시작된 후 다른 변형에 할당할 수 있습니다. ID를 사용하는 플래그를 평가하기 전에 ID를 설정하십시오.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(
    item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
    withNamespace: "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(with: identityMap)
```

>[!TAB Objective-C]

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc] initWithId:@"1111"
                                         authenticatedState:AEPAuthenticatedStateAuthenticated
                                                    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

>[!ENDTABS]


## API 참조 {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

현재 사용자에 대해 기능이 활성화되어 있는지 확인합니다. 기능이 있고 사용자가 타겟팅 규칙과 일치하며 사용자가 컨트롤 그룹에 없는 경우 결과는 `true`입니다. 그렇지 않으면 결과는 `false`입니다.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
              completion:(void (^)(BOOL))completion
           errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `completion` | `(Bool) -> Void` | 기능이 활성화된 경우 `true`(으)로 호출되고 그렇지 않은 경우 `false`로 호출됩니다. |
| `errorCallback` | `((AEPError) -> Void)?` | 선택 사항입니다. 빈 키, 구성 누락, 평가 실패 또는 시간 초과와 같은 정품 실패에 대해서만 호출됩니다. |

**예**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.isFeatureEnabled("new-flag", evaluationContext: context) { isEnabled in
    DispatchQueue.main.async {
        if isEnabled {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:context
                     completion:^(BOOL isEnabled) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (isEnabled) {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### getFeature {#get-feature}

>[!IMPORTANT]
>
>이전 버전에서는 기능이 제공되지 않을 때 `AEPError.unexpected`을(를) 사용하여 오류 콜백을 호출했습니다. 앱이 해당 오류를 &quot;기능 누락&quot;으로 처리하면 대신 완료에서 `nil`을(를) 처리하십시오.

메타데이터 및 사용자가 할당된 변형을 포함하여 현재 사용자에 대한 기능의 세부 정보를 반환합니다. 활성화되거나 비활성화되는 것보다 더 많은 것이 필요할 때 사용하십시오.

완료는 기능이 사용자에게 제공될 때만 결과와 함께 호출됩니다. 기능이 제공되지 않으면 완료는 `nil`(으)로 호출됩니다. 이는 오류가 아닌 일반적인 결과이며 오류 콜백은 호출되지 않습니다. 다음 경우에 완료 호출이 `nil`과(와) 함께 호출됩니다.

* 이 키를 가진 기능이 없습니다.
* 사용자가 타겟팅 규칙과 일치하지 않습니다.
* 사용자가 컨트롤 그룹에 있습니다.

오류 콜백은 기능 키가 비어 있거나, 필요한 구성 값이 없거나, 평가에 실패하거나, 응답을 읽을 수 없거나, 요청 시간이 초과되는 경우에만 `AEPError.unexpected`(또는 다른 `AEPError`)과 함께 호출됩니다.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion
     errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `completion` | `(FeatureEvaluationResult?) -> Void` | 평가된 기능 페이로드를 사용하여 호출됩니다. 알 수 없는 키, 일치하지 않는 타기팅 또는 컨트롤 그룹 등 사용자에게 기능이 제공되지 않을 때 `nil`과(와) 함께 호출됩니다. `nil`은(는) 오류가 아닙니다. |
| `errorCallback` | `((AEPError) -> Void)?` | 선택 사항입니다. 빈 키, 구성 누락, 평가 실패 또는 시간 초과와 같은 정품 실패에 대해서만 호출됩니다. 기능이 제공되지 않으면 호출되지 않습니다. |

**응답**

*FeatureEvaluationResult*

| 필드 | 유형 | 설명 |
|---|---|---|
| `id` | 정수 | 기능 ID |
| `key` | 문자열 | 기능 키 |
| `featureGroupKey` | 문자열? | 피쳐를 포함하는 피쳐 그룹의 키 |
| `meta` | 문자열? | 기능에 대해 구성된 메타데이터입니다. 메타데이터가 JSON인 경우 앱에서 디코딩합니다. |
| `analyticsParam` | AnalyticsParam? | 기능 및 사용자 변형의 식별자 |

**예**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.getFeature("new-flag", evaluationContext: context) { feature in
    DispatchQueue.main.async {
        guard let meta = feature?.meta, !meta.isEmpty else {
            // The feature is not served to this user (feature is nil), or it has no metadata.
            // Run the default behavior
            return
        }
        // Use the metadata to drive the feature behavior
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // A genuine failure occurred. Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:context
               completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (feature.meta.length > 0) {
            // Use the metadata to drive the feature behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Flags 확장 버전을 반환합니다.

*Swift*

```swift
let version = Flag.extensionVersion
```

*Objective-C*

```objc
NSString *version = [AEPMobileFlag flagExtensionVersion];
```

## API 요약 {#api-summary}

| API | 반환 |
|---|---|
| `isFeatureEnabled(_:evaluationContext:completion:errorCallback:)` | 완료 때까지 부울 |
| `getFeature(_:evaluationContext:completion:errorCallback:)` | 기능 평가 결과? 완료 후 |
| `extensionVersion` | 문자열 |
