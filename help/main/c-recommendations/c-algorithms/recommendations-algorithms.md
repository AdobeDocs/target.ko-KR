---
keywords: 권장 사항 알고리즘;모델 교육;모델 제공;컨텐츠 전달;항목 기반;사용자 기반;인기도 기반;장바구니 기반;사용자 지정 기준
description: 모델 교육 및 모델 서비스를 포함하여 [!DNL Target Recommendations]에서 사용되는 알고리즘에 대해 알아봅니다.
title: Target의 추천 알고리즘에 숨겨진 과학
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
mini-toc-levels: 2
exl-id: c156952b-8eda-491d-a68e-d3d09846f640
TQID: 'https://experienceleague.adobe.com/goYsorjFUweT4Aw0XvzQSeiqON7orDcLntZaJliqGl4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '2755'
ht-degree: 0%
---
# Target의 추천 알고리즘에 숨겨진 과학 {#recommendations-algorithms}

>[!BEGINSHADEBOX]

**이 페이지에서:** 모델 교육 및 모델 서비스에 대한 논리 및 수학 세부 정보를 포함하여 [!DNL Adobe Target Recommendations]의 알고리즘이 작동하는 방식을 알아봅니다.

>[!ENDSHADEBOX]

모델 교육은 [!DNL Adobe Target] 학습 알고리즘이 권장 사항을 생성하는 프로세스입니다. 모델 제공(콘텐츠 전달)은 [!DNL Target]에서 사이트 방문자에게 이러한 권장 사항을 제공하는 방법입니다.

[!DNL Target]은(는) [!DNL Recommendations]에서 다음 유형의 알고리즘을 제공합니다.

* **항목 기반 알고리즘**: &quot;이 항목을 보거나 구입한 사람도 이 항목을 보거나 구입한 사람&quot;이라는 논리를 따르십시오. 이러한 알고리즘은 항목-항목 공동 작업 필터링이라는 용어로 그룹화됩니다. 이 형식에는 **[!UICONTROL 비슷한 특성을 가진 항목]** 알고리즘도 포함됩니다.

* **사용자 기반 알고리즘**: **[!UICONTROL 최근에 본 항목]** 및 **[!UICONTROL 권장]** 알고리즘을 포함합니다.

* **인기도 기반 알고리즘**: 웹 사이트 전체, 범주 또는 항목 특성별로 가장 많이 본 항목 또는 가장 많이 구매한 항목을 반환합니다.

* **장바구니 기반 알고리즘**: &quot;이러한 항목을 보거나 구매한 사람도 해당 항목을 보거나 구매한 사람&quot;이라는 논리로 여러 항목을 추천합니다.

* **사용자 지정 기준**: [!DNL Target]에 업로드된 사용자 지정 파일을 권장 사항의 소스로 사용합니다.

각 알고리즘 유형 및 알고리즘에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오.

이러한 알고리즘 중 대부분은 [!DNL Target]이(가) 유사한 항목을 검색하기 위해 콘텐츠 전달 시(권장 사항이 있을 때) 사용하는 하나 이상의 키에 의존합니다. 고객이 지정한 키는 방문자가 보고 있는 현재 항목, 마지막으로 본 항목 또는 구매한 항목, 가장 많이 본 항목, 현재 카테고리 또는 방문자의 즐겨찾기 카테고리가 될 수 있습니다. 장바구니 기반 및 사용자 기반 알고리즘과 같은 다른 알고리즘에서는 고객이 구성할 수 없는 암시적 키를 사용합니다. 자세한 내용은 [추천 키](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys)를 참조하세요.

키는 모델 제공 시간(콘텐츠 전달)에만 적용됩니다. 오프라인 모델 교육 논리에는 영향을 주지 않습니다.

다음 섹션은 알고리즘을 모델 교육 논리의 유사성에 따라 그룹화하므로, 그룹은 위의 유형과 약간 다릅니다.

## 품목-품목 협업 필터링

알고리즘 에는 다음이 포함됩니다.

* **[!UICONTROL 이 항목을 보고 다른 항목도 본 사람]**
* **[!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]**
* **[!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]**

