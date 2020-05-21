---
keywords: analytics for target;a4t;analytics as the reporting source
description: Analytics를 Target(A4T)의 보고 소스로 사용하면 Target 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.
title: A4T 보고
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 44%

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

## Analytics의 보고서 {#section_F6884872DC864AE7913587FAED4CD11C}

In [!DNL Analytics], click **[!UICONTROL Target]** > **[!UICONTROL Target Activities]** in the left menu. In [!DNL Target], the activity&#39;s reports automatically show [!DNL Analytics] data, metrics, and segments. 데이터는 사이트에서 수집된 후 약 1시간 후에 이러한 보고서에 표시됩니다. 보고서에 있는 모든 지표, 대상, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

In [!DNL Analytics], use the [!UICONTROL Target Activities] report to view the results of your [!DNL Target] activity. Test&amp;Target (Legacy) Reports provides information about your old Test&amp;Target plug-in style page integrations and does not include [!DNL Analytics] for [!DNL Target] data. In the [!UICONTROL Activities] report, view information about your [!DNL Target] experiences. **[!UICONTROL 지표]**&#x200B;를 클릭하고 **[!UICONTROL Target 지표 유형을 선택합니다.]** 보고서에서 두 개의 지표를 사용할 수 있습니다.

* **활동 시작:**[!DNL Target] 보고서에서 참여자 수와 일치합니다.
* **활동 전환:**[!DNL Target] 보고서에서 사용자 지정 전환 수와 일치합니다.

>[!NOTE]
>
>[!DNL Target] 향상도 및 신뢰도 세부 사항도 제공됩니다 [!DNL Analytics]. 자세한 내용은 [Analytics 구성 요소 안내서의](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/report-target-lift-confidence.html) Target 향상도 및 신뢰도를 *참조하십시오*.

>[!IMPORTANT]
>
>If your [!UICONTROL Target Activities] report in [!DNL Analytics] lists &quot;unspecified&quot; instead of listing your activities, an update is required to your provisioned account. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

## Target의 보고서 {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] is used as the reporting source, reports in [!DNL Target] show the data gathered from [!DNL Analytics]. The report differs somewhat from other [!DNL Target] reports:

* The [!UICONTROL Audiences] list shows the audiences available to your [!DNL Analytics] report suite.
* The [!UICONTROL Metric] list shows every metric available through [!DNL Analytics].

   Every metric is available, including any custom or calculated metrics that are built-in in [!DNL Analytics].

   수치 증가가 실제로 불필요하더라도 증가되는 모든 숫자는 보고서에서 양수로 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the test has completed. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

Click to view the full [!DNL Analytics] report directly from the activity report page.

## Analysis Workspace의 보고서 {#reports-in-analysis-workspace}

[!DNL Adobe Analysis Workspace]를 사용하여 데이터를 보다 깊이 있게 분석하고 그 이면에 대한 통찰력을 얻을 수 있습니다.

자세한 정보 및 예제를 보려면 [분석 및 대상을 엽니다. 분석 모범 사례 자습서](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)(제공) [!DNL Adobe Experience League].

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 중에 [!UICONTROL 설정] 페이지에서 활동의 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. 대상이 아닌 세그먼트 [!DNL Analytics] 를 사용하는 [!DNL Adobe Analytics] [!DNL Target] 테스트입니다.

## Performing offline calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 

자세한 내용은 [Analytics for Target (A4T)에 사용할 오프라인 계산 수행](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)을 참조하십시오.
