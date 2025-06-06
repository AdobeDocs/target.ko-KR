---
keywords: 권장 사항 키;권장 사항 논리;현재 범주;사용자 지정 속성;마지막으로 구매한 항목;마지막으로 본 항목;가장 많이 본 항목;가장 많이 본 항목;즐겨찾기 범주;인기도;최근에 본 항목;마지막으로 구매한 항목;마지막으로 본 항목;가장 많이 본 항목;가장 많이 본 항목;즐겨찾기;최근에 본 항목
description: 방문자 동작 컨텍스트를 사용하여 [!UICONTROL Recommendations] 활동에서 관련 결과를 표시하는 키를 기반으로 권장 사항을 사용하는 방법에 대해 알아봅니다.
title: '[!UICONTROL Recommendation Key]에서 [!UICONTROL Recommendation]을(를) 기준으로 하려면 어떻게 합니까?'
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '3463'
ht-degree: 29%

---

# 권장 사항 키를 기반으로 권장 사항 만들기

알고리즘 기반의 Recommendations은 방문자 행동 컨텍스트를 사용하여 [!DNL Adobe Target] [!DNL Recommendations] 활동에서 관련 결과를 표시합니다.

각 알고리즘 유형은 다음 표와 같이 해당 유형에 적합한 다양한 알고리즘을 제공합니다.

| 알고리즘 유형 | 사용 가능한 알고리즘 |
| --- | --- |
| [!UICONTROL Cart-Based] | 사용자의 장바구니 콘텐츠를 기반으로 추천을 제공합니다.<ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul> |
| [!UICONTROL Popularity-Based] | 사이트에서 항목의 전체 인기도를 기반으로 추천하거나 사용자가 좋아하거나 가장 많이 본 카테고리, 브랜드, 장르 등의 항목 인기도를 기반으로 추천합니다. <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | 사용자가 현재 보고 있거나 최근에 본 항목과 유사한 항목을 찾은 후 권장 사항을 제공합니다. <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | 사용자의 행동을 기반으로 권장 사항을 제공합니다. <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | 업로드하는 사용자 지정 파일을 기반으로 권장 사항을 제공합니다. <ul><li>사용자 지정 알고리즘</li></ul> |

각 기준은 자체 탭에 정의됩니다. 트래픽은 여러 기준 테스트에 고르게 분할됩니다. 즉, 두 개의 기준이 있으면 트래픽이 이러한 두 기준 간에 동일하게 분할됩니다. 두 개의 기준과 두 개의 디자인이 있는 경우 트래픽이 네 개의 조합 간에 균일하게 분할됩니다. 또한 비교를 위해 기본 콘텐츠를 보는 사이트 방문자의 비율도 지정할 수 있습니다. 이 경우 지정된 비율의 방문자는 기본 콘텐츠를 보고 나머지 방문자는 기준과 디자인 조합 간에 분할됩니다.

기준을 만들고 해당 알고리즘 유형 및 알고리즘을 정의하는 방법에 대한 자세한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

다른 권장 사항 알고리즘은 서로 다른 유형의 페이지에 배치될 수 있도록 해줍니다. 각 알고리즘 유형 및 사용 가능한 알고리즘에 대한 자세한 내용은 다음 섹션을 참조하십시오.

## 장바구니 기반 {#cart-based}

[!UICONTROL Cart-Based] 알고리즘 유형을 사용하면 방문자의 현재 장바구니의 내용에 따라 항목을 추천할 수 있습니다. 권장 사항 키는 쉼표로 구분된 값으로 [mbox 매개 변수 `cartIds`](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=ko){target=_blank}을(를) 통해 제공됩니다. 처음 10개의 값만 고려됩니다.

장바구니 기반 권장 사항 논리는 &quot;[!UICONTROL Recommended For You]&quot; 사용자 기반 알고리즘 및 &quot;[!UICONTROL People Who Viewed These, Bought Those]&quot; 및 &quot;[!UICONTROL People Who Bought These, Bought Those]&quot; 항목 기반 알고리즘과 유사합니다.

