---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용;Analytics를 Target으로 사용
description: ' [!DNL Analytics] 을(를) 보고 소스(A4T)로 사용하는 [!DNL Target] 에서 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동을 만드는 방법을 알아봅니다.'
title: A4T가 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동을 지원합니까?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 80e4741f5f501a48b15b718c6c0bf55a86c4d676
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 1%

---

# [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동에 대한 A4T 지원

[Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)으로 알려진 [!DNL Adobe Target]-to-[!DNL Adobe Analytics] 통합은 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동을 지원합니다.

A4T 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.

* [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) multi-armed bandit 기능을 사용하여 트래픽을 승리 경험으로 유도합니다.
* [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 앙상블 머신 러닝 알고리즘을 사용하여 각 방문자에게 가장 적합한 경험을 선택하십시오. [!UICONTROL Auto-Target]은(는) [!DNL Adobe Analytics] 목표 지표와 [!DNL Adobe Analytics]의 풍부한 보고 및 분석 기능을 사용하는 동안 각 사용자의 프로필, 동작 및 컨텍스트를 기반으로 최상의 경험을 선택합니다.

[A/B 테스트 및 경험 타깃팅 활동과 함께 사용할 A4T를 구현했는지 확인](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). `analyticsLogging = client_side`을(를) 사용하는 경우 `sessionId` 값도 [!DNL Analytics]에 전달해야 합니다. 자세한 내용은 *Adobe Target 개발자 안내서*&#x200B;에서 [Analytics for Target(A4T) 보고](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank}를 참조하십시오.

시작하려면 다음 단계를 따르십시오. 

1. [[!UICONTROL A/B Test] 활동을 만드는 중](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) **[!UICONTROL Targeting]** 페이지에서 다음 옵션 중 하나를 **[!UICONTROL Traffic Allocation Method]**(으)로 선택합니다.

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experiences]

   ![트래픽 할당 방법 옵션: 수동, 자동 할당 및 자동 타겟](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   자세한 내용과 단계별 지침은 [자동 할당 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 타겟 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md)를 참조하십시오.

1. **[!UICONTROL Goals & Settings]** 페이지에서 **[!UICONTROL Reporting Source]**&#x200B;에 대해 **[!UICONTROL Adobe Analytics]**&#x200B;을(를) 선택하고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.

   ![목표 및 설정 페이지의 Source 보고 섹션](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. [!UICONTROL Primary Goal] 지표를 선택하십시오.

   * [!DNL Adobe Target]을(를) 사용하여 최적화 목표를 지정하려면 **[!UICONTROL Conversion]**&#x200B;을(를) 선택하십시오.
   * **[!UICONTROL Use an Analytics metric]**&#x200B;을(를) 선택한 다음 최적화 목표로 사용할 지표를 [!DNL Analytics]에서 선택하십시오. 기본 [!DNL Analytics] 전환 지표 또는 [!DNL Analytics] 사용자 지정 이벤트를 사용할 수 있습니다.

   자세한 내용은 아래의 [지원되는 목표 지표](#supported)를 참조하십시오.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL Auto-Allocate]은(는) 선택한 지표를 사용하여 활동을 최적화함으로써 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL Auto-Target]은(는) 선택한 지표를 사용하여 활동을 최적화함으로써 방문자를 개인화된 최상의 경험으로 유도합니다.

1. [!DNL Adobe Analytics] 지표를 선택하여 활동의 보고를 보려면 **[!UICONTROL Reports]** 탭을 사용하십시오. 보고 데이터를 자세히 살펴보고 추가로 세그먼트화하려면 **[!UICONTROL View in Analytics]**&#x200B;을(를) 클릭하십시오.

## 지원되는 목표 지표 {#supported}

[!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target]에 대한 [!UICONTROL A4T]을(를) 사용하면 최적화를 위한 기본 목표 지표로 다음 지표 유형 중 하나를 선택할 수 있습니다.

* 전환 지표 [!DNL Adobe Target]개
* 전환 지표 [!DNL Adobe Analytics]개
* [!DNL Adobe Analytics]개의 사용자 지정 이벤트

>[!NOTE]
>
>[!UICONTROL Use an Analytics Metric]을(를) 선택한 후 [!UICONTROL Maximize Unique Visitor Conversion Rate]을(를) 선택하여 사용 가능한 [!DNL Adobe Analytics] 전환 지표를 보고 [!UICONTROL Maximize Metric Value per Visitor]을(를) 선택하여 [!DNL Adobe Analytics] 사용자 지정 이벤트를 살펴보십시오.

[!DNL Target]을(를) 사용하면 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동에 [!UICONTROL A4T]을(를) 사용할 때 이항 이벤트를 기반으로 하는 지표 또는 연속 이벤트를 기반으로 하는 지표를 선택할 수 있습니다.

* **이항 이벤트를 기반으로 하는 지표**: 이항 이벤트가 발생하거나 발생하지 않습니다. 이항 이벤트에는 클릭, 전환, 순서 등이 포함됩니다. 이러한 유형의 이벤트는 베르누이, 이진 또는 이산 이벤트라고도 합니다.

* **연속 이벤트를 기반으로 한 지표**. 연속 지표에는 매출, 주문한 제품 수, 세션 기간, 세션의 페이지 보기 수 등이 포함됩니다. 이러한 유형의 이벤트는 비이항 또는 비베르누이 지표라고도 합니다.

>[!IMPORTANT]
>
>[!DNL Adobe Target Standard/Premium] 22.15.1 릴리스(2023년 3월 8일 및 9일)부터 [!DNL Target]은(는) 현재 지원되지 않는 지표(다음 표에 나열됨)를 사용하여 기존 활동을 계속 지원합니다. 그러나 2023년 9월 9일 이후에는 이러한 지표가 기존 활동에서 더 이상 지원되지 않으며 지원되지 않는 지표를 사용하는 모든 활동이 중단되어 기존 활동이 새 동작으로 강제 마이그레이션됩니다.

### [!UICONTROL Auto-Allocate]개 활동에 미치는 영향

| 지표 이름 | 다음에서 더 이상 지원되지 않음: |
| --- | --- |
| [!UICONTROL averagepagedepth] | 전환율, 지표 값 최대화 |
| [!UICONTROL averagetimespentonsite] | 전환율, 지표 값 최대화 |
| [!UICONTROL bouncerate] | 전환율, 지표 값 최대화 |
| [!UICONTROL bounces] | 전환율, 지표 값 최대화 |
| [!UICONTROL entries] | 전환율, 지표 값 최대화 |
| [!UICONTROL exits] | 전환율, 지표 값 최대화 |
| [!UICONTROL pageviews] | 지표 값 최대화 |
| [!UICONTROL reloads] | 지표 값 최대화 |
| [!UICONTROL visitors] | 전환율, 지표 값 최대화 |
| [!UICONTROL visits] | 지표 값 최대화 |

### [!UICONTROL Auto-Target]개 활동에 미치는 영향

| 지표 이름 | 다음에서 더 이상 지원되지 않음: |
| --- | --- |
| [!UICONTROL cartremovals] | 지표 값 최대화 |
| [!UICONTROL pageviews] | 지표 값 최대화 |
| [!UICONTROL visitors] | 전환율, 지표 값 최대화 |
| [!UICONTROL visits] | 지표 값 최대화 |

## 제한 사항 및 참고 사항

일부 제한 사항과 메모는 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동에 모두 적용됩니다. 다른 제한 사항 및 참고는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

### 자동 할당 및 자동 타겟 {#both}

* [!UICONTROL Auto-Allocate] 또는 [!UICONTROL Auto-Target]에 대한 보고 소스로 [!DNL Adobe Analytics]을(를) 사용하는 경우 항상 [!DNL Analytics]에서 보고서를 확인해야 합니다.
* 활동이 활성화된 후에는 보고 소스를 [!DNL Analytics]에서 [!DNL Target]&#x200B;(으)로 또는 그 반대로 변경할 수 없습니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 대신 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도된 결과를 얻을 수 있는 경우가 많습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target]은(는) 트래픽 분포가 균일하지 않은 것을 고려하여 방문 단위로 전환 지표를 자동으로 표준화하므로 표준화를 수행하기 위해 계산된 지표를 사용할 필요는 없습니다.

### 자동 할당 {#aa}

* **교육 빈도**: [!UICONTROL Auto-Allocate] 모델은 평소처럼 매시간 계속 교육합니다.
* **속성 모델**: [!DNL Target]에서는 A4T를 사용하는 [!UICONTROL &#x200B; Auto-Allocate] 활동에 대해 [!DNL Adobe Analytics] 기본 속성 모델을 사용합니다.
* **신뢰도**: [!UICONTROL Auto-Allocate] 활동에 사용되는 신뢰 수식이 [!DNL Adobe Analytics] [!UICONTROL A4T] 패널에 기본적으로 표시되는 수식과 다릅니다. [여기에 설명된 대로](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) [!UICONTROL Auto-Allocate]은(는) 일반 [!UICONTROL A/B Test] 활동보다 더 보수적인 신뢰 구간을 사용합니다. 이러한 보수적 신뢰 수준은 데이터에 대한 반복적인 평가(peeks)를 보상한다. 따라서 [!DNL Adobe Analytics]의 기본 보고서에 [!UICONTROL Auto-Allocate] 알고리즘에서 사용 중인 구간에 비해 더 좁은 신뢰 구간이 표시됩니다. 그럼에도 불구하고, 보내는 더 많은 고유 방문자가 있는 경험을 기반으로 알고리즘에서 선호하는 경험을 결정할 수 있습니다.
* **우승자 상태**: 현재 [!DNL Analysis Workspace]의 [!UICONTROL A4T] 패널에서 [&quot;아직 우승자 없음&quot; 및 &quot;우승자&quot; 배지](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)를 사용할 수 없습니다. 같은 보고서를 [!DNL Target]에서 보는 경우에는 이 배지도 사용할 수 없습니다. A4T를 사용하는 [!UICONTROL Auto-Allocate] 활동에 대한 [!DNL Target] 보고서에 표시된 우승자 &quot;별&quot; 배지는 무시해야 합니다. 이 배지는 [!UICONTROL Auto-Allocate]에서 사용하는 계산이 아니라 일반 신뢰도 계산을 반영합니다.

### 자동 타겟 {#at}

* [!UICONTROL Auto-Target] 모델은 평소처럼 24시간마다 계속 교육합니다. 그러나 [!DNL Analytics]에서 들어오는 전환 이벤트 데이터는 6시간에서 24시간 더 지연됩니다. 이 지연은 [!DNL Target]에 의한 트래픽 분배가 [!DNL Analytics]에 기록된 최신 이벤트를 추적하는 것을 의미합니다. 이러한 지연은 활동이 처음 활성화된 후 처음 48시간에서 가장 큰 영향을 미칩니다. 활동의 성능은 5일이 지난 후 [!DNL Analytics] 전환 동작을 더 가깝게 미러링합니다.

  대부분의 트래픽이 활동 수명 첫 5일 이내에 발생하는 단기 활동에는 [!UICONTROL Auto-Target] 대신 [!UICONTROL Auto-Allocate]을(를) 사용하는 것이 좋습니다.

* [!UICONTROL Auto-Target] 활동에 대한 데이터 소스로 [!DNL Analytics]을(를) 사용하는 경우 6시간이 경과하면 세션이 종료됩니다. 6시간 후에 발생하는 전환은 계산되지 않습니다.

자세한 내용은 *Analytics 도구 안내서*&#x200B;에서 [속성 모델 및 전환 확인 기간](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html)을 참조하십시오.

## 자습서

[!DNL Adobe Analytics] [!UICONTROL Analysis Workspace]에서 다양한 분석 기능을 사용할 수 있지만 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동을 올바르게 해석하려면 기본 [!UICONTROL Analytics for Target] 패널을 몇 가지 수정해야 합니다. 실험 활동(수동 A/B 및 [!UICONTROL Auto-Allocate])과 개인화 활동([!UICONTROL Auto-Target]) 간의 차이로 인해 이러한 수정이 필요합니다.

### [!UICONTROL Auto-Allocate] 활동에 대해 [!DNL Analysis Workspace]에서 A4T 보고서 설정 중

이 튜토리얼에서는 [!DNL Analysis Workspace]의 [!UICONTROL Auto-Allocate] 활동을 분석하기 위한 권장 수정 사항을 안내합니다.

자세한 내용은 *Adobe Target 자습서*&#x200B;에서 [자동 할당 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=ko-KR){target=_blank}을 참조하십시오.

### [!UICONTROL Auto-Target] 활동에 대해 [!DNL Analysis Workspace]에서 A4T 보고서 설정 중

이 튜토리얼에서는 [!DNL Analysis Workspace]의 [!UICONTROL Auto-Target] 활동을 분석하기 위한 권장 수정 사항을 안내합니다.

자세한 내용은 *Adobe Target 자습서*&#x200B;에서 [자동 타겟 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=ko-KR){target=_blank}을 참조하십시오.


