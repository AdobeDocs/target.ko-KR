---
keywords: random forest;의사 결정 트리;ap;Automated Personalization
description: '[!DNL Adobe Target]이(가) [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 타겟] 활동 모두에서 Random Forest 알고리즘을 사용하는 방법에 대해 알아봅니다.'
title: '[!DNL Target]에서 Random Forest 알고리즘을 사용하는 방법은 무엇입니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
TQID: 'https://experienceleague.adobe.com/Ui8E8CkiiJSdqim9fzIgPDdsKG1MMtuu3EUuAqgmm0M'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 6%
---
# Random Forest 알고리즘 {#random-forest-algorithm}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Target]이(가) Random Forest 알고리즘을 사용하여 **[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동의 개인화 모델을 만드는 방법을 알아봅니다.

>[!ENDSHADEBOX]

**[!UICONTROL AP(Automated Personalization]**) 및 **[!UICONTROL 자동 타겟]** 활동 모두에 사용되는 기본 개인화 알고리즘은 Random Forest입니다. 그것은 훈련할 때 다수의 의사결정나무를 구성하여 작동하는 분류법 또는 회귀법이다.

Random Forest는 앙상블 방법입니다. 통계를 생각하는 경우 결과를 예측하는 데 사용되는 단일 회귀 모델을 떠올릴 수도 있습니다. 최근의 데이터 과학 연구는 동일한 데이터 집합에서 여러 모형을 만든 다음 지능적으로 결합하는 &#39;앙상블 방법&#39;이 단일 모형을 기반으로 예측하거나 구성 학습 알고리즘 중 어느 것으로부터도 얻을 수 있는 것보다 더 좋은 결과를 낸다는 것을 시사한다.

## 의사 결정 트리가 무엇입니까? {#section_7F5865D8064447F4856FED426243FDAC}

의사 결정 트리는 시스템이 학습할 수 있는 모든 방문 데이터를 그룹으로 분류합니다. 각 그룹 내 방문은 목표 지표(예: 전환율)와 관련하여 가능한 한 서로 유사하며 그룹 간 방문은 가능한 한 다릅니다. 이를 위해 트리는 교육 세트의 변수를 보고 이 목표를 극대화하는 그룹(또는 &quot;잎&quot;)으로 상호 배타적인 총체적 전체(MECE) 방식으로 데이터를 분할합니다.

다음의 간단한 예에서 목표 지표는 전환이며 두 개의 입력 변수가 있습니다.

* 성별(두 개의 가능한 값, 남성 또는 여성)
* 우편 번호(작은 데이터 세트에 11111, 22222, 33333, 44444 또는 55555 5개의 잠재적 값 포함)

### 첫 번째 분할 {#first-split}

트리는 먼저 방문 데이터의 전환율에 있어 가장 큰 차이를 설명하는 두 변수 중 하나를 결정합니다. 우편 번호가 가장 예측 가능하다고 가정합니다. 이 변수는 트리의 첫 번째 &quot;분기&quot;를 형성합니다. 그런 다음 트리는 위에 설명된 대로 방문 데이터를 그룹으로 분할합니다. 11111, 22222, 33333이 하나의 분할이고 44444 및 55555이 두 번째 분할이라고 가정하자.

![결정 트리의 첫 번째 레이어](assets/decsion_tree_1.png){width="440" align="center"}

### 각 분기 내에서 분할 {#second-split}

이 트리는 &quot;가장 예측 가능한 변수는 무엇입니까?&quot;라는 질문을 던집니다. 다시 한 번 호출하고 유사한 연습을 완료하여 각 분기 내에서 *데이터를 분할합니다*. 성별만 남아 있으니 여기서의 답이다. 11111, 22222, 분지33333 남녀 간 전환에 차이가 있다고 가정한다. 그런 다음 두 잎(남성과 여성)이 있고, 이 가지는 완성된다. 44444과 55555에서 여성과 남성이 어떻게 전환하는지 통계적 차이가 없다고 가정하자. 이 경우 첫 번째 분할이 마지막 분할입니다.

![의사 결정 트리 완료](assets/decsion_tree_2.png){width="480" align="center"}

## Random Forest에서는 의사 결정 트리를 어떻게 사용합니까? {#section_536C105EF9F540C096D60450CAC6F627}

의사 결정 트리는 유용한 통계 도구입니다. 그러나 몇 가지 단점이 있습니다. 가장 중요한 것은 개별 트리가 초기 트리를 만드는 데 사용되지 않은 미래 데이터를 잘못 예측하도록 데이터를 &quot;과도하게 맞춤&quot;할 수 있다는 것입니다. 이 문제를 통계적 학습에서는 [편향-분산 트레이드오프](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff)&#x200B;(bias-variance tradeoff)라고 합니다.

랜덤 포레스트는 이 도전을 극복하는 데 도움이 됩니다. 랜덤 포레스트는 수백 개의 결정 트리가 같은 데이터 세트에 약간 다르게 만들어지고 개별 트리보다 더 나은 모델을 산출하기 위해 함께 &quot;투표&quot;하는 컬렉션입니다. 트리는 대체 항목이 있는 방문 레코드의 하위 집합을 임의로 선택하고(Bagging이라고 함) 속성의 하위 집합을 임의로 선택하여, 포리스트가 약간 다른 결정 트리로 구성되도록 합니다. 이 방법은 나무에 작은 변형을 도입한다. 이렇게 제어된 분산량을 추가하면 알고리즘의 예측 정확도가 향상되는 데 도움이 된다.

