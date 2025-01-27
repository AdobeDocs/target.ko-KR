---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: ' [!DNL Adobe Target] [!UICONTROL Multivariate Test] 활동을 성공시킬 수 있는 트래픽이 충분한지 확인할 수 있는 트래픽 견적 도구를 사용하는 방법을 알아봅니다.'
title: '[!UICONTROL Multivariate Test](MVT) 활동에 필요한 트래픽의 양은 얼마입니까?'
feature: Multivariate Tests
hide: true
hidefromtoc: true
source-git-commit: 4805da617962e29794bd3af16138f3887ad250d0
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 21%

---

# 성공적인 [!UICONTROL Multivariate Test] 활동에 필요한 트래픽 예측

다변량 테스트는 여러 개의 경험을 비교하기 때문에 의미있는 결과를 제공하는 데 필요한 트래픽의 양을 파악하는 것이 중요합니다. [!UICONTROL Traffic Estimator]은(는) 페이지 및 테스트되는 경험 수에 대한 통계를 사용하여 테스트를 성공적으로 수행하는 데 필요한 트래픽의 양과 테스트 기간을 예측합니다.

[!UICONTROL Traffic Estimator]은(는) 다음을 확인하는 데 필요한 샘플 크기를 예측합니다.

* 95% 신뢰도. 이 통계는 실제 상승도가 없는 경우 긍정 오류(false positive)를 보고할 확률이 5%(100% - 신뢰 수준)임을 의미합니다.
* 80%의 통계적 검증력. 이 통계는 테스트가 25% 이상의 실제 상승도를 감지할 확률이 80%라는 것을 의미합니다.
* 확실히 감지 가능한 최소 25% 상승도. [!DNL Target]은(는) 25% 이상의 실제 상승도를 감지할 80% 가능성을 가져야 하는 트래픽의 양을 계산합니다.

테스트는 Bonferroni 수정을 사용하여 다중 비교에 맞게 수정합니다. 이 방법은 비교적 큰 최소 안정적인 감지 가능한 상승도를 적용하여 균형을 맞추는 보수적 방식으로 알려져 있습니다.

[!UICONTROL Traffic Estimator]은(는) 테스트를 성공하기 위해 충분한 트래픽이 있는지 여부를 알 수 있는 피드백도 제공합니다.

1. [!UICONTROL Multivariate] 활동에 있는 [!UICONTROL Visual Experience Composer]의 [!UICONTROL Experiences] 페이지에서 [!UICONTROL Experiences] 페이지의 왼쪽 상단 모서리에 있는 **[!UICONTROL Traffic]** 아이콘(![트래픽 견적 도구 아이콘](/help/main/assets/icons/Gauge2.svg))을 클릭합니다.

   [!UICONTROL Traffic Estimator]이(가) 열립니다.

   ![트래픽 견적 도구 사용자 인터페이스](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   아이콘을 다시 클릭하여 [!UICONTROL Traffic Estimator]을(를) 숨길 수 있습니다.

   [!UICONTROL Traffic Estimator]의 상단 근처에서 입력한 값이 계산되고 결과가 표시됩니다.

1. (조건부) 일반적인 전환율, 일별 예상 방문자 수 및 테스트 기간을 제공합니다.

   * **[!UICONTROL Number of Content Combinations]**: 제외 후 활동의 일부로 만들어지는 경험 수에 따라 자동으로 계산됩니다.
   * **[!UICONTROL Typical Conversion Rate]**: 전환율은 사용자의 예측 또는 분석 시스템의 과거 데이터를 기준으로 백분율로 표시됩니다.
   * **[!UICONTROL Estimated Visitors Per Day]**: 타깃팅 기준에 따라 이 페이지를 볼 수 있는 방문자의 수입니다. 분석 데이터를 기준으로 생성될 수 있습니다.
   * **[!UICONTROL Test Duration]**: 활동을 실행할 일수입니다.

   [!UICONTROL Traffic Estimator]은(는) 이러한 통계를 사용하여 테스트를 성공적으로 실행하기 위해 필요한 조정을 결정합니다.

   숫자를 변경하면 예측값이 변경됩니다. 예를 들어, 많은 경험을 테스트하고 전환율과 노출이 너무 낮은 경우 [!UICONTROL Traffic Estimator]은(는) 테스트를 성공적으로 실행하기 위해 실행해야 하는 시간을 보여 줍니다. 또는 트래픽이 낮은 경우 [!UICONTROL Traffic Estimator]에서 더 적은 수의 경험을 제안하여 원하는 일수로 테스트를 실행할 수 있습니다.

   충분한 트래픽이 없는 경우 다음 중 한 가지 또는 두 작업을 모두 수행할 수 있습니다.

   * 오퍼의 조합 수와 위치 수를 줄입니다.
   * 테스트의 지속 기간을 늘립니다.

   [!UICONTROL Traffic Estimator]이(가) 트래픽이 충분함을 나타낼 때까지 숫자를 조정한 다음 그에 따라 테스트를 디자인합니다.
