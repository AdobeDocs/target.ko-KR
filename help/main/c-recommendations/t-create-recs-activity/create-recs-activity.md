---
keywords: 권장 사항 만들기;권장 사항 활동;새 권장 사항;권장 사항 개요
description: VEC( [!DNL Target] [!UICONTROL Visual Experience Composer])를 사용하여  [!DNL Recommendations] 활동을 만드는 방법을 알아봅니다.
title: ' [!DNL Recommendations] 활동을 만드는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 52%

---

# [!DNL Recommendations] 활동 만들기

[!DNL Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC)을(를) 사용하여 [!DNL Recommendations]을(를) 사용할 수 있는 페이지에서 직접 [!DNL Target] 활동을 만들고 [!DNL Target] 내에서 해당 페이지의 부분을 수정합니다.

1. **[!UICONTROL Activities]** > **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**&#x200B;을(를) 클릭합니다.

1. 필요한 경우 **[!UICONTROL Visual]**&#x200B;을(를) 선택합니다.

   [!UICONTROL Form-Based Experience Composer]을(를) 사용하려면 [!UICONTROL Form]을(를) 선택하십시오. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL Form-Based Experience Composer] 외에 [!DNL Target]에서 [!UICONTROL Single Page Application] VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [작업 영역](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을(를) 선택합니다.

1. 활동 URL을 지정한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `http://www.adobe.com`] 및 [!DNL `https://wwww.adobe.com`]이(가) 모두 일치합니다.

   활동 URL은 권장 사항이 표시되는 페이지입니다.

   [!UICONTROL Create]을(를) 클릭하면 VEC가 열리고 페이지가 표시됩니다. 현재 요소를 권장 사항으로 바꾸거나 권장 사항을 삽입할 수 있습니다.

