---
description: 권장 사항 활동에서 사용할 기준을 선택하십시오.
keywords: 권장 사항;권장 사항 활동;기준
seo-description: 권장 사항 활동에서 사용할 기준을 선택하십시오.
seo-title: 기준 선택
solution: Target
title: 기준 선택
title-outputclass: premium
topic: Premium
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) 기준 선택{#select-criteria}

권장 사항 활동에서 사용할 기준을 선택하십시오.

두 개 이상의 기준을 추가하여 여러 권장 사항 유형을 서로 비교하면서 테스트할 수 있습니다.

여러 기준을 선택하는 경우 선택한 기준 간에 트래픽이 균일하게 분할됩니다. 예를 들어, 두 개의 기준을 선택했으며 기본 컨텐츠를 활동 참여자의 20%에게 표시하도록 활동이 디자인된 경우 활동 참여자의 40%에게 각 기준에 따른 권장 사항이 표시됩니다. 각 기준의 백분율을 변경하는 옵션은 없습니다.

* 기존 기준을 검색하려면(예를 들어, 많은 기준 카드가 표시되는 경우) 원하는 기준이 나타날 때까지 검색 필드에 입력한 다음, 기준을 선택하고 **[!UICONTROL 완료를 클릭합니다]**.

   일부 기준은 [!DNL Recommendations]에서 제공됩니다. 사용자와 팀이 고유의 사용자 지정 기준을 만들 수도 있습니다.

* 새 기준을 만들려면 **[!UICONTROL 새로 만들기]**를 클릭하고 새 기준에 대한 정보를 채우십시오. 새 기준 만들기에 대한 내용은 [새 기준 만들기](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)를 참조하십시오.

1. [새 추천을 만들거나](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) 설정하고자 하는 기준에 해당하는 추천을 찾은 후 **[!UICONTROL 편집]**을 클릭합니다.
1. 산업 유형 및 페이지 유형을 선택합니다.

* **업계 유형:** 업계 유형은 기준을 분류하는 [!DNL Recommendations] 데 사용됩니다. 기본 수직 시장을 변경하려면 **[!UICONTROL 설정]**을 클릭하고 원하는 기본 **수직 시장]설정을 선택합니다.[!UICONTROL **
* **페이지 유형:**페이지 유형은 권장 사항을 분류하는 데 도움이 됩니다. 각 페이지 유형에 대해 선택할 수 있는 내장 기준도 있습니다.
* **호환:**선택한 페이지가 필수 데이터를 제공하는 기준만 표시합니다. 모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 [!DNL entity.categoryId]를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 활동에 대해 호환되지 않는 기준을 사용할 수 있도록 하려면 **[!UICONTROL 호환]선택란을 선택 취소하십시오.** 이 옵션은 [!DNL Target][!UICONTROL  기본 설정]에서 비활성화하거나 활성화할 수 있습니다.

1. **[!UICONTROL 추가를 클릭합니다]**.
