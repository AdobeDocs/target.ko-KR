---
description: 모바일 앱용 Adobe Target에 대한 FAQ입니다.
keywords: 모바일 앱;FAQ;대상 모바일 앱
seo-description: 모바일 앱용 Adobe Target에 대한 FAQ입니다.
seo-title: 모바일 앱용 Adobe Target에 대한 FAQ
title: 모바일 앱용 Adobe Target FAQ
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# 모바일 앱용 Target FAQ

모바일 앱에 [!DNL Target] 대한 FAQ 목록입니다.

## SDK를 배포하는 [!DNL Adobe Experience Platform Launch] 데 사용해야 합니까? 아니면 사용하지 않고 SDK를 배포할 수 [!DNL Launch]있습니까?

SDK는 Adobe Marketing Cloud [Git에서 사용할 수 있습니다](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Launch를 사용하지 [않는](https://docs.adobe.com/content/help/en/launch/using/overview.html)경우 자체 설정 파일을 관리하고 앱에서 관리해야 합니다.

## Adobe Experience Platform SDK v5에 대한 React-Native 지원과 함께 모바일 앱용 VEC(Visual Experience Composer)를 사용할 수 있습니까?

기본 [모바일 앱용 VEC는](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) 현재 React 기본 앱을 지원하지 않습니다. 양식 기반 [경험 작성기를 사용해야 합니다](/help/c-experiences/form-experience-composer.md).

## Mobile SDK 통합을 통해 새로운 모바일 기능을 롤아웃할 수 있습니까? 새로운 코드 배포 없이 기능 플래그를 켜거나 끌 수 있습니까?

예. Adobe 모바일 SDK를 사용하여 점진적으로 기능을 롤아웃할 수 있습니다.

## 보다 복잡한 로직의 경우 Mobile VEC를 사용하는 대신 앱에서 바로 개발해야 합니까? 그렇다면 어떤 개발 언어를 사용해야 합니까?

현재 VEC는 이미지, 텍스트, 색상 등의 일반적인 사용 사례를 지원합니다. 앱 레이아웃을 개인화하는 등의 고급 사용 사례를 보려면 코드에 [!DNL Target] 요청/위치(mbox)를 삽입하고 양식 기반 [경험](/help/c-experiences/form-experience-composer.md) 작성기를 사용하여 경험을 디자인하고 트래픽을 할당해야 합니다. Adobe 모바일 SDK는 Java, Objective C 및 Swift를 지원합니다. 팀의 선호도 및 리소스에 따라 언어를 선택할 수 있습니다.

## 현재 어떤 SDK가 제공됩니까?

Adobe Experience Platform Mobile SDK는 현재 iOS, Android 및 반응을 지원합니다. 자세한 내용은 Adobe Experience Cloud [Platform Mobile SDK 가이드를](https://aep-sdks.gitbook.io/docs/)참조하십시오.

## 위도 및 경도에 대한 확인 측면에서 위치 기반 기능의 빈도는 어떻게 됩니까?

자세한 내용은 [Adobe Places 설명서를](https://placesdocs.com/places-services-by-adobe-documentation/) 참조하십시오.

## 모바일 "보기"는 어떤 기본 클래스를 지원합니까? NSObject 파생 클래스(또는 Android 개체)나 NSViewController 및 활동을 지원합니까?

자세한 내용은 Android 설명서를 참조하십시오. [수동으로 뷰를](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views)선언하려면

## Adobe Experience Platform Mobile SDK가 작동하려면 at.js가 필요합니까?

아니요. 모바일 SDK를 사용하기 위해 at.js가 필요하지 않습니다. at.js는 [!DNL Target] 웹 사이트를 위한 JavaScript 라이브러리입니다. Adobe Experience Platform Mobile SDK는 모바일 앱용입니다.

## Target Mobile은 Adobe Target Premium 제품 SKU의 기능만 제공합니까?

Adobe Target Standard 고객의 경우 Adobe Mobile SDK를 A/B 테스트 및 경험 타깃팅(XT) 활동에만 사용할 수 있습니다. 모바일 앱에서 Recommendations 또는 AI 기반 기능을 사용하려면 Adobe Target Premium [라이선스가](/help/c-intro/intro.md#premium) 필요합니다.

## 모바일 앱용 VEC에서 AAM(Adobe Audience Manager)의 고객을 활용할 수 있습니까?

예. Adobe Experience Platform Mobile SDK는 Audience Manager, [Analytics](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html), [Campaign](https://docs.adobe.com/content/help/en/analytics/landing/home.html)및 [Target용으로](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html)구축되었습니다. Audience Manager의 대상은 공유됩니다 [!DNL Target].

## Adobe Experience Manager(AEM)와 Target 모바일 활동 간에 모바일 앱 통합이 있습니까?

로드맵에 있지만 아직 시간표가 없습니다. 현재 AEM에서 [Target](/help/c-experiences/c-manage-content/aem-experience-fragments.md) 으로 JSON 경험 조각을 공유할 수 있으며 모바일 앱 활동에서 이를 사용할 가능성이 있습니다.

## VEC를 사용하여 이미지를 더 추가하거나 기존 이미지만 변경할 수 있습니까?

현재 기존 이미지만 변경할 수 있습니다.
