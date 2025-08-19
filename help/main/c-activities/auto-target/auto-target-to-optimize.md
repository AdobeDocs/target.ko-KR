---
keywords: 자동 타겟;타깃팅;트래픽 할당;자주 묻는 질문;faq;문제 해결;문제해결
description: '[!UICONTROL Auto-Target] 활동이 고객 프로필 및 유사한 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL Auto-Target] 활동이란?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 18%

---

# [!UICONTROL Auto-Target] 개요

[!UICONTROL Auto-Target]의 [!DNL Adobe Target] 활동은 콘텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 선택합니다. [!UICONTROL Auto-Target]은(는) 개별 고객 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공합니다.

>[!NOTE]
>
>* [!UICONTROL Auto-Target]은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md)을 참조하십시오.
>
>* [!UICONTROL Analytics for Target]&#x200B;(A4T)에서 [!UICONTROL Auto-Target]개의 활동을 지원합니다. 자세한 내용은 자동 할당 및 자동 타겟 활동에 대한 [A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오.

## 자동 타겟을 사용한 실제 성공 사례 {#success}

한 주요 의류 retailer은 최근 10개의 제품 범주 기반 경험(무작위 제어 포함)과 함께 [!UICONTROL Auto-Target] 활동을 사용하여 각 방문자에게 올바른 콘텐츠를 전달했습니다. &quot;[!UICONTROL Add to Cart]&quot;이(가) 기본 최적화 지표로 선택되었습니다. 타겟팅된 경험의 상승도는 평균 29.09%였습니다. [!UICONTROL Auto-Target] 모델을 빌드한 후 활동은 90% 개인화된 경험으로 설정되었습니다.

불과 열흘 만에 170만 달러 이상의 리프트 달성이 이뤄졌다.

[!UICONTROL Auto-Target]을(를) 사용하여 조직의 향상도 및 매출을 높이는 방법에 대해 알아보려면 계속 읽어 보십시오.

## 개요 {#section_972257739A2648AFA7E7556B693079C9}

안내가 있는 3단계 워크플로우를 사용하여 [A/B 활동을 만드는 중](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) **[!UICONTROL Auto-Target for personalized experiences]** 페이지에서 **[!UICONTROL Targeting]** 옵션을 선택합니다(2단계).

![트래픽 할당 메서드 설정](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

A/B 활동 흐름 내의 [!UICONTROL Auto-Target] 옵션을 사용하면 한 번의 클릭으로 마케터가 정의한 일련의 경험들을 기반으로 개인화하는 기계 학습을 활용할 수 있습니다. [!UICONTROL Auto-Target]은(는) 각 방문자에 대해 표시할 경험을 결정함으로써 기존의 A/B 테스트나 [!UICONTROL Auto Allocate]에 비해 최대 최적화를 제공하도록 설계되었습니다. 목표가 단일 승자를 찾는 것인 A/B 활동과 달리 [!UICONTROL Auto-Target]은(는) 주어진 방문자에게 최상의 경험을 자동으로 결정합니다. 최상의 경험은 고도로 개인화된 경험을 제공하기 위해 방문자의 프로필 및 기타 컨텍스트 정보를 기반으로 합니다.

[!UICONTROL Automated Personalization]과(와) 마찬가지로 [!UICONTROL Auto-Target]은(는) 선도적인 데이터 과학 앙상블 방법인 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)을(를) 사용하여 방문자에게 표시할 최상의 경험을 결정합니다. [!UICONTROL Auto-Target]은(는) 방문자의 행동 변화에 적응할 수 있으므로 상승도를 제공하도록 지속적으로 실행할 수 있습니다. 이 방법을 &quot;항시적&quot; 모드라고도 합니다.

지정된 방문자에 대한 경험 할당이 고정된 A/B 활동과 달리 [!UICONTROL Auto-Target]은(는) 각 방문을 통해 지정된 비즈니스 목표를 최적화합니다. [!UICONTROL Auto Personalization]의 [!UICONTROL Auto-Target]과(와) 마찬가지로 기본적으로 활동의 트래픽 일부를 상승도를 측정하기 위한 컨트롤 그룹으로 예약합니다. 통제군에 있는 방문자는 활동에서 임의 경험을 제공받습니다.

## 고려 사항

[!UICONTROL Auto-Target]을(를) 사용할 때 염두에 두어야 할 몇 가지 중요한 고려 사항이 있습니다.

