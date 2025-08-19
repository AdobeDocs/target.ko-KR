---
keywords: 권장 사항;권장 사항 활동;기준;알고리즘;권장 사항 키;사용자 지정 키;업계 카테고리;소매;전자 상거래;리드 생성;b2b;금융 서비스;미디어;게시
description: Adobe [!DNL Target] [!DNL Recommendations]에서 기준을 사용하는 방법을 알아봅니다.
title: ' [!DNL Target] 추천에서 기준을 사용하는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 5%

---

# [!UICONTROL Criteria]

[!UICONTROL Criteria] [!DNL Adobe Target]의 [!DNL Recommendations]은(는) 사전 결정된 방문자 동작 집합을 기반으로 추천할 제품 또는 콘텐츠를 결정하는 규칙입니다. 기준은 인기 있는 트렌드, 방문자의 현재 및 과거 행동 또는 유사한 제품 및 콘텐츠를 기반으로 할 수 있습니다. 여러 알고리즘을 추가하여 여러 권장 사항 유형을 서로 비교하면서 테스트할 수 있습니다.

다음 섹션에서는 각 키에 사용할 수 있는 기준 키와 권장 사항 논리에 대해 자세히 설명합니다. 자세한 내용을 보려면 링크를 클릭하십시오.

## 업계 카테고리 {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

기준을 만드는 동안 권장 사항 활동의 목표를 기반으로 수직 산업을 선택합니다.

| 업계 카테고리 | 목표 |
|--- |--- |
| [!UICONTROL Retail/Ecommerce] | 구매를 발생시키는 전환 |
| [!UICONTROL Lead Generation/B2B/Financial Services] | 구매가 없는 전환 |
| [!UICONTROL Media/Publishing] | 참여 |

기타 기준 옵션은 선택한 수직 시장에 따라 달라집니다. **[!UICONTROL Administration]>[!UICONTROL Recommendations]** 페이지에서 기본 수직 시장을 설정하거나 각 기준에 수직 시장을 지정할 수 있습니다.

## 알고리즘 유형 {#section_885B3BB1B43048A88A8926F6B76FC482}

선택하는 알고리즘 유형에 따라 사용 가능한 알고리즘이 결정됩니다.

다음 표에서는 다양한 알고리즘 유형과 함께 제공되는 알고리즘에 대해 설명합니다.

| 알고리즘 유형 | 사용 시기 | 사용 가능한 알고리즘 |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | 사용자의 장바구니 콘텐츠를 기반으로 추천을 제공합니다. | <ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul>자세한 내용은 [추천 키를 기반으로 추천](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based)의 *장바구니 기반*&#x200B;을 참조하세요. |
| [!UICONTROL Popularity-Based] | 사이트에서 항목의 전체 인기도를 기반으로 추천하거나 사용자가 좋아하거나 가장 많이 본 카테고리, 브랜드, 장르 등의 항목 인기도를 기반으로 추천합니다. | <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | 사용자가 현재 보고 있거나 최근에 본 항목과 유사한 항목을 찾은 후 권장 사항을 제공합니다. | <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | 사용자의 행동을 기반으로 권장 사항을 제공합니다. | <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | 업로드하는 사용자 지정 파일을 기반으로 권장 사항을 제공합니다. | <ul><li>사용자 지정 알고리즘</li></ul> |

각 알고리즘에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오.

## 사용자 지정 권장 사항 키 사용 {#custom-key}

사용자 지정 프로필 속성 값을 기준으로 권장 사항을 지정할 수도 있습니다.

>[!NOTE]
>
>사용자 지정 프로필 매개 변수는 JavaScript, API 또는 통합을 통해 [!DNL Target]에 전달할 수 있습니다. 사용자 지정 프로필 특성에 대한 자세한 내용은 [방문자 프로필](/help/main/c-target/c-visitor-profile/visitor-profile.md)을 참조하세요.

예를 들어 사용자가 가장 최근에 큐에 추가한 동영상을 기반으로 권장 동영상을 표시하려고 한다고 가정합니다.

1. **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**&#x200B;을(를) 클릭합니다.

1. [기본 정보 섹션](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info)에 정보를 입력하십시오.

1. [권장 알고리즘](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) 섹션의 **[!UICONTROL Item Based]** 목록에서 **[!UICONTROL Algorithm Type]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL People Who Viewed This, Viewed That]** 목록에서 **[!UICONTROL Algorithm]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Recommendation Key]** 목록에서 사용자 지정 프로필 특성을 선택합니다(예: [!UICONTROL Last Show Added to Watchlist]).

## 기준 정보 보기 {#section_7162DE58E4594FD688A4D7FDB829FD8B}

[!UICONTROL Name] 열에서 원하는 기준을 클릭하여 기준 세부 정보를 볼 수 있습니다.

**[!UICONTROL Attributes]** 및 세부 정보 섹션에서 [!UICONTROL Name], [!UICONTROL Description], [!UICONTROL Industry Vertical], [!UICONTROL Page Types], [!UICONTROL Recommendation Key], [!UICONTROL Recommendation Logic], [!UICONTROL Algorithm ID] 및 마지막으로 수정된 정보(날짜 및 알고리즘을 수정한 사람)를 포함하여 선택한 기준에 대한 일반 정보를 볼 수 있습니다.

**[!UICONTROL Usage]** 섹션을 통해 선택한 조건을 참조하는 활동 목록을 볼 수 있습니다.

>[!NOTE]
>
>[!UICONTROL Algorithm Usage] 기능은 현재 [!DNL Recommendations] 활동에만 지원됩니다. 이 기능은 현재 [!UICONTROL A/B Test]오퍼로서 권장 사항[!UICONTROL Auto-Allocate]을 포함하는 [!UICONTROL Auto-Target], [!UICONTROL Experience Targeting], [ 및 ](/help/main/c-recommendations/recommendations-as-an-offer.md)(XT) 활동에 대해 지원되지 않습니다.
