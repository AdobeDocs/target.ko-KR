---
keywords: Recommendations
description: Analytics for [!DNL Target] (A4T)에 대한 구현 요구 사항과 이 통합을 구현하기 전에 고려해야 할 사항을 알아봅니다.
title: A4T를 구현하기 전에 무엇을 알아야 합니까?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 27%

---

# at.js로 타겟 (A4T) 에 대한 분석을 구현하기 전

[!DNL Adobe Target](A4T)의 보고 소스로 [!DNL Adobe Analytics]을(를) 설정할 때 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다.

이 통합을 사용하기 전에 다음 섹션을 검토하고 보고 프로세스에 미치는 영향을 고려하십시오.

>[!NOTE]
>
>이 문서는 at.js 구현에만 적용됩니다.

## 구현 요구 사항 {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정이 통합용으로 프로비저닝되도록 요청해야 합니다. [Marketing Cloud 통합 프로비저닝 양식](https://www.adobe.com/go/audiences_kr)을 사용하여 제공을 요청하십시오.

이 A4T 통합에서는 A4T와 함께 리디렉션 오퍼를 사용할지 여부에 따라 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다.

### A4T에서 리디렉션 오퍼를 사용하지 *않을* 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하지 않을 경우, 이 A4T 통합을 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 1.8.0
* [!DNL Adobe Target]: at.js  버전 0.9.1
* Adobe Analytics: appMeasurement.js 버전 1.7.0

### A4T에서 리디렉션 오퍼를 사용할 경우 필요한 요구 사항

A4T와 함께 리디렉션 오퍼를 사용하려면 다음 라이브러리 버전(또는 그 이상)을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js 버전 2.3.0

   **참고:**  at.js 1.8.0 이상 버전은 더 이상  [!DNL Adobe Audience Manager] (AAM) 매개 변수를 전달하기 위해 2.5.0 이전 버전의 방문자 API에서 작동하지 않습니다.

* [!DNL Adobe Target]: at.js  버전 1.6.2

* Adobe Analytics: appMeasurement.js 버전 2.1

다운로드 및 배포 지침은 [Target 구현을 위한 Analytics](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)에 나열되어 있습니다.

## 구현하기 전에 알아야 할 사항 {#section_50D49CC52E11414089C89FB67F9B88F5}

* [!DNL Analytics] 을 보고 소스로 사용하도록 선택하면 이 통합을 새 활동에 사용할 수 있습니다. 이 문서에 설명된 대로 구현을 변경해도 기존 활동에는 영향을 주지 않습니다.
* [!DNL Target]에 대한 보고 소스로 [!DNL Analytics]을 설정하는 프로세스에는 몇 가지 구현 단계가 포함되며 그 뒤에는 프로비저닝 단계가 옵니다. 구현을 시작하기 전에 아래 설명된 프로세스를 자세히 읽어 보십시오. 이 단계를 완료하면 활성화되었을 때 보고 소스로 [!DNL Analytics] 을 사용할 준비가 되었습니다. 제공 프로세스는 업무일 기준으로 5일 정도 걸릴 수 있습니다.
* [!DNL Visitor ID service]은 [!DNL Adobe Experience Cloud]에 걸쳐 공유 [!DNL Visitor ID]을 만듭니다. 이 ID는 [!DNL Target] mboxPC ID 또는 [!DNL Audience Manager] UUID를 대체하지 않지만 [!DNL Analytics] 가 새 방문자를 식별하는 방식은 대체되지 않습니다. 제대로 설정되면 반환 [!DNL Analytics] 방문자도 이전 [!DNL Analytics] ID를 통해 식별되어야 합니다. 마찬가지로 [!DNL Target] mboxPCid가 그대로 유지되므로 [!DNL Visitor ID service] 로 업그레이드할 때 [!DNL Target] 방문자 프로필 데이터가 손실되지 않습니다.
* [!DNL Visitor ID service]은 [!DNL Analytics] 및 [!DNL Target] 페이지 코드 앞에서 실행해야 합니다. `VisitorAPI.js`이 다른 모든 [!DNL Experience Cloud] 솔루션의 태그 위에 표시되어야 합니다.

