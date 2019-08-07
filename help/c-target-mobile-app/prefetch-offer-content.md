---
description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
keywords: 오퍼;미리 가져오기;iOS;Android; SDK; 모바일; Mobile SDK
seo-description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
seo-title: 오퍼 컨텐츠 미리 가져오기
solution: Target
title: 오퍼 컨텐츠 미리 가져오기
topic: 고급,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: 95bf4b2070cc2de235ac09ac164f0f9ec48dd6cd

---


# 오퍼 컨텐츠 미리 가져오기{#prefetch-offer-content}

[!DNL Target] 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.

이 프로세스는 로드 시간을 줄이고, 다중 네트워크 호출을 방지하며, 모바일 앱 사용자가 방문한 mbox를 [!DNL Target]에 알려줄 수 있도록 해줍니다. Prefetch 호출 동안 모든 컨텐츠가 검색되고 캐시되고, 지정된 mbox 이름에 캐시된 컨텐츠가 포함된 이후의 모든 호출에 대해 캐시에서 이 컨텐츠가 검색됩니다.

iOS 및 Android 모바일 SDK와 함께 Prefetch 메서드에서 사용하는 경우 다음 사항을 고려합니다.

* 미리 가져오기 컨텐츠는 실행 간에는 지속되지 않으며, 애플리케이션이 상주하는 동안 또는 `clearPrefetchCache()` 메서드가 호출될 때까지 캐시됩니다.
* iOs 및 Android Mobile SDK의 프리페치 기능은 자동 타겟, 자동 할당 및 자동화된 개인화 활동 유형에 대해 지원되지 않습니다.

미리 가져오기 방법, 공용 클래스 및 코드 샘플을 포함한 자세한 내용은 다음을 참조하십시오.

* **iOS:**[Experience Cloud Solutions용 iOS SDK 4.x](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) 안내서의 *iOS에서 오퍼 컨텐츠 미리 가져오기*.
* **Android:**[Experience Cloud Solutions용 Android SDK 4.x](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) 안내서의 *Android에서 오퍼 컨텐츠 미리 가져오기*.
