---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
title: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
feature: server-side
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 08ad3291a1f981fbc3963ce403bf19849c358b97
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 11%

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

배달 API를 통해 [!DNL Target] 다음을 수행할 수 있습니다.

* SPA, 모바일 채널 등 웹뿐만 아니라 커넥티드 TV, 키오스크 또는 매장 내 디지털 스크린과 같은 비브라우저 기반의 IoT 디바이스까지 경험을 전달할 수 있습니다.
* HTTP/s 호출을 수행할 수 있는 모든 서버측 플랫폼 또는 애플리케이션에서 경험을 제공할 수 있습니다.
* 방문자가 비즈니스에 참여하는 데 사용한 채널 또는 디바이스에 상관없이 방문자에게 일관되고 개인화된 경험을 제공할 수 있습니다.
* 여러 API 호출을 피할 수 있도록 서버의 세션 내에 방문자에 대한 경험을 캐시하여 더 나은 성능을 얻을 수 있습니다.
* 서버 측 [!DNL Adobe Experience Cloud] , [!DNL Adobe Analytics](AAM) [!DNL Adobe Audience Manager] 과 같은 [!DNL Experience Cloud ID Service] 제품과 완벽하게통합할 수 있습니다.

## Node.js SDK

링크: [Node.js SDK](https://github.com/adobe/target-nodejs-sdk)

Node.js SDK는 쿠키, 세션 및 제품 [!DNL Experience Cloud] 과 통합하는 복잡한 작업을 제거하는 정교한 소프트웨어 개발 키트입니다 [!DNL Analytics][!DNL Experience Cloud Visitor ID Service][!DNL Audience Manager]. 백그라운드에서 Node.js SDK는 `/rest/v1/delivery` API를 사용합니다. 다음은 Node.js SDK에서 지원되는 몇 가지 주목할 만한 기능입니다.

* **캐시를 통해 성능을 최적화할 수 있는 프리페치 및 알림 지원:** Node.js SDK를 사용하여 사용자 서버 호출을 최소화하고 애플리케이션 성능을 최적화하기 위한 목적으로 경험을 검색하고 Node.js 서버에 로컬로 캐시할 수 [!DNL Target] 있습니다.
* **VEC에서 만든 활동을 검색하는 기능:** 서버측에서 VEC에서 만든 활동을 검색합니다. VEC에서 만든 활동이 포함된 응답에는 개인화해야 하는 페이지의 일부만을 미리 숨기는 데 사용할 수 있는 선택기가 있습니다. 이를 통해 [Google PageRank](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)시스템에서 높은 점수를 얻을 수 있는 중요한 KPI인 페이지의 [첫 번째 콘텐츠 페인트 지표를](https://en.wikipedia.org/wiki/PageRank) 최적화할 수 있습니다.

## Target Java SDK

링크: [Target Java SDK](https://github.com/adobe/target-java-sdk)

Java SDK는 쿠키, 세션 및 솔루션(예: [!DNL Adobe Experience Cloud] , [!DNL Adobe Analytics], and [!DNL Experience Cloud Visitor ID Service])과 같은 [!DNL Adobe Audience Manager]솔루션을 통합하는 복잡성을 제거하는 정교한 소프트웨어 개발 키트입니다. 백그라운드에서 Java SDK는 `/rest/v1/delivery` API를 사용합니다. 다음은 Java SDK에서 지원되는 몇 가지 주목할 만한 기능입니다.

* **캐시를 통해 성능을 최적화할 수 있는 프리페치 및 알림 지원**:JavaSDK를 사용하여 Java 서버에 대한 서버 호출을 최소화하고 애플리케이션 성능을 최적화할 목적으로 경험을 검색하고 Java 서버에 로컬로 캐시할 수 [!DNL Target] 있습니다.
* **VEC에서 만든 활동을 검색할 수 있는 기능**:서버측에서 VEC에서 만든 활동을 검색합니다. VEC에서 만든 활동이 포함된 응답에는 개인화해야 하는 페이지의 일부만을 미리 숨기는 데 사용할 수 있는 선택기가 있습니다. 이를 통해 [Google PageRank](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) 시스템에서 높은 점수를 얻을 수 있는 중요한 KPI인 페이지의 [첫 번째 콘텐츠 페인트](https://en.wikipedia.org/wiki/PageRank) 지표를 최적화할 수 있습니다.

## Adobe Target 개발자

링크: [Adobe Target 개발자](http://developers.adobetarget.com/)

Adobe Target 개발자 사이트를 통해 클라이언트측 애플리케이션, 서버측 애플리케이션, 모바일 앱, IoT 등을 [!DNL Target] 구현할 수 있습니다. 또한 데이터를 타사 솔루션으로 내보낼 수도 있습니다. [!DNL Target]

## Target Recommendations API

링크: [Target Recommendations API](https://developers.adobetarget.com/api/recommendations) 및 [Adobe Recommendations API 개요](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html).

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
