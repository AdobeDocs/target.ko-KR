---
keywords: 시각적 경험 작성기 선택 사항;경험 작성기 선택 사항;경험 선택 사항;오퍼 결정;offer decisioning;ajo;여정 최적화 프로그램
description: 에서 만든 오퍼 결정을 추가하는 방법을 알아봅니다 [!DNL Adobe Journey Optimizer] 활동에 대한 업데이트입니다.
title: 오퍼 결정을 사용하려면 어떻게 해야 합니까?
feature: Visual Experience Composer (VEC)
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: 987a6a8d9726f631e0c1416df62a0ed18d5e544a
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---

# 오퍼 결정 사용

사용 [!DNL Adobe Target] with [!DNL Adobe Journey Optimizer] 웹 및 모바일에서 방문자를 위한 다음 최상의 오퍼를 결정하고 전달하는 오퍼를 결정합니다.

에서 만든 오퍼 결정 추가 [!DNL Adobe Journey Optimizer] to [!DNL Target] 활동(수동) [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타깃팅])을 사용하여 다음을 수행할 수 있습니다. [!UICONTROL 시각적 경험 작성기] (VEC) 또는 [!UICONTROL 양식 기반 작성기] 다음 방법으로 제공되는 인바운드 채널에서 개인화된 오퍼를 방문자에게 테스트 및 전달합니다 [!DNL Target].

>[!NOTE]
>
>현재 베타 버전에서 이 항목에 설명된 오퍼 결정 기능이며 고객만 선택할 수 있습니다.

에 대한 자세한 정보 [!DNL Adobe Journey Optimizer]를 참조하십시오. [Journey Optimizer 시작](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html) 에서 *Journey Optimizer* 설명서.

오퍼 결정에 대한 자세한 내용은 [의사 결정 관리 정보](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html) 에서 *[!DNL Journey Optimizer]설명서*.

## 전제 조건

에서 오퍼 결정을 사용하려면 [!DNL Target]를 채울 때는 다음 항목이 필요합니다.

