---
keywords: Recommendations
description: 용 Analytics에 대한 구현 요구 사항 알아보기 [!DNL Target] (A4T) 및 이 통합을 구현하기 전에 고려해야 할 사항.
title: A4T를 구현하기 전에 알아야 할 사항은 무엇입니까?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 24%

---

# at.js로 Analytics for Target(A4T)을 구현하기 전

을 활성화하면 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다 [!DNL Adobe Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Adobe Target] (A4T).

이 통합을 사용하기 전에 다음 섹션을 검토하여 보고 프로세스에 미치는 영향을 고려하십시오.

>[!NOTE]
>
>이 문서는 at.js 구현에만 적용됩니다.

## 구현 요구 사항 {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정에 통합을 위한 권한이 제공되도록 요청해야 합니다. 사용 [Marketing Cloud 통합 프로비저닝 양식](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} 을(를) 요청하십시오.

이 A4T 통합에서는 A4T와 함께 리디렉션 오퍼를 사용할지 여부에 따라 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다.

>[!NOTE]
>
>다음 요구 사항에는 *최소값* A4T 구현에 필요한 at.js 버전입니다. 다음 [!DNL Target] 팀은 의 두 버전만 유지 관리합니다. [!DNL at.js]- 현재 버전과 바로 전 버전. 지원되는 버전을 실행 중인지 확인하려면 [!DNL at.js]를 필요에 따라 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

### A4T에서 리디렉션 오퍼를 사용하지 *않을* 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하지 않을 경우, 이 A4T 통합을 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 1.8.0
* [!DNL Adobe Target]: at.js  버전 0.9.1
* Adobe Analytics: appMeasurement.js 버전 1.7.0

