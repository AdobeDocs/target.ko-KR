---
keywords: 트래픽 견적 도구;자동화된 개인화;ap;트래픽 예측
description: '[!UICONTROL 트래픽 견적 도구]를 사용하여 [!UICONTROL Automated Personalization] 활동을 성공적으로 수행할 수 있는 트래픽이 충분한지 평가하십시오.'
title: 성공적인 [!UICONTROL Automated Personalization] 활동을 위해 필요한 트래픽의 양은 얼마입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
TQID: 'https://experienceleague.adobe.com/rLjNgDlAWK-r9Zv7083vo-PdWTPy3aHGS4fXEGeTdnY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 8%
---
# 성공에 필요한 트래픽 예측 {#traffic-estimator}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 트래픽 견적 도구]**&#x200B;를 사용하여 **[!UICONTROL Automated Personalization]** 활동에 충분한 트래픽이 있는지 확인하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target] **[!UICONTROL 트래픽 견적 도구]**&#x200B;는 **[!UICONTROL Automated Personalization]**(AP) 활동이 성공하기 위한 트래픽이 충분한지 여부를 알 수 있는 피드백을 제공합니다. AP 활동은 여러 오퍼 조합을 사용하므로 의미 있는 결과를 제공하는 데 필요한 트래픽의 양을 파악하는 것이 중요합니다. **[!UICONTROL 트래픽 견적 도구]**&#x200B;는 페이지 및 테스트되는 경험 수에 대한 통계를 사용하여 성공적인 활동을 만드는 데 필요한 트래픽의 양과 테스트 기간을 예측합니다.

**[!UICONTROL 트래픽 견적 도구]**&#x200B;는 예상 페이지 노출 횟수와 해당 페이지의 일반 전환율을 비교하여 개인화된 모델을 생성할 트래픽이 충분한지 여부를 결정합니다. 이상적으로는 활동이 성공하려면 올바른 샘플 크기를 사용되어 개인화된 콘텐츠가 활동 지속 기간의 50% 또는 14일 중에서 더 짧은 기간 안에 준비될 수 있어야 합니다. 이 프로세스를 통해 개인화된 콘텐츠를 획득하고 전달할 콘텐츠를 학습하는 데 충분한 시간이 소요됩니다.

[!DNL Target]은(는) 개인화 알고리즘이 빌드될 때까지 경험을 임의로 제공합니다. 각 오퍼 옆의 확인 표시 아이콘은 해당 오퍼에 대한 모델이 준비되고, [!DNL Target]에서 개인화된 콘텐츠를 전달할 수 있게 되면 표시됩니다. 상승도는 모델이 준비된 후에만 예상되므로 시각적 표시를 통해 적절한 기대를 설정할 수 있습니다. 모델이 준비되는 시기에 대한 지침을 얻으려면 **[!UICONTROL 시각적 경험 작성기]**(VEC)의 **[!UICONTROL 트래픽 견적 도구]**&#x200B;를 사용하십시오.

>[!NOTE]
>
>트래픽이 충분하더라도 개인화된 모델이 항상 배포되는 것은 아닙니다. [!DNL Target]이(가) 모델을 빌드하고 테스트하지만 무작위로 선택한 경험보다 성능이 더 좋은 경우에만 모델을 배포합니다. 모델이 무작위보다 낫지 않으면 오퍼가 서로 충분히 다르지 않을 수 있습니다. 이 경우, 메시징이 유사한 경우 오퍼를 시각적으로 더 다르게 만들거나 메시지 자체를 변경합니다.

## 트래픽 견적 도구 사용 {#use-traffic-estimator}

**[!UICONTROL Automated Personalization]** 활동을 빌드하는 동안 **[!UICONTROL 트래픽 견적 도구]**&#x200B;를 사용하여 페이지에 대한 트래픽이 개인화된 모델을 적시에 준비하기에 충분한지 확인할 수 있습니다. 활동을 시작하기 전에 이 검사를 실행하면 개인화된 콘텐츠를 제공할 만큼 충분한 방문자에게 도달할 수 없는 테스트를 방지하는 데 도움이 되며, 트래픽이 충분하지 않은 경우 오퍼 조합 수 또는 활동 기간을 조정하는 방법을 보여 줍니다.

