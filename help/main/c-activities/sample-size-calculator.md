---
keywords: 샘플 크기 계산기;A/B;자동 할당;통계적 중요도;트래픽 볼륨
description: Adobe Target 샘플 크기 계산기 를 사용하여 실험 기간, 트래픽 볼륨 또는 최소 감지 가능한 효과를 추정하십시오.
title: 샘플 크기 계산기
feature: Activities
badge: label="Beta" type="Informative"
source-git-commit: d3fb1b69975951d41803be0eb902333332cb1ed1
workflow-type: tm+mt
source-wordcount: '1604'
ht-degree: 11%
---
# 샘플 크기 계산기

>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="일별 트래픽"
>abstract="매일 실험에 참여하는 사용자 수입니다. 이 값을 모를 경우 위의 트래픽 볼륨을 선택하면 계산기가 다른 입력을 사용하여 이를 해결합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="신뢰 수준"
>abstract="결과가 중요하다고 하기 전에 무작위로 우연한 기회에 의한 것이 아니라는 것을 얼마나 확신할 수 있는가? 95% 신뢰 수준은 긍정 오류(false positive)가 발생할 가능성이 최대 5%임을 의미합니다. 값이 높을수록 긍정 오류(false positive)는 감소하지만 더 많은 데이터가 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="통계적 검증력"
>abstract="실제 효과가 존재하는 경우 이를 감지할 확률. 80% 전력 레벨은 실제 효과를 감지할 확률이 80%임을 의미합니다. 높은 전력은 거짓 음성을 감소시키지만, 더 많은 트래픽 또는 더 긴 런타임이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup_cja"
>title="테스트 설정"
>abstract="이 필드에서는 실험, 예상 결과 및 결과에 대한 신뢰 임계값을 정의합니다. 위에서 선택한 값에 연결된 필드는 자동으로 해결됩니다. 나머지 필드는 예상 값으로 완료하십시오."


>[!AVAILABILITY]
>
>이 샘플 크기 계산기 (Beta)를 사용하면, 귀하는 Beta이 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공된다는 것을 인정합니다. Adobe은 Beta을 유지, 수정, 업데이트, 변경, 수정 또는 지원할 의무가 없습니다. 이러한 Beta 및/또는 동봉된 자료의 올바른 기능이나 성능에 어떤 식으로든 의존하지 말고 주의하는 것이 좋습니다. Beta은 Adobe의 기밀 정보로 간주됩니다.  귀하가 Adobe에 제공한 &quot;피드백&quot;(Beta 사용 중 발생하는 문제 또는 결함, 제안, 개선 사항 및 권장 사항을 포함하되 이에 제한되지 않는 Beta 관련 정보)은 해당 피드백에 대한 모든 권한, 제목 및 관심을 포함하여 Adobe에 할당됩니다.

**[!UICONTROL 샘플 크기 계산기]**&#x200B;를 사용하면 실험을 시작하기 전에 실험 계획에 필요한 입력을 예측할 수 있습니다. 계산기는 필요한 트래픽의 양, 테스트를 실행해야 하는 시간, 포함할 경험의 수 또는 제공한 값을 기반으로 안정적으로 감지할 수 있는 최소 효과를 결정하는 데 도움이 됩니다.

**[!UICONTROL 샘플 크기 계산기]**&#x200B;에 액세스하려면 **[!UICONTROL 활동]** 메뉴로 이동하십시오.

![](assets/calculator_menu.png)

## A/B(타겟 보고)

>[!CONTEXTUALHELP]
>id="target_sample_size_bonferroni"
>title="본페로니 교정"
>abstract="두 개 이상의 오퍼를 제어와 동시에 비교하기 위해 신뢰 수준을 조정합니다. 오퍼 수가 2개 이상인 경우에만 문제가 됩니다. 이는 Adobe의 공개 Target Calculator 도구에 사용된 것과 동일한 수정 사항과 일치합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="지표 유형"
>abstract="측정 중인 지표 유형입니다. 각 사용자가 작업을 완료하거나 완료하지 않는 클릭 또는 전환과 같은 이진 결과에 백분율을 사용합니다. 사용자마다 값이 크게 다를 수 있는 매출액 또는 페이지 보기 수와 같은 지표에 숫자를 사용하십시오."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_offers"
>title="오퍼 수"
>abstract="제어를 포함한 실험의 경험 수입니다. 두 개 이상의 오퍼가 모든 비교에서 전체 신뢰 수준을 정확하게 유지하기 위해 Bonferroni 수정 (활성화된 경우)을 자동으로 적용합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_lift"
>title="상승도"
>abstract="감지하려는 기준선에 대한 상대적 개선 사항입니다. 베이스라인의 백분율로 입력합니다. 예를 들어 11.8% 기준 요소 전환율에 대한 5% 상승도는 12.39%를 목표로 합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_conversion_rate"
>title="베이스라인 전환율"
>abstract="실험이 시작되기 전의 현재 전환율, 즉 컨트롤 암 평균입니다. 이 값은 항상 필요합니다. 백분율 지표에 5%와 같은 백분율을 입력합니다. 수 지표의 경우 원시 십진 값을 입력하십시오."

