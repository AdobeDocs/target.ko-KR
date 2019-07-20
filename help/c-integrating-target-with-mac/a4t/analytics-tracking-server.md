---
description: 이전 버전의 at.js나 mbox.js를 사용하는 경우 Analytics for Target(A4T)을 사용하는 활동용으로 Analytics 추적 서버를 지정해야 합니다.
keywords: analytics 추적 서버;A4T;Adobe Experience Cloud 디버거;보고 소스
seo-description: 이전 버전의 at.js나 mbox.js를 사용하는 경우 Analytics for Target(A4T)을 사용하는 활동용으로 Analytics 추적 서버를 지정해야 합니다.
seo-title: Analytics 추적 서버 사용을 참조하십시오
title: Analytics 추적 서버 사용을 참조하십시오
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Analytics 추적 서버 사용{#use-an-analytics-tracking-server}을 참조하십시오

이전 버전의 at.js나 mbox.js를 사용하는 경우 Analytics for Target(A4T)을 사용하는 활동용으로 Analytics 추적 서버를 지정해야 합니다.

>[!NOTE]
>
>Adobe Analytics를 활동의 보고 소스로 사용하는 경우, mbox.js 버전 61 이상 또는 at.js 버전 0.9.1 이상을 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

Target의 데이터가 Analytics의 올바른 위치로 이동되려면 Target에서 Modstats으로의 모든 호출에 Analytics 추적 서버가 전송되어야 합니다. 여러 추적 서버를 사용하는 구현의 경우, Adobe Experience Cloud Debugger를 사용하여 활동에 맞는 올바른 추적 서버를 확인할 수 있습니다.

올바른 추적 서버를 선택하도록 하기 위해 활동이 전달될 페이지에 이 디버그가 표시됩니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 Adobe Experience Cloud Debugger를 엽니다. 

   이 디버거를 설치하지 않은 경우 [Adobe Debugger 설치 지침](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_install.html)을 따르십시오.

   ![](assets/Screen_DebuggerTrackServ.png)

   Analytics 추적 서버는 디버거의 SiteCatalyst 이미지 섹션에 있습니다. 이 필드를 구현에 따라 *자사 쿠키* 또는 *타사 쿠키*&#x200B;라고 하며, Analytics 추적 서버값은 다음 형식 중 하나입니다.

   * (CNAME 구현의 경우)
   * (비RDC 구현의 경우)
   * (RDC 구현의 경우)
   *Company*&#x200B;는 Analytics 회사 이름을 나타내고, *metrics*&#x200B;는 CNAME 값의 예이며 *d1*&#x200B;은 Analytics 데이터 센터의 예입니다.
1.  필드의 전체 컨텐츠를 복사합니다. 
1. 활동의 [!UICONTROL 목표 및 설정][!UICONTROL  화면에 있는 ]보고 설정&#x200B;**섹션에서 추적 서버 정보를[!UICONTROL 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >추적 서버 필드를 사용하려면 활동에 대한 보고 소스로 Adobe Analytics를 선택해야 합니다.

