---
keywords: 최적화;개인화;adobe 여정 최적화 프로그램;ajo;사용 사례;시나리오;콘텐츠 변경/ab 테스트;프로필 속성;이미지 변경;이미지 교체
description: Adobe Journey Optimizer의 효과적인 A/B 테스트 콘텐츠 변경 사항 비밀 잠금 해제
title: ' [!DNL Adobe Journey Optimizer]의 A/B 테스트를 통한 콘텐츠 변경'
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
source-git-commit: b66abe9649f8c257891c1cd8e5736b7f91501c13
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 1%

---

# [!DNL Adobe Journey Optimizer]에서 A/B 테스트를 통한 콘텐츠 변경

이 사용 사례는 [!DNL Adobe Journey Optimizer]에서 효과적인 A/B 테스트 콘텐츠 변경 내용에 대한 비밀을 잠금 해제하는 데 도움이 됩니다.

이 사용 사례에서는 [!DNL Adobe Target] 대신 [!DNL Journey Optimizer]을(를) 사용하여 [!DNL Adobe Target]의 [A/B 테스트 활동](/help/main/c-activities/t-test-ab/test-ab.md)을 통해 A/B 테스트와 같은 익숙한 작업을 수행하는 방법을 보여 줍니다.

## 이점 및 가치

* **콘텐츠 효율성 최적화**: 고객에게 가장 공감하는 콘텐츠 변형 및 요소를 확인하여 참여도 및 전환율을 높일 수 있습니다.
* **데이터 기반 결정**: 데이터를 활용하여 콘텐츠 전략에서 정보에 입각한 결정을 내려 최대의 효과를 얻을 수 있습니다.
* **개인화된 사용자 경험**: 모든 대상 세그먼트의 고유한 환경 설정 및 요구 사항을 충족하도록 콘텐츠를 맞춤화합니다.

## 가능한 시나리오

* 한 의류 회사는 다양한 이미지를 테스트하고 클릭 유도 문안 텍스트에서 사용자 이름으로 캠페인 랜딩 페이지를 개인화하여 전환을 늘렸습니다.

* 한 전자상거래 업체는 자사 골드 충성도 멤버들이 캠페인 랜딩 페이지에서 다양한 제품 설명과 이미지를 테스트해 전환율이 높아져 매출 증가를 이끌었다는 사실을 발견했다.

## 단계

>[!NOTE]
>
>이 섹션의 지침은 이미지를 변경하고 프로필 속성을 사용하여 텍스트 메시지를 개인화하는 데 필요한 단계를 강조 표시합니다. [!DNL Journey Optimizer] 웹 디자이너의 사용 가능한 옵션에 대한 자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [웹 디자이너와 작업](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank}을 참조하십시오.
>
>페이지 하단에 있는 비디오가 특히 유용합니다.

프로필 스크립트를 사용하여 다양한 이미지를 테스트하고 사용자의 이름으로 메시지를 개인화하여 웹 페이지를 최적화하려면 다음을 수행하십시오.

1. [!DNL Journey Optimizer]에서 왼쪽 레일의 **캠페인**&#x200B;을 클릭하여 [!UICONTROL Campaigns] 페이지를 표시합니다.

1. [!UICONTROL Campaigns] 페이지의 오른쪽 위 모서리에서 **[!UICONTROL Create Campaign]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Scheduled - Marketing]**(기본값)을 선택한 다음 **만들기**&#x200B;를 클릭하여 [!UICONTROL Campaign] 세부 정보 페이지를 표시합니다.

1. **[!UICONTROL Properties]** 섹션에서 캠페인에 대한 설명 이름과 선택적 설명을 입력합니다.

1. (조건부) **[!UICONTROL Audience]** 섹션에서 **[!UICONTROL Select Audience]**&#x200B;을(를) 클릭하고 원하는 대상을 선택합니다.

   이 사용 사례의 경우 [!UICONTROL All Visitors]에 대한 캠페인(기본값)을 활성화할 수 있습니다.

1. **[!UICONTROL Action]** 섹션의 **[!UICONTROL Action]** 드롭다운 목록에서 **[!UICONTROL Web]**&#x200B;을(를) 선택한 다음 새 웹 구성을 선택하거나 만듭니다.

   웹 구성 또는 채널 표면은 시스템 관리자가 정의한 구성입니다. 웹 구성에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다.

   자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [채널 표면 설정](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank}을 참조하세요.

