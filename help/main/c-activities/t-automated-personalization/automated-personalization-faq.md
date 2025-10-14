---
keywords: 문제 해결;자주 묻는 질문;FAQ;FAQ;자동화된 개인화;제어;기본 경험;우수 사례
description: '[!UICONTROL Automated Personalization]의 [!UICONTROL Adobe Target]​(AP) 활동에 대한 FAQ 및 답변 목록을 살펴봅니다.'
title: '[!UICONTROL Automated Personalization] 활동에 대한 FAQ를 찾으려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 21%

---

# AUTOMATED PERSONALIZATION FAQ

[!UICONTROL Automated Personalization]의 [!DNL Adobe Target] 활동과 함께 작업할 때 다음 FAQ 및 답변을 참조하십시오.

## [!UICONTROL Automated Personalization] 활동에서 컨트롤로 사용할 특정 환경을 지정할 수 있습니까?

+++세부 정보 보기

AP([Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)) 또는 AT([자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) 활동을 만드는 동안 컨트롤로 사용할 환경을 선택할 수 있습니다.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 환경으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대해 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

자세한 내용은 [특정 환경을 제어로 사용](/help/main/c-activities/t-automated-personalization/experience-as-control.md)을 참조하십시오.

+++

## [!UICONTROL Automated Personalization]을(를) 기본 경험과 비교하려면 어떻게 해야 합니까? {#section_46C1A620A2384C2C8392D6716DD18495}

+++세부 정보 보기

[!UICONTROL Automated Personalization]을(를) 기본 경험과 비교하는 턴키 옵션이 없습니다. 그러나 해결 방법으로, 기본 오퍼 또는 경험이 전체 활동의 일부로 존재하는 경우 기준 성능을 이해하려면 보고서에서 &quot;[!UICONTROL Control]&quot; 세그먼트를 클릭하고 결과 오퍼 수준 보고서에서 해당 특정 오퍼를 찾습니다. 이 오퍼에 대해 기록된 전환율을 사용하여 전체 &quot;Random Forest&quot; 세그먼트의 대화율과 비교할 수 있습니다. 이렇게 하면 기본 오퍼와 비교하여 시스템이 수행하는 방식을 비교하는 데 도움이 됩니다.

+++

## [!UICONTROL Automated Personalization] 활동을 설정하는 모범 사례는 무엇입니까? {#section_E155B26282BE49B58EA2683413D11DE6}

+++세부 정보 보기

* 낮은 트래픽의 페이지를 개인화하려는 경우 또는 개인화하고 있는 경험을 구조적으로 변경하려면 [!UICONTROL Auto-Target] 대신 [!UICONTROL Automated Personalization] 활동을 사용하는 것이 좋습니다. [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 참조하세요.
* [!UICONTROL A/B Test] 활동에서 사용할 오퍼와 위치 간에 [!UICONTROL Automated Personalization] 활동을 완료하여 위치 및 오퍼가 최적화 목표에 영향을 주는지 확인해 보십시오. [!UICONTROL A/B Test] 활동이 상당한 차이를 보이지 않는 경우 [!UICONTROL Automated Personalization]도 향상되지 않을 수 있습니다.

   * A/B...N 테스트에서 경험 간에 통계적으로 중요한 차이가 없는 경우 다음 상황 중 하나 이상이 원인일 수 있습니다.

      * 오퍼는 서로 충분히 다르지 않을 수 있습니다.
      * 선택한 위치는 성공 지표에 영향을 주지 않습니다.
      * 전환 단계에서 최적화 목표가 너무 멀어서 선택한 오퍼의 영향을 받을 수 없습니다.

* [&#x200B; 활동에서 개인화 모델을 만드는 데 걸리는 시간을 파악할 수 있도록 &#x200B;](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714)트래픽 견적 도구[!UICONTROL Automated Personalization]를 사용하십시오.
* 목표를 기반으로 활동을 시작하기 전에 통제와 타깃팅 간의 할당을 결정합니다.

  활동의 목표와 선택한 제어 유형에 따라 고려할 시나리오가 세 가지가 있습니다.

   * **제어 및 활동 목표로서의 무작위 경험은 개인화 알고리즘의 효과를 테스트하는 것입니다**: 개인화 알고리즘을 평가하는 것이 목표라면 리프트를 정확하게 파악하고자 합니다. 단순히 [!UICONTROL A/B Test]&#x200B;(임의로 제공된 제어)을 수행한 경우 경험 또는 오퍼에 대한 전환율을 비교하려고 할 수도 있습니다. 이 경우, 임의로 제공된 환경에 대한 제어에 50% 할당을 사용하는 것이 좋습니다.
   * **&quot;무작위 경험&quot;을 제어 및 활동 목표로 사용하여 개인화된 트래픽을 최대화하는 것입니다**: 알고리즘을 사용하는 데 익숙하고 최대 트래픽 양을 개인화하려는 경우 제어에 10%~30%를 할당하는 것이 좋습니다. 여기서 장점은 리프트 정보에 표시되는 정확도입니다. 제어 트래픽으로 유입되는 트래픽이 감소하므로 제어 트래픽의 신뢰 구간이 더 큽니다.
   * **다음 두 가지 목표 유형을 사용하여 특정 경험을 제어로 사용**: 특정 마케터 중심의 경험을 개인화 모델과 비교하려면 제어의 10%~30% 할당이 권장됩니다. 한 개의 경험만 제어로 선택하면 활동의 모든 오퍼 또는 경험에 트래픽이 분산되지 않습니다.

* 타깃팅 규칙은 모델의 최적화 기능을 방해할 수 있으므로 가능한 한 덜 사용해야 합니다.
* 보고 그룹은 [!UICONTROL Automated Personalization] 활동의 성공을 제한할 수 있습니다. 특정 조건에서만 보고 그룹 사용:

   * 다음 조건이 충족되는 경우에만 보고 그룹을 사용하십시오.

      * 활동이 실행되는 동안 새 오퍼를 바꾸거나 추가할 계획입니다.
      * 보고 그룹의 오퍼는 동일한 방문자에게 어필됩니다.
      * 해당 보고 그룹의 오퍼의 전체 응답률은 거의 동일합니다.

   * 보고 그룹의 오퍼 간에는 개인화가 없습니다. 오퍼는 개인화 모델에 의해 모두 동일하게 처리됩니다.
   * 활동에 있는 모든 오퍼를 하나의 보고 그룹에 넣지 마십시오. 이렇게 하면 활동의 모든 방문자에게 모든 오퍼가 균일하게 임의로 제공됩니다.

+++

## [!UICONTROL Automated Personalization]에 제한이 있습니까? {#section_08BA09ED51B547299963C94FE6417CFA}

+++세부 정보 보기

[!DNL Target]은(는) 30,000개의 경험으로 제한되어 있지만 10,000개 미만의 경험이 만들어졌을 때 가장 잘 작동합니다.

이 제한은 활동이 [!UICONTROL Disalow Duplicates] 옵션을 활성화한 경우에도 적용됩니다.

[!DNL Target]의 활동 및 기타 요소에 영향을 주는 문자 제한 및 기타 제한(오퍼 크기, 대상, 프로필, 값, 매개 변수 등)에 대한 자세한 내용은 [제한](/help/main/r-troubleshooting-target/target-limits.md)을 참조하십시오.

+++

## 오퍼 수준의 타깃팅은 어떻게 구현합니까? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++세부 정보 보기

각 방문자가 도착하면 방문자가 볼 수 있는 가능한 오퍼 세트가 오퍼 수준 타깃팅 규칙에 따라 결정됩니다. 그런 다음 알고리즘에서는 모델이 예측하는 오퍼가 해당 오퍼 중에서 가장 기대하는 매출이나 전환 가능성이 가장 큰 오퍼를 선택합니다. 오퍼 타깃팅은 [!DNL Target] 머신 러닝 알고리즘의 효과에 영향을 미치므로, 가능한 한 드물게 사용해야 합니다.

+++

## [!UICONTROL Automated Personalization] 활동에 상승도가 표시되지 않는 이유는 무엇입니까? {#section_BFA07C8C258F45318F73A461B8F32737}

+++세부 정보 보기

[!UICONTROL Automated Personalization] 활동에서 상승도를 생성하는 데에는 네 가지 요소가 필요합니다.

* 각 위치의 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 위치는 최적화 목표에 영향을 주는 위치여야 합니다.
* 활동에 상승도를 감지하기에 충분한 트래픽 및 통계적 검정력이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

가장 좋은 작업 방침은 먼저 활동 경험을 구성하는 콘텐츠와 위치가 간단한 개인화되지 않은 [!UICONTROL A/B Test] 활동을 사용하는 전반적인 응답률과 분명한 차이가 있는지 확인하는 것입니다. 반드시 미리 샘플 크기를 계산하여, 지정된 시간에 실행을 중단하거나 변경하지 않고도 적당한 상승도를 확인하고 A/B 테스트를 실행할 수 있는 전원이 있는지 확인하십시오. A/B 테스트 결과가 하나 이상의 경험에서 통계적으로 유의한 상승도를 보이면 개인화된 활동이 성공할 가능성이 높습니다. Personalization은 경험의 전체 응답률에 차이가 없어도 작동할 수 있습니다. 일반적으로 이 문제는 통계적 유의성을 가지고 감지할 최적화 목표에 충분히 큰 영향을 주지 않는 오퍼 또는 위치에서 비롯됩니다.

자세한 내용은 [자동화된 개인화 문제 해결](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA)을 참조하십시오.

+++

## [!UICONTROL Automated Personalization]이(가) 내 활동의 트래픽을 어떻게 할당합니까? {#section_4369364F77804E0D9B78BEE551DA5659}

+++세부 정보 보기

[!UICONTROL Automated Personalization]은(는) 각 모델을 위해 만들어진 가장 최신 [랜덤 포레스트](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) 모델을 기반으로 가장 높게 예측된 성공 지표가 있는 경험으로 방문자를 보냅니다. 이러한 예측은 방문자의 특정 정보와 방문 컨텍스트를 기반으로 합니다.

예를 들어, [!UICONTROL Automated Personalization] 활동에 각각 두 개의 오퍼가 있는 두 개의 위치가 있다고 가정해 봅시다. 첫 번째 위치에서 오퍼 A는 특정 방문자에 대한 예측 전환율이 3%이고 오퍼 B는 예측 전환율이 1%입니다. 두 번째 위치에서 오퍼 C는 동일한 방문자에 대한 예측 전환율이 2%이고 오퍼 D는 예측 전환율이 5%입니다. 따라서 [!UICONTROL Automated Personalization]은(는) 이 방문자에게 오퍼 A와 오퍼 D에 대한 경험을 제공합니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동을 언제 중지해야 합니까? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++세부 정보 보기

[!UICONTROL Automated Personalization]은(는) 항상 최적화되는 &quot;항시적&quot; 개인화로 사용할 수 있습니다. 특히 항상 사용되는 콘텐츠의 경우 [!UICONTROL Automated Personalization] 활동을 중지할 필요가 없습니다. 현재 [!UICONTROL Automated Personalization] 활동에 있는 오퍼와 유사하지 않은 콘텐츠를 크게 변경하려면 새 활동을 시작하는 것이 좋습니다. 새 활동을 시작하면 보고서를 검토하는 다른 사용자가 과거 결과를 다른 콘텐츠와 혼동하거나 관련시키지 않도록 할 수 있습니다.

+++

## 모델이 만들어지기까지 얼마나 기다려야 합니까? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++세부 정보 보기

일반적으로 활동에서 모델을 만드는 데 걸리는 시간은 선택한 활동 위치에 대한 트래픽과 활동 성공 지표에 따라 다릅니다. [트래픽 견적 도구](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714)를 사용하여 활동에서 모델을 만드는 데 걸리는 예상 시간을 결정합니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동 내에 모델 하나가 만들어져 있습니다. 해당 경험에 대한 방문이 개인화됩니까? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++세부 정보 보기

아니요. 개인화를 시작하려면 활동에 만들어져 있는 모델이 두 개 이상이라야 합니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동의 결과는 언제 볼 수 있습니까? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++세부 정보 보기

모델이 만들어져 있는 경험용으로 모델이 있는 경험을 두 개 이상 만들면(녹색 확인 표시) 그때부터 [!UICONTROL Automated Personalization] 활동의 결과를 볼 수 있습니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동에서 모델을 만드는 데 필요한 시간을 줄이려면 어떻게 해야 합니까? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++세부 정보 보기

활동 설정을 검토하고 모델이 만들어지는 속도를 개선하기 위해 기꺼이 변경할 사항이 있는지 확인하십시오.

* 성공 지표가 활동 경험에서 판매 경로의 아래쪽에 있습니까? 활동 전환율이 낮으면 최소의 전환 횟수가 필요하므로 모델 작성에 필요한 트래픽 요구 수준이 늘어납니다.
* 성공 지표가 RPV로 설정된 경우 전환으로 변경할 수 있습니까? 전환 활동은 일반적으로 모델을 만드는 데 필요한 트래픽이 적습니다. 
* 활동에서 삭제할 수 있는 경험이 있습니까? 활동에서 경험 수를 줄이면 모델을 만드는 시간이 빨라집니다.
* 이 활동이 더 성공할 수 있는 더 높은 트래픽 페이지가 있습니까? 활동 위치에 트래픽과 전환이 많을수록 모델이 더 빨리 구축됩니다.

+++

## 방문자에게 표시되지 않아야 하는 [!UICONTROL Automated Personalization] 활동에 대한 경험이 방문자에게 표시되는 이유는 무엇입니까? {#section_41CECEAE0881446A8D9F3B016857914B}

+++세부 정보 보기

[!UICONTROL Automated Personalization]개의 활동이 세션당 한 번 평가됩니다. 특정 경험에 적합한 활성 세션이 있고 이제 여기에 새 오퍼가 추가된 경우 방문자는 이전에 표시된 오퍼와 함께 새 콘텐츠를 보게 됩니다. 이러한 방문자는 이전에 해당 경험에 대한 자격이 있었으므로 세션 중에 이러한 경험을 계속 보게 됩니다. 모든 페이지 방문 시 이를 평가하려면 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동 유형으로 변경해야 합니다.

+++

## [!UICONTROL Automated Personalization] 활동 중간에 목표 지표를 변경할 수 있습니까? {#change-metric}

+++세부 정보 보기

[!DNL Adobe]은(는) 활동 중간에 목표 지표를 변경하지 않는 것이 좋습니다. [!DNL Target] UI를 사용하는 활동 중에 목표 지표를 변경할 수 있지만 항상 새 활동을 시작해야 합니다. [!DNL Adobe]은(는) 활동이 실행된 후 목표 지표를 변경하면 어떻게 되는지 보증하지 않습니다.

이 권장 사항은 [!UICONTROL Auto-Allocate] 또는 [!UICONTROL Auto-Target]&#x200B;(A4T)을 보고 소스로 사용하는 [!UICONTROL Automated Personalization], [!DNL Target] 및 [!DNL Analytics] 활동에 적용됩니다.

+++

## [!UICONTROL Reset Report Data] 활동을 실행하는 동안 [!UICONTROL Automated Personalization] 옵션을 사용할 수 있습니까?

+++세부 정보 보기

[!DNL Adobe]은(는) [!UICONTROL Reset Report Data] 활동에 대해 [!UICONTROL Automated Personalization] 옵션을 사용하지 않는 것이 좋습니다. 이 옵션을 사용하면 표시되는 보고 데이터는 제거되지만 [!UICONTROL Automated Personalization] 모델에서 모든 교육 기록이 제거되지는 않습니다. [!UICONTROL Reset Report Data] 활동에 [!UICONTROL Automated Personalization] 옵션을 사용하는 대신 새 활동을 만들고 원래 활동을 비활성화하십시오. 이 지침은 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동에도 적용됩니다.

+++

## [!UICONTROL Automated Personalization]은(는) 환경과 관련하여 모델을 어떻게 구축합니까?

+++세부 정보 보기

한 가지 모델이 만들어져 무작위로 제공되는 트래픽과 전체 우승 경험에 모든 트래픽을 보내는 개인화 전략의 성능을 식별합니다. 이 모델은 기본 환경에서만 히트 및 전환을 고려합니다.

두 번째 모델 집합의 트래픽은 각 모델링 그룹([!UICONTROL Automated Personalization]) 또는 경험([!UICONTROL Auto-Target])에 대해 빌드됩니다. 이러한 각 모델에 대해 모든 환경의 히트 및 전환이 고려됩니다.

따라서 환경에 관계없이 동일한 모델에서 요청이 제공됩니다. 그러나, 복수의 트래픽은 식별된 전체 우승 경험이 실제 동작과 일관되도록 기본 환경에서 가져와야 합니다.

+++
