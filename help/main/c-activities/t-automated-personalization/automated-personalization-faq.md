---
keywords: 문제 해결;자주 묻는 질문;FAQ;FAQ;자동화된 개인화;제어;기본 경험;우수 사례
description: '[!UICONTROL Adobe Target]의 [!UICONTROL Automated Personalization] (AP) 활동에 대한 FAQ 및 답변 목록을 살펴보십시오.'
title: '[!UICONTROL Automated Personalization] 활동에 대한 FAQ를 찾으려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
TQID: 'https://experienceleague.adobe.com/cYdFwvkJDlfGYdcxql9iWGwNiTed4Lb2kC7JdN7xgdo'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 6%
---
# AUTOMATED PERSONALIZATION FAQ {#ap-faq}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL Automated Personalization]** 활동에 대한 FAQ에 대한 답변을 찾아보세요.

>[!ENDSHADEBOX]

다음 질문과 대답은 [!DNL Adobe Target]에서 **[!UICONTROL Automated Personalization]** 활동을 설정하는 방법, 개인화 모델을 만드는 방법, 트래픽이 할당되는 방법, 결과를 읽는 방법을 다룹니다.

## 활동 설정 {#set-up-an-activity}

+++ [!UICONTROL Automated Personalization] 활동을 설정하는 모범 사례는 무엇입니까?

