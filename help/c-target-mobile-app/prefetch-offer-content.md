---
keywords: 오퍼;프리페치;iOS;android;sdk;mobile;mobile sdk
description: Adobe Target 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.
title: 프리패치 오퍼 콘텐츠
feature: Implement Mobile
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 60%

---


# 오퍼 컨텐츠 미리 가져오기{#prefetch-offer-content}

[!DNL Target] 미리 가져오기 기능은 iOS 및 Android Mobile SDK를 사용하여 서버 응답을 캐시하여 가능한 한 적은 시간에 오퍼 컨텐츠를 가져옵니다.

이 프로세스는 로드 시간을 줄이고, 다중 네트워크 호출을 방지하며, 모바일 앱 사용자가 방문한 mbox를 [!DNL Target]에 알려줄 수 있도록 해줍니다. 모든 콘텐츠는 미리 가져오기 호출 중에 검색되고 캐시되며, 이 콘텐츠는 지정된 mbox 이름에 대해 캐시된 콘텐츠를 포함하는 이후의 모든 호출에 대한 캐시에서 검색됩니다.

iOS 및 Android Mobile SDK에서 프리페치 방법을 사용할 때는 다음 제한 사항을 고려하십시오.

* 미리 가져오기 콘텐츠는 실행 간에는 지속되지 않으며, 애플리케이션이 상주하는 동안 또는 `clearPrefetchCache()` 메서드가 호출될 때까지 캐시됩니다.
* 프리페치 기능은 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 트래픽 할당 메서드, [!UICONTROL Automated Personalization] 또는 [!UICONTROL Recommendations] 활동 유형 또는 A/B 또는 XT 활동](/help/c-recommendations/recommendations-as-an-offer.md)의 권장 사항에 대해 지원되지 않습니다.[

미리 가져오기 방법, 공용 클래스 및 코드 샘플을 포함한 자세한 내용은 다음을 참조하십시오.

* **iOS:**  [Mobile Services iOS SDK 도움말의 ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOS에서  *콘텐츠를 프리페치합니다*.
* **Android:**  [Mobile Services Android SDK 도움말의 ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android에서  *컨텐츠를 프리페치합니다*.
