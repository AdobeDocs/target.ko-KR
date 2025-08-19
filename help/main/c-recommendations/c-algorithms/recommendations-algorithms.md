---
keywords: 권장 사항 알고리즘;모델 교육;모델 제공;컨텐츠 전달;항목 기반;사용자 기반;인기도 기반;장바구니 기반;사용자 지정 기준
description: 모델 교육 및 모델 서비스를 포함하여  [!DNL Target Recommendations]에서 사용되는 알고리즘에 대해 알아봅니다.
title: Target의 추천 알고리즘에 숨겨진 과학에 대한 내용은 어디에서 확인할 수 있습니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
mini-toc-levels: 2
exl-id: c156952b-8eda-491d-a68e-d3d09846f640
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2739'
ht-degree: 0%

---

# Target의 추천 알고리즘에 숨겨진 과학

모델 교육 및 모델 제공 프로세스에 대한 논리 및 수학 세부 정보를 포함하여 [!DNL Adobe Target Recommendations]에서 사용되는 알고리즘에 대한 심층적인 설명입니다.

모델 교육은 [!DNL Adobe Target] 학습 알고리즘에서 권장 사항을 생성하는 프로세스입니다. 모델 제공은 [!DNL Target]이(가) 사이트 방문자에게 권장 사항을 제공하는 방법입니다(콘텐츠 제공이라고도 함).

[!DNL Target]은(는) [!DNL Recommendations]에 다음과 같은 광범위한 유형의 알고리즘을 포함합니다.

* **항목 기반 알고리즘**: &quot;이 항목을 보거나 구입한 사람도 이 항목을 보거나 구입한 사람&quot;이라는 논리를 따르는 알고리즘을 포함합니다. 이러한 알고리즘은 [!UICONTROL Items with Similar Attributes] 알고리즘과 함께 포괄적 용어 항목-항목 공동 작업 필터링으로 그룹화됩니다.

* **사용자 기반 알고리즘**: [!UICONTROL Recently Viewed] 및 [!UICONTROL Recommended for You] 알고리즘을 포함합니다.

* **인기도 기반 알고리즘**: 웹 사이트에서 가장 많이 본 항목 또는 가장 많이 구매한 항목, 범주 또는 항목 특성별로 가장 많이 본 항목 또는 가장 많이 구매한 항목을 반환하는 알고리즘을 포함합니다.

* **장바구니 기반 알고리즘**: &quot;이러한 항목을 보거나 구입한 사람, 해당 항목을 보거나 구입한 사람&quot;이라는 논리를 사용하여 다중 항목 기반 권장 사항을 포함합니다.

* **사용자 지정 기준**: [!DNL Target]에 업로드된 사용자 지정 파일에 따른 권장 사항을 포함합니다.