[!DNL Target]은(는) 공동 작업 필터링 기법을 사용하여 방문자 장바구니에 있는 각 항목의 유사성을 확인한 다음 각 항목 간에 이러한 비헤이비어 유사성을 결합하여 병합 목록을 가져옵니다.

또한 [!DNL Target]을(를) 통해 마케터는 단일 세션 내에서 또는 여러 세션에서 방문자 행동을 볼 수 있습니다.

* **[!UICONTROL Single Session]**: 다른 방문자가 단일 세션 내에서 수행한 작업을 기반으로 합니다.

  사용, 상황 또는 이벤트에 따라 제품이 서로 강력하게 &quot;함께&quot; 이동한다는 느낌이 있을 때 단일 세션 내에서 동작을 살펴보는 것이 적절할 수 있습니다. 예를 들어 방문자가 프린터를 구입하고 있으며 잉크와 용지도 필요할 수 있습니다. 또는 방문자가 땅콩 버터를 구매하고 빵과 젤리도 필요할 수 있습니다.

* **[!UICONTROL Across Sessions]**: 다른 방문자가 여러 세션에서 수행한 작업을 기반으로 합니다.

  방문자의 선호도나 취향에 따라 제품이 서로 강하게 &quot;함께&quot; 이동한다는 느낌이 있을 때 여러 세션에서 동작을 살펴보는 것이 적절할 수 있습니다. 예를 들어 방문자는 스타워즈를 좋아하고 인디애나 존스를 좋아하지만, 같은 자리에서 두 영화를 모두 보고 싶지 않은 경우에도 마찬가지입니다. 또는 방문자가 보드 게임 &quot;Codenames&quot;를 좋아하고 보드 게임 &quot;Avalon&quot;을 좋아할 수도 있습니다. 방문자가 두 게임을 동시에 플레이할 수 없는 경우에도 마찬가지입니다.

[!DNL Target]은(는) 단일 세션 내에서 방문자 행동을 보는지 아니면 여러 세션에서 방문자 행동을 보는지 여부에 관계없이 현재 장바구니에 있는 항목을 기준으로 각 방문자에 대해 권장 사항을 제공합니다.

[!UICONTROL Cart-Based] 알고리즘 유형에서 다음 알고리즘을 사용할 수 있습니다.

### [!UICONTROL People Who Viewed This, Also Viewed]

지정한 항목을 본 것과 동일한 세션에서 가장 자주 본 항목을 추천합니다.

이 논리는 이 항목을 본 후에 본 다른 제품을 반환합니다. 지정한 제품이 결과 세트에 포함되어 있지 않습니다.

이 논리를 사용하면 항목을 본 다른 방문자도 본 항목을 추천하여 추가 전환 기회를 만들 수 있습니다. 예를 들어 사이트에서 도로 자전거를 보는 방문자는 자전거 헬멧, 자전거 키트, 자물쇠 등도 살펴볼 수 있습니다. 다른 제품이 매출을 증대하는 데 도움이 됨을 제안하는 이 논리를 사용하여 권장 사항을 만들 수 있습니다.

이 알고리즘을 선택하는 경우 다음 Recommendations 키를 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Also Bought]

지정된 항목을 보는 것과 동일한 세션에서 가장 자주 구입하는 항목을 권장합니다.

이 논리는 사용자가 이 제품을 본 후 구매한 다른 제품을 반환합니다. 지정한 제품이 결과 세트에 포함되어 있지 않습니다.

이 논리를 사용하면 제품을 본 다른 방문자가 구매한 항목을 표시하는 제품 페이지 등에 권장 사항을 표시하여 교차 판매 기회를 늘릴 수 있습니다. 예를 들어 방문자가 낚싯대를 보고 있는 경우, 권장 사항에는 다른 방문자가 구매한 항목(태클 상자, 장롱 및 낚시 미끼와 같은)이 추가로 표시될 수 있습니다. 방문자가 사이트를 탐색할 때 추가 구매 추천을 제공합니다.

이 알고리즘을 선택하는 경우 다음 Recommendations 키를 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Also Bought]

지정한 항목과 동시에 고객이 가장 자주 구입한 항목을 추천합니다.

이 논리는 사용자가 이 제품을 구매한 후 다른 제품을 구매한 것으로 반환됩니다. 지정한 제품이 결과 세트에 포함되어 있지 않습니다.

