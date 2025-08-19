---
keywords: analytics 추적 서버;A4T;Adobe Experience Cloud debugger;Adobe Experience Platform debugger;보고 소스;개발자 도구
description: 이전 버전의 at.js를 사용하는 경우 Analytics for [!DNL Target] (A4T)을(를) 사용하는 활동에 대한 Analytics 추적 서버를 지정하는 방법을 알아봅니다.
title: Analytics 추적 서버를 사용하려면 어떻게 합니까?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%

---

# [!DNL Analytics] 추적 서버 사용

이전 버전의 at.js를 사용하는 경우 [!DNL Analytics]에 대해 [!DNL Adobe Analytics]을(를) 사용하는 활동(A4T)에 대해 [!DNL Adobe Target] 추적 서버를 지정해야 합니다.

>[!NOTE]
>
>at.js 버전 0.9.1 이상을 사용 중이면 활동 생성 도중 추적 서버를 지정하지 않아도 됩니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 만드는 동안 [!UICONTROL Tracking Server] 페이지의 [!UICONTROL Goals & Settings] 필드를 비워 둘 수 있습니다.
>
>[!DNL Target] 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2 모두에 있는 Hide Body(본문 숨기기) 및 Show Body(본문 표시) 호출을 보여줍니다.*x*. 지원되는 버전을 실행 중인지 확인하려면 at.js의 주요 버전 중 가장 최근의 업데이트로 업그레이드하십시오. 자세한 내용은 [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank}을 참조하십시오.

[!DNL Target]의 데이터가 [!DNL Analytics]의 올바른 위치로 이동하도록 하려면 A4T에서는 [!DNL Analytics]의 모든 Modstats 호출에서 [!DNL Target] 추적 서버를 보내야 합니다. 여러 추적 서버를 사용하는 구현의 경우 [!DNL Adobe Experience Platform Debugger] 또는 브라우저의 개발자 도구를 사용하여 활동에 대한 올바른 추적 서버를 결정하십시오.

## [!DNL Analytics]을(를) 사용하여 [!DNL Adobe Experience Platform Debugger] 추적 서버 가져오기

올바른 추적 서버를 선택하려면 활동이 전달되는 페이지에서 디버거를 확인해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 [!DNL Adobe Experience Platform Debugger]을(를) 엽니다.

   디버거를 설치하지 않았다면 [Adobe Experience Platform Debugger 개요](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html?lang=ko)를 참조하십시오.

1. 왼쪽 탐색 메뉴에서 **[!UICONTROL Analytics]**&#x200B;을(를) 클릭합니다.

   ![Screen_DebuggerTrackServ 이미지](assets/Screen_DebuggerTrackServ.png)

   디버거의 [!DNL Analytics] 섹션에 [!UICONTROL Hostname] 추적 서버가 있습니다.

   * **퍼스트 파티 추적 서버**: 요청의 호스트 이름이 현재 있는 도메인과 일치하면 퍼스트 파티 추적 서버입니다. 예를 들어 `adobe.com`에 있는 경우 `adobe.com`은(는) 자사 추적 서버입니다.
   * **타사 추적 서버**: 타사 추적 서버는 일반적으로 `[company].sc.omtrdc.net`이며 여기서 회사는 회사 이름이지만 항상 `sc.omtrdc.net`로 끝납니다.
   * **CNAME 구현**: `sstats.adobe.com`은(는) https(보안) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com`은(는) http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1. 필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL Reporting Settings]** 화면에 있는 **[!UICONTROL Goal & Settings]** 섹션에서 **[!UICONTROL Tracking Server]** 필드에 추적 서버 정보를 붙여 넣습니다.

   >[!NOTE]
   >
   >[!UICONTROL Analytics as the Reporting Source] 필드를 사용하려면 활동에 대해 [!UICONTROL Tracking Server]을(를) 선택하십시오.

## 브라우저의 개발자 도구를 사용하여 [!DNL Analytics] 추적 서버 가져오기

개발자 도구는 올바른 추적 서버를 선택했는지 확인하기 위해 활동이 제공되는 페이지에 표시되어야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 브라우저의 개발자 도구를 엽니다(Google Chrome에서 오른쪽 상단 모서리의 3개 수직 줄임표 > 추가 도구 > 개발자 도구 클릭).

   ![Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. **[!UICONTROL Network]** 탭을 클릭합니다.

1. `/ss,`을(를) 필터링하여 [!DNL Analytics] 요청을 표시합니다.

   ![/ss search가 있는 Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   추적 서버는 요청의 호스트 이름입니다.

   * **퍼스트 파티 추적 서버**: 요청의 호스트 이름이 현재 있는 도메인과 일치하면 퍼스트 파티 추적 서버입니다. 예를 들어 `adobe.com`에 있는 경우 `adobe.com`은(는) 자사 추적 서버입니다.
   * **타사 추적 서버**: 타사 추적 서버는 일반적으로 `[company].sc.omtrdc.net`이며 여기서 회사는 회사 이름이지만 항상 `sc.omtrdc.net`로 끝납니다.
   * **CNAME 구현**: `sstats.adobe.com`은(는) https(보안) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com`은(는) http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1. 필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL Reporting Settings]** 화면에 있는 **[!UICONTROL Goal & Settings]** 섹션에서 **[!UICONTROL Tracking Server]** 필드에 추적 서버 정보를 붙여 넣습니다.

   >[!NOTE]
   >
   >[!UICONTROL Analytics as the Reporting Source] 필드를 사용하려면 활동에 대해 [!UICONTROL Tracking Server]을(를) 선택하십시오.
