---
keywords: analytics 추적 서버;A4T;Adobe Experience Cloud 디버거;Adobe Experience Platform 디버거;보고 소스;개발자 도구
description: Analytics를 사용하는 활동에 대해 Analytics 추적 서버를 지정하는 방법을 알아봅니다. [!DNL Target] (A4T) 이전 버전의 at.js를 사용하는 경우
title: Analytics 추적 서버를 어떻게 사용합니까?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 21%

---

# 다음 중 하나를 사용합니다 [!DNL Analytics] 추적 서버

at.js의 이전 버전을 사용하는 경우 다음을 지정해야 합니다 [!DNL Analytics] 를 사용하는 활동에 대한 추적 서버 [!DNL Adobe Analytics] 대상 [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>at.js 버전 0.9.1 이상을 사용 중이면 활동 생성 도중 추적 서버를 지정하지 않아도 됩니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 생성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.
>
>다음 [!DNL Target] 팀은 at.js 1.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행 중인지 확인하려면 at.js의 주요 버전을 최신 업데이트로 업그레이드하십시오. 자세한 내용은 [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

데이터를에서 [!DNL Target] 에서 올바른 위치로 이동 [!DNL Analytics], A4T에는 [!DNL Analytics] Modstats에 대한 모든 호출에서 전송할 추적 서버 [!DNL Target]. 여러 추적 서버를 사용하는 구현의 경우 [!DNL Adobe Experience Platform Debugger] 또는 브라우저의 개발자 도구를 사용하여 활동에 대한 올바른 추적 서버를 결정합니다.

## 가져오기 [!DNL Analytics] 를 사용하여 추적 서버 [!DNL Adobe Experience Platform Debugger]

올바른 추적 서버를 선택해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 를 엽니다 [!DNL Adobe Experience Platform Debugger].

   디버거를 설치하지 않았다면 을 참조하십시오. [Adobe Experience Platform Debugger 개요](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. 클릭 **[!UICONTROL Analytics]** 를 클릭합니다.

   ![Screen_DebuggerTrackServ 이미지](assets/Screen_DebuggerTrackServ.png)

   다음 [!DNL Analytics] 추적 서버는 [!UICONTROL 호스트 이름] 섹션에 있는 마지막 항목이 될 필요가 없습니다.

   * **자사 추적 서버**: 요청의 호스트 이름이 현재 있는 도메인과 일치하면 이는 자사 추적 서버입니다. 예를 들어, `adobe.com`, `adobe.com` 는 자사 추적 서버입니다.
   * **타사 추적 서버**: 일반적으로 타사 추적 서버는 `[company].sc.omtrdc.net` 여기서 회사는 회사의 이름이지만 항상 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` https(secure) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com` http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >선택 [!UICONTROL 보고 소스로서의 Analytics] 을 사용하도록 선택할 수 있습니다. [!UICONTROL 추적 서버] 필드를 사용할 수 있습니다.

## 가져오기 [!DNL Analytics] 브라우저의 개발자 도구를 사용하여 추적 서버

올바른 추적 서버를 선택해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 브라우저의 개발자 도구(Google Chrome에서 오른쪽 상단 모서리의 세 개의 세로 줄임표 > 추가 도구 > 개발자 도구)를 클릭합니다.

   ![Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. 을(를) 클릭합니다. **[!UICONTROL 네트워크]** 탭.

1. 필터 대상 `/ss,` 를 [!DNL Analytics] 요청.

   ![/ss 검색을 사용하는 Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   추적 서버는 요청의 호스트 이름입니다.

   * **자사 추적 서버**: 요청의 호스트 이름이 현재 있는 도메인과 일치하면 이는 자사 추적 서버입니다. 예를 들어, `adobe.com`, `adobe.com` 는 자사 추적 서버입니다.
   * **타사 추적 서버**: 일반적으로 타사 추적 서버는 `[company].sc.omtrdc.net` 여기서 회사는 회사의 이름이지만 항상 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` https(secure) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com` http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >선택 [!UICONTROL 보고 소스로서의 Analytics] 을 사용하도록 선택할 수 있습니다. [!UICONTROL 추적 서버] 필드를 사용할 수 있습니다.
