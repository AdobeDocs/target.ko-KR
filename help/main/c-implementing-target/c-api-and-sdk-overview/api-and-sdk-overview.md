---
keywords: 서버 측;서버 측;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Adobe에 대해 알아보기 [!DNL Target] 서버 측 배달 API, SDK 및 [!DNL Target] Recommendations API.
title: 어디에서 배울 수 있습니까 [!DNL Target] 서버 측 배달 API 및 SDK는 무엇입니까?
feature: Implement Server-side
role: Developer
exl-id: cdee007f-f54d-4cf3-9575-6319da3434a5
source-git-commit: db288fbb4ddf011b7051257fdc8126d1158c8469
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 23%

---

# 서버 측: Target 구현

정보 [!DNL Adobe Target] 서버 측 배달 API, SDK 및 [!DNL Target Recommendations] API.

다음 프로세스는 [!DNL Target]의 서버 측 구현 시 발생합니다.

1. 클라이언트 장치는 서버를 통해 경험을 요청합니다.
1. 서버가 해당 요청을 [!DNL Target]에 전송합니다.
1. [!DNL Target]에서 응답을 다시 서버로 전송합니다.
1. 서버가 렌더링하기 위해 클라이언트 장치에 전달할 경험을 결정합니다.

경험은 브라우저에 표시될 필요가 없습니다. 경험은 음성 도우미를 통해 또는 시각적이지 않은 경험 또는 브라우저를 기반으로 하지 않는 장치를 통해 이메일이나 키오스크에 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다.

>[!NOTE]
>
>첫 번째 방문자는 클라이언트측에서만 초기화할 수 있습니다. 처음 방문자 *사용할 수 없음* 서버 측에서 초기화됩니다.

다음 섹션에서는 다양한 API 및 NodeJS SDK에 대한 자세한 정보를 제공합니다.

## 서버 측 배달 API

링크: [서버 측 배달 API](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

사용 [!DNL Target] 배달 API를 사용하여 다음을 수행할 수 있습니다.

* 연결된 TV, 키오스크 또는 매장 내 디지털 스크린과 같은 비브라우저 기반 IoT 장치뿐만 아니라 SPA 및 모바일 채널을 포함한 웹 전반에 경험을 제공합니다.
* HTTP/s를 호출할 수 있는 서버측 플랫폼 또는 애플리케이션에서 경험을 제공합니다.
* 방문자가 비즈니스를 수행하는 데 사용한 채널 또는 장치에 상관없이 방문자에게 일관되고 개인화된 경험을 제공합니다.
* 서버의 세션 내에 방문자에 대한 경험을 캐시하여 여러 API 호출을 방지할 수 있으므로 성능이 향상됩니다.
* 와 원활하게 통합 [!DNL Adobe Experience Cloud] 와 같은 제품 [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) 및 [!DNL Experience Cloud ID Service] 를 반환합니다.

## 서버 측 SDK

링크: [Adobe Target SDK](https://adobetarget-sdks.gitbook.io/docs/)

다음 [!DNL Adobe Target] 서버측 SDK 설명서 포털은 [!DNL Target] 원하는 언어로 서버에 연결할 수 있습니다.

## Target Recommendations API

링크: [Recommendations API Target](https://developers.adobetarget.com/api/recommendations) 및 [Adobe Recommendations API 개요](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Recommendations API를 사용하면 프로그래밍 방식으로 와 상호 작용할 수 있습니다 [!DNL Target] 권장 사항 서버. 이러한 API는 다양한 애플리케이션 스택과 통합하여 일반적으로 [!DNL Target] 사용자 인터페이스.