1. **[!UICONTROL Action]** 섹션에서 **[!UICONTROL Edit Content]**&#x200B;을(를) 클릭하여 [!DNL Journey Optimizer] 웹 디자이너에서 웹 사이트를 엽니다.

   A/B 테스트를 위해서는 두 개 이상의 실험이 필요합니다. 기존 홈 페이지를 첫 번째 실험으로 사용할 수 있습니다. 후속 단계에서는 두 번째 실험을 설정하는 방법을 설명합니다.

   ![LUMA 웹 사이트의 요가 랜딩 페이지](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. 더 나은 성과를 확인하는 실험을 만들려면 **[!UICONTROL Create Experiment]**&#x200B;을(를) 클릭합니다.

   콘텐츠 실험을 통해 메시지 콘텐츠, 주제 또는 발신자를 다양하게 설정하여 여러 처리를 정의하고 대상자에게 가장 적합한 조합을 결정할 수 있습니다. 자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [콘텐츠 실험 만들기](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank}를 참조하십시오.

1. 성공 지표를 선택하고 클릭 작업을 수행합니다.

   자세한 내용 및 관련 문서에 대한 링크를 보려면 도움말 아이콘을 클릭하십시오.

1. **[!UICONTROL Add Treatment]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   이 사용 사례에서는 각 실험에 대해 분포를 50%로 유지할 수 있다.

1. [!UICONTROL Campaign] 세부 정보 페이지의 **[!UICONTROL Action]**&#x200B;에서 **[!UICONTROL Edit Content]**&#x200B;을(를) 클릭합니다.

1. 처리 B 아래에서 웹 을 클릭합니다.

   이 사용 사례의 경우 A/B 테스트의 첫 번째 경험으로 원본 경험을 사용하려면 [!UICONTROL Treatment A]을(를) 변경하지 마십시오.

1. 오른쪽 레일에서 **[!UICONTROL Edit Web Page]**&#x200B;을(를) 클릭합니다.

   ![요가 랜딩 페이지의 콘텐츠 페이지 편집](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. 대표 이미지를 변경하려면 변경할 이미지를 클릭한 다음 **[!UICONTROL Choose Image]** 단추를 클릭합니다.

   ![이미지 선택 단추](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. 원하는 이미지를 찾아 선택한 다음 **[!UICONTROL Use This Image]**&#x200B;을(를) 클릭합니다.

   ![요가 페이지의 새로운 영웅 이미지](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. 프로필 속성을 사용하여 사용자의 이름을 사용하여 메시지를 개인화하려면 개인화할 텍스트를 클릭한 다음 **[!UICONTROL Add Personalization]**&#x200B;을(를) 클릭하여 [!UICONTROL Add Personalization] 페이지를 표시합니다.

   ![Personalization 단추 추가](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   프로필 특성에 대한 자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [개인화 편집기 시작하기](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank}를 참조하십시오.

1. 플러스 기호를 검색하여 &quot;이름&quot; 프로필 특성을 추가하고 텍스트를 원하는 대로 조정한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![이름에 대한 프로필 특성 추가](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [개인화 편집기 시작](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank}을 참조하세요.

1. 왼쪽 위 모서리에 있는 뒤로 화살표를 클릭하여 웹 디자이너로 돌아갑니다.

   ![뒤로 화살표](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. **[!UICONTROL Review to Activate]**&#x200B;을(를) 클릭하고 모든 항목이 예상대로 표시되는지 확인한 다음 **활성화**&#x200B;를 클릭합니다.

## 보고서 보기

[!UICONTROL Reports] 단추를 클릭한 다음 원하는 보고 기간을 클릭합니다.

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

자세한 내용은 *Journey Optimizer 설명서*&#x200B;에서 [새 보고 인터페이스 시작](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank}을 참조하세요.

>[!MORELIKETHIS]
>
>*Journey Optimizer 설명서*&#x200B;에서 [웹 디자이너와 작업](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank}
>[*Journey Optimizer 자습서*&#x200B;에서 캠페인 만들기](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank}