항목-항목 공동 작업 필터링 알고리즘은 많은 사용자의 행동 패턴을 사용하여(따라서 공동 작업) 주어진 항목과 관련된 항목을 추천하고, 이는 가능한 항목의 카탈로그를 필터링합니다. 많은 다른 알고리즘들이 공동 필터링의 일반적인 범위에 속하며, 이들 모두는 행동적 데이터를 입력으로 사용한다. [!DNL Target Recommendations]에서 이러한 입력은 사용자가 항목을 고유 보고 구매한 것입니다.

&quot;이 항목을 보거나 구매한 사람 및 이 항목을 보거나 구매한 사람&quot; 알고리즘의 목표는 모든 항목 쌍 간의 유사성 s(A,B)를 계산하는 것입니다. 주어진 항목 A의 경우, 상위 권장 사항은 유사성 s(A,B)로 순서가 정해진 항목입니다.

유사성의 한 가지 예는 항목 간의 동시 발생입니다(두 항목을 모두 구매한 사용자 수). 이 지표는 인기 있는 항목을 추천하는 데 편향되었기 때문에 직관적이지만 순진합니다. 예를 들어 대부분의 사람들이 빵을 구매하는 식료품 retailer에서 빵은 모든 품목과 동시다발성이 높지만 반드시 좋은 추천은 아니다. [!DNL Target]은(는) 대신 로그 우도비(LLR)를 사용합니다. 이 수량은 두 문항 A와 B의 동시 발생 확률과 그렇지 않은 확률이 매우 다를 때 크다. 예를 들어, **[!UICONTROL 본 사람, 구매 대상]** 알고리즘의 경우 B를 구매한 사람이 A를 보았는지 여부와 관계없이 *그렇지 않음*&#x200B;일 확률이 높을 때 LLR 유사성이 큽니다.

다음과 같은 경우에는 품목 B를 품목 A와 함께 사용하지 않는 것이 좋습니다.

![열람한/구매한 알고리즘에 대한 수식](/help/main/c-recommendations/c-algorithms/assets/formula.png)

로그 가능성 비율 유사성 계산에 대한 자세한 내용은 [이 PDF](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)을 참조하세요.

다음 도식 다이어그램은 알고리즘 구현의 논리적 흐름을 보여 줍니다.

![본/산 알고리즘의 도식 다이어그램](/help/main/c-recommendations/c-algorithms/assets/diagram1.png)

단계는 다음과 같습니다.

