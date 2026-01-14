---
keywords: 최적화;개인화;adobe 여정 최적화 도구;ajo;사용 사례;시나리오;콘텐츠 추가;콘텐츠 숨기기;구성 요소 추가;구성 요소 숨기기
description: ' [!DNL Adobe Journey Optimizer]을(를) 사용하여 웹 페이지에서 구성 요소를 추가하거나 숨기는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Journey Optimizer]에서 웹 페이지에 구성 요소 추가 또는 숨기기'
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
feature: Integrations
hide: true
hidefromtoc: true
exl-id: 8c4fba88-908e-4742-ac4b-bdf7f4c882db
source-git-commit: 122484056e73f8f679312a3e776e623d905701d5
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 2%

---

# 웹 페이지에 구성 요소 추가 또는 숨기기

이 사용 사례는 [!DNL Adobe Journey Optimizer]에서 효과적인 A/B 테스트 콘텐츠 변경 내용에 대한 비밀을 잠금 해제하는 데 도움이 됩니다.

이 사용 사례에서는 [&#x200B; 대신 &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md)을(를) 사용하여 [!DNL Journey Optimizer]A/B 테스트 활동[!DNL Adobe Target]으로 A/B 테스트와 같은 익숙한 작업을 수행하는 방법을 보여 줍니다.

이 사용 사례는 [!DNL Adobe Target]을(를) 사용하여 수행했을 수 있는 익숙한 작업, [A/B 테스트 활동](/help/main/c-activities/t-test-ab/test-ab.md)을(를) 사용하여 A/B 테스트를 수행했을 수 있지만 [!DNL Journey Optimizer]을(를) 사용하는 방법을 보여 주기 위해 설계되었습니다.

## 이점 및 가치

* **사용자 참여 개선**: 프로모션과 같은 관련 정보를 강조 표시하는 최적화된 페이지 디자인으로 사용자의 관심을 사로잡습니다.
* **검색 기능 개선**: 웹 또는 모바일 앱에 전략적으로 새 구성 요소나 콘텐츠를 배치하여 작업을 간소화하고 탐색을 향상시킵니다.
* **추가 터치 포인트 증가**: 비즈니스 영향을 가속화하는 전환 이벤트 및 목표를 효과적으로 사용자에게 안내합니다.

## 가능한 시나리오

* 한 금융회사는 대출계산기에 빠르게 접근할 수 있도록 홈페이지에 새로운 타일을 추가해 검색시간을 줄이고 대출신청이 활성화되도록 할 계획이다.

* 한 의류 회사는 웹 페이지에 새 call-to-action 버튼을 추가하여 전환율을 높였습니다.

## 단계

>[!NOTE]
>
>이 섹션의 지침은 이미지를 변경하고 프로필 속성을 사용하여 텍스트 메시지를 개인화하는 데 필요한 단계를 강조 표시합니다. [!DNL Journey Optimizer] 웹 디자이너의 사용 가능한 옵션에 대한 자세한 내용은 [Journey Optimizer 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank}에서 *웹 디자이너와 작업*&#x200B;을 참조하십시오.
>
>페이지 하단에 있는 비디오가 특히 유용합니다.

웹 페이지에서 구성 요소를 추가하거나 구성 요소를 숨기려면 다음 단계를 수행하십시오.

1. [!DNL Adobe Journey Optimizer]에서 왼쪽 레일의 **캠페인**&#x200B;을 클릭하여 [!UICONTROL Campaigns] 페이지를 표시합니다.

   캠페인 탭이 강조 표시된 ![Adobe Journey Optimizer 랜딩 페이지입니다.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. **[!UICONTROL Create Campaign]** 페이지의 오른쪽 위 모서리에서 [!UICONTROL Campaigns]을(를) 클릭합니다.

1. **[!UICONTROL Scheduled - Marketing]**(기본값)을 선택한 다음 **만들기**&#x200B;를 클릭하여 [!UICONTROL Campaign] 세부 정보 페이지를 표시합니다.

   ![Adobe Journey Optimizer의 캠페인 세부 정보 페이지](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. **[!UICONTROL Properties]** 섹션에서 캠페인에 대한 설명 이름과 선택적 설명을 입력합니다.

1. (조건부) **[!UICONTROL Audience]** 섹션에서 **[!UICONTROL Select Audience]**&#x200B;을(를) 클릭하고 원하는 대상을 선택합니다.

   이 사용 사례의 경우 [!UICONTROL All Visitors]에 대한 캠페인(기본값)을 활성화할 수 있습니다.

1. **[!UICONTROL Action]** 섹션의 **[!UICONTROL Web]** 드롭다운 목록에서 **[!UICONTROL Action]**&#x200B;을(를) 선택한 다음 새 웹 구성을 선택하거나 만듭니다.

   웹 구성 또는 채널 표면은 시스템 관리자가 정의한 구성입니다. 웹 구성에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다.

   자세한 내용은 [Journey Optimizer 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank}에서 *채널 표면 설정*&#x200B;을 참조하세요.

1. **[!UICONTROL Action]** 섹션에서 **[!UICONTROL Edit Content]**&#x200B;을(를) 클릭하여 [!DNL Journey Optimizer] 웹 디자이너에서 웹 사이트를 엽니다.

   ![LUMA 웹 사이트의 요가 랜딩 페이지](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. 요소 숨기기를 추가하려면 오른쪽 레일에서 **[!UICONTROL Edit Web Page]**&#x200B;을(를) 클릭합니다.

1. 숨기려는 요소를 클릭한 다음 오른쪽 레일에서 [!UICONTROL Hide] 단추를 클릭합니다.

   오른쪽 레일에는 선택한 요소에 대해 수행할 수 있는 옵션이 표시됩니다. 이러한 옵션은 선택한 요소에 따라 다릅니다.

   ![요소 숨기기 단추](/help/main/c-integrating-target-with-mac/ajo/assets/hide-element.png)

1. 왼쪽 위 모서리에 있는 뒤로 화살표를 클릭하여 웹 디자이너로 돌아갑니다.

   ![뒤로 화살표](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. **[!UICONTROL Review to Activate]**&#x200B;을(를) 클릭하고 모든 항목이 예상대로 표시되는지 확인한 다음 **활성화**&#x200B;를 클릭합니다.

## 보고서 보기

[!UICONTROL Reports] 단추를 클릭한 다음 원하는 보고 기간을 클릭합니다.

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

자세한 내용은 [Journey Optimizer 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank}에서 *새 보고 인터페이스 시작*&#x200B;을 참조하세요.

>[!MORELIKETHIS]
>
>[Journey Optimizer 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank}에서 *웹 디자이너와 작업*
>[&#128279;](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank}Journey Optimizer 자습서&#x200B;*에서 캠페인 만들기*
