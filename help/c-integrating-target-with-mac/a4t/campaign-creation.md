---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.
title: 활동 만들기
feature: a4t general
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 21%

---


# 활동 만들기{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. 활동의 최종 성공 지표를 선택합니다. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

## Analytics를 보고 소스로 사용하는 활동 만들기

Creating a [!DNL Target] activity that uses [!DNL Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in [!DNL Analytics] can be applied when viewing a report.

1. **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >An activity name cannot include the &quot;%&quot; character if [!DNL Analytics] is used as the reporting source.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.
1. 활동 만들기 흐름의 **[!UICONTROL 설정]** 부분으로 이동되면 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택하고 회사를 지정합니다.
1. 보고서 세트를 선택합니다.

   You can choose any report suite that is available to you in [!DNL Analytics]. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 규정합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.

      You might need to check your [!DNL Analytics] company. If your [!DNL Adobe Experience Cloud] account is tied to more than one [!DNL Analytics] company, log out of [!DNL Target], and log in to [!DNL Analytics] under the right company. Then return to [!DNL Target], and the report suites will load.

   * 예상한 보고서 세트가 표시되지 않습니다.

      Only report suites that are provisioned to connect to [!DNL Target] will be available for selection. If you don&#39;t see the report suite(s) you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again.
   If the report suite(s) is still missing from the list, please [contact Customer Care](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다.
1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. For example, you can monitor clicking on a page, which is usually not tracked by [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the &quot;[!DNL Target] Conversion&quot; metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 콘텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] 세그먼트는 활동 보고서에서 사용할 수 [!DNL Target] 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 자동 할당 활동에 대한 Target(A4T) 지원 분석 {#a4t-aa}

Target용 [분석으로 알려진 Adobe Target과 Adobe Analytics 간의 통합을 업그레이드했습니다](/help/c-integrating-target-with-mac/a4t/a4t.md).

[!UICONTROL 이제 자동 할당] 활동이 Target에 [!UICONTROL 대한 분석을 지원합니다]. 이 통합을 사용하면 목표 지표 및/또는 보고 및 분석 기능을 사용하는 동안 자동 할당의 다중 무장 강도 기능을 사용하여 트래픽을 추첨 경험으로 유도할 수 [!DNL Adobe Analytics] [!DNL Adobe Analytics] 있습니다. A/B 테스트 및 경험 타깃팅 활동 [](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)에 사용할 수 있도록 A4T를 이미 구현한 경우 이제 시작할 준비가 되었습니다.

시작하려면 다음 단계를 따르십시오. 

1. A/B 테스트 활동을 만들고 타깃팅 **** 페이지에서 트래픽 할당 방법 **[!UICONTROL 으로 최적의 경험에]** 자동 할당을 [!UICONTROL 선택합니다] .
1. 목표 및 설정 **[!UICONTROL 페이지]** 에서 **[!UICONTROL 보고 소스]** 에 대한 **[!UICONTROL Adobe Analytics을]** 선택하고 원하는 최적화 목표에 해당하는 보고서 세트를 선택합니다.
1. 기본 목표 지표를 선택합니다.

   최적화 **[!UICONTROL 목표를]** 지정하는 데 사용할 [!DNL Adobe Target] 전환을 선택합니다.

   또는

   Analytics 지표 **** 사용을 선택한 다음 최적화 목표로 사용할 지표 [!DNL Analytics] 를 선택합니다. 즉시 사용 가능한 전환 [!DNL Analytics] 지표나 사용자 지정 이벤트를 사용할 수 [!DNL Analytics] 있습니다.

1. 활동을 저장하고 활성화합니다.

   [!UICONTROL 자동] 할당에서는 선택한 지표를 사용하여 활동을 최적화하여 방문자를 목표 지표를 최대화하는 경험으로 유도합니다.

1. 보고서 **[!UICONTROL 탭을]** 사용하여 선택한 지표에 따라 활동 보고를 [!DNL Adobe Analytics] 봅니다. Analytics **[!UICONTROL 에서]** 보기를 클릭하여 보고 데이터를 심층 분류합니다.

### 지원되는 목표 지표

자동 할당에 대한 A4T [!UICONTROL 를] 사용하면 최적화를 위한 기본 목표 지표로 다음 지표 유형을 선택할 수 있습니다.

* [!DNL Adobe Target] 전환 지표
* [!DNL Adobe Analytics] 전환 지표
* [!DNL Adobe Analytics]사용자 지정 이벤트 개

자동 [!UICONTROL 할당에 대한] A4T를 사용하려면 이진 이벤트, 즉 클릭, 전환, 주문 등과 같이 발생하거나 일어나지 않는 이벤트 등을 기반으로 하는 지표를 선택해야 합니다. 이러한 유형의 이벤트를 베르누이, 이진 또는 개별 이벤트라고도 합니다.

A4T for [!UICONTROL Auto-Allocate] 는 매출, 주문한 제품 수, 세션 기간, 세션 내 페이지 보기 횟수 등과 같은 연속 지표에 대한 최적화를 지원하지 않습니다. 지원되지 않는 이러한 유형의 지표는 비결합 또는 비베른리 지표라고도 합니다.

다음 지표 유형은 기본 목표 지표로 지원되지 않습니다.

* [!DNL Adobe Target] 참여 및 매출 지표
* [!DNL Adobe Analytics] 참여 및 매출 지표

   >[!NOTE]
   >
   >참여 및 매출 지표를 기본 목표 지표로 선택할 수 있을 수 있습니다. 이 지표는 모든 참여 및 매출 지표를 식별할 [!DNL Analytics] 수 없기 때문입니다 [!DNL Target] [!DNL Analytics]. 상호 작용 지표나 사용자 지정 이벤트만 선택하려면 주의하십시오 [!DNL Analytics].

* Adobe Analytics 계산된 지표

### 제한 사항 및 메모

* 활동이 활성화된 후에는 보고 소스 [!DNL Analytics] 를 (으)로 [!DNL Target] 또는 그 반대로 변경할 수 없습니다.
* 계산된 지표는 기본 목표 지표로 지원되지 않지만, 사용자 지정 이벤트를 기본 목표 지표로 선택함으로써 의도한 결과를 얻을 수 있습니다. 예를 들어 &quot;방문자당 양식 완료&quot;와 같은 지표에 대해 최적화하려는 경우 &quot;양식 완료&quot;에 해당하는 사용자 지정 이벤트를 기본 목표 지표로 선택합니다. [!DNL Target] 균일하지 않은 트래픽 분포를 고려하여 방문별로 전환 지표를 자동으로 정규화합니다. 따라서 계산된 지표를 사용하여 표준화를 수행할 필요가 없습니다.
* [!DNL Target] A4T 자동 할당 구현에서 &quot;동일한 터치&quot; 속성 모델을 사용합니다.

자세한 내용은 [분석 도구 안내서](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) 의 속성 개요를 *참조하십시오*.
