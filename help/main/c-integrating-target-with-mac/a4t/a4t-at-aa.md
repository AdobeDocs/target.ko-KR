---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe에서 자동 할당 및 자동 Target 활동을 만드는 방법을 알아봅니다 [!DNL Target] analytics를 보고 소스로 사용(A4T)
title: A4T가 자동 할당 및 자동 Target 활동을 지원합니까?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 2%

---

# 자동 할당 및 자동 타겟 활동에 대한 A4T 지원

다음 [!DNL Adobe Target]-에서-[!DNL Adobe Analytics] 통합, 다음으로 알려짐 [Target 분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) 지원 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동.

A4T 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.

* 사용 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)트래픽을 승리 경험으로 유도하는 의 multi-armed bandit 기능입니다.
* 사용 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)각 방문자에게 최상의 경험을 선택하기 위한 의 앙상블 머신 러닝 알고리즘. 자동 Target 은 를 사용하는 동안 사용자의 프로필, 동작 및 컨텍스트를 기반으로 최상의 경험을 선택합니다. [!DNL Adobe Analytics] 목표 지표 및 [!DNL Adobe Analytics]&#39; 풍부한 보고 및 분석 기능.

다음을 수행했는지 확인하십시오. [a/B 테스트 및 경험 타깃팅 활동과 함께 사용할 A4T를 구현했습니다](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). 을 사용하는 경우 `analyticsLogging = client_side`, 또한 을 전달해야 합니다. `sessionId` 값: 까지 [!DNL Analytics]. 자세한 내용은 [A4T(Target 분석) 보고](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} 다음에서 *ADOBE TARGET SDK* 가이드.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 만드는 동안 **[!UICONTROL 타겟팅]** 페이지에서 다음 옵션 중 하나를 로 선택합니다 **[!UICONTROL 트래픽 할당 방법]**:

   * [!UICONTROL 최고 경험에 자동 할당]
   * [!UICONTROL 개인화된 경험에 대한 자동 Target]

   ![트래픽 할당 방법 옵션: 수동, 자동 할당 및 자동 Target](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   자세한 내용 및 단계별 지침은 [자동 할당 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 Target 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md).

1. 선택 **[!UICONTROL Adobe Analytics]** 에 대한 **[!UICONTROL 보고 소스]** 다음에 있음 **[!UICONTROL 목표 및 설정]** 원하는 최적화 목표에 해당하는 보고서 세트를 페이지 지정하고 선택합니다.

   ![목표 및 설정 페이지의 보고 소스 섹션](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. 기본 목표 지표를 선택합니다.

   * 사용 [!DNL Adobe Target] 최적화 목표를 지정하려면 다음을 선택합니다. **[!UICONTROL 전환]** .
   * 선택 **[!UICONTROL Analytics 지표 사용]** 그런 다음 다음에서 지표를 선택합니다. [!DNL Analytics] 을 최적화 목표로 사용합니다. 기본 설정을 사용할 수 있습니다. [!DNL Analytics] 전환 지표 또는 [!DNL Analytics] 사용자 지정 이벤트.

   다음을 참조하십시오 [지원되는 목표 지표](#supported) 자세한 내용은 아래를 참조하십시오.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동 할당] 은 선택한 지표를 사용하여 활동을 최적화함으로써 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL 자동 Target] 은 선택한 지표를 사용하여 활동을 최적화함으로써 방문자를 개인화된 최상의 경험으로 유도합니다.

1. 사용 **[!UICONTROL 보고서]** 탭으로 이동하여 선택한 항목별로 활동의 보고 보기 [!DNL Adobe Analytics] 지표. 클릭 **[!UICONTROL Analytics에서 보기]** 자세히 살펴보고 보고 데이터를 추가로 세그먼트화합니다.

## 지원되는 목표 지표 {#supported}

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 을 사용하면 다음 지표 유형 중 하나를 최적화를 위한 기본 목표 지표로 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 은 이항 이벤트를 기반으로 하는 지표를 선택해야 합니다. 이항 이벤트가 발생하거나 발생하지 않습니다. 이항 이벤트에는 클릭, 전환, 순서 등이 포함됩니다. 이러한 유형의 이벤트는 베르누이, 이진 또는 이산 이벤트라고도 합니다.

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 은 연속 지표에 대한 최적화를 지원하지 않습니다. 연속 지표에는 매출, 주문한 제품 수, 세션 기간, 세션의 페이지 보기 수 등이 포함됩니다. 이러한 지원되지 않는 유형의 지표를 비이항 또는 비베르누이 지표라고도 합니다.

다음 지표 유형은 기본 목표 지표로 지원되지 않습니다.

* [!DNL Adobe Target] 참여 및 매출 지표
* [!DNL Adobe Analytics] 참여 및 매출 지표

   다음을 선택할 수 있습니다. [!DNL Analytics] 다음 이유로 인해 참여 또는 매출 지표를 기본 목표 지표로 사용함 [!DNL Target] 에서 모든 참여 및 매출 지표를 식별하고 제외할 수 없음 [!DNL Analytics]. 다음에서 이항 전환 지표 또는 사용자 지정 이벤트만 선택 [!DNL Analytics].

* [!DNL Adobe Analytics] 계산된 지표

## 제한과 참고 사항

몇 가지 제한 사항과 참고 사항은 두 가지 모두에 적용됩니다 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동. 다른 제한 사항 및 참고는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

### 자동 할당 및 자동 타겟팅 {#both}

* 사용 시 [!DNL Adobe Analytics] 을(를) 위한 보고 소스로 사용 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target], 에서는 항상 보고서를 확인해야 합니다. [!DNL Analytics].
* 보고 소스를에서 변경할 수 없습니다. [!DNL Analytics] 끝 [!DNL Target] 또는 반대로 활동이 활성화된 후입니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 대신 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도된 결과를 얻을 수 있는 경우가 많습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 트래픽 분포가 균일하지 않도록 전환 지표를 방문별로 자동으로 표준화하므로 계산된 지표를 사용하여 표준화를 수행할 필요는 없습니다.
* 사용 시 [!DNL Adobe Analytics] 을(를) 위한 보고 소스로 사용 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target] 활동, 항상 다음 위치에서 보고서를 확인해야 함: [!DNL Analytics].
* 보고 소스를에서 변경할 수 없습니다. [!DNL Analytics] 끝 [!DNL Target] 또는 활동이 활성화된 후 그 반대의 경우도 가능합니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 대신 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도된 결과를 얻을 수 있는 경우가 많습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 에 대해 방문자별로 전환 지표를 자동으로 표준화합니다. [!UICONTROL 자동 할당] 활동을 활성화하므로 계산된 지표를 사용하여 표준화를 수행할 필요는 없습니다.

### 자동 할당 {#aa}

* **교육 빈도**: [!UICONTROL 자동 할당] 모델들은 평소처럼 매시간 계속해서 훈련을 합니다.
* **속성 모델**: [!DNL Target] 를 사용합니다. [!DNL Adobe Analytics] 에 대한 기본 속성 모델[!UICONTROL  자동 할당] a4T를 사용하는 활동.
* **신뢰도**: 다음에서 사용하는 신뢰도 공식 [!UICONTROL 자동 할당] 활동은 다음에 기본적으로 표시되는 수식과 다릅니다. [!DNL Adobe Analytics] [!UICONTROL A4T] 패널. [여기에 설명된대로](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL 자동 할당] 보통보다 더 보수적인 신뢰 구간을 사용합니다. [!UICONTROL A/B 테스트] 활동. 이러한 보수적 신뢰 수준은 데이터에 대한 반복적인 평가(peeks)를 보상한다. 따라서 의 기본 보고서가 [!DNL Adobe Analytics] 에서 사용 중인 신뢰 구간에 비해 좁은 신뢰 구간을 표시합니다. [!UICONTROL 자동 할당] 알고리즘. 그럼에도 불구하고, 보내는 더 많은 고유 방문자가 있는 경험을 기반으로 알고리즘에서 선호하는 경험을 결정할 수 있습니다.
* **우승자 상태**: 현재 [&quot;아직 우승자 없음&quot; 및 &quot;우승자&quot; 배지](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) 은(는) 다음에서 사용할 수 없습니다. [!UICONTROL A4T] 패널 위치 [!DNL Analysis Workspace]. 동일한 보고서를에서 보는 경우에는 이러한 배지도 사용할 수 없습니다 [!DNL Target]. 에 표시된 우승자 &quot;별&quot; 배지 [!DNL Target] 다음에 대한 보고서 [!UICONTROL 자동 할당] A4T를 사용하는 활동은 무시해야 합니다. 이 배지는 일반 신뢰도 계산을 반영하며 다음에 의해 사용되는 것을 반영하지 않습니다. [!UICONTROL 자동 할당].

### 자동 타겟 {#at}

* [!UICONTROL 자동 Target] 모델들은 평소처럼 24시간 간격으로 계속 훈련합니다. 하지만 전환 이벤트 데이터는에서 가져옵니다. [!DNL Analytics] 6시간에서 24시간 더 지연됩니다. 이 지연은 다음 기준에 따른 트래픽 분포를 의미합니다. [!DNL Target] 에 기록된 최신 이벤트를 추적합니다 [!DNL Analytics]. 이러한 지연은 활동이 처음 활성화된 후 처음 48시간에서 가장 큰 영향을 미칩니다. 활동의 성과는 더욱 면밀하게 반영됩니다 [!DNL Analytics] 5일이 경과한 후 전환 동작이 수행됩니다. 사용 고려 [!UICONTROL 자동 할당] 대신 [!UICONTROL 자동 Target] 대부분의 트래픽이 활동 수명 첫 5일 이내에 발생하는 짧은 기간 활동의 경우.
* 사용 시 [!DNL Analytics] 를 위한 데이터 소스로 [!UICONTROL 자동 Target] 활동, 세션은 6시간이 경과하면 종료됩니다. 6시간 후에 발생하는 전환은 계산되지 않습니다.

자세한 내용은 [속성 모델 및 전환 확인 기간](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) 다음에서 *Analytics 툴 안내서*.

## 자습서: 자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법 {#tutorial}

다양한 분석 기능은에서 사용할 수 있습니다 [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], 기본값에 대한 몇 가지 수정 사항 [!UICONTROL Target 분석] 패널은 자동 Target 활동을 올바르게 해석하는 데 필요합니다. 실험 활동(수동 A/B 및 [!UICONTROL 자동 할당]) 및 개인화 활동([!UICONTROL 자동 Target]).

이 자습서에서는 분석을 위한 권장 수정 사항을 안내합니다 [!UICONTROL 자동 Target] 의 활동 [!UICONTROL 작업 영역].

자세한 내용은 [자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) 위치: *Adobe Target Tutorials*.
