---
description: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
keywords: 서버 측;서버측;api;sdk;node.js;nodejs;노드 js;recommendations api;api:apis
seo-description: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
seo-title: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
solution: Target
title: '서버 측: Target 구현'
topic: 권장 사항
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: afec96b2bec18048ab7132232711d2c14769c46c

---


# 서버 측: Target 구현{#server-side-implement-target}

서버측 전달 API, Node.js SDK 및 API에 대한 [!DNL Adobe Target] [!DNL Target Recommendations] 정보입니다.

다음 프로세스는 [!DNL Target]의 서버 측 구현 시 발생합니다.

1. 클라이언트 장치는 서버를 통해 경험을 요청합니다.
1. 서버가 해당 요청을 [!DNL Target]에 전송합니다.
1. [!DNL Target]에서 응답을 다시 서버로 전송합니다.
1. 서버가 클라이언트 장치에 제공할 경험을 결정합니다.

브라우저에 경험을 표시할 필요가 없습니다. 이 경험은 이메일 또는 키오스크, 음성 지원, 기타 비시각적 경험 또는 비브라우저 기반 장치를 통해 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다.

다음 섹션에서는 다양한 API 및 NodeJS SDK에 대한 자세한 정보를 제공합니다.

## 서버 측 배달 API

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Delivery API를 [!DNL Target] 통해 다음을 수행할 수 있습니다.

* SPA, 모바일 채널 등 웹뿐만 아니라 연결된 TV, 키오스크 또는 매장 내 디지털 화면과 같은 비브라우저 기반의 IoT 디바이스까지 경험을 전달할 수 있습니다.
* HTTP/s 호출을 수행할 수 있는 서버측 플랫폼 또는 애플리케이션에서 경험을 제공할 수 있습니다.
* 방문자가 비즈니스에 참여하는 데 사용한 채널 또는 디바이스에 상관없이 방문자에게 일관되고 개인화된 경험을 제공할 수 있습니다.
* 여러 API 호출을 방지할 수 있도록 서버의 세션 내에서 방문자에 대한 경험을 캐시하여 성능을 향상시킵니다.
* AAM( [!DNL Adobe Experience Cloud][!DNL Adobe Analytics]AAM) 및 서버측의 제품과 원활하게 통합됩니다 [!DNL Adobe Audience Manager] [!DNL Experience Cloud ID Service] .

## Node.js SDK

링크:Node.js [SDK](https://github.com/adobe/target-nodejs-sdk)

Node.js SDK는 쿠키, 세션, [!DNL Experience Cloud][!DNL Analytics]및 [!DNL Experience Cloud Visitor ID Service]같은 [!DNL Audience Manager]제품과 통합하는 복잡성을 제거하는 정교한 소프트웨어 개발 키트입니다. 백그라운드에서 Node.js SDK는 API를 `/rest/v1/delivery` 사용합니다. 다음은 Node.js SDK 파섹

* **** 캐싱을 통해 성능을 최적화할 수 있는 프리페치 및 알림 지원:Node.js SDK를 사용하여 Node.js 서버에 대한 서버 호출을 최소화하고 애플리케이션 성능을 최적화하기 위한 목적으로 경험을 검색하고 Node.js 서버에 로컬로 캐시할 [!DNL Target] 수 있습니다.
* **** VEC에서 만든 활동을 검색할 수 있는 기능:서버측에서 VEC에서 만든 활동을 검색합니다. VEC에서 만든 활동이 포함된 응답에는 개인화해야 하는 페이지 부분만 미리 숨기는 데 사용할 수 있는 선택기가 있습니다. 이를 통해 Google PageRank [시스템에서 높은 점수를 얻기 위해 비즈니스에 중요한 KPI인 페이지의 첫 번째 컨텐츠 페인트 지표를](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)최적화할 [수 있습니다](https://en.wikipedia.org/wiki/PageRank) .

## Target Java SDK

Java SDK는 쿠키, 세션 관리 및 [!DNL Adobe Experience Cloud] 솔루션(예: [!DNL Adobe Analytics]및 [!DNL Experience Cloud Visitor ID Service][!DNL Adobe Audience Manager])과의 통합에 대한 복잡성을 해소해주는 정교한 소프트웨어 개발 키트입니다. 백그라운드에서 Java SDK는 API를 `/rest/v1/delivery` 사용합니다. 다음은 Java SDK에서 지원되는 몇 가지 주목할 만한 기능입니다.

* **캐싱을**&#x200B;통해 성능을 최적화할 수 있는 프리페치 및 알림 지원:서버 호출을 최소화하고 애플리케이션 성능을 최적화하기 위해 JavaSDK를 사용하여 경험을 검색하고 Java 서버에 로컬로 캐시할 [!DNL Target] 수 있습니다.
* **VEC에서 만든 활동을**&#x200B;검색하는 기능:서버측에서 VEC에서 만든 활동을 검색합니다. VEC에서 만든 활동이 포함된 응답에는 개인화해야 하는 페이지 부분만 미리 숨기는 데 사용할 수 있는 선택기가 있습니다. 이를 통해 Google PageRank [시스템에서 높은 점수를](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) 얻기 위해 비즈니스에 중요한 KPI인 페이지의 첫 번째 컨텐츠 [페인트 지표를 최적화할](https://en.wikipedia.org/wiki/PageRank) 수 있습니다.

## Target Recommendations API

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
