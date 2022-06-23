---
keywords: AB;A/B;AB...n;샘플 크기;샘플 크기 계산기;자동 할당;자동 할당;계산기
description: Learn how long to run an A/B test. Adobe에서 성공적인 A/B 테스트 [!DNL Target] 전환율을 높이려면 충분한 방문자(샘플 크기)가 필요합니다.
title: A/B 테스트를 얼마 동안 실행해야 합니까?
feature: A/B Tests
exl-id: 4f4ce387-bbbe-44af-965b-affc3ee09d74
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '3060'
ht-degree: 63%

---

# A/B 테스트를 얼마 동안 실행해야 합니까?

성공 [!UICONTROL A/B 테스트] 활동 [!DNL Adobe Target] 전환율을 높이려면 충분한 방문자(샘플 크기)가 필요합니다. A/B 테스트를 얼마 동안 실행해야 하는지 어떻게 알 수 있습니까? 이 문서에는 [!UICONTROL 자동 할당] 활동 및 [!UICONTROL Adobe Target] 활동에 목표를 달성할 수 있는 충분한 방문자가 있는지 확인하는 데 도움이 되는 샘플 크기 계산기.

오퍼들 중 하나의 성과가 활동의 처음 몇 일 내에 다른 오퍼보다 훨씬 더 낫거나 훨씬 나쁘면 활동을 중지하려는 마음이 생길 수 있습니다. 그러나 관찰 수가 낮으면 낮은 방문자 수에 대해 전환율 평균을 내므로 뜻밖에 양수 상승도나 음수 상승도가 관찰될 가능성이 높습니다. 활동이 더 많은 데이터 포인트를 수집함에 따라, 전환율이 해당하는 실제 장기간 값에 수렴합니다.

