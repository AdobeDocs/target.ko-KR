---
keywords: 반응형;모바일 뷰포트;뷰포트;장치;모바일;반응형 웹 디자인;RWD
description: 모바일 뷰포트는 Adobe [!DNL Target] 활동이 다양한 크기의 Screens에서 어떻게 표시되는지 확인하는 데 도움이 됩니다. 자주 찾는 장치 뷰포트 크기 및 해상도 목록을 확인하십시오.
title: 반응형 경험을 위해 모바일 뷰포트를 사용하는 방법은 무엇입니까?
feature: Visual Experience Composer (VEC)
exl-id: 1062e7a1-10b4-4746-bce9-67017978578d
TQID: 'https://experienceleague.adobe.com/uBJtaoaCh28mRGwc-SlK-XhU6sOIK3RaT58-ZXxSsHw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 19%
---
# 반응형 경험을 위한 모바일 뷰포트 {#mobile-viewports}

>[!BEGINSHADEBOX]

**이 페이지에서:** 모바일 뷰포트를 구성하고 이를 사용하여 다양한 크기의 화면에 대한 환경을 미리 보고 빌드하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

모바일 뷰포트는 다양한 장치의 화면 크기로 [!DNL Adobe Target] 활동을 표시합니다. 데스크탑, 노트북, 태블릿 및 휴대폰에 자동으로 적용되는 반응형 사이트를 위해 설계되었으며 각 사이트에서 경험이 잘 렌더링되는지 확인할 수 있습니다.

