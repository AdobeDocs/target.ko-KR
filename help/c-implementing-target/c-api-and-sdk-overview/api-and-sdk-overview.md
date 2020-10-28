---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Adobe Target 서버측 전달 API, SDK 및 Target Recommendations API에 대한 정보입니다.
title: Adobe Target 서버측 전달 API, Node.js SDK 및 Target Recommendations API에 대한 정보입니다.
feature: server-side
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 42ecb1d2eee4b12e4eff3a646e6d596286e01e00
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 20%

---


# 서버 측: Target 구현{#server-side-implement-target}

서버측 전달 API, SDK 및 API에 대한 [!DNL Adobe Target] [!DNL Target Recommendations] 정보입니다.

다음 프로세스는 [!DNL Target]의 서버 측 구현 시 발생합니다.

1. 클라이언트 장치는 서버를 통해 경험을 요청합니다.
1. 서버가 해당 요청을 [!DNL Target]에 전송합니다.
1. [!DNL Target]에서 응답을 다시 서버로 전송합니다.
1. 서버가 클라이언트 장치에 제공할 경험을 결정합니다.

브라우저에 경험을 표시할 필요가 없습니다. 이 경험은 이메일 또는 키오스크, 음성 지원, 기타 비시각적 경험 또는 비브라우저 기반 장치를 통해 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다.

>[!NOTE]
>
>첫 번째 방문자는 클라이언트 쪽에서만 초기화할 수 있습니다. 첫 번째 방문자는 서버측에서 초기화할 *수* 없습니다.

다음 섹션에서는 다양한 API 및 NodeJS SDK에 대한 자세한 정보를 제공합니다.

## 서버 측 배달 API

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

배달 API를 통해 [!DNL Target] 다음을 수행할 수 있습니다.

* 연결된 TV, 키오스크 또는 매장 내 디지털 화면과 같은 브라우저 기반의 IoT 디바이스뿐만 아니라 SPA, 모바일 채널을 비롯한 다양한 웹 채널에 경험을 전달할 수 있습니다.
* HTTP/s 호출을 수행할 수 있는 모든 서버측 플랫폼 또는 애플리케이션에서 경험을 제공할 수 있습니다.
* 방문자가 비즈니스에 참여하는 데 사용한 채널 또는 디바이스에 상관없이 방문자에게 일관되고 개인화된 경험을 제공할 수 있습니다.
* 여러 API 호출을 피할 수 있도록 서버의 세션 내에 방문자에 대한 경험을 캐시하여 더 나은 성능을 얻을 수 있습니다.
* 서버 측 [!DNL Adobe Experience Cloud] , [!DNL Adobe Analytics](AAM) [!DNL Adobe Audience Manager] 과 같은 [!DNL Experience Cloud ID Service] 제품과 완벽하게통합할 수 있습니다.

## 서버측 SDK

링크: [Adobe Target SDK](https://adobetarget-sdks.gitbook.io/docs/)

서버측 [!DNL Adobe Target] SDK 설명서 포털은 원하는 언어로 서버 [!DNL Target] 에 구현하는 데 도움이 됩니다.

## Target Recommendations API

링크: [Target Recommendations API](https://developers.adobetarget.com/api/recommendations) 및 [Adobe Recommendations API 개요](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html).

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
