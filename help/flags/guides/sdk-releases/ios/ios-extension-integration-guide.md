---
title: iOS 통합 안내서의 플래그 확장
description: Flags 확장을 iOS의 Adobe Experience Platform Mobile SDK과 통합하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
hide: true
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 5%

---

# iOS용 플래그 확장 {#ios-extension-integration-guide}

이 안내서에서는 iOS에서 Adobe Experience Platform Mobile SDK과 플래그 확장을 통합하는 방법을 설명합니다.

## 사전 요구 사항 {#prerequisites}

Flags 확장을 구현하기 전에 다음을 확인하십시오.

* [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에 구성된 모바일 속성
* 모바일 속성에 설치되고 구성된 플래그 확장
* Adobe Experience Cloud 조직 ID
* 최소 배포 대상: iOS 12.0

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

#### Swift 패키지 관리자 사용 {#swift-package-manager}

Xcode에서 **파일** > **패키지 추가**&#x200B;를 선택하고 다음 Adobe Experience Platform Mobile SDK 패키지 URL을 추가합니다.

| 패키지 | URL |
|---|---|
| AEPCore | `https://github.com/adobe/aepsdk-core-ios.git` |
| AEPEDGE | `https://github.com/adobe/aepsdk-edge-ios.git` |
| AEPEdgeIdentity | `https://github.com/adobe/aepsdk-edgeidentity-ios.git` |

메시지가 표시되면 다음 라이브러리를 선택하여 타겟에 추가합니다.

* `AEPCore`, `AEPLifecycle`(`aepsdk-core-ios`부터)
* `AEPEdge`(`aepsdk-edge-ios`부터)
* `AEPEdgeIdentity`(`aepsdk-edgeidentity-ios`부터)

AEPCore 5.8.0 이상을 사용합니다.

>[!NOTE]
>
>Xcode에서 패키지를 추가할 때 각 패키지에 대한 종속성 규칙(예: **다음 메이저 버전까지**)을 선택합니다. 이 규칙은 다음 메이저 버전을 제외하는 동안 새로운 마이너 및 패치 릴리스를 자동으로 선택합니다. 최신 릴리스 버전은 GitHub에서 각 확장의 릴리스 페이지를 확인하십시오.

### 플래그 패키지 추가 {#add-flags-package}

앱 대상에 대해 Swift 패키지 또는 XCFramework 통합 방법을 사용하고 둘 다 사용하지 마십시오.

#### Package.swift 파일이 없는 Xcode 프로젝트의 경우 {#xcode-project}

1. Xcode에서 **파일** > **패키지 추가**&#x200B;를 선택합니다.
1. **로컬 추가**&#x200B;를 선택합니다.
1. `Package.swift`이(가) 포함된 제공된 `Packages/AEPFlags` 디렉터리를 선택하십시오.
1. 응용 프로그램 대상에 `AEPFlags` 라이브러리를 추가합니다.

Xcode는 프로젝트에 로컬 패키지 참조를 저장하므로 응용 프로그램에는 자체 `Package.swift` 파일이 필요하지 않습니다.

#### Package.swift 파일이 있는 프로젝트의 경우 {#package-swift-project}

기존 매니페스트에서 응용 프로그램 대상 종속성에 `AEPFlags`을(를) 추가하고 제공된 매니페스트의 URL 및 체크섬을 사용하여 이진 대상을 추가합니다.

```swift
targets: [
    .target(
        name: "YourApp",
        dependencies: [
            "AEPFlags"
        ]
    ),
    .binaryTarget(
        name: "AEPFlags",
        url: "<AEPFlags binary URL>",
        checksum: "<AEPFlags binary checksum>"
    )
]
```

Swift Package Manager는 로컬 Xcode, CI 및 아카이브 빌드에 대한 이진 대상을 확인합니다.

#### XCFramework를 직접 추가합니다. {#xcframework}

또는 제공된 `AEPFlags.xcframework`을(를) Xcode 프로젝트 탐색기로 드래그하여 응용 프로그램 대상에 추가합니다. **일반** > **프레임워크, 라이브러리 및 포함된 콘텐츠**&#x200B;에서 프레임워크를 **포함 및 서명**&#x200B;으로 설정하십시오.

### SDK 초기화 {#initialize-sdk}

Flags API를 호출하기 전에 `AppDelegate`에서 Mobile SDK 확장을 등록하십시오. ID, Edge 및 라이프사이클 뒤에 `Flag`을(를) 등록한 다음 모바일 속성의 환경 파일 ID를 사용하여 SDK을 구성합니다.

#### 확장 등록 및 구성 {#register-configure}

>[!IMPORTANT]
>
>프로덕션 앱의 경우 `.error` 로그 수준만 사용합니다. 릴리스 빌드에서는 `.debug` 또는 `.trace`을(를) 사용하지 마십시오.

**Swift**

```swift
// AppDelegate.swift
import AEPCore
import AEPLifecycle
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import UIKit

final class AppDelegate: NSObject, UIApplicationDelegate {

    func application(_: UIApplication,
                      didFinishLaunchingWithOptions _: [UIApplication.LaunchOptionsKey: Any]? = nil) -> Bool {
        // Production: use .error only. Do not use .debug or .trace in release builds.
        MobileCore.setLogLevel(.error)

        MobileCore.registerExtensions([
            Identity.self,
            Edge.self,
            Lifecycle.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "YOUR_ENVIRONMENT_FILE_ID")
            MobileCore.lifecycleStart(additionalContextData: nil)
        }

        return true
    }
}
```

**Objective-C**

```objc
// AppDelegate.m
#import "AppDelegate.h"
@import AEPCore;
@import AEPLifecycle;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;

@implementation AppDelegate

- (BOOL)application:(UIApplication *)application
    didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {

    // Production: use AEPLogLevelError only. Do not use Debug or Trace in release builds.
    [AEPMobileCore setLogLevel:AEPLogLevelError];

    [AEPMobileCore registerExtensions:@[
        AEPMobileEdgeIdentity.class,
        AEPMobileEdge.class,
        AEPMobileLifecycle.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"YOUR_ENVIRONMENT_FILE_ID"];
        [AEPMobileCore lifecycleStart:nil];
    }];

    return YES;
}

@end
```

## 평가 컨텍스트 {#evaluation-context}

`FeatureEvaluationContext`에 타겟팅 특성이 포함되어 있습니다(플래그 규칙 일치에 사용됨).

| 매개 변수 | 필수 여부 | 설명 |
|---|---|---|
| `attributes` | 아니요 | `[String: [String]]`. 키는 플래그 규칙에 사용되는 컨텍스트 특성 이름입니다(예: `locale`, `platform`, `appVersion`, `deviceType`). 값은 현재 사용자/세션에 대한 해당 키의 후보 특성 값 목록입니다(예: `["en_US"]` 또는 `["phone"]`). |

**Swift**

```swift
import AEPFlags

let attrs: [String: [String]] = [
    "locale": ["en_US"],
    "platform": ["IOS"],
    "appVersion": ["3.0.0"]
]

let ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Objective-C**

```objc
@import AEPFlags;

NSDictionary<NSString *, NSArray<NSString *> *> *attrs = @{
    @"locale": @[@"en_US"],
    @"platform": @[@"IOS"],
    @"appVersion": @[@"3.0.0"]
};

AEPFeatureEvaluationContextBuilder *builder = [AEPFeatureEvaluationContext builder];
AEPFeatureEvaluationContext *ctx = [[builder withAttributes:attrs] build];
```

### 샘플 타깃팅 속성 {#sample-attributes}

| 특성 | 설명 | 값 예 |
|---|---|---|
| `locale` | 사용자의 로케일/언어 | `["en_US"]`, `["fr_FR"]` |
| `platform` | 플랫폼 식별자 | `["IOS"]` |
| `appVersion` | 애플리케이션 버전 | `["3.0.0"]` |
| `deviceType` | 디바이스 유형 | `["phone"]`, `["tablet"]` |

### 사용자 정의 ID {#custom-identity}

플래그 확장은 ID 확인을 위해 Edge Network용 ID 확장을 사용합니다. 기능 플래그는 사용자 지정 ID(예: CRM ID 또는 로열티 ID)에 코호트되어 변형 분할 및 분석이 애플리케이션에 중요한 ID에 연결될 수 있습니다.

기능 플래그가 작성되면 플래그 UI에서 사용자 지정 ID 네임스페이스를 선택해야 합니다. 해당 ID에 대해 플래그를 평가하려면 일치하는 네임스페이스를 사용하여 장치의 Edge ID `identityMap`에 동일한 ID가 있어야 합니다. 런타임 시 Edge Network `updateIdentities` API에 대한 ID를 제공합니다.

#### ID 맵에 사용자 지정 ID 추가 {#add-identity}

기능 플래그에 구성된 동일한 네임스페이스 아래에 ID를 추가합니다.

**Swift**

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
                 withNamespace: "userCRMId") // must match the namespace configured on the feature flag
Identity.updateIdentities(with: identityMap)
```

**Objective-C**

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc]
    initWithId:@"1111"
    authenticatedState:AEPAuthenticatedStateAuthenticated
    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

