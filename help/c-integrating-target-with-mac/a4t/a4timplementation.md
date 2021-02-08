---
keywords: A4T;Adobe Analytics;Analytics 기반 활동;Analytics 보고서 세트;보고서 세트;Analytics Target 통합;보고서 세트 구성
description: Adobe Target 및 Adobe Analytics 솔루션에서 A4T(Target)용 Analytics를 구현하는 데 필요한 단계를 수행합니다.
title: Target(A4T)에 대한 분석을 구현하려면 어떻게 합니까?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 47%

---


# Analytics for Target 구현{#analytics-for-target-implementation}

[!DNL Adobe Analytics]을(를) [!DNL Target](A4T)의 보고 소스로 구현할 때에는 몇 가지 단계가 필요합니다.

## 구현 단계 {#section_73961BAD5BB4430A95E073DE5C026277}

다음 섹션에서는 이 통합을 사이트에 배포하는 데 필요한 단계에 대해 설명합니다.

## 1단계: Analytics 및 Target 제공 요청

[!DNL Target]의 보고 소스로 [!DNL Analytics]을(를) 구현한 후에는 [!DNL Analytics] 및 [!DNL Target]에 대한 프로비저닝을 받아야 합니다. [이 양식을 사용하여 제공을 요청합니다](http://www.adobe.com/go/audiences).

## 2단계: 사용자 권한 설정

[!DNL Target]에서 [!DNL Analytics] 기반 활동을 만들려면 사용자 계정 요구 사항을 충족해야 합니다. [사용자 권한 요구 사항](/help/c-integrating-target-with-mac/a4t/account-reqs.md)을 참조하십시오.

## 3단계: Experience Cloud 방문자 ID 서비스 구현

방문자 ID 서비스를 통해 [!DNL Adobe Experience Cloud] 솔루션에서 사용자를 식별할 수 있습니다. 필요한 Experience Cloud 방문자 ID 버전을 구현하거나 이 버전으로 마이그레이션해야 합니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

*Experience Cloud 방문자 ID 서비스* 설명서의 [Target](https://experienceleague.adobe.com/docs/id-service/using/implementation-guides/setup-target.html)에 대한 Experience Cloud ID 서비스 구현을 참조하십시오.

## 4단계: AppMeasurement for JavaScript 또는 s_code의 AppMeasurement 업데이트

필요한 appMeasurement.js 버전을 구현하거나 이 버전으로 마이그레이션해야 합니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

새 구현에 대해서는 *Analytics 구현 안내서*&#x200B;의 [JavaScript 구현 개요](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/javascript-implementation-overview.html)를 참조하십시오.

마이그레이션에 대해서는 *Analytics 구현 안내서*&#x200B;에서 [JavaScript용 AppMeasurement](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html)로 마이그레이션을 참조하십시오.

## 5단계:at.js 다운로드 및 업데이트

프로덕션 계정을 사용하여 필수 버전의 at.js를 구현하거나 마이그레이션해야 합니다. 이 코드를 수정할 필요가 없습니다.

자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

## 6단계:at.js 호스팅

이전에 at.js를 배포한 경우 기존 파일을 업데이트된 버전으로 바꿀 수 있습니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

그렇지 않으면, JavaScript 파일용 AppMeasurement 및 방문자 ID 서비스와 함께 이 파일을 호스트할 수 있습니다. 이러한 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스트되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다.

## 7단계:모든 사이트 페이지 {#step7}의 at.js 참조

각 페이지의 태그에 다음 코드 행을 추가하여 VisitorAPI.js 아래에 at.js를 포함하십시오.

at.js의 경우:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js를 at.js보다 먼저 로드해야 합니다.기존 at.js 또는 mbox.js 파일을 업데이트하는 경우 로드 순서를 확인하십시오.

구현 관점에서 [!DNL Target] 및 [!DNL Analytics] 통합에 대해 기본 설정을 구성하는 방법은 페이지에서 전달된 SDID를 사용하여 [!DNL Target] 및 [!DNL Analytics] 요청을 자동으로 백엔드에서 결합하는 것입니다.

그러나 보고용으로 [!DNL Target]과(와) 관련된 분석 데이터를 [!DNL Analytics]에 전송하는 방법과 시기를 더 잘 제어하고 싶고 [!DNL Target] 및 [!DNL Analytics]이(가) SDID를 통해 분석 데이터를 자동으로 연결하는 기본 설정으로 옵트인하기를 원하지 않는 경우 **analyticsLogging = client_side** 창을 통해 **를 설정할 수 있습니다..targetGlobalSettings**. 참고: 2.1 이하의 버전은 이 방법을 지원하지 않습니다.

예:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

이 설정에는 전역 효과가 있습니다. 즉, at.js에 의한 모든 호출에는 요청 내에 전송된 **analyticsLogging: &quot;client_side&quot;**&#x200B;가 있으며 모든 요청마다 Analytics 페이로드가 반환됩니다. [!DNL Target] 이 기능이 설정되면 반환되는 페이로드의 형식은 다음과 같이 나타납니다.

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

페이로드를 [데이터 삽입 API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)를 통해 Analytics로 전달할 수 있습니다. [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동의 경우 sessionId도 전달해야 합니다. 자세한 내용은 *Adobe Target SDK* 안내서의 [Target(A4T) 보고](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting)을 참조하십시오.

글로벌 설정을 원하지 않고 더 많은 요구 방식이 필요한 경우 at.js 함수 [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)를 사용하면 **analyticsLogging: &quot;client_side&quot;**&#x200B;를 전달하여 이를 수행할 수 있습니다. 이 호출에 대해서만 분석 페이로드가 반환되고 [!DNL Target] 백엔드는 페이로드를 [!DNL Analytics]에 전달하지 않습니다. 이 접근 방식을 추진하면 모든 at.js [!DNL Target] 요청은 기본적으로 페이로드를 반환하지 않고, 대신 원하는 경우에만 지정하고 지정합니다.

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

페이로드를 [데이터 삽입 API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)를 통해 [!DNL Analytics]에 전달할 수 있습니다.

## 8단계: 구현의 유효성 검사 {#step8}

JavaScript 라이브러리를 업데이트한 후 페이지를 로드하여 호출의 `mboxMCSDID`[!DNL Target] 매개 변수 값이 page-view 호출의 `sdid`[!DNL Analytics] 매개 변수 값과 일치하는지 확인하십시오.

이 검사는 호출 순서가 항상 예측 가능하지는 않은 단일 페이지 애플리케이션(SPA)에서 확인하는 데 특히 중요합니다.

**참고:** A4T가 올바로 작동하려면 이 값이 일치해야 합니다.

## 9단계: (선택 사항) 이전 통합 코드 제거

구현을 간소화하고 시스템 간의 불일치를 처리할 필요가 없도록 이전 통합을 제거하는 것이 좋습니다. `mboxLoadSCPlugin`을 비롯하여 이전 SC에 배포한 모든 코드를 T&amp;T 통합으로 이동할 수 있습니다.

## 10단계: Analytics를 Target의 보고 소스로 사용하기 위한 선택 사항 활성화

[!DNL Target]에서 **[!UICONTROL 관리 > Visual Experience Composer]**&#x200B;를 클릭하고 **[!UICONTROL 활동당 선택]** 또는 **[!UICONTROL Adobe Analytics]**&#x200B;을 선택하여 옵션을 활성화합니다.

* **[!UICONTROL 활동당]** 을 선택하면  [!DNL Target] 각 활동을 만들  [!DNL Analytics] 때 중에서 선택할 수 있습니다.
* **[!UICONTROL Adobe]**&#x200B;에서는 만들어지는 모든 활동에 대해 [!DNL Analytics]Analytics를 보고 소스로 설정합니다.

