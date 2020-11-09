---
keywords: Recommendations
description: Analytics를 Target(A4T)의 보고 소스로 설정할 때 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다.
title: Adobe Target(A4T)의 보고 소스로 Adobe Analytics을 구현하기 전에
feature: a4t implementation
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 52%

---


# 구현하기 전에{#before-you-implement}

Several changes occur in your data collection process when enabling [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

이 통합의 사용 여부를 결정하기 전에, 다음 섹션을 검토하여 보고 프로세스에 미치는 영향을 고려하십시오.

## 구현 요구 사항 {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정을 통합용으로 공급하도록 요청해야 합니다. 프로비저닝을 요청하려면 [Marketing Cloud 통합 규정 양식을](https://www.adobe.com/go/audiences_kr) 사용하십시오.

이 A4T 통합에서는 A4T와 함께 리디렉션 오퍼를 사용할지 여부에 따라 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다.

### A4T에서 리디렉션 오퍼를 사용하지 *않을* 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하지 않을 경우, 이 A4T 통합을 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]:visitorAPI.js 버전 1.8.0
* [!DNL Adobe Target](구현에 따라 다름): at.js 버전 0.9.1 또는 mbox.js 버전 61
* Adobe Analytics: appMeasurement.js 버전 1.7.0

### A4T에서 리디렉션 오퍼를 사용할 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]:visitorAPI.js 버전 2.3.0
* [!DNL Adobe Target]: at.js 버전 1.6.2

   **참고:** mbox.js 라이브러리는 A4T를 사용하는 리디렉션 오퍼를 지원하지 않습니다. 구현에서 at.js를 사용해야 합니다.

* Adobe Analytics: appMeasurement.js 버전 2.1

Download and deployment instructions are listed in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## 구현하기 전에 알아야 할 사항 {#section_50D49CC52E11414089C89FB67F9B88F5}

* This integration is enabled on new activities when you select to use [!DNL Analytics] as the reporting source. 이 문서에 설명된 대로 구현을 변경해도 기존 활동에는 영향을 주지 않습니다.
* The process of setting up [!DNL Analytics] as the reporting source for [!DNL Target] includes several implementation steps, followed by a provisioning step. 구현을 시작하기 전에 아래 설명된 프로세스를 자세히 읽어 보십시오. After you complete these steps, you will be ready to use [!DNL Analytics] as your reporting source as soon as it is enabled for you. 제공 프로세스는 업무일 기준으로 5일 정도 걸릴 수 있습니다.
* The [!DNL Visitor ID service] creates a shared [!DNL Visitor ID] across the [!DNL Adobe Experience Cloud]. Although it does not replace the [!DNL Target] mboxPC id or [!DNL Audience Manager] UUID, it does replace the way [!DNL Analytics] identifies new visitors. If set up properly, returning [!DNL Analytics] visitors should also be identified via their old [!DNL Analytics] ID to prevent visitor cliffing. Similarly, because the [!DNL Target] mboxPCid remains intact, no [!DNL Target] visitor profile data is lost when you upgrade to the [!DNL Visitor ID service].
* 이 [!DNL Visitor ID service] 는 [!DNL Analytics] 및 [!DNL Target] 페이지 코드 앞에서 실행해야 합니다. Make sure that `VisitorAPI.js` appears above the tags for all other [!DNL Experience Cloud] solutions.

## 지연 {#section_9489BE6FD21641A4844E591711E3F813}

After this integration is enabled, you will experience an additional 5-10 minutes of latency in [!DNL Analytics]. This latency increase allows data from [!DNL Analytics] and [!DNL Target] to be stored on the same hit, allowing you to break down activities by page and site section.

This increase is reflected in all [!DNL Analytics] services and tools, including the live-stream and real-time reporting, and applies in the following scenarios:

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표의 현재 데이터, 완료된 데이터, 데이터 피드의 경우 모든 히트 수가 추가적으로 5-7분 지연됩니다.

Be aware that the latency increase starts after you implement the [!DNL Experience Cloud] visitor ID service, even if you have not fully implemented this integration.

## 보충 ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

All [!DNL Target] calls used by an A4T activity to deliver content or record the goal metric must have a corresponding [!DNL Analytics] hit that shares the same supplemental ID for A4T to work properly.

Hits that contain data from [!DNL Analytics] and [!DNL Target] contain a supplemental data ID. You can see this ID in the [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) as the `sdid` parameter. 예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. 이 ID는 다음 기준이 충족될 때 생성됩니다.

* 방문자 ID 서비스가 구현됨
* 이 통합을 지원하는 [!DNL mbox.js] 버전이 구현됨

When [troubleshooting](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), be sure to confirm that the supplemental ID is present on [!DNL Analytics] hits.

## 클라이언트 측 분석 로깅 {#client-side}

기본적으로 at.js, [!DNL Experience Cloud Visitor ID Service] 및 appMeasurement.js가 페이지에 있을 경우 위에 설명된 대로 올바른 보충 ID가 페이지에 포함되어 있으면 [!DNL Analytics] 및 [!DNL Target]은 백엔드에서 보고 및 분석 목적을 위해 이벤트를 올바르게 연결합니다. A4T가 제대로 작동하도록 하기 위해 추가 작업을 관리 및 수행할 필요가 없습니다.

하지만 보고 목적으로 [!DNL Target]과 관련된 분석 데이터를 언제, 어떻게 [!DNL Analytics]로 보낼 것인지를 세부적으로 제어하려는 경우도 있습니다. 내부 용도로 활용하는 사내 분석 도구가 있을 수도 있지만, 사내 분석 제품을 통해 [!DNL Analytics]로 분석 데이터를 전송하여 조직의 다른 구성원이 [!DNL Analytics]를 시각적 보고 소스로 계속 활용할 수 있도록 하려는 경우도 있습니다. 자세한 내용은 *타겟 분석 구현*&#x200B;의 [7단계: 모든 사이트 페이지에서 at.js 또는 mbox.js 참조](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7)를 참조하십시오.

## 공유 대상

Marketing Cloud 통합 프로비저닝 양식 [을 채우는 동안 &quot;프로비저닝을 요청하는 기능](https://www.adobe.com/go/audiences_kr)을 [!UICONTROL 찾는 기능&quot; 아래에 나열된] 공유 대상[!UICONTROL 옵션에 대한 다음 중요한 정보]에 주의하십시오.

![양식 요청](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

공유 대상 [!UICONTROL 을 요청할 때]Target [!UICONTROL 및] Adobe Audience Manager [!UICONTROL (AAM)이] 정보를 공유할 수 있도록 합니다(이 경우 대상).

>[!IMPORTANT]
>
>이러한 [!UICONTROL Target] 와 AAM의 통합은 추가 비용이 동반됩니다. AAM의 각 [!UICONTROL Target] 콜에 대해 청구됩니다.
