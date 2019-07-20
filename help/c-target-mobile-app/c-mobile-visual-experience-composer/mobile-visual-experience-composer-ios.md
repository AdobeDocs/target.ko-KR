---
description: Adobe Target 모바일 VEC(시각적 경험 작성기)를 사용하여 개발자는 iOS 모바일 앱에서 일회성 설정을 수행하고 마케터는 모바일 앱 VEC의 기능을 사용할 수 있습니다.
keywords: 모바일 앱 VEC;모바일 시각적 경험 작성기;모바일 경험 작성기 선택 사항;설정;ios;apple
seo-description: Adobe Target 모바일 VEC(시각적 경험 작성기)를 사용하여 개발자는 iOS 모바일 앱에서 일회성 설정을 수행하고 마케터는 모바일 앱 VEC의 기능을 사용할 수 있습니다.
seo-title: iOS - 모바일 앱 설정
solution: Target
title: iOS - 모바일 앱 설정
topic: Standard
uuid: 6db4f06a-d8f4-4192-af6f-917594e721e6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# iOS - 모바일 앱 설정{#ios-set-up-the-mobile-app}

Adobe Target 모바일 앱 VEC(시각적 경험 작성기)를 사용하여 개발자는 iOS 모바일 앱에서 일회성 설정을 수행하고 마케터는 모바일 앱 VEC의 기능을 사용할 수 있습니다.

Adobe Target VEC 확장 프로그램 활성화에 대한 자세한 내용은 [Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec)에서 *Adobe Target - 시각적 경험 작성기*&#x200B;를 참조하십시오.

## Mobile SDK 및 Target 라이브러리 포함 {#sdk-library}

1. 'Pod [!DNL Podfile]'(을)를 추가하여 Cocoapods를 통해 프로젝트에 라이브러리를 추가합니다.`ACPTargetVEC`

1. XCode에서 Objective-C 애플리케이션 프로젝트를 엽니다.

1. 아직 설정되지 않았다면 프로젝트 빌드 설정으로 이동하여 'Always Embed swift Standard Libraries'를 Yes로 설정합니다.

1. 프로젝트 빌드 설정에서 "Other linker flags"를 찾고 아직 없는 경우 `$(inherited)`를 추가합니다.

1. objective-C 전용 프로젝트의 경우 - 스위프트 파일을 만들어 브릿징 헤더를 만듭니다. Swift를 위한 애플리케이션 환경을 설정하게 됩니다.

1. 딥링크 핸들러를 추가합니다.

   1. 애플리케이션 프로젝트 설정에서 **[!UICONTROL 정보를 클릭합니다]**.
   1. **[!UICONTROL URL 유형]**&#x200B;에서 삼각형을 클릭하여 연 다음 더하기 기호를 클릭하여 새 필드를 추가합니다.
   1. 다음 정보를 추가합니다.

      * 식별자: `com.adobe.sdktest`
      * URL 체계: `vectester`
      * 역할: 편집기
   1. 애플리케이션 프로젝트 설정 &gt; **[!UICONTROL 일반 바깥쪽을 클릭합니다]**.
   1. 애플리케이션 프로젝트 설정 &gt; **[!UICONTROL 정보]에서 뒤로를 클릭하여 설정이 저장되었는지 확인하십시오.**

      예제 URL 유형을 사용하면 앱의 URL 체계는 다음과 같습니다.

      ```
      vectester://com.adobe.sdktest
      ```


1. XCode에서 [!DNL AppDelegate] 파일을 엽니다.

1. 파일 맨 위에서 가져오기 끝에 다음 줄을 추가합니다:

   `#import "ACPTargetVEC.h"`

   Swift를 사용하는 경우 다음 줄을 추가합니다.

   `import ACPTargetVEC`