* **입력 데이터**: [Target 구현](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 또는 [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}에서 수집된 방문자 보기 및 구매 형식의 동작 데이터입니다.

* **모델 교육**:

  * **데이터 정리 및 샘플링**: N일 전환 확인이 있는 알고리즘의 경우 동작 데이터가 먼저 N일 데이터만 포함하도록 필터링됩니다. 그런 다음 컬렉션 규칙 및 전역 제외가 적용되어 권장되지 않아야 하는 모든 항목을 제거합니다. 마지막으로 1,000개 이상의 항목과 상호 작용한 방문자의 사용 데이터를 1,000개 항목으로 샘플링합니다.
  * **항목 유사성 계산**: 핵심 계산 단계입니다. [!DNL Target]은(는) 모든 후보 항목 쌍 간의 로그 가능성 비율 유사성을 계산하고 이 점수로 쌍의 순위를 지정합니다.
  * **오프라인 필터링**: 적용 가능한 모든 동적 필터가 적용됩니다(예: 동적 범주 제외). 그런 다음 미리 계산된 권장 사항이 전역적으로 캐시되어 제공할 준비가 됩니다.

* **모델 제공**: [!DNL Target]의 [전역 &quot;Edge&quot; 네트워크](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934)에서 권장 사항이 전달됩니다. [!DNL Target]에게 mbox 요청을 하고 권장 사항 콘텐츠를 페이지에 전달해야 한다고 판단되면 알고리즘이 필요로 하는 [항목 키](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys)를 요청에서 구문 분석하거나 방문자 프로필에서 조회합니다. [!DNL Target]은(는) 이 키를 사용하여 이전 단계에서 계산된 권장 사항을 검색하고 추가 동적 필터를 적용한 다음 적절한 [디자인](/help/main/c-recommendations/c-design-overview/create-design.md)을(를) 렌더링합니다.

## 콘텐츠 유사성

알고리즘 포함:

* **[!UICONTROL 비슷한 특성을 가진 항목]**

이 알고리즘에서는 두 항목의 이름과 텍스트 설명이 의미상 유사한 경우 두 항목이 관련됩니다. 행동 데이터가 필요한 대부분의 권장 사항 알고리즘과 달리, 콘텐츠 유사성 알고리즘은 제품 카탈로그 메타데이터에서 항목 간의 유사성을 파생합니다. 따라서 [!DNL Target]은(는) 아직 동작 데이터가 수집되지 않은 이른바 &quot;콜드 스타트&quot; 시나리오에서 권장 사항을 제공할 수 있습니다(예: [!DNL Target] 활동의 시작 시).

콘텐츠 유사성 알고리즘에 대한 모델 서비스 및 콘텐츠 전달은 다른 항목 기반 알고리즘의 모델과 동일합니다. 모델 교육은 매우 다릅니다. 다음 다이어그램과 같이 일련의 자연어 처리 및 전처리 단계가 포함되어 있습니다. 유사도 계산의 핵심은 카탈로그의 각 항목을 나타내는 수정된 tf-idf 벡터의 코사인 유사도이다.

![콘텐츠 유사성 프로세스의 흐름을 보여 주는 다이어그램](/help/main/c-recommendations/c-algorithms/assets/diagram2.png)

단계는 다음과 같습니다.

* **입력 데이터**: 이 알고리즘은 [카탈로그 피드, 엔터티 API 또는 페이지 업데이트를 통해 [!DNL Target]에 수집된 카탈로그 데이터만 사용합니다](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

* **모델 교육**:

  * **특성 추출**: 정적 필터, 카탈로그 규칙 및 전역 제외가 적용된 후 알고리즘에서 엔터티 스키마에서 관련 텍스트 필드를 추출합니다. [!DNL Target]은(는) 엔터티 특성의 이름, 메시지 및 범주 필드를 자동으로 사용합니다. 또한 사용자 지정 [엔터티 특성](/help/main/c-recommendations/c-products/entity-attributes.md)에서 문자열 필드를 추출하려고 합니다. 필드는 값의 대부분을 숫자, 날짜 또는 부울로 구문 분석할 수 없는 경우 문자열 필드로 처리됩니다.
  * **어간 및 정지어 제거**: 텍스트 유사성을 보다 정확하게 일치시키기 위해 [!DNL Target]은(는) 항목의 의미를 크게 변경하지 않는 매우 일반적인 &quot;정지어&quot; 단어(예: &quot;was&quot;, &quot;is&quot;, &quot;and&quot;)를 제거합니다. 어간 분석에서는 동일한 의미(예: &quot;connect&quot;, &quot;connecting&quot; 및 &quot;connection&quot;은 모두 &quot;connect&quot; 루트를 가짐)를 가진 루트 단어에 접미사가 다른 단어를 줄입니다. [!DNL Target]이(가) Snowball Stemer를 사용합니다. 자동 언어 감지를 먼저 수행하고, 최대 50개 언어에 대한 정지어 제거 및 18개 언어에 대한 스테밍 수행이 가능하다.
  * **n그램 만들기**: 이전 단계 후에 각 단어는 토큰으로 처리됩니다. 토큰의 연속적인 시퀀스를 단일 토큰으로 결합하는 것을 n-그램 생성이라고 한다. [!DNL Target]은(는) 최대 2그램을 고려합니다.
  * **tf-idf 계산**: 다음 단계에서는 항목 설명에 있는 토큰의 상대적 중요도를 반영하는 tf-idf 벡터를 만듭니다. 항목 i의 각 토큰 또는 용어 t에 대해 를 포함하는 카탈로그 D에서 항목 |D|개, [!DNL Target]은(는) 먼저 항목 i에 용어가 나타나는 횟수인 용어 빈도 TF(t, i)와 토큰 t가 있는 항목 수인 문서 빈도 DF(t, D)를 계산합니다. tf-idf 측정값은 다음과 같습니다.

    ![tf-idf 측정값을 표시하는 수식](/help/main/c-recommendations/c-algorithms/assets/formula2.png)

    [!DNL Target]은(는) Apache Spark의 *tf-idf* 기능 구현을 사용합니다. 이 구현은 각 토큰을 2<sup>18</sup> 토큰 공간으로 해시합니다. 이 단계에서는 각 벡터의 용어 빈도를 조정하여 [criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity)에 지정된 속성 부스팅과 매립도 적용합니다.

  * **항목 유사성 계산**: 최종 항목 유사성은 근사 코사인 유사성으로 계산됩니다. 벡터 tA와 tB가 있는 두 항목 *A* 및 *B*&#x200B;의 경우 코사인 유사성은 다음과 같이 정의됩니다.

    ![항목 유사성 계산을 보여 주는 수식](/help/main/c-recommendations/c-algorithms/assets/formula3.png)

    모든 N x N 항목 간의 유사성 계산이 상당히 복잡하지 않도록 하기 위해 *tf-idf* 벡터가 가장 큰 500개의 항목으로 잘리며 항목 간의 코사인 유사성이 잘린 표현에서 계산됩니다. 이 접근법은 국소성 민감 해싱과 같은 다른 근사 최근접 이웃(ANN) 기술보다 희소 벡터 유사성 계산에 더 강건하다.

* **모델 제공**: 이 프로세스는 이전 섹션에서 설명한 항목-항목 공동 작업 필터링에 대한 프로세스와 동일합니다.

## 다중 키 권장 사항

알고리즘 에는 다음이 포함됩니다.

* 장바구니 기반 권장 사항
* **[!UICONTROL 추천]**

**[!UICONTROL 추천됨]** 및 장바구니 기반 알고리즘에서는 공동 작업 필터링 기술을 사용하여 개별 항목 기반 추천을 구성합니다. 그런 다음 서비스 시 여러 항목이 이러한 항목 기반 권장 사항을 검색하는 키로 사용됩니다. 방문자의 검색 기록(**[!UICONTROL 사용자에게 권장]**&#x200B;용) 또는 방문자의 현재 장바구니({장바구니 기반 권장 사항)에 있는 항목입니다. 검색된 권장 사항이 병합되어 최종 목록이 됩니다. 다중 키 알고리즘을 사용하면 방문자의 검색 기록이 있는 즉시 권장 사항을 사용할 수 있으며 최신 방문자 행동을 반영하도록 업데이트됩니다.

이러한 알고리즘은 항목 기반 권장 사항 섹션에 설명된 협업 필터링 기술을 기반으로 하며, 하이퍼파라미터 튜닝을 사용하여 항목 간의 최적의 유사성 지표를 결정합니다. 이 알고리즘은 사용자가 나중에 보거나 구매하는 항목을 예측하려고 시도하는 동안 각 사용자의 행동 데이터를 시간 순으로 분할하고 이전 데이터에 대한 추천 모델을 교육합니다. 그런 다음 평균 평균 정밀도가 가장 높은 유사성 지표가 선택됩니다.

다음 다이어그램은 모델 교육 및 채점 단계의 논리를 보여 줍니다.

![모델 교육 및 채점 단계의 논리를 보여 주는 다이어그램](/help/main/c-recommendations/c-algorithms/assets/diagram3.png)

단계는 다음과 같습니다.

* **입력 데이터**: 항목-항목 공동 작업 필터링(CF) 방법과 동일합니다. **[!UICONTROL 사용자 추천]**&#x200B;과(와) 장바구니 기반 알고리즘 모두 [Target 구현](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 또는 [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}에서 수집된 사용자 보기 및 구매 형식의 행동 데이터를 사용합니다.

* **모델 교육**:

  * **데이터 정리 및 샘플링**: 공동 작업 필터링 방법과 동일합니다. 전환 확인 창은 동작 데이터를 적절한 날짜 범위로 필터링하며, 그런 다음 카탈로그 규칙 및 글로벌 제외가 적용됩니다. 1,000개 이상의 항목과 상호 작용한 방문자의 경우, 가장 최근의 1,000개 사용만 고려됩니다.
  * **테스트 분할 연습**: 각 사용자의 사용법이 시간 순으로 분할됩니다. 처음 80%는 훈련 데이터에 할당되고 나머지 20%는 테스트 데이터에 할당됩니다.
  * **항목 유사성 모델 교육**: 핵심 항목 유사성 계산은 후보 항목 벡터가 구성되는 방법에서 **[!UICONTROL 사용자에게 권장됨]**&#x200B;과(와) 장바구니 기반 간에 다릅니다. **[!UICONTROL 사용자 추천]**&#x200B;의 경우 항목 벡터에는 차원 NUsers가 있으며 각 항목은 사용자가 항목에 제공한 암시적 등급의 합계입니다. 구매 비중은 조회수의 2배입니다. 장바구니 기반 권장 사항의 경우 항목 벡터에는 이진 항목이 있습니다. 세션 내 비헤이비어만 고려하는 경우 모든 세션에 대해 하나의 항목이 있습니다. 그렇지 않으면 모든 방문자에 대해 하나의 항목이 있습니다.

    훈련 단계는 다음과 같이 정의된 LLR 유사성([PDF 참조](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), 코사인 유사성(이전에 정의됨) 및 정규화된 L2 유사성 등 여러 유형의 벡터 유사성을 계산합니다.

    ![교육 계산을 보여 주는 수식](/help/main/c-recommendations/c-algorithms/assets/formula4.png)

  * **항목 유사성 모델 평가**: 이전 단계에서 생성된 권장 사항은 테스트 데이터 집합에서 예측을 수행하여 평가됩니다. 온라인 채점 단계는 테스트 데이터 세트에서 각 사용자의 항목 사용을 시간순으로 정렬한 다음, 정렬된 항목 하위 집합에 대해 100개의 권장 사항을 만들어 후속 보기 및 구매를 예측하는 방식으로 모방됩니다. 이러한 권장 사항의 품질은 정보 검색 지표인 평균 정밀도 (Mean Average Precision)로 평가됩니다. 이 지표는 권장 사항 순서를 고려하며 목록에서 더 높은 관련 항목을 선호하며, 이는 등급 시스템의 중요한 속성입니다.
  * **모델 선택**: 오프라인 평가 후 평균 정밀도(Mean Average Precision)가 가장 높은 모델이 선택되고 모든 개별 항목 항목 권장 사항이 계산됩니다.
  * **오프라인 필터링**: 모델 교육의 마지막 단계는 적용 가능한 모든 동적 필터를 적용합니다. 그런 다음 미리 계산된 권장 사항이 전역적으로 캐시되어 제공할 준비가 됩니다.

* **모델 제공**: 검색할 단일 키를 지정한 다음 비즈니스 규칙을 적용하는 이전 알고리즘과 달리 **[!UICONTROL 사용자 추천]** 및 장바구니 기반에서는 보다 복잡한 런타임 프로세스를 사용합니다.

  * **다중 키 검색 및 병합**: 장바구니 기반 권장 사항의 경우 장바구니에서 전달된 최대 10개의 항목이 검색을 위한 키로 사용되며 각 키의 권장 사항에 동일한 가중치가 적용됩니다. **[!UICONTROL 추천 항목]**&#x200B;의 경우, 최근에 본 고유 항목 5개와 최근에 구매한 고유 항목 5개가 키로 사용되며, 구매한 항목에서 추천한 항목은 본 항목에서 추천한 항목보다 두 배 더 가중치가 적용됩니다. 권장 사항이 병합되면 여러 목록에 표시되는 항목의 가중치가 적용된 유사성 점수가 추가됩니다. 그 결과가 내림차순으로 순위가 매겨진 재가중치가 적용된 권장 사항의 병합된 목록입니다.
  * **필터링**: 이전에 본 항목 또는 구매한 항목 제거와 같은 필터링 규칙과 기타 동적 비즈니스 규칙이 적용됩니다.

다음 이미지는 항목 A를 보고 항목 B를 구매한 방문자에 대한 이러한 프로세스를 보여 줍니다. 개별 권장 사항은 각 항목 레이블 아래에 표시된 오프라인 유사성 점수로 검색된 다음 합산된 가중 유사성 점수와 병합됩니다. 마지막으로, 고객이 이전에 본 항목 및 구매한 항목을 필터링해야 한다고 지정한 경우 필터링 단계에서 권장 사항 목록에서 항목 A 및 B가 제거됩니다.

![다중 키 알고리즘 처리를 보여 주는 다이어그램](/help/main/c-recommendations/c-algorithms/assets/diagram4.png)

## 인기도 기반

알고리즘 에는 다음이 포함됩니다.

* **[!UICONTROL 사이트에서 가장 많이 본 항목]**
* **[!UICONTROL 범주별 가장 많이 본 항목]**
* **[!UICONTROL 가장 많이 본 항목 특성]**
* **[!UICONTROL 프로필 속성별로 가장 많이 조회한 항목]**
* **[!UICONTROL 사이트 전체 최상위 판매자]**
* **[!UICONTROL 범주별 최상위 판매자]**
* **[!UICONTROL 항목 특성별 최상위 판매자]**
* **[!UICONTROL 프로필 특성별 최상위 판매자]**

[!DNL Target]은(는) 웹 사이트에서 또는 항목 속성이나 카테고리별로 분류된 가장 많이 본 항목 및 가장 많이 판매된 항목에 대한 인기도 기반 알고리즘을 제공합니다. 이러한 알고리즘은 주어진 시간대에서 항목을 보거나 구매한 세션 수로 항목의 등급을 지정합니다.

이러한 모든 알고리즘은 시간별 및 일별 해상도 모두에서 항목을 보고 구매한 총 세션 수를 기록하는 집계된 행동 데이터를 결합합니다. 그런 다음 각 알고리즘은 고객이 구성한 전환 확인 기간에 대해 가장 많이 본 항목 또는 가장 많이 구매한 항목을 찾습니다.

알고리즘은 다음과 같이 다릅니다.

* **[!UICONTROL 사이트에서 가장 많이 본 항목]**&#x200B;과 **[!UICONTROL 사이트에서 최상위 판매자]**&#x200B;는 각각 항목을 보거나 구매한 세션의 집계 수에 따라 항목의 등급을 매깁니다. 출력은 권장 항목의 단일(키가 없는) 목록입니다.
* 카테고리 또는 항목 속성별 가장 많이 본 항목 및 최상위 판매자도 집계 세션 카운트별로 항목을 정렬하지만, 항목 카테고리 또는 특정 항목 속성별로 그룹화합니다. 출력은 카테고리 또는 항목 속성의 값을 기준으로 입력되는 권장 항목 목록입니다.
* **[!UICONTROL 프로필 특성별 가장 많이 본 항목]** 및 **[!UICONTROL 프로필 특성별 최상위 판매자]** 또한 집계 보기 또는 구매 횟수별로 항목의 등급을 매기지만 항목 속성 대신 국가, 지역 또는 멤버십 계층과 같은 방문자 프로필 특성별로 그룹화됩니다. 각 세션의 수는 상호 작용 시 방문자가 보유한 프로필 값에 기인하며, 항목의 속성은 아닙니다. 그 결과, 해당 프로필 속성의 고유한 값에 의해 입력된 추천 목록 세트가 됩니다.

## 최근에 본 항목

&quot;최근에 본 항목&quot; 알고리즘은 추천의 세션 내 개인화를 제공합니다. 오프라인 모델 교육이 필요하지 않습니다. 대신 [!DNL Target]은(는) 고유한 [방문자 프로필](/help/main/c-target/c-visitor-profile/visitor-profile.md)을 사용하여 세션에서 본 항목의 실행 목록을 유지하고 이러한 항목을 권장 사항 활동에 표시할 수 있습니다. 이를 통해 추천과 다음 페이지 개인화에 대한 실시간 업데이트가 가능합니다.

## 사용자 지정 기준

사용자 지정 기준을 통해 고객은 [자신의 권장 사항을 Target에 업로드](/help/main/c-recommendations/c-algorithms/recommendations-csv.md)할 수 있습니다. 이렇게 하면 유연성을 제공하고 &quot;나만의 모델을 가져옴&quot; 기능을 사용할 수 있습니다. 사용자 지정 기준이 **[!UICONTROL 항목 기반]** 권장 사항의 오프라인 교육 부분을 대체합니다. 온라인 콘텐츠 게재 중에는 항목 기반 알고리즘처럼 동작합니다. 권장 사항을 검색하는 데 단일 키를 사용하고 비즈니스 규칙 및 필터가 적용됩니다.