* 특정 활동을 [!UICONTROL Auto-Target]에서 [!UICONTROL Automated Personalization]&#x200B;(으)로 전환할 수 없습니다.
* [!UICONTROL Manual] 트래픽 할당(기존 [!UICONTROL A/B Test])에서 [!UICONTROL Auto-Target]&#x200B;(으)로 전환할 수 없으며, 반대로 활동이 초안으로 저장됩니다.
* 한 가지 모델이 만들어져 무작위로 제공되는 트래픽과 전체 우승 경험에 모든 트래픽을 보내는 개인화 전략의 성능을 식별합니다. 이 모델은 기본 환경에서만 히트 및 전환을 고려합니다.

  두 번째 모델 세트의 트래픽은 각 모델링 그룹 (AP) 또는 경험 (AT)에 대해 빌드됩니다. 이러한 각 모델에 대해 모든 환경의 히트 및 전환이 고려됩니다.

  요청은 환경에 관계없이 동일한 모델로 제공됩니다. 그러나, 복수의 트래픽은 식별된 전체 우승 경험이 실제 동작과 일관되도록 기본 환경에서 가져와야 합니다.

* 최소 2개의 경험을 사용합니다.

## Terminology {#section_A309B7E0B258467789A5CACDC1D923F3}

다음 용어는 [!UICONTROL Auto-Target]에 대해 논의할 때 유용합니다.