1. [!DNL AppDelegate] 파일에서 다음 줄을 `AppDelegate::application:didFinishLaunchingWithOptions:`에 추가합니다. 위임 함수가 정의되지 않은 경우에는 작성하여 Objective-C 또는 Swift 애플리케이션의 다음 줄을 각각 추가합니다.

   ```
   // CONFIGURATION LINE FOR OBJECTIVE C ONLY
   - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
     //Other Extensions that you need
     [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"];
     [ACPCore setLogLevel:ACPMobileLogLevelDebug];
     [ACPTarget registerExtension];
     [ACPTargetVEC registerExtension];
     [ACPCore start:^{
       [ACPCore lifecycleStart:nil];
     }];
     // Override point for customization after application launch.
     return YES;
   }
   
   // CONFIGURATION LINE FOR SWIFT ONLY: 
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
     //Other Extensions that you need
     ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID")
     ACPCore.setLogLevel(ACPMobileLogLevel.debug)
     ACPTarget.registerExtension()
     ACPTargetVEC.registerExtension()
     [ACPCore start:^{
       [ACPCore lifecycleStart:nil];
     }];
     return true
   }
   ```

1. `AppDelegate:application:openURL`의 시작 부분에 다음 줄을 추가합니다. 위임 함수가 정의되지 않은 경우에는 작성하여 다음 줄을 추가합니다.

   ```
   // URL HANDLER LINE FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<NSString *, id> *)options {
     [ACPCore collectLaunchInfo:@ {@"adb_deeplink": url.absoluteString}];
     return YES;
   }
   
   // URL HANDLER LINE FOR SWIFT ONLY: 
   func application(_ app: UIApplication, open url: URL, options: [UIApplicationOpenURLOptionsKey : Any] = [:]) -> Bool {
     ACPCore.collectLaunchInfo(["adb_deeplink": url.absoluteString])
     return true
   }
   ```

   애플리케이션을 빌드 및 실행하고 이를 사용하여 모바일 앱 VEC 기능을 테스트합니다.


## 모바일 앱에 대한 Target 보기 설정 {#views}

Adobe Mobile SDK는 새 보기가 렌더링될 때마다 개발자가 트리거할 수 있는 새 메서드를 표시합니다. iOS 앱에 대한 Target 보기 API 호출을 제대로 삽입하는 방법에 대한 일반 지침을 참조하십시오. iOS에서 모든 Target 보기는 표시되는 `UIViewController`를 기준으로 하여 정의됩니다. 따라서 Android와 달리 `TargetViews`의 삽입은 다음 호출로 제한됩니다.

Adobe 모바일 앱 VEC 확장 프로그램은 하위 클래스 `UIViewControllers`의 클래스 이름을 기반으로 하여 모바일 앱 VEC 프레임워크 내에서 `UIViewController`가 상호 작용하는 이름을 자동으로 생성합니다. 이러한 이름을 재정의하려면 `ViewController`의 `viewWillAppear`에서 다음 메서드를 호출할 수 있습니다.

```
// TARGET VIEW LINE FOR OBJECTIVE C ONLY 
[ACPTargetVEC setTargetView:@"exampleViewController"]; 
   
// TARGET VIEW LINE FOR SWIFT ONLY 
ACPTargetVEC.setTargetView("exampleViewController")
```

또한 Adobe Mobile SDK는 런타임 중에 개발자가 사용자 지정 보기를 타깃팅하는 다른 방법을 제공합니다. 개발자로서 보기에 이름이 고유하게 지정되었는지 확인해야 합니다. `superview`에 보기를 추가하기 전에 다음 메서드를 호출합니다.

```
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN OBJECTIVE C 
CustomPopupView *popupView = [[CustomPopupView alloc] initWithFrame:CGRectMake(0, 0, 300, 200)]; 
[ACPTargetVEC setTargetView:@"myCustomPopupView" forView:popupView];

// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN SWIFT 
let popupView = CustomPopupView.init(frame: CGRect(x: 0, y: 0, width: 300, height: 200)) 
ACPTargetVEC.setTargetView("myCustomPopupView", for: popupView)
```

