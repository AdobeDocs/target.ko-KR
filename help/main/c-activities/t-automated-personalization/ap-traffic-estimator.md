---
keywords: 트래픽 견적 도구;자동화된 개인화;ap;트래픽 예측;자동 타겟
description: Adobe 사용 [!DNL Target] 트래픽 견적 도구 를 사용하십시오.
title: 성공적인 활동에 필요한 트래픽은 얼마입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 14%

---

# 성공에 필요한 트래픽 예측

다음 [!DNL Adobe Target] [!UICONTROL 트래픽 견적 도구] 은 사용자의 트래픽이 충분한지 여부를 알 수 있도록 해주는 피드백을 제공합니다 [!UICONTROL Automated Personalization] 성공을 위한 활동.

왜냐면 [!UICONTROL Automated Personalization] 활동에서는 여러 오퍼 조합을 사용하므로 의미 있는 결과를 제공하는 데 필요한 트래픽의 양을 파악하는 것이 중요합니다. 다음 [!UICONTROL 트래픽 견적 도구] 에서는 페이지 및 테스트되는 경험 수에 대한 통계를 사용하여 트래픽 양과 활동을 성공적으로 수행하는 데 필요한 테스트 기간을 예측합니다.

다음 [!UICONTROL 트래픽 견적 도구] 예상 페이지 노출 수와 페이지에 대한 일반적인 전환율을 비교하여 개인화된 모델을 생성할 충분한 트래픽이 있는지 여부를 결정합니다. 이상적으로는 활동이 성공하려면 올바른 샘플 크기를 사용되어 개인화된 콘텐츠가 활동 지속 기간의 50% 또는 14일 중에서 더 짧은 기간 안에 준비될 수 있어야 합니다. 이 프로세스를 통해 개인화된 콘텐츠를 획득하고 전달할 콘텐츠를 학습하기 위한 충분한 시간을 확보할 수 있습니다.

기억해 [!DNL Target] 개인화 알고리즘이 빌드될 때까지 경험을 임의로 제공합니다. 각 오퍼 옆의 확인 표시 아이콘은 해당 오퍼에 대한 모델이 준비되면 표시됩니다. [!DNL Target] 은 개인화된 콘텐츠를 전달할 수 있습니다. 상승도는 모델이 준비된 후에만 예측되므로 시각적 표시를 통해 적절한 기대 수준을 설정할 수 있습니다. 를 사용하십시오 [!UICONTROL 트래픽 견적 도구] 에서 [!UICONTROL 시각적 경험 작성기] (VEC) 를 사용하여 모델이 준비되는 시점을 안내할 수 있습니다.

## 트래픽 견적 도구 사용

1. 에서 [!UICONTROL 시각적 경험 작성기]를 클릭합니다. **[!UICONTROL 트래픽]**.

   ![트래픽 아이콘](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   다음 [!UICONTROL 트래픽 견적 도구] 엽니다. **[!UICONTROL 트래픽]**[!UICONTROL 을 다시 클릭하여 트래픽 견적 도구를 숨길 수 있습니다].

   ![트래픽 견적 도구 사용자 인터페이스](assets/ap_est.png)

1. 일반적인 전환율(또는 이 활동에서 예상하는 전환율), 일별 예상 활동 노출 수 및 테스트 지속 기간을 지정합니다.

   | 지표 | 설명 |
   | --- | --- |
   | **[!UICONTROL 오퍼 수]** | 이 지표는 제외 후 활동의 일부로 만들어지는 경험 수에 따라 자동으로 계산됩니다. |
   | **[!UICONTROL 일반적인 전환율]** | 이 지표는 사용자의 예측 또는 분석 시스템의 과거 데이터를 기준으로 백분율로 표시됩니다. |
   | **[!UICONTROL 일별 예상 방문 수]** | 이 지표는 타깃팅 기준에 따라 활동을 볼 수 있는 방문자의 일별 방문 수입니다. 이 지표는 분석 데이터를 기반으로 할 수 있습니다. 이 숫자는 고유 방문자가 아니라 방문이어야 합니다. |
   | **[!UICONTROL 테스트 지속 기간]** | 활동을 실행할 일수입니다. |

   다음 [!UICONTROL 트래픽 견적 도구] 이 지표를 사용하여 성공적인 테스트를 실행하기 위해 필요한 조정을 확인합니다.

   위쪽 [!UICONTROL 트래픽 견적 도구]입력한 값이 계산되고 결과가 표시됩니다.

   ![값과 결과가 표시된 트래픽 예측](assets/ap_est_no.png)

   숫자를 변경하면 예측값이 변경됩니다. 예를 들어, 많은 조합을 테스트하고 전환율과 노출이 너무 낮은 경우 [!UICONTROL 트래픽 견적 도구] 테스트를 실행해야 하는 시간을 표시합니다. 또는 트래픽이 낮은 경우 [!UICONTROL 트래픽 견적 도구] 테스트를 실행할 수 있도록 낮은 수의 오퍼 조합을 제안할 수 있습니다.

   트래픽이 충분하지 않은 경우 다음을 고려하십시오.

   * 다음 사용 고려 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 활동 대신 [!UICONTROL Automated Personalization] 한 경험 변수에서 여러 오퍼 변경 사항이 있는 경험을 만들려면 다음을 수행하십시오.
   * 내 오퍼 조합 수를 줄입니다 [!UICONTROL Automated Personalization] 활동.
   * 활동의 지속 기간을 늘립니다.

   숫자를 [!UICONTROL 트래픽 견적 도구] 트래픽이 충분함을 나타내는 다음, 그에 따라 테스트를 디자인합니다.

   ![충분한 트래픽 메시지를 표시하는 트래픽 견적 도구](assets/ap_est_yes.png)

   트래픽이 충분하면 [!UICONTROL 트래픽] 아이콘에 녹색 확인이 표시됩니다. 충분하지 않은 경우 아이콘은 빨간색 경고 레이블을 표시합니다.

## 트래픽 견적 도구에 대한 FAQ

작업 시 다음 FAQ를 고려하십시오 [!UICONTROL 트래픽 견적 도구]:

### 내 AP 활동에 트래픽이 충분해도 개인화된 모델이 만들어지지 않는 이유는 무엇입니까?

특정 상황에서 트래픽이 커서 개인화된 모델을 구축할 수 있지만 트래픽이 이를 알릴 수 있습니다 [!DNL Target] 개인화된 모델과 무작위 간에 의미 있는 차이가 없다는 것입니다. 모델이 빌드되어 있지만 [!DNL Target] 그리고 테스트한 경우, 모델이 임의 모델보다 나은 것이 아니므로 배포되지 않습니다.

모델이 무작위보다 더 나은 것이 아닌 가능한 이유는 오퍼가 서로 충분히 다르지 않기 때문입니다. 그럴 경우 메시징이 유사한 경우 오퍼를 시각적으로 더 다르게 하거나 메시지 자체를 변경해 볼 수 있습니다.
