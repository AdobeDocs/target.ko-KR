---
keywords: 반응형;모바일 뷰포트;뷰포트;장치;모바일;반응형 웹 디자인;rewd
description: 모바일 뷰포트를 사용하면 Adobe [!DNL Target] 활동이 다양한 크기의 화면에서 어떻게 표시되는지 확인할 수 있습니다. 널리 사용되는 디바이스 뷰포트 크기 및 해상도 목록을 확인합니다.
title: 반응형 경험에 모바일 뷰포트를 사용하려면 어떻게 해야 합니까?
feature: 시각적 경험 작성기(VEC)
exl-id: 1062e7a1-10b4-4746-bce9-67017978578d
translation-type: tm+mt
source-git-commit: cb42be6b0791711d3a9ddf5680cf6d6e32045579
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 34%

---

# 반응형 경험을 위한 모바일 뷰 포트

모바일 뷰포트를 사용하면 다양한 크기의 화면에서 [!DNL Adobe Target] 활동을 미리 볼 수 있습니다.

모바일 뷰어 미리 보기 기능은 다양한 장치, 창 및 화면 크기에서 제대로 렌더링되는 응답형 사이트를 위해 설계되었습니다. 반응형 사이트는 데스크톱, 랩톱, 태블릿 또는 휴대폰 등 모든 화면 크기에 맞게 자동으로 조정되고 조정됩니다.

>[!NOTE]
>
> * 사이트가 응답하고 데스크톱 페이지에 있는 것과 동일한 요소가 다른 구성으로 모바일 페이지에서 사용되는 경우 모바일 뷰포트를 사용하십시오. `m.mysite.com`과 같은 별도의 구조가 있는 별도의 모바일 사이트가 있는 경우 대신 [여러 페이지 활동](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48)을 사용하십시오.
   >
   >
* 리디렉션 오퍼 오버레이와 겹칠 경우에는 모바일 뷰포트를 사용할 수 없습니다.


뷰포트는 화면의 웹 페이지에 의해 채워진 사각형의 크기로 정의됩니다. 뷰포트는 브라우저 창의 크기에서 스크롤 막대 및 도구 모음을 뺀 것입니다. 브라우저는 &quot;CSS 픽셀&quot;을 사용합니다. Retina 화면을 사용하는 장치와 같이 많은 장치의 경우, 뷰포트는 광고된 장치 해상도보다 작습니다.

다음은 인기 있는 장치에 대한 뷰포트 및 해상도입니다. [!DNL Target]에서 뷰포트 크기를 사용해야 합니다.

