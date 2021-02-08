---
keywords: 추천;추천 활동;기준;알고리즘
description: Adobe Target Recommendations 활동에서 사용할 기준(추천할 제품 또는 컨텐츠를 결정하는 규칙)을 선택하는 방법에 대해 알아보십시오.
title: Recommendations 활동의 기준을 어떻게 선택합니까?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 72%

---


# ![PREMIUM](/help/assets/premium.png) 기준 선택{#select-criteria}

[!DNL Adobe Target Recommendations] 활동에 사용할 [기준](/help/c-recommendations/c-algorithms/algorithms.md)을 선택합니다. 기준은 사전 결정된 방문자 행동 세트를 기준으로 추천할 제품을 결정하는 규칙입니다.

두 개 이상의 기준을 추가하여 여러 권장 사항 유형을 서로 비교하면서 테스트할 수 있습니다.

여러 기준을 선택하는 경우 선택한 기준 간에 트래픽이 균일하게 분할됩니다. 예를 들어, 두 개의 기준을 선택했으며 기본 콘텐츠를 활동 참여자의 20%에게 표시하도록 활동이 디자인된 경우 활동 참여자의 40%에게 각 기준에 따른 권장 사항이 표시됩니다. 각 기준의 백분율을 변경하는 옵션은 없습니다.

* 기존 기준을 검색하려면(예를 들어, 많은 기준 카드가 표시되는 경우) 원하는 기준이 나타날 때까지 검색 필드에 입력한 다음, 기준을 선택하고 **[!UICONTROL 완료를 클릭합니다]**.

   일부 기준은 [!DNL Recommendations]에서 제공됩니다. 사용자와 팀이 고유의 사용자 지정 기준을 만들 수도 있습니다.

* 새 기준을 만들려면 **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 만들기]**&#x200B;를 클릭한 다음 새 기준에 대한 정보를 입력합니다. 새 기준 만들기에 대한 내용은 [새 기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)를 참조하십시오.

**기준을 선택하려면 다음을 수행하십시오.**

1. [새 권장 사항](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)을 만드는 동안 **[!UICONTROL 기준 선택]** 대화 상자에서 하나 이상의 기준을 찾아 선택합니다.

   ![기준 선택 대화 상자](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   [!UICONTROL 업계 유형] 필터, [!UICONTROL 페이지 유형] 필터 및 [!UICONTROL 호환] 확인란을 사용하여 기준 목록을 필터링할 수 있습니다. 이러한 옵션은 원하는 기준을 찾는 데 도움이 됩니다.

   * **업계 유형:** 업계 유형은 [!DNL Recommendations] 기준을 분류하는 데 사용됩니다. 기본 업계 수직 설정을 변경하려면 **[!UICONTROL Recommendations]** > **[!UICONTROL 설정]**&#x200B;을 클릭하고 원하는 기본 **[!UICONTROL 업계 수직]** 설정을 선택합니다.
   * **페이지 유형:**&#x200B;페이지 유형은 권장 사항을 분류하는 데 도움이 됩니다. 각 페이지 유형에 대해 선택할 수 있는 내장 기준도 있습니다.
   * **호환:**&#x200B;선택한 페이지가 필수 데이터를 제공하는 기준만 표시합니다. 모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 `entity.categoryId`를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 활동에 대해 호환되지 않는 기준을 사용할 수 있도록 하려면 **[!UICONTROL 호환]** 선택란을 선택 취소하십시오. 이 옵션은 설정을 비활성화하거나 활성화할 수 있습니다.**[!UICONTROL Recommendations]** > **[!UICONTROL 설정]**.

1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 [디자인 선택](/help/c-recommendations/c-design-overview/design-overview.md) 대화 상자를 표시합니다.
