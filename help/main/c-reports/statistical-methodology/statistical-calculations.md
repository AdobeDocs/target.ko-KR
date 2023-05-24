---
keywords: 보고서;통계 방법론;통계 계산;통계;평균;전환율;방문자당 매출;rpv;신뢰 구간;상승도;상승도 t-테스트;오프라인 계산
description: 설명서에 사용된 통계 계산에 대해 알아봅니다 [!UICONTROL A/B 테스트] 의 활동 [!DNL Adobe Target].
title: 에서 사용되는 통계 계산에 대해 알아보려면 어떻게 해야 합니까? [!UICONTROL A/B 테스트] 활동?
feature: Reports
exl-id: 5f7377b9-0567-4b6f-8968-4696b2088d0a
source-git-commit: f997b6a0ea9e0cebf7b414c029971d8520f8b95f
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 5%

---

# A/Bn 테스트의 통계 계산

이 문서는에서 수동 A/Bn 테스트에 사용된 자세한 통계 계산을 문서화합니다. [!DNL Adobe Target]. 정의는 다음과 같습니다. [!UICONTROL 전환율], [!UICONTROL 전환율의 신뢰 구간], [!UICONTROL 상승도], [!UICONTROL 상승도에 대한 신뢰 구간], 및 [!UICONTROL 신뢰도].

>[!NOTE]
>
>이 문서의 정보는 이전에 이 사이트에서 다운로드할 수 있었던 *A/B 테스트를 위한 Adobe Target 계산* pdf 파일을 대체합니다.

![다음을 보여주는 Target 보고서 [!UICONTROL 전환율], [!UICONTROL 평균 상승도 및 신뢰 구간], 및 [!UICONTROL 신뢰도] A/B 테스트 활동.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## 평균 성과

다음 섹션에서는 이전 그림에서 사용한 계산에 대해 설명합니다.

### RPV(방문자당 전환율 및 수익) 캠페인

다음 그림은 를 보여 줍니다 [!UICONTROL 전환율], [!UICONTROL 전환율의 신뢰 구간], 및 수 [!UICONTROL 전환] 다음 기간: [!DNL Target] 보고서. 예를 들어 첫 번째 줄은 경험 A의 경우 [!UICONTROL 전환율] 이(가) 25.81%임 [!UICONTROL 신뢰 구간] ±7.7%와 32건의 전환율을 기록하였다. 124명의 방문자가 이 경험을 봤다고 가정하면 32/124 = 25.81%에 해당합니다.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

전환율 또는 **평균**, *μ<sub>ν</sub>*, 각 경험에 대해 *ν* 실험에서는 해당 지표에 할당된 단위 수에 대한 지표 합계의 비율로 정의됩니다. *N<sub>ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

여기에서,

* *Y<sub>iν</sub>* 각 단위에 대한 지표 값입니다 *i*: 지정된 경험에 할당됨 *ν*.

* 단위에 대한 합계 *i* 계산 방법론의 선택에 따라 다릅니다.

   * If *[!UICONTROL 방문자 수]* 계산 방법론으로 사용되는 각 단위는 활동의 수명 동안 활동에 고유한 참가자로 정의된 고유한 방문자입니다.
   * If *[!UICONTROL 방문 횟수]* 계산 방법론으로 사용됩니다. 각 단위는 다음 기간 동안 경험에 고유한 참가자로 정의된 고유한 방문입니다. [!DNL Target] 세션(고유 포함) `sessionId`). 다음의 경우 `sessionId` 를 변경하거나 방문자가 전환 단계에 도달하면 새 방문이 계산됩니다.
   * If *[!UICONTROL 활동 노출 횟수]* 계산 방법론으로 사용됩니다. 각 단위는 방문자가 활동의 페이지를 로드할 때마다 정의된 고유한 노출입니다.

## [!UICONTROL 평균 신뢰 구간]/[!UICONTROL 전환율]

전환율의 신뢰 구간은 기본 데이터와 일치하는 가능한 전환율 범위로 직관적으로 정의된다.

실험을 실행할 때 주어진 경험에 대한 전환율은 입니다 *예상* 를 반환합니다. 이 추정치의 불확실성을 수량화하기 위해 [!DNL Target] 신뢰 구간을 사용합니다. [!DNL Target] 항상 95% 신뢰 구간을 보고합니다. 즉, 계산된 신뢰 구간의 95%에는 경험의 실제 전환율이 포함됩니다.

전환율의 95% 신뢰 구간 *μ<sub>ν</sub>* 은 값의 범위로 정의됩니다.

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

여기서 평균의 표준 오차는

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

샘플 표준 편차의 비편향 추정치를 사용하는 경우:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

캠페인이 전환율 캠페인(즉, 전환 지표가 이진수)인 경우 표준 오류는 다음과 같이 줄어듭니다.

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## 상승도