A/B 테스트를 계획하고 실행하는 데 필요한 입력 예측 이러한 값은 필요한 트래픽의 양, 테스트를 실행해야 하는 시간, 그리고 실제로 감지할 수 있는 효과 크기를 결정하는 데 도움이 됩니다.

1. **[!UICONTROL A/B(Target 보고)]** 탭에 액세스하여 A/B 테스트에 대한 계획 입력을 계산합니다.

1. **[!UICONTROL 수정 적용]** 옵션을 활성화하여 두 개 이상의 오퍼를 컨트롤과 동시에 비교하기 위한 신뢰 수준을 조정합니다.

1. **[!UICONTROL 지표 유형]** 선택:

   * 전환율: 클릭 또는 구매와 같은 바이너리 결과에 대해 사용하며, 여기서 각 방문자는 작업을 완료하거나 완료하지 않습니다.
   * 방문자당 매출: 방문자마다 값이 크게 다를 수 있는 매출 스타일 지표에 사용합니다.

     ![](assets/calculator-target_reporting_1.png)

1. 매일 실험에 들어가는 사용자의 수인 **[!UICONTROL 일별 트래픽]**&#x200B;을(를) 지정하십시오.

1. **[!UICONTROL 테스트 설정]**&#x200B;에서 나머지 값을 입력하십시오.

   * **[!UICONTROL 오퍼 수]**: 컨트롤을 포함한 실험의 경험 수입니다. 두 개 이상의 오퍼가 활성화되면 전체 신뢰 수준을 유지하기 위해 Bonferroni 수정 이 적용됩니다.

   * **[!UICONTROL 상승도]**: 검색하려는 기준선에 대한 상대적 개선 사항입니다. 베이스라인의 백분율로 입력합니다(예: 11.8% 베이스라인 전환율 목표의 5% 상승도 12.39%).

     ![](assets/calculator-target_reporting_2.png)

1. 실험이 시작되기 전에 현재 경험에 대한 **[!UICONTROL 기준선 전환율]**&#x200B;을 지정하십시오.

1. **[!UICONTROL 고급 통계 설정]**&#x200B;을 확장하여 선택한 계산에 사용할 수 있는 경우 추가 통계 입력을 제공할 수 있습니다.

   * **[!UICONTROL 신뢰 수준]**: 결과가 우연에 의한 것이 아닐 가능성. 95% 수준은 긍정 오류(false positive)의 가능성을 5% 허용합니다.

   * **[!UICONTROL 통계적 검증력]**: 실제 효과를 감지할 가능성. 80%의 전력은 거짓 음성을 감소시키지만 더 많은 트래픽이나 시간을 필요로 합니다.

1. **[!UICONTROL 계산 실행]**&#x200B;을 선택하여 예상 값을 생성합니다. 현재 입력을 지우고 다시 시작하려면 **[!UICONTROL 재설정]**&#x200B;을 선택하세요.

필수 필드를 완료하고 계산을 실행한 후 **[!UICONTROL 결과]** 패널에 예상 값이 표시됩니다. 필수 필드가 불완전한 경우, 패널에 누락된 값을 입력하라는 메시지가 표시됩니다.

![](assets/calculator-cja-analytics-3.png)

계산기는 실험을 계획하기 위한 추정치를 제공한다. 활동 실행 시간을 결정할 때 실험 설계, 예상 트래픽, 기준 성능 및 통계 요구 사항과 함께 결과를 사용합니다.

## A/B (CJA/Adobe Analytics)

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="경험 수"
>abstract="통제를 포함하여, 실험의 변형 수입니다. A/B 테스트에는 2개의 군이 있습니다. 변형 5개에 통제군 1개를 더하면 6개가 됩니다. 실험군이 늘어날수록 통계적 검정력을 유지하기 위해 비례적으로 더 많은 트래픽이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="A/B 테스트 기간"
>abstract="실험이 실행될 기간(일)입니다. 기간이 길수록 실험에서 데이터를 수집하는 시간이 더 많아지므로 더 작은 효과를 안정적으로 감지할 수 있습니다. 기간이 짧을수록 신뢰할 수 있는 결과에 도달하기 위해 더 큰 효과나 더 많은 일별 트래픽이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="예상되는 개선도"
>abstract="감지가 필요한 가장 작은 개선 단위로, 조치하고자 하는 지표의 최소 변화 단위입니다. 백분율 포인트 단위의 상승폭을 나타내며 기준선 대비 백분율 변화를 의미하지 않습니다. 예를 들어 기준선이 5%이고 1% 포인트 상승폭이 중요한 경우 1을 입력합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="분산"
>abstract="평균값이 아닌 지표 값을 분산하는 방법입니다. 클릭률(대부분 0초 및 1초)과 같은 지표는 일반적으로 변량이 적은 반면, 사용자당 매출과 같은 지표는 변량이 훨씬 높을 수 있습니다. 확실하지 않은 경우 기본값을 1로 둡니다."

