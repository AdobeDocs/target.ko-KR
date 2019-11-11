---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java-sdk
description: Adobe Target의 Java SDK와 관련된 릴리스 노트입니다.
title: Adobe Target의 Java SDK와 관련된 릴리스 노트입니다.
topic: Standard
translation-type: tm+mt
source-git-commit: af0434a14bf9a816366941b9e2108fb8ba7c9d24

---


# 릴리스 노트 - Target Java SDK

Target Java SDK와 관련된 [릴리스 노트입니다](https://github.com/adobe/target-java-sdk).

Java [!DNL Target] SDK를 사용하여 [!DNL Target] 서버측을 배포할 수 있습니다. 이 Java SDK를 사용하면 [!DNL Target] 및 [!DNL Adobe Experience Cloud] 같은 다른 솔루션과 쉽게 통합할 수 [!DNL Adobe Experience Cloud Identity Service][!DNL Adobe Analytics][!DNL Adobe Audience Manager]있습니다.

Java SDK는 Adobe의 전달 API를 [!DNL Target] 통해 통합할 때 모범 사례를 도입하고 복잡성을 제거하여 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 합니다.

새로운 Target Java SDK를 사용한 Adobe 기술 블로그 - [서버측 최적화에 대한 자세한 내용을 살펴보십시오](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## 버전 1.0.1(2019년 11월 11일)

다음 섹션에서는 Target Java SDK의 버전 1.0.1에 대한 자세한 정보를 제공합니다.

### 고정

* 방문자 API 쿠키가 없는 경우에도 Target 요청에서 보충 데이터 ID를 보냅니다.

## 버전 1.0.0(2019년 10월 31일)

다음 섹션에서는 Target Java SDK 버전 1.0.0에 대한 자세한 정보를 제공합니다.

### Admin Console 도움말에

* [Target View Delivery v1 API](https://developers.adobetarget.com/api/delivery-api/) 지원(페이지 로드 및 미리 보기 프리페치 포함)
   * VEC(Visual Experience Composer)에서 제작한 모든 유형의 오퍼를 제공할 수 있도록 지원합니다.
* 프리페치 및 알림을 지원하므로 프리페치 컨텐츠를 캐싱하여 성능을 최적화할 수 있습니다.
* 서버측 및 클라이언트측에서 모두 [!DNL Target] 배포되는 경우, `serverState`[!DNL Target] 이를 통해 하이브리드 통합에서 성능을 최적화하는 기능이 지원됩니다.
   * 서버측을 통해 검색되는 경험이 `serverState` 포함된 설정이라는 설정을 소개합니다. 따라서 at.js v2.2+는 경험을 검색할 추가 서버 호출을 하지 않습니다. 이 방법은 페이지 로드 성능을 최적화합니다.
* Target Java SDK로 GitHub에서 [제공되는 오픈 소스](https://github.com/adobe/target-java-sdk).
* SDK API 메서드 인수의 유효성 검사.
* README, 샘플 및 단위 테스트가 추가되었습니다.
* CoC, 기여도 지침, PR 및 발행물 템플릿이 추가되었습니다.