이 논리를 사용하면 다른 구매자가 구매한 항목을 표시하는 장바구니 요약 페이지에 추천을 표시하여 교차 판매 기회를 늘릴 수 있습니다. 예를 들어 방문자가 정장을 구매하는 경우, 권장 사항에는 다른 방문자가 정장과 함께 구매한 넥타이, 정장 신발 및 커프링크와 같은 추가 항목이 표시될 수 있습니다. 방문자가 구매를 검토하면, 추가 권장 사항을 제공합니다.

이 알고리즘을 선택하는 경우 다음 Recommendations 키를 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## [!UICONTROL Popularity-Based]

[!UICONTROL Popularity-Based] 알고리즘 유형을 사용하면 사이트 전체 항목의 전체 인기 또는 사용자가 좋아하거나 가장 많이 본 카테고리, 브랜드, 장르 등의 항목 인기에 따라 권장 사항을 만들 수 있습니다.

[!UICONTROL Popularity-Based] 알고리즘 유형에서 다음 알고리즘을 사용할 수 있습니다.

### [!UICONTROL Most Viewed Across the Site] {#most-viewed}

권장 사항은 가장 자주 본 항목에 의해 결정됩니다. 이 항목은 다음과 같이 동작하는 최신/빈도 기준에 의해 결정됩니다.

* 첫 번째 제품 보기에 대해 10포인트
* 모든 후속 보기에 대해 5포인트
* 세션 끝에서 모든 값을 2로 나누기

예를 들어 한 세션에서 서프보드 A를 본 다음 서프보드 B를 보면 A: 10, B: 5가 됩니다. 세션이 종료되면 A: 5, B: 2.5가 됩니다. 다음 세션에서 동일한 항목을 볼 경우 값이 A: 15 B: 7.5로 변경됩니다.

홈 페이지 또는 랜딩 페이지 및 오프사이트 광고와 같은 일반 페이지에서 이 알고리즘을 사용합니다.

### [!UICONTROL Most Viewed by Category] {#most-viewed-category}

제품 대신 카테고리 점수가 산정되는 것만 제외하고, &quot;가장 많이 본 항목&quot;에 사용된 것과 동일한 방법을 사용하여, 가장 많은 활동을 받은 카테고리에 의해 권장 사항이 결정됩니다.

이 항목은 다음과 같이 동작하는 최신/빈도 기준에 의해 결정됩니다.

* 첫 번째 카테고리 보기에 대해 10포인트
* 모든 후속 보기에 대해 5포인트

처음으로 방문한 카테고리에는 10포인트가 부여됩니다. 같은 카테고리에 대한 후속 방문에는 5포인트가 부여됩니다. 각 방문에서 이전에 본 비현재 카테고리는 1포인트씩 감소됩니다.

예를 들어 한 세션에서 카테고리 A를 본 다음 카테고리 B를 보면 A: 9, B: 10이 됩니다. 다음 세션에서 동일한 항목을 보는 경우 값은 A: 20 B: 9로 변경됩니다.

홈 페이지 또는 랜딩 페이지 및 오프사이트 광고와 같은 일반 페이지에서 이 알고리즘을 사용합니다.

가장 많이 본 카테고리 알고리즘을 선택하는 경우 다음 Recommendations 키를 선택할 수 있습니다.

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Most Viewed by Item Attribute]

사이트에서 가장 많이 본 항목 또는 미디어와 유사한 항목 또는 미디어를 권장합니다.

이 알고리즘을 사용하면 &quot;이름&quot; 또는 &quot;브랜드&quot;와 같이 권장 사항의 기반이 되는 항목 속성을 선택할 수 있습니다.

그런 다음 방문자의 프로필에 저장된 프로필 속성 중 일치시킬 프로필 속성을 선택합니다(예: &quot;Favorite Brand&quot;, &quot;Last Item Added to Cart&quot; 또는 &quot;Most Viewed Show&quot;).

### [!UICONTROL Top Sellers Across the Site] {#top-sellers}