* [!DNL Adobe Target Standard] 또는 [!DNL Adobe Target Premium] 를 사용하여 [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

   이 기능은 구현할 때 사용할 수 없습니다 [!DNL Target] at.js 또는 기타 [!DNL Target] SDK

* [!DNL Adobe Journey Optimizer Ultimate] (AJ0 + Offer decisioning) 또는 [!DNL Adobe Experience Platform] 그리고 [!UICONTROL offer decisioning] 응용 프로그램 서비스 추가 기능.

## 샘플 사용 사례

다음 예는 를 사용할 수 있는 방법에 대한 사용 사례입니다 [!DNL Target]/[!DNL Adobe Journey Optimizer] 통합 [!DNL Target] 활동:

### 스포츠 머천다이징

스포츠 리그의 마케터는 홈 페이지(데스크탑 및 모바일 웹 사이트 모두)에서 콘텐츠를 개인화하려고 합니다. 여러 차원을 기반으로 컨텐츠를 개인화하고 관련 가맹점 제품을 구매할 수 있는 오퍼를 제공하려는 경우 관심 있는 사항:

* 방문자가 가장 좋아하는 팀
* 최근 선수/플레이어 활동(예: 팀 이동, 계약 업데이트 또는 부상)

예를 들어 다음 각 지역에 대해 개인화된 경험을 제공하려고 합니다. 도르트문트, 프랑크푸르트, 보훔과 이 팀의 암시적이고 노골적인 팬인 사용자들을 위한. 지표로 제품 사이트에 대한 방문 및 클릭 수를 볼 수 있습니다.

디자인 [!UICONTROL A/B 테스트] 기본 경험과 개인화된 경험 간에 활동(50/50 분할). 여기에는 각 지역 및 팀에 대한 오퍼가 포함된 오퍼 결정이 포함됩니다. 이 활동을 사용하여 개인화된 경험과 제어에 대한 전환과 상승도를 결정하려고 합니다.

### 게임 스트리밍 플랫폼

게임 조직의 마케터는 다양한 지역의 데스크탑 및 모바일 사용자를 위한 게임 스트리밍 플랫폼에 대한 개인화된 오퍼를 제공하고자 합니다. 독일, 프랑스, 멕시코, 그리고 브라질. 방문자가 해당 지역 중 하나에서 데스크탑 또는 모바일 웹 사이트에 액세스하면 로컬 언어로 게임 스트리밍을 위한 오퍼를 제공하고 로컬 통화에 해당하는 가격으로 제공하려고 합니다.

in [!DNL Adobe Journey Optimizer]를 설정하는 경우 타깃팅된 각 지리적 위치에 대해 개인화된 홈 페이지 영웅 오퍼와 기본 홈 페이지 히어로 대체 오퍼를 만들 수 있습니다. 그런 다음 이러한 오퍼와 해당 자격 규칙을 통합하는 오퍼 결정을 만들 수 있습니다. 그런 다음 [!DNL Target]를 만들 수 있습니다 [!DNL Experience Targeting] (XT) 활동을 만들고 데스크탑 또는 모바일 웹 사이트에 해당 오퍼 결정을 삽입하여 방문자에게 개인화된 경험을 제공합니다.

## 오퍼 결정을 사용하는 경험을 만듭니다.

1. 설명서를 편집하거나 작성하는 동안 [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타깃팅] (XT) 활동을 만들 수도 있습니다 [!UICONTROL 시각적 경험 작성기] (VEC)에서 페이지 요소를 클릭하여 [옵션 메뉴](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![시각적 경험 작성기의 옵션 메뉴](assets/options-menu1.png)

   >[!NOTE]
   >
   >를 사용하는 경험을 만들 수도 있습니다 [!UICONTROL 오퍼 결정] 에서 [[!UICONTROL 양식 기반 경험 작성기]](/help/c-experiences/form-experience-composer.md).

1. 클릭 **[!UICONTROL 다음 항목 앞에 삽입]**, **[!UICONTROL 다음 항목 뒤에 삽입]**, 또는 **[!UICONTROL 컨텐츠 바꾸기]**&#x200B;를 클릭한 다음 **[!UICONTROL 오퍼 결정]**.

   다음 [!UICONTROL 오퍼 결정] 옵션을 사용하거나 만들 때 사용할 수 있습니다 [수동 [!UICONTROL A/B 테스트]](/help/c-activities/t-test-ab/test-ab.md#types) 또는 [[!UICONTROL 경험 타깃팅]](/help/c-activities/t-experience-target/experience-target.md) (XT) 활동만 해당. 이 옵션은 다른 활동 유형에는 사용할 수 없습니다. 메뉴에서 사용할 수 있는 옵션은 선택한 요소에 따라 다릅니다.

   ![시각적 경험 작성기의 옵션 메뉴](assets/options-menu.png)

1. 에서 **[!UICONTROL 오퍼 결정 추가]** 대화 상자에서 원하는 샌드박스 및 배치를 선택합니다.

   A [샌드박스](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html)의 {target=_blank} [!DNL Adobe Experience Platform] 인스턴스를 가상 환경으로 분할할 수 있습니다. 예를 들어 프로덕션 환경과 스테이징 환경이 있을 수 있습니다. A [배치](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/create-components/creating-placements.html){target=_blank}의 [!DNL Adobe Journey Optimizer] 은 올바른 오퍼 컨텐츠가 올바른 위치에 표시되는지 확인하는 데 도움이 됩니다.

   ![오퍼 결정 추가 대화 상자의 샌드박스 및 배치 드롭다운 목록](/help/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. 원하는 오퍼 결정을 선택하고 을 클릭합니다 **[!UICONTROL 만들기]**.

   ![오퍼 결정 추가 대화 상자에서 선택한 오퍼 결정](assets/offer-decision.png)

   웹 사이트는 VEC에 표시되며, 여기서 에서 새로 만든 오퍼 결정을 볼 수 있습니다 [!UICONTROL 수정 사항] 오른쪽 창. 수정 사항을 마우스로 가리킨 다음 [!UICONTROL 미리 보기] 아이콘을 클릭하여 오퍼 결정을 검사합니다.

   ![미리 보기 아이콘](assets/preview-icon.png)

   오퍼의 하단에 있는 적절한 아이콘을 클릭하여 오퍼에 포함된 다양한 오퍼를 검사할 수 있습니다 [!UICONTROL 오퍼 미리 보기] 대체 오퍼를 포함하는 대화 상자. 방문자가 컬렉션에서 개인화된 오퍼에 적합하지 않을 때 표시되는 기본 오퍼는 대체 오퍼입니다.

   ![오퍼 미리 보기](assets/offer-preview.png)

1. 을(를) 완료하여 활동 만들기를 완료합니다 [!UICONTROL 타깃팅] 및 [!UICONTROL 목표 및 설정] 세 부분으로 구성된 안내 워크플로우의 단계입니다.

   >[!IMPORTANT]
   >
   >다음을 확인하려면 [!DNL Target] 활동이 개인화된 경우, 현재 활동 시작/종료 날짜가 오퍼 결정의 시작/종료 날짜와 동기화되어 있는지 확인하십시오. [!DNL Adobe Journey Optimizer]. 만약 [!DNL Target] 시작/종료 날짜는 오퍼 결정의 시작/종료 날짜 범위인 기본 날짜 범위를 벗어납니다 [!DNL Target] 방문자에게 콘텐츠가 표시됩니다.

   ![오퍼 결정 경고 메시지](/help/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## 참고 및 제한 사항

오퍼 결정을 사용하여 작업할 때 다음 참고 사항 및 제한 사항을 고려하십시오.

* offer decisioning 통합은 [!DNL Target] 구현을 기반으로 합니다 [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). 이 기능은 구현할 때 사용할 수 없습니다 [!DNL Target] at.js 또는 기타 [!DNL Target] SDK

* Target/Adobe Journey Optimizer 통합이 지원합니다 [수동 [!UICONTROL A/B 테스트]](/help/c-activities/t-test-ab/test-ab.md#types) 및 [[!UICONTROL 경험 타깃팅]](/help/c-activities/t-experience-target/experience-target.md) (XT) 활동만 해당. 이 기능은 다른 활동 유형에는 사용할 수 없습니다.

* 텍스트/html 콘텐츠 유형을 사용하는 오퍼는 deliveryURL 콘텐츠 전달을 지원하지 않습니다. deliveryURL은 클라이언트가 컨텐츠를 명시적으로 가져오고 작성할 책임이 있는 양식 기반 경험 작성기를 통해 지원됩니다.

* [!DNL Target] 보고에서는 오퍼 결정 수준 보고를 제공하지 않습니다.

* 시각화 [QA 링크](/help/c-activities/c-activity-qa/activity-qa.md) 대상 [!DNL Target] 오퍼 결정을 포함하는 경험은 설정된 빈도 제한에 영향을 줍니다 [!DNL Adobe Journey Optimizer] 이러한 오퍼 결정을 위한 것입니다.
