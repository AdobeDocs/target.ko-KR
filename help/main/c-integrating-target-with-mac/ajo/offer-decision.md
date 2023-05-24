---
keywords: 시각적 경험 작성기 선택 사항;경험 작성기 선택 사항;경험 선택 사항;오퍼 결정;offer decisioning;ajo;여정 최적화 도구
description: 에서 만든 오퍼 결정을 추가하는 방법을 알아봅니다. [!DNL Adobe Journey Optimizer] (을)를 선택합니다.
title: 오퍼 의사 결정을 사용하려면 어떻게 합니까?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 1%

---

# 오퍼 의사 결정 사용

사용 [!DNL Adobe Target] 포함 [!DNL Adobe Journey Optimizer] 웹 및 모바일에서 방문자를 위한 다음 베스트 오퍼를 결정하고 제공하는 오퍼 의사 결정.

다음에서 생성된 오퍼 결정 추가 [!DNL Adobe Journey Optimizer] 끝 [!DNL Target] 활동(수동) [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타기팅]) [!UICONTROL 시각적 경험 작성기] (VEC) 또는 [!UICONTROL 양식 기반 작성기] 을 통해 제공되는 인바운드 채널에서 방문자에게 개인화된 오퍼를 테스트하고 전달합니다. [!DNL Target].

에 대한 자세한 내용 [!DNL Adobe Journey Optimizer] 및 오퍼 의사 결정은 *[!DNL Journey Optimizer]* 설명서:

* [Journey Optimizer 시작하기](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [의사 결정 관리 정보](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html)

## 전제 조건

에서 오퍼 의사 결정을 사용하려면 [!DNL Target], 다음이 필요합니다.

* [!DNL Adobe Target Standard] 또는 [!DNL Adobe Target Premium] 를 사용하여 구현됨 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

   이 기능은 구현 시 사용할 수 없습니다. [!DNL Target] at.js 또는 기타 [!DNL Target] SDK.

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer decisioning) 또는 [!DNL Adobe Experience Platform] 및 [!UICONTROL Offer decisioning] 응용 프로그램 서비스 추가 기능입니다.

## 샘플 사용 사례

다음 예는 를 사용할 수 있는 방법의 사용 사례입니다. [!DNL Target]/[!DNL Adobe Journey Optimizer] 에서 오퍼 의사 결정을 사용하기 위한 통합 [!DNL Target] 활동:

### 스포츠 머천다이징

스포츠 리그의 마케터는 홈페이지(데스크탑 및 모바일 웹 사이트 모두)에서 콘텐츠를 개인화할 수 있습니다. 다차원 기반의 콘텐츠를 개인화하고 관련 프랜차이즈 상품을 쇼핑할 수 있는 오퍼를 제시하고자 합니다. 다음에 관심이 있습니다.

* 방문자가 가장 좋아하는 팀
* 최근 선수/선수 활동(예: 팀 이동, 계약 업데이트 또는 부상)

예를 들어, 도르트문트, 프랑크푸르트, 보훔 등의 각 지역과 이러한 팀의 암시적이고 명시적인 팬인 사용자에게 개인화된 경험을 제공하려고 합니다. 지표로, 상품 사이트 방문 횟수 및 클릭 수를 확인하고자 합니다.

을(를) 디자인하려는 경우 [!UICONTROL A/B 테스트] 기본 경험과 개인화된 경험(각 지역 및 팀에 대한 오퍼와 함께 오퍼 의사 결정 포함) 간의 활동(50/50 분할). 이 활동을 사용하여 개인화된 경험과 제어에 대한 전환 및 상승도를 결정하려고 합니다.

### 게임 스트리밍 플랫폼

게임 조직의 마케터로서 독일, 프랑스, 멕시코, 브라질 등 다양한 지역의 데스크탑 및 모바일 사용자를 위한 게임 스트리밍 플랫폼을 위한 개인화된 오퍼를 제공하고자 합니다. 방문자가 이러한 지역 중 하나에서 데스크탑 또는 모바일 웹 사이트에 액세스하면 로컬 언어로 게임 스트리밍에 대한 오퍼를 로컬 통화에 대한 해당 가격과 함께 제공하려고 합니다.

위치 [!DNL Adobe Journey Optimizer], 타겟팅된 각 지역에 대해 개인화된 홈 페이지 히어로 오퍼를 만들고 기본 홈 페이지 히어로가 있는 대체 오퍼를 만들 수 있습니다. 그런 다음 이러한 오퍼와 해당 자격 규칙을 통합하는 오퍼 결정을 만들 수 있습니다. 그런 다음 [!DNL Target], 다음을 만들 수 있습니다. [!DNL Experience Targeting] (XT) 데스크탑 또는 모바일 웹 사이트에 해당 오퍼 결정을 삽입 및 활동하여 방문자에게 개인화된 경험을 제공합니다.

## 오퍼 결정을 사용하는 경험을 만듭니다.

