---
description: Target 서버 측 배달 API, Recommendations API 및 NodeJS SDK에 대한 정보입니다.
keywords: 서버 측;서버측;api;sdk;nodejs;node js;recommendations api
seo-description: Adobe Target 서버측 배달 API, Recommendations API 및 nodejs SDK에 대한 정보입니다.
seo-title: 서버측 Adobe Target 구현
solution: Target
title: '서버 측: Target 구현'
topic: 권장 사항
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 385864d9daae19468c4557e51043d5b788924658

---


# 서버 측: Target 구현{#server-side-implement-target}

[!DNL Adobe Target] 서버측 배달 API, 서버측 일괄전달 API, nodejs SDK, [!DNL Target Recommendations] API 및 [!DNL Target Classic] API (디컴파일) 에 대한 정보입니다.

다음 프로세스는 다음 서버 [!DNL Target]측 구현에서 발생합니다.

1. 클라이언트 장치는 서버를 통해 경험을 요청합니다.
1. 서버가 해당 요청을 [!DNL Target]전송합니다.
1. [!DNL Target] 응답을 서버로 다시 전송합니다.
1. 서버가 렌더링하기 위해 클라이언트 장치에 전달할 경험을 결정합니다.

경험은 브라우저에 표시할 필요가 없습니다. 이메일, 키오스크, 음성, 키오스크, 비시각적 또는 비브라우저 기반의 장치를 통해 표시할 수 있습니다. 서버가 클라이언트와 클라이언트 사이에 [!DNL Target]존재하기 때문에 이러한 유형의 구현도 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이상적입니다.

다음 섹션에서는 여러 API 및 NodeJS SDK를 나열하고 추가 정보를 제공합니다.

## 서버 측 배달 API

Link: [서버측 배달 API](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target] 응용 프로그램이 브라우저, 모바일 장치 또는 다른 서버에서 mbox 호출을 만들 수 있도록 해줍니다. 서버측 전달 API는 HTTP/HTTPS 호출을 수행하는 서버측 플랫폼과 통합되도록 [!DNL Target] 특별히 설계되었습니다.

API를 사용하여 사용자 지정 애플리케이션을 [!DNL Target]통합할 수 있습니다. 이 기능은 스마트 TV, 키오스크 또는 매장 내 디지털 스크린과 같은 브라우저를 기반으로 하지 않는 IoT 장치로 타깃팅을 전달하려는 조직에 특히 중요합니다.

이 엔드포인트는 일반 mbox에 대한 오퍼만 반환할 수 있습니다. 단일 mbox에 대한 컨텐츠만 가져올 수도 있습니다.

이 API는 RESTful 방식으로 기존 mbox 기능을 구현합니다.

이 API는 쿠키를 처리하거나 호출을 리디렉션하지 않습니다.

## 서버 측 배치 배달 API

Link: [서버측 일괄 배달 API](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

배치 배달 API를 사용하면 애플리케이션에서 단일 호출로 여러 mbox에 대한 컨텐츠를 요청할 수 있습니다. 또한 모바일 앱, 서버 등의 클라이언트가 한 요청에서 여러 mbox에 대한 컨텐츠를 가져오고, 로컬에 캐시하고, 사용자가 이러한 mbox를 방문할 때 알림을 받을 [!DNL Target] 수 있도록 해주는 프리페치 모드도 있습니다.

이 엔드포인트는 일반 mbox에 대한 오퍼만 반환할 수 있습니다. 여러 mbox에 대한 컨텐츠를 가져올 수 있으므로 성능을 위해 배치 mbox API를 사용하는 것이 적합합니다. 이렇게 하면 비용이 많이 드는 여러 HTTP 요청이 실행되지 않도록 할 수 있습니다.

## NodeJS SDK

Link: [Nodejs SDK](https://www.npmjs.com/package/@adobe/target-node-client)

SDK의 측면에서 현재는 유일한 SDK인 NodeJS SDK가 있습니다.

NodeJS SDK는 NodeJS 코어 HTTP/HTTPS 모듈의 씬 래퍼입니다. NodeJS SDK API는 백그라운드에서 동일한 서버 측 배달 API를 사용합니다.

다음은 매핑입니다.

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] API

Link: [Target Recommendations API](https://developers.adobetarget.com/api/recommendations)

Recommendations API를 사용하면 Target의 Recommendations 서버와 프로그래밍 방식으로 상호 작용할 수 있습니다. 이러한 API는 일반적으로 사용자 인터페이스를 통해 이루어지는 기능을 수행하기 위해 애플리케이션 스택의 범위와 통합될 수 있습니다.

## [!DNL Target Classic] API

[!DNL Target Classic] UI 및 API가 해체되었습니다. Target의 최신 API로 전환하는 방법에 대한 자세한 내용은 [Target 레거시 API에서 Adobe I/O로 전환](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2)을 참조하십시오.

>[!NOTE]
>활동, 오퍼, 대상 등을 만드는 작성 API는 CORS(원본 간 리소스 공유)를 지원하지 않습니다.

## 서버 측 배달 API와 NodeJS SDK의 차이 {#section_10336B7934F54CE98E35907A4748A4A4}

많은 고객이 서버 측 배달 API와 NodeJS SDK의 차이점을 혼동하고 있습니다. 특히 성능과 관련하여 더욱 그렇습니다.

다음 FAQ는 사용할 것을 결정하는 데 도움이 됩니다.

**&quot;원시&quot; 서버 측 API와 NodeJS SDK는 언제 사용해야 합니까?**

NodeJS를 백엔드 기술로 사용하는 경우에는 NodeJS SDK를 선택하는 것이 좋습니다. SDK는 쿠키, 헤더, 페이로드 등과 같은 여러 세부 사항을 처리합니다. 이 경우 애플리케이션의 핵심에 초점을 맞출 수 있습니다.

**NodeJS SDK를 사용하여 성능을 향상해야 합니까?**

안타깝게도 성능 수치가 없습니다. 그러나 NodeJS 이벤트 주도 아키텍처 덕분에 일반적으로 NodeJS SDK의 성능이 향상됩니다. 대부분의 시간은 [!DNL Target] 백엔드에서 사용됩니다. NodeJS SDK는 거의 처리하지 않습니다. SDK는 기본적으로 [!DNL Target] 요청을 패키지화하고 [!DNL Target] 응답을 구문 분석합니다.