## 지연 {#section_9489BE6FD21641A4844E591711E3F813}

이 통합이 활성화되면 [!DNL Analytics]에서 5~-10분 동안 지연이 추가로 발생할 수 있습니다. 추가적인 지연 시간으로 인해 [!DNL Analytics] 및 [!DNL Target] 의 데이터가 동일한 히트에 저장되므로 활동을 페이지 및 사이트 섹션별로 분류할 수 있습니다.

이러한 증가는 라이브 스트림 및 실시간 보고를 포함하여 모든 [!DNL Analytics] 서비스 및 도구에 반영되며 다음 시나리오에 적용됩니다.

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표, 종결된 데이터 및 데이터 피드에 대한 현재 데이터의 경우, 모든 히트는 5~7분 더 지연됩니다.

이 통합을 완전히 구현하지 않았더라도 [!DNL Experience Cloud] 방문자 ID 서비스를 구현하면 추가적인 지연 시간이 발생하기 시작합니다.

## 보충 ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

컨텐츠를 전달하거나 목표 지표를 기록하기 위해 A4T 활동에서 사용하는 모든 [!DNL Target] 호출에는 A4T가 제대로 작동하도록 보충 ID를 공유하는 해당 [!DNL Analytics] 히트가 있어야 합니다.

[!DNL Analytics] 및 [!DNL Target]의 데이터가 포함된 히트에 보충 데이터 ID가 들어 있습니다. 이 ID는 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)에서 `sdid` 매개 변수로 표시됩니다. 예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. 이 ID는 다음 기준이 충족될 때 생성됩니다.

* 방문자 ID 서비스가 구현됨

[문제 해결](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)에서는 보충 ID가 [!DNL Analytics] 히트에 있는지 확인하십시오.

## 클라이언트 측 분석 로깅 {#client-side}

at.js, [!DNL Experience Cloud Visitor ID Service] 및 appMeasurement.js가 페이지에 있는 경우, 올바른 보충 ID가 페이지에 포함되어 있으면 [!DNL Analytics] 및 [!DNL Target] 는 백엔드에서 보고 및 분석 목적을 위해 이벤트를 올바르게 결합합니다. A4T가 제대로 작동하도록 하기 위해 추가 작업을 관리 및 수행할 필요가 없습니다.

보고 목적으로 [!DNL Target]과 관련된 분석 데이터를 [!DNL Analytics]에 언제, 어떻게 보낼 것인지를 세부적으로 제어하려는 경우도 있습니다. 내부 용도로 사용하는 사내 분석 도구가 있을 수 있습니다. 그러나 사내 분석 제품을 통해 [!DNL Analytics]에 분석 데이터를 전송하여 조직의 다른 구성원이 [!DNL Analytics]을 계속 시각적 보고 소스로 사용할 수 있도록 하려는 경우도 있습니다. [7단계를 참조하십시오. 자세한 내용은 *Target 구현*&#x200B;에서 모든 사이트 페이지](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7)에서 at.js를 참조하십시오.

## 공유 대상

[Marketing Cloud 통합 프로비저닝 양식](https://www.adobe.com/go/audiences)을 채우는 동안 &quot;[!UICONTROL 프로비저닝을 요청하는 기능에 대해 나열된 [!UICONTROL 공유 대상] 옵션에 대한 다음 중요한 정보를 알아 두십시오.&quot;]

![요청 양식](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

[!UICONTROL 공유 대상]을 요청하면, 이 경우 [!UICONTROL Target] 및 [!UICONTROL Adobe Audience Manager](AAM)이 정보를 공유하도록 활성화합니다.

>[!IMPORTANT]
>
>[!UICONTROL Target]과 AAM 간의 이러한 통합은 추가 비용이 발생합니다. AAM의 각 [!UICONTROL Target] 호출에 대해 청구됩니다.