>[!NOTE]
>
>각 알고리즘 유형 및 개별 알고리즘에 대한 일반 정보는 [권장 사항 키를 기반으로 권장 사항 만들기](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오.

위에 나열된 알고리즘 중 다수는 하나 또는 여러 키의 존재를 기반으로 합니다. 이러한 키는 콘텐츠 전달 시 (권장 사항이 작성될 때) 유사한 항목을 검색하는 데 사용됩니다. 고객이 지정한 키에는 사용자가 보고 있는 현재 항목, 마지막으로 본 항목 또는 구매한 항목, 가장 많이 본 항목, 현재 카테고리 또는 해당 방문자의 즐겨찾기 카테고리가 포함될 수 있습니다. 장바구니 기반 또는 사용자 기반 권장 사항과 같은 기타 알고리즘은 암시적 키(고객이 구성할 수 없음)를 사용합니다. 자세한 내용은 *권장 사항 키*, [권장 사항 키를 기반으로 권장 사항 만들기](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys)를 참조하십시오. 단, 이러한 키는 모델 제공 시간에만 관련이 있습니다(컨텐츠 전달). 이러한 키는 &quot;오프라인&quot; 또는 모델 교육 시간 논리에 영향을 주지 않습니다.

다음 섹션은 위에서 설명한 알고리즘 유형과 약간 다른 방식으로 알고리즘을 그룹화합니다. 다음의 그룹화는 모델 훈련 로직의 유사성을 기준으로 한다.

## 품목-품목 협업 필터링

알고리즘 에는 다음이 포함됩니다.

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

항목-항목 공동 작업 필터링 권장 사항 알고리즘은 많은 사용자의 행동 패턴을 사용하여(따라서 공동 작업) 주어진 항목에 유용한 권장 사항을 제공해야 한다는 아이디어(예: 권장할 가능한 항목의 카탈로그를 필터링해야 함)에 기반을 둡니다. [공동 작업 필터링](https://en.wikipedia.org/wiki/Collaborative_filtering)의 일반적인 범위에 속하는 다양한 알고리즘이 있지만 이러한 알고리즘은 일반적으로 행동 데이터 소스를 입력으로 사용합니다. [!DNL Target Recommendations]에서 이러한 입력은 사용자가 항목을 고유 보고 구매한 것입니다.

&quot;이 항목을 보거나 구매한 사람 및 이 항목을 보거나 구매한 사람&quot; 알고리즘의 목표는 모든 항목 쌍 간의 유사성 s(A,B)를 계산하는 것입니다. 주어진 항목 A에 대해 상위 권장 사항은 그 유사성 s(A,B)별로 순서가 지정됩니다.

이러한 유사성의 한 예는 항목 간의 공동 발생입니다. 두 항목을 모두 구매한 사용자 수의 간단한 카운트입니다. 직관적이긴 하지만, 이러한 지표는 인기 항목을 추천하는 것에 치우쳐 있다는 점에서 순진하다. 예를 들어, 식료품 retailer에서 대부분의 사람들이 빵을 구매한다면, 빵은 모든 품목과 높은 동시성을 가지지만, 반드시 좋은 추천은 아니다. [!DNL Target]은(는) 대신 로그 우도비(LLR)라고 하는 더 정교한 유사성 지표를 사용합니다. 이 양은 두 문항 A와 B의 동시 발생 확률이 서로 미발생 확률과 매우 다를 때 크다. 자세한 내용을 보려면 [!UICONTROL People Who Viewed This, Bought That] 알고리즘의 사례를 고려하십시오. B를 구매했을 확률이 A를 보았는지 여부와 관계없이 *not*&#x200B;일 때 LLR 유사도가 크다.

예를 들어

![열람한/구매한 알고리즘에 대한 수식](assets/formula.png)

그런 다음 항목 B는 항목 A와 함께 권장되지 않습니다. 이 로그 가능성 비율 유사성 계산에 대한 전체 세부 정보가 [이 PDF에서](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)에 제공됩니다.

실제 알고리즘 구현의 논리 흐름은 다음 도식도에 나와 있습니다.

![조회/구매 알고리즘의 도식 다이어그램](assets/diagram1.png)

이러한 단계의 세부 사항은 다음과 같습니다.

* **입력 데이터**: [Target 구현](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 또는 [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}에서 수집된 방문자 보기 및 구매 형식의 행동 데이터입니다.

* **모델 교육**:

   * **데이터 정리 및 샘플링**: N일 전환 확인이 있는 알고리즘의 경우 동작 데이터가 먼저 N일 데이터만 포함하도록 필터링됩니다. 그런 다음 컬렉션 규칙 및 전역 제외가 적용되어 권장되지 않아야 하는 모든 항목을 제거합니다. 마지막으로 1,000개 이상의 항목과 상호 작용한 모든 방문자는 사용 데이터를 1,000개 항목으로만 샘플링했습니다.
   * **항목 유사성 계산**: 이 유사성 점수로 모든 후보 항목 쌍 간의 로그 가능성 비율 유사성과 항목의 순위 쌍을 계산하는 핵심 계산 단계입니다.
   * **오프라인 필터링**: 마지막으로 적용 가능한 모든 동적 필터가 적용됩니다(예: 동적 범주 제외). 이 단계 후에는 사전 계산된 권장 사항이 전역적으로 캐시되어 제공할 수 있습니다.

* **모델 제공**: 권장 사항 콘텐츠가 [!DNL Target]의 [글로벌 &quot;Edge&quot; 네트워크에서 전달됩니다](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934). [!DNL Target]에 mbox 요청을 하고 권장 사항 콘텐츠를 페이지로 전달해야 한다고 결정되면 권장 사항 알고리즘에 대한 적절한 [항목 키](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys)에 대한 요청을 요청에서 구문 분석하거나 사용자 프로필에서 조회한 다음 이전 단계에서 계산된 권장 사항을 검색하는 데 사용합니다. 적절한 [디자인](/help/main/c-recommendations/c-design-overview/create-design.md)이 렌더링되기 전에 현재 동적 필터가 추가로 적용됩니다.

## 콘텐츠 유사성

알고리즘 포함:

* [!UICONTROL Items with Similar Attributes]

이러한 유형의 알고리즘에서 두 항목은 이름과 텍스트 설명이 의미상 유사하면 관련이 있는 것으로 간주됩니다. 행동 데이터 소스를 사용해야 하는 대부분의 권장 사항 알고리즘과 달리, 콘텐츠 유사성 알고리즘은 제품 카탈로그의 메타데이터를 사용하여 항목 간의 유사성을 도출합니다. 따라서 [!DNL Target]은(는) 동작 데이터가 수집되지 않은 이른바 &quot;콜드 스타트&quot; 시나리오에서 권장 사항을 유도할 수 있습니다(예: [!DNL Target] 활동의 시작 시).

[!DNL Target]의 콘텐츠 유사성 알고리즘의 모델 서비스 제공 및 콘텐츠 전달 측면은 다른 항목 기반 알고리즘과 동일하지만 모델 교육 단계는 크게 다르며 다음 다이어그램에 표시된 대로 일련의 자연어 처리 및 전처리 단계를 포함합니다. 유사도 계산의 핵심은 카탈로그의 각 항목을 나타내는 수정된 tf-idf 벡터의 코사인 유사도를 사용하는 것이다.

![콘텐츠 유사성 프로세스의 흐름을 보여 주는 다이어그램](assets/diagram2.png)

이러한 단계의 세부 사항은 다음과 같습니다.

* **입력 데이터**: 앞에서 설명한 대로 이 알고리즘은 순전히 카탈로그 데이터([!DNL Target]카탈로그 피드, 엔터티 API 또는 페이지 업데이트를 통해 [에 수집됨](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}을(를) 기반으로 합니다.

* **모델 교육**:

   * **특성 추출**: 일반 정적 필터, 카탈로그 규칙 및 전역 제외를 적용한 후 이 알고리즘은 엔터티 스키마에서 관련 텍스트 필드를 추출합니다. [!DNL Target]은(는) 엔터티 특성에서 이름, 메시지 및 범주 필드를 자동으로 사용하며 사용자 지정 [엔터티 특성](/help/main/c-recommendations/c-products/entity-attributes.md)에서 문자열 필드를 추출하려고 합니다. 이 프로세스는 해당 필드에 대한 값의 대부분을 숫자, 날짜 또는 부울로 구문 분석할 수 없도록 함으로써 수행됩니다.
   * **어간 및 정지어 제거**: 텍스트 유사성을 보다 정확하게 일치시키려면 항목의 의미(예: &quot;was&quot;, &quot;is&quot;, &quot;and&quot; 등)를 크게 변경하지 않는 매우 일반적인 &quot;정지어&quot; 단어를 제거하는 것이 좋습니다. 마찬가지로 형태소 분석이란 동일한 의미(예: &quot;connect&quot;, &quot;connecting&quot;, &quot;connection&quot;은 모두 동일한 루트 단어를 가지고 있습니다. &quot;connect&quot;)를 가진 루트 단어에 접미사가 다른 단어를 축소하는 과정을 말합니다. [!DNL Target]이(가) Snowball Stemer를 사용합니다. [!DNL Target]은(는) 먼저 자동 언어 검색을 수행하고 최대 50개 언어에 대해 단어 제거를 중단하고 18개 언어에 대해 어간을 분석할 수 있습니다.
   * **n그램 만들기**: 이전 단계 후에 각 단어는 토큰으로 처리됩니다. 토큰의 연속적인 시퀀스를 하나의 토큰으로 결합하는 과정을 n-그램 생성이라고 한다. [!DNL Target]의 알고리즘은 최대 2g까지 고려합니다.
   * **tf-idf 계산**: 다음 단계에서는 항목 설명에 있는 토큰의 상대적 중요도를 반영하도록 tf-idf 벡터를 만듭니다. 항목 i의 각 토큰/용어 t에 대해 다음을 포함하는 카탈로그 D의 |D| 항목 빈도 TF(t, i)라는 용어와 문서 빈도 DF(t, D)라는 용어가 먼저 계산됩니다(항목 i에 용어가 나타나는 횟수). 본질적으로, 토큰 t가 존재하는 항목의 수. 그러면 tf-idf 측정값이

     ![tf-idf 측정값을 표시하는 수식](assets/formula2.png)

     [!DNL Target]은(는) Apache Spark의 *tf-idf* 기능 구현을 사용합니다. 후드에서 각 토큰을 218개 토큰 공간으로 해시합니다. 이 단계에서는 [criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity)에 지정된 설정을 기반으로 각 벡터의 용어 빈도를 조정하여 고객이 지정한 특성 부스팅 및 매립도 적용합니다.

   * **항목 유사성 계산**: 최종 항목 유사성 계산은 근사 코사인 유사성을 사용하여 수행됩니다. 벡터 tA와 tB가 있는 두 항목 *A* 및 *B*&#x200B;의 경우 코사인 유사성은 다음과 같이 정의됩니다.

     ![항목 유사성 계산을 보여 주는 수식](assets/formula3.png)

     모든 N x N 항목 간의 유사성을 계산하는 데 상당한 복잡성을 방지하기 위해 *tf-idf* 벡터를 최대 500개의 항목만 포함하도록 잘린 다음 이 잘린 벡터 표현을 사용하여 항목 간의 코사인 유사성을 계산합니다. 이 접근법은 국소성 민감 해싱과 같은 다른 근사 최근접 이웃(ANN) 기법에 비해 희소 벡터 유사성 계산에 더 강건하다는 것을 입증한다.

   * **모델 제공**: 이 프로세스는 이전 섹션에서 설명한 항목-항목 공동 작업 필터링 기술과 동일합니다.

## 다중 키 권장 사항

알고리즘 에는 다음이 포함됩니다.

* 장바구니 기반 권장 사항
* [!UICONTROL Recommended For You]

권장 사항 알고리즘 집합 [!DNL Target]에 추가된 가장 최근 항목은 [!UICONTROL Recommended For You]과(와) 일련의 장바구니 기반 권장 사항 알고리즘입니다. 두 유형의 알고리즘 모두 협업 필터링 기법을 사용하여 개별 항목 기반 추천을 형성합니다. 그런 다음, 서비스 시 사용자의 검색 기록([!UICONTROL Recommended For You]의 경우)에 있는 여러 항목 또는 사용자의 현재 장바구니( 장바구니 기반 권장 사항의 경우)를 사용하여 이러한 항목 기반 권장 사항을 검색한 다음, 병합하여 최종 권장 사항 목록을 만듭니다. 개인화된 추천 알고리즘의 다양한 유형이 존재한다는 점을 참고하십시오. 다중 키 알고리즘의 선택은 방문자가 검색 기록을 가지고 있고 최신 방문자 행동에 대응하기 위해 권장 사항을 업데이트할 수 있는 직후에 권장 사항을 사용할 수 있음을 의미합니다.

이러한 알고리즘은 항목 기반 권장 사항 섹션에 설명된 기본 공동 작업 필터링 기술을 기반으로 하지만 하이퍼파라미터 튜닝을 통합하여 항목 간 최적의 유사성 지표를 결정합니다. 이 알고리즘은 각 사용자에 대해 행동 데이터를 시간별로 분할하고, 사용자가 나중에 보거나 구매하는 항목을 예측하려고 시도하는 동안 이전 데이터에 대한 추천 모델을 교육합니다. 그런 다음 최적의 [평균 평균 정밀도]&#x200B;(https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval))를 생성하는 유사성 지표가 선택됩니다.

다음 다이어그램에는 모델 교육 및 채점 단계의 논리가 나와 있습니다.

![모델 교육 및 채점 단계의 논리를 보여 주는 다이어그램](assets/diagram3.png)

이러한 단계의 세부 사항은 다음과 같습니다.

* **입력 데이터**: 항목-항목 공동 작업 필터링(CF) 방법과 동일합니다. [!UICONTROL Both Recommended For You] 및 장바구니 기반 알고리즘에서는 [Target 구현](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 또는 [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}에서 수집된 사용자의 보기 및 구매 형식의 행동 데이터를 사용합니다.

* **모델 교육**:

   * **데이터 정리 및 샘플링**: 이는 다시 공동 작업 필터링 방법과 동일합니다. 전환 확인 기간은 동작 데이터를 적절한 날짜 범위로 필터링한 다음 카탈로그 규칙 및 전역 제외를 적용하는 데 적용됩니다. 1,000개 이상의 항목과 상호 작용한 방문자는 가장 최근의 1,000개 사용법만 고려합니다.
   * **테스트 분할**: 각 사용자에 대한 사용량을 시간별로 분할하고 사용량의 처음 80%는 교육 데이터에 할당하며 나머지 20%는 테스트 데이터에 할당됩니다.
   * **항목 유사성 모델 교육**: 핵심 항목 유사성 계산은 후보 항목 벡터가 구성되는 방식에서 [!UICONTROL Recommended For You] 및 장바구니 기반 알고리즘에 대해 다릅니다. [!UICONTROL Recommended For You]의 경우 항목 벡터에는 차원 NUsers가 있습니다. 여기서 각 항목은 항목의 해당 사용자에 대한 암시적 등급의 합을 나타냅니다. 항목의 구매 횟수에는 항목 보기의 2배 가중치가 제공됩니다. 장바구니 기반 권장 사항의 경우 항목 벡터에는 이진 항목이 있습니다. 세션 내 비헤이비어만 고려하는 경우 모든 세션에 대해 새 항목이 있습니다. 그렇지 않으면 모든 방문자에 대해 이 항목 벡터에 항목이 있습니다.

  트레이닝 단계는 다음과 같이 정의된 LLR 유사성([여기에서 논의됨](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), 코사인 유사성(이전에 정의됨) 및 정규화된 L2 유사성 등 여러 유형의 벡터 유사성을 계산합니다.

  ![교육 계산을 보여 주는 수식](assets/formula4.png)

   * **항목 유사성 모델 평가**: 모델 평가는 이전 단계에서 생성된 권장 사항을 취하고 테스트 데이터 집합에 대한 예측을 수행하여 수행됩니다. 온라인 채점 단계는 테스트 데이터 세트에서 각 사용자의 항목 사용을 시간 순으로 정렬한 다음, 후속 보기 및 구매를 예측하기 위해 정렬된 항목 하위 집합에 대해 100개의 권장 사항을 만드는 방식으로 모방됩니다. 이러한 권장 사항의 품질을 평가하는 데 정보 검색 지표인 [평균 정밀도]&#x200B;(https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval))가 사용됩니다. 이 지표는 권장 사항 순서를 고려하며 권장 사항 목록 위에 있는 관련 항목을 선호합니다. 이는 등급 시스템의 중요한 속성입니다.
   * **모델 선택**: 오프라인 평가 후 평균 평균 정밀도가 가장 높은 모델이 선택되고 모든 개별 항목 권장 사항이 계산됩니다.
   * **오프라인 필터링**: 모델 교육의 마지막 단계는 적용 가능한 동적 필터를 적용하는 것입니다. 이 단계 후에는 사전 계산된 권장 사항이 전역적으로 캐시되어 제공할 수 있습니다.

* **모델 제공**: 추천 제공에 검색할 단일 키를 지정한 후 비즈니스 규칙을 적용하는 이전 알고리즘과 달리 [!UICONTROL Recommended for You] 및 장바구니 기반 알고리즘에서는 보다 복잡한 런타임 프로세스를 사용합니다.

   * **다중 키 검색 및 병합**: 장바구니 기반 권장 사항의 경우 장바구니에 전달된 최대 10개의 항목이 검색 키로 간주되며 각 항목의 권장 사항은 동일한 가중치를 갖습니다. [!UICONTROL Recommended for You]의 경우 마지막으로 본 고유 항목 5개와 마지막으로 구매한 고유 항목 5개가 검색을 위한 키로 간주되며, 구매한 항목에서 발생한 권장 사항은 본 항목에서 발생한 권장 사항보다 두 배 가중치가 적용됩니다. 권장 사항을 병합할 때 항목이 권장 사항의 여러 개별 목록에 나타나는 경우 가중치가 적용된 유사성 점수가 추가됩니다. 이 단계의 최종 권장 사항 목록은 내림차순으로 순위가 매겨진 재가중 권장 사항의 병합된 목록입니다.
   * **필터링**: 다음으로 이전에 본 항목 및/또는 구매한 항목 제거와 같은 필터링 규칙과 기타 동적 비즈니스 규칙이 적용됩니다.

이러한 프로세스는 방문자가 항목 A를 보고 항목 B를 구매한 다음 이미지에 나와 있습니다. 개별 권장 사항은 각 항목 레이블 아래에 표시된 오프라인 유사성 점수로 검색됩니다. 검색 후 권장 사항은 가중치가 적용된 유사성 점수와 병합됩니다. 마지막으로, 고객이 이전에 본 항목과 구매한 항목을 필터링해야 한다고 지정한 시나리오에서는 필터링 단계에서 권장 사항 목록에서 항목 A와 B가 제거됩니다.

![다중 키 알고리즘 처리를 보여 주는 다이어그램](assets/diagram4.png)

## 인기도 기반

알고리즘 에는 다음이 포함됩니다.

* [!UICONTROL Most Viewed Across the Site]
* [!UICONTROL Most Viewed by Category]
* [!UICONTROL Most Viewed by Item Attribute]
* [!UICONTROL Top Sellers Across the Site]
* [!UICONTROL Top Sellers by Category]
* [!UICONTROL Top Sellers by Item Attribute]

[!DNL Target]은(는) 가장 많이 본 항목과 웹 사이트 또는 항목 특성이나 카테고리별로 분류된 가장 많이 판매된 항목 모두에 대한 인기도 기반 알고리즘을 제공합니다. 인기도 기반 알고리즘 은 주어진 시간대에서 해당 항목을 보거나 구매한 세션 수에 따라 항목의 등급을 지정합니다.

이러한 모든 알고리즘은 항목을 보고 구매한 총 세션 수가 시간별 및 일별 해상도 모두에서 기록되는 집계된 행동 데이터를 결합합니다. 그런 다음 개별 알고리즘은 고객이 구성한 전환 확인 기간에 대해 가장 많이 본 항목 또는 가장 많이 구매한 항목을 찾습니다.

개별 알고리즘 뉘앙스는 다음과 같습니다.

* [!UICONTROL Most Viewed Across the Site] 및 [!UICONTROL Top Sellers Across the Site]은(는) 이러한 항목을 각각 보거나 구입한 세션의 집계 수를 기준으로 항목의 등급을 지정합니다. 출력은 권장 항목의 단일(키가 없는) 목록입니다.
* 카테고리/항목 속성별 가장 많이 본 항목/최상위 판매자는 이러한 항목이 본 세션이나 구매된 세션의 집계 카운트로 항목이 정렬되는 권장 사항이지만 항목 카테고리 또는 특정 항목 속성별로 그룹화됩니다. 출력은 카테고리 값 또는 항목 속성 값을 기준으로 처리된 권장 항목 목록입니다.

## 최근에 본 항목

최근에 본 권장 사항 알고리즘을 사용하면 권장 사항의 세션 내 개인화를 수행할 수 있습니다. 이 알고리즘에는 오프라인 &quot;모델 교육&quot;이 필요하지 않습니다. 대신 [!DNL Target]은(는) 고유한 [방문자 프로필](/help/main/c-target/c-visitor-profile/visitor-profile.md)을(를) 사용하여 특정 세션에서 본 항목의 실행 목록을 유지하고 이러한 항목을 권장 사항 활동에 표시할 수 있습니다. 이를 통해 추천과 다음 페이지 개인화에 대한 실시간 업데이트를 수행할 수 있습니다.

## 사용자 지정 기준

사용자 지정 기준을 사용하면 고객이 [자신의 권장 사항을  [!DNL Target]](/help/main/c-recommendations/c-algorithms/recommendations-csv.md)에 업로드할 수 있으므로 중요한 유연성을 제공하고 &quot;고유한 모델을 가져옴&quot; 기능을 사용할 수 있습니다. 사용자 지정 기준은 [!UICONTROL Item-Based] 권장 사항의 &quot;오프라인 교육&quot; 부분을 대체하지만, 권장 사항 검색에 단일 키를 사용하고 비즈니스 규칙/필터를 적용한다는 점에서 온라인 콘텐츠 게재 단계 동안 항목 기반 권장 사항 알고리즘과 유사하게 동작합니다.
