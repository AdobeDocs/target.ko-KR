---
keywords: Recommendations
description: Analytics에 대한 구현 요구 사항 알아보기 [!DNL Target] (A4T) 및 이 통합을 구현하기 전에 고려해야 할 사항.
title: A4T를 구현하기 전에 무엇을 알아야 합니까?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 9a1603cbbe773638693f5836b6cf7c62dc0b56b8
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 26%

---

# at.js.로 Analytics for Target (A4T)을 구현하기 전

활성화 시 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다 [!DNL Adobe Analytics] 를 [!DNL Adobe Target] (A4T).

이 통합을 사용하기 전에 다음 섹션을 검토하고 보고 프로세스에 미치는 영향을 고려하십시오.

>[!NOTE]
>
>이 문서는 at.js 구현에만 적용됩니다.

## 구현 요구 사항 {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정이 통합용으로 프로비저닝되도록 요청해야 합니다. 를 사용하십시오 [Marketing Cloud 통합 프로비저닝 양식](https://www.adobe.com/go/audiences_kr) 프로비저닝을 요청 합니다.

이 A4T 통합에서는 A4T와 함께 리디렉션 오퍼를 사용할지 여부에 따라 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다.

>[!NOTE]
>
>다음 요구 사항은 다음과 같습니다 *최소* A4T를 구현하는 데 필요한 at.js 버전. 다음 [!DNL Target] 팀에서는 두 버전만 유지 관리합니다 [!DNL at.js]- 현재 버전 및 두 번째 최신 버전입니다. 지원되는 버전을 실행 중인지 확인하려면 [!DNL at.js]를 필요에 따라 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)을 참조하십시오.

### A4T에서 리디렉션 오퍼를 사용하지 *않을* 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하지 않을 경우, 이 A4T 통합을 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 1.8.0
* [!DNL Adobe Target]: at.js  버전 0.9.1
* Adobe Analytics: appMeasurement.js 버전 1.7.0

### A4T에서 리디렉션 오퍼를 사용할 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 2.3.0

   >[!NOTE]
   >
   >at.js 1.8.0+ 및 at.js 2.x+는 Adobe Audience Manager(AAM) 매개 변수 전달에 대해 더 이상 2.5.0 이전 버전의 방문자 API와 동작하지 않습니다.

* [!DNL Adobe Target]: at.js  버전 1.6.2

* Adobe Analytics: appMeasurement.js 버전 2.1

