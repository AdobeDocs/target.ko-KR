---
keywords: 기준 시퀀스;여러 기준;알고리즘;기준;권장 사항 기준;시퀀스;반환되는 항목 수 제한;슬롯 수준 제어;슬롯
description: 최대 5개의 기준 시퀀스를 설정하여 Recommendations 활동에 표시되는 항목을 보다 세밀하게 제어하는 방법에 대해 알아봅니다.
title: Recommendations에서 기준 시퀀스를 만들려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: c8b0e0414603761b1c67b13d74ffa96d745c99e3
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 18%

---

# 기준 시퀀스 만들기

[!DNL Adobe Target] [!UICONTROL Recommendations] 활동에 나타나는 항목을 더 자세히 제어하려면 최대 5개의 기준 시퀀스를 사용하십시오. 반환되는 항목의 수를 제한할 수도 있습니다(&quot;슬롯 수준 제어&quot;라고도 함).

>[!NOTE]
>
>기준 시퀀스를 2016년 10월 릴리스([!DNL Target Premium]) 이전에 만든 [!UICONTROL Recommendations] 활동과 함께 사용할 수 없습니다.

기준 시퀀스를 만들려면 먼저 시퀀스에 포함할 기준을 만들어야 합니다. 자세한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

기준이 디자인을 채울 수 있는 충분한 결과를 반환하지 않을 경우, 기준 시퀀스를 사용하여 일반적인 백업 권장 사항을 사용하는 대신 추가로 타깃팅된 권장 사항을 제공할 수 있습니다. 일반적으로 기준 시퀀스는 보다 구체적인 타겟팅에서 진행되며, 이는 더 적은 결과를 반환할 수도 있고, 보다 일반적인 타겟팅으로 진행되며, 이는 일반적으로 더 많은 결과를 반환합니다.

기준 시퀀스는 다음 예에 표시된 대로 페이지 유형에 따라 순서대로 달라질 수 있습니다.

| 페이지 유형 | 가능한 시퀀스 순서 |
| --- | --- |
| 제품 페이지 | <ol><li>동일한 브랜드의 현재 항목을 기반으로 함</li><li>모든 브랜드의 현재 항목 기준</li><li>컨텐츠 유사성 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |
| 홈 페이지 | <ol><li>방문자의 마지막 구매 기준 </li><li>방문자의 즐겨찾기 항목 기준</li><li>방문자의 즐겨찾기 카테고리 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |

## 기준 시퀀스 만들기

[!UICONTROL Create Criteria Sequence] 화면에서 기준 시퀀스를 만듭니다.

[!UICONTROL Create Criteria Sequence] 화면에 액세스하는 방법에는 여러 가지가 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** 라이브러리 화면에서 **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**&#x200B;을(를) 클릭합니다. 여기서 만드는 기준은 자동으로 모든 [!UICONTROL Recommendations] 활동에 사용 가능해집니다.
* [!UICONTROL Recommendations] 활동을 만드는 경우 [!UICONTROL Select Criteria] 화면에서 **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**&#x200B;을(를) 클릭합니다. 다른 [!UICONTROL Recommendations] 활동과 함께 사용할 새 기준 시퀀스를 저장하는 옵션이 있습니다.
* [!UICONTROL Recommendations] 활동을 편집하는 경우 페이지에서 [!UICONTROL Recommendations Location] 상자를 클릭한 다음 **[!UICONTROL Change Criteria]**&#x200B;을(를) 선택합니다. [!UICONTROL Select Criteria] 화면에서 **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**&#x200B;을(를) 클릭합니다. 다른 [!UICONTROL Recommendations] 활동과 함께 사용할 새 기준을 저장할 수 있습니다.

다음 단계에서는 첫 번째 메서드를 사용하여 [!UICONTROL Create Criteria Sequence] 화면에 액세스한다고 가정합니다. **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** 라이브러리 화면.

1. **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**&#x200B;을(를) 클릭합니다.

1. [기본 정보](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) 섹션에 정보를 입력하십시오.

1. **[!UICONTROL Criteria Sequence]** 섹션에서 더하기(+) 기호를 클릭하여 하나 이상의 기준 시퀀스를 추가합니다.

   시퀀스 순서는 디자인이 채워지는 순서를 정의합니다. 기준 1에 디자인을 채울 권장 사항이 충분하지 않으면 나머지 슬롯이 기준 2로 채워집니다.

1. [!UICONTROL Select Criteria] 화면에서 조건을 선택한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Search] 상자와 필터 옵션을 사용하여 원하는 기준을 찾을 수 있습니다.

1. (선택 사항) **[!UICONTROL Limit the number of items returned]** 토글을 &quot;켜짐&quot; 위치로 밀고 항목 수(1에서 50 사이)를 지정합니다.

   [!UICONTROL Limit the number of items returned] 옵션(&quot;슬롯 수준 제어&quot;라고도 함)의 값을 이해하는 데 도움이 되도록 다음 사용 사례를 고려하십시오.

   * **사용 사례 1**: 하나의 권장 사항 트레이에 여러 종류의 항목을 혼합하려는 경우 예를 들어, 겉옷(재킷)과 상의(셔츠, 티셔츠)를 혼합하여 표시하려고 합니다. 이를 위해서는 디자인의 모든 슬롯에 원하는 모든 잠재적 제품 유형을 포함하는 활동에 대한 컬렉션을 사용하십시오. 그런 다음 겉옷만 포함하도록 기준을 제한하는 정적 필터를 사용하여 첫 번째 기준을 설정하고, 상단만 포함하도록 기준을 제한하는 정적 필터를 사용하여 두 번째 기준을 설정합니다. 마지막으로 두 기준을 기준 시퀀스에 추가하고 첫 번째 기준을 슬롯 2개로 제한합니다.

     사이트에서는 권장 사항 트레이가 다음과 같을 수 있습니다.

     ![추천 제품 추천 트레이](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **사용 사례 2**: 대체 항목과 보조 항목을 모두 혼합해야 합니다. 조회/조회 알고리즘을 사용하도록 하나의 기준을 설정하고 권장 항목을 현재 항목의 카테고리로 제한하는 동적 필터를 사용합니다. 조회/구매 알고리즘을 사용하도록 두 번째 기준을 설정하고 현재 항목의 카테고리와 일치하지 않는 권장 항목만 포함하는 동적 필터를 사용합니다. 마지막으로 두 기준을 시퀀스에 추가하고 첫 번째 기준을 슬롯 2개로 제한합니다.

1. 시퀀스에 추가 기준을 계속 추가합니다. 시퀀스에 최대 5개의 기준을 추가할 수 있습니다.

1. [백업 콘텐츠 옵션](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)을 사용하도록 설정합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

   기준 시퀀스가 [!UICONTROL Criteria] 목록에 표시됩니다.

   권장 사항 논리 선택 사항에 대한 자세한 내용은 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.