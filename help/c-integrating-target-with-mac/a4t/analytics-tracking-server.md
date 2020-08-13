---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;reporting source
description: 이전 버전의 at.js나 mbox.js를 사용하는 경우 Analytics for Target(A4T)을 사용하는 활동용으로 Analytics 추적 서버를 지정해야 합니다.
title: Analytics 추적 서버 사용을 참조하십시오
feature: a4t general
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 53%

---


# Analytics 추적 서버 사용을 참조하십시오{#use-an-analytics-tracking-server}

If you are using an older version of at.js or mbox.js, you must specify an analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Cloud Debugger] to determine the correct tracking server for your activity.

올바른 추적 서버를 선택하도록 하기 위해 활동이 전달될 페이지에 이 디버그가 표시됩니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 활동을 엽니다 [!DNL Adobe Experience Cloud Debugger].

   디버거를 설치하지 않은 경우 Experience Cloud Debugger [설치를 참조하십시오](https://docs.adobe.com/content/help/en/debugger/using/install-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

   The analytics tracking server is found in the [!UICONTROL SiteCatalyst Image] section of the debugger. 이 필드를 구현에 따라 *자사 쿠키* 또는 *타사 쿠키*&#x200B;라고 하며,  추적 서버값은 다음 형식 중 하나입니다.[!DNL Analytics]

   * (CNAME 구현의 경우)
   * (비RDC 구현의 경우)
   * (RDC 구현의 경우)

   *Company*[!DNL Analytics]는 회사 이름을 나타내고, *metrics*&#x200B;는 CNAME 값의 예이며 *d1*&#x200B;은 데이터 센터의 예입니다.[!DNL Analytics]
1.  필드의 전체 컨텐츠를 복사합니다. 
1. 활동의 [!UICONTROL 목표 및 설정][!UICONTROL  화면에 있는 ]보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

