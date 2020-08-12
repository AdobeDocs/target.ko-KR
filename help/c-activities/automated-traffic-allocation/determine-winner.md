---
keywords: automated traffic allocation;targeting;winner;statistical guarantee;confidence;determine winner;lift;confidence;default;default experience
description: Target UI에서 표시를 보고 자동 할당 A/B 활동에서 승자를 결정합니다.
title: 승자 결정
feature: null
topic: Standard
uuid: 0bcc11b2-44bd-450c-a504-a8ff7a4d72e6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 49%

---


# 자동 할당 보고서 해석 {#determine-a-winner}

Target UI에서 리프트 및 신뢰도를 비롯한 중요한 지표를 검사하여 자동 할당 A/B 활동의 결과를 해석합니다.

많은 마케터가 결과가 명확한 승자를 표시하기 전에 가장 성과가 좋은 경험을 조급하게 선언합니다. 이제 승자를 결정하는 것이 쉬워졌습니다.

>[!NOTE]
>
>우승자 선언에 대한 일반적인 정보는 10 [가지 일반적인 A/B 테스트 문제와 이를 피하는 방법을 참조하십시오](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## 우승 경험 식별 {#section_24007470CF5B4D30A06610CE8DD23CE3}

[!UICONTROL 자동 할당] 기능을 사용하는 경우 [!DNL Target]에서는 활동이 충분히 신뢰할 수 있는 최소 전환 수에 도달하기 전까지 활동의 페이지 상단에 &quot;아직 우승자 없음&quot; 배지가 표시됩니다.

![우승자 배지 없음](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

명백한 승자를 선언할 때에는 [!DNL Target]에 &quot;우승자: 경험 X&quot;라고 표시됩니다.

![](assets/winner.png)

>[!NOTE]
>
>자동 할당 활동은 통제군과의 쌍별 비교를 수행할 뿐만 아니라 모든 선택 사항 중에서 최고의 경험을 찾도록 설계되었습니다.

## Statistical guarantees of Auto-Allocate {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

A/B 활동의 끝에서 자동 할당은 결정된 승자에 5%의 유효한 긍정 오류(false positive) 비율이 있다는 것을 보장합니다. 이것은 5% 동안만 결정된 승자가 활동의 모든 경험 중에서 실제로 최고의 경험이 아님을 의미합니다. A/A 테스트(동일한 경험 사용)의 경우에는 5% 미만으로 테스트 결론을 내립니다. A/A 테스트(동일한 경험 사용)에 대한 예상 동작은 무기한으로 실행되는 것이므로 승자 배지가 나타나지 않아야 합니다.

자동 할당에는 p 값 기반 신뢰도가 사용되지 않습니다.

자동 할당 활동의 신뢰도 열(아래 그림 참조)에는 경험이 1% 오차 범위 내에서 승자가 되는 확률이 표시됩니다(즉, 이 알고리즘에서는 1위와 2위 전환율 간에 최소 1%의 감지 가능한 효과를 사용합니다.). 이 알고리즘에서는 [Bernstein 부등식](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory))을 사용하여 이 확률을 계산합니다.

일반 A/B 테스트는 p 값을 기반으로 신뢰도를 계산합니다. 자동 할당에서는 p 값을 사용하지 않습니다. p 값은 주어진 경험이 통제 경험과 다를 확률을 &quot;대략&quot; 계산합니다. 이 p값은 경험이 통제 경험과 다른지 여부를 판별하는 데에만 사용할 수 있습니다. 이 값은 경험이 통제 경험이 아닌 다른 경험과 다른지 판별하는 데에는 사용할 수 없습니다.

>[!IMPORTANT]
>
>미리 정의된 최소 전환 수 후 우승자를 Target에 표시합니다.그러나 최종 선택은 언제나 Adobe Target [샘플 크기 계산기의 결과여야 한다](https://docs.adobe.com/content/target-microsite/testcalculator.html). Target은 사이트의 기본 전환율 및 활동 기간을 결정하기 위해 계산기로 제공되는 기타 중요한 측면을 고려하지 않습니다. 따라서 Target은 최소 전환 수를 기준으로 예상보다 빨리 우승자를 표시할 수 있습니다. 자세한 내용은 [샘플 크기 계산기를 참조하십시오](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## 자동 할당 활동의 리프트 및 신뢰도 보고 이해 {#lift-confidence}

자동 할당 활동에서 첫 번째 경험(기본적으로 경험 A)은 보고서 탭에서 항상 &quot;제어&quot; 경험으로 정의됩니다. 이 경험은 경험의 성능을 결정하는 데 사용되는 모델링에서 진정한 통계 컨트롤로 간주되지 않지만, 보고서의 일부 그림에 대한 참조나 기준선으로 처리됩니다.

각 경험에 대한 &quot;리프트&quot; 숫자 값과 95% 바운드는 정의된 &quot;제어&quot; 경험을 참조하여 항상 계산됩니다. 정의된 &quot;제어&quot; 경험에는 자신을 기준으로 한 리프트를 사용할 수 없으므로 이 경험에 대해 빈 &quot;—&quot; 값이 보고됩니다. A/B 테스트와 달리 자동 할당 테스트에서는 경험이 정의된 컨트롤보다 더 나쁜 경우 음수 리프트 값이 보고되지 않습니다.대신 &quot;—&quot;가 표시됩니다.

표시된 신뢰 구간 막대는 경험의 평균 예상 전환율의 95% 신뢰 구간을 나타냅니다. 또한 정의된 &quot;제어&quot; 경험과 관련하여 색상으로 구분됩니다. &quot;컨트롤&quot; 경험의 막대는 항상 회색으로 표시됩니다. &quot;제어&quot; 경험의 신뢰 구간 아래에 있는 신뢰 구간 부분은 빨간색으로 표시되고, &quot;제어&quot; 경험 위에 있는 신뢰 구간 부분이 녹색으로 표시됩니다.

선도적인 경험의 95% 신뢰 구간이 다른 경험과 겹치지 않으면 우승자가 발견되었습니다. 우승 경험은 경험 이름 왼쪽 및 &quot;우승자&quot; 배너에 녹색 별 배지가 있는 것으로 지정됩니다. 별이 보이지 않으면 배너가 &quot;아직 우승자 없음&quot;으로 표시되어 우승자를 아직 찾지 못했습니다.

&quot;신뢰&quot; 번호는 현재 선두 또는 우승 경험 옆에 보고됩니다. 이 수치는 선도적인 경험의 신뢰도가 최소 60%가 될 때까지만 보고됩니다. 자동 할당 실험에 정확히 두 개의 경험이 있는 경우 이 숫자는 경험이 다른 경험보다 성과가 더 좋은 신뢰 수준을 나타냅니다. 자동 할당 실험에 두 개 이상의 경험이 있는 경우 이 숫자는 정의된 &quot;제어&quot; 경험보다 경험이 더 잘 수행되는 신뢰 수준을 나타냅니다. &quot;Control&quot; 경험이 승리되는 경우 &quot;Confidence&quot; 수치는 보고되지 않습니다.

## FAQ {#section_C8E068512A93458D8C006760B1C0B6A2}

**활동을 시작한 지 며칠이 되었습니다. 모든 신뢰도 값이 여전히 0%로 표시되는 이유는 무엇입니까?**

모든 활동에 대해 보고서의 [!UICONTROL 신뢰도] 열에 0%가 표시되는 이유는 다음 중에 있습니다.

* 수동 A/B 테스트와 자동 할당이 서로 다른 통계를 사용하여 신뢰도 값을 표시합니다.

   수동 A/B 테스트는 [학생 t 검증(t-test)](https://en.wikipedia.org/wiki/Student%27s_t-test)에 기반한 p 값을 사용합니다. p 값은 실제로는 경험과 제어에서 관찰되는(또는 더 극단적인) 차이가 없다는 것을 감안할 때 그러한 차이를 찾을 확률입니다. 이러한 p 값은 관찰된 데이터가 주어진 경험과 일치하는지와 제어가 동일한지 여부를 결정하는 데만 사용할 수 있습니다. 이 값은 경험이 통제 경험이 아닌 다른 경험과 다른지 판별하는 데에는 사용할 수 없습니다.

   자동 할당은 주어진 경험이 활동의 모든 경험에 대해 실제 승자가 되는 확률을 표시합니다. 이것은 가장 성과가 좋은 경험(승자가 될 가능성이 가장 높은 경험)의 신뢰도 값만 0이 아님을 의미합니다. 다른 모든 경험은 패자가 될 가능성이 높으며 0%가 표시됩니다.

* 자동 할당은 가장 성과가 좋은 경험이 60% 신뢰도를 모은 후에만 신뢰도 표시를 시작합니다. 이러한 신뢰 수준은 일반적으로 일반 A/B 테스트를 완료하는 데 걸리는 약 2분 내에 나타납니다(보장되지는 않지만). To determine how long a normal A/B test would run, please use a [sample size calculator](https://docs.adobe.com/content/target-microsite/testcalculator.html): plug control&#39;s conversion-rate in &quot;Baseline conversion rate,&quot; &quot;5%&quot; for &quot;Lift,&quot; and 95% for &quot;Confidence.&quot; 일반적으로 신뢰도는 각 경험이 경험당 필요한 샘플을 50% 이상 축적하면 표시를 시작합니다. 이것으로 신뢰도 표시가 시작되는 시기를 알 수 있습니다.
* 보고서가 보드 전체에서 0%를 표시한다면 활동이 너무 이른 것일 수 있습니다.