를 사용한 A4T 구현에 대한 정보는 [!DNL Platform Web SDK], 참조 [Adobe Experience Platform 웹 SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

### A4T에서 리디렉션 오퍼를 사용할 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 2.3.0

   >[!NOTE]
   >
   >at.js 1.8.0+ 및 at.js 2.x+는 Adobe Audience Manager(AAM) 매개변수 전달에 대해 더 이상 2.5.0 이전 버전의 방문자 API와 동작하지 않습니다.

* [!DNL Adobe Target]: at.js  버전 1.6.2

* Adobe Analytics: appMeasurement.js 버전 2.1

다운로드 및 배포 지침은 [Analytics for Target 구현](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

를 사용한 A4T 구현에 대한 정보는 [!DNL Platform Web SDK], 참조 [Adobe Experience Platform 웹 SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

## 구현하기 전에 알아야 할 사항 {#section_50D49CC52E11414089C89FB67F9B88F5}

* 이 통합은 을(를) 사용하도록 선택하면 새 활동에서 활성화됩니다 [!DNL Analytics] 를 보고 소스로 사용합니다. 이 문서에 설명된 대로 구현을 변경해도 기존 활동에는 영향을 주지 않습니다.
* 설정 프로세스 [!DNL Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Target] 에는 몇 가지 구현 단계, 그 뒤에 프로비저닝 단계가 포함됩니다. 구현을 시작하기 전에 아래 설명된 프로세스를 자세히 읽어 보십시오. 이 단계를 완료하고 나면 사용할 준비가 된 것입니다 [!DNL Analytics] 를 보고 소스로 사용하도록 설정한 경우 제공 프로세스는 업무일 기준으로 5일 정도 걸릴 수 있습니다.
* 다음 [!DNL Visitor ID service] 공유 항목 만들기 [!DNL Visitor ID] 의 맞은편에 [!DNL Adobe Experience Cloud]. 를 대체하지는 않지만 [!DNL Target] mboxPC id 또는 [!DNL Audience Manager] UUID, 다음 방법을 대체합니다. [!DNL Analytics] 는 새 방문자를 식별합니다. 제대로 설정된 경우 [!DNL Analytics] 방문자는 이전 방문자를 통해서도 식별되어야 합니다 [!DNL Analytics] ID 마찬가지로, [!DNL Target] mboxPCid는 그대로 유지되며, 아니요 [!DNL Target] 로 업그레이드하면 방문자 프로필 데이터가 손실됩니다. [!DNL Visitor ID service].
* 다음 [!DNL Visitor ID service] 은(는) 다음 작업 이전에 실행되어야 합니다. [!DNL Analytics] 및 [!DNL Target] 페이지 코드. 다음을 확인합니다. `VisitorAPI.js` 다른 모든 태그에 대한 태그 위에 표시 [!DNL Experience Cloud] 솔루션.

## 지연 {#section_9489BE6FD21641A4844E591711E3F813}

이 통합이 활성화되면 에서 5~10분 동안 지연이 추가로 발생합니다. [!DNL Analytics]. 이러한 지연 시간 증가를 통해 다음에서 데이터가 허용됩니다. [!DNL Analytics] 및 [!DNL Target] 동일한 히트에 저장되므로 페이지 및 사이트 섹션별로 활동을 분류할 수 있습니다.

이러한 증가는 모든 항목에 반영됩니다 [!DNL Analytics] 라이브 스트림 및 실시간 보고를 포함하는 서비스 및 도구이며, 다음 시나리오에 적용됩니다.

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표에 대한 현재 데이터, 최종 데이터 및 데이터 피드의 경우 모든 히트가 5~7분 더 지연됩니다.

지연 증가는 구현 후 시작됩니다. [!DNL Experience Cloud] 이 통합을 완전히 구현하지 않았더라도 방문자 ID 서비스입니다.

## 보충 ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

모두 [!DNL Target] 콘텐츠를 전달하거나 목표 지표를 기록하기 위해 A4T 활동에서 사용하는 호출에는 해당하는 항목이 있어야 합니다. [!DNL Analytics] a4T용 보조 ID를 공유하는 히트가 제대로 작동하도록 합니다.

의 데이터가 포함된 히트 [!DNL Analytics] 및 [!DNL Target] 에는 보조 데이터 ID가 포함되어 있습니다. 이 ID는 [Adobe Experience Cloud 디버거](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) (으)로 `sdid` 매개 변수. 예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. 이 ID는 다음 기준이 충족될 때 생성됩니다.

* 방문자 ID 서비스가 구현됨

날짜 [문제 해결](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)에 보조 ID가 있는지 확인하십시오. [!DNL Analytics] 히트 수.

## 클라이언트 측 분석 로깅 {#client-side}

at.js인 경우 [!DNL Experience Cloud Visitor ID Service]및 appMeasurement.js가 페이지에 있는 경우 [!DNL Analytics], 및 [!DNL Target] 올바른 보충 ID가 페이지에 포함되어 있으면 백엔드에서 보고 및 분석 목적으로 이벤트를 올바르게 결합합니다. A4T가 올바르게 작동하기 위해 추가 작업을 관리하고 수행할 필요가 없습니다.

관련된 분석 데이터를 언제, 어떻게 보낼 것인지를 세부적으로 제어하려는 경우가 있습니다. [!DNL Target] 끝 [!DNL Analytics] 보고 목적으로. 내부 용도로 사용하는 사내 분석 도구가 있을 수 있습니다. 하지만 Analytics 데이터도 로 보내려고 합니다. [!DNL Analytics] 조직의 다른 구성원이 계속 사용할 수 있도록 사내 analytics 제품을 통해 [!DNL Analytics] 를 시각적 보고 소스로 사용할 수도 있습니다. 다음을 참조하십시오 [7단계: 모든 사이트 페이지에서 at.js 참조](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) 위치: *Analytics for Target 구현* 추가 정보.

## 공유 대상

을(를) 채우는 동안 [Marketing Cloud 통합 프로비저닝 양식](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}, 다음에 대한 중요한 정보를 숙지하십시오. [!UICONTROL 공유 대상자] &quot; 아래에 나열된 옵션[!UICONTROL 프로비저닝을 요청하는 기능]?&quot;

![요청 양식](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

요청 시 [!UICONTROL 공유 대상자]를 활성화하면 [!UICONTROL Target] 및 [!UICONTROL Adobe Audience Manager] (AAM) 정보를 공유합니다. 이 경우 대상자.

>[!IMPORTANT]
>
>이 통합 [!UICONTROL Target] 그리고 AAM에는 추가 비용이 있습니다. 각각에 대해 청구됩니다. [!UICONTROL Target] AAM을 호출합니다.
