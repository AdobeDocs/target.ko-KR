---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.
title: 활동 만들기
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 40%

---


# 활동 만들기{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. 활동의 최종 성공 지표를 선택합니다. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

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
