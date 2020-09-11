---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Adobe Target Recommendations의 기준은 미리 결정된 방문자 행동을 기반으로 권장할 제품을 결정하는 규칙입니다.
title: Adobe Target Recommendations의 기준
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
translation-type: tm+mt
source-git-commit: 55f0791bb68fc98e319fa70a647e5168ac72ae1e
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 68%

---


# ![PREMIUM](/help/assets/premium.png) 기준

기준은 사전 결정된 방문자 행동 세트를 기준으로 추천할 제품을 결정하는 규칙입니다.

기준은 어느 작업으로 인해 어느 권장 사항이 발생하는지를 결정합니다. 여러 알고리즘을 추가하여 여러 권장 사항 유형을 서로 비교하면서 테스트할 수 있습니다.

## 업계 카테고리 {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

추천 활동의 목표를 기반으로 산업 수직을 선택합니다. 선택하는 수직 산업에 따라

| 업계 카테고리 | 목표 |
|--- |--- |
| 소매/Ecommerce | 구매를 발생시키는 전환 |
| 리드 생성/B2B/금융 서비스 | 구매가 없는 전환 |
| 미디어/게시 | 참여 |

## Recommendation key {#section_885B3BB1B43048A88A8926F6B76FC482}

선택하는 권장 사항 키는 기준 유형을 결정합니다. [!DNL Recommendations] 활동을 설정할 때 기준 카드로 표현되는 몇 가지 기준 유형이 있습니다.

