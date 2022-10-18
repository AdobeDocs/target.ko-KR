---
keywords: 보고서;통계적 방법론;통계적 계산;통계;평균;전환율;방문자당 수입;rpv;신뢰도 구간;리프트;웰치 t 테스트;오프라인 계산
description: 수작업에 사용되는 통계 계산에 대해 알아봅니다 [!UICONTROL A/B 테스트] 활동 [!DNL Adobe Target].
title: 에 사용된 통계 계산에 대해 어떻게 알 수 있습니까? [!UICONTROL A/B 테스트] 활동?
feature: Reports
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 5%

---

# A/Bn 테스트의 통계 계산

이 문서에서는 의 수동 A/Bn 테스트에 사용되는 자세한 통계적 계산 [!DNL Adobe Target]. 에 대한 정의가 제공됩니다 [!UICONTROL 전환율], [!UICONTROL 전환율의 신뢰도 구간], [!UICONTROL 상승도], [!UICONTROL 상승도 신뢰 구간 을 참조하십시오], 및 [!UICONTROL 신뢰도].

>[!NOTE]
>
>이 문서의 정보는 이전에 이 사이트에서 다운로드할 수 있었던 *A/B 테스트를 위한 Adobe Target 계산* pdf 파일을 대체합니다.

![을 보여주는 Target 보고서 [!UICONTROL 전환율], [!UICONTROL 평균 상승도 및 신뢰도 구간], 및 [!UICONTROL 신뢰도] A/B 테스트 활동 중 하나를 선택합니다.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## 평균 성능

다음 섹션에서는 이전 그림에서 사용된 계산에 대해 설명합니다.

### RPV(방문자당 전환율 및 매출) 캠페인

다음 그림은 [!UICONTROL 전환율], [!UICONTROL 전환율의 신뢰도 구간], 및의 수 [!UICONTROL 전환] 에서 [!DNL Target] 보고서 세트에 대해 설명합니다. 예를 들어 첫 번째 줄은 경험 A에 대해 다음을 보여줍니다. a [!UICONTROL 전환율] is 25.81% with a [!UICONTROL 신뢰도 구간] 건당 7.7%, 32건의 건전화기록이 기록된 건 연쇄폭발이었다. 124명의 방문자가 경험을 본 경우 이것은 32/124 = 25.81%와 같습니다.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

전환율 또는 **평균**, *um<sub>ν</sub>*, 각 경험에 대해 *ν* 실험에서는 해당 지표에 지정된 단위 수에 대한 지표 합계의 비율로 정의됩니다. *N<sub>ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

여기에서,

* *Y<sub>iν</sub>* 은 각 단위에 대한 지표 값입니다 *i*: 해당 경험에 할당됩니다 *ν*.

* 단위 합계 *i* 계산 방법론 선택에 따라 다릅니다.

   * If *[!UICONTROL 방문자 수]* 를 계산 방법론으로 사용하는 각 단위는 활동 수명 동안 활동에서 고유한 참여자로 정의된 고유 방문자입니다.
   * If *[!UICONTROL 방문 횟수]* 를 계산 방법론으로 사용하면, 각 단위는 다음 기간 동안 경험에 대한 고유 방문으로 정의된 고유한 방문입니다 [!DNL Target] 세션(고유 `sessionId`). 이 `sessionId` 변경 사항이나 방문자가 전환 단계에 도달하면 새 방문이 계산됩니다.
   * If *[!UICONTROL 활동 노출 횟수]* 를 계산 방법론으로 사용하는 각 단위는 방문자가 활동의 모든 페이지를 로드할 때마다 정의된 고유한 노출입니다.

## [!UICONTROL 평균 신뢰 구간]/[!UICONTROL 전환율]

전환율의 신뢰 구간은 기본 데이터와 일치하는 가능한 전환율의 범위로 직관적으로 정의됩니다.

실험을 실행할 때 주어진 경험에 대한 전환율은 *예상* 의 &quot;true&quot; 전환율. 이 추정의 불확실성을 수치화하려면 [!DNL Target] 는 신뢰 구간을 사용합니다. [!DNL Target] 항상 95% 신뢰 구간을 보고합니다. 즉, 마지막에 계산된 신뢰 구간의 95%에는 경험의 실제 전환율이 포함됩니다.

전환율의 95% 신뢰 구간 *um<sub>ν</sub>* 는 값 범위로 정의됩니다.

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

여기서 평균에 대한 표준 오류가

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

샘플 표준 편차의 편차 견적이 사용되는 경우:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

캠페인이 전환율 캠페인(즉, 전환 지표가 바이너리임)이면 표준 오류가 감소하여 다음과 같이 됩니다.

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## 상승도

다음 그림은 [!UICONTROL 상승도] 및 [!UICONTROL 상승도 신뢰 구간] 에서 [!DNL Target] 보고서. 숫자는 상승도 한계 범위의 평균을 나타내며 화살표는 상승도가 양수이거나 음수이면 반영됩니다. 신뢰도가 95%를 넘을 때까지 화살표가 회색으로 표시됩니다. 신뢰도가 임계값을 지나면 화살표는 양수 또는 음수 상승도를 기반으로 녹색 또는 빨간색으로 표시됩니다.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

경험 간의 상승도  *ν*, 및 제어 경험 *ν<sub>0</sub>* 는 로 정의된 전환율의 상대 &quot;델타&quot;입니다

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

여기서 개별 전환율이 위에서 정의한 바와 같습니다. 더 간단하게,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

제어 경험의 전환율인 경우 *ν<sub>0</sub>* 0이면 상승도가 없습니다.

## [!DNL Confidence Interval of Lift]

의 상자그림 그래프 [!UICONTROL 평균 상승도 및 신뢰도 구간] 열은 평균 값을 나타내고 95%를 나타냅니다 [!UICONTROL 상승도 신뢰 구간]. 제어 경험의 신뢰 구간과 지정된 비제어 경험의 신뢰 구간에 겹치는 부분이 있으면 상자플로우는 회색으로 표시됩니다. 주어진 경험의 신뢰 구간 범위가 통제 경험의 신뢰 구간 이상이거나 미만인 경우 상자플롯은 녹색 또는 빨간색으로 표시됩니다.

경험 간의 상승도 표준 오류입니다  *ν*, 및 제어 경험  *ν<sub>0</sub>* 가 다음으로 정의됩니다.

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="지표 평균"></p>

그런 다음 상승도의 95% 신뢰 구간 은 다음과 같습니다.

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

이 계산은 &quot;Delta&quot; 메서드를 사용하며, 다음과 같이 설명합니다 [이 문서의 자세한 내용](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL 신뢰도]

마지막 열에는 [!DNL Target] 보고서 세트에 대해 설명합니다. null 가설이 true인 경우, 경험의 신뢰도는 관찰된 것보다 덜 극단적인 결과를 얻을 확률(백분율로 표시됨)입니다. p 값 측면에서 표시되는 신뢰도는 *1 - p 값*. 직관적으로, 더 높은 신뢰도는 통제 경험과 비제어 경험이 동일한 전환율을 가질 가능성이 적다는 것을 의미합니다.

in [!DNL Target]양쪽의 꼬리표 **웰치의 t 테스트** 테스트 경험과 제어 경험 사이에 수행되어 테스트 및 제어 경험의 방법이 동일한지 테스트합니다. 우리는 일반적으로 실험을 실행하기 전에 두 그룹의 샘플 크기와 차이가 동일한지 모르므로 [!DNL Target] 또한 각 경험에 전송되는 트래픽의 비율을 불균등하게 가질 수도 있으므로 각 경험에 대한 분산이 같다고 가정하지 않습니다. 따라서, 웰치의 t-테스트는 학생의 t-테스트 대신 선택된다.

웰치의 t-테스트를 수행하기 위해, 먼저 t-통계와 자유도 계산을 시작한 다음, 두 개의 검증 t 테스트를 실행하여 p-값을 생성합니다. 마지막으로 p 값을 기준으로 신뢰도를 계산합니다.

다음 *t*&quot;통계치는 두 개의 독립 임의 변수의 수단의 차이로 정의됩니다. *ν* 및 *ν<sub>0</sub>*&#x200B;을 차이의 표준 오차로 나눈 값입니다.

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

위치 *um<sub>v</sub>* 및 *um<sub>v0</sub>* 의 목적은 *ν*  및 *ν<sub>0</sub>* 각각 및 의 차이값의 표준 오차 *um<sub>v</sub>* 및 *um<sub>v0</sub>* 제공 대상:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

위치 *시그마<sup>2개</sup><sub>v</sub>* 및 *시그마<sup>2개</sup><sub>v<sub>0</sub></sub>* 두 경험의 차이가 있습니다 *ν*  및 *ν<sub>0</sub>* 각각 및 *N<sub>v</sub>* 및 *N<sub>v<sub>0</sub></sub>* 에 대한 샘플 크기 *ν* 및 *ν<sub>0</sub>* 각각 사용할 수 있습니다.

Welch의 t-test에서 자유의 정도는 다음과 같이 계산됩니다.

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

그리고 자유도 *ν*  및 *ν<sub>0</sub>* 다음으로 정의됩니다.

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

그런 다음 p-value는 *t*-distribution:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

마침내, 그 자신감은 [!DNL Target] 가 다음으로 정의됩니다.

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## 계산을 오프라인으로 수행

[다운로드한 CSV 보고서](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md)는 원시 데이터만 포함하며 A/B 테스트에 사용되는 방문자당 수입, 상승도 또는 신뢰도와 같이 계산된 지표는 포함하지 않습니다.

이러한 통계 수량을 계산하려면 [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) 활동의 값을 입력할 Excel 파일입니다.