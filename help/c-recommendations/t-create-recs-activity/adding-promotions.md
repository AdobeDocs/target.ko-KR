---
keywords: 프로모션;전면 프로모션;후속 프로모션;프로모션 유형;항목 목록;속성별 판촉;컬렉션 판촉
description: 프로모션된 항목을 추가하고 Adobe에서 해당 배치를 제어하는 방법을 알아봅니다 [!DNL Target] Recommendations 디자인. 정적 및 동적 프로모션을 추가할 수 있습니다.
title: Recommendations 디자인에 프로모션을 추가하려면 어떻게 해야 합니까?
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 0d8d04091968923c7d343692140279c026d579f4
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 49%

---

# ![PREMIUM](/help/assets/premium.png) 프로모션 추가

프로모션된 항목을 추가하고 위치에서 해당 배치를 제어합니다 [!DNL Adobe Target Recommendations] 디자인. 정적 및 동적 프로모션을 추가할 수 있습니다.

>[!IMPORTANT]
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오는 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

[!DNL Recommendations] 활동을 만들 때 [!DNL Recommendations] 디자인에 판촉된 항목을 포함할 수 있는 선택 사항이 있습니다. 프로모션은 디자인에서 사용 가능한 슬롯을 사용하며, 기준 결과 및 백업 권장 사항보다 우선합니다. 예를 들어, 디자인에 6개의 슬롯이 있고 이 중 2개를 프로모션으로 사용하는 경우 4개의 슬롯은 기준에 따라 권장되는 항목에 대해 사용할 수 있습니다.

프로모션은 활동 기준에서 권장하는 항목에 대해 중복 제거되므로, 제공된 항목이 단일 권장 사항 트레이에 두 번 표시되지 않습니다.

특정 항목을 판촉하거나, 항목을 동적으로 판촉하거나, 속성을 기준으로 항목을 판촉하거나, 컬렉션을 판촉할 수 있습니다.

![[!UICONTROL 전면 프로모션] 및 [!UICONTROL 후속 프로모션] 옵션 [!DNL Target] UI](assets/add_promotion_toggles.png)

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

      선택하는 경우 [!UICONTROL 속성별 홍보]를 사용하여 동적 일치를 만들 수 있습니다. 자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * **[!UICONTROL 컬렉션 판촉]**&#x200B;을 선택하고 판촉할 항목의 컬렉션을 선택합니다.

      프로모션에 사용할 새 컬렉션을 만들 수 있습니다. 자세한 내용은 [컬렉션 만들기](/help/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) 추가 정보.
   선택한 경우 **[!UICONTROL 항목 목록]** 로서의 **[!UICONTROL 프로모션 유형]**&#x200B;를 클릭하고, **[!UICONTROL 항목 순서 무작위 지정]** 원하는 경우 확인란을 선택합니다.

   에 대한 기본 정렬 순서 [!UICONTROL 항목 목록] 은 [!DNL Target] UI 또는 API. 목록에 프로모션용으로 설정한 슬롯 수보다 많은 항목이 포함된 경우 [!UICONTROL 항목 순서 무작위 지정] 선택 사항은 디자인에 표시되는 판촉된 항목을 임의로 지정합니다. 이 옵션을 선택하면 [!DNL Target] 각 히트에 설정된 전체 프로모션 중에서 템플릿의 프로모션에 대해 활성화된 항목을 임의로 선택합니다.

   엔티티에 `entity.value` 속성(예: 제품을 판매하지 않음)에서에 숫자 값을 전달할 수 있습니다. `entity.value` 게시 날짜와 같은 속성입니다. 이 경우 승격된 항목은 가장 최근 게시 날짜를 기준으로 내림차순으로 승격할 수 있습니다. 다음 `entity.value` 특성이 double 형식입니다. 문자열을 허용하지 않습니다.

   을(를) 선택한 경우 **[!UICONTROL 속성별 홍보]** 또는 **[!UICONTROL 컬렉션 홍보]** 옵션을 선택하면 순서를 무작위 지정하는 옵션을 적용할 수 없습니다.

   을 사용하여 특정 항목을 프로모션하는 경우 [!UICONTROL 속성별 홍보] 또는 [!UICONTROL 컬렉션 홍보] 옵션, 항목이 표시되는 기본 순서는 `entity.value` 속성을 내림차순으로 표시합니다.

   다음 표에서는 이 옵션의 차이점을 설명합니다.

   | 프로모션 유형 | 기본 정렬 | 백업 정렬 | 동적 필터링 옵션 |
   | --- | --- | --- | --- |
   | [!UICONTROL 항목 목록] | Target UI/API에 입력된 순서 | 임의(UI/API를 통해 선택한 경우) | 아니오 |
   | [!UICONTROL 속성별 홍보] | `entity.value` (내림차순 순서) | 임의 지정 안 함 | 예 |
   | [!UICONTROL 컬렉션 홍보] | `entity.value` (내림차순 순서) | 임의 지정 안 함 | 아니오 |

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

활동의 모든 경험에 프로모션이 적용됩니다.