| 용어 | 정의 |
|---|---|
| [Multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | 최적화에 대한 multi-armed bandit 접근 방식은 탐색 학습과 해당 학습의 이용 간에 균형을 이룹니다. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest는 선도적인 기계 학습 접근 방식입니다. 데이터 과학 스피크에서 방문자와 방문 속성을 기반으로 많은 의사 결정 트리를 구성하여 작동하는 앙상블 분류, 즉 회귀 방법이다. [!DNL Target] 내에서 Random Forest를 사용하여 각 특정 방문자에 대해 전환 가능성이 가장 높거나 방문당 매출이 가장 높을 것으로 예상되는 경험을 결정합니다. |
| [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Thompson 샘플링의 목표는 해당 경험을 찾는 &quot;비용&quot;을 최소화하면서 전체적(개인화되지 않음)으로 가장 좋은 경험을 결정하는 것입니다. 톰슨 샘플링은 항상 두 경험 사이에 통계적 차이가 없더라도 승자를 선택합니다. |

## [!UICONTROL Auto-Target] 작동 방식 {#section_77240E2DEB7D4CD89F52BE0A85E20136}

아래 링크에서 [!UICONTROL Auto-Target] 및 [!UICONTROL Automated Personalization]의 원본으로 사용하는 데이터 및 알고리즘에 대해 자세히 알아보세요.

| 용어 | 세부 사항 |
|--- |--- |
| [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | [!DNL Target]과(와) [!UICONTROL Auto-Target] 모두에서 사용되는 [!UICONTROL Automated Personalization]의 기본 개인화 알고리즘은 Random Forest입니다. Random Forest와 같은 앙상블 방법은 구성 학습 알고리즘 중 어느 것으로부터도 얻을 수 있는 것보다 더 나은 예측 성능을 얻기 위해 다중 학습 알고리즘을 사용한다. [!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동의 Random Forest 알고리즘은 교육 시간에 다수의 의사 결정 트리를 구성하여 작동하는 분류 또는 회귀 방법입니다. |
| [ [!DNL Target]의 Personalization 알고리즘에 대한 데이터 업로드](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | [!UICONTROL Auto-Target] 및 [!UICONTROL Automated Personalization] 모델에 대한 데이터를 입력하는 방법에는 여러 가지가 있습니다. |
| [ [!DNL Target]의 Personalization 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md) | [!DNL Target]의 개인화 알고리즘에서 다양한 데이터를 자동으로 수집합니다. |

## 트래픽 할당 결정 {#section_AB3656F71D2D4C67A55A24B38092958F}

활동의 목표에 따라 제어와 통제 경험과 개인화된 경험 간에 서로 다른 트래픽 할당을 선택할 수 있습니다. 활동을 라이브 상태로 만들기 전에 이 목표를 결정하는 것이 좋습니다.

[!UICONTROL Custom Allocation] 드롭다운 목록에서 다음 옵션 중 하나를 선택할 수 있습니다.

* [!UICONTROL Evaluate Personalization Algorithm (50/50)]
* [!UICONTROL Maximize Personalization Traffic (90/10)]
* [!UICONTROL Custom Allocation]

![할당 목표 드롭다운 목록](/help/main/c-activities/assets/split-new-ui.png)

다음 표에서는 세 가지 옵션에 대해 설명합니다.

| 활동 목표 | 제안된 트래픽 할당 | 트레이드오프 |
|--- |--- |--- |
| **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: 목표가 알고리즘을 테스트하는 것이면 제어 및 타깃팅된 알고리즘 간에 50/50%로 분할된 방문자를 사용합니다. 이 분할은 가장 정확한 상승도 추정치를 제공합니다. 임의 경험을 제어로 사용하는 것이 좋습니다. | 50% 통제/50% 개인화 경험 분할 | <ul><li>통제 경험과 개인화된 경험 간 상승도의 정확성을 극대화합니다.</li><li>개인화된 경험을 가진 방문자가 상대적으로 적습니다</li></ul> |
| **[!UICONTROL Maximize Personalization Traffic (90/10)]**: 목표가 &quot;상시 설정&quot; 활동을 만드는 것이면 10%의 방문자를 제어 알고리즘에 추가하여 충분한 데이터를 보장함으로써 시간에 따른 학습이 계속 진행될 수 있게 합니다. 여기서 장점은 더 많은 트래픽 비율을 개인화하는 대신 정확한 상승도를 파악하는 데는 정밀도가 떨어진다는 점입니다. 목표에 관계없이, 특정 경험을 제어로 사용할 때 권장되는 트래픽 분할입니다. | 10%~30% 통제/70%~90% 개인화된 경험 분할을 사용하는 것이 좋습니다. | <ul><li>개인화된 경험을 가진 방문자의 수를 최대화합니다.</li><li>상승도를 극대화합니다.</li><li>활동에 대한 상승도 크기와 관련하여 정확도가 낮습니다.</li></ul> |
| **사용자 지정 할당** | 백분율을 원하는 대로 수동으로 분할하십시오. | <ul><li>원하는 결과를 얻지 못할 수 있습니다. 잘 모르는 경우에는 앞의 선택 사항들 중 하나에 대한 제안을 따르십시오.</li></ul> |

[!UICONTROL Control] 백분율을 조정하려면 [!UICONTROL Experiences] 창에서 [!UICONTROL Traffic Allocation]을(를) 클릭한 다음 원하는 대로 백분율을 조정하십시오. 통제군은 10% 미만으로 줄일 수 없습니다.

특정 경험을 [선택하여 컨트롤로](/help/main/c-activities/t-automated-personalization/experience-as-control.md) 사용하거나 임의의 선택 사항을 사용할 수 있습니다.

## [!UICONTROL Auto-Target]보다 [!UICONTROL Automated Personalization]을(를) 언제 선택해야 합니까? {#section_BBC4871C87944DD7A8B925811A30C633}

[!UICONTROL Auto-Target]보다 [!UICONTROL Automated Personalization]을(를) 사용할 수 있는 시나리오가 몇 가지 있습니다.

* 경험을 형성하기 위해 자동으로 결합되는 개별 오퍼가 아닌 전체 경험을 정의하려는 경우.
* 사용자 지정 코드 편집기, 여러 경험 대상 등, [!UICONTROL Visual Experience Composer]에서 지원하지 않는 [!UICONTROL Auto Personalization]&#x200B;(VEC) 기능의 전체 집합을 사용하려면
* 다양한 경험에서 내 페이지의 구조를 변경하려는 경우. 예를 들어 홈 페이지에서 요소를 다시 정렬하려면 [!UICONTROL Auto-Target]이(가) [!UICONTROL Automated Personalization]보다 더 적합합니다.

## [!UICONTROL Auto-Target]은(는) [!UICONTROL Automated Personalization]과(와) 어떤 공통점이 있습니까? {#section_2A601F482F9A44E38D4B694668711319}

### 알고리즘은 각 방문에 대해 유리한 결과를 최적화합니다.

* 알고리즘은 최고의 경험을 제공하기 위해 방문자의 전환 성향(또는 전환으로 인한 예상 매출)을 예측합니다.
* 기존 세션이 종료되면 방문자에게 새 경험을 부여할 수 있습니다(방문자가 컨트롤 그룹에 속해 있지 않은 경우 첫 번째 방문에서 할당된 경험은 후속 방문에도 동일하게 유지됨).
* 세션 내에서는 시각적 일관성을 유지하기 위해 예측이 변경되지 않습니다.

### 이 알고리즘은 방문자 행동 변화에 적응합니다.

* Multi-arm bandit을 사용하면 모델이 항상 작은 부분 트래픽을 &quot;지출&quot;하여 활동 학습 기간 동안 계속 학습하고 이전에 학습한 트렌드의 과도한 사용을 방지할 수 있습니다.
* [!DNL Target]이(가) 항상 변화하는 방문자 환경 설정을 활용하고 있는지 확인하기 위해 최신 방문자 동작 데이터를 사용하여 기본 모델이 24시간마다 다시 작성됩니다.
* 알고리즘이 개인에 대해 가장 성과가 좋은 경험을 결정할 수 없는 경우 개인화된 승자를 계속 찾으면서도 전체적으로 성과가 가장 좋은 경험을 표시하도록 자동으로 전환합니다. 성과가 가장 좋은 경험은 [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling)을 사용하여 발견됩니다.

### 알고리즘은 단일 목표 지표에 대해 계속 최적화됩니다.

* 이 지표는 전환 기반 또는 매출 기반(좀 더 구체적으로 [!UICONTROL Revenue per Visit])일 수 있습니다.

### [!DNL Target]은(는) 방문자에 대한 정보를 자동으로 수집하여 개인화 모델을 만듭니다.

* [!UICONTROL Auto-Target] 및 [!UICONTROL Automated Personalization]에서 사용되는 매개 변수에 대한 자세한 내용은 [Automated Personalization 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하세요.

### [!DNL Target]은(는) 자동으로 모든 [!DNL Adobe Experience Cloud] 공유 대상을 사용하여 개인화 모델을 만듭니다.

* 모델에 대상을 추가하기 위해 특정한 작업을 수행할 필요가 없습니다. [!DNL Target]에서 [!DNL Experience Cloud Audiences] 사용에 대한 자세한 내용은 [Experience Cloud 대상자](/help/main/c-integrating-target-with-mac/mmp.md)를 참조하십시오.

### 마케터는 오프라인 데이터, 성향 점수 또는 기타 사용자 지정 데이터를 업로드하여 개인화 모델을 만들 수 있습니다.

* [ 및 [!UICONTROL Auto-Target]에 대한 [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md) 데이터 업로드에 대해 자세히 알아보세요.

## [!UICONTROL Auto-Target]과(와) [!UICONTROL Automated Personalization]의 차이점은 무엇입니까? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Auto-Target]은(는) 개인화된 모델을 만드는 데 [!UICONTROL Automated Personalization]보다 적은 트래픽을 필요로 하는 경우가 많습니다.

*또는* 모델을 만드는 데 필요한 트래픽의 양 [!UICONTROL Auto-Target]경험당[!UICONTROL Auto Personalization]은 동일하지만 일반적으로 [!UICONTROL Automated Personalization] 활동보다 [!UICONTROL Auto-Target] 활동에 더 많은 경험이 있습니다.

예를 들어, 두 개의 위치에 위치당 두 개의 오퍼를 만든 [!UICONTROL Auto Personalization] 활동이 있었다면, 활동에 총 4개(2 = 4)의 경험이 포함되어 있을 것입니다(제외 없음). [!UICONTROL Auto-Target]을(를) 사용하여 경험 1을 위치 1에서 오퍼 1을 포함하고, 위치 2에서 오퍼 2를 포함하도록 설정하고, 경험 2를 위치 1에서 오퍼 1을 포함하고, 위치 2에서 오퍼 2를 포함하도록 설정할 수 있습니다. [!UICONTROL Auto-Target]을(를) 사용하면 한 경험 내에 여러 가지 변경이 생기도록 선택할 수 있으므로 활동에 있는 총 경험 수를 줄일 수 있습니다.

[!UICONTROL Auto-Target]의 경우 간단한 경험 법칙을 사용하여 트래픽 요구 사항을 이해할 수 있습니다.

* **[!UICONTROL Conversion]이(가) 성공 지표인 경우:** 경험당 하루에 1,000번의 방문과 최소 50번의 전환이 필요하며, 활동에는 최소 7,000번의 방문과 350번의 전환이 있어야 합니다.
* **[!UICONTROL Revenue per Visit]이(가) 성공 지표인 경우:** 경험당 하루에 1,000번의 방문과 최소 50번의 전환이 필요하며, 활동에는 경험당 최소 1,000번의 전환이 있어야 합니다. RPV를 사용할 때에는 전환율을 사용할 때와 비교하여 방문 매출에 일반적으로 존재하는 더 높은 데이터 분산으로 인해 모델을 만드는 데 더 많은 데이터가 필요합니다.

### [!UICONTROL Auto-Target]에 완전한 설정 기능이 있습니다.

* [!UICONTROL Auto-Target]이(가) A/B 활동 워크플로에 포함되어 있으므로 [!UICONTROL Auto-Target]은(는) 보다 발전되고 완전한 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)의 이점을 얻을 수 있습니다. [과(와) 함께 ](/help/main/c-activities/c-activity-qa/activity-qa.md)QA 링크[!UICONTROL Auto-Target]을(를) 사용할 수도 있습니다.

### [!UICONTROL Auto-Target]은(는) 광범위한 온라인 테스트 프레임워크를 제공합니다.

* Multi-arm bandit은 [!DNL Adobe]명의 데이터 과학자와 연구원이 실제 환경에서 지속적으로 개선되는 이점을 이해할 수 있는 대규모 온라인 테스트 프레임워크의 일부입니다.
* 앞으로 이 테스트 베드를 통해 [!DNL Adobe] 머신 러닝 플랫폼을 데이터 전문 클라이언트에게 열어 해당 고객이 직접 모델을 가져와 [!DNL Target] 모델을 늘릴 수 있습니다.

## 보고 및 [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

자세한 내용은 [보고 및 자동 타겟](/help/main/c-activities/auto-target/reporting-and-auto-target.md)을 참조하세요.
