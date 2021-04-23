---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Analytics를 보고 소스(A4T)로 사용하는 Adobe [!DNL Target] 에서 자동 할당 및 자동 Target 활동을 만드는 방법을 알아봅니다.
title: A4T는 자동 할당 및 자동 Target 활동을 지원합니까?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 2%

---

# 자동 할당 및 자동 Target 활동에 대한 A4T 지원

[!DNL Adobe Target]-to-[!DNL Adobe Analytics] 통합(Target](/help/c-integrating-target-with-mac/a4t/a4t.md)(A4T)에 대한 분석)은 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동을 지원합니다.[

A4T 통합을 사용하여 다음을 수행할 수 있습니다.

* [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)의 다중 무장 강도적 기능을 사용하여 트래픽을 획득 경험으로 유도합니다.
* [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md)의 앙상블 머신 러닝 알고리즘을 사용하여 각 방문자에게 가장 적합한 경험을 선택하십시오. 자동 Target은 [!DNL Adobe Analytics] 목표 지표 및 [!DNL Adobe Analytics]&#39;의 풍부한 보고 및 분석 기능을 사용하는 동안 사용자의 프로필, 행동 및 컨텍스트를 기반으로 최상의 경험을 선택합니다.

A/B 테스트 및 경험 타깃팅 활동](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)에 사용할 수 있도록 [구현된 A4T가 있는지 확인합니다. `analyticsLogging = client_side`을(를) 사용하는 경우 `sessionId` 값도 [!DNL Analytics]에 전달해야 합니다. 자세한 내용은 *Adobe Target SDK* 안내서의 [Target(A4T) 보고](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting)을 참조하십시오.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 만드는 동안 **[!UICONTROL 타깃팅]** 페이지에서 **[!UICONTROL 트래픽 할당 방법]** 중 하나를 선택합니다.

   * [!UICONTROL 최적의 경험에 자동 할당]
   * [!UICONTROL 개인화된 경험을 위한 자동 Target]

   ![트래픽 할당 방법 옵션:수동, 자동 할당 및 자동 Target](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   자세한 내용 및 단계별 지침은 [자동 할당 활동 만들기](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 Target 활동 만들기](/help/c-activities/auto-target/create-auto-target.md)를 참조하십시오.

1. **[!UICONTROL 목표 및 설정]** 페이지에서 **[!UICONTROL 보고 소스]**&#x200B;에 대해 **[!UICONTROL Adobe Analytics]**&#x200B;을 선택하고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.

   ![목표 및 설정 페이지의 보고 소스 섹션](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. 기본 목표 지표를 선택합니다.

   * [!DNL Adobe Target]을(를) 사용하여 최적화 목표를 지정하려면 **[!UICONTROL 전환]**&#x200B;을 선택합니다.
   * **[!UICONTROL Analytics 지표 사용]**&#x200B;을 선택한 다음 최적화 목표로 사용할 [!DNL Analytics]의 지표를 선택합니다. 기본적으로 [!DNL Analytics] 전환 지표나 [!DNL Analytics] 사용자 지정 이벤트를 사용할 수 있습니다.

   자세한 내용은 아래 [지원되는 목표 지표](#supported)를 참조하십시오.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동 ] 할당에서는 선택한 지표를 사용하여 활동을 최적화하여 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL 자동 ] 타깃팅은 선택한 지표를 사용하여 활동을 최적화하여 방문자를 개인화된 최상의 경험으로 유도합니다.

1. [!DNL Adobe Analytics] 지표 선택에 따라 **[!UICONTROL 보고서]** 탭을 사용하여 활동의 보고를 봅니다. 보고 데이터를 심층적이고 자세히 세그먼트화하려면 **[!UICONTROL Analytics]**&#x200B;에서 보기를 클릭합니다.

## 지원되는 목표 지표 {#supported}

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetlet에서는 다음 지표 유형을 최적화를 위한 기본 목표 지표로 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-] Targetting을 사용하려면 이진 이벤트를 기반으로 하는 지표를선택해야 합니다. 이진 이벤트는 발생하지 않거나 발생하지 않습니다. 결합 이벤트에는 클릭, 전환, 주문 등이 포함됩니다. 이러한 유형의 이벤트를 베르누이, 이진 또는 개별 이벤트라고도 합니다.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocation 및  [!UICONTROL Auto-Targetting은 연속 지표에 대한 최적화] 를 지원하지 않습니다. 지속적인 지표에는 매출, 주문한 제품 수, 세션 기간, 세션 내 페이지 보기 횟수 등이 포함됩니다. 지원되지 않는 이러한 유형의 지표는 비결합 지표라고도 하며 그렇지 않은 지표라고도 합니다.

다음 지표 유형은 기본 목표 지표로 지원되지 않습니다.

* [!DNL Adobe Target] 참여 및 매출 지표
* [!DNL Adobe Analytics] 참여 및 매출 지표

   [!DNL Target]은(는) [!DNL Analytics]에서 모든 참여 및 매출 지표를 식별하고 제외할 수 없으므로 [!DNL Analytics] 참여 또는 매출 지표를 기본 목표 지표로 선택할 수 있습니다. [!DNL Analytics]에서 이진 전환 지표나 사용자 지정 이벤트만 선택합니다.

* [!DNL Adobe Analytics] 계산된 지표

## 제한 사항 및 메모

일부 제한 사항과 메모는 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동 모두에 적용됩니다. 다른 제한 사항과 메모는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

### 자동 할당 및 자동 Target

* 활동이 활성화된 후에는 보고 소스를 [!DNL Analytics]에서 [!DNL Target](으)로 변경할 수 없습니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만 사용자 지정 이벤트를 기본 목표 지표로 선택하는 대신 원하는 결과를 얻을 수 있는 경우가 많습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 방문당 전환 지표를 자동으로 정규화하여 불규칙한 트래픽 배포를 고려하므로 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.
* [!DNL Target] 자동 할당 기능에서 &quot;동일한 터치&quot; 속성  [!UICONTROL 모델을 ] 사용합니다.Target(A4T)에 대한 분석.

### 자동 할당

* [!UICONTROL 자동 ] Allocatemodels는 평소대로 2시간마다 트레이닝을 받습니다.

### 자동 타겟

* [!UICONTROL 자동차 ] 타게트모델은 평소대로 24시간마다 계속해서 훈련합니다. 그러나 [!DNL Analytics]에서 오는 전환 이벤트 데이터는 추가 6-24시간 지연됩니다. 이러한 지연은 [!DNL Target]에 의한 트래픽 분배가 [!DNL Analytics]에 기록된 최신 이벤트의 추적을 의미합니다. 이러한 지연은 활동이 처음 활성화된 후 처음 48시간 이내에 가장 큰 영향을 줍니다. 5일이 경과된 후 활동의 성능이 [!DNL Analytics] 전환 동작을 보다 면밀하게 반영합니다. 활동 수명 후 처음 5일 이내에 대부분의 트래픽이 발생하는 단기 활동에 대해 [!UICONTROL 자동 Target] 대신 [!UICONTROL 자동 할당]을 사용하는 것이 좋습니다.
* [!UICONTROL 자동 Target] 활동의 데이터 소스로 [!DNL Analytics]을(를) 사용할 때 6시간이 경과하면 세션이 종료됩니다. 6시간 후 발생하는 전환은 계산되지 않습니다.

자세한 내용은 *분석 도구 안내서*&#x200B;에서 [속성 모델 및 전환 창](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html)을 참조하십시오.

## 자습서:자동 Target 활동에 대해 Analysis Workspace에서 A4T 보고서를 설정하는 방법 {#tutorial}

풍부한 분석 기능은 [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace]에서 사용할 수 있지만, 자동 Target 활동을 올바로 해석하려면 기본 [!UICONTROL Target] 패널에 대한 분석을 몇 가지 수정해야 합니다. 이러한 수정은 실험 활동(수동 A/B와 [!UICONTROL 자동 할당])과 개인화 활동([!UICONTROL 자동 Target])의 차이로 인해 필요합니다.

이 자습서에서는 [!UICONTROL 작업 공간]에서 [!UICONTROL 자동 Target] 활동을 분석하기 위한 권장 수정 사항을 안내합니다.

자세한 내용은 *Adobe Target Tutorials*&#x200B;의 자동 Target 활동에 대해 Analysis Workspace에서 A4T 보고서를 설정하는 방법을 참조하십시오](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html).[