Adobe Analytics 또는 Customer Journey Analytics 데이터에 의존하는 A/B 활동에 대한 계획 입력을 예측합니다. 활동을 시작하기 전에 실험 크기, 예상 상승도 및 테스트 기간을 정의하는 데 도움이 됩니다.

1. **[!UICONTROL A/B(CJA/Adobe Analytics)]** 탭에 액세스하여 A/B 테스트에 대한 계획 입력을 계산합니다.

1. **[!UICONTROL 알고 싶은 내용]**&#x200B;에서 계산기에서 확인할 값을 선택하십시오.

   * **[!UICONTROL 기간]**: 테스트를 염두에 두고 있으며 실행하는 데 걸리는 시간과 실행할 가치가 있는지 알고 싶습니다.
   * **[!UICONTROL 경험 수]**: 실험을 실행할 위치가 있으며 트래픽이 지원할 수 있는 처리 수를 파악하고자 합니다.
   * **[!UICONTROL 트래픽 볼륨]**: 염두에 둔 실험이 있으며 통계적 중요도에 도달하기 위해 필요한 방문자 수를 알고 싶어합니다.
   * **[!UICONTROL 최소 감지 가능한 효과]**: 실행하려고 하지만 통계적 중요도에 도달하기 위해 필요한 상승도의 양을 알고 싶은 실험이 있습니다. 이는 실험이 실행할 가치가 있는지 또는 계획할 가치가 있는지 평가하는 데 도움이 됩니다.

   선택한 값에 따라 양식의 필드가 변경됩니다. 계산기는 다른 입력을 사용하여 선택된 결과를 결정합니다.

   ![](assets/calculator-cja-analytics-1.png)

1. 매일 실험에 들어가는 사용자의 수인 **[!UICONTROL 일별 트래픽]**&#x200B;을(를) 지정하십시오.

1. **[!UICONTROL 테스트 설정]**&#x200B;에서 나머지 값을 입력하십시오.

   * **[!UICONTROL 경험 수]**: 컨트롤을 포함한 변형 수입니다. 더 많은 변형에는 더 많은 트래픽이 필요합니다.

   * **[!UICONTROL A/B 테스트 기간]**: 실험이 실행되는 일수입니다. 더 긴 검사는 더 작은 효과를 검출할 수 있습니다.

   * **[!UICONTROL 예상되는 개선 사항]**: 실험이 만들어낼 것으로 기대하는 개선 사항입니다.

   * **[!UICONTROL 분산]**: 지표 값의 분산 정도. 클릭스루 비율은 일반적으로 변량이 적으므로 사용자당 매출이 훨씬 높을 수 있습니다. 확실하지 않은 경우 기본값을 1로 둡니다.

     [Analytics 설명서](https://experienceleague.adobe.com/en/docs/analytics/components/calculated-metrics/calcmetrics-reference/cm-functions#variance)에서 **[!UICONTROL 분산]**&#x200B;을 계산하는 방법을 알아봅니다.

     ![](assets/calculator-cja-analytics-2.png)

1. **[!UICONTROL 고급 통계 설정]**&#x200B;을 확장하여 선택한 계산에 사용할 수 있는 경우 추가 통계 입력을 제공할 수 있습니다.

   * **[!UICONTROL 신뢰 수준]**: 결과가 우연에 의한 것이 아닐 가능성. 95% 수준은 긍정 오류(false positive)의 가능성을 5% 허용합니다. 신뢰 수준이 낮으면 더 적은 트래픽이 필요함을 의미하지만, 이는 긍정 오류(false positive)의 위험도 증가시킵니다.

   * **[!UICONTROL 통계적 검증력]**: 실제 효과를 감지할 가능성. 80%의 전력은 거짓 음성을 감소시키지만 더 많은 트래픽이나 시간을 필요로 합니다.

1. **[!UICONTROL 계산 실행]**&#x200B;을 선택하여 예상 값을 생성합니다. 현재 입력을 지우고 다시 시작하려면 **[!UICONTROL 재설정]**&#x200B;을 선택하세요.

필수 필드를 완료하고 계산을 실행한 후 **[!UICONTROL 결과]** 패널에 예상 값이 표시됩니다. 필수 필드가 불완전한 경우, 패널에 누락된 값을 입력하라는 메시지가 표시됩니다.

![](assets/calculator-cja-analytics-4.png)

계산기는 실험을 계획하기 위한 추정치를 제공한다. 활동 실행 시간을 결정할 때 실험 설계, 예상 트래픽, 기준 성능 및 통계 요구 사항과 함께 결과를 사용합니다.
