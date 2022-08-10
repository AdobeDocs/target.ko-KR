---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe에서 자동 할당 및 자동 Target 활동을 만드는 방법을 알아봅니다 [!DNL Target] 를 보고 소스로 사용(A4T)하는 것과 같습니다.
title: A4T가 자동 할당 및 자동 Target 활동을 지원합니까?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: e8fc28ef2497c1dfea523a769c9c817cbd74fea2
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 3%

---

# 자동 할당 및 자동 타겟 활동에 대한 A4T 지원

다음 [!DNL Adobe Target]-to-[!DNL Adobe Analytics] 통합, 알려진 [Target 분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T)에서 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동.

A4T 통합을 사용하면 다음 작업을 수행할 수 있습니다.

* 사용 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)트래픽을 유도하여 우승 경험으로 전환하는 의 다중 무장 bandit 기능입니다.
* 사용 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)의 ensemble machine learning 알고리즘을 사용하여 각 방문자에 대해 최상의 경험을 선택할 수 있습니다. 자동 Target은 을 사용하는 동안 사용자의 프로필, 동작 및 컨텍스트를 기반으로 최상의 경험을 선택합니다 [!DNL Adobe Analytics] 목표 지표 및 [!DNL Adobe Analytics]&#39; 풍부한 보고 및 분석 기능.