1. **[!UICONTROL Automated Personalization]** 활동에서 **[!UICONTROL 시각적 경험 작성기]의 &#x200B;** [!UICONTROL 경험]** 페이지에 액세스합니다.

1. **[!UICONTROL 트래픽]** 아이콘(![트래픽 견적 도구 아이콘](/help/main/assets/icons/Gauge2.svg))을 클릭합니다.

   **[!UICONTROL 트래픽 견적 도구]**&#x200B;가 열립니다. 창을 종료하려면 아이콘을 다시 클릭합니다.

   ![트래픽 견적 도구 사용자 인터페이스](assets/ap-est.png)

1. 일반적인 전환율(또는 이 활동에서 예상하는 전환율), 일별 예상 활동 노출 수 및 테스트 기간을 지정합니다.

   **[!UICONTROL 트래픽 견적 도구]**&#x200B;는 이러한 지표를 사용하여 테스트를 성공적으로 실행하기 위해 필요한 조정을 결정합니다.

   | 지표 | 설명 |
   | --- | --- |
   | **[!UICONTROL 오퍼 수]** | 이 지표는 제외 후 활동의 일부로 만들어지는 경험 수에 따라 자동으로 계산됩니다. |
   | **[!UICONTROL 일반 전환율]** | 이 지표는 사용자의 예측 또는 분석 시스템의 과거 데이터를 기반으로 백분율로 표시됩니다. |
   | **[!UICONTROL 일별 예상 방문자 수]** | 이 지표는 타깃팅 기준에 따라 활동을 볼 수 있는 방문자의 일일 방문 횟수입니다. 이 지표는 분석 데이터를 기반으로 할 수 있습니다. 이 숫자는 고유 방문자가 아닌 방문자여야 합니다. |
   | **[!UICONTROL 테스트 기간]** | 활동을 실행할 일수입니다. |



1. 결과를 검토합니다. 숫자를 변경하면 예측값이 변경됩니다.

   예를 들어, 많은 조합을 테스트하고 전환율과 노출이 너무 낮은 경우 **[!UICONTROL 트래픽 견적 도구]**&#x200B;는 테스트가 성공적으로 실행되기 위해 실행해야 하는 시간을 보여 줍니다. 또는 트래픽이 낮은 경우 **[!UICONTROL 트래픽 견적 도구]**&#x200B;에서 더 적은 수의 오퍼 조합을 제안하여 원하는 일수로 테스트를 실행할 수 있습니다.

   ![값 및 결과가 표시된 트래픽 예상](assets/ap-est-no.png)

1. 트래픽이 충분하지 않은 경우 다음 옵션을 고려하십시오.

   * **[!UICONTROL Automated Personalization]** 대신 [**[!UICONTROL 자동 타겟]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 활동을 사용하여 하나의 경험 변형에서 여러 오퍼 변경 사항을 사용하는 경험을 만드십시오.
   * **[!UICONTROL Automated Personalization]** 활동 내에서 오퍼 조합 수를 줄이십시오.
   * 활동의 지속 기간을 늘립니다.

1. **[!UICONTROL 트래픽 견적 도구]**&#x200B;가 충분한 트래픽이 있음을 나타낼 때까지 숫자를 조정한 다음 그에 따라 테스트를 디자인합니다.

   트래픽이 충분하면 **[!UICONTROL 트래픽]** 아이콘에 녹색 확인이 표시됩니다. 충분하지 않은 경우 아이콘은 빨간색 경고 레이블을 표시합니다.

   ![트래픽 견적 도구(충분한 트래픽 메시지 표시)](assets/ap-est-yes.png)
