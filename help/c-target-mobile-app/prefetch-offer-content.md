---
description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
keywords: 오퍼;미리 가져오기;iOS;Androidsdk;mobile;mobile sdk
seo-description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
seo-title: 오퍼 컨텐츠 미리 가져오기
solution: Target
title: 오퍼 컨텐츠 미리 가져오기
topic: 고급,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: ce8a890d0d662c0eec4d7fe254da371694811822

---


# 오퍼 컨텐츠 미리 가져오기{#prefetch-offer-content}

[!DNL Target] 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.

이 프로세스는 로드 시간을 줄이고, 다중 네트워크 호출을 방지하며, 모바일 앱 사용자가 방문한 mbox를 [!DNL Target]에 알려줄 수 있도록 해줍니다. 모든 컨텐츠는 프리페치 호출 동안 검색되고 캐시되며, 이 컨텐츠는 지정된 mbox 이름에 대해 캐시된 컨텐츠가 들어 있는 모든 향후 호출에 대해 캐시에서 검색됩니다.

iOS 및 Android Mobile SDK에서 프리페치 방법을 사용할 때는 다음 사항을 고려하십시오.

* 미리 가져오기 컨텐츠는 실행 간에는 지속되지 않으며, 애플리케이션이 상주하는 동안 또는 `clearPrefetchCache()` 메서드가 호출될 때까지 캐시됩니다.
* iOs 및 Android Mobile SDK의 프리페치 기능은 자동 타겟, 자동 할당 및 자동화된 개인화 활동 유형에서 지원되지 않습니다.

미리 가져오기 방법, 공용 클래스 및 코드 샘플을 포함한 자세한 내용은 다음을 참조하십시오.

* **** iOS: iOS에서 [오퍼](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) 컨텐츠를 프리페치(Prefetch) *할 수 있습니다*.
* **** Android: Android [의 오퍼](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/c-mob-target-prefetch-android.html) 내용은 Mobile Services Android SDK *도움말에서 미리 가져올 수 있습니다*.
