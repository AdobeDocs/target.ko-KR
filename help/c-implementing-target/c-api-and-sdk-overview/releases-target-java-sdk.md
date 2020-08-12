---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Adobe Target의 Java SDK와 관련된 릴리스 노트입니다.
title: Adobe Target의 Java SDK와 관련된 릴리스 노트입니다.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# 릴리스 노트 - Target Java SDK

Target Java [SDK와 관련된 릴리스 노트입니다](https://github.com/adobe/target-java-sdk).

Java SDK를 사용하여 [!DNL Target] [!DNL Target] 서버측을 배포할 수 있습니다. 이 Java SDK를 사용하면 [!DNL Target] , [!DNL Adobe Experience Cloud] 및 [!DNL Adobe Experience Cloud Identity Service]같은 다른 [!DNL Adobe Analytics]솔루션과 손쉽게 통합할 수 있습니다 [!DNL Adobe Audience Manager].

Java SDK는 Adobe 전달 API를 [!DNL Target] 통해 통합할 때 모범 사례를 도입하고 복잡성을 제거하여 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 합니다.

새로운 Target Java SDK를 사용한 Adobe 기술 블로그 - [서버측 최적화의 Target Java SDK에 대해 자세히 알아보십시오](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## 버전 1.1.0(2019년 12월 16일)

다음 섹션에서는 Target Java SDK의 버전 1.1.0에 대한 자세한 정보를 제공합니다.

### Admin Console 도움말에

* @hisham-hassan의 오픈 소스 기여도로 인해 프록시 구성에 대한 지원이 추가되었습니다.

## 버전 1.0.1(2019년 11월 11일)

다음 섹션에서는 Target Java SDK의 버전 1.0.1에 대한 자세한 정보를 제공합니다.

### 고정

* 방문자 API 쿠키가 없는 경우에도 보충 데이터 ID를 Target 요청에 전송합니다.

## 버전 1.0.0(2019년 10월 31일)

다음 섹션에서는 Target Java SDK의 버전 1.0.0에 대한 자세한 정보를 제공합니다.

### Admin Console 도움말에

* [페이지 로드 및 프리페치 보기를 비롯한 Target 보기 배달 v1 API](https://developers.adobetarget.com/api/delivery-api/) 지원.
   * VEC(Visual Experience Composer)에서 제작된 모든 유형의 오퍼를 전달하기 위한 완벽한 지원
* 프리페치된 컨텐츠를 캐싱하여 성능 최적화를 허용하는 프리페치 및 알림 지원
* 서버측 및 클라이언트측에서 모두 배포되는 경우 [!DNL Target] 를 통해 하이브리드 `serverState`통합에서 성능을 최적화하는 [!DNL Target] 지원
   * 서버 측을 통해 검색된 경험이 들어 있는 &#39; `serverState` 서버 측&#39;이라는 설정이 도입되어 at.js v2.2+에서는 경험을 검색할 추가 서버 호출을 하지 않습니다. 이 방법은 페이지 로드 성능을 최적화합니다.
* GitHub에서 [Target Java SDK로 소스를 엽니다](https://github.com/adobe/target-java-sdk).
* SDK API 메서드 인수의 유효성 검사.
* README, 샘플 및 단위 테스트가 추가되었습니다.
* CoC, 기여도 지침, PR 및 발행물 템플릿이 추가되었습니다.