>[!NOTE]
>
>다양한 웹 사이트가 많이 사용되는 장치에 대한 뷰포트 크기 목록을 제공합니다. 예를 들어 [https://viewportsizer.com/devices/](https://viewportsizer.com/devices/)을(를) 참조하십시오. 가장 정확하고 최신 정보는 디바이스 제조업체의 웹 사이트를 참조하십시오.

| 장치 | 뷰포트 크기 (너비 x 높이) | 장치 해상도(너비 x 높이) |
|---|---|---|
| iPhone12 | 390 x 844 | 1170 x 2532 |
| iPhone 12 Mini | 360 x 780 | 1080 x 2340 |
| iPhone 12 Pro | 390 x 844 | 1170 x 2532 |
| iPhone 12 Pro Max | 428 x 926 | 1248 x 2778 |
| iPhone SE | 214 x 379 | 640 x 1136 |
| iPhone 11 Pro Max | 414 x 896 | 1242 x 2688 |
| iPhone 11 Xs Max | 414 x 896 | 1242 x 2688 |
| iPhone11 | 414 x 896 | 828 x 1792 |
| iPhone 11 Xr | 414 x 896 | 828 x 1792 |
| iPhone 12 Pro | 375 x 812 | 1125 x 2436 |
| iPhone 11 X | 375 x 812 | 1125 x 2436 |
| iPhone 11 Xs | 375 x 812 | 1125 x 2436 |
| iPhone X | 375 x 812 | 1125 x 2436 |
| iPhone 8 Plus | 414 x 736 | 1080 x 1920 |
| iPhone8 | 375 x 667 | 750 x 1334 |
| iPhone 7 Plus | 414 x 736 | 1080 x 1920 |
| iPhone7 | 375 x 667 | 750 x 1334 |
| iPhone 6s Plus | 414 x 736 | 1080 x 1920 |
| iPhone6s | 375 x 667 | 750 x 1334 |
| iPhone 6 Plus | 414 x 736 | 1080 x 1920 |
| iPhone6 | 375 x 667 | 750 x 1334 |
| iPad Pro | 1024 x 1366 | 2048 x 2732 |
| iPad Third &amp; Fourth Generation | 768 x 1024 | 1536 x 2048 |
| iPad Air 1 및 2 | 768 x 1024 | 1536 x 2048 |
| iPad Mini | 768 x 1024 | 768 x 1024 |
| iPad Mini 2 및 3 | 768 x 1024 | 1536 x 2048 |
| Nexus 6P | 411 x 731 | 1440 x 2560 |
| Nexus 5X | 411 x 731 | 1080 x 1920 |
| Google Pixel | 411 x 731 | 1080 x 1920 |
| Google Pixel XL | 411 x 731 | 1440 x 2560 |
| Google Pixel 2 | 411 x 731 | 1080 x 1920 |
| Google Pixel 2 XL | 411 x 823 | 1440 x 2880 |
| Samsung Galaxy Note 5 | 480 x 853 | 1440 x 2560 |
| LG G5 | 360w x 640 | 1440 x 2560 |
| LG G4 | 360w x 640 | 1440 x 2560 |
| LG G3 | 360w x 640 | 1440 x 2560 |
| One Plus 3 | 480 x 853 | 1080 x 1920 |
| Samsung Galaxy S9 | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S9+ | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S8 | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S8+ | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S7 | 360 x 640 | 1440 x 2560 |
| Samsung Galaxy S7 Edge | 360 x 640 | 1440 x 2560 |
| Nexus 7 (2013) | 600 x 960 | 1200 x 1920 |
| Nexus 9 | 768 x 1024 | 1536 x 2048 |
| Samsung Galaxy Tab 10 | 800 x 1280 | 800 x 1280 |
| Chromebook Pixel | 1280 x 850 | 2560 x 1700 |

특정 장치의 방문자에게 활동을 제공하려면 활동 다이어그램에서 해당 장치의 적절한 대상을 선택합니다. 모바일 웹 작성기를 사용하여 해당 장치용 활동의 페이지를 편집하십시오. 모든 디바이스에서 올바로 표시되도록 전체 디지털 환경에서 활동을 실행하려면 타깃팅을 적용하지 마십시오. 대신 모바일 뷰포트를 사용하여 각 화면 크기의 활동을 미리 봅니다.

응답형 사이트의 경우 일반적으로 사이트는 특정 화면 크기의 장치에서 액세스할 때 다른 보기로 열립니다. 새 보기를 트리거하는 이러한 화면 크기는 CSS 중단점으로 알려져 있습니다. CSS 중단점은 방문자에게 최적의 레이아웃을 표시하기 위해 웹 사이트 컨텐츠가 장치 폭에 따라 응답하는 지점입니다. CSS 중단점을 [미디어 쿼리](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)라고도 합니다.

CSS 중단점을 [!DNL Target]에 저장하면 정의한 각 뷰에 대한 경험을 미리 볼 수 있습니다. 이러한 각 경험은 [!DNL Target] 인터페이스의 모바일 뷰포트에 표시됩니다. 디스플레이 상단에 있는 해당 뷰포트를 클릭하여 각 화면 크기에 대한 보기를 여십시오.

사이트가 응답적이지 않은 경우 모바일 웹 작성기를 사용하여 활동이 특정 장치에 타깃팅된 경우 사이트를 봅니다.

>[!IMPORTANT]
>
>모바일 뷰포트 내에서 경험을 편집할 수 있습니다. 하지만 이러한 변경 사항은 작업 중인 뷰포트뿐만 아니라 모든 뷰포트 및 장치에 적용됩니다. 마찬가지로, 일반 데스크톱 보기에서 경험을 편집하면 페이지가 데스크톱 보기뿐만 아니라 모든 화면 크기용으로 변경됩니다. 현재 [!DNL Target]은(는) 뷰포트 특정 페이지 변경을 지원하지 않습니다.

## 모바일 뷰포트 구성 {#task_B4B161499DC0470584ED922A4D20FCAB}

경험을 만드는 동안 사용할 수 있도록 하려는 모바일 뷰포트를 구성합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 모바일 뷰어 구성]** 섹션에서 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

   ![뷰포트 추가](/help/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   또는

   기존 모바일 뷰포트의 구성을 변경하려면 해당 뷰포트를 선택한 다음 [!UICONTROL 편집](연필) 아이콘을 클릭합니다.

1. 모바일 뷰포트의 이름을 입력합니다.

   모바일 뷰포트에 쉽게 인식할 수 있는 수사적 이름을 지정합니다. 이름은 최대 36자까지 사용할 수 있습니다.

1. 모바일 장치의 화면 크기(폭과 높이 모두)를 지정합니다.

   너비는 150~968픽셀일 수 있습니다. 높이는 150~1280픽셀일 수 있습니다.

1. (선택 사항) 장치의 운영 체제를 선택합니다.

   옵션:

   * Android
   * iOS
   * Windows
   * Symbian
   * Blackberry

   [Enhanced Experience Composer](/help/c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D)를 사용하고 운영 체제를 선택하면 페이지를 볼 때 [!DNL Target]는 해당 장치를 에뮬레이션합니다. 예를 들어 응답형 사이트의 iOS에 비해 Android에 대한 모양과 느낌이 다른 경우 [!DNL Target]은(는) 해당 동작을 모방합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>사용 중인 모바일 뷰포트를 삭제하려고 하면 다음 메시지가 표시됩니다.&quot;이 뷰포트는 현재 하나 이상의 활동과 연결되어 있습니다. 삭제하기 전에 해당 활동에서 뷰포트를 제거해야 합니다.&quot;

## 반응형 경험 {#task_D6332438B5EE48CCA8AF199270F1CAEF} 만들기

모바일 뷰포트를 [!DNL Target] 활동에 추가하여 모바일 화면에 대한 반응형 경험을 만듭니다.

1. [원하는 활동](/help/c-activities/activities.md)을 만듭니다.
1. [!UICONTROL Visual Experience Composer](VEC)에서 **[!UICONTROL 설정]** 톱니바퀴 아이콘을 클릭한 다음 **[!UICONTROL 모바일 뷰포트 추가]**&#x200B;를 선택합니다.

   ![모바일 보기 포트 추가 옵션](/help/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. **[!UICONTROL 장치]** 아이콘을 클릭한 다음, 모바일 뷰포트가 필요한 각 장치를 활성화합니다.

   ![모바일 보기 포트 사용](/help/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   모바일 뷰포트는 너비가 가장 좁은 것부터 가장 넓은 순으로 표시됩니다.

1. 원하는 대로 모바일 뷰포트를 편집합니다.

   경험에 대한 모든 변경 사항은 모든 장치의 경험에 적용됩니다. 예를 들어 머리글의 텍스트를 변경할 수 있습니다.

   뷰포트의 이름 위로 마우스를 가져가 뷰포트의 크기를 볼 수 있습니다.

   ![iPhone 11 Pro Max 반응형 경험](/help/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. 원하는 경우 원하는 방향 아이콘을 클릭하여 세로 모드와 가로 모드 간을 전환합니다.

   ![방향 옵션](/help/c-experiences/c-visual-experience-composer/assets/orientation.png)

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 시각적 경험 작성기(2/2)(7:29)  ![개요 배지](/help/assets/overview.png)

다음 데모 비디오에는 시각적 경험 작성기에서 모바일 뷰포트로 작업하는 방법에 대한 정보가 포함되어 있습니다.

* 경험 이름 변경 및 경험 복제
* 리디렉션 경험 만들기
* 활동을 단일 URL 또는 URL 그룹에 타깃팅
* 다중 페이지 활동 만들기
* 응답형 웹 사이트용 경험 미리 보기 및 빌드
* 오버레이를 사용하여 요소 유형을 강조 표시

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Adobe Target ![개요 배지](/help/assets/overview.png)의 계정 환경 설정

이 비디오에는 비디오의 4:40부터 모바일 뷰어 설정에 대한 정보가 포함되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
