---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe에서 자동 할당 및 자동 Target 활동을 만드는 방법을 알아봅니다 [!DNL Target] 를 보고 소스로 사용(A4T)하는 것과 같습니다.
title: A4T가 자동 할당 및 자동 Target 활동을 지원합니까?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: f203a7298ca0ee2c5f58fe5b0fdb43a13bb9680b
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 2%

---

# 자동 할당 및 자동 타겟 활동에 대한 A4T 지원

다음 [!DNL Adobe Target]-to-[!DNL Adobe Analytics] 통합, 알려진 [Target 분석](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T)에서 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동.

A4T 통합을 사용하면 다음 작업을 수행할 수 있습니다.

* 사용 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)트래픽을 유도하여 우승 경험으로 전환하는 의 다중 무장 bandit 기능입니다.
* 사용 [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md)의 ensemble machine learning 알고리즘을 사용하여 각 방문자에 대해 최상의 경험을 선택할 수 있습니다. 자동 Target은 을 사용하는 동안 사용자의 프로필, 동작 및 컨텍스트를 기반으로 최상의 경험을 선택합니다 [!DNL Adobe Analytics] 목표 지표 및 [!DNL Adobe Analytics]&#39; 풍부한 보고 및 분석 기능.

다음을 확인하십시오. [A/B 테스트 및 경험 타깃팅 활동에 사용하기 위해 A4T를 구현했습니다](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). 사용 중인 경우 `analyticsLogging = client_side`, 도 전달해야 합니다. `sessionId` 값 [!DNL Analytics]. 자세한 내용은 [A4T(Target 분석) 보고](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) 에서 *Adobe Target SDK* 안내서.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 작성하는 동안 **[!UICONTROL 타깃팅]** 페이지에서 다음 옵션 중 하나를 **[!UICONTROL 트래픽 할당 방법]**:

   * [!UICONTROL 최고 경험에 자동 할당]
   * [!UICONTROL 개인화된 경험에 대한 자동 Target]

   ![트래픽 할당 방법 옵션: 수동, 자동 할당 및 자동 Target](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   자세한 내용 및 단계별 지침은 [자동 할당 활동 만들기](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 Target 활동 만들기](/help/c-activities/auto-target/create-auto-target.md).

1. 선택 **[!UICONTROL Adobe Analytics]** 에 대해 **[!UICONTROL 보고 소스]** on **[!UICONTROL 목표 및 설정]** 페이지를 열고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.

   ![목표 및 설정 페이지의 보고 소스 섹션](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. 기본 목표 지표를 선택합니다.

   * 를 사용하려면 [!DNL Adobe Target] 최적화 목표를 지정하려면 **[!UICONTROL 전환]** .
   * 선택 **[!UICONTROL Analytics 지표 사용]** 그런 다음 지표 [!DNL Analytics] 을 최적화 목표로 사용할 수 있습니다. 즉시 사용 가능한 [!DNL Analytics] 전환 지표 또는 [!DNL Analytics] 사용자 지정 이벤트.

   자세한 내용은 [지원되는 목표 지표](#supported) 아래 정보를 참조하십시오.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동 할당] 선택한 지표를 사용하여 활동을 최적화하고 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL 자동 Target] 선택한 지표를 사용하여 활동을 최적화하고 방문자를 개인화된 최상의 경험으로 유도합니다.

1. 를 사용하십시오 **[!UICONTROL 보고서]** 탭하여 선택 사항별로 활동의 보고를 볼 수 있습니다. [!DNL Adobe Analytics] 지표 를 참조하십시오. 클릭 **[!UICONTROL Analytics에서 보기]** 보고 데이터를 심층적으로 세분화하기 위해

## 지원되는 목표 지표 {#supported}

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 을 사용하면 최적화를 위한 기본 목표 지표로 다음 지표 유형을 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 을 사용하려면 이진 이벤트를 기반으로 하는 지표를 선택해야 합니다. 이항 이벤트는 발생하지 않거나 발생하지 않습니다. 이항 이벤트에는 클릭, 전환, 주문 등이 포함됩니다. 이러한 유형의 이벤트는 경우에 따라 베르누이, 이진 또는 개별 이벤트라고도 합니다.

[!UICONTROL A4T] 대상 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 은 연속 지표에 대한 최적화를 지원하지 않습니다. 연속 지표에는 매출, 주문한 제품 수, 세션 기간, 세션 중의 페이지 보기 수 등이 포함됩니다. 이러한 지원되지 않는 유형의 지표는 비바인더 또는 비베른울리 지표라고도 합니다.

다음 지표 유형은 기본 목표 지표로 지원되지 않습니다.

* [!DNL Adobe Target] 참여 및 매출 지표
* [!DNL Adobe Analytics] 참여 및 매출 지표

   을(를) 선택할 수 있습니다 [!DNL Analytics] 참여 또는 매출 지표를 기본 목표 지표로 사용하는 이유 [!DNL Target] 모든 참여 및 매출 지표를 [!DNL Analytics]. 에서 이진 전환 지표나 사용자 지정 이벤트만 선택합니다 [!DNL Analytics].

* [!DNL Adobe Analytics] 계산된 지표

## 제한과 참고 사항

몇 가지 제한 사항과 참고는 두 가지 모두에 적용됩니다 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동. 다른 제한 사항 및 참고는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

### 자동 할당 및 자동 Target {#both}

* 사용 시 [!DNL Adobe Analytics] 를 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target]에서는 항상 보고서를 [!DNL Analytics].
* 보고 소스를 [!DNL Analytics] to [!DNL Target] 또는 반대로 활동이 활성화되면 무시됩니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도한 결과를 달성하는 것이 종종 가능합니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면, &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 불규칙한 트래픽 분포를 설명하기 위해 방문당 전환 지표를 자동으로 표준화하므로 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.
* 사용 시 [!DNL Adobe Analytics] 를 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target] 활동은 항상 [!DNL Analytics].
* 보고 소스를 [!DNL Analytics] to [!DNL Target] 활동이 활성화되면 그 반대로 할 수 있습니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 사용자 지정 이벤트를 기본 목표 지표로 선택하여 의도한 결과를 달성하는 것이 종종 가능합니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면, &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 에 대해 방문자별로 전환 지표를 자동으로 정규화합니다. [!UICONTROL 자동 할당] 활동. 따라서 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.

### 자동 할당 {#aa}

* **교육 빈도**: [!UICONTROL 자동 할당] 모델들은 평상시처럼 매시간 훈련한다.
* **속성 모델**: [!DNL Target] 사용 [!DNL Adobe Analytics] 기본 속성 모델[!UICONTROL  자동 할당] A4T를 사용하는 활동.
* **신뢰도**: 에 사용되는 신뢰도 공식입니다 [!UICONTROL 자동 할당] 활동은 기본적으로 [!DNL Adobe Analytics] [!UICONTROL A4T] 패널. [여기에 설명된 대로](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL 자동 할당] 일반보다 더 많은 보수적 신뢰 구간을 사용합니다 [!UICONTROL A/B 테스트] 활동. 이러한 보수적 신뢰 수준은 데이터에 대한 반복적인 평가(매)를 보완합니다. 따라서 의 기본 보고서는 [!DNL Adobe Analytics] 에 사용되는 간격과 비교하여 더 좁은 신뢰 구간을 표시합니다 [!UICONTROL 자동 할당] 알고리즘에 대해 설명합니다. 하지만 고유 방문자가 더 많은 경험을 기반으로 알고리즘에서 선호되는 경험을 결정할 수 있습니다.
* **우승자 상태**: 현재, [&quot;아직 우승자 없음&quot; 및 &quot;우승자&quot; 배지](/help/c-activities/automated-traffic-allocation/determine-winner.md) 에서 사용할 수 없음 [!UICONTROL A4T] 패널 [!DNL Analysis Workspace]. 이러한 배지는 같은 보고서를 [!DNL Target]. 에 표시되는 승자 &quot;별&quot; 배지 [!DNL Target] 보고서 [!UICONTROL 자동 할당] A4T를 사용하는 활동은 무시해야 합니다. 이 배지는 일반적인 신뢰 계산을 반영하며 [!UICONTROL 자동 할당].

### 자동 타겟 {#at}

* [!UICONTROL 자동 Target] 모델들은 평소대로 24시간 간격으로 훈련을 계속한다. 그러나 전환 이벤트 데이터는에서 가져옵니다 [!DNL Analytics] 6시간에서 24시간 더 지연됩니다. 이러한 지연은 트래픽 분포를 의미합니다 [!DNL Target] 에 기록된 최신 이벤트의 추적 [!DNL Analytics]. 이 지연은 활동이 처음 활성화된 후 처음 48시간 이내에 가장 큰 영향을 줍니다. 활동의 성과가 더 밀접하게 반영될 것입니다 [!DNL Analytics] 5일이 경과된 후의 전환 동작입니다. 사용 고려 [!UICONTROL 자동 할당] 대신 [!UICONTROL 자동 Target] 활동 수명 후 처음 5일 이내에 대부분의 트래픽이 발생하는 단기 활동입니다.
* 사용 시 [!DNL Analytics] 를 [!UICONTROL 자동 Target] 활동, 세션이 6시간이 경과하면 종료됩니다. 6시간 후 발생하는 전환은 카운트되지 않습니다.

자세한 내용은 [속성 모델 및 전환 확인 기간](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) 에서 *Analytics 툴 안내서*.

## 자습서: 자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법 {#tutorial}

다양한 분석 기능은에서 사용할 수 있지만 [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], 기본값에 대한 몇 가지 수정 사항 [!UICONTROL Target 분석] 자동 Target 활동을 올바르게 해석하려면 패널이 필요합니다. 실험 활동(수동 A/B와 수동 A/B) 간의 차이로 인해 이러한 수정 사항이 필요합니다 [!UICONTROL 자동 할당]) 및 개인화 활동( )[!UICONTROL 자동 Target]).

이 자습서에서는 분석을 위한 권장 수정 사항을 안내합니다 [!UICONTROL 자동 Target] 활동 [!UICONTROL 작업 공간].

자세한 내용은 [자동 Target 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