다운로드 및 배포 지침은 [Analytics for Target 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## 구현하기 전에 알아야 할 사항 {#section_50D49CC52E11414089C89FB67F9B88F5}

* 사용하도록 선택하면 이 통합을 새 활동에 사용할 수 있습니다 [!DNL Analytics] 를 보고 소스로 사용 이 문서에 설명된 대로 구현을 변경해도 기존 활동에는 영향을 주지 않습니다.
* 설정 프로세스 [!DNL Analytics] 를 [!DNL Target] 에는 몇 가지 구현 단계와 프로비저닝 단계가 순서대로 포함됩니다. 구현을 시작하기 전에 아래 설명된 프로세스를 자세히 읽어 보십시오. 이 단계를 완료하면 다음을 사용할 수 있습니다 [!DNL Analytics] 을 사용가능으로 설정한 경우 제공 프로세스는 업무일 기준으로 5일 정도 걸릴 수 있습니다.
* 다음 [!DNL Visitor ID service] 공유 만들기 [!DNL Visitor ID] 건너편 [!DNL Adobe Experience Cloud]. 이 변수는 [!DNL Target] mboxPC id 또는 [!DNL Audience Manager] UUID로 대체됩니다 [!DNL Analytics] 새 방문자를 식별합니다. 제대로 설정되면 재방문 [!DNL Analytics] 방문자는 이전 버전도 통해 식별되어야 합니다 [!DNL Analytics] ID. 마찬가지로 [!DNL Target] mboxPCid가 그대로 유지되며 아무 것도 표시되지 않습니다 [!DNL Target] 방문자 프로필 데이터는 로 업그레이드할 때 손실됩니다 [!DNL Visitor ID service].
* 다음 [!DNL Visitor ID service] 먼저 실행해야 함 [!DNL Analytics] 및 [!DNL Target] 페이지 코드. 확인 `VisitorAPI.js` 은 기타 모든 태그의 태그 위에 표시됩니다 [!DNL Experience Cloud] 솔루션.

## 지연 {#section_9489BE6FD21641A4844E591711E3F813}

이 통합이 활성화되면에서 5~10분의 추가 지연이 발생합니다. [!DNL Analytics]. 추가적인 지연 시간으로 인해 [!DNL Analytics] 및 [!DNL Target] 동일한 히트에 저장되므로 페이지 및 사이트 섹션별로 활동을 분류할 수 있습니다.

이 증가는 모두 반영되었습니다 [!DNL Analytics] 라이브 스트림 및 실시간 보고를 포함한 서비스 및 도구는 다음 시나리오에 적용됩니다.

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표, 종결된 데이터 및 데이터 피드에 대한 현재 데이터의 경우, 모든 히트는 5~7분 더 지연됩니다.

지연 증가는 를 구현하면 시작됩니다 [!DNL Experience Cloud] 이 통합을 완전히 구현하지 않았더라도 방문자 ID 서비스.

## 보충 ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

모두 [!DNL Target] 컨텐츠를 전달하거나 목표 지표를 기록하기 위해 A4T 활동에서 사용하는 호출에는 해당 값이 있어야 합니다 [!DNL Analytics] a4T에 대한 보조 ID가 제대로 작동하도록 해당 히트가 수정되었습니다.

의 데이터가 포함된 히트 수 [!DNL Analytics] 및 [!DNL Target] 추가 데이터 ID를 포함합니다. 이 ID는 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) 로서의 `sdid` 매개 변수. 예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. 이 ID는 다음 기준이 충족될 때 생성됩니다.

* 방문자 ID 서비스가 구현됨

When [문제 해결](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)를 설치한 경우 보조 ID가 [!DNL Analytics] 히트 수.

## 클라이언트 측 분석 로깅 {#client-side}

at.js를 사용 중이라면 [!DNL Experience Cloud Visitor ID Service], 및 appMeasurement.js는 페이지에 있습니다. [!DNL Analytics], 및 [!DNL Target] 페이지에 올바른 보충 ID가 포함되어 있으면 백엔드에서 보고 및 분석 목적을 위해 이벤트를 올바르게 결합할 수 있습니다. A4T가 제대로 작동하도록 하기 위해 추가 작업을 관리 및 수행할 필요가 없습니다.

와 관련된 분석 데이터를 언제, 어떻게 로 보낼 것인지를 세부적으로 제어하려는 경우도 있습니다 [!DNL Target] to [!DNL Analytics] 참조하십시오. 내부 용도로 사용하는 사내 분석 도구가 있을 수 있습니다. 그러나 분석 데이터를에 보내려 합니다 [!DNL Analytics] 내부 analytics 제품을 통해 조직의 다른 구성원이 계속 사용할 수 있도록 합니다 [!DNL Analytics] 를 시각적 보고 소스로 사용 자세한 내용은 [7단계: 모든 사이트 페이지에서 at.js 참조](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics for Target 구현* 추가 정보.

## 공유 대상

을 채우는 동안 [Marketing Cloud 통합 프로비저닝 양식](https://www.adobe.com/go/audiences)를 사용하는 경우 [!UICONTROL 공유 대상] 아래에 나열된 옵션[!UICONTROL 프로비전을 요청하는 기능]?

![요청 양식](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

요청 시 [!UICONTROL 공유 대상], 활성화 [!UICONTROL Target] 및 [!UICONTROL Adobe Audience Manager] (AAM) 을 사용하여 정보를 공유할 수 있습니다(이 경우 대상).

>[!IMPORTANT]
>
>이 통합 [!UICONTROL Target] 그리고 AAM은 추가 비용을 제공합니다. 요금은 각 항목에 대해 청구됩니다 [!UICONTROL Target] AAM에서 를 호출합니다.
