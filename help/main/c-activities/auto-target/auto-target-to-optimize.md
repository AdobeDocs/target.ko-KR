---
keywords: 자동 타겟;타깃팅;트래픽 할당;자주 묻는 질문;faq;문제 해결;문제해결
description: '[!UICONTROL 자동 타겟] 활동이 고객 프로필 및 유사한 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL 자동 타겟] 활동이란?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
TQID: 'https://experienceleague.adobe.com/uKmfIlOcT-tZgOjuvERXuif-Y5-2Jw3prtPbuBjv1is'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: de439134b0ee5aa795ae255bba852b9b6f10da12
workflow-type: tm+mt
source-wordcount: '2072'
ht-degree: 12%
---
# [!UICONTROL 자동 타겟] 시작 {#auto-target-overview}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 자동 타겟]** 활동이 각 방문자에게 가장 적합한 경험을 제공하는 방법, 작동 방법, 트래픽 할당을 선택하는 방법, **[!UICONTROL Automated Personalization]**&#x200B;와(과) 비교하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL 자동 타겟]** 활동에서는 콘텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 선택합니다. **[!UICONTROL 자동 타겟]**&#x200B;은(는) 개별 고객 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공합니다.

>[!NOTE]
>
>* **[!UICONTROL 자동 타겟]**&#x200B;은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md)을 참조하십시오.
>
>* **[!UICONTROL Analytics for Target]**(A4T)에서 **[!UICONTROL 자동 타겟]** 활동을 지원합니다. 자세한 내용은 자동 할당 및 자동 타겟 활동에 대한 [A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오.

안내가 있는 3단계 워크플로우로 [A/B 활동을 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)하는 경우 **[!UICONTROL 타깃팅]** 페이지(2단계)에서 **[!UICONTROL 개인화된 경험에 대한 자동 타깃팅]** 옵션을 선택하십시오. 단계는 [자동 타겟 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md)를 참조하십시오.

![트래픽 할당 메서드 설정](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

A/B 활동 흐름 내의 이 선택 사항을 사용하면 머신 러닝을 사용하여 한 번의 클릭으로 마케터가 정의한 일련의 경험들을 기반으로 콘텐츠를 개인화할 수 있습니다. **[!UICONTROL 자동 타겟]**&#x200B;은(는) 각 방문자에 대해 표시할 경험을 결정함으로써 기존의 A/B 테스트나 **[!UICONTROL 자동 할당]**&#x200B;에 비해 최대 최적화를 제공하도록 설계되었습니다. 목표가 단일 승자를 찾는 것인 A/B 활동과 달리, **[!UICONTROL 자동 타겟]**&#x200B;은(는) 주어진 방문자에게 최상의 경험을 자동으로 결정합니다. 최상의 경험은 방문자 프로필과 기타 컨텍스트 정보를 기반으로 합니다.

**[!UICONTROL Automated Personalization]**&#x200B;과 마찬가지로 **[!UICONTROL 자동 타겟]**&#x200B;에서는 선도적인 데이터 과학 Ensemble 방식인 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)을 사용하여 방문자에게 표시할 최상의 경험을 결정합니다. **[!UICONTROL 자동 타겟]**&#x200B;은(는) 방문자의 행동 변화에 맞게 조정될 수 있으므로 상승도를 제공하도록 지속적으로 실행될 수 있습니다. 이 방법을 &quot;항시적&quot; 모드라고도 합니다.

지정된 방문자에 대한 경험 할당이 고정된 A/B 활동과 달리, **[!UICONTROL 자동 타겟]**&#x200B;은(는) 각 방문을 통해 지정된 비즈니스 목표를 최적화합니다. **[!UICONTROL Automated Personalization]**&#x200B;에서와 같이 **[!UICONTROL 자동 타겟]**&#x200B;은(는) 상승도를 측정하기 위해 활동 트래픽의 일부를 기본적으로 컨트롤 그룹으로 예약합니다. 통제군에 있는 방문자는 활동에서 임의 경험을 제공받습니다.

## 고려 사항 {#considerations}

**[!UICONTROL 자동 타겟]**&#x200B;을 사용할 때는 다음 사항을 염두에 두십시오.

* 활동 형태에 주의하십시오. 성능은 원시 경험 개수보다 오퍼× 위치 수에 더 의존합니다. 큰 카티시안 조합은 문서화된 경험 제한보다 낮더라도 **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 로드 및 편집 속도가 느려질 수 있습니다.

  가장 좋은 방법은 **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]** 활동을 위치당 4~6개의 오퍼를 사용하는 4~6개의 위치에 유지하는 것입니다. 더 큰 구성은 권장되지 않습니다. 이러한 활동은 **[!UICONTROL 경험]** 단계에서 직접 빌드되므로 구성이 지원되는 임계값을 초과할 때 [!DNL Target] UI에 인라인 경고가 표시되거나 저장이 차단될 수 있습니다.

* 특정 활동을 **[!UICONTROL 자동 타겟]**&#x200B;에서 **[!UICONTROL Automated Personalization]**(으)로 전환하거나 그 반대로 전환할 수 없습니다.
* 활동이 초안으로 저장된 후에는 **[!UICONTROL 수동]** 트래픽 할당(기존 **[!UICONTROL A/B 테스트]**)에서 **[!UICONTROL 자동 타겟]**(또는 그 반대 방식)으로 전환할 수 없습니다.
* 한 가지 모델이 만들어져 무작위로 제공되는 트래픽과 전체 우승 경험에 모든 트래픽을 보내는 개인화 전략의 성능을 식별합니다. 이 모델은 기본 환경에서만 히트 및 전환을 고려합니다.

  두 번째 모델 세트는 각 모델링 그룹(AP) 또는 경험(AT)에 대해 빌드됩니다. 이러한 각 모델에 대해 모든 환경의 히트 및 전환이 고려됩니다.

  요청은 환경에 관계없이 동일한 모델로 제공됩니다. 그러나, 복수의 트래픽은 식별된 전체 우승 경험이 실제 동작과 일관되도록 기본 환경에서 가져와야 합니다.

* 최소 2개의 경험을 사용합니다.

## Terminology {#section_A309B7E0B258467789A5CACDC1D923F3}

다음 용어는 **[!UICONTROL 자동 타겟]**&#x200B;에 대해 논의할 때 유용합니다.

| 용어 | 정의 |
|---|---|
| [Multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | 최적화에 대한 multi-armed bandit 접근 방식은 탐색 학습과 해당 학습의 이용 간에 균형을 이룹니다. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest는 선도적인 기계 학습 접근 방식입니다. 데이터 과학 용어에서 방문자와 방문 속성을 기반으로 많은 의사 결정 트리를 구성하여 작동하는 앙상블 분류, 즉 회귀 방법이다. [!DNL Target] 내에서 Random Forest를 사용하여 각 특정 방문자에 대해 전환 가능성이 가장 높거나 방문당 매출이 가장 높을 것으로 예상되는 경험을 결정합니다. |
| [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Thompson 샘플링의 목표는 해당 경험을 찾는 &quot;비용&quot;을 최소화하면서 전체적(개인화되지 않음)으로 가장 좋은 경험을 결정하는 것입니다. Thompson 샘플링은 두 경험 간에 통계적 차이가 없더라도 항상 우승자를 선택합니다. |

## [!UICONTROL 자동 타겟] 작동 방식 {#section_77240E2DEB7D4CD89F52BE0A85E20136}

다음 페이지에서는 **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]**&#x200B;의 기본 데이터 및 알고리즘을 설명합니다.

| 주제 | 세부 사항 |
|--- |--- |
| [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]**&#x200B;에서 모두 사용되는 [!DNL Target]의 기본 개인화 알고리즘은 Random Forest입니다. Random Forest와 같은 앙상블 방법은 구성 학습 알고리즘 중 어느 것으로부터도 얻을 수 있는 것보다 더 나은 예측 성능을 얻기 위해 다중 학습 알고리즘을 사용한다. **[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동의 Random Forest 알고리즘은 교육 시간에 다수의 의사 결정 트리를 구성하여 작동하는 분류 또는 회귀 방법입니다. |
| [Personalization 알고리즘을 위한 데이터 업로드 [!DNL Target] 2&rbrace;](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md) | **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]** 모델에 대한 데이터를 입력하는 방법에는 여러 가지가 있습니다. |
| [데이터 수집 대상 [!DNL Target] Personalization 알고리즘](/help/main/c-activities/t-automated-personalization/ap-data.md) | [!DNL Target]의 개인화 알고리즘이 자동으로 다양한 데이터를 수집합니다. |

## 트래픽 할당 결정 {#section_AB3656F71D2D4C67A55A24B38092958F}

활동의 목표에 따라 제어와 개인화된 경험 간에 다른 트래픽 할당을 선택할 수 있습니다. 활동을 라이브 상태로 만들기 전에 이 목표를 결정하는 것이 좋습니다.

**[!UICONTROL 사용자 지정 할당]** 드롭다운 목록에서 다음 선택 사항 중에 선택할 수 있습니다.

* **[!UICONTROL Personalization 알고리즘 평가(50/50)]**
* **[!UICONTROL Personalization 트래픽 최대화(90/10)]**
* **[!UICONTROL 사용자 지정 할당]**

![할당 목표 드롭다운 목록](/help/main/c-activities/assets/split-new-ui.png)

다음 표에서는 세 가지 옵션에 대해 설명합니다.

| 활동 목표 | 제안된 트래픽 할당 | 트레이드오프 |
|--- |--- |--- |
| **[!UICONTROL 개인화 알고리즘 평가(50/50)]**: 목표가 알고리즘을 테스트하는 것이면 제어 및 타깃팅된 알고리즘 간에 50/50%로 분할된 방문자를 사용합니다. 이 분할은 가장 정확한 상승도 추정치를 제공합니다. 임의 경험을 제어로 사용하는 것이 좋습니다. | 50% 통제/50% 개인화 경험 분할 | <ul><li>통제 경험과 개인화된 경험 간 상승도의 정확성을 극대화합니다.</li><li>개인화된 경험을 가진 방문자가 상대적으로 적습니다</li></ul> |
| **[!UICONTROL Personalization 트래픽 최대화(90/10)]**: 목표가 &quot;상시 설정&quot; 활동을 만드는 것이면 10%의 방문자를 제어 알고리즘에 추가하여 충분한 데이터를 보장함으로써 시간에 따른 학습이 계속 진행될 수 있게 합니다. 여기서 장점은 더 많은 트래픽 비율을 개인화하는 대신 정확한 상승도를 파악하는 데는 정밀도가 떨어진다는 점입니다. 목표에 관계없이, 특정 경험을 제어로 사용할 때 권장되는 트래픽 분할입니다. | 10%~30% 통제/70%~90% 개인화된 경험 분할을 사용하는 것이 좋습니다. | <ul><li>개인화된 경험을 가진 방문자의 수를 최대화합니다.</li><li>상승도를 극대화합니다.</li><li>활동에 대한 상승도 크기와 관련하여 정확도가 낮습니다.</li></ul> |
| **[!UICONTROL 사용자 지정 할당]** | 백분율을 원하는 대로 수동으로 분할하십시오. | <ul><li>원하는 결과를 얻지 못할 수 있습니다. 잘 모르는 경우에는 앞의 선택 사항들 중 하나에 대한 제안을 따르십시오.</li></ul> |

**[!UICONTROL 컨트롤]** 백분율을 조정하려면 **[!UICONTROL 트래픽 할당]** 창에서 **[!UICONTROL 경험]**&#x200B;을 클릭한 다음 원하는 대로 백분율을 조정하십시오. 통제군은 10% 미만으로 줄일 수 없습니다.

[제어로 사용할 특정 환경을 선택](/help/main/c-activities/t-automated-personalization/experience-as-control.md)하거나 **[!UICONTROL 임의 환경]** 옵션을 사용할 수 있습니다.

## [!UICONTROL 자동 타겟]과(와) [!UICONTROL Automated Personalization] 비교 {#compare-at-ap}

**[!UICONTROL 자동 타겟]**&#x200B;과(와) **[!UICONTROL Automated Personalization]**&#x200B;은(는) 같은 알고리즘과 데이터를 공유하지만 경험이 만들어지는 방식과 모델에 필요한 트래픽의 양이 다릅니다.

### 두 활동 유형의 공통점 {#section_2A601F482F9A44E38D4B694668711319}

* **각 방문에 대한 최적화.** 알고리즘은 최고의 경험을 제공하기 위해 전환하려는 방문자의 성향(또는 전환으로 인한 예상 매출)을 예측합니다. 방문자는 기존 세션이 끝날 때 새 경험을 사용할 수 있습니다. 예외는 첫 번째 방문에서 할당된 경험을 유지하는 컨트롤 그룹의 방문자입니다. 세션 내에서는 시각적 일관성을 유지하기 위해 예측이 변경되지 않습니다.
* **방문자 행동 변화에 적응합니다.** multi-armed bandit는 활동 기간 동안 계속 학습하고 이전에 학습한 트렌드의 과도한 사용을 방지하기 위해 항상 트래픽의 작은 부분을 &quot;지출&quot;합니다. 기본 모델은 최신 방문자 동작 데이터를 사용하여 24시간마다 재구축됩니다. 알고리즘이 개인에게 우승 경험을 결정할 수 없는 경우 개인화된 우승자를 계속 찾는 동안 [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling)을 사용하여 찾은 전반적인 성과가 가장 좋은 경험을 표시하는 것으로 자동 전환됩니다.
* **단일 목표 지표입니다.** 알고리즘은 전환 기반 또는 매출 기반(좀 더 구체적으로 말하면 **[!UICONTROL 방문당 매출]**)인 하나의 지표에 대해 계속 최적화됩니다.
* **자동 데이터 수집** [!DNL Target]은(는) 방문자에 대한 정보를 자동으로 수집하여 개인화 모델을 만듭니다. 사용된 매개 변수에 대한 자세한 내용은 [Automated Personalization 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하세요.
* **공유 대상자.** [!DNL Target]은(는) 자동으로 모든 [!DNL Adobe Experience Cloud] 공유 대상을 사용하여 개인화 모델을 만듭니다. 모델에 대상을 추가하기 위해 수행해야 할 특별한 작업은 없습니다. [!DNL Target]에서 [!DNL Experience Cloud Audiences] 사용에 대한 자세한 내용은 [Experience Cloud 대상자](/help/main/c-integrating-target-with-mac/mmp.md)를 참조하십시오.
* **사용자 지정 데이터** 마케터는 오프라인 데이터, 성향 점수 또는 기타 사용자 지정 데이터를 업로드하여 개인화 모델을 만들 수 있습니다. [자동 타겟 및 Automated Personalization에 대한 데이터 업로드](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)에 대해 자세히 알아보세요.

### 두 활동 유형의 차이점 {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

전체 경험을 정의하거나 **[!UICONTROL 시각적 경험 작성기]**(VEC) 기능의 전체 세트를 사용하거나 페이지의 구조를 변경하려면 **[!UICONTROL Automated Personalization]** 대신 **[!UICONTROL 자동 타겟]**&#x200B;을(를) 고려해 보십시오.

| | [!UICONTROL 자동 타깃팅] | [!UICONTROL 자동화된 개인화] |
|---|---|---|
| **경험 정의** | 여러 변경 사항을 포함할 수 있는 전체 경험을 정의합니다. | 개별 오퍼가 자동으로 결합되어 경험을 형성합니다. |
| **[!UICONTROL 시각적 경험 작성기] 기능** | **[!UICONTROL 자동 타겟]**&#x200B;은(는) A/B 활동 워크플로우에 포함되어 있으므로 보다 발전되고 완전한 VEC의 이점을 얻을 수 있습니다. [QA 링크](/help/main/c-activities/c-activity-qa/activity-qa.md)를 사용할 수도 있습니다. | 사용자 지정 코드 편집기, 여러 경험 대상 및 기타 기능은 지원되지 않습니다. |
| **페이지에 대한 구조적 변경** | 더 적절해 예를 들어 홈 페이지에서 요소를 다시 정렬할 수 있습니다. | 덜 적절합니다. |
| **경험 수** | 한 경험에 여러 변경 사항이 포함될 수 있으므로 일반적으로 더 적습니다. | 일반적으로 더 많이 사용하는 이유는 경험이 모두 오퍼와 위치의 조합이기 때문입니다. |
| **모델을 만드는 데 필요한 트래픽** | 대개는 적습니다. | 더 자주 전체. |

모델을 만드는 데 필요한 트래픽의 양 *경험당*&#x200B;은(는) 두 활동 유형에 대해 동일합니다. **[!UICONTROL 자동 타겟]**&#x200B;은(는) 일반적으로 경험이 적기 때문에 총 트래픽이 적게 필요합니다.

예를 들어 위치당 두 개의 오퍼와 두 개의 위치가 있는 **[!UICONTROL Automated Personalization]** 활동에서는 활동에 총 4개(2 × 2 = 4)의 경험이 있습니다(제외 없음). **[!UICONTROL 자동 타겟]**&#x200B;에서 경험 1을 위치 1에서 오퍼 1을 포함하고, 위치 2에서 오퍼 2를 포함하도록 설정하고, 경험 2를 위치 1에서 오퍼 2를 포함하고, 위치 2에서 오퍼 1을 포함하도록 설정할 수 있습니다. **[!UICONTROL 자동 타겟]**&#x200B;에서는 한 경험 내에 여러 개의 변경을 허용하므로 활동에 있는 총 경험 수를 줄일 수 있습니다.

### [!UICONTROL 자동 타겟]에 대한 트래픽 요구 사항 {#traffic-requirements}

다음 경험적 규칙은 트래픽 요구 사항을 이해하는 데 도움이 됩니다.

* **[!UICONTROL 전환]이 성공 지표인 경우:** 경험당 하루 1,000회 방문 및 최소 50회 전환. 또한 활동에는 최소 7,000개의 방문과 350개의 전환이 있어야 합니다.
* **방문당 매출이 성공 지표인 경우:** 경험당 하루 1,000회 방문 및 최소 50회 전환. 또한 활동에는 경험당 최소 1,000개의 전환이 있어야 합니다. **[!UICONTROL 방문당 매출]**&#x200B;은(는) 일반적으로 전환율보다 방문 매출의 차이가 더 높기 때문에 모델을 만드는 데 더 많은 데이터가 필요합니다.

**[!UICONTROL 자동 타겟]**&#x200B;에서도 광범위한 온라인 테스트 프레임워크를 제공합니다. multi-armed bandit는 [!DNL Adobe] 데이터 과학자와 연구원이 실제 환경에서 지속적으로 개선되는 이점을 이해할 수 있도록 하는 대규모 온라인 테스트 프레임워크의 일부입니다. 앞으로 이 테스트 베드를 통해 [!DNL Adobe]이(가) 데이터를 많이 사용하는 클라이언트에 머신 러닝 플랫폼을 열어 [!DNL Target] 모델을 늘릴 수 있습니다.

보고에 대한 자세한 내용은 [보고 및 자동 타겟](/help/main/c-activities/auto-target/reporting-and-auto-target.md)을 참조하세요.