사이트에서 가장 많이 완료된 주문에 포함된 품목을 표시합니다. 단일 주문에서 여러 개의 동일한 항목은 하나의 주문으로 계산됩니다.

이 알고리즘을 사용하여 사이트의 최상위 판매 항목에 대한 권장 사항을 만들어 전환율과 매출을 높일 수 있습니다. 이 논리는 특히 사이트를 처음 방문하는 사용자에게 적합합니다.

### [!UICONTROL Top Sellers by Category]

범주별로 가장 완료된 주문에 포함된 품목을 표시합니다. 단일 주문에서 여러 개의 동일한 항목은 하나의 주문으로 계산됩니다.

이 알고리즘을 사용하면 카테고리를 기반으로 사이트의 최상위 판매 항목에 대한 권장 사항을 만들어 전환율과 매출을 높일 수 있습니다. 이 논리는 특히 사이트를 처음 방문하는 사용자에게 적합합니다.

[!UICONTROL Most Viewed by Category] 알고리즘을 선택하면 다음 [!UICONTROL Recommendations Keys]을(를) 선택할 수 있습니다.

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Top Sellers by Item Attribute]

사이트에서 가장 많이 구매한 항목 또는 미디어와 유사한 항목 또는 미디어를 권장합니다.

이 알고리즘을 사용하면 &quot;이름&quot; 또는 &quot;브랜드&quot;와 같이 권장 사항의 기반이 되는 항목 속성을 선택할 수 있습니다.

그런 다음 방문자의 프로필에 저장된 프로필 속성 중 일치시킬 프로필 속성을 선택합니다(예: &quot;Favorite Brand&quot;, &quot;Last Item Added to Cart&quot; 또는 &quot;Most Viewed Show&quot;).

### [!UICONTROL Top by Analytics Metric]

*x*&#x200B;이(가) 임의의 [!DNL Analytics] 지표인 &quot;상단 x&quot;를 표시합니다. mbox의 동작 데이터를 사용할 때 [!UICONTROL Top Sold] 또는 [!UICONTROL Top Viewed] (x = &quot;Sold&quot; 또는 x = &quot;Viewed&quot;)을 사용할 수 있습니다. [!DNL Adobe Analytics]의 동작 데이터를 사용하는 경우 x = &quot;장바구니 추가&quot; 또는 다른 [!DNL Analytics] 지표를 사용할 수 있습니다.

## [!UICONTROL Item-Based]

[!UICONTROL Item-Based] 권장 사항 유형을 사용하면 사용자가 현재 보고 있거나 최근에 본 항목과 유사한 항목을 찾은 후 권장 사항을 제공할 수 있습니다.

[!UICONTROL Item-Based] 알고리즘 유형에서 다음 알고리즘을 사용할 수 있습니다.

### [!UICONTROL People Who Viewed This, Viewed That] {#viewed-viewed}

지정한 항목을 본 것과 동일한 세션에서 가장 자주 본 항목을 추천합니다.

이 논리는 이 항목을 본 후에 본 다른 제품을 반환합니다. 지정된 제품은 결과 세트에 포함되지 않습니다.

이 논리를 사용하면 항목을 본 다른 방문자도 본 항목을 추천하여 추가 전환 기회를 만들 수 있습니다. 예를 들어 사이트에서 도로 자전거를 보는 방문자는 자전거 헬멧, 자전거 키트, 자물쇠 등도 살펴볼 수 있습니다. 다른 제품이 매출을 증대하는 데 도움이 됨을 제안하는 이 논리를 사용하여 권장 사항을 만들 수 있습니다.

