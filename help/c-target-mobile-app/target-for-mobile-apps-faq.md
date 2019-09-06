---
description: 모바일 앱용 Adobe Target에 대한 FAQ
keywords: 모바일 앱; FAQFAQ; Target 모바일 앱
seo-description: 모바일 앱용 Adobe Target에 대한 FAQ
seo-title: 모바일 앱용 Adobe Target에 대한 FAQ
title: 모바일 앱용 Adobe Target FAQ
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# 모바일 앱용 타겟 FAQ

모바일 앱에 [!DNL Target] 대한 FAQ 목록입니다.

## SDK를 배포하는 [!DNL Adobe Experience Platform Launch] 데 사용해야 합니까? 아니면 SDK를 사용하지 [!DNL Launch]않고 배포할 수 있습니까?

SDK는 [Adobe Marketing Cloud Git에서 사용할](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)수 있습니다. [론치를](https://docs.adobe.com/content/help/en/launch/using/overview.html)사용하지 않는 경우 자신의 설정 파일을 관리하고 앱에서 관리해야 합니다.

## 모바일 앱용 Visual Experience Composer (VEC) 를 Adobe Experience Platform SDK v 5에 대한 반응형 지원과 함께 사용할 수 있습니까?

기본 모바일 앱용 [vec는](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) 현재 기본 앱 반응을 지원하지 않습니다. [양식 기반 Experience Composer](/help/c-experiences/form-experience-composer.md)를 사용해야 합니다.

## 모바일 SDK 통합을 통해 새로운 모바일 기능이 롤아웃될 수 있습니까? 새로운 코드 배포 없이 기능 플래그를 켜거나 끌 수 있습니까?

예. 모바일 SDK를 사용하여 점진적으로 기능을 롤아웃할 수 있습니다.

## 보다 복잡한 로직을 위해 Mobile VEC를 사용하는 대신 앱에서 직접 개발해야 합니까? 그렇다면 어떤 개발 언어를 사용해야 합니까?

현재 VEC는 이미지, 텍스트, 색상 등 일반적인 사용 사례를 지원합니다. 앱 레이아웃을 개인화하는 것과 같은 고급 사용 사례가 필요하면 코드에 [!DNL Target] 요청/위치 (mbox) 를 삽입하고 [양식 기반 Experience Composer](/help/c-experiences/form-experience-composer.md) 를 사용하여 경험을 디자인하고 트래픽을 할당해야 합니다. Adobe Mobile SDK는 Java, Objective C 및 Swift를 지원합니다. 팀의 선호도 및 리소스를 선택하여 언어를 선택합니다.

## 현재 제공되는 SDK는 무엇입니까?

현재 Adobe Experience Platform Mobile SDK는 iOS, Android 및 반응을 지원합니다. 자세한 내용은 [Adobe Experience Cloud Platform Mobile SDK 안내서를](https://aep-sdks.gitbook.io/docs/)참조하십시오.

## 위도 및 경도에 대한 확인 측면에서 위치 기반 기능의 빈도란 무엇입니까?

자세한 내용은 [Adobe 장소 설명서를](https://placesdocs.com/places-services-by-adobe-documentation/) 참조하십시오.

## 모바일 "보기" 가 지원하는 기본 클래스는 무엇입니까? They they support any nsobject derived class (or any Android object) or just nsviewcontroller and activities?

자세한 내용은 뷰를 선언하는 [수동 방법에 대한 Android 설명서를 참조하십시오](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views).

## Adobe Experience Platform Mobile SDK에 대한. js가 필요합니까?

아니요. 모바일 SDK를 사용하기 위해 at. js가 필요 없습니다. at. js는 웹 사이트를 위한 [!DNL Target] JavaScript 라이브러리입니다. Adobe Experience Platform Mobile SDK는 모바일 앱용입니다.

## Target Mobile는 Adobe Target Premium 제품 SKU 에만 해당됩니까?

Adobe Target Standard 고객의 경우, A/B 테스트 및 경험 타깃팅 (XT) 활동에만 Adobe Mobile SDK를 사용할 수 있습니다. 모바일 앱에서 Recommendations 또는 AI 기반의 기능을 사용하려면 [Adobe Target Premium](/help/c-intro/intro.md#premium) 라이선스가 있어야 합니다.

## 모바일 앱용 VEC에서 AAM (Adobe Audience Manager) 의 대상을 이용할 수 있습니까?

예. Adobe Experience Platform Mobile SDK는 [Audience Manager](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html), [Analytics](https://docs.adobe.com/content/help/en/analytics/landing/home.html), [Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html)및 Target 용으로 구축되었습니다. Audience Manager의 대상은 [!DNL Target]공유됩니다.

## AEM (Adobe Experience Manager) 간의 모바일 앱 통합이 있고 모바일 모바일 활동이 있습니까?

Adobe 로드맵에 있지만 아직은 타임라인이 없습니다. 현재 JSON [경험 조각은 AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md) 에서 Target로 공유할 수 있으며, 이를 모바일 앱 활동에서 사용할 가능성이 있을 수 있습니다.

## VEC를 사용하여 이미지를 더 추가하거나 기존 이미지만 변경할 수 있습니까?

현재 기존 이미지만 변경할 수 있습니다.
