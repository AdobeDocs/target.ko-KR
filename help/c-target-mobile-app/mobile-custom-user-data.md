---
description: 위치 또는 사용자에 대한 추가 정보를 이름-값 쌍으로 Target에 보낼 수 있습니다.
keywords: 모바일 앱;모바일 앱 데이터 전송;target 모바일 앱;모바일 사용자 지정 사용자 데이터;모바일 앱 사용자 지정 데이터
seo-description: 위치 또는 사용자에 대한 추가 정보를 이름-값 쌍으로 Target에 보낼 수 있습니다.
seo-title: iOS - 사용자 지정 사용자 데이터 전송
title: iOS - 사용자 지정 사용자 데이터 전송
topic: Target
uuid: 00baa1e2-4d1c-4835-ac55-47c9ac8985ac
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# iOS - 사용자 지정 사용자 데이터 전송{#ios-send-custom-user-data}

위치 또는 사용자에 대한 추가 정보를 이름-값 쌍으로 Target에 보낼 수 있습니다.

이 정보는 사용자 지정 대상(예: 25,000마일 이상 떨어진 사용자) 작성 및 보고 작업에 사용할 수 있습니다.

Target 호출을 사용하여 전송할 수 있는 매개 변수 유형에는 다음 두 가지가 있습니다.

* mbox 매개 변수

   Mbox 매개 변수는 세션이 바뀌면 지속되지 않습니다.
* 프로필 매개 변수

   프로필 매개 변수는 방문자 프로필 저장소에 저장되며 세션이 바뀌어도 지속됩니다. Mbox 매개 변수는 지속되지 않습니다. 일부 키가 예약되어 있지만, 프로필 및 mbox 매개 변수 둘 다 사용자 지정 키-값 쌍으로 지정할 수 있습니다.

일부 예약된 키가 있지만 프로필 및 mbox 매개 변수 둘 다 사용자 지정 키-값 쌍을 포함할 수 있습니다.

1. 사전을 만듭니다.

   먼저 Target으로 전달하기 위해 전송하는 값을 사용하여 사전을 만듭니다. 편의를 위해 `welcomeMessageCampaign` 메서드 내에 사전을 추가하면 범위에 대해 걱정할 필요가 없습니다.

   다음은 샘플 사전입니다. 복사한 후 `(void)welcomeMessageCampaign` 내부에 붙여넣을 수 있습니다. `userLevel` 및 `userMiles`와 같은 키의 값은 이 예에서 하드 코딩됩니다. 일반적으로 사용자가 해당 변수를 제공합니다.

   ```
   NSDictionary *targetParams = [[NSDictionary alloc] initWithObjectsAndKeys: 
                                 @"platinum",@"userLevel", 
                                 @26500,@"userMiles", 
                                 @"1067007",@"entity.id", 
                                 @"dealsapp.qa", @"host", 
                                 @"fashion",@"entity.categoryId", 
                                 @"millenial", @"profile.persona", 
                                 @"cohort_5", @"profile.cohort", 
                                 nil];
   ```

   * 접두어 프로필(예: `profile.persona`)이 있는 키는 사용자 프로필에 저장됩니다.

      이러한 프로필 속성은 여러 활동 및 채널에서 사용할 수 있습니다.

   * 접두사가 없는 키(예: `userMiles`)는 mbox 매개 변수입니다.

      이러한 매개 변수는 세션 중에만 사용 가능합니다.

   * 접두부 엔티티가 있는 키(예: `entity.category.id`)는 제품 권장 사항에 사용됩니다.

1. 데이터를 확인합니다.
   1. 애플리케이션 `didFinishLaunchingWithOptions`에서 주석 처리를 해제하거나 `[ADBMobile setDebugLogging:YES];`를 추가합니다.

      이렇게 하면 자세한 디버그 로그가 인쇄됩니다.
   1. 앱을 빌드합니다.
   1. 매개 변수가 대상 호출에 전달되었는지 확인합니다.

      디버그 콘솔에서 목표 위치 이름을 검색합니다. 방금 전달한 모든 매개 변수를 사용한 `YOUR-CLIENT-CODE.tt.omtrdc.net`에 대한 호출이 표시됩니다.

      ![](assets/mobile-debug.png)
   Target Standard에서 이러한 매개 변수를 사용하여 대상을 작성하고 컨텐츠 표시를 제한하거나 타깃팅할 수 있습니다.
