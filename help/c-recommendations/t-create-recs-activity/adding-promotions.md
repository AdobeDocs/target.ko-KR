---
keywords: 홍보;전진 프로모션;전진 프로모션 유형;항목 목록;속성별 홍보;컬렉션 홍보
description: Adobe [!DNL Target] Recommendations 디자인에서 홍보된 항목을 추가하고 해당 항목의 배치를 제어하는 방법에 대해 알아보십시오. 정적 및 동적 프로모션을 추가할 수 있습니다.
title: Recommendations 디자인에 프로모션을 추가하려면 어떻게 해야 합니까?
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 56%

---

# ![PREMIUM](/help/assets/premium.png) 프로모션 추가

프로모션된 항목을 추가하고 Adobe Target 권장 사항 디자인에서 해당 배치를 제어합니다. 정적 및 동적 프로모션을 추가할 수 있습니다.

>[!IMPORTANT]
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

[!DNL Recommendations] 활동을 만들 때 [!DNL Recommendations] 디자인에 판촉된 항목을 포함할 수 있는 선택 사항이 있습니다. 프로모션은 디자인에서 사용 가능한 슬롯을 사용하며, 기준 결과 및 백업 권장 사항보다 우선합니다. 예를 들어, 디자인에 6개의 슬롯이 있고 이 중 2개를 프로모션으로 사용하는 경우 4개의 슬롯은 기준에 따라 권장되는 항목에 대해 사용할 수 있습니다.

프로모션은 활동 기준에서 권장하는 항목에 대해 중복 제거되므로, 제공된 항목이 단일 권장 사항 트레이에 두 번 표시되지 않습니다.

특정 항목을 판촉하거나, 항목을 동적으로 판촉하거나, 속성을 기준으로 항목을 판촉하거나, 컬렉션을 판촉할 수 있습니다.

![](assets/add_promotion_toggles.png)

>[!NOTE]
>
>프로모션을 사용하면 CSV 구조 및 출력이 변경됩니다. 이러한 변경 사항은 CSV를 포함하는 외부 프로세스(예: 이메일)에 영향을 줄 수 있습니다.

1. **[!UICONTROL 옵션]** 페이지에서 **[!UICONTROL 전면 프로모션]** 또는 **[!UICONTROL 후면 프로모션]** 전환을 클릭합니다.

   다음 그림은 [!UICONTROL 전면 프로모션] 전환이 &quot;켜짐&quot; 위치에 있음을 보여줍니다.

   ![전면 프로모션 옵션 추가](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   기준 결과 이전 *및* 이후에 프로모션을 삽입할 수 있습니다.
1. 판촉된 항목에 사용할 디자인 슬롯 수를 설정합니다.

   [!DNL Recommendations] 디자인에 따라 최대 20개의 슬롯을 사용할 수 있습니다. 사용하는 각 슬롯은 기준에 따라 반환되는 권장 사항에는 사용할 수 없게 됩니다.

1. 판촉된 항목의 시작 날짜 및 종료 날짜를 설정합니다.

   시작 날짜를 설정하지 않으면 프로모션이 즉시 시작됩니다. 종료 날짜를 설정하지 않으면 프로모션이 무기한 실행됩니다.

1. **[!UICONTROL 프로모션 유형]**&#x200B;을 선택합니다.

   * **[!UICONTROL 항목 목록]**&#x200B;을 선택하고, 판촉할 특정 항목의 `entity.id` 값을 쉼표로 구분해서 입력합니다.

   * **[!UICONTROL 속성별 판촉]**&#x200B;을 선택하고 규칙을 추가하여 판촉할 항목의 속성을 정의합니다.

      속성별 판촉을 선택하는 경우 다이내믹 일치를 만들 수 있습니다. 자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

   * **[!UICONTROL 컬렉션 판촉]**&#x200B;을 선택하고 판촉할 항목의 컬렉션을 선택합니다.

      프로모션에 사용할 새 컬렉션을 만들 수 있습니다. 자세한 내용은 [컬렉션 만들기](/help/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08)를 참조하십시오.
   **[!UICONTROL 항목 목록]**&#x200B;을 **[!UICONTROL 판촉 유형]**&#x200B;으로 선택한 경우 원하는 경우 **[!UICONTROL 항목 주문 무작위 지정]** 확인란을 선택할 수 있습니다.

   [!UICONTROL 항목 목록]에 대한 기본 정렬 순서는 Target UI 또는 API에서 입력한 순서를 기반으로 합니다. 목록에 프로모션을 위해 설정한 슬롯 수보다 많은 항목이 포함되어 있는 경우 [!UICONTROL 항목 순서 무작위 지정] 옵션은 디자인에 표시되는 승격된 항목을 임의화합니다. 이 옵션을 선택하면 각 히트에 대해 설정된 전체 판촉 설정에서 템플릿의 판촉 행사에 대해 활성화된 항목을 임의로 선택합니다.[!DNL Target]

   엔티티에 `entity.value` 특성이 없는 경우(예: 제품을 판매하지 않는 경우) 게시 날짜와 같은 숫자 값을 `entity.value` 속성에 전달할 수 있습니다. 이 경우 가장 최근 게시 날짜를 기준으로 승격된 항목을 내림차순으로 승격할 수 있습니다. `entity.value` 특성은 double; 형식입니다.문자열을 허용하지 않습니다.

   **[!UICONTROL 특성]** 또는 **[!UICONTROL 컬렉션 홍보]** 옵션을 선택한 경우 순서를 무작위 지정하는 옵션을 적용할 수 없습니다.

   [!UICONTROL 특성] 또는 [!UICONTROL 컬렉션 홍보] 옵션을 사용하여 특정 항목을 홍보할 때 항목이 표시되는 기본 순서는 내림차순으로 `entity.value` 특성을 기준으로 합니다.

   다음 표는 이러한 옵션 간의 차이점을 보여 줍니다.

   | 프로모션 유형 | 기본 정렬 | 백업 정렬 | 동적 필터링 옵션 |
   | --- | --- | --- | --- |
   | 항목 목록 | Target UI/API에 입력한 순서 | 임의(UI/API를 통해 선택한 경우) | 아니오 |
   | 속성별 홍보 | `entity.value` (내림차순) | 각 요청에 대해 무작위 지정(`entity.value` 특성이 없을 경우) | 예 |
   | 컬렉션 홍보 | `entity.value` (내림차순) | 각 요청에 대해 무작위 지정(`entity.value` 특성이 없을 경우) | 아니오 |

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

활동의 모든 경험에 프로모션이 적용됩니다.
