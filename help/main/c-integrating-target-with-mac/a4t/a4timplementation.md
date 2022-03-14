---
keywords: A4T;Adobe Analytics;Analytics 기반 활동;Analytics 보고서 세트;보고서 세트;Analytics Target 통합;보고서 세트 구성;at.js;atjs;adobe experience platform 웹 sdk;aep 웹 sdk;플랫폼 웹 sdk
description: Analytics를 구현하는 데 필요한 단계를 수행합니다 [!DNL Target] (A4T)를 Adobe에 추가합니다 [!DNL Target] 및 Adobe Analytics 솔루션.
title: Analytics를 구현하려면 어떻게 합니까? [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 23%

---

# [!DNL Target]구현에 대한 분석

구현할 때 몇 가지 단계가 필요합니다 [!DNL Adobe Analytics] 를 [!DNL Adobe Target] (A4T). 프로세스는 A4T를 [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) at.js를 사용하여 또는

## ![Adobe Experience Platform 웹 SDK 배지](/help/main/assets/platform.png) Adobe Experience Platform Web SDK 구현을 위한 구현 단계 {#platform}

다음 섹션에서는 Platform Web SDK를 사용하려는 경우 사이트에 이 통합을 배포하는 데 필요한 단계에 대해 설명합니다.

### 1단계: 프로비저닝 요청 [!DNL Analytics] 및 [!DNL Target]

A4T를 구현하기 전에 [!DNL Analytics] 및 [!DNL Target]. [이 양식을 사용하여 제공을 요청합니다](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES).

### 2단계: 사용자 권한 설정

을 기반으로 활동을 만들려면 먼저 사용자 계정 요구 사항을 충족해야 합니다 [!DNL Analytics] in [!DNL Target]. 자세한 내용은 [사용자 권한 요구 사항 을 참조하십시오](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### 3단계: Edge 구성 만들기

을 사용하여 Edge 구성 만들기 [!DNL Adobe Experience Platform] 모서리 구성 도구 사용. 구성 [[!DNL Analytics] and [!DNL Target] edge 구성 설정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html).

### 4단계: Platform Web SDK 설치 및 구성

게재를 시작하려면 [!DNL Target] 경험 및 적용 [!DNL Analytics] 추적 및 분석 목적으로 [설치](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) 및 [구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) 를 클릭합니다.

### 5단계: A4T 사용 옵션을 활성화합니다

에서 [!DNL Target] UI에서 **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**&#x200B;그런 다음 중 하나를 선택합니다. **[!UICONTROL 활동당 선택]** 또는 **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL 활동당 선택]** 다음 중 하나를 선택할 수 있습니다 [!DNL Target] 및 [!DNL Analytics] 각 활동을 만들 때
* **[!UICONTROL Adobe]**&#x200B;에서는 만들어지는 모든 활동에 대해 [!DNL Analytics]Analytics를 보고 소스로 설정합니다.

## ![at.js 배지](/help/main/assets/atjs.png) at.js 구현을 위한 구현 단계{#section_73961BAD5BB4430A95E073DE5C026277}

다음 섹션에서는 at.js를 사용하려는 경우 사이트에 이 통합을 배포하는 데 필요한 단계에 대해 설명합니다.

### 1단계: Analytics 및 Target 제공 요청

구현 후 [!DNL Analytics] 를 [!DNL Target], 에 대해 프로비저닝되어 있어야 합니다. [!DNL Analytics] 및 [!DNL Target]. [이 양식을 사용하여 제공을 요청합니다](https://www.adobe.com/go/audiences_kr).

### 2단계: 사용자 권한 설정

만들기 전에 사용자 계정 요구 사항을 충족해야 합니다 [!DNL Analytics]의 기반 활동 [!DNL Target]. 자세한 내용은 [사용자 권한 요구 사항 을 참조하십시오](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### 3단계: Experience Cloud 방문자 ID 서비스 구현

방문자 ID 서비스를 통해 [!DNL Adobe Experience Cloud] 솔루션에서 사용자를 식별할 수 있습니다. 필요한 Experience Cloud 방문자 ID 버전을 구현하거나 이 버전으로 마이그레이션하십시오. 자세한 내용은 [구현하기 전에](/help/main/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

자세한 내용은 [Target용 Experience Cloud ID 서비스 구현](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) 에서 *Experience Cloud 방문자 ID 서비스* 설명서.

### 4단계: AppMeasurement for JavaScript 또는 s_code의 AppMeasurement 업데이트

필요한 appMeasurement.js 버전을 구현하거나 이 버전으로 마이그레이션하십시오. 자세한 내용은 [구현하기 전에](/help/main/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

새로운 구현의 경우 다음을 참조하십시오 [JavaScript 구현 개요](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 에서 *Analytics 구현 안내서*.

마이그레이션에 대해서는 [JavaScript용 AppMeasurement로의 마이그레이션](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) 에서 *Analytics 구현 안내서*.

### 5단계: at.js 다운로드 및 업데이트

프로덕션 계정을 사용하여 필요한 at.js 버전을 구현하거나 이 버전으로 마이그레이션하십시오. 이 코드를 수정할 필요가 없습니다.

자세한 내용은 [구현하기 전에](/help/main/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

### 6단계: at.js 호스팅

이전에 at.js를 배포한 경우에는 기존 파일을 업데이트된 버전으로 대체할 수 있습니다. 자세한 내용은 [구현하기 전에](/help/main/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

그렇지 않으면, JavaScript 파일용 AppMeasurement 및 방문자 ID 서비스와 함께 이 파일을 호스트할 수 있습니다. 이러한 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스트되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다.

### 7단계: 모든 사이트 페이지에서 at.js 참조 {#step7}

각 페이지의 태그에 다음 코드 행을 추가하여 VisitorAPI.js 아래에 at.js를 포함합니다.

at.js의 경우:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js는 at.js 앞에 로드해야 합니다. 기존 at.js 파일을 업데이트하는 경우 로드 순서를 확인해야 합니다.

에 대한 기본 설정 [!DNL Target] 및 [!DNL Analytics] 구현 관점에서 통합은 페이지에서 전달되는 SDID를 사용하여 를 연결하는 것입니다 [!DNL Target] 및 [!DNL Analytics] 자동으로 백엔드에서 함께 요청합니다.

와 관련된 분석 데이터를 전송하는 방법 및 시기를 제어할 수 있습니다 [!DNL Target] to [!DNL Analytics] 참조하십시오. 다음과 같은 기본 설정을 사용하지 않으려면 [!DNL Target] 및 [!DNL Analytics] sdid를 통해 analytics 데이터를 자동으로 연결, **analyticsLogging = client_side** via **window.targetGlobalSettings**. 참고: 2.1 이하의 버전은 이 방법을 지원하지 않습니다.

예:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

이 설정에는 전역 효과가 있습니다. 즉, at.js에 의한 모든 호출에는 **analyticsLogging: &quot;client_side&quot;** 전송 [!DNL Target] 모든 요청에 대해 요청 및 analytics 페이로드가 반환됩니다. 이 옵션을 설정하면 반환되는 페이로드의 형식은 다음과 같이 나타납니다.

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

그런 다음 을 통해 페이로드를 Analytics에 전달할 수 있습니다. [데이터 삽입 API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). 자동 할당 및 자동 Target 활동의 경우 sessionId도 전달해야 합니다. 자세한 내용은 [A4T(Target 분석) 보고](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) 에서 *Adobe Target SDK* 안내서.

글로벌 설정을 원하지 않고 더 많은 요구 방식이 필요한 경우 at.js 함수를 사용하십시오 [getOffers()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) 다음을 통해 **analyticsLogging: &quot;client_side&quot;**. Analytics 페이로드는 이 호출에 대해서만 반환되고, [!DNL Target] 백엔드가 페이로드를 [!DNL Analytics]. 이 방법을 사용하여 모든 at.js를 [!DNL Target] 요청은 기본적으로 페이로드를 반환하지만, 대신 원하는 경우 지정된 경우에만 페이로드를 반환합니다.

예:

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

이 호출은 Analytics 페이로드를 추출할 수 있는 응답을 호출합니다.

응답은 다음과 같습니다.

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

그런 다음 페이로드를 [!DNL Analytics] 사용 [데이터 삽입 API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### 8단계: 구현의 유효성 검사 {#step8}

JavaScript 라이브러리를 업데이트한 후 페이지를 로드하여 호출의 `mboxMCSDID`[!DNL Target] 매개 변수 값이 page-view 호출의 `sdid`[!DNL Analytics] 매개 변수 값과 일치하는지 확인하십시오.

특히 이러한 값이 호출 순서를 항상 예측할 수 없는 단일 페이지 애플리케이션(SPA)에서 일치하는지 확인하는 것이 중요합니다.

>[!NOTE]
>
>A4T가 올바르게 작동하려면 이러한 값과 일치하는 값이 필요합니다.

### 9단계: (선택 사항) 이전 통합 코드 제거

Adobe은 이전 통합을 제거하여 구현을 단순화하고 시스템 간의 불일치를 처리할 필요가 없도록 권장합니다. 다음을 포함하여 이전 SC에 배포한 모든 코드를 T&amp;T 통합으로 이동할 수 있습니다 `mboxLoadSCPlugin`.

### 10단계: Analytics를 Target의 보고 소스로 사용하기 위한 선택 사항 활성화

in [!DNL Target]를 클릭합니다. **[!UICONTROL 관리 > 시각적 경험 작성기]** 다음 중 하나를 선택합니다. **[!UICONTROL 활동당 선택]** 또는 **[!UICONTROL Adobe Analytics]** 을 클릭하여 옵션을 활성화합니다.

* **[!UICONTROL 활동당 선택]** 다음 중 하나를 선택할 수 있습니다 [!DNL Target] 및 [!DNL Analytics] 각 활동을 만들 때
* **[!UICONTROL Adobe]**&#x200B;에서는 만들어지는 모든 활동에 대해 [!DNL Analytics]Analytics를 보고 소스로 설정합니다.


