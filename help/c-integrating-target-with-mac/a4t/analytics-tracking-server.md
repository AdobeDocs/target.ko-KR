---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;Adobe Experience Cloud debugger;reporting source;developer tools
description: 이전 버전의 at.js나 mbox.js를 사용하는 경우 Analytics for Target(A4T)을 사용하는 활동용으로 Analytics 추적 서버를 지정해야 합니다.
title: Analytics 추적 서버 사용을 참조하십시오
feature: a4t general
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 570f844c8b4ff6a4240262e6a1d2acf0e264ad18
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 24%

---


# Analytics 추적 서버 사용을 참조하십시오{#use-an-analytics-tracking-server}

If you are using an older version of at.js or mbox.js, you must specify an analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.
>
>팀은 at.js 1 모두를 [!DNL Target] 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행하고 있는지 확인하려면 at.js의 주요 버전을 최신 버전으로 업그레이드하십시오. For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Platform Debugger] or your browser&#39;s Developer Tools to determine the correct tracking server for your activity.

## Adobe Experience Platform 디버거를 사용하여 분석 추적 서버 가져오기

올바른 추적 서버를 선택하도록 하기 위해 활동이 전달될 페이지에 이 디버그가 표시됩니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 활동을 엽니다 [!DNL Adobe Experience Platform Debugger].

   디버거를 설치하지 않은 경우 Adobe Experience Platform 디버거 [소개를 참조하십시오](https://docs.adobe.com/content/help/en/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. 왼쪽 탐색 메뉴에서 **[!UICONTROL Analytics]** 를 클릭합니다.

   The analytics tracking server is found in the [!UICONTROL Hostname] section of the debugger.

   * **퍼스트 파티 추적 서버**:요청의 호스트 이름이 현재 사용 중인 도메인과 일치하는 경우 퍼스트 파티 추적 서버입니다. 예를 들어, 사용 중인 경우 `adobe.com`퍼스트 파티 추적 서버 `adobe.com` 가 됩니다.
   * **타사 추적 서버**:타사 추적 서버는 일반적으로 회사 `[company].sc.omtrdc.net` 가 회사의 이름이지만 항상 이 서버로 끝나는 서버입니다 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 는 https(secure) 요청에 대한 CNAME 퍼스트 파티 추적 서버의 예입니다. `stats.adobe.com` 는 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 
1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

## 브라우저의 개발자 도구를 사용하여 분석 추적 서버 가져오기

올바른 추적 서버를 선택할 수 있도록 활동이 제공되는 페이지에서 개발자 도구를 확인해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 브라우저의 개발자 도구를 엽니다(Google Chrome에서 오른쪽 위 모서리에 있는 세 개의 세로 줄임표 > 추가 도구 > 개발자 도구).

   ![Chrome 개발자 툴](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Click the **[!UICONTROL Network]** tab.

1. 분석 요청 `/ss,` 을 표시할 필터입니다.

   ![/ss 검색을 사용하는 Chrome 개발자 툴](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   추적 서버는 요청의 호스트 이름입니다.

   * **퍼스트 파티 추적 서버**:요청의 호스트 이름이 현재 사용 중인 도메인과 일치하는 경우 퍼스트 파티 추적 서버입니다. 예를 들어, 사용 중인 경우 `adobe.com`퍼스트 파티 추적 서버 `adobe.com` 가 됩니다.
   * **타사 추적 서버**:타사 추적 서버는 일반적으로 회사 `[company].sc.omtrdc.net` 가 회사의 이름이지만 항상 이 서버로 끝나는 서버입니다 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 는 https(secure) 요청에 대한 CNAME 퍼스트 파티 추적 서버의 예입니다. `stats.adobe.com` 는 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

