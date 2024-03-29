---
keywords: 기준 시퀀스;여러 기준;알고리즘;기준;권장 사항 기준;시퀀스;반환되는 항목 수 제한;슬롯 수준 제어;슬롯
description: Adobe에 표시되는 항목을 보다 세밀하게 제어할 수 있도록 최대 5개의 기준 시퀀스를 설정하는 방법을 알아봅니다 [!DNL Target] Recommendations 활동.
title: Recommendations에서 기준 시퀀스를 만들려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 34%

---

# 기준 시퀀스 만들기

[!UICONTROL 권장 사항] 활동에 나타나는 항목을 더 잘 제어하려면 기준이 최대 5개인 시퀀스를 사용하십시오. 반환되는 항목의 수를 제한할 수도 있습니다(&quot;슬롯 수준 제어&quot;라고도 함).

>[!NOTE]
>
>기준 시퀀스를 2016년 10월 릴리스 이전에 만든 [!UICONTROL 권장 사항] 활동에는 사용할 수 없습니다[!DNL Target Premium].

기준 시퀀스를 만들려면 먼저 시퀀스에 포함할 기준을 만들어야 합니다. 각 유형의 대상 규칙을 구성하는 방법에 대한 자세한 내용은 [자세한 내용은 기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

기준이 디자인을 채울 수 있는 충분한 결과를 반환하지 않을 경우, 기준 시퀀스를 사용하여 일반적인 백업 권장 사항을 사용하는 대신 추가로 타깃팅된 권장 사항을 제공할 수 있습니다. 일반적으로 기준 시퀀스는 더 적은 결과를 반환할 수 있는 더 구체적인 타겟팅에서 더 많은 결과를 반환하는 더 일반적인 타겟팅으로 진행됩니다.

기준 시퀀스는 다음 예에 표시된 대로 페이지 유형에 따라 순서대로 달라질 수 있습니다.

| 페이지 유형 | 가능한 시퀀스 순서 |
| --- | --- |
| 제품 페이지 | <ol><li>동일한 브랜드의 현재 항목 기준</li><li>모든 브랜드의 현재 항목 기준</li><li>컨텐츠 유사성 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |
| 홈 페이지 | <ol><li>방문자의 마지막 구매 기준 </li><li>방문자의 즐겨찾기 항목 기준</li><li>방문자의 즐겨찾기 카테고리 기준</li><li>최상위 판매자 기준</li><li>사이트에서 가장 많이 본 항목 기준</li></ol> |

## 기준 시퀀스 만들기

다음에서 기준 시퀀스를 만듭니다. [!UICONTROL 기준 시퀀스 만들기] 화면.

[!UICONTROL 기준 시퀀스 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* **[!UICONTROL 권장 사항]** > **[!UICONTROL 기준]** 라이브러리 화면에서 **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**&#x200B;를 클릭합니다. 여기서 만드는 기준은 자동으로 모든 [!UICONTROL 권장 사항] 활동에 사용 가능해집니다.
* 다음을 만들 때 [!UICONTROL Recommendations] 활동, 기준 선택 화면에서 **[!UICONTROL 새로 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**. 다른 [!UICONTROL 권장 사항] 활동과 함께 사용할 새 기준 시퀀스를 저장하는 옵션이 있습니다.
* 을(를) 편집할 때 [!UICONTROL Recommendations] 활동, 클릭 [!UICONTROL Recommendations 위치] 상자를 선택한 다음 **[!UICONTROL 기준 변경]**. [!UICONTROL 기준 선택] 화면에서 **[!UICONTROL 새로 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**&#x200B;를 클릭합니다. 다른 [!UICONTROL 권장 사항] 활동과 함께 사용할 새 기준을 저장하는 옵션이 있습니다.

다음 단계에서는 [!UICONTROL 기준 시퀀스 만들기] 첫 번째 방법을 사용하여 스크린: **[!UICONTROL Recommendations]** > **[!UICONTROL 기준]** 라이브러리 화면입니다.

1. 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL 기준]**.

1. 클릭 **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 시퀀스 만들기]**.

   ![CreateCriteriaSequence 이미지](assets/CreateCriteriaSequence.png)

1. 다음에 정보를 입력하십시오. [기본 정보](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) 섹션.

1. 다음에서 **[!UICONTROL 기준 시퀀스]** 섹션, 클릭 **[!UICONTROL 기준 추가]**.

   시퀀스 순서는 디자인이 채워지는 순서를 정의합니다. 기준 1에 디자인을 채울 권장 사항이 충분하지 않으면 나머지 슬롯이 기준 2로 채워집니다.

   ![기준 추가](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png)

1. 다음에서 [!UICONTROL 기준 선택] 화면에서 기준을 선택한 다음 **[!UICONTROL 추가]**.

   검색 상자와 필터 드롭다운을 사용하여 원하는 기준을 찾을 수 있습니다.

   ![기준 선택](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (선택 사항) **[!UICONTROL 반환되는 항목 수 제한]** 켜기 위치로 전환한 다음 항목의 수(1에서 50 사이)를 지정합니다.

   ![반환되는 항목 수 제한 토글](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   의 가치를 이해하는 데 도움이 됩니다. [!UICONTROL 반환되는 항목 수 제한] 옵션(&quot;슬롯 수준 제어&quot;라고도 함)은 다음 사용 사례를 고려합니다.

   * **사용 사례 1**: 단일 권장 사항 트레이에 서로 다른 종류의 항목이 혼합되어 있어야 합니다. 예를 들어, 겉옷(재킷)과 상의(셔츠, 티셔츠)를 혼합하여 표시하려고 합니다. 이를 위해서는 디자인의 모든 슬롯에 원하는 모든 잠재적 제품 유형을 포함하는 활동에 대한 컬렉션을 사용하십시오. 그런 다음 겉옷만 포함하도록 기준을 제한하는 정적 필터를 사용하여 첫 번째 기준을 설정하고, 상단만 포함하도록 기준을 제한하는 정적 필터를 사용하여 두 번째 기준을 설정합니다. 마지막으로 두 기준을 기준 시퀀스에 추가하고 첫 번째 기준을 슬롯 2개로 제한합니다.

      사이트에서는 권장 사항 트레이가 다음과 같을 수 있습니다.

      ![추천 제품 추천 트레이](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **사용 사례 2**: 대체 항목과 보조 항목을 모두 혼합해야 합니다. 조회/조회 알고리즘을 사용하도록 하나의 기준을 설정하고 권장 항목을 현재 항목의 카테고리로 제한하는 동적 필터를 사용합니다. 조회/구매 알고리즘을 사용하도록 두 번째 기준을 설정하고 현재 항목의 카테고리와 일치하지 않는 권장 항목만 포함하는 동적 필터를 사용합니다. 마지막으로 두 기준을 시퀀스에 추가하고 첫 번째 기준을 슬롯 2개로 제한합니다.

1. 시퀀스에 추가 기준을 계속 추가합니다. 시퀀스에 최대 5개의 기준을 추가할 수 있습니다.

1. 사용 [백업 컨텐츠 옵션](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   기준 시퀀스가 기준 목록에 나타납니다.

   권장 사항 논리 선택 사항에 대한 자세한 내용은 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

## 교육 비디오: 추천에서 기준 만들기(12:33) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
