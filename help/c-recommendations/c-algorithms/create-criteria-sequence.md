---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned
description: 최대 5개의 기준의 시퀀스를 사용하여 Adobe Target Recommendations 활동에 표시되는 항목을 보다 정확하게 제어할 수 있습니다.
title: 기준 시퀀스 만들기
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 36%

---


# ![PREMIUM](/help/assets/premium.png) 기준 시퀀스 만들기

[!UICONTROL 권장 사항] 활동에 나타나는 항목을 더 잘 제어하려면 기준이 최대 5개인 시퀀스를 사용하십시오.

>[!NOTE]
>
>기준 시퀀스를 2016년 10월 릴리스 이전에 만든 [!UICONTROL 권장 사항] 활동에는 사용할 수 없습니다[!DNL Target Premium].

기준 시퀀스를 만들려면 먼저 시퀀스에 포함할 기준을 만들어야 합니다. 각 유형의 대상 규칙을 구성하는 방법에 대한 자세한 내용은 [자세한 내용은 기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

기준이 디자인을 채울 수 있는 충분한 결과를 반환하지 않을 경우, 기준 시퀀스를 사용하여 일반적인 백업 권장 사항을 사용하는 대신 추가로 타깃팅된 권장 사항을 제공할 수 있습니다. 일반적으로 기준 시퀀스는 더 적은 결과를 반환하는 보다 구체적인 타깃팅에서 더 일반적인 타깃팅으로 진행되므로 더 많은 결과를 반환합니다.

다음 예에서 보듯이 기준 시퀀스는 페이지 유형에 따라 달라질 수 있습니다.

| 페이지 유형 | 가능한 시퀀스 순서 |
| --- | --- |
| 제품 페이지 | <ol><li>동일한 브랜드의 현재 항목 기준</li><li>모든 브랜드의 현재 항목 기준</li><li>컨텐츠 유사성 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |
| 홈 페이지 | <ol><li>방문자의 마지막 구매 기준 </li><li>방문자의 즐겨찾기 항목 기준</li><li>방문자의 즐겨찾기 카테고리 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |

## 기준 시퀀스 만들기

기준 시퀀스 생성 화면에서 기준 [!UICONTROL 시퀀스를] 생성합니다.

[!UICONTROL 기준 시퀀스 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* **[!UICONTROL 권장 사항]** > **[!UICONTROL 기준]** 라이브러리 화면에서 **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**&#x200B;를 클릭합니다. 여기서 만드는 기준은 자동으로 모든 [!UICONTROL 권장 사항] 활동에 사용 가능해집니다.
* [!UICONTROL Recommendations] 활동을 생성하는 경우 기준 선택 화면에서 새로 만들기 **[!UICONTROL 만들기]** > 기준 시퀀스 **[!UICONTROL 만들기를 클릭합니다]**. 다른 [!UICONTROL 권장 사항] 활동과 함께 사용할 새 기준 시퀀스를 저장하는 옵션이 있습니다.
* [!UICONTROL Recommendations] 활동을 편집할 때 페이지의 [!UICONTROL Recommendations 위치] 상자를 클릭한 다음 기준 **[!UICONTROL 변경을 선택합니다]**. [!UICONTROL 기준 선택] 화면에서 **[!UICONTROL 새로 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**&#x200B;를 클릭합니다. 다른 [!UICONTROL 권장 사항] 활동과 함께 사용할 새 기준을 저장하는 옵션이 있습니다.

다음 단계에서는 첫 번째 방법을 사용하여 기준 시퀀스 [!UICONTROL 생성] 화면에 액세스한다고 가정합니다.[ **[!UICONTROL Recommendations]** ] > [ **[!UICONTROL 기준]** 라이브러리] 화면

1. Recommendations **[!UICONTROL >]** 기준을 클릭합니다 ****.

1. 기준 **[!UICONTROL 만들기]** > 기준 **[!UICONTROL 시퀀스 만들기를 클릭합니다]**.

   ![](assets/CreateCriteriaSequence.png)

1. Fill in the information in the [Basic Information](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. 기준 **[!UICONTROL 시퀀스]** 섹션에서 기준 **[!UICONTROL 추가를 클릭합니다]**.

   시퀀스 순서는 디자인이 채워지는 순서를 정의합니다. 기준 1에 디자인을 채울 권장 사항이 충분하지 않으면 나머지 슬롯은 기준 2로 채워집니다.

   ![기준 추가](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. 기준 [!UICONTROL 선택] 화면에서 기준을 선택한 다음 **[!UICONTROL 추가를 클릭합니다]**.

   검색 상자 및 필터 드롭다운을 사용하여 원하는 기준을 찾을 수 있습니다.

   ![기준 선택](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (선택 사항) &quot; **[!UICONTROL 켜짐&quot; 위치로 전환된]** 항목의 수를 제한하고 항목 수(1과 50 사이)를 지정합니다.

   ![반환된 항목 수 제한](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   반환되는 항목 수 제한 [!UICONTROL 옵션의 값을] 이해하는 데 도움이 되도록 다음 사용 사례를 고려하십시오.

   * **사용 사례 1**:단일 권장 사항 트레이에 여러 종류의 항목을 혼합하려는 경우 예를 들어, 겉옷(자켓)과 윗옷(셔츠, 티셔츠)을 혼합하여 표시하려고 합니다. 이를 위해서는 컬렉션의 디자인 슬롯에서 원하는 모든 잠재적 제품 유형을 포함하는 활동을 이용하십시오. 그런 다음 기준을 제한하는 정적 필터로 첫 번째 기준을 설정하고 기준을 가장 바깥옷만 포함하도록 제한하는 정적 필터로 두 번째 기준을 설정합니다. 마지막으로 기준 시퀀스에 두 기준을 추가하고 첫 번째 기준을 2개의 슬롯으로 제한합니다.

      권장 사항 트레이는 사이트에서 다음과 같이 표시될 수 있습니다.

      ![주요 제품 추천 트레이](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **사용 사례 2**:대체 항목과 보조 항목을 모두 혼합해야 합니다. 조회한/본 알고리즘을 사용하고 권장 항목을 현재 항목 카테고리로 제한하는 동적 필터를 사용하도록 한 기준을 설정합니다. 두 번째 기준을 설정하여 보고/구입한 알고리즘을 사용하고 현재 항목의 카테고리와 일치하지 않는 권장 항목만 포함하는 동적 필터를 사용하십시오. 마지막으로 두 기준을 모두 시퀀스에 추가하고 첫 번째 기준을 2개의 슬롯으로 제한합니다.

1. 시퀀스에 기준을 계속 추가합니다. 시퀀스에 최대 5개의 기준을 추가할 수 있습니다.

1. 백업 [컨텐츠 옵션을 활성화합니다](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   기준 시퀀스가 기준 목록에 나타납니다.

   권장 사항 논리 선택 사항에 대한 자세한 내용은 [기준](/help/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

## 교육 비디오: 추천에서 기준 만들기(12:33) ![자습서 배지](/help/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