이 알고리즘을 선택하면 다음 [!UICONTROL Recommendations Keys]을(를) 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Bought That] {#viewed-bought}

지정한 항목을 본 것과 동일한 세션에서 가장 자주 구입한 항목을 추천합니다. 이 기준은 이 항목을 본 사용자가 구입한 다른 제품을 반환하고 지정된 제품은 결과 세트에 포함되지 않습니다.

이 논리는 사용자가 이 제품을 본 후 구매한 다른 제품을 반환합니다. 지정된 제품은 결과 세트에 포함되지 않습니다.

이 논리를 사용하면 제품을 본 다른 방문자가 구매한 항목을 표시하는 제품 페이지 등에 권장 사항을 표시하여 교차 판매 기회를 늘릴 수 있습니다. 예를 들어 방문자가 낚싯대를 보고 있는 경우, 권장 사항에는 다른 방문자가 구매한 항목(태클 상자, 장롱 및 낚시 미끼와 같은)이 추가로 표시될 수 있습니다. 방문자가 사이트를 탐색할 때 추가 구매 추천을 제공합니다.

이 알고리즘을 선택하면 다음 [!UICONTROL Recommendations Keys]을(를) 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Bought That] {#bought-bought}

지정한 항목과 동시에 고객이 가장 자주 구입한 항목을 추천합니다.

이 논리는 사용자가 이 제품을 구매한 후 다른 제품을 구매한 것으로 반환됩니다. 지정한 제품이 결과 세트에 포함되어 있지 않습니다.

이 논리를 사용하면 다른 구매자가 구매한 항목을 표시하는 장바구니 요약 페이지에 추천을 표시하여 교차 판매 기회를 늘릴 수 있습니다. 예를 들어 방문자가 정장을 구매하는 경우, 권장 사항에는 다른 방문자가 정장과 함께 구매한 넥타이, 정장 신발 및 커프링크와 같은 추가 항목이 표시될 수 있습니다. 방문자가 구매를 검토하면, 추가 권장 사항을 제공합니다.

이 알고리즘을 선택하면 다음 [!UICONTROL Recommendations Keys]을(를) 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL Items with Similar Attributes] {#similar-attributes}

현재 페이지 활동 또는 과거 방문자 행동을 기반으로 한 항목 또는 미디어와 유사한 항목 또는 미디어를 추천합니다.

[!UICONTROL Items with Similar Attributes] 또는 [!UICONTROL Media with Similar Attributes]을(를) 선택하면 콘텐츠 유사성 규칙을 설정할 수 있습니다.

콘텐츠 유사성을 사용하여 권장 사항을 생성하는 방식은 [!UICONTROL People Who Viewed This], [!UICONTROL Viewed That] 및 과거 동작을 기반으로 하는 기타 논리를 사용하는 권장 사항에 표시되지 않는 새 항목에 특히 유용합니다. 또한 콘텐츠 유사성을 사용하여 과거 구입 내역 또는 기타 기록 데이터가 없는 새 방문자를 위한 유용한 권장 사항을 생성할 수도 있습니다.

이 알고리즘을 선택하면 다음 [!UICONTROL Recommendations Keys]을(를) 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

자세한 내용은 [콘텐츠 유사성](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity)을 참조하세요.

## [!UICONTROL User-Based]

[!UICONTROL User-Based] 알고리즘 유형을 사용하면 사용자의 동작을 기반으로 권장 사항을 제공할 수 있습니다.

[!UICONTROL User-Based] 알고리즘 유형에서 다음 알고리즘을 사용할 수 있습니다.

### [!UICONTROL Recently Viewed Items] {#recently-viewed}

방문자의 기록(여러 세션)을 사용하여 디자인의 슬롯 수에 따라 방문자가 마지막으로 본 *x*&#x200B;개 항목을 표시합니다.

[!UICONTROL Recently Viewed Items] 알고리즘이 지정된 [환경](/help/main/administrating-target/hosts.md)에 대한 결과를 반환합니다. 방문자가 서로 다른 환경에 속한 두 사이트 간에 전환하는 경우 각 사이트에는 해당 사이트에서 최근에 본 항목만 표시됩니다. 방문자가 동일한 환경에 있는 두 사이트 간에 전환하는 경우 방문자에게 두 사이트에 대해 최근에 본 동일한 항목이 표시됩니다.

>[!NOTE]
>
>백업 권장 사항에는 [!UICONTROL Recently Viewed Items] 기준을 사용할 수 없습니다.

특정 특성이 있는 항목만 표시되도록 [!UICONTROL Recently Viewed Items] 또는 [!UICONTROL Recently Viewed Media]을(를) 필터링할 수 있습니다.

* [!UICONTROL Recently Viewed] 기준은 권장 사항의 다른 기준처럼 구성할 수 있습니다.
* 다른 기준과 동일한 방법으로 [컬렉션](/help/main/c-recommendations/c-products/collections.md), [제외](/help/main/c-recommendations/c-products/exclusions.md) 및 [포함](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)(가격 및 재고에 대한 특별한 규칙 포함)을 사용할 수 있습니다.

가능한 사용 사례로는 여러 비즈니스를 운영하는 다국적 기업이 여러 디지털 속성에서 방문자 보기 항목을 가질 수 있는 경우를 들 수 있습니다. 이 경우 항목을 본 각각의 속성에 대해서만 표시하도록 최근에 본 항목을 제한할 수 있습니다. 이렇게 하면 최근에 본 항목이 다른 디지털 속성의 사이트에 표시되지 않습니다.

홈 페이지 또는 랜딩 페이지 및 오프사이트 광고와 같은 일반 페이지에서 이 알고리즘을 사용합니다.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items]은(는) 활동에 대한 제외 전역 설정과 선택한 컬렉션 설정을 모두 준수합니다. 항목이 전역 제외에 의해 제외되거나 선택한 컬렉션에 포함되지 않은 경우 표시되지 않습니다. 따라서 [!UICONTROL Recently Viewed Items] 기준을 사용하는 경우 일반적으로 &quot;모든 컬렉션&quot; 설정을 사용해야 합니다.

