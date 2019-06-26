---
description: Target 서버 측 배달 API, Recommendations API 및 NodeJS SDK에 대한 정보입니다.
keywords: 서버 측;서버 측;api;sdk;nodejs;node js;recommendations api
seo-description: Adobe Target 서버측 배달 API, Recommendations API 및 nodejs SDK에 대한 정보입니다.
seo-title: 서버측 Adobe Target 구현
solution: Target
title: '서버 측: Target 구현'
topic: 권장 사항
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 서버 측: Target 구현{#server-side-implement-target}

[!DNL Adobe Target] 서버측 배달 API, 서버측 일괄전달 API, nodejs SDK, [!DNL Target Recommendations] API 및 [!DNL Target Classic] API (디컴파일) 에 대한 정보입니다.

The following process occurs in a server-side implementation of [!DNL Target]:

1. 클라이언트 장치는 서버를 통해 경험을 요청합니다.
1. Your server sends that request to [!DNL Target].
1. [!DNL Target] 응답을 서버로 다시 전송합니다.
1. 서버가 렌더링하기 위해 클라이언트 장치에 전달할 경험을 결정합니다.

경험은 브라우저에 표시할 필요가 없습니다. 이메일, 키오스크, 음성, 키오스크, 비시각적 또는 비브라우저 기반의 장치를 통해 표시할 수 있습니다. Because your server sits between the client and [!DNL Target], this type of implementation is also ideal if you need greater control and security or have complex backend processes that you want to run on your server.

다음 섹션에서는 여러 API 및 NodeJS SDK를 나열하고 추가 정보를 제공합니다.

## 서버 측 배달 API

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target] 응용 프로그램이 브라우저, 모바일 장치 또는 다른 서버에서 mbox 호출을 만들 수 있도록 해줍니다. The Server Side delivery API is specifically designed to integrate [!DNL Target] with any server-side platform that makes HTTP/HTTPS calls.

You can use the API to integrate your custom application with [!DNL Target]. 이 기능은 스마트 TV, 키오스크 또는 매장 내 디지털 스크린과 같은 브라우저를 기반으로 하지 않는 IoT 장치로 타깃팅을 전달하려는 조직에 특히 중요합니다.

이 엔드포인트는 일반 mbox에 대한 오퍼만 반환할 수 있습니다. 단일 mbox에 대한 컨텐츠만 가져올 수도 있습니다.

이 API는 RESTful 방식으로 기존 mbox 기능을 구현합니다.

이 API는 쿠키를 처리하거나 호출을 리디렉션하지 않습니다.

## 서버 측 배치 배달 API

Link: [Server Side Batch Delivery APIs](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

배치 배달 API를 사용하면 애플리케이션에서 단일 호출로 여러 mbox에 대한 컨텐츠를 요청할 수 있습니다. It also has a prefetch mode that enables clients like mobile apps, servers, and so forth to fetch content for multiple mboxes in one request, cache it locally, and later notify [!DNL Target] when the user visits those mboxes.

이 엔드포인트는 일반 mbox에 대한 오퍼만 반환할 수 있습니다. 여러 mbox에 대한 컨텐츠를 가져올 수 있으므로 성능을 위해 배치 mbox API를 사용하는 것이 적합합니다. 이렇게 하면 비용이 많이 드는 여러 HTTP 요청이 실행되지 않도록 할 수 있습니다.

## NodeJS SDK

Link: [NodeJS SDK](https://www.npmjs.com/package/@adobe/target-node-client)

SDK의 측면에서 현재는 유일한 SDK인 NodeJS SDK가 있습니다.

NodeJS SDK는 NodeJS 코어 HTTP/HTTPS 모듈의 씬 래퍼입니다. NodeJS SDK API는 백그라운드에서 동일한 서버 측 배달 API를 사용합니다.

다음은 매핑입니다.

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] API

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

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

안타깝게도 성능 수치가 없습니다. 그러나 NodeJS 이벤트 주도 아키텍처 덕분에 일반적으로 NodeJS SDK의 성능이 향상됩니다. Be aware that most of the time is spent on the [!DNL Target] backend. NodeJS SDK는 거의 처리하지 않습니다. The SDK is basically responsible for packaging a [!DNL Target] request and parsing a [!DNL Target] response.