>[!NOTE]
>
> * 사이트가 응답하고 모바일 페이지가 다른 레이아웃에서 데스크탑 페이지의 요소를 재사용하는 경우 모바일 뷰포트를 사용합니다. 모바일 사이트가 분리되어 있고 `m.mysite.com`과(와) 같은 자체 구조가 있는 경우 대신 [다중 페이지 활동](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#multipage-activity)을 사용하십시오.
>
>* 리디렉션 오퍼 오버레이가 겹치면 모바일 뷰포트를 사용할 수 없습니다.

## 뷰포트 및 CSS 중단점

뷰포트는 웹 페이지가 채우는 화면의 영역입니다. 스크롤 막대 및 도구 모음을 제외한 브라우저 창의 크기입니다. 브라우저는 CSS 픽셀로 측정하므로, retina 스크린이 있는 디바이스와 같이 많은 디바이스에서 뷰포트가 광고된 디바이스 해상도보다 작습니다. 항상 [!DNL Target]의 뷰포트 크기를 사용하십시오. 다음 표에는 자주 사용하는 장치에 대한 두 값이 모두 나열되어 있습니다.

+++ 많이 사용되는 장치의 뷰포트 및 해상도

>[!NOTE]
>
>다양한 웹 사이트에서 많이 사용되는 장치에 대한 뷰포트 크기 목록을 제공합니다. (예: `https://viewportsizer.com/devices/`) 가장 정확한 최신 정보를 확인하려면 장치 제조업체의 웹 사이트를 참조하십시오.
>
>뷰포트 크기가 &quot;est&quot;로 표시됨. 는 예상 값입니다.

| 디바이스 | 뷰포트 크기(폭 x 높이) | 디바이스 해상도(폭 x 높이) |
|---|---|---|
| iPhone Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone Pro | 402 x 874 | 1206 x 2622 |
| iPhone Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone Pro | 402 x 874 | 1206 x 2622 |
| iPhone 항공 | 420 x 912 | 1260 x 2736 |
| iPhone | 402 x 874 | 1206 x 2622 |
| iPhone 16e | 390 x 844 | 1170 x 2532 |
| iPad (A16) | 820 x 1180 | 1640 x 2360 |
| iPad mini (A17 Pro) | 744 x 1133 | 1488 x 2266 |
| iPad Air 11&quot; (M3 / M4) | 820 x 1180 | 1640 x 2360 |
| iPad Pro 11&quot;(M5) | 834 x 1210 | 1668 x 2420 |
| Google 픽셀 11 | 412 x 924(예상) | 1080 x 2424 |
| Google Pixel 11 Pro | 410 x 914(예상) | 1280 x 2856 |
| Google Pixel 11 Pro XL | 448 x 997(예상) | 1344 x 2992 |
| Google 픽셀 10 | 412 x 924 | 1080 x 2424 |
| Google Pixel 10 Pro | 410 x 914(예상) | 1280 x 2856 |
| Google Pixel 10 Pro XL | 448 x 997(예상) | 1344 x 2992 |
| 삼성 갤럭시 | 360 x 780 | 1080 x 2340 |
| 삼성 갤럭시 울트라 | 412 x 891 | 1440 x 3120 |
| iPhone 듀오(펼침) | 890 x 626(예상) | 2670 x 1878 |
| iPhone 듀오(접힌) | 466 x 678(예상) | 1398 x 2034 |
| Samsung Galaxy Z Fold 7 (접힌) | 412 x 960(예상) | 1080 x 2520 |
| 삼성 갤럭시 플립 | 360 x 840(예상) | 1080 x 2520 |
| Google Pixel 11 Pro Fold(펼침) | 791 x 820(예상) | 2076 x 2152 |

+++

응답형 사이트는 특정 화면 크기의 다른 레이아웃으로 전환됩니다. 이러한 크기를 CSS 중단점 또는 [미디어 쿼리](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)라고 합니다. 사이트의 CSS 중단점을 [!DNL Target]에 저장하면 각 보기를 미리 볼 수 있으며, 디스플레이 위쪽에 있는 뷰포트를 클릭하면 해당 화면 크기에 대한 보기가 열립니다.

특정 장치에 활동을 전달하려면 활동 다이어그램에서 해당 장치의 대상을 선택한 다음, 모바일 웹 작성기에서 해당 장치의 페이지를 편집하십시오. 활동이 특정 디바이스를 타깃팅할 때 응답하지 않는 사이트를 보는 데 동일한 도구를 사용합니다. 모든 장치에서 활동을 실행하려면 타깃팅을 적용하지 않고 모바일 뷰포트를 통해 각 화면 크기에서 활동을 미리 봅니다.

>[!IMPORTANT]
>
>경험은 모바일 뷰포트 내에서 편집할 수 있지만 변경 사항은 사용 중인 뷰포트뿐만 아니라 모든 뷰포트 및 장치에 적용됩니다. 마찬가지로 데스크탑 보기에서 경험을 편집하면 모든 화면 크기에 대해 페이지가 변경됩니다. [!DNL Target]은(는) 현재 뷰포트별 페이지 변경을 지원하지 않습니다.

## 모바일 뷰포트 구성 {#task_B4B161499DC0470584ED922A4D20FCAB}

경험을 만들 때 사용할 수 있는 모바일 뷰포트를 정의합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 모바일 뷰포트 구성]** 섹션에서 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

   ![뷰포트 추가](/help/main/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   또는

   기존 모바일 뷰포트의 구성을 변경하려면 해당 뷰포트를 선택한 다음 **[!UICONTROL 편집]**(연필 모양) 아이콘을 클릭합니다.

1. 모바일 뷰포트에 대한 수사적 이름을 입력합니다. 이름은 최대 36자까지 사용할 수 있습니다.
1. 모바일 장치의 화면 크기를 입력합니다. 폭은 150 내지 968 픽셀일 수 있고, 높이는 150 내지 1280 픽셀일 수 있다.
1. (선택 사항) 장치의 운영 체제를 선택합니다.

   옵션:

   * Android
   * iOS
   * Windows
   * Symbian
   * Blackberry

   [향상된 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#enable-eec)를 사용하도록 설정하고 운영 체제를 선택한 경우 [!DNL Target]은(는) 페이지를 볼 때 해당 장치를 에뮬레이션합니다. 예를 들어 응답형 사이트에 iOS과 Android의 모양과 느낌이 다른 경우 [!DNL Target]이(가) 해당 동작을 모방합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>사용 중인 모바일 뷰포트를 삭제하려고 하면 다음 메시지가 표시됩니다. &quot;이 뷰포트가 현재 하나 이상의 활동과 연결되어 있습니다. 뷰포트를 삭제하려면 먼저 해당 활동에서 뷰포트를 제거해야 합니다.&quot;

## 반응형 경험 작성 {#task_D6332438B5EE48CCA8AF199270F1CAEF}

모바일 화면을 위한 응답형 경험을 만들려면 모바일 뷰포트를 [!DNL Target] 활동에 추가하십시오.

1. [원하는 활동](/help/main/c-activities/activities.md)을 만듭니다.
1. **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 **[!UICONTROL 설정]** 톱니바퀴 아이콘을 클릭한 다음 **[!UICONTROL 모바일 뷰포트 추가]**&#x200B;를 선택합니다.

   ![모바일 뷰포트 옵션 추가](/help/main/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. **[!UICONTROL 장치]** 아이콘을 클릭한 다음 모바일 뷰포트가 필요한 각 장치를 활성화합니다.

   ![모바일 뷰포트 활성화](/help/main/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   모바일 뷰포트는 너비가 가장 좁은 것부터 가장 넓은 순으로 표시됩니다.

1. 필요에 따라 모바일 뷰포트에서 경험을 편집합니다. 모든 변경 사항은 제목 텍스트 변경 사항과 같은 모든 장치의 경험에 적용됩니다. 뷰포트의 이름 위로 마우스를 가져가 뷰포트의 크기를 볼 수 있습니다.

   ![iPhone 11 Pro Max 반응형 경험](/help/main/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. (선택 사항) 방향 아이콘을 클릭하여 세로 및 가로 모드 간을 전환합니다.

   ![방향 옵션](/help/main/c-experiences/c-visual-experience-composer/assets/orientation.png)

## 교육 비디오

다음 비디오에는 모바일 뷰포트에 대한 자세한 정보가 포함되어 있습니다.

### 시각적 경험 작성기(2/2) (7:29) ![개요 배지](/help/main/assets/overview.png)

다음 데모 비디오에는 시각적 경험 작성기를 사용하여 모바일 뷰포트 작업에 대한 정보가 포함되어 있습니다.

* 경험 이름 변경 및 경험 복제
* 리디렉션 경험 만들기
* 활동을 단일 URL 또는 URL 그룹에 타기팅
* 다중 페이지 활동 만들기
* 반응형 웹 사이트용 경험 미리보기 및 빌드
* 오버레이를 사용하여 요소 유형을 강조 표시

>[!VIDEO](https://video.tv.adobe.com/v/30526?captions=kor)

### Adobe Target ![개요 배지](/help/main/assets/overview.png)의 계정 환경 설정

이 비디오에는 모바일 뷰포트 설정에 대한 정보(4:40)가 포함되어 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3507630?captions=kor)
