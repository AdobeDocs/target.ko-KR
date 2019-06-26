---
description: Target의 새 SDK 라이브러리를 사용하여 개발자가 Android 모바일 앱에서 일회 설정을 수행하고 마케터가 모바일 VEC(시각적 경험 작성기)의 기능을 사용할 수 있습니다.
keywords: 모바일 vec;모바일 시각적 경험 작성기;모바일 경험 작성기 선택 사항;설정;android
seo-description: Target의 새 SDK 라이브러리를 사용하여 개발자가 Android 모바일 앱에서 일회 설정을 수행하고 마케터가 모바일 VEC(시각적 경험 작성기)의 기능을 사용할 수 있습니다.
seo-title: Android - 모바일 앱 설정
solution: Target
title: Android - 모바일 앱 설정
topic: Standard
uuid: 39938ec2-b12e-44cf-9218-69195fba0ff7
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Android - 모바일 앱 설정{#android-set-up-the-mobile-app}

Adobe Target 모바일 앱 VEC(시각적 경험 작성기)를 사용하여 개발자는 Android 모바일 앱에서 일회성 설정을 수행하고 마케터는 모바일 앱 VEC의 기능을 사용할 수 있습니다.

Adobe Target VEC 확장 프로그램 활성화에 대한 자세한 내용은 [Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec)에서 *Adobe Target - 시각적 경험 작성기*를 참조하십시오.

## Mobile SDK 및 Target 라이브러리 포함 {#sdk-library}

1. SDK V5 초기화에 대한 자세한 내용은 [SDK 초기화 및 추적 설정](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk)을 참조하십시오.
1. 종속성 섹션에 다음 행을 추가하십시오.

   ```
   implementation 'com.adobe.marketing.mobile:target-vec:1.+'
   ```

1. 모바일 앱 VEC는 `build.gradle`에 종속으로 포함될 다음 가공물이 필요합니다.

   ```
    implementation 'com.google.code.gson:gson:2.8.2'
    implementation 'android.arch.lifecycle:extensions:1.1.1'
    implementation('io.github.sac:SocketclusterClientJava:1.7.5')
    implementation 'com.android.support:support-annotations:28.0.0'
    implementation 'com.android.support:support-compat:28.0.0'
    implementation 'com.android.support:design:28.0.0'
   ```

1. `AndroidManifest.XML` 파일에 의도 필터를 추가하여 모바일 앱 VEC 작성에 고유한 딥링크 체계를 선택합니다(예: `[sdkbetabus://com.adobe.sdkbetabus](sdkbetabus://com.adobe.sdkbetabus)`).

   ```
   <activity 
       android:name=".listing.MoviesListingActivity" 
       android:launchMode="singleTask"> 
       <intent-filter> 
           <action android:name="android.intent.action.VIEW" /> 
   
           <category android:name="android.intent.category.DEFAULT" /> 
           <category android:name="android.intent.category.BROWSABLE" /> 
   
           <data 
               android:host="com.adobe.sdkbetabus" 
               android:scheme="sdkbetabus" /> 
       </intent-filter> 
   </activity>
   ```

1. 모바일 프로젝트로 이동하여 `Application::onCreate override`의 끝에 다음 행을 삽입합니다.

   ```
   public class SDKTest extends MultiDexApplication { 
   
       @Override 
       public void onCreate() { 
           /* Put Your App's implementation */ 
           MobileCore.setApplication(this); 
           MobileCore.setLogLevel(LoggingMode.DEBUG); 
           MobileCore.configureWithAppID("YOUR_ADOBE_LAUNCH_APP_ID"); 
   
           ... 
           try { 
               TargetVEC.registerExtension(); //Single line code to initialize TargetVEC
               Target.registerExtension();
               Identity.registerExtension();
               Lifecycle.registerExtension();
               Signal.registerExtension();
               MobileCore.start(new AdobeCallback () {
                  @Override
                  public void call(Object o) {
                     MobileCore.configureWithAppID("launch-EN4e833d644d1949e39e985ddad4f52bd4-development");
                  }
               });
           } catch (InvalidInitException e) { 
             .. 
           }
       }
   
   /* Rest of Application test goes here ... */
   ```

1. 빌드가 작동하지 않을 경우 기본 설정을 빌드해야 하는 아래에 제공된 예제 프로젝트를 검토하고 다음 위치에서 변경 사항을 검토하십시오.

   1. `Application::OnCreate override`
   1. `AndroidManifest.XML`
   1. Android 애플리케이션의 `build.gradle`

## 모바일 앱에서 Target 보기 설정 {#views}

Adobe Mobile SDK는 새 보기가 렌더링될 때마다 개발자가 트리거할 수 있는 새 메서드를 표시합니다. 개발자로서, 뷰 이름이 고유하게 지정되어 있고 `targetView` 호출이 UI 기본 스레드에 있는지 확인해야 합니다. 이 섹션에서는 먼저 두 개의 서로 다른 데모 애플리케이션을 사용하여 이러한 호출을 삽입하는 방법을 보여 주고, Android 앱에 대한 Target 보기 API 호출을 올바르게 삽입하는 방법에 대한 일반 지침을 설명합니다.

>[!NOTE]
>
>`targetView function`이 트리거되지 않으면 VEC 확장 프로그램이 Android 활동에서 보기를 식별하려고 시도합니다. 동적 보기가 없는 애플리케이션의 경우 옵션 단계일 수 있습니다.

함수 호출을 사용하여 Target 보기를 트리거할 수 있습니다. 보기에 모든 타깃팅 매개 변수를 선택적으로 제공할 수 있습니다.

```
public class TargetVEC { 
   
   /** 
    * Marks a view hierarchy for editing in Mobile App VEC.  Call must insert when the view hierarchy 
    * is memory and committed to being shown, but not yet shown on the screen. 
    * 
    * @param viewName the unique Target View Name 
    */ 
   public static void targetView(String viewName); 
  
  /** 
   * Trigger Target view 
   * Triggering a Target view may cause Target offers to be applied on the current container component. 
   * Note that Target offers are applied from local Target cache, so flicker should be negligible. 
   * 
   * @param viewName Mandatory Target View name, which must be unique at app level 
   * @param parameters Parameters to be included in the next Target call 
   */ 
  
    public static void targetView(String viewName, TargetParameters parameters); 
}
```

첫 번째 예제 프로젝트는 간단한 버스 스케줄 애플리케이션의 모형입니다. 모바일 앱 VEC에서 사용하도록 이 애플리케이션을 설정하려면 다음을 수행하십시오.

1. Android Studio에서 패키지 하위 디렉터리 `build.gradle`에서 `BusBooking` 파일이 있는 프로젝트를 엽니다.
1. `DemoApplication::OnCreate` 메서드에서 `TargetVEC.registerExtension()`을 추가하여 다른 확장 프로그램과 함께 Target VEC 확장 프로그램을 등록합니다.
1. 응용 프로그램을 빌드하고 실행합니다.
1. 모바일 앱 VEC 작성 모드로 전환하려면 [!DNL sdkbetabus://com.adobe.sdkbetabus]를 해당 URL 체계로 사용하고 장치에서 생성된 딥링크를 엽니다(아래 지시 사항 참조).

이러한 간단한 버스 예약 응용 프로그램에서는 활동 라이프사이클과 연관된 자동으로 생성된 Target 보기를 모두 사용합니다. 또한 숨겨진 단추를 클릭하면(화면의 오퍼 이미지) 동적으로 추가되는 사용자 지정 보기 요소에서 Target 보기 API를 호출하여 API의 유연성을 보여 줍니다. 이 새 Target 보기는 코드에서 `OfferDetailsActivity.java:40`에 API 호출을 삽입하여 구현됩니다. 숨겨진 단추를 클릭하면 &quot;SURPRISE_VIEW&quot;라는 새 Target 보기 이벤트가 실행되므로 마케터가 애플리케이션 환경에서 더욱 정밀하게 대상을 변경할 수 있습니다.

타깃팅된 동적 보기 삽입:

```
package com.adobe.target.examples.bus; 
   
import android.app.DialogFragment; 
import android.os.Bundle; 
import android.os.Handler; 
import android.support.v7.app.AppCompatActivity; 
import android.support.v7.widget.Toolbar; 
import android.view.View; 
import android.view.ViewGroup; 
import android.widget.LinearLayout; 
import android.widget.Toast; 
   
import com.adobe.target.mobile.TargetVEC; 
   
/** 
 * This activity class is responsible to show offer details 
 */ 
public class OfferDetailsActivity extends AppCompatActivity { 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        setContentView(R.layout.activity_offer_details); 
        setUpToolBar(); 
        final Handler mainHandler = new Handler(getApplicationContext().getMainLooper()); 
   
        final View surpriseView = getLayoutInflater().inflate(R.layout.suprise_layout, 
                (ViewGroup) findViewById(android.R.id.content), false); 
   
        final View imagePresentView = this.findViewById(R.id.image_present); 
        final LinearLayout currentLayout = this.findViewById(R.id.offer_layout); 
   
        imagePresentView.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                Toast.makeText(getApplicationContext(),"Surprise!", Toast.LENGTH_SHORT).show(); 
                mainHandler.post(new Runnable() { 
                    @Override 
                    public void run() { 
                        currentLayout.addView(surpriseView); 
                        TargetVEC.targetView("SURPRISE_VIEW"); 
                        currentLayout.invalidate(); 
                    } 
                }); 
                // One-shot.  Remove clicker afterwards. 
                imagePresentView.setOnClickListener(null); 
            } 
        }); 
    } 
   
    private void setUpToolBar() { 
        Toolbar toolbar = findViewById(R.id.toolbar); 
        toolbar.setNavigationIcon(R.drawable.abc_ic_ab_back_material); 
        toolbar.setTitle("Buy 1 Get 1"); 
        toolbar.setNavigationOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                onBackPressed(); 
            } 
        }); 
    } 
   
    @Override 
    protected void onPause() { 
        super.onPause();
        MobileCore.lifecyclePause();
    } 
   
    @Override 
    protected void onResume() { 
        super.onResume();
        MobileCore.lifecycleStart(null);
    } 
}
```

## 프로필 매개 변수 및 기타 글로벌 매개 변수 설정 {#parameters}

이제 각 API 호출에서 전달되는 전역 매개 변수를 설정하고 해당 보기에 mbox/view 매개 변수를 전달할 수 있습니다.

매개 변수는 다음과 같습니다.

* mbox/view 매개 변수
* 프로필 매개 변수
* 제품 매개 변수
* 주문 매개 변수

**전역 매개 변수 지원:**

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("mboxparam1", "mboxvalue1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekey1", "profilevalue1"); 
  
TargetVEC.setGlobalRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**다음 보기 트리거에 대한 매개 변수 전달:**

앱에 있는 각 활동 및 조각에 대해 &quot;`AUTO_<activity|fragment name>`&quot;과 같이 기본적으로 생성되는 일부 자동 보기가 제공되어 있습니다. 이러한 매개 변수를 전달하려는 경우 다음 API를 호출할 수 있습니다.

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("viewKey1", "viewparam1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekeyforview1", "profilevalueforview1"); 
  
TargetVEC.setRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**특정 보기에 매개 변수 전달:**

`TargetVEC.targetView("view_name")`를 통해 API 트리거 보기를 보았습니다. 특정 보기에 특정한 매개 변수를 다음과 같이 전달할 수도 있습니다.

```
Map<String, String> profileParams = new HashMap<>(); 
profileParams.put("surprisekey1", "surprisevalue1");  //ProfileParams 
TargetVEC.targetView("SURPRISE_VIEW", 
        new TargetParameters.Builder() 
                .profileParameters(profileParams) 
                .product(new TargetProduct("3354", "kitchen")) 
                .build());
```

## API 미리 가져오기를 명시적으로 호출 {#section_2D02B74558474D3BA9F25E4D25E7C7E3}

캐시에 저장된 오퍼를 새로 고침하기 위해 API 미리 가져오기를 다시 호출하려는 경우 특정 시나리오가 있을 수 있습니다. 다음과 같이 설명되는 API가 노출됩니다.

* **prefetchOffers**

   ```
   /** 
    * Prefetch Target offers. 
    * Note that calling this will pre-hide the current layout, until Target offers are prefetched 
    * and applied to currently visible Target views, possibly causing flicker, thus it's recommended 
    * to call this method inside the containing component's onCreate() lifecycle method 
    */ 
   public static void prefetchOffers();
   ```

* **prefetchOffersBackground**

   ```
   /** 
    * Prefetch Target offers in the background. 
    * Note, that in contrast to prefetchOffers(), calling this method will NOT pre-hide 
    * the current layout, instead prefetched Target offers will be only be cached and will subsequently 
    * be applied as Target Views are being triggered. 
    */ 
   public static void prefetchOffersBackground();
   ```

## Tutorial: Implement the Experience Cloud in Mobile Android Applications {#tutorial}

* [모바일 Android 애플리케이션에서 Experience Cloud 구현](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-android-apps-with-launch/index.html)

이 자습서를 완료한 후 다음을 수행할 수 있습니다.

* 모바일 론치 속성 만들기
* Android 앱에 론치 속성 설치
* 다음과 같은 Adobe Experience Cloud 솔루션을 구현합니다.
   * Experience Cloud ID 서비스
   * Adobe Target
   * Adobe Analytics
   * Adobe Audience Manager

* 개발, 스테이징 및 프로덕션 환경을 통해 론치 변경 사항 게시