* 총 경험 수에 주의하지 말고 *활동 모양*(위치 수 × 오퍼 수)에 주의하십시오. 위치와 오퍼의 데카르트 조합은 원시 경험 수보다 작성 시간 성능에 더 영향을 줍니다. 최적의 성능과 관리 용이성을 위해 &quot;Automated Personalization의 제한은 무엇입니까?&quot;라는 질문에 설명된 대로 **[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동을 위치당 4-6개의 오퍼가 있는 4-6개의 위치로 제한합니다. 이 섹션에서 참조할 수 있습니다. 더 큰 구성은 권장되지 않으며 **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 로드 또는 편집이 느려질 수 있습니다.
* 낮은 트래픽의 페이지를 개인화하거나 개인화하는 경험에 대한 구조를 변경하려면 **[!UICONTROL Automated Personalization]** 대신 [**[!UICONTROL 자동 타겟&#x200B;]**&#x200B;활동](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 사용하는 것이 좋습니다.
* **[!UICONTROL Automated Personalization]** 활동에 사용할 오퍼와 위치 간에 **[!UICONTROL A/B 테스트]** 활동을 실행하여 위치 및 오퍼가 최적화 목표에 영향을 주는지 확인해 보십시오. **[!UICONTROL A/B 테스트]** 활동이 상당한 차이를 보이지 않는 경우 **[!UICONTROL Automated Personalization]**&#x200B;도 향상되지 않을 수 있습니다.

  A/B...N 테스트에서 경험 간에 통계적으로 중요한 차이가 없는 경우 다음 상황 중 하나 이상이 원인일 수 있습니다.

  * 오퍼는 서로 충분히 다르지 않을 수 있습니다.
  * 선택한 위치는 성공 지표에 영향을 주지 않습니다.
  * 전환 funnel에서 최적화 목표가 너무 멀어서 선택한 오퍼의 영향을 받을 수 없습니다.

* [트래픽 견적 도구](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator)를 사용하여 **[!UICONTROL Automated Personalization]** 활동에서 개인화 모델을 만드는 데 걸리는 시간을 파악합니다.
* 활동을 시작하기 전에 목표를 기반으로 제어와 타겟팅된 트래픽 간의 할당을 결정합니다. 다음 표에는 활동의 목표 및 선택한 제어 유형에 따라 고려해야 할 세 가지 시나리오가 나열되어 있습니다.

  | 제어 및 활동 목표 | 컨트롤에 대한 권장 할당 | 세부 사항 |
  | --- | --- | --- |
  | **[!UICONTROL 무작위 경험]**&#x200B;을 제어로 사용하며 목표는 개인화 알고리즘의 효과를 테스트하는 것입니다. | 50% | 이 목표를 위해서는 더 정확한 상승도를 파악해야 합니다. 또한 경험 또는 오퍼의 전환율을 간단한 **[!UICONTROL A/B 테스트]**(임의로 제공된 제어)가 제공하는 비율과 비교하려 할 수 있습니다. |
  | **[!UICONTROL 무작위 경험]**&#x200B;을 제어로 사용하며 목표는 개인화된 트래픽을 최대화하는 것입니다. | 10%~30% | 알고리즘을 사용하는 데 익숙하고 최대 트래픽 양을 개인화하려는 경우 이 옵션을 사용합니다. 트레이드오프는 리프트 정보의 정확성입니다. 제어 트래픽에 유입되는 트래픽이 감소하므로 신뢰 구간이 더 큽니다. |
  | **[!UICONTROL 특정 경험]**&#x200B;을 제어로 사용합니다(두 가지 목표 포함). | 10%~30% | 이 옵션을 사용하여 특정 마케터 중심의 경험을 개인화 모델과 비교할 수 있습니다. 한 개의 경험만 제어로 선택하면 해당 트래픽이 활동의 모든 오퍼 또는 경험에 분산되지 않습니다. |

* 모델의 최적화 기능을 방해할 수 있으므로 타깃팅 규칙을 가능한 한 적게 사용합니다. 자세한 내용은 [자동화된 개인화 오퍼 타깃팅](/help/main/c-activities/t-automated-personalization/ap-target-offers.md)을 참조하십시오.
* 보고 그룹은 **[!UICONTROL Automated Personalization]** 활동의 성공을 제한할 수 있으므로 특정 조건에서만 사용하십시오. 자세한 내용은 [Automated Personalization의 오퍼 보고 그룹](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md)을 참조하세요.

  * 다음 조건이 모두 충족되는 경우에만 보고 그룹을 사용하십시오.

    * 활동이 실행되는 동안 오퍼를 바꾸거나 추가할 계획입니다.
    * 보고 그룹의 오퍼는 동일한 방문자에게 어필됩니다.
    * 보고 그룹의 오퍼의 전체 응답률은 거의 동일합니다.

  * 보고 그룹의 오퍼 간에는 개인화가 없습니다. 개인화 모델은 모든 오퍼를 동일한 것으로 처리합니다.
  * 활동에 있는 모든 오퍼를 하나의 보고 그룹에 넣지 마십시오. 이렇게 하면 활동의 모든 방문자에게 모든 오퍼가 균일하게 임의로 제공됩니다.

+++

+++ [!UICONTROL Automated Personalization]에 제한이 있습니까?

[!DNL Target]은(는) 30,000개의 경험으로 제한되어 있지만 10,000개 미만의 경험이 만들어졌을 때 가장 잘 작동합니다. 활동에 **[!UICONTROL 중복 허용 안 함]** 옵션이 활성화된 경우에도 동일한 제한이 적용됩니다.

**[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동은 많은 수의 경험을 지원할 수 있지만 작성 성능은 *활동 모양*(위치 수 × 오퍼 수)에 따라 크게 달라집니다. 특정 구성은 문서화된 경험 제한보다 적더라도 로드 및 편집 성능에 상당한 영향을 줄 수 있는 큰 직각적 조합을 만듭니다.

최적의 성능과 관리 용이성을 위해 **[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동을 위치당 4~6개의 오퍼를 제공하는 4~6개의 위치로 제한하십시오. 더 큰 구성은 권장되지 않으며 [!DNL Target] UI에서 제한될 수 있습니다.

현재 [!DNL Target] UI에서 **[!UICONTROL Automated Personalization]** 및 **[!UICONTROL 자동 타겟]** 활동은 **[!UICONTROL 경험]** 단계에서 직접 구성됩니다. [!DNL Target]은(는) 구성이 지원되는 임계값을 초과하는 경우 인라인 경고를 표시하거나 활동을 저장하지 못하도록 할 수 있으며 **[!UICONTROL 다음]**, **[!UICONTROL 저장]** 및 **[!UICONTROL 게시]**&#x200B;에서 활동 셰이프의 유효성을 다시 확인합니다.

[!DNL Target]의 활동 및 기타 요소에 영향을 주는 문자 제한 및 기타 제한(오퍼 크기, 대상, 프로필, 값, 매개 변수 등)에 대한 자세한 내용은 [제한](/help/main/r-troubleshooting-target/target-limits.md)을 참조하십시오.

+++

+++ [!UICONTROL Automated Personalization] 활동에서 컨트롤로 사용할 특정 환경을 지정할 수 있습니까?

AP([**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview)) 또는 AT([**[!UICONTROL 자동 타겟]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) 활동을 만드는 동안 컨트롤로 사용할 특정 환경을 선택할 수 있습니다.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 해당 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대해 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

자세한 내용은 [제어 경험 선택](/help/main/c-activities/t-automated-personalization/experience-as-control.md)을 참조하십시오.

+++

+++ 오퍼 수준의 타깃팅은 어떻게 구현합니까?

각 방문자가 도착하면 오퍼 수준 타깃팅 규칙이 방문자가 볼 수 있는 오퍼 집합을 결정합니다. 그런 다음 알고리즘에서는 이러한 오퍼 중에서 모델이 예측하는 오퍼가 예상 매출이나 전환 가능성이 가장 높은 오퍼를 선택합니다. 오퍼 타깃팅은 [!DNL Target] 머신 러닝 알고리즘의 효과에 영향을 주므로 가능한 한 제한적으로 사용하십시오. 자세한 내용은 [자동화된 개인화 오퍼 타깃팅](/help/main/c-activities/t-automated-personalization/ap-target-offers.md)을 참조하십시오.

+++

## 모델 구축 및 트래픽 할당 {#models-and-traffic}

+++ [!UICONTROL Automated Personalization]에서 내 활동의 트래픽을 할당하는 방법은 무엇입니까?

**[!UICONTROL Automated Personalization]**&#x200B;은(는) 가장 최근의 [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) 모델을 기반으로 가장 높게 예측된 성공 지표가 있는 경험으로 방문자를 보냅니다. 이 예측은 방문자의 특정 정보 및 방문 컨텍스트를 기반으로 합니다.

예를 들어 **[!UICONTROL Automated Personalization]** 활동에 각각 오퍼가 두 개인 위치가 두 개라고 가정해 보겠습니다. 첫 번째 위치에서 오퍼 A는 특정 방문자에 대한 예측 전환율이 3%이고 오퍼 B는 예측 전환율이 1%입니다. 두 번째 위치에서 오퍼 C는 동일한 방문자에 대한 예측 전환율이 2%이고 오퍼 D는 예측 전환율이 5%입니다. 따라서 **[!UICONTROL Automated Personalization]**&#x200B;은(는) 이 방문자에게 오퍼 A와 오퍼 D에 대한 경험을 제공합니다.

+++

+++ [!UICONTROL Automated Personalization]은(는) 환경과 관련하여 모델을 어떻게 구축합니까?

한 가지 모델이 만들어져 무작위로 제공되는 트래픽과 전체 우승 경험에 모든 트래픽을 보내는 개인화 전략의 성능을 식별합니다. 이 모델은 기본 환경에서만 히트 및 전환을 고려합니다.

각 보고 그룹(**[!UICONTROL Automated Personalization]**) 또는 경험(**[!UICONTROL 자동 타겟]**)에 대해 두 번째 모델 집합이 만들어집니다. 이러한 각 모델에 대해 모든 환경의 히트 및 전환이 고려됩니다.

따라서 환경에 관계없이 동일한 모델에서 요청이 제공됩니다. 그러나, 복수의 트래픽은 식별된 전체 우승 경험이 실제 동작과 일관되도록 기본 환경에서 가져와야 합니다.

+++

+++ 모델이 만들어지기까지 얼마나 기다려야 합니까?

일반적으로 활동에서 모델을 만드는 데 걸리는 시간은 선택한 활동 위치에 대한 트래픽 및 활동 성공 지표에 따라 다릅니다. [트래픽 견적 도구](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator)를 사용하여 활동에서 모델을 만드는 데 걸리는 예상 시간을 결정합니다.

+++

+++ 내 [!UICONTROL Automated Personalization] 활동에서 모델을 만드는 데 필요한 시간을 줄이려면 어떻게 해야 합니까?

모델이 만들어지는 속도를 향상시키는 변경 사항에 대해서는 활동 설정을 검토하십시오. 예를 들어, RPV 성공 지표를 전환으로 변경하거나, 판매 funnel에서 활동 경험에 더 가까운 성공 지표를 선택하거나, 활동에서 일부 경험을 삭제하거나, 더 높은 트래픽 페이지를 사용합니다. 자세한 내용은 [Automated Personalization 문제 해결](/help/main/c-activities/t-automated-personalization/ap-trouble.md)을 참조하세요.

+++

+++ 내 [!UICONTROL Automated Personalization] 활동 내에 모델 하나가 만들어져 있습니다. 해당 경험에 대한 방문이 개인화됩니까?

아니오. 개인화를 시작하려면 활동 내에 두 개 이상의 모델을 구축해야 합니다.

+++

## 결과 및 상승도 {#results-and-lift}

+++ 내 [!UICONTROL Automated Personalization] 활동의 결과는 언제 볼 수 있습니까?

두 개 이상의 경험에 모델이 만들어지면(녹색 확인 표시로 표시됨) **[!UICONTROL Automated Personalization]** 활동의 결과를 볼 수 있습니다.

+++

+++ [!UICONTROL Automated Personalization] 활동에 상승도가 표시되지 않는 이유는 무엇입니까?

**[!UICONTROL Automated Personalization]** 활동에서 상승도를 생성하려면 네 가지 요소가 필요합니다.

* 각 위치의 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 위치는 최적화 목표에 영향을 주는 위치여야 합니다.
* 활동에 상승도를 감지하기에 충분한 트래픽 및 통계적 검정력이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

가장 좋은 작업 방침은 먼저 간단한 개인화되지 않은 **[!UICONTROL A/B 테스트]** 활동을 사용하여 활동 경험을 구성하는 콘텐츠 및 위치가 전체 응답률에 정말로 영향을 주는지 확인하는 것입니다. 전체 절차는 [Automated Personalization 문제 해결](/help/main/c-activities/t-automated-personalization/ap-trouble.md)을 참조하십시오.

+++

+++ [!UICONTROL Automated Personalization]을(를) 기본 경험과 비교하려면 어떻게 해야 합니까?

**[!UICONTROL Automated Personalization]**&#x200B;을(를) 기본 경험과 비교할 수 있는 턴키 옵션이 없습니다. 해결 방법으로, 기본 오퍼 또는 경험이 활동의 일부로 존재하는 경우 보고서에서 **[!UICONTROL 컨트롤]** 세그먼트를 클릭하고 결과 오퍼 수준 보고서에서 해당 오퍼를 찾습니다. 이 오퍼에 대해 기록된 전환율은 전체 &quot;Random Forest&quot; 세그먼트의 전환율과 비교할 수 있습니다. 이 비교는 기본 오퍼와 비교하여 모델이 수행되는 방식을 보여 줍니다.

+++

## 라이브 활동 관리 {#manage-live-activity}

+++ 내 [!UICONTROL Automated Personalization] 활동을 언제 중지해야 합니까?

**[!UICONTROL Automated Personalization]**&#x200B;은(는) 항상 최적화되는 &quot;항시적&quot; 개인화로 사용할 수 있습니다. 특히 항상 사용되는 콘텐츠의 경우 **[!UICONTROL Automated Personalization]** 활동을 중지할 필요가 없습니다. 현재 활동에 있는 오퍼와 유사하지 않은 콘텐츠를 크게 변경하려면 새 활동을 시작하는 것이 좋습니다. 새 활동을 시작하면 보고서를 검토하는 다른 사용자가 과거 결과를 다른 콘텐츠와 혼동하거나 연관시키지 않도록 하는 데 도움이 됩니다.

+++

+++ [!UICONTROL Automated Personalization] 활동 중간에 목표 지표를 변경할 수 있습니까?

[!DNL Adobe]은(는) 활동 중간에 목표 지표를 변경하지 않는 것이 좋습니다. [!DNL Target] UI를 사용하여 활동 중에 목표 지표를 변경할 수 있지만 항상 새 활동을 대신 시작하십시오. [!DNL Adobe]은(는) 활동이 실행된 후 목표 지표를 변경할 경우 어떤 결과가 발생하는지 보장하지 않습니다.

이 권장 사항은 [!DNL Target] 또는 [!DNL Analytics]&#x200B;(A4T)을 보고 소스로 사용하는 **[!UICONTROL 자동 할당]**, **[!UICONTROL 자동 타겟]** 및 **[!UICONTROL Automated Personalization]** 활동에 적용됩니다.

+++

+++ [!UICONTROL Automated Personalization] 활동을 실행하는 동안 [!UICONTROL 보고서 데이터 재설정] 옵션을 사용할 수 있습니까?

[!DNL Adobe]은(는) **[!UICONTROL Automated Personalization]** 활동에 대해 **[!UICONTROL 보고서 데이터 재설정]** 옵션을 사용하지 않는 것이 좋습니다. 이 옵션을 사용하면 표시되는 보고 데이터는 제거되지만 **[!UICONTROL Automated Personalization]** 모델에서 모든 교육 기록이 제거되지는 않습니다. **[!UICONTROL 보고서 데이터 재설정]** 옵션을 사용하는 대신 새 활동을 만들고 원래 활동을 비활성화하십시오. 이 지침은 **[!UICONTROL 자동 할당]** 및 **[!UICONTROL 자동 타겟]** 활동에도 적용됩니다.

+++

+++ 방문자에게 표시되지 않아야 하는 [!UICONTROL Automated Personalization] 활동에 대한 경험이 방문자에게 표시되는 이유는 무엇입니까?

**[!UICONTROL Automated Personalization]** 활동은 세션당 한 번씩 평가됩니다. 특정 경험에 적합한 활성 세션이 있고 그 후에 새 오퍼가 이 경험에 추가된 경우 방문자는 이전에 표시된 오퍼와 함께 새 콘텐츠를 볼 수 있습니다. 이러한 방문자는 이전에 해당 경험에 대한 자격이 있었으므로 세션 중에 이러한 경험을 계속 볼 수 있습니다. 모든 페이지 방문 시 활동을 평가하려면 **[!UICONTROL 경험 타깃팅]**(XT) 활동 유형으로 변경하십시오.

+++