>[!IMPORTANT]
>
>활동을 조기에 중지하는 것은 A/B 테스트를 수행할 때 발생할 수 있는 10가지 중요한 위험 중 하나입니다. 자세한 내용은 [10가지 공통 A/B 테스트 위험 및 방지 방법](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md#concept_578A7947C9554868B30F12DFF9E3F8E3).

[!DNL Adobe Target] 은 활동 크기가 전환 목표를 달성하는 데 도움이 되는 충분한 샘플 크기를 갖도록 하는 도구를 제공합니다. 자동 할당.

## 자동 할당 {#auto-allocate}

An [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 활동은 두 개 이상의 경험에서 승자를 식별하는 A/B 테스트의 유형입니다. 자동 할당 테스트는 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다.

표준 A/B 테스트에는 기본 비용이 있습니다. 각 경험의 성과를 측정하고 분석을 통해 가장 성과가 좋은 경험을 알아내는 데 트래픽을 사용해야 합니다. 일부 경험이 다른 경험에 비해 성과가 더 좋다는 것을 인지한 후에도 트래픽 분배가 고정적으로 유지됩니다. 또한 샘플 크기를 알아내는 것도 복잡하며, 활동의 전체 과정을 실행해야 승자에 대해 작업할 수 있습니다. 그리고 식별된 승자가 진정한 승자가 아닐 가능성이 여전히 있습니다.

The solution is [!UICONTROL Auto-Allocate]. [!UICONTROL 자동 할당은 이러한 비용과 우승 경험을 알아내는 데 드는 오버헤드를 줄여줍니다. ] [!UICONTROL 자동 할당 기능에서는 모든 경험의 목표 지표 성과를 모니터링하고, 성과가 좋은 경험에는 비례하여 더 많은 새 참여자를 보냅니다. ] 다른 경험을 탐색하도록 충분한 트래픽이 예약되어 있습니다. You can see the benefits of the activity on your results, even while the activity is still running: optimization occurs in parallel with learning.

[!UICONTROL 자동 할당은 활동을 끝까지 수행하여 승자를 완전히 판별할 때까지 기다리게 하기보다는 방문자를 성과가 우승 경험으로 점차적으로 이동시킵니다. ] 덜 성공적인 경험으로 보내졌을 활동 참여자가 잠재적으로 우승 경험으로 표시되므로 더 빠른 성과 향상(상승도)의 혜택을 얻을 수 있습니다.

[!UICONTROL 자동 할당] 기능을 사용하는 경우 [!DNL Adobe Target]에서는 활동이 충분히 신뢰할 수 있는 최소 전환 수에 도달하기 전까지 활동의 페이지 상단에 &quot;아직 우승자 없음&quot; 배지가 표시됩니다. [!DNL Target] then declares the winning experience by displaying a badge at the top of the activity&#39;s page.

For more information, see [Auto-Allocate overview](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

## Adobe [!DNL Target] 샘플 크기 계산기 {#section_6B8725BD704C4AFE939EF2A6B6E834E6}

If you choose to use a manual [!UICONTROL A/B Test] activity rather than [!UICONTROL Auto-Allocate], the [!DNL Target] Sample Size Calculator helps you determine the sample size needed for a successful test. 수동 A/B 테스트는 고정된 수평선 테스트이므로 계산기가 유용합니다. Using the calculator for an [!UICONTROL Auto-Allocate] activity is optional because [!UICONTROL Auto-Allocate] declares a winner for you. 계산기는 필요한 샘플 크기를 대략적으로 추정합니다. 계산기 사용 방법에 대한 자세한 내용을 계속 확인하십시오.

A/B 테스트를 설정하기 전에 Adobe Target에 액세스하십시오 [샘플 크기 계산기](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=ko-KR).

![Adobe Target 샘플 크기 계산기](/help/main/c-activities/t-test-ab/assets/sample_size_calculator-new.png)

It is important to determine an adequate sample size (number of visitors) before doing any A/B test in order to establish the time that the activity should run before evaluating the results. Simply monitoring the activity until statistical significance is achieved causes the confidence interval to be vastly underestimated, making the test unreliable. 이러한 결과 때문에 통계적으로 유의미한 결과가 감지되는 경우 테스트가 중지되고 승자가 선언됩니다. 그러나 결과가 통계적으로 유의미하지 않다면 테스트는 계속될 것이고, 이러한 절차는 긍정 오류(false positive) 비율을 증가시키는 긍정적인 결과를 매우 편애하는 것이므로, 테스트의 유효한 유의 수준이 왜곡됩니다.

This can result in many false positives, which leads to implementation of offers that do not deliver the predicted lift in the end. 향상도가 나쁘면 그 자체가 만족스럽지 않은 결과이지만, 더 심각한 결과는 시간이 지나면서 정확히 예측하지 못하는 것이 실제 실험으로 조직적 신뢰를 손상시키는 것이다.

이 문서에서는 샘플 크기가 결정될 때 균형을 맞춰야 하는 요소들에 대해 설명하고 적절한 샘플 크기 예측을 위한 스프레드시트 계산기를 소개합니다. A/B 테스트가 시작되기 전에 샘플 크기 계산기(위에 제공된 링크)를 사용하여 샘플 크기를 계산하면 통계적 표준을 준수하는 고품질 A/B 테스트를 항상 실행할 수 있습니다.

A/B 테스트를 정의하는 5개의 사용자 정의 매개 변수가 있습니다. 이 매개 변수는 상호 연결되어 있으므로 네 개 매개 변수를 설정하면 다섯 번째 매개 변수를 계산할 수 있습니다.

* 통계적 유의도
* 통계적 검증력
* 확실히 감지 가능한 최소 상승도
* 베이스라인 전환율
* 방문자 수

A/B 테스트의 경우, 통계적 유의도, 통계적 검증력, 확실히 감지 가능한 최소 상승도 및 베이스라인 전환율은 분석가에 의해 설정되며 그런 다음 필요한 방문자 수가 이러한 수치들로부터 계산됩니다. This article discusses these elements and gives guidelines for how to determine these metrics for a specific test.

![](assets/samplesize.png)

아래 그림은 A/B 테스트의 네 가지 가능한 결과를 보여줍니다.

![](assets/outcomes.png)

긍정 오류(false positive) 또는 부정 오류(false negative)가 발생하지 않는 것이 좋지만, However, obtaining zero false positives can never be guaranteed by a statistical test. 관찰된 트렌드가 기본 전환율을 대표하지 않을 가능성은 항상 있습니다. 예를 들어, 동전의 앞면이나 뒷면이 더 가능성이 있는지 확인하기 위한 테스트에서, 비록 공정한 동전으로 할지라도, 여러분은 우연한 기회에 10개의 면에서도 10개의 앞면을 얻을 수 있습니다. 통계적 유의도 및 검증력은 긍정 오류(false positive)와 부정 오류(false negative) 비율을 결정하는 데 도움이 되며, 지정된 테스트에 대해 이러한 비율을 합리적인 수준으로 유지할 수 있도록 해줍니다.

### 통계적 유의도 {#section_8230FB9C6D1241D8B1786B72B379C3CD}

테스트의 유의 수준은 실제로 실제 차이가 없을 때, 테스트가 두 개의 다른 오퍼 간의 전환율에 중요한 차이를 보고하는지 여부를 결정합니다. This situation is known as a false positive or a Type I error. 유의 레벨은 사용자가 지정한 임계값이며 긍정 오류(false positive)에 대한 허용치와 테스트에 포함되어야 하는 방문자 수 간의 차수입니다.

A/B 테스트를 시작할 때에는 두 오퍼의 전환율이 모두 동일하다고 가정합니다. 그런 다음 관찰된 결과의 확률을 이 가정을 기반으로 계산합니다. 이 확률(p-값)이 일부 사전 정의된 임계값(중요도 수준)보다 작은 경우, [!DNL Target] 에서는 두 오퍼가 동일한 전환율을 가지며, 초기 가정이 잘못되었다고 가정합니다. 따라서 A와 B의 전환율은 주어진 유의 수준에서 통계적으로 다릅니다.

A/B 테스트에서 일반적으로 사용되는 유의 수준은 5%이며 이는 95% 신뢰 수준에 해당합니다(신뢰 수준 = 100% - 유의 수준). 신뢰 수준 95%는 테스트를 수행할 때마다, 오퍼 간 차이가 없더라도 통계적으로 유의미한 상승도를 감지할 확률이 5% 있음을 의미합니다.

신뢰 수준에 대한 일반적인 해석은 아래 표에 요약되어 있습니다.

| 신뢰도 수준 | 해석 |
|--- |--- |
| &lt; 90% | 전환율 간에 차이가 있다는 증거가 없음 |
| 90 ~ 95% | 전환율 간에 차이가 있다는 증거가 약함 |
| 95 ~ 99% | 전환율 간에 차이가 있다는 증거가 보통임 |
| 99 ~ 99.9% | 전환율 간에 차이가 있다는 증거가 강함 |
| +99.9% | 전환율 간에 차이가 있다는 증거가 매우 강함 |

항상 95% 이상의 신뢰 수준을 사용하는 것이 좋습니다.

It is desirable to use the highest possible confidence level, so that the test yields few false positives. 그러나 높은 신뢰 수준을 사용할수록 더 많은 수의 방문자가 필요하며 그럴 경우 테스트를 수행하는 데 필요한 시간이 늘어납니다. 또한 신뢰 수준이 증가하면 통계적 검증력은 감소합니다.

### 통계적 검증력 {#section_1169C27F8E4643719D38FB9D6EBEB535}

A/B 테스트의 통계적 검증력은 특정 규모의 전환율에서 실제 차이를 감지하는 확률입니다. 전환 이벤트의 무작위(확률론적) 특성으로 인해 두 오퍼 간의 실제 전환율 차이가 있더라도 통계적으로 유의미한 차이가 관찰되지 않을 수 있습니다(단순한 우연으로). 이 시나리오를 false 음수 또는 유형 II 오류라고 합니다.

통계적 유의도와 대조적으로 통계적 검증력의 결정은 A/B 테스트를 수행하지 않아도 되므로 통계적 검증력은 종종 무시됩니다. 그러나 통계적 검증력을 무시하면, 너무 작은 샘플 크기로 인해 다양한 오퍼의 전환율 간 실제 차이가 테스트에서 감지되지 않을 가능성이 큽니다. 이렇게 되면 긍정 오류(false positive)가 테스트를 지배합니다.

따라서 테스트에서 실질적인 전환율 차이를 식별할 가능성이 크고, 부정 오류(false negative)가 많이 나오지 않도록 높은 통계적 검증력을 확보하는 것이 바람직합니다. However, a larger number of visitors are required to increase the statistical power of detecting any given lift, which increases the time required to do the test.

통계적 검증력에 일반적으로 사용되는 값은 80%이며, 이 값은 테스트에서 확실히 감지 가능한 최소 상승도와 같은 차이를 감지할 확률이 80%임을 의미합니다. 이 테스트에서는 작은 상승도를 감지할 확률은 낮고, 큰 상승도를 감지할 확률은 높습니다.

### 확실히 감지 가능한 최소 상승도 {#section_6101367EE9634C298410BBC2148E33A9}

작은 상승도라도 구현할 가치는 있으므로 대부분의 조직은 전환율에서 가장 작은 가능한 차이를 측정하려고 합니다. 하지만 A/B 테스트가 작은 상승도를 감지할 가능성이 높은 것으로 하려면 테스트에 포함되어야 하는 방문자 수는 엄청나게 커질 수 있습니다. 그 이유는 전환율 차이가 작은 경우 두 전환율을 높은 정확도로 예측하여 차이를 식별해야 하므로 많은 방문자가 필요하기 때문입니다. 따라서 확실히 감지 가능한 최소 상승도는 작은 상승도를 감지하는 것과 오랜 시간 동안 테스트를 실행하는 것 사이의 균형점을 고려하는 비즈니스 요구 사항으로 결정해야 합니다.

예를 들어, 두 오퍼(A 및 B)의 실제 전환율이 각각 10%와 15%라고 가정할 때, 이 오퍼들이 각각 100명의 방문자에게 표시된다면 전환의 확률론적 특성으로 인해 오퍼 A의 경우 4% ~ 16% 범위, 오퍼 B의 경우 8% ~ 22% 범위의 전환율을 관찰할 확률은 95% 있습니다. 이 범위들은 통계에서 신뢰 구간이라고 하며, 예상 전환율의 정확성에 대한 신뢰도를 나타냅니다. 샘플 크기가 클수록(더 많은 방문자) 전환율의 추정값이 정확하다는 것을 더 확신할 수 있습니다.

아래 그림은 이러한 확률 분포를 보여줍니다.

![](assets/probability_distributions.png)

두 범위가 크게 겹치므로 이 테스트는 전환율이 다른지 여부를 판결할 수 없습니다. 따라서 방문자가 100명인 이 테스트는 두 오퍼를 구별할 수 없습니다. However, if Target exposes the offers to 5,000 visitors each, then there is a 95% chance that the observed conversion rates fall in the ranges of 9% to 11% and 14% to 16%, respectively.

![](assets/probability_distributions2.png)

이 경우 테스트가 잘못된 결론에 도달하지는 않으므로 5,000명의 방문자가 있는 테스트는 두 오퍼를 구별할 수 있습니다. 방문자가 5,000명인 테스트의 신뢰 구간은 약 +/-1%입니다. 이것은 테스트에서 약 1%의 차이를 감지할 수 있음을 의미합니다. 따라서 오퍼의 실제 전환율이 10%와 15%가 아니라 10%와 10.5%처럼 1% 미만의 차이가 나는 경우에는 훨씬 더 많은 방문자가 필요합니다.

### 베이스라인 전환율 {#section_39380C9CA3C649B6BE6E1F8A06178B05}

베이스라인 전환율은 통제 오퍼(오퍼 A)의 전환율입니다. 종종 이전 경험을 기반으로 오퍼의 전환 수준을 적절하게 파악할 수 있습니다. 새 유형의 오퍼 또는 크리에이티브인 이유로 파악하기 어려운 경우에는, 샘플 크기 계산에 사용할 수 있는 대략적인 베이스라인 전환율 추정치를 얻을 수 있도록 테스트를 하루 동안 실행할 수 있습니다.

### 방문자 수 {#section_19009F165505429E95291E6976E498DD}

장시간 동안의 테스트 실행 기회비용과 긍정 오류(false positive) 및 부정 오류(false negative)의 위험 사이에 균형을 이루는 것은 어려울 수 있습니다. 분명, 틀린 결정을 내려서도 안 되지만 너무 엄격하거나 융통성 없는 테스트 표준으로 인해 테스트가 무력해지는 것도 바람직하지 않습니다.

따라서 일반 지침으로서 95% 신뢰 수준과 80% 통계적 검증력이 권장됩니다.

샘플 크기 계산기(위에 제공된 링크)는 통계적 유의도(권장: 95%) 및 통계적 검증력(권장: 80%)으로 결정하도록 요구합니다. 모든 오퍼에 대한 베이스라인 전환율과 일별 트래픽을 입력하면 스프레드시트에서는 테스트의 지정된 검증력과 동일한 확률로 1%, 2%, 5%, 10%, 15%, 20%의 상승도를 감지하는 데 필요한 방문자 수를 출력합니다. 사용자가 스프레드시트에서 확실히 감지 가능한 사용자 지정 최소 상승도를 입력할 수도 있습니다. 더욱이 스프레드시트에서는 사용자가 입력한 트래픽 수준을 기반으로 테스트에 필요한 주 수를 출력합니다. 필요한 주 수는 결과에 영향을 미치는 요일 효과를 방지하기 위해 가장 가까운 정수로 올림됩니다.

테스트에서 확실히 식별할 수 있는 최소 상승도와 필요한 방문자 수 간에는 균형점이 있습니다. 베이스라인(통제) 전환율 5%에 유효한 아래 그림에서는 방문자 수를 늘리기 위한 급격히 감소하는 수익을 보여줍니다. 확실히 감지할 수 있는 최소 상승도는 테스트에 처음 몇 명의 방문자를 추가할 때에는 엄청나게 개선되지만, 테스트를 개선하기 위해서는 점점 더 많은 방문자를 필요로 합니다. 이 그림은 테스트를 실행하는 데 필요한 시간(필요한 방문자 및 사이트 트래픽에 의해 결정된 대로)과 테스트에서 확실히 감지할 수 있는 최소 상승도 간의 적절한 균형점을 찾는 데 도움이 됩니다.

![](assets/samplesizecontrol.png)

이 예에서는 100개의 테스트 중 80개에서 5%(대안 오퍼의 전환율(100%+5%)*5% = 5.25%에 해당)의 상승도를 감지할 수 있는 것이 적절하고, 따라서 각 오퍼에 대해 100,000명이라는 방문자 샘플 크기가 필요하다고 결정할 수 있습니다. 사이트에 하루에 20,000명의 방문자가 있고 두 개의 오퍼를 테스트하는 중이라면, 대안 오퍼가 통제 오퍼보다 통계적으로 유의미하게 우수한지 여부를 판별하려면 먼저 2*100,000/20,000 = 10일 동안 테스트를 실행할 수 있어야 합니다.

이때도 필요한 시간은 요일 효과가 방지하도록 항상 가장 가까운 정수 주 수로 올림하는 것이 좋습니다. 따라서 이 예에서는 결과를 평가하기 전 2주 동안 테스트가 실행됩니다.

### 방문당 수입(RPV) 지표 {#section_C704C0861C9B4641AB02E911648D2DC2}

방문당 수입(RPV)을 지표로 사용할 때 RPV는 주문당 수익과 전환율의 곱(RPV = 수익 / 방문자# = (주문당 수익 * 주문#) / 방문자# = 주문당 수익 * (방문자# * CTR) / 방문자# = 주문당 수익 * CTR)이고 각각은 자체 변화가 있으므로 추가적인 변화 소스가 추가됩니다. 전환율의 분산은 수학 모델을 사용하여 직접 추정할 수 있지만 주문당 수익의 분산은 활동에 따라 다릅니다. 따라서, 과거 활동에서 이러한 분산에 대한 지식을 사용하거나 며칠 동안 A/B 테스트를 실행하여 매출액의 분산을 예측합니다. 분산은 CSV 다운로드 파일에 있는 판매 합계, 판매 제곱 합계 및 방문자 수 값에서 계산됩니다. 설정이 완료되면 스프레드시트를 사용하여 테스트를 완료하는 데 필요한 시간을 계산합니다.

샘플 크기 계산기(위에 제공된 링크)는 RPV 지표를 구성하는 데 도움이 될 수 있습니다. 계산기를 열면 이라는 레이블이 지정된 탭이 표시됩니다 [!UICONTROL RPV 지표]. RPV 버전의 계산기를 사용할 때에는 다음 정보가 필요합니다.

* 통제 오퍼에 대한 방문자 수
* 통제 오퍼에 대한 총 수익

   Make sure the extreme order filter is selected.

* 통제 오퍼에 대한 수익 제곱의 합계

   예외적인 주문 필터가 선택되었는지 확인하십시오.

In general, using RPV as a metric requires 20-30% longer to achieve the same level of statistical confidence for the same level of measured lift. 이것은 RPV가 전환당 다른 주문 크기의 분산이 추가되었기 때문입니다. This should be a consideration when choosing between straight conversion rate and RPV as the metric on which to base your final business decision.

## 여러 오퍼를 비교하기 위한 보정 {#section_1474113764224D0B85472D8B023CCA15}

두 오퍼를 비교할 때마다 긍정 오류(false positive)를 얻을 확률(전환율에 차이가 없는 경우에도 통계적으로 유의미한 차이를 관찰하여)은 유의 수준과 동일합니다. 예를 들어, 5개의 오퍼 A/B/C/D/E가 있고 A가 통제 오퍼라면, 개의 비교가 수행되고(통제와 B, 통제와 C, 통제와 D, 통제와 E), 신뢰 수준이 95%일 때에도 긍정 오류(false positive)의 확률은 18.5%입니다. Pr(긍정 오류가 하나 이상) = 1 - Pr(긍정 오류가 없음) = 1 - 0.954 = 18.5%이기 때문입니다. 긍정 오류(false positive)는 대안과 통제 간에 사실상 차이가 없을 때 통제가 대안보다 낫다고 보고되거나 대안이 통제보다 낫다고 보고되는 것 중 하나로 정의되는 컨텍스트에서 발생합니다.

## 결론 {#section_AEA2427B90AE4E9395C7FF4F9C5CA066}

By using an [!UICONTROL Auto-Allocate] activity, [!DNL Target] identifies a winner among two or more experiences and automatically reallocates more traffic to the winner to increase conversions while the test continues to run and learn. [!UICONTROL 자동 지정을 통해 추측 작업을 제거하는 동시에 변환 목표를 쉽게 달성할 수 있습니다.]

이 문서에 도입된 샘플 크기 계산기(위에 제공된 링크)를 사용하여 테스트가 제안된 시간 동안 실행되도록 함으로써, 사용자가 결정한 잘못된 양수 및 잘못된 음수 비율을 준수하는 고품질 A/B 테스트를 항상 특정 테스트에 적합하도록 할 수 있습니다. 이렇게 하면 테스트가 일관되며 찾고 있는 상승도를 확실히 감지할 수 있습니다.