### [!UICONTROL Recommended for You] {#recommended-for-you}

각 방문자의 검색, 보기 및 구매 기록에 따라 항목을 추천합니다.

이 알고리즘을 사용하여 새 방문자와 돌아오는 방문자 모두에게 개인화된 내용과 경험을 전달할 수 있습니다. 권장 사항 목록은 방문자의 가장 최근 활동에 가중치가 부여되며 세션 중에 업데이트되고 사용자가 사이트를 탐색할 때 더 개인화됩니다.

보기와 구매 모두 권장 품목을 결정하는 데 사용됩니다. 지정한 권장 사항 키(예: [!UICONTROL Current Item])는 선택한 포함 규칙 필터를 적용하는 데 사용됩니다.

예를 들어 다음 작업을 수행할 수 있습니다.

* 특정 기준을 충족하지 않는 항목(제품 품절, 30일 이상 전에 게시된 문서, R 등급의 영화 등)은 제외합니다.
* 포함된 항목을 단일 범주 또는 현재 범주로 제한.

이 알고리즘을 선택하는 경우 다음 필터링 키를 선택할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## 사용자 지정 기준 {#custom}

[!UICONTROL Custom Criteria] 알고리즘 유형을 사용하면 업로드하는 사용자 지정 파일을 기반으로 권장 사항을 만들 수 있습니다.

권장 사항은 방문자 프로필에 저장된 항목에 따라 결정되며, user.*x* 또는 profile.*x* 속성을 사용합니다.

이 옵션을 선택하는 경우 `entity.id` 값이 프로필 속성에 있어야 합니다.

사용자 지정 속성을 권장 사항의 기반으로 사용할 때에는 사용자 지정 속성을 선택한 다음, 권장 사항 유형을 선택해야 합니다.

자신만의 사용자 지정 기준 출력의 맨 위에서 실시간 필터링을 수행할 수 있습니다. 예를 들어 권장 사항 항목을 방문자가 선호하는 범주 또는 브랜드의 항목으로만 제한할 수 있습니다. 이렇게 하면 오프라인 계산을 실시간 필터링과 결합할 수 있습니다.

이 기능은 [!DNL Target]을(를) 사용하여 오프라인 계산된 권장 사항이나 사용자 지정 조정 목록의 맨 위에 개인화를 추가할 수 있음을 의미합니다. 이 작업에서는 데이터 과학자 및 연구의 힘을 Adobe의 유효성이 증명된 전달, 런타임 필터링, A/B 테스트, 타깃팅, 보고, 통합 등과 결합합니다.

[!UICONTROL Custom Criteria]에 포함 규칙을 추가하면 기존의 정적 권장 사항이 방문자의 관심 사항을 기반으로 하는 동적 권장 사항으로 변경됩니다.

