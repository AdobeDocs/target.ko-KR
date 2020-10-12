---
keywords: recommendations;recommendations activity;criteria;algorithm
description: Adobe Target 권장 사항 활동에서 사용할 기준을 선택하십시오.
title: 기준 선택
feature: recs creation
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
translation-type: tm+mt
source-git-commit: 8ae2bf479a9b53693f830515aee55573987bb05b
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 80%

---


# ![PREMIUM](/help/assets/premium.png) 기준 선택{#select-criteria}

Select the [criteria](/help/c-recommendations/c-algorithms/algorithms.md) to use in your [!DNL Adobe Target Recommendations] activity. 기준은 사전 결정된 방문자 행동 세트를 기준으로 추천할 제품을 결정하는 규칙입니다.

두 개 이상의 기준을 추가하여 여러 권장 사항 유형을 서로 비교하면서 테스트할 수 있습니다.

여러 기준을 선택하는 경우 선택한 기준 간에 트래픽이 균일하게 분할됩니다. 예를 들어, 두 개의 기준을 선택했으며 기본 콘텐츠를 활동 참여자의 20%에게 표시하도록 활동이 디자인된 경우 활동 참여자의 40%에게 각 기준에 따른 권장 사항이 표시됩니다. 각 기준의 백분율을 변경하는 옵션은 없습니다.

* 기존 기준을 검색하려면(예를 들어, 많은 기준 카드가 표시되는 경우) 원하는 기준이 나타날 때까지 검색 필드에 입력한 다음, 기준을 선택하고 **[!UICONTROL 완료를 클릭합니다]**.

   일부 기준은 [!DNL Recommendations]에서 제공됩니다. 사용자와 팀이 고유의 사용자 지정 기준을 만들 수도 있습니다.

* To create a new criteria, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**, then fill in the information for the new criteria. 새 기준 만들기에 대한 내용은 [새 기준 만들기](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)를 참조하십시오.

**기준을 선택하려면 다음을 수행하십시오.**

1. While [creating a new recommendation](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F), in the **[!UICONTROL Select Criteria]** dialog box, locate and select one or more criteria.

   ![기준 선택 대화 상자](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   [!UICONTROL 업계 유형] 필터, [!UICONTROL 페이지 유형] 필터 및 [!UICONTROL 호환] 확인란을 사용하여 기준 목록을 필터링할 수 있습니다. 이러한 옵션은 원하는 기준을 찾는 데 도움이 됩니다.

   * **업계 유형:** 업계 유형은 [!DNL Recommendations] 기준을 분류하는 데 사용됩니다. To change your default industry vertical, click **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** and select your desired default **[!UICONTROL Industry Vertical]** setting.
   * **페이지 유형:**&#x200B;페이지 유형은 권장 사항을 분류하는 데 도움이 됩니다. 각 페이지 유형에 대해 선택할 수 있는 내장 기준도 있습니다.
   * **호환:**&#x200B;선택한 페이지가 필수 데이터를 제공하는 기준만 표시합니다. 모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 `entity.categoryId`를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 활동에 대해 호환되지 않는 기준을 사용할 수 있도록 하려면 **[!UICONTROL 호환]** 선택란을 선택 취소하십시오. This option can be disabled or enabled in your settings: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 [디자인 선택](/help/c-recommendations/c-design-overview/design-overview.md) 대화 상자를 표시합니다.