## [!DNL Target] 개인화 알고리즘에서 Random Forest를 사용하는 방법은 무엇입니까? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### 모델 구축 방법

[!DNL Target]은(는) 자동으로 수집하는 데이터와 사용자가 제공한 사용자 지정 데이터를 사용하여 개인화 알고리즘을 만듭니다. 다음 다이어그램은 **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]** 활동에 대해 모델을 만드는 방법을 요약합니다.

![Random Forest 모델을 만드는 방법을 요약하는 흐름](assets/random_forest_flow.png){width="850" zoomable="yes"}

1. [!DNL Target]은(는) 경험이나 오퍼를 임의로 제공하는 동안 방문자에 대한 데이터를 수집합니다.
1. [!DNL Target]이(가) 중요한 데이터 덩어리에 도달한 후 [!DNL Target]이(가) 기능 엔지니어링을 수행합니다.
1. [!DNL Target]은(는) 각 경험 또는 오퍼에 대해 Random Forest 모델을 만듭니다.
1. [!DNL Target]이(가) 임계값 품질 점수를 충족하는지 확인하여 모델의 유효성을 검사합니다.
1. [!DNL Target]이(가) 향후 트래픽을 개인화하기 위해 모델을 프로덕션으로 푸시합니다.

이러한 모델은 방문자에게 표시할 최고의 경험이나 오퍼를 예측합니다. 일반적으로 경험(**[!UICONTROL 자동 타겟]** 활동) 또는 오퍼(**[!UICONTROL Automated Personalization]** 활동)별로 하나의 모델이 만들어집니다. 그런 다음 [!DNL Target]은(는) 가장 높은 예상 성공 지표(예: 전환율)를 산출하는 경험 또는 오퍼를 표시합니다. 무작위로 제공된 방문에 대해 모델을 교육해야 예측에 사용할 수 있습니다. 그 결과, 개인화된 그룹에 있는 방문자들도 활동이 처음 시작될 때 개인화 알고리즘이 준비될 때까지 다른 경험이나 오퍼를 임의로 표시합니다.

모델은 AUC(Area Under the Curve)를 기반으로 하여 검증되므로 각 모델이 활동에 사용되기 전에 방문자의 행동을 잘 예측할 수 있습니다. 모델이 개인화된 경험을 제공하기 시작하는 정확한 시간은 데이터의 세부 사항에 따라 다릅니다. 먼저 모델의 유효성을 검사해야 하기 때문입니다. 실제로 트래픽 계획 용도로 제공하려는 경우, 각 모델이 유효해지기까지는 최소 전환 개수를 사용할 때보다 많은 시간이 소요됩니다.

모델이 경험 또는 오퍼에 대해 유효하게 되면 경험 또는 오퍼 이름 왼쪽에 있는 시계 아이콘이 녹색 확인란으로 변경됩니다. 최소 2개의 경험 또는 오퍼에 대해 유효한 모델이 있는 경우 일부 방문이 개인화되기 시작합니다.

### 기능 변환

데이터가 개인화 알고리즘을 거치기 전에 기능 변환을 거치는데, 이는 교육 기록에 수집된 데이터를 개인화 모델이 사용할 수 있도록 준비하는 것으로 생각할 수 있다. 변환은 속성 유형(또는 데이터 과학자가 때때로 설명하듯이 &quot;기능&quot;)에 따라 다릅니다.

| 기능 유형 | 설명 | 변환 |
|---|---|---|
| **범주형** | 셀 수 없지만 국가, 성별 또는 우편번호와 같은 다양한 그룹으로 분류할 수 있습니다. | 모든 가능한 특징들의 세트가 유지되고 데이터 크기를 감소시키기 위해 우도 변환이 사용된다. |
| **숫자** | 연령 또는 소득과 같이 측정하거나 계산할 수 있습니다. | 크기 조정을 통해 보드 전체에서 기능을 비교할 수 있습니다. |

### Multi-armed bandit 방식으로 학습과 개인화 간 균형 잡기

[!DNL Target]이(가) 개인화 모델을 구축한 후에는 향후 활동 방문자가 트레이드오프에 직면하게 됩니다. 현재 모델을 기반으로 모든 트래픽을 개인화할 수 있으며, 무작위로 오퍼를 제공하여 새 방문자로부터 계속 배울 수 있습니다. 개인화 알고리즘은 대부분의 트래픽을 개인화하는 동안 항상 방문자의 새로운 트렌드에 대해 학습해야 합니다. Multi-armed bandit은 [!DNL Target]이(가) 이 목표를 충족하는 방법입니다. 모델이 항상 적은 양의 트래픽을 사용하여 활동 기간 동안 계속 학습하고 이전에 학습한 트렌드의 과도한 사용을 방지합니다.

데이터과학계에서 멀티암드 밴딧 문제는 탐구 대 착취 딜레마의 전형적인 사례로, 각각 보상확률 미상의 1인 암적 도적떼의 모음이 주어진다. 성공 확률이 가장 높은 팔을 플레이하는 전략을 개발해 획득한 총 보상을 극대화하는 게 핵심이다. Multi-armed bandit 는 온라인 모델이 구축된 후 온라인 점수를 얻기 위해 시스템에서 사용됩니다. 이 과정은 탐색 중 온라인 학습에 도움이 된다. 현재의 다중 무장 알고리즘은 엡실론(ε) 그리디 알고리즘이다. 이 알고리즘에서는 확률 1 - ε를 사용하여 가장 좋은 팔이 선택됩니다. 확률 ε를 사용하면 다른 모든 팔이 임의로 선택됩니다.