* 사용자 지정 기준은 권장 사항에 있는 다른 기준처럼 구성이 가능합니다.
* 다른 기준과 동일한 방법으로 [컬렉션](/help/main/c-recommendations/c-products/collections.md), [제외](/help/main/c-recommendations/c-products/exclusions.md) 및 [포함](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)(가격 및 재고에 대한 특별한 규칙 포함)을 사용할 수 있습니다.

가능한 사용 사례는 다음과 같습니다.

* 사용자 지정 조정 목록에서 동영상을 추천하고 싶은데, 방문자가 아직 시청하지 않은 경우에만 추천하고 싶습니다.
* 오프라인 알고리즘을 실행하고 결과를 사용하여 권장 사항을 제공하려고 하지만, 재고 부족 항목은 권장되지 않도록 해야 합니다.
* 이 방문자의 선호 카테고리에 있는 항목만 포함하려 합니다.

## 권장 사항 키 {#keys}

[!UICONTROL Recommendation Key] 드롭다운 목록에서 다음 권장 사항 키를 사용할 수 있습니다.

### [!UICONTROL Current Item] {#current-item}

권장 사항은 현재 방문자가 보고 있는 항목에 의해 결정됩니다.

권장 사항에는 특정 항목에 관심이 있는 방문자의 흥미를 끌 수 있는 다른 항목이 표시됩니다.

이 옵션을 선택한 경우 디스플레이 mbox에 매개 변수로 `entity.id` 값을 전달해야 합니다.

다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

다음에서 사이트의 [!UICONTROL Current Item] 권장 사항 키 사용:

* 제품 페이지와 같은 단일 항목 페이지입니다.
* null 검색 결과 페이지는 사용하지 마십시오.

### [!UICONTROL Last Purchased Item] {#last-purchased}

고유의 각 방문자가 구매한 마지막 항목에 의해 권장 사항이 결정됩니다. 이 값은 자동으로 캡처되므로 페이지에서 값을 전달해서는 안 됩니다.

다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

다음에서 사이트의 [!UICONTROL Last Purchased Item] 권장 사항 키 사용:

* 홈 페이지, 내 계정 페이지, 오프사이트 광고
* 제품 페이지 또는 구매와 관련된 페이지에서는 사용하지 마십시오.

#### 사용자 지정 권장 사항 키

사용자 지정 프로필 속성값을 기준으로 하여 권장 사항을 만들 수 있습니다. 예를 들어 방문자가 가장 최근에 큐에 추가한 동영상을 기반으로 권장 동영상을 표시하려고 한다고 가정합니다.

1. **[!UICONTROL Recommendation Key]** 드롭다운 목록에서 사용자 지정 프로필 특성을 선택합니다(예: &quot;[!UICONTROL Last Show Added to Watchlist]&quot;).
1. 그런 다음 **[!UICONTROL Recommendation Logic]**(예: &quot;[!UICONTROL People Who Viewed This, Viewed That]&quot;)을(를) 선택합니다.

사용자 지정 프로필 속성이 단일 엔티티 ID와 직접 일치하지 않는 경우 엔티티에 대한 일치가 어떻게 일치하는지 [!DNL Recommendations]에 설명해야 합니다. 예를 들어 방문자가 좋아하는 브랜드에서 상위 판매 항목을 표시한다고 가정합니다.

1. **[!UICONTROL Recommendation Key]** 드롭다운 목록에서 사용자 지정 프로필 속성을 선택합니다(예: &quot;Favorite Brand&quot;).

1. 그런 다음 이 키와 함께 사용할 **[!UICONTROL Recommendation Logic]**&#x200B;을(를) 선택합니다(예: &quot;[!UICONTROL Top Sellers]&quot;).

   [!UICONTROL Group By Unique Value Of] 옵션이 표시됩니다.

1. 선택한 키와 일치하는 엔티티 속성을 선택합니다. 이 경우 &quot;[!UICONTROL Favorite Brand]&quot;은(는) `entity.brand`과(와) 일치합니다.

   [!DNL Recommendations]은(는) 이제 각 브랜드에 대한 &quot;[!UICONTROL Top Sellers]&quot; 목록을 생성하고 방문자의 [!UICONTROL Favorite Brand] 프로필 특성에 저장된 값을 기반으로 적절한 &quot;[!UICONTROL Top Sellers]&quot; 목록을 표시합니다.

