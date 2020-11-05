---
keywords: analytics for target;a4t;analytics as the reporting source
description: Analytics를 Target(A4T)의 보고 소스로 사용하면 Target 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.
title: A4T 보고
feature: a4t reports
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 35%

---


# A4T 보고{#a-t-reporting}

Using [!DNL Analytics] as your reporting source for [!DNL Target] (A4T) gives you access to [!DNL Analytics] reports for your [!DNL Target] activities.

You can view reports for your activities in both [!DNL Analytics] and [!DNL Target].

For reporting best practices using [!DNL Analytics] for [!DNL Target], [visit this Adobe Spark page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## 개요 {#section_035A62D65608423285D8A5A54731E2C5}

Both [!DNL Analytics] and [!DNL Target] reports measure entrants (the people who enter the tests), rather than visitors to the site.

Every time a visitor sees activity content on the page, [!DNL Target] makes a direct server-to-server call to [!DNL Analytics], including which activity and experience the visitor saw. [!DNL Target] 또한 전환이 이루어지는 [!DNL Analytics] 때마다 호출됩니다. [!DNL Analytics] 이 전환을 &quot;활동 전환&quot;이라는 이름의 특정 새 [!DNL Analytics] [!DNL Analytics]이벤트로 추가하고, 이 이벤트는

When the [!UICONTROL Select] operation is used and you sort on *Entrants*, then only experiences that received entrants during the selected time period are displayed in the reports.

>[!NOTE]
>
>Reports powered by [!DNL Target] have a latency of four minutes. For activities powered by A4T, in both the [!DNL Target] and [!DNL Analytics] reports, it can take up to 24 hours after the activity is initially saved before the report data can be broken down by experiences. 처음 24시간 내에 수집된 데이터는 정확하며 올바른 경험에 지정됩니다.

## Analytics의 보고서 {#analytics}

A4T 통합 [!DNL Analytics]이 활성화된 후 사용할 수 있는 차원 및 지표가 몇 가지 있습니다.

### 차원

* [!UICONTROL Target] 분석 - 통합을 통해 전달된 상위 ID입니다. 이 차원의 형식은 입니다 `Activity ID:Experience ID:3rd ID`. 아래 차원은 이 차원의 분류입니다.
* [!UICONTROL 타겟 활동]
* [!UICONTROL 타겟 경험]
* [!UICONTROL Target 활동] > [!UICONTROL 경험]
* [!UICONTROL 세 번째 ID] - 무시할 수 있음

### 지표

* [!UICONTROL 활동 노출 횟수] - 보고서의 [!UICONTROL 참여자] 수와 [!DNL Target] 일치합니다.
* [!UICONTROL 활동 전환] - [!UICONTROL 보고서의] 사용자 지정 전환 [!DNL Target] 번호와 일치합니다.

에서 [!DNL Analysis Workspace]Target용 [!UICONTROL 분석] 패널을 사용하여 [!DNL Target] 활동 및 경험을 향상시키거나 자신있게 분석할 수 있습니다. 자세한 내용은 [분석 도구 안내서의 Target(A4T) 패널](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) 분석을 *참조하십시오*.

>[!IMPORTANT]
>
>If your [!UICONTROL Target Activities] report in [!DNL Analytics] lists &quot;unspecified&quot; instead of listing your activities, an update is required to your provisioned account. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, provided by Adobe Experience League.

## Target의 보고서 {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] is used as the reporting source, reports in [!DNL Target] show the data gathered from [!DNL Analytics]. The report differs somewhat from other [!DNL Target] reports:

* The [!UICONTROL Audiences] list shows the audiences available to your [!DNL Analytics] report suite.
* The [!UICONTROL Metric] list shows every metric available through [!DNL Analytics].

   Every metric is available, including any custom or calculated metrics that are built-in in [!DNL Analytics].

   수치 증가가 실제로 불필요하더라도 증가되는 모든 숫자는 보고서에서 양수로 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the test has completed. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

Click to view the full [!DNL Analytics] report directly from the activity report page.

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 중에 [!UICONTROL 설정] 페이지에서 활동의 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. 대상이 아닌 세그먼트 [!DNL Analytics] 를 사용하는 [!DNL Adobe Analytics] [!DNL Target] 테스트입니다.

## Performing offline calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 

자세한 내용은 [Analytics for Target (A4T)에 사용할 오프라인 계산 수행](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)을 참조하십시오.