| 기준 유형 | 키 |
|--- |--- |
| 현재 페이지 활동 | 사용자가 현재 페이지에서 수행하는 활동을 기준으로 항목을 추천합니다. 예를 들어, 특정 문서를 보는 방문자는 동일한 카테고리의 다른 문서를 볼 수 있습니다.<ul><li>[현재 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[현재 카테고리](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| 사용자 지정 | 사용자 지정 속성을 기준으로 항목을 추천합니다.<ul><li>[사용자 지정 속성](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>사용자 지정 속성을 권장 사항의 기반으로 사용할 때에는 사용자 지정 속성을 선택한 다음, 권장 사항 유형을 선택해야 합니다. |
| 과거 동작 | 방문자가 과거에 항목에 반응을 보인 방법을 기반으로 항목을 추천합니다. 예를 들어, 특정 브랜드를 구입한 사람은 해당 브랜드의 다른 항목을 구입할 가능성이 더 높았습니다.<ul><li>[마지막으로 구매한 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[마지막으로 본 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[가장 많이 본 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[즐겨찾는 카테고리](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| 인기도 | 관련 카테고리에서 가장 인기 있는 비디오나, 사이트에서 가장 자주 보는 제품과 같이 가장 인기 있는 항목을 추천합니다.<ul><li>[인기도](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| 최근에 본 항목 | 방문자가 마지막으로 사이트를 방문했을 때 본 항목과 같이 방문자가 가장 최근에 본 항목이나 현재 가장 트렌드가 되는 문서를 추천합니다.<br>최근에 본 항목 알고리즘은 [환경](/help/administrating-target/hosts.md) 내의 방문자 활동에 따른 결과를 반환합니다. 방문자가 서로 다른 환경에 속한 두 사이트 간에 전환하는 경우 알고리즘은 해당 사이트에서 최근에 본 항목만 반환합니다.<br>이 기준 유형은 컬렉션으로 제한되지 않습니다.<ul><li>[최근에 본 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed)</li></ul>**참고:** 백업 권장 사항에는 최근에 본 항목 기준을 사용할 수 없습니다.<br>최근에 본 항목/미디어는 특정 속성이 있는 항목만 표시되도록 필터링 할 수 있습니다.<ul><li>최근에 본 항목 기준은 권장 사항에 있는 다른 기준처럼 구성이 가능합니다.</li><li>다른 기준과 동일한 방법으로 [컬렉션](/help/c-recommendations/c-products/collections.md), [제외](/help/c-recommendations/c-products/exclusions.md) 및 [포함](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)(가격 및 재고에 대한 특별한 규칙 포함)을 사용할 수 있습니다.</li></ul>가능한 사용 사례는 다음과 같습니다.<ul><li>여러 가지 비즈니스를 하는 다국적 기업에는 여러 디지털 속성을 갖는 방문자 보기 항목이 있을 수 있습니다. 이 경우 항목을 본 각각의 속성에 대해서만 표시하도록 최근에 본 항목을 제한할 수 있습니다. 이렇게 하면 최근에 본 항목이 다른 디지털 속성의 사이트에 표시되지 않습니다.</li></ul> |

## 사용자 지정 권장 사항 키 사용 {#custom-key}

사용자 지정 프로필 속성 값을 기반으로 권장 사항을 만들 수도 있습니다.

>[!NOTE]
>
>사용자 지정 프로필 매개 변수는 JavaScript, API 또는 통합을 통해 Target으로 전달할 수 있습니다. 사용자 지정 프로필 속성에 대한 자세한 내용은 [방문자 프로필을 참조하십시오](/help/c-target/c-visitor-profile/visitor-profile.md).

예를 들어 사용자가 대기열에 가장 최근에 추가한 동영상을 기준으로 권장 동영상을 표시하려고 한다고 가정합니다.

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Last Show Added to Watchlist]).

1. Select your [!UICONTROL Recommendation Logic] (for example, [!UICONTROL People Who Viewed This, Viewed That]).

   ![새 기준 만들기 대화 상자](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

If your custom profile attribute does not directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur.

예를 들어 사용자가 좋아하는 브랜드의 최상위 판매 항목을 표시하려는 경우

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Favorite Brand]).

1. Select the [!UICONTROL Recommendation Logic] you want to use with this key (for example, [!UICONTROL Top Sellers]).

   [!UICONTROL 다음의 고유한 값으로 그룹화] 옵션이 표시됩니다.

1. 선택한 키와 일치하는 엔티티 속성을 선택합니다. In this case [!UICONTROL Favorite Brand] matches to `entity.brand`.

   [!DNL Recommendations] 이제 각 브랜드에 대해 &quot;최상위 판매자&quot; 목록을 생성하고 즐겨찾기 브랜드 프로필 속성에 저장된 값을 기반으로 사용자에게 적절한 &quot; [!UICONTROL 최상위 판매자&quot; 목록을] 표시합니다.

   ![최상위 판매자 속성](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algorithms {#criteria-algorithms}

[!DNL Target Recommendations]에서는 정교한 알고리즘을 사용하여 방문자의 작업이 활동에 설정된 기준에 적합한 경우를 판별합니다. 사용 가능한 권장 사항 논리 선택 사항은 권장 사항 키가 판별합니다.

| 기준 | 설명 |
|--- |--- |
| [비슷한 속성을 갖는 항목/미디어](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#similar-attributes) | 현재 페이지 활동 또는 과거 방문자 행동을 기반으로 한 항목 또는 미디어와 유사한 항목 또는 미디어를 추천합니다. |
| [이 항목을 보고 다른 항목도 본 사람](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-viewed) | 지정한 항목을 본 것과 동일한 세션에서 가장 자주 본 항목을 추천합니다. |
| [이 항목을 보고 다른 항목을 구입한 사람](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-bought) | 지정한 항목을 본 것과 동일한 세션에서 가장 자주 구입한 항목을 추천합니다. |
| [이 항목을 구입하고 다른 항목도 구입한 사람](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#bought-bought) | 지정한 항목과 동시에 고객이 가장 자주 구입한 항목을 추천합니다. |
| [사이트 친화성](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#site-affinity) | 항목 간 관계의 확실성에 따라 항목을 추천합니다. |
| [최상위 판매자](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#top-sellers) | 가장 많이 완료된 주문에 포함된 항목. 단일 주문에서 여러 개의 동일한 항목은 하나의 주문으로 계산됩니다. |
| [가장 많이 본 항목](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed) | 가장 자주 표시되는 항목 또는 미디어. |
| [사용자 기반 Recommendations](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | 각 방문자의 탐색, 보기 및 구매 내역을 기준으로 항목을 권장합니다. 이러한 항목을 일반적으로 &quot;권장 사항&quot;이라고 합니다. |

>[!NOTE]
>
>권장 사항을 실행하는 중 기준을 변경하면 보고 데이터를 잃게 됩니다.

방문자에 대해 알려진 추가 정보를 사용하여 권장 사항을 향상시킬 수도 있습니다.

모든 1일 기준이 매일 두 번 실행됩니다. 모든 1주 이상 기준은 하루에 한 번 실행됩니다. 사이트 친화성 기준은 하루에 한 번 실행됩니다. 백업 기준은 하루에 두 번 실행됩니다.

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

카드 위로 마우스를 이동하고 기준을 열지 않은 상태로 기준 카드에서 정보 아이콘을 클릭하여 팝업 카드에 대한 기준 세부 사항을 볼 수 있습니다.

![기준 카드 가리키기](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

**[!UICONTROL 알고리즘 정보]** 탭을 클릭하여 이름, 설명, 업계, 페이지 유형, 권장 사항 키, 권장 사항 논리 및 알고리즘 ID를 포함하여 선택한 기준에 대한 일반 정보를 볼 수 있습니다.

![알고리즘 정보 탭](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

**[!UICONTROL 알고리즘 사용]** 탭을 클릭하여 선택한 기준을 참조하는 활동 목록을 표시합니다. 이 카드에는 활성, 비활성 및 초안 활동이 나열됩니다. 라이브 활동/비활성 활동/초안 활동 드롭다운 목록을 클릭하여 해당 기준을 참조하는 전체 활동 목록을 봅니다. 활동 링크를 클릭하여 편집할 활동을 열 수 있습니다.

![알고리즘 사용 탭](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>현재 [!UICONTROL 알고리즘 사용] 기능은 Recommendations 활동에서만 지원됩니다. 이 기능은 현재 오퍼로 [권장 사항을 포함하는 A/B 테스트, 자동 할당, 자동 Target 및 경험 타깃팅(XT) 활동에 대해 지원되지 않습니다](/help/c-recommendations/recommendations-as-an-offer.md).