1. 설명서 편집 또는 작성 중 [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타기팅] (XT) 활동 [!UICONTROL 시각적 경험 작성기] (VEC) 페이지 요소를 클릭하여 [옵션 메뉴](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![시각적 경험 작성기의 선택 사항 메뉴](assets/options-menu1.png)

   >[!NOTE]
   >
   >다음을 사용하는 경험을 만들 수도 있습니다. [!UICONTROL 오퍼 결정] 다음에서 [[!UICONTROL 양식 기반 경험 작성기]](/help/main/c-experiences/form-experience-composer.md).

1. 클릭 **[!UICONTROL 다음 항목 앞에 삽입]**, **[!UICONTROL 다음 항목 뒤에 삽입]**, 또는 **[!UICONTROL 컨텐츠 바꾸기]**&#x200B;을 클릭한 다음 을 클릭합니다 **[!UICONTROL 오퍼 결정]**.

   다음 [!UICONTROL 오퍼 결정] 옵션을 편집하거나 만들 때 사용할 수 있습니다. [manual [!UICONTROL A/B 테스트]](/help/main/c-activities/t-test-ab/test-ab.md#types) 또는 [[!UICONTROL 경험 타기팅]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) 활동만 이 옵션은 다른 활동 유형에는 사용할 수 없습니다. 메뉴에서 사용할 수 있는 옵션은 선택한 요소에 따라 달라집니다.

   ![시각적 경험 작성기의 선택 사항 메뉴](assets/options-menu.png)

1. 다음에서 **[!UICONTROL 오퍼 결정 추가]** 대화 상자에서 원하는 샌드박스와 배치를 선택합니다.

   A [샌드박스](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in the [!DNL Adobe Experience Platform] lets you partition your instance into virtual environments. For example, you might have a production environment and a staging environment. A [placement](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} 위치: [!DNL Adobe Journey Optimizer] 는 올바른 오퍼 컨텐츠가 올바른 위치에 표시되도록 하는 데 도움이 됩니다.

   ![오퍼 결정 추가 대화 상자의 샌드박스 및 배치 드롭다운 목록](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. 원하는 오퍼 결정을 선택하고 **[!UICONTROL 만들기]**.

   ![오퍼 결정 추가 대화 상자에서 선택한 오퍼 결정](assets/offer-decision.png)

   웹 사이트는에서 새로 만든 오퍼 결정을 볼 수 있는 VEC에 표시됩니다. [!UICONTROL 수정 사항] 오른쪽 창 마우스를 수정 사항 위로 가져간 다음 [!UICONTROL 미리 보기] 아이콘을 클릭하여 오퍼 결정을 검사합니다.

   ![미리 보기 아이콘](assets/preview-icon.png)

   아래쪽의 적절한 아이콘을 클릭하여 오퍼에 포함된 다양한 오퍼를 검사할 수 있습니다 [!UICONTROL 오퍼 미리 보기] 대체 오퍼가 포함된 대화 상자. 대체 오퍼는 방문자가 컬렉션에 있는 개인화된 오퍼에 대한 자격이 없을 때 표시되는 기본 오퍼입니다.

   ![오퍼 미리보기](assets/offer-preview.png)

1. 다음을 완료하여 활동 만들기를 완료합니다. [!UICONTROL 타겟팅] 및 [!UICONTROL 목표 및 설정] 안내가 있는 3부분 워크플로의 단계입니다.

   >[!IMPORTANT]
   >
   >을(를) 확인하기 위해 [!DNL Target] 활동이 개인화되었습니다. 현재 활동 시작/종료 날짜가 오퍼 결정의 시작/종료 날짜와 동기화되었는지 확인하십시오. [!DNL Adobe Journey Optimizer]. 다음과 같은 경우 [!DNL Target] 시작/종료 날짜가 오퍼 결정의 시작/종료 날짜 범위(기본값)를 벗어났습니다. [!DNL Target] 방문자에게 컨텐츠가 표시됩니다.

   ![오퍼 결정 경고 메시지](/help/main/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## 참고 사항 및 제한 사항

오퍼 결정을 사용할 때 다음 정보를 고려하십시오.

* offer decisioning 통합은 다음에 대해 작동합니다. [!DNL Target] 를 기반으로 한 구현 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. 이 기능은 구현 시 사용할 수 없습니다. [!DNL Target] at.js 또는 기타 [!DNL Target] SDK.

* 다음 [!DNL Target]/[!DNL Adobe Journey Optimizer] 통합 지원 [manual [!UICONTROL A/B 테스트]](/help/main/c-activities/t-test-ab/test-ab.md#types) 및 [[!UICONTROL 경험 타기팅]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) 활동만 이 기능은 다른 활동 유형에는 사용할 수 없습니다.

* 다음을 사용할 수 없습니다. [[!UICONTROL 보고 소스로서의 Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) (활동에서 오퍼 의사 결정을 사용하는 경우). 선택 [!DNL Target] 을(를) 의 보고 소스로 사용 [!UICONTROL 목표 및 설정] 활동에서 오퍼 의사 결정을 사용하는 경우 활동 설정 중 페이지를 표시합니다.

* 텍스트/html 컨텐츠 유형의 오퍼는 deliveryURL 컨텐츠 전달을 지원하지 않습니다. deliveryURL은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 클라이언트가 컨텐츠를 명시적으로 가져오고 작성하는 역할을 하는 경우에만 해당됩니다.

* [!DNL Target] 보고에서는 오퍼 결정 수준 보고를 제공하지 않습니다.

* 시각화 [QA 링크](/help/main/c-activities/c-activity-qa/activity-qa.md) 대상 [!DNL Target] 오퍼 의사 결정이 포함된 경험은 의 빈도 제한 세트에 영향을 줍니다. [!DNL Adobe Journey Optimizer] 오퍼 의사 결정.
