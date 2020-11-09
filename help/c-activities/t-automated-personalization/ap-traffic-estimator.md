---
keywords: traffic estimator;automated personalization;ap
description: 트래픽 견적 도구는 Adobe Target 활동이 성공할 수 있는 충분한 트래픽이 있는지 여부를 알 수 있는 피드백을 제공합니다.
title: 성공에 필요한 트래픽 예측
feature: ap
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 24%

---


# ![PREMIUM](/help/assets/premium.png) 성공에 필요한 트래픽 예측{#estimate-the-traffic-required-for-success}

The [!UICONTROL Traffic Estimator] provides feedback that lets you know whether you have sufficient traffic for your [!DNL Adobe Target] activity to succeed.

Because an [!UICONTROL Automated Personalization] activity uses multiple offer combinations, it is important to know how much traffic is required to provide meaningful results. The [!UICONTROL Traffic Estimator] uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the activity successful.

The [!UICONTROL Traffic Estimator] determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. 이상적으로는 활동이 성공하려면 올바른 샘플 크기를 사용되어 개인화된 콘텐츠가 활동 지속 기간의 50% 또는 14일 중에서 더 짧은 기간 안에 준비될 수 있어야 합니다. 이렇게 하면 개인화된 콘텐츠를 획득하고 전달할 콘텐츠를 학습하기 위한 충분한 시간이 보장됩니다.

Remember that [!DNL Target] randomly serves experiences until the personalization algorithms are built. The checkmark icon beside each offer shows when the model for that offer is ready and [!DNL Target] is able to begin delivering personalized content. 상승도는 모델이 준비된 후에만 예측되므로 시각적 표시를 통해 적절한 기대 수준을 설정할 수 있습니다. Use the [!UICONTROL Traffic Estimator] in the [!UICONTROL Visual Experience Composer] (VEC) to get a guideline of when the models will be ready.

## 트래픽 견적 도구 사용

1. From the [!UICONTROL Visual Experience Composer], click **[!UICONTROL Traffic]**.

   ![트래픽 아이콘](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   The [!UICONTROL Traffic Estimator] opens. **[!UICONTROL 트래픽]**[!UICONTROL 을 다시 클릭하여 트래픽 견적 도구를 숨길 수 있습니다].

   ![](assets/ap_est.png)

1. 일반적인 전환율(또는 이 활동에서 예상하는 전환율), 일별 예상 활동 노출 수 및 테스트 지속 기간을 제공합니다.

   * **오퍼 수**:제외 후 활동의 일부로 만들어지는 경험의 수를 기반으로 자동으로 계산됩니다.
   * **일반 전환율**:전환율은 분석 시스템의 예측 또는 과거 데이터를 기반으로 백분율로 표현됩니다.
   * **예상 일별 방문 수**:타깃팅 기준을 기반으로 활동을 볼 수 있는 방문자의 일별 방문 수입니다. 분석 데이터를 기준으로 생성될 수 있습니다. 이 숫자는 고유한 방문자 수가 아니라 방문 수여야 합니다.
   * **테스트 기간**: 활동을 실행할 일수입니다.

   The [!UICONTROL Traffic Estimato]r uses these statistics to determine what adjustments are needed to run a successful test.

   Near the top of the [!UICONTROL Traffic Estimator], the values you entered are calculated and the results are shown.

   ![](assets/ap_est_no.png)

   숫자를 변경하면 예측값이 변경됩니다. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the [!UICONTROL Traffic Estimator] shows how long the test will need to run to be successful. Or, if your traffic is low, the [!UICONTROL Traffic Estimator] might suggest a lower number of offer combinations so you can run the test the desired number of days.

   충분한 트래픽이 없는 경우 다음 중 한 가지 또는 모든 작업을 수행할 수 있습니다.

   * Consider using an [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) activity instead of [!UICONTROL Automated Personalization] to create experiences with several offer changes in one experience variation.
   * [!UICONTROL Automated Personalization] 활동 내에서 오퍼 조합 수를 줄입니다.
   * 활동의 지속 기간을 늘립니다.

   Adjust the numbers until the [!UICONTROL Traffic Estimator] says you have sufficient traffic, then design your test accordingly.

   ![](assets/ap_est_yes.png)

   If the traffic is sufficient, the [!UICONTROL Traffic] icon shows a green check. 충분하지 않은 경우 아이콘은 빨간색 경고 레이블을 표시합니다.

## 트래픽 견적 도구에 대한 FAQ

트래픽 견적 도구에서 작업할 때 다음 FAQ를 [!UICONTROL 고려하십시오].

### AP 활동이 충분한 트래픽을 가지고 있을 때 맞춤형 모델을 구축하지 [!DNL Target] 않는 이유는 무엇입니까?

특정 상황에서 트래픽이 너무 커서 개인화된 모델이 빌드될 수 있지만 트래픽은 개인화된 모델과 임의 간에 의미 있는 차이가 없음을 나타낼 수 [!DNL Target] 있습니다. 모델이 내장된 [!DNL Target] 후 테스트되더라도 모델이 무작위보다 크게 뛰어난 것은 아니므로 배포되지 않습니다.

모델이 무작위보다 좋지 않은 이유는 오퍼가 서로 크게 다르지 않기 때문일 수 있습니다. 이 경우 메시지가 유사한 경우 오퍼를 시각적으로 더 다르게 만들거나 메시지 자체를 변경해 볼 수 있습니다.
