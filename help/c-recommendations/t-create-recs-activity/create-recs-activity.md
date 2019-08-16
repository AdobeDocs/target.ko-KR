---
description: Target을 사용할 수 있는 페이지에서 바로 권장 사항 활동을 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target 시각적 경험 작성기(VEC)를 사용하십시오.
keywords: 권장 사항 만들기;권장 사항 활동;새 권장 사항;권장 사항 개요
seo-description: Target을 사용할 수 있는 페이지에서 바로 권장 사항 활동을 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target 시각적 경험 작성기(VEC)를 사용하십시오.
seo-title: 권장 사항 활동 만들기
solution: Target
title: 권장 사항 활동 만들기
title-outputclass: premium
topic: Premium
uuid: c3f22cce-204a-4509-92c4-8fec43fbaebe
badge: premium
translation-type: tm+mt
source-git-commit: 0466b6d5cf6804ec3a26716a9ade35fe5678bcb6

---


# ![PREMIUM](/help/assets/premium.png) 권장 사항 활동 만들기{#create-a-recommendations-activity}

Target을 사용할 수 있는 페이지에서 바로 권장 사항 활동을 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target 시각적 경험 작성기(VEC)를 사용하십시오.

1. **[!UICONTROL 활동 만들기]** &gt; **[!UICONTROL 권장 사항]**&#x200B;을 클릭합니다.

   ![Recommendations 활동 만들기](/help/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. 필요한 경우 **[!UICONTROL 시각적 (기본값)]**&#x200B;를 선택합니다.

   ![권장 사항 활동 만들기 대화 상자](/help/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   양식 기반 경험 작성기를 사용하려면 [!UICONTROL 양식을 선택합니다]. See [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >Target는 VEC 및 양식 기반 Experience Composer 외에도 단일 페이지 애플리케이션 VEC와 모바일 앱용 VEC를 제공합니다. 다양한 컴포저에 대한 자세한 내용은 [경험과 오퍼를 참조하십시오.](/help/c-experiences/experiences.md)
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >the [! 이전 [일러스트레이션에서 Uicontrol 선택 작업 영역](/help/administrating-target/c-user-management/property-channel/property-channel.md) 옵션은 [Target Premium](/help/c-intro/intro.md) 기능입니다. 이 옵션이 표시되지 않는 경우 조직에 Target Standard 라이선스가 있습니다.]

1. (조건부) Target Premium [고객인](/help/c-intro/intro.md#premium)경우 [작업 영역을 선택합니다](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. 활동 URL을 지정하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `http://www.adobe.com`]과 [!DNL `https://wwww.adobe.com`]은 모두 같습니다.

   활동 URL은 권장 사항이 표시될 페이지입니다.

   [!UICONTROL 다음]을 클릭하면 VEC가 열리고 페이지가 표시됩니다. 현재 요소를 권장 사항으로 바꾸거나 권장 사항을 삽입할 수 있습니다.

1. Click an element on your page, then if recommendations are available where that element is located, click **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]**, or **[!UICONTROL Insert Recommendations After]**.

   ![Recommendations 옵션](/help/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   요소를 권장 사항으로 바꾸면 현재 컨텐츠가 삭제되고 권장 사항으로 바뀝니다.

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
   ![페이지 유형 선택 옵션](/help/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Select one or more [criteria](/help/c-recommendations/c-algorithms/algorithms.md).

   기준은 각 기준에 대한 정보를 표시하는 카드로 표시됩니다. 기본적으로 [!UICONTROL 기준 선택] 화면에 사용자의 수직 시장과 호환되는 기준과 선택한 페이지 유형이 표시됩니다. 이러한 옵션을 변경하여 다른 기준을 표시할 수 있습니다.

   >[!NOTE]
   >
   >모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 `entity.categoryId`를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 활동에 대해 호환되지 않는 기준을 사용할 수 있도록 하려면 **[!UICONTROL 호환]선택란을 선택 취소하십시오.** [!UICONTROL 호환] 선택 사항은 권장 사항 설정(**[!UICONTROL 권장 사항]** &gt; **[!UICONTROL 설정]** &gt; **[!UICONTROL 호환되지 않는 기준 필터링]**)에 따라 표시되지 않을 수 있습니다. 자세한 내용은 [설정](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)을 참조하십시오.

   ![기준 선택 대화 상자](/help/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   여러 기준을 선택하는 경우 선택한 기준 간에 트래픽이 균일하게 분할됩니다. 예를 들어, 두 개의 기준을 선택했으며 기본 컨텐츠를 활동 참여자의 20%에게 표시하도록 활동이 디자인된 경우 활동 참여자의 40%에게 각 기준에 따른 권장 사항이 표시됩니다. 각 기준의 백분율을 변경하는 옵션은 없습니다.

   * To search for an existing criteria (for example, if a large number of criteria cards are displayed), type in the search field until the desired criteria appears, then select the criteria and click **[!UICONTROL Next]**.

      일부 기준은 [!DNL Recommendations]에서 제공됩니다. 사용자와 팀이 고유의 사용자 지정 기준을 만들 수도 있습니다.

   * To create a new criteria, click **[!UICONTROL Create Criteria]** &gt; **[!UICONTROL Create Criteria]**, then fill in the information for the new criteria. 새 기준 만들기에 대한 내용은 [기준 만들기](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)를 참조하십시오.
   * 기준을 시퀀스로 그룹화할 수도 있습니다. To create a new criteria sequence, click **[!UICONTROL Create Criteria]** &gt; **[!UICONTROL Create Criteria Sequence]**. 자세한 내용은 [기준 시퀀스 만들기](../../c-recommendations/c-algorithms/create-criteria-sequence.md#task_8A9CB465F28D44899F69F38AD27352FE)를 참조하십시오.

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. [디자인을](/help/c-recommendations/c-design-overview/design-overview.md)선택합니다.

   디자인은 페이지에서 위치의 모양을 결정하는 템플릿입니다. [!DNL Target]에는 사전 구성된 디자인이 포함되어 있습니다. 사용자 고유의 사용자 지정 디자인을 만들 수도 있습니다. 자세한 내용은 [디자인 만들기](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) 및 [디자인 사용자 지정](../../c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59)을 참조하십시오.

   ![디자인 대화 상자 선택](/help/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   각 디자인은 어떤 모양으로 표시될지 보여 주는 그래픽 표현과 현재 해당 디자인을 사용하는 라이브 및 비활성 활동의 수를 보여 주는 아이콘을 표시합니다.

   * To select one or more existing designs, click the designs, then click **[!UICONTROL Next]**.

      여러 기준을 선택한 경우 하나의 디자인을 선택할 수 있습니다.

   * To create a custom design, click **[!UICONTROL Create Design]**, then fill in the name and code for the new design. **[!UICONTROL 다음]**&#x200B;을 클릭한 후 이미지를 선택하거나 업로드하고 **[!UICONTROL 완료]** &gt; **[!UICONTROL 완료]** 를 클릭합니다. 새 디자인 만들기에 대한 내용은 [디자인 만들기](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14)를 참조하십시오.

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   권장 사항에 프로모션을 추가할 수 있는 옵션이 있습니다. 전면 및 후속 프로모션을 추가하는 방법에 대한 자세한 내용은 [프로모션 추가](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).
1. **[!UICONTROL 저장을 클릭합니다]**.

   VEC 화면은 페이지에 권장 사항 디자인을 표시합니다.

1. (선택 사항) **[!UICONTROL 미리 보기]**&#x200B;를 클릭하여 활동이 방문자에게 표시되는 방식을 확인합니다.

   [!UICONTROL 기회비용 보기] 모드에서는 방문자와 마찬가지로 권장 사항과 상호 작용할 수 있습니다.

   권장 사항 기회비용 보기를 마치면 **[!UICONTROL 작성을 클릭합니다]**.

1. 권장 사항을 VEC에서 검토한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. 흐름 다이어그램에서 [!DNL Recommendations] 활동을 검토하고 필요에 맞게 변경합니다.

   ![Recommendations 흐름 다이어그램](/help/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   흐름 다이어그램은 활동의 대상을 선택하고, 경험을 설정하고, 성공 지표를 지정하는 단계를 안내합니다.

   흐름 다이어그램에서 다음을 수행할 수 있습니다.

   * 권장 사항을 표시할 대상 변경

      >[!NOTE]
      >
      >기존 대상을 선택할 수 있을 뿐만 아니라, [활동 전용 대상을 만들거나](../../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483), 새 대상을 만들지 않고 [여러 대상을 결합](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)하여 임시 대상을 만들 수도 있습니다.

      기본적으로 모든 사용자는 권장 사항을 볼 수 있습니다. 그러나 권장 사항을 특정 대상으로 타깃팅할 수 있습니다.

      [!DNL Recommendations] 활동의 경우, 통제군에게 권장 사항 없는 페이지가 표시됩니다.

   * 기준 보기
   * 컬렉션 변경([!UICONTROL 기준] 레이블 옆에 표시)
   * 제어 경험이 표시되는 참여자의 비율 변경
   * 디자인 코드 보기
   * 디자인 변경 또는 제거

1. 완료되면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. 활동 설정을 지정합니다.

   예를 들어, 활동에 대한 이름(필수) 및 목표(선택 사항)를 입력합니다. 설정에 대한 내용은 [권장 사항 활동 설정](../../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >[!DNL Recommendations Classic]의 다른 활동에 이미 존재하는 [!DNL Recommendation] 활동 이름을 지정하는 경우 새 활동이 새 이름으로 다시 동기화됩니다. 새 이름을 고유하게 만들기 위해 원래 이름에 타임스탬프가 추가됩니다. 이 새 이름은 [!DNL Target Standard/Premium]과 [!DNL Recommendations Classic] 모두에 표시됩니다.

1. When finished, click **[!UICONTROL Save &amp; Close]**.

   활동의 개요가 표시됩니다.

   [!UICONTROL 개요] 페이지에서 다음을 수행할 수 있습니다.

   * 활동 활성화
   * 활동 편집
   * Experience Cloud 보드에 활동 고정
   * 경험 URL 보기
   * 데이터 다운로드
   * 제어 경험이 표시되는 활동 참여자의 비율 변경
   * 기준 세부 사항 표시 또는 숨기기
   * 디자인 코드 보기

1. (선택 사항) [!UICONTROL 보고서] 페이지를 열어 [!DNL Recommendations] 활동의 성과를 보여 주는 보고서를 확인합니다.
1. (선택 사항) [!UICONTROL 충돌] 페이지를 열어 발생할 수 있는 [활동 충돌](https://marketing.adobe.com/resources/help/en_US/target/target/c_activity_collisions.html)을 봅니다.

   활동 충돌은 여러 활동이 동일한 페이지로 컨텐츠를 전달하도록 설정되어 있을 때 발생하며, 이로 인해 예상치 못한 컨텐츠가 표시될 수 있습니다.

## 교육 비디오: 권장 사항 활동 만들기 (7:15)

>[!VIDEO](https://video.tv.adobe.com/v/27688?captions=kor)