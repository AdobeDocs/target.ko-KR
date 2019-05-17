---
description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
keywords: 오퍼;미리 가져오기;iOS;Android
seo-description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
seo-title: 오퍼 컨텐츠 미리 가져오기
solution: Target
title: 오퍼 컨텐츠 미리 가져오기
topic: 고급,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 오퍼 컨텐츠 미리 가져오기{#prefetch-offer-content}

[!DNL Adobe Target] 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.

이 프로세스는 로드 시간을 줄이고, 다중 네트워크 호출을 방지하며, 모바일 앱 사용자가 방문한 mbox를 [!DNL Target]에 알려줄 수 있도록 해줍니다. 모든 컨텐츠는 미리 가져오기 호출 중에 검색되고 캐시되며, 이 컨텐츠는 지정된 mbox 이름에 대해 캐시된 컨텐츠를 포함하는 이후의 모든 호출에 대한 캐시에서 검색됩니다.

미리 가져오기 컨텐츠는 실행 간에는 지속되지 않으며, 애플리케이션이 상주하는 동안 또는 `clearPrefetchCache()` 메서드가 호출될 때까지 캐시됩니다.

미리 가져오기 방법, 공용 클래스 및 코드 샘플을 포함한 자세한 내용은 다음을 참조하십시오.

* **iOS:**[* Ios SDK 4. x 용 * iOS SDK 4. x 안내서의 오퍼](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) 콘텐츠 프리페치를 참조하십시오.
* **Android:**[Experience Cloud Solutions용 Android SDK 4.x](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) 안내서의 *Android에서 오퍼 컨텐츠 미리 가져오기*.