---
keywords: 보고서;통계 방법론;통계 계산;통계;평균;전환율;방문자당 매출;rpv;신뢰 구간;상승도;상승도 t-테스트;오프라인 계산
description: '[!UICONTROL A/B Test]의 수동  [!DNL Adobe Target] 활동에 사용되는 통계 계산에 대해 알아봅니다.'
title: '[!UICONTROL A/B Test] 활동에 사용되는 통계 계산에 대해 알아보려면 어떻게 해야 합니까?'
feature: Reports
exl-id: 5f7377b9-0567-4b6f-8968-4696b2088d0a
source-git-commit: 18f8ccd3edfda635c3f47bd67ff0b7a516748fa8
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 2%

---

# A/Bn 테스트의 통계 계산

이 문서에서는 [!DNL Adobe Target]의 수동 A/Bn 테스트에 사용된 자세한 통계 계산을 문서화합니다. [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate], [!UICONTROL Lift], [!UICONTROL Confidence Interval for Lift] 및 [!UICONTROL Confidence]에 대한 정의가 제공됩니다.

>[!NOTE]
>
>이 문서의 정보는 이전에 이 사이트에서 다운로드할 수 있었던 *A/B 테스트를 위한 Adobe Target 계산* pdf 파일을 대체합니다.

![A/B 테스트 활동의 [!UICONTROL Conversion Rate], [!UICONTROL Average Lift and Confidence Interval] 및 [!UICONTROL Confidence]을(를) 보여 주는 대상 보고서.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## 평균 성과

다음 섹션에서는 이전 그림에서 사용한 계산에 대해 설명합니다.

### RPV(방문자당 전환율 및 수익) 캠페인

다음 그림은 [!UICONTROL Conversion Rate] 보고서의 [!UICONTROL Confidence Interval of Conversion Rate], [!UICONTROL Conversions] 및 [!DNL Target] 수를 보여줍니다. 예를 들어 첫 번째 줄은 경험 A의 경우 [!UICONTROL Conversion Rate]이(가) 25.81%이고 [!UICONTROL Confidence Interval]이(가) ±7.7%이며 32개의 전환이 기록되었음을 보여 줍니다. 124명의 방문자가 이 경험을 봤다고 가정하면 32/124 = 25.81%에 해당합니다.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

실험에서 각 경험 **ν**&#x200B;에 대한 전환율 또는 *평균<sub>,</sub>*&#x200B;μ&#x200B;*ν*&#x200B;은 해당 지표에 할당된 단위 수 *N<sub>ν</sub>*&#x200B;에 대한 지표 합계의 비율로 정의됩니다.

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

여기에서,

* *Y<sub>iν</sub>*&#x200B;은(는) 주어진 경험 *ν*&#x200B;에 할당된 각 단위 *i*&#x200B;에 대한 지표 값입니다.

* 단위 *i*&#x200B;에 대한 합계는 계산 방법론의 선택에 따라 다릅니다.

   * *[!UICONTROL Visitors]*&#x200B;을(를) 계산 방법론으로 사용하는 경우 각 단위는 활동 기간 동안 활동에 고유한 참가자로 정의된 고유한 방문자입니다.
   * *[!UICONTROL Visits]*&#x200B;을(를) 계산 방법론으로 사용하는 경우, 각 단위는 [!DNL Target] 세션(고유한 `sessionId`을(를) 사용하는) 동안 경험의 고유한 참가자로 정의된 고유한 방문입니다. `sessionId`이(가) 변경되거나 방문자가 전환 단계에 도달하면 새 방문이 계산됩니다.
   * *[!UICONTROL Activity Impressions]*&#x200B;을(를) 계산 방법론으로 사용하는 경우 각 단위는 방문자가 활동의 페이지를 로드할 때마다 정의된 고유한 노출입니다.

## [!UICONTROL Confidence Interval of Mean]/[!UICONTROL Conversion Rate]

전환율의 신뢰 구간은 기본 데이터와 일치하는 가능한 전환율 범위로 직관적으로 정의된다.

실험을 실행할 때 주어진 경험에 대한 전환율은 &quot;true&quot; 전환율의 *estimate*&#x200B;입니다. 이 추정치에서 불확실성을 정량화하기 위해 [!DNL Target]은(는) 신뢰 구간을 사용합니다. [!DNL Target]은(는) 항상 95% 신뢰 구간을 보고합니다. 즉, 계산된 신뢰 구간의 95%에 경험의 실제 전환율이 포함되어 있습니다.

현재 선두이거나 우승한 경험 옆에도 &quot;신뢰도&quot; 수치가 보고됩니다. 이 수치는 선행 경험의 [!UICONTROL Confidence]이(가) 60% 이상에 도달할 때까지만 보고됩니다. 활동에 두 개의 경험이 있는 경우, 이 숫자는 경험이 다른 경험보다 더 잘 수행되고 있다는 신뢰 수준을 나타냅니다. 활동에 경험이 두 개 이상 있는 경우, 이 숫자는 정의된 &quot;제어&quot; 경험보다 경험이 더 잘 수행되고 있다는 신뢰 수준을 나타냅니다. 제어 경험이 이기는 경우 &quot;신뢰도&quot; 수치가 보고되지 않습니다.

전환율 *μ<sub>ν</sub>*&#x200B;의 95% 신뢰 구간이 값의 범위로 정의됩니다.

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

여기서 평균의 표준 오차는

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

샘플 표준 편차의 비편향 추정치를 사용하는 경우:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

캠페인이 전환율 캠페인(즉, 전환 지표가 이진수)인 경우 표준 오류는 다음과 같이 줄어듭니다.

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## 상승도

다음 그림은 [!UICONTROL Lift] 보고서의 [!UICONTROL Confidence Interval of Lift] 및 [!DNL Target]을(를) 보여 줍니다. 숫자는 상승도 한계 범위의 평균을 나타내고 화살표는 상승도가 양수이거나 음수이면 반영합니다. 신뢰도가 95%를 넘을 때까지 화살표가 회색으로 표시됩니다. 신뢰도가 임계값을 넘으면 양수 또는 음수 상승도를 기준으로 화살표가 녹색 또는 빨간색입니다.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

경험 *ν*&#x200B;과(와) 제어 경험 *ν<sub>0</sub>* 사이의 상승도는 다음으로 정의된 전환율에 있는 상대적 &quot;델타&quot;입니다.

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

여기서 개별 전환율은 위에서 정의된 대로 입니다. 보다 간단하게,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

제어 경험 *ν<sub>0</sub>*&#x200B;의 전환율이 0이면 상승도가 없습니다.

## [!DNL Confidence Interval of Lift]

[!UICONTROL Average Lift and Confidence Interval] 열의 상자그림 그래프는 평균 값과 95% [!UICONTROL Confidence Interval of Lift]을(를) 나타냅니다. 주어진 비제어 경험의 신뢰 구간이 제어 경험의 신뢰 구간과 겹치는 경우 상자그림은 회색으로 표시됩니다. 주어진 경험의 신뢰 구간 범위가 통제 경험의 신뢰 구간 이상이거나 미만인 경우 상자그림은 녹색 또는 빨간색입니다.

경험 *ν*&#x200B;과(와) 제어 경험 *ν<sub>0</sub>* 사이의 상승도에 대한 표준 오류는 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="지표 평균"></p>

상승도의 95% 신뢰 구간은 다음과 같습니다.

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

이 계산에서는 &quot;Delta&quot; 메서드를 사용하며 [이 문서에 자세히 설명되어 있습니다](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL Confidence]

마지막 열은 [!DNL Target] 보고서의 신뢰도를 표시합니다. 경험의 신뢰도는 귀무 가설이 참인 경우 관찰되는 결과만큼 극단적인 결과를 얻을 확률(백분율로 표시)입니다. p 값의 경우 표시되는 신뢰도는 *1 - p 값*&#x200B;입니다. 직관적으로, 신뢰도가 높다는 것은 제어 경험과 비제어 경험이 동일한 전환율을 가질 가능성이 적다는 것을 의미한다.

[!DNL Target]에서 테스트 경험과 제어 경험 사이에 양측 **Welch의 t-test**&#x200B;가 수행되어 테스트 및 제어 경험이 동일한지 테스트합니다. 일반적으로 실험을 실행하기 전에 두 그룹의 샘플 크기와 분산이 같은지 알 수 없으며, [!DNL Target]을(를) 사용하면 각 경험에 보낸 트래픽의 백분율이 동일하지 않을 수 있으므로 각 경험의 분산이 같다고 가정하지 않습니다. 따라서, Welch의 t-test는 Student&#39;s t-test 대신 선택됩니다.

Welch의 t-검정을 수행하기 위해 먼저 t-통계량과 자유도들을 계산하기 시작한 다음, 양측 t-검정을 실행하여 p-값을 생성한다. 마지막으로, 우리는 p-값에 기초하여 신뢰도를 계산한다.

*t* 통계는 두 개의 독립 임의 변수(*ν* 및 *ν<sub>0</sub>*)의 평균 차이를 차이의 표준 오류로 나눈 값으로 정의됩니다.

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

여기서 *μ<sub>v</sub>* 및 *μ<sub>v0</sub>*&#x200B;은(는) 각각 *ν* 및 *ν<sub>0</sub>*&#x200B;을 의미하며 *μ<sub>v</sub>*&#x200B;과(와) *μ<sub>v0</sub>* 간의 차이의 표준 오차는 다음과 같습니다.

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

여기서 *σ<sup>2</sup><sub>v</sub>* 및 *σ<sup>2</sup><sub>v<sub>0</sub></sub>*&#x200B;은(는) 두 경험의 분산 *ν* 및 *ν<sub>0</sub>*&#x200B;이고, *N<sub>v</sub>* 및 *N<sub>v<sub>0</sub></sub>*&#x200B;은(는) 각각 *ν* 및 *ν<sub>0</sub>*&#x200B;의 샘플 크기입니다.

Welch&#39;s t-test의 경우, 자유도는 다음과 같이 계산된다.

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

*ν* 및 *ν<sub>0</sub>*&#x200B;에 대한 자유도는 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

그런 다음 *t* 분포의 끝에 있는 영역에서 p 값을 계산할 수 있습니다.

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

마지막으로 [!DNL Target]에서 보고된 신뢰도는 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## 오프라인 계산 수행

[다운로드한 CSV 보고서](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md)는 원시 데이터만 포함하며 A/B 테스트에 사용되는 방문자당 수입, 상승도 또는 신뢰도와 같이 계산된 지표는 포함하지 않습니다.

이러한 통계 수량을 계산하려면 [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel 파일을 다운로드하여 활동의 값을 입력하십시오.
