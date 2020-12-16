---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.
title: A4T를 보고 소스로 사용하는 활동 만들기
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 17%

---


# Analytics를 보고 소스로 사용하는 활동 만들기

[!DNL Target]에서 [!DNL Adobe Analytics]을 보고 소스(A4T)로 사용하도록 활동을 구성할 수 있습니다.

보고 소스로 [!DNL Analytics]을(를) 사용하는 활동을 설정하기 전에 방문자당 매출 향상(RPV) 또는 장바구니 클릭 수 증가 등 활동의 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. [!DNL Analytics]에서 언제든지 추가 지표를 선택할 수 있지만, 이 테스트에 영향을 줄 특정 지표를 지정해야 합니다.

## 활동을 만듭니다

보고 소스로 [!DNL Analytics]을 사용하는 [!DNL Target] 활동을 만드는 것은 몇 가지 중요한 차이점과 함께 일반 [!DNL Target] 활동 설정과 비슷합니다. 예를 들어 활동을 만드는 동안 보고용 세그먼트를 선택할 수 없습니다. 보고서를 볼 때 [!DNL Analytics]에서 사용할 수 있는 모든 세그먼트를 적용할 수 있기 때문입니다.

1. **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Analytics]이(가) 보고 소스로 사용되는 경우 활동 이름은 &quot;%&quot; 문자를 포함할 수 없습니다.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.
1. 활동 만들기 흐름의 **[!UICONTROL 설정]** 부분으로 이동되면 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택하고 회사를 지정합니다.
1. 보고서 세트를 선택합니다.

   [!DNL Analytics]에서 사용할 수 있는 모든 보고서 세트를 선택할 수 있습니다. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 규정합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.

      [!DNL Analytics] 회사를 확인해야 할 수도 있습니다. [!DNL Adobe Experience Cloud] 계정이 둘 이상의 [!DNL Analytics] 회사에 연결되어 있으면 [!DNL Target]에서 로그아웃하고 올바른 회사 아래의 [!DNL Analytics]에 로그인합니다. 그런 다음 [!DNL Target]으로 돌아오면 보고서 세트가 로드됩니다.

   * 예상한 보고서 세트가 표시되지 않습니다.

      [!DNL Target]에 연결하도록 제공된 보고서 세트만 선택할 수 있습니다. 원하는 보고서 세트가 표시되지 않는 경우에는 먼저 [!DNL Adobe Experience Cloud]에서 로그아웃했다가 다시 로그인하여 다시 시도하십시오.
   보고서 세트가 목록에 아직 없는 경우에는 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다.
1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. [!DNL Analytics] 지표 선택기에서 사용할 수 있는 [!DNL Analytics] 지표를 선택할 수 있습니다.

   >[!NOTE]
   >
   >[!DNL Analytics] 데이터에만 의존하지 않고 사용자 지정 Target 기반 지표를 [!DNL Analytics]에 보낼 수 있습니다. 예를 들어, 일반적으로 [!DNL Analytics]에 의해 추적되지 않는 페이지 클릭을 모니터링할 수 있습니다. 이 사용자 지정 지표는 [!DNL Target] 서버에서 자동으로 [!DNL Analytics]으로 전송되고 [!DNL Analytics]의 지표 선택기에 &quot;[!DNL Target] 전환&quot; 지표로 나타납니다. [!DNL Analytics] 지표를 사용하도록 선택하면 [!DNL Target] 전환 지표가 비어 있습니다.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 콘텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >[!DNL Analytics]을(를) 보고 소스로 설정한 후 활동을 설정할 때 보고 대상을 설정하는 옵션이 없습니다. [!DNL Analytics] 세그먼트는  [!DNL Target] 활동 보고서에서 사용할 수 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 자동 할당 및 자동 Target 활동에 대한 Target(A4T) 지원 분석 {#a4t-aa}

Target](/help/c-integrating-target-with-mac/a4t/a4t.md)에 대한 [Analytics로 알려진 Adobe Target-Adobe Analytics 통합을 업그레이드했습니다. 자동 할당 및 자동 Target 활동은 이제 Target에 대한 분석을 지원합니다.

이 통합을 통해 다음 작업을 수행할 수 있습니다.

* [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)의 여러 무장 강도적 기능을 사용하여 트래픽을 유도하여 성공적인 경험을 제공할 수 있습니다.
* [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md)의 앙상블 머신 러닝 알고리즘을 사용하여 [!DNL Adobe Analytics] 목표 지표 및 [!DNL Adobe Analytics]&#39;의 풍부한 보고 및 분석 기능을 사용하는 동안 프로필, 행동 및 컨텍스트를 기반으로 각 방문자에 대해 최상의 경험을 선택하십시오.

A/B 테스트 및 경험 타깃팅 활동](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)에 사용할 수 있도록 [구현된 A4T가 있는지 확인합니다. `analyticsLogging = client_side`을(를) 사용하는 경우 `sessionId` 값을 [!DNL Analytics]에 전달해야 합니다. 자세한 내용은 *Adobe Target SDK* 안내서의 [Target(A4T) 보고](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting)을 참조하십시오.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 만드는 동안 **[!UICONTROL 타깃팅]** 페이지에서 **[!UICONTROL 트래픽 할당 방법]** 중 하나를 선택합니다.

   * 최적의 경험에 자동 할당
   * 개인화된 경험을 위한 자동 타깃팅

1. **[!UICONTROL 목표 및 설정]** 페이지에서 **[!UICONTROL 보고 소스]**&#x200B;에 대해 **[!UICONTROL Adobe Analytics]**&#x200B;을 선택하고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.

1. 기본 목표 지표를 선택합니다.

   * [!DNL Adobe Target]을(를) 사용하여 최적화 목표를 지정하려면 **[!UICONTROL 전환]**&#x200B;을 선택합니다.
   * **[!UICONTROL 분석 지표 사용]**&#x200B;을 선택한 다음 최적화 목표로 사용할 [!DNL Analytics]의 지표를 선택합니다. 기본적으로 [!DNL Analytics] 전환 지표나 [!DNL Analytics] 사용자 지정 이벤트를 사용할 수 있습니다.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동 ] 할당에서는 선택한 지표를 사용하여 활동을 최적화하여 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

   또는

   [!UICONTROL 자동 ] 타깃팅은 선택한 지표를 사용하여 활동을 최적화하고 방문자를 개인화된 최상의 경험으로 유도합니다.

1. [!DNL Adobe Analytics] 지표 선택에 따라 **[!UICONTROL 보고서]** 탭을 사용하여 활동의 보고를 봅니다. 보고 데이터를 심층적이고 자세히 세그먼트화하려면 **[!UICONTROL Analytics]**&#x200B;에서 보기를 클릭합니다.

### 지원되는 목표 지표

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocateand  [!UICONTROL Auto-Targetcan] 은 최적화를 위한 기본 목표 지표로 다음 지표 유형을 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

[!UICONTROL A4] Tfor   자동 할당 및  [!UICONTROL 자동 타깃팅에 대해] 는 이진 이벤트(예: 클릭, 전환, 주문 등)를 기반으로 하거나 일어나지 않는 이벤트)를 기반으로 하는 지표를 선택해야 합니다. 이러한 유형의 이벤트를 베르누이, 이진 또는 개별 이벤트라고도 합니다.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allocation 및   Auto-Targetting은 매출, 주문된 제품 수, 세션 기간, 세션 내 페이지 뷰 수 등과 같은 연속 지표에 대한 최적화를 지원하지 않습니다. (지원되지 않는 이러한 유형의 지표는 비결합 지표라고도 하며 그렇지 않은 지표라고도 합니다.)