1. 페이지의 요소를 클릭한 다음, 해당 요소가 있는 위치에서 권장 사항을 사용할 수 있는 경우 **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]** 또는 **[!UICONTROL Insert Recommendations After]**&#x200B;을(를) 클릭합니다.

   사이트 방문자는 권장 사항에 적합한 경우에만 권장 콘텐츠를 보게 됩니다. 권장 사항에 대한 자격이 없는 방문자에게는 기본 콘텐츠가 표시됩니다.

   ![권장 사항 옵션](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: 요소를 권장 사항으로 바꾸면 현재 콘텐츠가 삭제되고 권장 사항으로 바뀝니다. 방문자가 사이트를 방문하여 권장 사항에 대한 자격을 얻으면, 기존 콘텐츠 대신 지정된 영역에 권장 사항 항목이 표시됩니다.
   * **[!UICONTROL Insert Recommendations Before]**: 선택한 요소 앞에 권장 사항을 삽입하면 해당 요소 앞에 권장 콘텐츠가 배치됩니다. 페이지 구성에 따라 권장 사항이 선택한 요소의 위 또는 왼쪽에 표시됩니다.
   * **[!UICONTROL Insert Recommendations After]**: 선택한 요소 뒤에 권장 사항을 삽입하면 해당 요소 뒤에 권장 콘텐츠가 배치됩니다. 페이지 구성에 따라 권장 사항이 선택한 요소의 아래 또는 오른쪽에 표시됩니다.

   **[!UICONTROL Expand Selection]** 옵션을 사용하면 선택한 위치(상위 컨테이너)를 확장하여 원하는 페이지 요소를 쉽게 식별하고 포함할 수 있습니다.

1. 페이지 유형을 선택합니다.

   페이지 유형에는 다음이 포함될 수 있습니다.

   * 장바구니 페이지
   * 카테고리 페이지
   * 홈 페이지
   * 랜딩 페이지
   * 제품 페이지
   * 검색 결과 페이지
   * 감사 페이지
   * 기타

   ![페이지 유형 선택 옵션](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 하나 이상 선택합니다.

   기준은 각 기준에 대한 정보를 표시하는 카드로 표시됩니다. 기본적으로 [!UICONTROL Select Criteria] 화면에는 업계 카테고리 및 이전 단계에서 선택한 페이지 유형과 호환되는 기준이 표시됩니다. 이러한 옵션을 변경하여 다른 기준을 표시할 수 있습니다.

   >[!NOTE]
   >
   >모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 `entity.categoryId`를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 활동에 대해 호환되지 않는 기준을 사용할 수 있도록 하려면 **[!UICONTROL Compatible]** 확인란의 선택을 취소하십시오. 권장 사항 설정에 따라 [!UICONTROL Compatible] 옵션이 표시되지 않을 수 있습니다(**[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). 자세한 내용은 [설정](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=ko){target=_blank}을 참조하십시오.

   ![기준 선택 대화 상자](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   여러 기준을 선택하는 경우 선택한 기준 간에 트래픽이 균일하게 분할됩니다. 예를 들어, 두 개의 기준을 선택했으며 기본 콘텐츠를 활동 참여자의 20%에게 표시하도록 활동이 디자인된 경우 활동 참여자의 40%에게 각 기준에 따른 권장 사항이 표시됩니다. 각 기준의 백분율을 변경하는 옵션은 없습니다.

   * 기존 기준을 검색하려면(예를 들어, 많은 기준 카드가 표시되는 경우) 원하는 기준이 나타날 때까지 검색 필드에 입력한 다음, 기준을 선택하고 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

     일부 기준은 [!DNL Recommendations]에서 제공됩니다. 사용자와 팀이 고유의 사용자 지정 기준을 만들 수도 있습니다.

   * 새 기준을 만들려면 **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**&#x200B;을(를) 클릭한 다음 새 기준에 대한 정보를 입력하십시오. 새 기준 만들기에 대한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.
   * 기준을 시퀀스로 그룹화할 수도 있습니다. 새 기준 시퀀스를 만들려면 **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**&#x200B;을(를) 클릭합니다. 자세한 내용은 [기준 시퀀스 만들기](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md)를 참조하십시오.

1. **[!UICONTROL Next]** 아이콘을 클릭합니다.
1. [디자인](/help/main/c-recommendations/c-design-overview/design-overview.md)을 선택합니다.

   디자인은 페이지에서 위치의 모양을 결정하는 템플릿입니다. [!DNL Target]에 사전 구성된 디자인이 여러 개 포함되어 있습니다. 사용자 고유의 사용자 지정 디자인을 만들 수도 있습니다. 자세한 내용은 [디자인 만들기](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) 및 [디자인 사용자 지정](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59)을 참조하십시오.

   ![디자인 선택 대화 상자](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   각 디자인은 어떤 모양으로 표시될지 보여 주는 그래픽 표현과 현재 해당 디자인을 사용하는 라이브 및 비활성 활동의 수를 보여 주는 아이콘을 표시합니다.

   * 하나 이상의 기존 디자인을 선택하려면 디자인을 클릭한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

     여러 기준을 선택한 경우 디자인을 한 개만 선택할 수 있습니다.

   * 사용자 지정 디자인을 만들려면 **[!UICONTROL Create Design]**&#x200B;을(를) 클릭한 다음 새 디자인의 이름과 코드를 입력합니다. **[!UICONTROL Next]**&#x200B;을(를) 클릭한 다음 이미지를 선택하거나 업로드하고 **[!UICONTROL Done]** > **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다. 새 디자인 만들기에 대한 내용은 [디자인 만들기](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14)를 참조하십시오.

1. **[!UICONTROL Next]** 아이콘을 클릭합니다.

   권장 사항에 프로모션을 추가할 수 있는 옵션이 있습니다. 전면 및 후면 프로모션 추가에 대한 자세한 내용은 [프로모션 추가](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14)를 참조하십시오.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

   VEC 화면은 페이지에 권장 사항 디자인을 표시합니다.

1. (선택 사항) 활동이 방문자에게 표시되는 방식을 보려면 **[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Preview] 모드에서는 방문자와 마찬가지로 권장 사항과 상호 작용할 수 있습니다.

   권장 사항 미리 보기를 마치면 **[!UICONTROL Compose]**&#x200B;을(를) 클릭합니다.

1. 권장 사항을 VEC에서 검토한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. 흐름 다이어그램에서 [!DNL Recommendations] 활동을 검토하고 필요에 맞게 변경합니다.

   ![권장 사항 흐름 다이어그램](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   흐름 다이어그램은 활동의 대상자를 선택하고, 경험을 설정하고, 성공 지표를 지정하는 단계를 안내합니다.

   흐름 다이어그램에서 다음을 수행할 수 있습니다.

   * 권장 사항을 표시할 대상 변경

     >[!NOTE]
     >
     >기존 대상자를 선택할 수 있을 뿐만 아니라, [활동 전용 대상자를 만들거나](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483), 새 대상자를 만들지 않고 [여러 대상자를 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)하여 임시 대상자를 만들 수도 있습니다.

     기본적으로 모든 사용자는 권장 사항을 볼 수 있습니다. 그러나 권장 사항을 특정 대상으로 타깃팅할 수 있습니다.

     [!DNL Recommendations] 활동의 경우, 통제군에게 권장 사항 없는 페이지가 표시됩니다.

   * 기준 보기
   * 컬렉션 변경([!UICONTROL Criteria] 레이블 옆)
   * 제어 경험이 표시되는 참여자의 비율 변경
   * 디자인 코드 보기
   * 디자인 변경 또는 제거

1. 완료되면 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 활동 설정을 지정합니다.

   예를 들어, 활동에 대한 이름(필수) 및 목표(선택 사항)를 입력합니다. 설정에 대한 자세한 내용은 [권장 사항 활동 설정](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)을 참조하세요.

   >[!NOTE]
   >
   >[!DNL Recommendations Classic]의 다른 활동에 이미 존재하는 [!DNL Recommendation] 활동 이름을 지정하는 경우 새 활동이 새 이름으로 다시 동기화됩니다. 새 이름을 고유하게 만들기 위해 원래 이름에 타임스탬프가 추가됩니다. 이 새 이름은 [!DNL Target Standard/Premium]과 [!DNL Recommendations Classic] 모두에 표시됩니다.

1. 완료되면 **[!UICONTROL Save & Close]**&#x200B;을(를) 클릭합니다.

   활동의 개요가 표시됩니다.

   [!UICONTROL Overview] 페이지에서 다음을 수행할 수 있습니다.

   * 활동 활성화
   * 활동 편집
   * 활동을 Experience Cloud 피드에 공유
   * 활동 QA
   * 경험 URL 보기
   * 데이터 다운로드
   * 제어 경험이 표시되는 활동 참여자의 비율 변경
   * 기준 세부 사항 표시 또는 숨기기
   * 디자인 코드 보기

1. (선택 사항) [!UICONTROL Reports] 페이지를 열어 [!DNL Recommendations] 활동의 성과를 보여 주는 보고서를 확인합니다.

1. (선택 사항) [!UICONTROL Collisions] 페이지를 열어 발생할 수 있는 [활동 충돌](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md)을 확인합니다.

   활동 충돌은 여러 활동이 동일한 페이지로 콘텐츠를 전달하도록 설정되어 있을 때 발생하며, 이로 인해 예상치 못한 콘텐츠가 표시될 수 있습니다.

## 교육 비디오: 권장 사항 활동 만들기(7:15) ![튜토리얼 배지](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/33986?captions=kor)