## 프로필 매개 변수 및 기타 글로벌 매개 변수 설정 {#parameters}

이제 각각의 모든 API 호출에서 전달되는 전역 매개 변수 설정과 해당 보기에 대한 mbox/view 매개 변수 전달을 지원합니다.

매개 변수는 다음과 같습니다.

* mbox/view 매개 변수
* 프로필 매개 변수
* 제품 매개 변수
* 주문 매개 변수

**전역 매개 변수 지원:**

```
//For Objective-c 
NSDictionary *mboxParams = @{@"mboxparam1":@"mboxvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekey1":@"profilevalue1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters: mboxParams
                      profileParameters: profileParams
                      product: product
                      order: order];
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product = ACPTargetProduct(id: "1234", categoryId: "furniture")
var order = ACPTargetOrder(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"])
var targetParams = ACPTargetParameters(parameters: mboxParams, profileParameters: profileParams, product: product, order: order)
ACPTargetVEC.setGlobalRequest(targetParams)
```

**다음 보기 트리거에 대한 매개 변수 전달:**

앱에 있는 각 보기 컨트롤러에 대해 "`AUTO_<viewControllerName>`"과 같이 기본적으로 생성되는 일부 자동 보기가 제공되어 있습니다. 이러한 매개 변수를 전달하려는 경우 다음 API를 호출할 수 있습니다.

```
//For Objective-c 
NSDictionary *mboxParams = @{@"viewparam1":@"viewvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekeyforview1":@"profilevalueforview1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters:mboxParams 
                                                                      profileParameters:profileParams 
                                                                                product:product 
                                                                                  order:order]; 
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product = ACPTargetProduct(id: "1234", categoryId: "furniture")
var order = ACPTargetOrder(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"])
var targetParams = ACPTargetParameters(parameters: mboxParams, profileParameters: profileParams, product: product, order: order)
ACPTargetVEC.setRequest(targetParams)
```

**특정 보기에 매개 변수 전달:**

`TargetVEC.targetView("view_name")`를 통해 API 트리거 보기를 보았습니다. 특정 보기에 특정한 매개 변수를 다음과 같이 전달할 수도 있습니다.

```
//For Objective-c 
[ACPTargetVEC setTargetView:@"VIEW_NAME" withParameters:TARGET_PARAMS];

//FOR SWIFT 
ACPTargetVEC.setTargetView("VIEW_NAME", with: TARGET_PARAMS)
```

## API 미리 가져오기를 명시적으로 호출 {#section_373DB4527FC649C58FBA3DF0C18C9836}

캐시에 저장된 오퍼를 새로 고침하기 위해 API 미리 가져오기를 다시 호출하려는 경우 특정 시나리오가 있을 수 있습니다. 다음과 같이 설명되는 API가 노출됩니다.

**오퍼 미리 가져오기:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the main thread blocking the UI. 
 */ 
+ (void) prefetchOffers;
```

**배경에서 오퍼 미리 가져오기:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the background thread so doesn't block UI. 
 */ 
+ (void) prefetchOffersBackground;
```

## Tutorials: Implement the Experience Cloud in Mobile iOS Objective-C and Swift applications {#tutorial}

* [Mobile iOS Objective-C 응용 프로그램에서 Experience Cloud 구현](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-objective-c-apps-with-launch/index.html)
* [Mobile iOS Swift 애플리케이션에서 Experience Cloud 구현](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-swift-apps-with-launch/index.html)

이러한 자습서를 완료한 후 다음을 수행할 수 있습니다.

* 모바일 론치 속성 만들기
* Objective-C 또는 Swift 앱에 론치 속성 설치
* 다음과 같은 Adobe Experience Cloud 솔루션을 구현합니다.
   * Experience Cloud ID 서비스
   * Adobe Target
   * Adobe Analytics
   * Adobe Audience Manager

* 개발, 스테이징 및 프로덕션 환경을 통해 론치 변경 사항 게시