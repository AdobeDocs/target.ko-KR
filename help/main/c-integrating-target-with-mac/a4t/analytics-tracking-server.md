---
keywords: analytics 추적 서버;A4T;Adobe Experience Cloud debugger;Adobe Experience Platform debugger;보고 소스;개발자 도구
description: 용 Analytics를 사용하는 활동에 대한 Analytics 추적 서버를 지정하는 방법을 알아봅니다 [!DNL Target] (A4T) (이전 버전의 at.js를 사용하는 경우).
title: Analytics 추적 서버를 사용하려면 어떻게 합니까?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 21%

---

# 사용 [!DNL Analytics] 추적 서버

이전 버전의 at.js를 사용하는 경우 [!DNL Analytics] 를 사용하는 활동에 대한 추적 서버 [!DNL Adobe Analytics] 대상 [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>at.js 버전 0.9.1 이상을 사용 중이면 활동 생성 도중 추적 서버를 지정하지 않아도 됩니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 생성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.
>
>다음 [!DNL Target] 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행 중인지 확인하려면 at.js의 주요 버전 중 가장 최근의 업데이트로 업그레이드하십시오. 자세한 내용은 [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

에서 데이터를 확인하려면 [!DNL Target] 의 올바른 위치로 이동합니다. [!DNL Analytics], A4T에는 [!DNL Analytics] 에서 Modstats에 대한 모든 호출에서 전송될 추적 서버 [!DNL Target]. 여러 추적 서버를 사용하는 구현의 경우 [!DNL Adobe Experience Platform Debugger] 또는 브라우저의 개발자 도구를 사용하여 활동에 대한 올바른 추적 서버를 결정할 수 있습니다.

## 가져오기 [!DNL Analytics] 를 사용하는 추적 서버 [!DNL Adobe Experience Platform Debugger]

올바른 추적 서버를 선택하려면 활동이 전달되는 페이지에서 디버거를 확인해야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 를 엽니다. [!DNL Adobe Experience Platform Debugger].

   디버거를 설치하지 않았다면 다음을 참조하십시오 [Adobe Experience Platform Debugger 개요](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. 클릭 **[!UICONTROL 분석]** 왼쪽 탐색 메뉴에서 을 클릭합니다.

   ![Screen_DebuggerTrackServ 이미지](assets/Screen_DebuggerTrackServ.png)

   다음 [!DNL Analytics] 추적 서버는 [!UICONTROL 호스트 이름] 디버거의 섹션입니다.

   * **자사 추적 서버**: 요청의 호스트 이름이 현재 사용 중인 도메인과 일치하면 자사 추적 서버입니다. 예를 들어 을 사용 중인 경우 `adobe.com`, `adobe.com` 는 자사 추적 서버입니다.
   * **서드파티 추적 서버**: 서드파티 추적 서버는 일반적으로 `[company].sc.omtrdc.net` 여기서 는 회사의 이름이지만 항상 로 끝납니다. `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 은 https(보안) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com` 은 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >선택 [!UICONTROL 보고 소스로서의 Analytics] 을(를) 위한 활동에 대해 [!UICONTROL 추적 서버] 사용할 수 있는 필드입니다.

## 가져오기 [!DNL Analytics] 브라우저의 개발자 도구를 사용한 추적 서버

개발자 도구는 올바른 추적 서버를 선택했는지 확인하기 위해 활동이 제공되는 페이지에 표시되어야 합니다. 각 계정에 대해 기본 추적 서버를 지정할 수도 있습니다. 고객 지원 센터에 문의하여 기본값을 지정하거나 수정하십시오.

1. 활동을 만드는 페이지에서 브라우저의 개발자 도구를 엽니다(Google Chrome에서 오른쪽 상단 모서리의 3개 수직 줄임표 > 추가 도구 > 개발자 도구 클릭).

   ![Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. 다음을 클릭합니다. **[!UICONTROL 네트워크]** 탭.

1. 필터 대상 `/ss,` 을(를) 표시하려면 [!DNL Analytics] 요청.

   ![/ss search를 사용한 Chrome 개발자 도구](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   추적 서버는 요청의 호스트 이름입니다.

   * **자사 추적 서버**: 요청의 호스트 이름이 현재 사용 중인 도메인과 일치하면 자사 추적 서버입니다. 예를 들어 을 사용 중인 경우 `adobe.com`, `adobe.com` 는 자사 추적 서버입니다.
   * **서드파티 추적 서버**: 서드파티 추적 서버는 일반적으로 `[company].sc.omtrdc.net` 여기서 는 회사의 이름이지만 항상 로 끝납니다. `sc.omtrdc.net`.
   * **CNAME 구현**: `sstats.adobe.com` 은 https(보안) 요청에 대한 CNAME 자사 추적 서버의 예입니다. `stats.adobe.com` 은 http(비보안) 페이지에 대한 CNAME 자사 요청의 예입니다.

1.  필드의 전체 컨텐츠를 복사합니다. 

1. 활동의 **[!UICONTROL 목표 및 설정]****[!UICONTROL 화면에 있는]**&#x200B;보고 설정&#x200B;**[!UICONTROL 섹션에서 추적 서버 정보를 추적 서버]** 필드에 붙여넣으십시오.

   >[!NOTE]
   >
   >선택 [!UICONTROL 보고 소스로서의 Analytics] 을(를) 위한 활동에 대해 [!UICONTROL 추적 서버] 사용할 수 있는 필드입니다.
