---
keywords: 분석 추적 서버;A4T;Adobe Experience Cloud 디버거;Adobe Experience Platform 디버거;보고 소스;개발자 도구
description: 'at.js 또는 mbox.js의 이전 버전을 사용하는 경우 Target(A4T)용 Analytics를 사용하는 활동에 대한 Analytics 추적 서버를 지정하는 방법에 대해 학습합니다. '
title: Analytics 추적 서버를 어떻게 사용합니까?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 22%

---


# Analytics 추적 서버 사용을 참조하십시오

at.js 또는 mbox.js의 이전 버전을 사용하는 경우 [!DNL Target](A4T)에 [!DNL Analytics]을(를) 사용하는 활동에 대한 Analytics 추적 서버를 지정해야 합니다.

>[!NOTE]
>
>활동의 보고 소스로 [!DNL Analytics]을 사용하는 경우 mbox.js 버전 61(이상) 또는 at.js 버전 0.9.1(이상)를 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.
>
>[!DNL Target] 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행하고 있는지 확인하려면 at.js의 주요 버전 중 하나의 최신 버전으로 업그레이드하십시오. 자세한 내용은 [at.js 버전 세부 정보](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)를 참조하십시오.

[!DNL Target]의 데이터가 [!DNL Analytics]의 올바른 위치로 이동하도록 하려면 A4T에서 [!DNL Target]의 모든 Modstats 호출에서 Analytics 추적 서버를 전송해야 합니다. 여러 추적 서버를 사용하는 구현의 경우 [!DNL Adobe Experience Platform Debugger] 또는 브라우저의 개발자 도구를 사용하여 활동에 대한 올바른 추적 서버를 확인할 수 있습니다.

## Adobe Experience Platform Debugger를 사용하여 Analytics 추적 서버 가져오기

올바른 추적 서버를 선택하도록 하기 위해 활동이 전달될 페이지에 이 디버그가 표시됩니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 [!DNL Adobe Experience Platform Debugger]을 엽니다.

   디버거를 설치하지 않은 경우 [Adobe Experience Platform 디버거 소개](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html)를 참조하십시오.

   ![](assets/Screen_DebuggerTrackServ.png)

1. 왼쪽 탐색 메뉴에서 **[!UICONTROL 분석]**&#x200B;을 클릭합니다.

   Analytics 추적 서버는 디버거의 [!UICONTROL 호스트 이름] 섹션에 있습니다.

   * **자사 추적 서버**:요청의 호스트 이름이 현재 있는 도메인과 일치하는 경우 퍼스트 파티 추적 서버입니다. 예를 들어 `adobe.com`에 있는 경우 `adobe.com`은(는) 퍼스트 파티 추적 서버입니다.
   * **타사 추적 서버**:제3자 추적 서버는 일반적으로 회사  `[company].sc.omtrdc.net` 이름이지만 항상 다음으로 끝납니다 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 는 https(secure) 요청에 대한 CNAME 퍼스트 파티 추적 서버의 예입니다. `stats.adobe.com` 는 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >[!UICONTROL 추적 서버] 필드를 사용할 수 있게 하려면 [!UICONTROL Analytics를 보고 소스]로 선택해야 합니다.

## 브라우저의 개발자 도구를 사용하여 Analytics 추적 서버 가져오기

올바른 추적 서버를 선택할 수 있도록 활동이 제공되는 페이지에서 개발자 도구를 확인해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 브라우저의 개발자 도구를 엽니다(Google Chrome에서 오른쪽 위 모서리에 있는 3개의 세로 줄임표 > 추가 도구 > 개발자 도구).

   ![Chrome 개발자 툴](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. **[!UICONTROL 네트워크]** 탭을 클릭합니다.

1. Analytics 요청을 표시하는 `/ss,`에 대한 필터입니다.

   ![/ss 검색을 사용한 Chrome 개발자 툴](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   추적 서버는 요청의 호스트 이름입니다.

   * **자사 추적 서버**:요청의 호스트 이름이 현재 있는 도메인과 일치하는 경우 퍼스트 파티 추적 서버입니다. 예를 들어 `adobe.com`에 있는 경우 `adobe.com`은(는) 퍼스트 파티 추적 서버입니다.
   * **타사 추적 서버**:제3자 추적 서버는 일반적으로 회사  `[company].sc.omtrdc.net` 이름이지만 항상 다음으로 끝납니다 `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 는 https(secure) 요청에 대한 CNAME 퍼스트 파티 추적 서버의 예입니다. `stats.adobe.com` 는 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >[!UICONTROL 추적 서버] 필드를 사용할 수 있게 하려면 [!UICONTROL Analytics를 보고 소스]로 선택해야 합니다.