### [!UICONTROL Last Viewed Item] {#last-viewed}

고유의 각 방문자가 본 마지막 항목에 의해 권장 사항이 결정됩니다. 이 값은 자동으로 캡처되므로 페이지에서 값을 전달해서는 안 됩니다.

다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

다음에서 사이트의 [!UICONTROL Last Viewed Item] 권장 사항 키 사용:

* 홈 페이지, 내 계정 페이지, 오프사이트 광고
* 제품 페이지 또는 구매와 관련된 페이지에서는 사용하지 마십시오.

### [!UICONTROL Most Viewed Item] {#most-viewed-logic}

사이트에서 가장 자주 보는 항목 또는 미디어를 표시합니다.

이 논리를 사용하면 사이트에서 가장 많이 본 항목을 기반으로 한 권장 사항을 표시하여 다른 항목에 대한 전환을 늘릴 수 있습니다. 예를 들어 미디어 사이트는 방문자가 추가 비디오를 보도록 가장 많이 본 비디오에 대한 권장 사항을 홈 페이지에 표시할 수 있습니다.

이 권장 사항 키는 다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

### [!UICONTROL Current Category] {#current-category}

권장 사항은 현재 방문자가 보고 있는 제품 카테고리에 의해 결정됩니다.

권장 사항에는 지정된 제품 카테고리의 항목이 표시됩니다.

이 옵션을 선택한 경우 디스플레이 mbox에 매개 변수로 `entity.categoryId` 값을 전달해야 합니다.

이 권장 사항 키는 다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

다음에서 사이트의 [!UICONTROL Current Category] 권장 사항 키 사용:

* 단일 카테고리 페이지입니다.
* null 검색 결과 페이지는 사용하지 마십시오.

### [!UICONTROL Favorite Category] {#favorite-category}

권장 사항은 방문자가 선호하는 제품 카테고리에 따라 결정됩니다.

권장 사항에는 지정된 제품 카테고리의 항목이 표시됩니다.

이 옵션을 선택한 경우 디스플레이 mbox에 매개 변수로 `entity.categoryId` 값을 전달해야 합니다.

이 권장 사항 키는 다음 알고리즘과 함께 사용할 수 있습니다.

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

다음에서 사이트의 [!UICONTROL Current Category] 권장 사항 키 사용:

* 단일 카테고리 페이지입니다.
* null 검색 결과 페이지는 사용하지 마십시오.

### [!UICONTROL Site Affinity] {#site-affinity}

항목 간 관계의 확실성에 따라 항목을 추천합니다. [!UICONTROL Inclusion Rules] 슬라이더를 사용하여 권장 사항을 제공하기 전에 필요한 데이터의 양을 결정하도록 이 기준을 구성할 수 있습니다. 예를 들어 매우 강력함을 선택하면 일치 확실성이 가장 강한 제품이 권장됩니다.

예를 들어 매우 강력한 관심도를 설정하고 디자인에 5개의 항목이 포함되어 있으며 그중 세 개 항목이 연결 임계값의 강도를 충족하는 경우, 최소 강도 요구 사항을 충족하지 않는 두 항목은 권장 사항에 표시되지 않고 정의된 백업 항목으로 교체됩니다. 친화성이 가장 강한 항목부터 표시됩니다.

예를 들어 온라인 소매업체는 방문자가 이전 세션 중에 관심을 보였던 항목을 이후 방문에서 추천할 수 있습니다. 각 방문자의 세션에 대한 활동이 캡처되어 최신성 및 빈도 모델을 기반으로 친화성을 계산합니다. 이 방문자가 사이트로 돌아가면 사이트 친화성은 사이트에 대한 이전 작업을 기반으로 한 권장 사항을 표시하는 데 사용됩니다.

제품 컬렉션과 사이트 행동이 다양한 일부 고객의 경우 사이트 관심도를 낮게 설정하면 더 좋은 결과를 얻을 수도 있습니다.

이 논리는 다음 권장 사항 키와 함께 사용할 수 있습니다.

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]