다음 그림은 를 보여 줍니다 [!UICONTROL 상승도] 및 [!UICONTROL 상승도의 신뢰 구간] 다음 기간: [!DNL Target] 보고. 숫자는 상승도 한계 범위의 평균을 나타내고 화살표는 상승도가 양수이거나 음수이면 반영합니다. 신뢰도가 95%를 넘을 때까지 화살표가 회색으로 표시됩니다. 신뢰도가 임계값을 넘으면 양수 또는 음수 상승도를 기준으로 화살표가 녹색 또는 빨간색입니다.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

경험 사이의 상승도  *ν*, 및 제어 경험 *ν<sub>0</sub>* 는 다음과 같이 정의된 전환율의 상대적 &quot;델타&quot;입니다.

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

여기서 개별 전환율은 위에서 정의된 대로 입니다. 보다 간단하게,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

제어 경험의 전환율인 경우 *ν<sub>0</sub>* 0이면 리프트가 없습니다.

## [!DNL Confidence Interval of Lift]

의 상자 그림 그래프 [!UICONTROL 평균 상승도 및 신뢰 구간] 열은 평균값과 95%를 나타냅니다. [!UICONTROL 상승도의 신뢰 구간]. 주어진 비제어 경험의 신뢰 구간이 제어 경험의 신뢰 구간과 겹치는 경우 상자그림은 회색으로 표시됩니다. 주어진 경험의 신뢰 구간 범위가 통제 경험의 신뢰 구간 이상이거나 미만인 경우 상자그림은 녹색 또는 빨간색입니다.

경험 간 상승도의 표준 오차  *ν*, 및 제어 경험  *ν<sub>0</sub>* 은 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="지표 평균"></p>

상승도의 95% 신뢰 구간은 다음과 같습니다.

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

이 계산에서는 &quot;Delta&quot; 메서드를 사용하며 [이 문서에서 더 자세히](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL 신뢰도]

마지막 열은 의 신뢰도를 나타냅니다. [!DNL Target] 보고서. 경험의 신뢰도는 귀무 가설이 참인 경우 관찰된 결과보다 덜 극단적인 결과를 얻을 확률(백분율로 표시)입니다. p 값의 경우 표시되는 신뢰도는 다음과 같습니다. *1 - p 값*. 직관적으로, 신뢰도가 높다는 것은 제어 경험과 비제어 경험이 동일한 전환율을 가질 가능성이 적다는 것을 의미한다.

위치 [!DNL Target], 두 개의 꼬리 **웰치 티테스트** 테스트 경험과 제어 경험 사이에 수행되어 테스트 수단과 제어 경험이 동일한지 테스트합니다. 우리는 보통 실험을 실행하기 전에 두 그룹의 샘플 크기와 분산이 동일한지 모르기 때문에, [!DNL Target] 또한 각 경험에 전송된 트래픽의 비율이 동일하지 않을 수 있으므로 각 경험에 대한 분산이 동일하다고 가정하지 않습니다. 따라서, Welch의 t-test는 Student&#39;s t-test 대신 선택됩니다.

Welch의 t-검정을 수행하기 위해 먼저 t-통계량과 자유도들을 계산하기 시작한 다음, 양측 t-검정을 실행하여 p-값을 생성한다. 마지막으로, 우리는 p-값에 기초하여 신뢰도를 계산한다.

다음 *t*-statistic은 임의의 두 개의 독립적인 확률변수들의 평균의 차이로 정의된다. *ν* 및 *ν<sub>0</sub>*&#x200B;를 차이의 표준 오류로 나눕니다.

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

위치 *μ<sub>v</sub>* 및 *μ<sub>v0</sub>* 의 수단임 *ν*  및 *ν<sub>0</sub>* 각각 및 간의 차이에 대한 표준 오차 *μ<sub>v</sub>* 및 *μ<sub>v0</sub>* 은(는) 다음 사람에게 제공됩니다.

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

위치 *σ<sup>2</sup><sub>v</sub>* 및 *σ<sup>2</sup><sub>v<sub>0</sub></sub>* 두 경험의 차이점 *ν*  및 *ν<sub>0</sub>* 및 *N<sub>v</sub>* 및 *N<sub>v<sub>0</sub></sub>* 다음에 대한 샘플 크기: *ν* 및 *ν<sub>0</sub>* 각각.

Welch&#39;s t-test의 경우, 자유도는 다음과 같이 계산된다.

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

및 의 자유도 *ν*  및 *ν<sub>0</sub>* 은 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

그런 다음 p 값은 의 뒷부분에 있는 영역에서 계산할 수 있습니다. *t*-distribution:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

마지막으로 신뢰도가 보고되었습니다. [!DNL Target] 은 다음과 같이 정의됩니다.

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## 오프라인 계산 수행

[다운로드한 CSV 보고서](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md)는 원시 데이터만 포함하며 A/B 테스트에 사용되는 방문자당 수입, 상승도 또는 신뢰도와 같이 계산된 지표는 포함하지 않습니다.

이러한 통계 수량을 계산하려면 다음을 다운로드하십시오. [!DNL Target] [완료 신뢰도 계산기](/help/main/assets/complete_confidence_calculator.xlsx) 활동의 값을 입력할 Excel 파일입니다.
