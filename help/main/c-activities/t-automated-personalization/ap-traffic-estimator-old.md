---
keywords: 트래픽 견적 도구;자동화된 개인화;ap;트래픽 예측
description: ' [!DNL Adobe Target] [!UICONTROL Traffic Estimator]을(를) 사용하여 [!UICONTROL Automated Personalization] 활동이 성공하기에 충분한 트래픽이 있는지 확인하십시오.'
title: 성공적인 [!UICONTROL Automated Personalization] 활동을 위해 필요한 트래픽의 양은 어느 정도입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 10%

---

# 성공에 필요한 트래픽 예측

[!DNL Adobe Target] [!UICONTROL Traffic Estimator]은(는) [!UICONTROL Automated Personalization](AP) 활동을 성공적으로 수행할 수 있는 트래픽이 충분한지 여부를 알 수 있는 피드백을 제공합니다.

[!UICONTROL Automated Personalization] 활동은 여러 오퍼 조합을 사용하므로 의미 있는 결과를 제공하는 데 필요한 트래픽의 양을 파악하는 것이 중요합니다. [!UICONTROL Traffic Estimator]은(는) 페이지 및 테스트되는 경험 수에 대한 통계를 사용하여 성공적인 활동을 만드는 데 필요한 트래픽의 양과 테스트 기간을 예측합니다.

[!UICONTROL Traffic Estimator]은(는) 예상 페이지 노출 횟수와 해당 페이지의 일반 전환율을 비교하여 개인화된 모델을 생성할 트래픽이 충분한지 확인합니다. 이상적으로는 활동이 성공하려면 올바른 샘플 크기를 사용되어 개인화된 콘텐츠가 활동 지속 기간의 50% 또는 14일 중에서 더 짧은 기간 안에 준비될 수 있어야 합니다. 이 프로세스를 통해 개인화된 콘텐츠를 획득하고 전달할 콘텐츠를 학습하는 데 충분한 시간이 소요됩니다.

[!DNL Target]은(는) 개인화 알고리즘이 빌드될 때까지 경험을 임의로 제공합니다. 각 오퍼 옆의 확인 표시 아이콘은 해당 오퍼에 대한 모델이 준비되고, [!DNL Target]에서 개인화된 콘텐츠를 전달할 수 있게 되면 표시됩니다. 상승도는 모델이 준비된 후에만 예상되므로 시각적 표시를 통해 올바른 기대를 설정할 수 있습니다. 모델이 준비되는 시기에 대한 지침을 얻으려면 [!UICONTROL Visual Experience Composer](VEC)의 [!UICONTROL Traffic Estimator]을(를) 사용하십시오.

## 트래픽 견적 도구 사용

1. [!UICONTROL Automated Personalization] 활동에 있는 [!UICONTROL Visual Experience Composer]의 [!UICONTROL Experiences] 페이지에서 **[!UICONTROL Traffic]** 아이콘을 클릭합니다.

   ![트래픽 아이콘](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   [!UICONTROL Traffic Estimator]이(가) 열립니다. **[!UICONTROL Traffic]**&#x200B;을(를) 다시 클릭하여 [!UICONTROL Traffic Estimator]을(를) 숨길 수 있습니다.

   ![트래픽 견적 도구 사용자 인터페이스](assets/ap_est.png)

1. 일반적인 전환율(또는 이 활동에서 예상하는 전환율), 일별 예상 활동 노출 수 및 테스트 기간을 지정합니다.

   | 지표 | 설명 |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | 이 지표는 제외 후 활동의 일부로 만들어지는 경험 수에 따라 자동으로 계산됩니다. |
   | **[!UICONTROL Typical Conversion Rate]** | 이 지표는 사용자의 예측 또는 분석 시스템의 과거 데이터를 기반으로 백분율로 표시됩니다. |
   | **[!UICONTROL Estimated Visits Per Day]** | 이 지표는 타깃팅 기준에 따라 활동을 볼 수 있는 방문자의 일일 방문 횟수입니다. 이 지표는 분석 데이터를 기반으로 할 수 있습니다. 이 숫자는 고유 방문자가 아닌 방문자여야 합니다. |
   | **[!UICONTROL Test Duration]** | 활동을 실행할 일수입니다. |

   [!UICONTROL Traffic Estimator]은(는) 이러한 지표를 사용하여 테스트를 성공적으로 실행하기 위해 필요한 조정을 결정합니다.

   [!UICONTROL Traffic Estimator]의 상단 근처에서 입력한 값이 계산되고 결과가 표시됩니다.

   ![값 및 결과가 표시된 트래픽 예상](assets/ap_est_no.png)

   숫자를 변경하면 예측값이 변경됩니다. 예를 들어, 많은 조합을 테스트하고 있으며 전환율과 노출이 너무 낮은 경우 [!UICONTROL Traffic Estimator]은 테스트를 성공적으로 실행하기 위해 실행해야 하는 시간을 보여줍니다. 또는 트래픽이 낮은 경우 [!UICONTROL Traffic Estimator]에서 더 적은 수의 오퍼 조합을 제안하여 원하는 일수로 테스트를 실행할 수 있습니다.

   트래픽이 충분하지 않은 경우 다음 사항을 고려하십시오.

   * 한 경험 변형에서 여러 오퍼 변경 사항을 가진 경험을 만들려면 [!UICONTROL Automated Personalization] 대신 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 활동을 사용하는 것이 좋습니다.
   * [!UICONTROL Automated Personalization] 활동 내에서 오퍼 조합 수를 줄이십시오.
   * 활동의 지속 기간을 늘립니다.

   [!UICONTROL Traffic Estimator]이(가) 트래픽이 충분함을 나타낼 때까지 숫자를 조정한 다음 그에 따라 테스트를 디자인합니다.

   ![트래픽 견적 도구(충분한 트래픽 메시지 표시)](assets/ap_est_yes.png)

   트래픽이 충분하면 [!UICONTROL Traffic] 아이콘에 녹색 확인이 표시됩니다. 충분하지 않은 경우 아이콘은 빨간색 경고 레이블을 표시합니다.

## 트래픽 견적 도구 와 관련하여 자주 묻는 질문

[!UICONTROL Traffic Estimator] 작업 시 다음 FAQ를 고려하십시오.

### AP 활동에 트래픽이 충분한데 개인화된 모델이 만들어지지 않는 이유는 무엇입니까?

특정 상황에서 트래픽은 개인화된 모델을 만들 수 있을 만큼 충분히 크지만 해당 트래픽은 [!DNL Target]에 개인화된 모델과 임의 모델 간에 의미 있는 차이가 없음을 알릴 수 있습니다. 모델이 [!DNL Target]에 만들어져 테스트되었지만 모델이 임의 모델보다 좋지 않으므로 배포되지 않습니다.

모델이 무작위보다 좋지 않은 가능한 이유는 오퍼가 서로 충분히 다르지 않기 때문일 수 있습니다. 그렇다면 메시징이 유사한 경우 오퍼를 시각적으로 더 다르게 만들거나 메시지 자체를 변경할 수 있습니다.
