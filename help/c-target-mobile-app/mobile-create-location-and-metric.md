---
keywords: mobile app;mobile app location;target mobile app;mobile target locations;mobile app success metrics
description: 모바일 앱에서 Target을 사용하려면 위치 및 성공 지표를 만드십시오.
title: iOS - Target 위치 및 성공 지표 만들기
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 92%

---


# iOS - Target 위치 및 성공 지표 만들기{#ios-create-a-target-location-and-success-metric}

모바일 앱에서 Target을 사용하려면 위치 및 성공 지표를 만드십시오.

이 섹션에는 앱용 템플릿으로 사용할 수 있는 샘플 코드가 포함되어 있습니다. 이 섹션의 샘플에는 iOS용 코드가 포함되어 있습니다. 동일한 패턴이 Android에 적용됩니다. Android 관련 구문은 [](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/target-main.html)Experience Cloud용 Android SDK 4.x 솔루션 가이드에서 찾을 수 있습니다.

>[!NOTE]
>
>See the [Mobile documentation](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-target-methods.html) for a list of all the available Target methods.

앱에서 Target 위치를 만들고 요청을 수행하려면 다음 두 가지 기본 메서드를 사용할 수 있습니다.

* `targetCreateRequestWithName`
* `targetLoadRequest`

1. Target 위치를 만듭니다.

   다음은 요청을 만들기 위한 샘플 호출입니다.

   ```
   // make your request 
   ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
                                                    defaultContent:@"default.png" 
                                                    parameters:nil];
   ```

   | 매개 변수 | 설명 |
   |---|---|
   | `ADBTargetLocationRequest *myRequest` | `myRequest`를 앱의 `targetLocation` 이름으로 바꿉니다. |
   | `targetCreateRequestWithName:@"heroBanner"` | `heroBanner`를 Target의 `targetLocation` 이름으로 바꿉니다. 이것은 mbox 이름과 동일합니다. 이 히어로 배너는 Target 인터페이스에 나타납니다. |
   | `defaultContent:@"default.png"` | `default.png`을 Target이 응답하지 않는 경우 앱이 사용하는 값으로 바꿉니다. |
   | `parameters:nil` | 프로필 또는 mbox 매개 변수를 지정합니다. &#39;사용자 지정 데이터 전달&#39; 섹션에서 자세한 내용을 참조하십시오. |

   다음은 요청을 로드하기 위한 샘플 호출입니다.

   ```
   // load your request 
   [ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
                                        // do something with content 
                                        heroImage.image = [UIImage imageNamed:content]; 
   }];
   ```

   | 매개 변수 | 설명 |
   |---|---|
   | `targetLoadRequest:myRequest` | `myRequest`를 앱의 `targetLocation` 이름으로 바꿉니다. |
   | `NSString *content` | content를 Adobe에서 가져온 실제 컨텐츠로 바꿉니다. 이 문자열은 XML, JSON 또는 일반 문자열일 수 있습니다. 이 코드 섹션을 사용하여 변수를 정의하거나, 이미지 경로를 설정하거나, 컨트롤러 흐름 또는 트랜잭션 지점을 보거나 원하는 다른 작업을 수행할 수 있습니다. Target은 UI에 입력된 컨텐츠를 정확히 동일한 형식으로 반환합니다. |
   | `heroImage.image = [UIImage imageNamed:content];` | 예: 컨텐츠를 가져오고 히어로 이미지에 대한 경로를 설정합니다. |

1. 성공 지표를 만듭니다.

   `targetCreateOrderConfirmRequestWithName` 메서드를 사용하여 앱에서 전환/성공 지표를 추적할 수 있습니다.

   ```
   ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
                                              orderId: orderId 
                                              orderTotal: @"39.95" 
                                              productPurchasedId: _galleryItem.title 
                                              parameters: nil]; 
   [ADBMobile targetLoadRequest: req callback: nil];
   ```

   | 매개 변수 | 설명 |
   |---|---|
   | `orderId` | 고유한 주문 ID를 나타내는 다이내믹 변수로 바꿉니다. |
   | `@"39.95"` | 고유한 주문 총액을 나타내는 다이내믹 변수로 바꿉니다. |
   | `_galleryItem.title` | 구입한 제품의 쉼표로 구분된 목록을 나타내는 다이내믹 변수로 바꿉니다. |
   | `parameters: nil` | 추가 매개 변수의 선택적 사전입니다. |

1. 앱을 빌드합니다.

   단계 결과: Target 위치를 만들고 성공 지표에 태그를 지정한 후에는 A/B 테스트를 만듭니다. 양식 기반 경험 작성기를 사용하여 활동을 만들 수 있습니다.