다음을 확인하십시오. [A/B 테스트 및 경험 타깃팅 활동에 사용하기 위해 A4T를 구현했습니다](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). 사용 중인 경우 `analyticsLogging = client_side`, 도 전달해야 합니다. `sessionId` 값 [!DNL Analytics]. 자세한 내용은 [A4T(Target 분석) 보고](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/)의 {target=_blank} *Adobe Target SDK* 안내서.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 작성하는 동안 **[!UICONTROL 타깃팅]** 페이지에서 다음 옵션 중 하나를 **[!UICONTROL 트래픽 할당 방법]**:

   * [!UICONTROL 최고 경험에 자동 할당]
   * [!UICONTROL 개인화된 경험에 대한 자동 Target]

   ![트래픽 할당 방법 옵션: 수동, 자동 할당 및 자동 Target](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   자세한 내용 및 단계별 지침은 [자동 할당 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 Target 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md).

1. 선택 **[!UICONTROL Adobe Analytics]** 에 대해 **[!UICONTROL 보고 소스]** on **[!UICONTROL 목표 및 설정]** 페이지를 열고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.

   ![목표 및 설정 페이지의 보고 소스 섹션](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. 기본 목표 지표를 선택합니다. 첫 번째 드롭다운에서 목표를 지정할 수 있습니다. [!DNL Adobe Target] (그런 다음 [!DNL Adobe Analytics] 를 &quot;활동 전환&quot; 지표로 사용하거나 [!DNL Analytics] 지표를 목표로 합니다.

   * 를 사용하려면 [!DNL Adobe Target] 최적화 목표를 지정하려면 **[!UICONTROL 전환]**, 그런 다음 전환 목표에 도달했음을 나타내기 위해 대상자가 수행해야 하는 작업을 지정합니다.
   * 대신 을(를) 선택하는 경우 **[!UICONTROL Analytics 지표 사용]**&#x200B;그런 다음 사용해야 하는 최적화 기준 유형을 선택할 수 있습니다.  자세한 내용은 [지원되는 목표 지표 및 최적화 기준](#supported) 아래 정보를 참조하십시오. 최적화 기준을 지정한 후 호환되는 지표를 선택할 수 있습니다 [!DNL Analytics] 을 최적화 목표로 사용할 수 있습니다. 즉시 사용 가능한 [!DNL Analytics] 전환 지표 또는 [!DNL Analytics] 사용자 지정 이벤트.


1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동 할당] 선택한 지표를 사용하여 활동을 최적화하고 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL 자동 Target] 선택한 지표를 사용하여 활동을 최적화하고 방문자를 개인화된 최상의 경험으로 유도합니다.

1. 를 사용하십시오 **[!UICONTROL 보고서]** 탭하여 활동의 보고를 보고 및 **[!UICONTROL Analytics에서 보기]** Adobe Analytics Workspace에서 보고 데이터를 심층적으로 세분화하기 위해 아래 자습서에 따라 Workspace에서 보고서를 설정하는 방법을 볼 수 있습니다.
* 자동 할당: 참조 [자동 할당 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*
* 자동 Target: 참조 [자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.

## 지원되는 목표 지표 및 최적화 기준 {#supported}

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 을 사용하면 최적화를 위한 기본 목표 지표로 다음 지표 유형을 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

하지만, [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 모델이 **정규화** 활동 유형에 따라 정확한 표준화와 함께 이러한 지표의 버전입니다. 각 활동 유형에 대한 최적화 기준에 대한 옵션은 아래 표에 설명되어 있습니다.

| 활동 유형 | 지표 소스 | 최적화 기준 | 설명 |
|---------------|---------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 자동 할당 | Analytics | 고유 방문자 전환율 최대화 | 모델은 Analytics 지표가 0이 아닌 방문자의 수로 정의되는 가장 높은 고유 방문자 전환율을 사용하여 경험을 찾으려고 합니다. 이 수는 해당 경험을 받은 방문자의 총 수로 나누어집니다. 이것은 지표가 활동의 각 고유 방문자에 대해 바이너리로 처리되거나, 0이거나 1로 처리됨을 의미합니다.   특정 작업을 수행하는 사용자의 일부에만 관심이 있거나 단일 사용자에 대한 여러 전환 이벤트가 의미 없는 경우 이 옵션을 사용합니다. |
| 자동 할당 | Analytics | 방문자당 지표 값 최대화 | 모델은 해당 경험에 노출된 모든 사용자에 대한 지표의 합계 값으로 해당 경험을 받은 총 방문자 수로 나눈 방문자당 가장 높은 지표 값을 갖는 경험을 찾으려고 합니다. 즉, 지표는 활동의 각 고유 방문자에 대해 어떤 값이든 취할 수 있습니다. 예를 들어 방문자가 여러 번 전환하는 경우 각 전환이 카운트됩니다.  총 매출과 같은 연속 지표를 최대화하거나 단일 사용자에 대한 여러 전환 이벤트가 두 개보다 의미 있는 경우(예: 여러 주문이 두 개 이상의 가치 있는 경우) 이 선택 사항을 사용합니다 |
| 자동 할당 | Target | (구성할 수 없음) | 지표는 바이너리로 처리되며 고유한 방문자 전환율을 극대화합니다. |
| 자동 타겟 | Analytics | 고유 방문 전환율 최대화 | 자동 할당 또는 수동 A/B 테스트와 달리, 자동 타겟의 개인화된 특성은 방문자가 보는 경험이 새로운 모든 방문에 대해 변경될 수 있음을 의미합니다. 그런 다음 적절한 비율은 비0 지표가 기록되는 방문의 분수로 정의된 방문 표준화된 전환율입니다. 이것은 자동 타겟에 의해 최적화된 전환율입니다.   자동 할당과 마찬가지로, 단일 방문에 대해 발생하는 여러 전환 이벤트가 중요하지 않은 경우 전환이 발생하는 방문의 분수에 대해 고려할 때 이 옵션을 선택해야 합니다. |
| 자동 타겟 | Analytics | 방문당 지표 값 최대화 | 최적화되는 지표가 지속(예: 수입)이거나, 단일 방문에서 여러 전환 이벤트가 존재하는 것이 의미 있는 경우(예: 여러 주문) 방문당 지표 값을 최대화하도록 선택할 수 있습니다. 최적화되는 &quot;비율&quot;은 지표의 합계 값으로서 방문 횟수로 나눈 값입니다. |
| 자동 타겟 | Target | (구성할 수 없음) | 지표는 바이너리로 처리되며 고유한 방문 전환율을 극대화합니다. |



최적화 기준에 따라 특정 [!DNL Adobe Analytics] 지표는 지원되지 않습니다.

* [!DNL Adobe Analytics] 계산된 지표는 지원되지 않습니다.
* [!DNL Adobe Analytics] 지표는 항상 세그먼트화할 수 있어야 하며, 방문자/방문당 값이 최적화된 경우 지표에 양의 극성이 있어야 합니다(즉, 양수 값이 음수 값보다 나음)
* [!DNL Adobe Analytics] 에 사용된 지표 [!DNL Auto-Target] 활동은 DataWarehouse 내보내기에서 사용할 수 있어야 합니다.

## 제한과 참고 사항

몇 가지 제한 사항과 참고는 두 가지 모두에 적용됩니다 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동. 다른 제한 사항 및 참고는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

### 자동 할당 및 자동 타기팅 {#both}

* 사용 시 [!DNL Adobe Analytics] 를 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target]에서는 항상 보고서를 [!DNL Analytics].
* 보고 소스를 [!DNL Analytics] to [!DNL Target] 또는 반대로 활동이 활성화되면 무시됩니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도한 결과를 달성하는 것이 종종 가능합니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면, &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. 에 설명된 대로 [지원되는 목표 지표 및 최적화 기준](#supported), 활동 유형 및 최적화 기준에 따라, [!DNL Target] 은 전환 지표를 자동으로 정규화하므로 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.


### 자동 할당 {#aa}

* **교육 빈도**: [!UICONTROL 자동 할당] 모델들은 평상시처럼 매시간 훈련한다.
* **속성 모델**: [!DNL Target] 사용 [!DNL Adobe Analytics] 기본 속성 모델[!UICONTROL  자동 할당] A4T를 사용하는 활동.
* **신뢰도**: 에 사용되는 신뢰도 공식입니다 [!UICONTROL 자동 할당] 활동은 기본적으로 [!DNL Adobe Analytics] [!UICONTROL A4T] 패널. [여기에 설명된 대로](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL 자동 할당] 일반보다 더 많은 보수적 신뢰 구간을 사용합니다 [!UICONTROL A/B 테스트] 활동. 이러한 보수적 신뢰 수준은 데이터에 대한 반복적인 평가(매)를 보완합니다. 따라서 의 기본 보고서는 [!DNL Adobe Analytics] 에 사용되는 간격과 비교하여 더 좁은 신뢰 구간을 표시합니다 [!UICONTROL 자동 할당] 알고리즘에 대해 설명합니다. 하지만 고유 방문자가 더 많은 경험을 기반으로 알고리즘에서 선호되는 경험을 결정할 수 있습니다.
* **우승자 상태**: 현재, [&quot;아직 우승자 없음&quot; 및 &quot;우승자&quot; 배지](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) 에서 사용할 수 없음 [!UICONTROL A4T] 패널 [!DNL Analysis Workspace]. 이러한 배지는 같은 보고서를 [!DNL Target]. 에 표시되는 승자 &quot;별&quot; 배지 [!DNL Target] 보고서 [!UICONTROL 자동 할당] A4T를 사용하는 활동은 무시해야 합니다. 이 배지는 일반적인 신뢰 계산을 반영하며 [!UICONTROL 자동 할당].

### 자동 타겟 {#at}

* **교육 빈도**: [!UICONTROL 자동 Target] 모델들은 평소대로 24시간 간격으로 훈련을 계속한다. 그러나 전환 이벤트 데이터는에서 가져옵니다 [!DNL Analytics] 6시간에서 24시간 더 지연됩니다. 이러한 지연은 트래픽 분포를 의미합니다 [!DNL Target] 에 기록된 최신 이벤트의 추적 [!DNL Analytics]. 이 지연은 활동이 처음 활성화된 후 처음 48시간 이내에 가장 큰 영향을 줍니다. 활동의 성과가 더 밀접하게 반영될 것입니다 [!DNL Analytics] 5일이 경과된 후의 전환 동작입니다. 사용 고려 [!UICONTROL 자동 할당] 대신 [!UICONTROL 자동 Target] 활동 수명 후 처음 5일 이내에 대부분의 트래픽이 발생하는 단기 활동입니다.
* 사용 시 [!DNL Analytics] 를 [!UICONTROL 자동 Target] 활동, 세션이 6시간이 경과하면 종료됩니다. 6시간 후 발생하는 전환은 카운트되지 않습니다.

자세한 내용은 [속성 모델 및 전환 확인 기간](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) 에서 *Analytics 툴 안내서*.

## 자동 Target 및 자동 할당 활동에 대해 Analysis Workspace에서 A4T 보고서를 설정하는 방법 {#tutorial}

다양한 분석 기능은에서 사용할 수 있지만 [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], 기본값에 대한 몇 가지 수정 사항 [!UICONTROL Target 분석] 자동 할당 및 자동 Target 활동을 올바르게 해석하려면 패널이 필요합니다.

이러한 수정은 에 설명된 전환율의 정확한 정의로 인해 필요합니다 [지원되는 목표 지표 및 최적화 기준](#supported)및 실험 활동 간의 차이점(수동 A/B 및 [!UICONTROL 자동 할당]) 및 개인화 활동( )[!UICONTROL 자동 Target]).

이 자습서에서는 분석을 위한 권장 수정 사항을 안내합니다 [!UICONTROL A4T] [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동 [!UICONTROL 작업 공간].

자세한 내용은
* [자동 할당 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
* [자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