## API 참조 {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled`은(는) 특정 컨텍스트에 대해 플래그 기능이 설정되어 있는지 여부를 반환합니다. `featureKey`, `FeatureEvaluationContext`(선택적 타깃팅 특성) 및 완료 닫기를 전달합니다. [평가 컨텍스트](#evaluation-context)를 참조하십시오.

**서명**

*Swift*

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void
)
```

*Objective-C*

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
               completion:(void (^)(BOOL))completion;
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `completion` | `(Bool) -> Void` | 기능이 활성화된 경우 `true`(으)로 호출되고 그렇지 않은 경우 `false`로 호출됩니다. |

**예**

*Swift*

```swift
import AEPFlags

Flag.isFeatureEnabled(
    "new-flag",
    evaluationContext: ctx
) { isEnabled in
    if isEnabled {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:ctx
                      completion:^(BOOL isEnabled) {
    if (isEnabled) {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}];
```

### getFeature {#get-feature}

`getFeature`이(가) 제공된 컨텍스트에 대해 평가된 기능 페이로드를 반환합니다. 활성화/비활성화보다 더 필요하고 기능 메타데이터 또는 값을 원하는 경우 이 API를 사용하십시오.

**서명**

*Swift*

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void
)
```

*Objective-C*

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion;
```

**매개 변수**

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| `featureKey` | 문자열 | 플래그에서 평가할 기능 키 |
| `evaluationContext` | 기능 평가 컨텍스트 | 필요에 따라 타깃팅 특성을 포함합니다. 빈 컨텍스트의 경우 `FeatureEvaluationContext.builder().build()`을(를) 사용하십시오. [평가 컨텍스트](#evaluation-context)를 참조하십시오. |
| `completion` | `(FeatureEvaluationResult?) -> Void` | 평가된 기능 페이로드로 호출됩니다. 기능을 찾을 수 없을 때 `nil`. |

**응답**

*FeatureEvaluationResult*

| 필드 | 유형 | 설명 |
|---|---|---|
| `id` | 정수 | 숫자 기능 식별자 |
| `key` | 문자열 | 기능 키 |
| `featureGroupKey` | 문자열? | 사용 가능한 경우 기능 그룹 키 |
| `meta` | 문자열? | 사용 가능한 경우 불투명 기능 메타데이터 |
| `analyticsParam` | AnalyticsParam? | 평가된 기능에 대한 Analytics 세부 정보 |

*AnalyticsParam*

| 필드 | 유형 | 설명 |
|---|---|---|
| `featureGroupId` | 정수 | 숫자 기능 그룹 식별자 |
| `featureId` | 정수 | 숫자 기능 식별자 |
| `variantId` | 문자열? | 변형 식별자 |

**예**

*Swift*

```swift
import AEPFlags

Flag.getFeature(
    "new-flag",
    evaluationContext: ctx
) { feature in
    guard let meta = feature?.meta, !meta.isEmpty else {
        // No metadata available: fall back to the default behavior
        return
    }
    // Feature metadata is available: use it to drive the feature behavior
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:ctx
                completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    NSString *meta = feature.meta;
    if (meta.length > 0) {
        // Feature metadata is available: use it to drive the feature behavior
    } else {
        // No metadata available: fall back to the default behavior
    }
}];
```

### extensionVersion {#extension-version}

Flags 확장의 버전 문자열을 반환합니다.

**구문**

*Swift*

```swift
static var extensionVersion: String
```

*Objective-C*

```objc
+ (nonnull NSString *)flagExtensionVersion;
```

**예**

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
| `isFeatureEnabled(_:evaluationContext:completion:)`. `FeatureEvaluationContext`은(는) 규칙에 대한 타깃팅 특성을 전달합니다. [isFeatureEnabled](#is-feature-enabled)을(를) 참조하십시오. | 완료 닫기를 통한 부울 |
| `getFeature(_:evaluationContext:completion:)`. 특정 컨텍스트에 대해 평가된 기능 페이로드를 반환합니다. [getFeature](#get-feature)을(를) 참조하십시오. | 기능 평가 결과? 폐쇄를 통함 |
| `extensionVersion` | 문자열 |

## 참조: {#see-also}

* [모바일 애플리케이션](../../integrate/mobile-applications.md)
* [SDK](../../integrate/sdks.md)
* [Android 확장 통합 안내서](../android/android-extension-integration-guide.md)

<!-- -->