다음 지표 유형은 기본 목표 지표로 지원되지 않습니다.

* [!DNL Adobe Target] 참여 및 매출 지표
* [!DNL Adobe Analytics] 참여 및 매출 지표

   [!DNL Target]은(는) [!DNL Analytics]에서 모든 참여 및 매출 지표를 식별하고 제외할 수 없으므로 [!DNL Analytics] 참여 또는 매출 지표를 기본 목표 지표로 선택할 수 있습니다. [!DNL Analytics]에서 이진 전환 지표나 사용자 지정 이벤트만 선택하도록 주의하십시오.

* [!DNL Adobe Analytics] 계산된 지표

### 제한 사항 및 메모

일부 제한 사항과 메모는 자동 할당 및 자동 Target 모두에 적용됩니다. 다른 제한 사항과 메모는 한 활동 유형 또는 다른 활동 유형에 적용됩니다.

#### 자동 할당 및 자동 Target

* 활동이 활성화된 후에는 보고 소스를 [!DNL Analytics]에서 [!DNL Target](으)로 또는 그 반대로 변경할 수 없습니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만 사용자 지정 이벤트를 기본 목표 지표로 선택하는 대신 원하는 결과를 얻을 수 있는 경우가 많습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려면 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 방문당 전환 지표를 자동으로 정규화하여 불규칙한 트래픽 배포를 고려하므로 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.
* [!DNL Target] Auto-AllocateA4T 구현에서 &quot;동일한 터치&quot;  [!UICONTROL 속성 ] 모델을 사용합니다.

#### 자동 할당

* [!UICONTROL 자동 ] Allocatemodels는 평소대로 2시간마다 트레이닝을 받습니다.

#### 자동 타겟

* [!UICONTROL 자동차 ] 타게트모델은 평소대로 24시간마다 계속해서 훈련합니다. 그러나 [!DNL Analytics]에서 오는 전환 이벤트 데이터는 6-24시간 추가 지연이 발생합니다. 이러한 지연은 [!DNL Target]에 의한 트래픽 분배가 [!DNL Analytics]에 기록된 최신 이벤트를 추적합니다. 활동이 처음 활성화된 후 처음 48시간 이내에 가장 큰 효과를 가져옵니다.5일이 경과된 후 활동의 성능은 [!DNL Analytics] 전환 동작을 보다 자세히 반영합니다. 대부분의 트래픽이 활동 수명 후 처음 5일 이내에 발생하는 단기 활동에 대해 [!UICONTROL 자동 Target] 대신 [!UICONTROL 자동 할당]을 사용하는 것이 좋습니다.
* [!DNL Analytics]자동 Target] 활동에 대한 데이터 소스로 &lt;a0/>을(를) 사용하는 경우 6시간이 경과하면 세션이 종료된 것으로 간주됩니다. [!UICONTROL  6시간 후에 발생하는 전환은 카운트되지 않습니다.

자세한 내용은 *분석 도구 안내서*&#x200B;에서 [속성 모델 및 전환 창](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html)을 참조하십시오.
