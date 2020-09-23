---
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
description: Adobe Target의 서버측 API와 관련된 릴리스 노트입니다.
title: Adobe Target의 Node.js SDK와 관련된 릴리스 노트입니다.
feature: release notes
topic: Standard
translation-type: tm+mt
source-git-commit: 21c49efb4b5de0ae14215712f4ec87b4759f29e1
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---


# 릴리스 노트 - Target Node.js SDK

Adobe Target의 [Node.js SDK와 관련된 릴리스 노트입니다](https://github.com/adobe/target-nodejs-sdk).

Target Node.js SDK를 사용하면 [!DNL Target] 서버측을 배포할 수 있습니다.

이 Node.js SDK는 [!DNL Target] , [!DNL Adobe Experience Cloud] 및 [!DNL Adobe Experience Cloud Identity Service]같은 다른 [!DNL Adobe Analytics]솔루션과 쉽게 통합되도록 도와줍니다 [!DNL Adobe Audience Manager].

Node.js SDK는 Adobe 전달 API를 [!DNL Target] 통해 통합할 때 비즈니스 로직에 집중할 수 있도록 모범 사례를 도입하고 복잡성을 제거합니다.

Adobe 기술 블로그 - 새 Adobe Target 노드.js SDK의 [오픈 소싱에 대한 자세한 내용을 살펴보십시오](https://medium.com/adobetech/open-sourcing-the-new-adobe-target-node-js-sdk-b6feafd828bc).

## 버전 1.0.0(2019년 10월 9일)

다음 섹션에서는 Target Node.js SDK의 버전 1.0.0에 대한 자세한 정보를 제공합니다.

### Admin Console 도움말에

* 페이지 로드 및 프리페치 보기를 비롯한 Target 보기 배달 v1 API 지원.
* VEC(Visual Experience Composer)에서 제작된 모든 유형의 오퍼를 전달하기 위한 완벽한 지원
* 프리페치된 컨텐츠를 캐시하여 성능 최적화를 위한 프리페치 및 알림 지원
* 서버측 및 클라이언트측에서 모두 배포되는 경우 [!DNL Target] 를 통해 하이브리드 `serverState` 통합에서 성능 최적화 [!DNL Target] 를 지원합니다.

   서버 측을 통해 검색된 경험이 들어 있는 &#39; `serverState` 서버 측&#39;이라는 설정이 도입되어 at.js v2.2+에서는 경험을 검색할 추가 서버 호출을 하지 않습니다. 이 방법은 페이지 로드 성능을 최적화합니다.

* GitHub에서 [Target Node.js SDK로 소스를 엽니다](https://github.com/adobe/target-nodejs-sdk).
* getOffers()를 통해 프리페치된 컨텐츠에 [대해 표시/클릭한 알림을 전송하기 위한 새로운](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclientsendnotifications) sendNotifications() API 메서드 [!DNL Target][입니다](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclientsendnotifications).
* 내부 필드 자동 완성, 기본값(예:, `request.id``request.context`등)이 있는 간단한 보기 배달 API 요청 작성.
* SDK API 메서드 인수의 유효성 검사.
* 업데이트된 README, 샘플 및 유닛 테스트.
* GitHub 동작을 사용하여 새로운 CI 흐름을 설정할 수 있습니다.
* CoC, 기여도 지침, PR 및 발행물 템플릿 추가

### 변경

* 프로젝트의 이름이 로 변경되었습니다 `target-nodejs-sdk`.
* Target BatchMbox v2 API를 Target 보기 배달 v1 API로 대체하는 주요 리팩토링
* [create() API 메서드](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclientcreate) 인수가 수정되어 중복된 중첩을 제거합니다( [여기](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)에서 이전 메서드 선언 참조).
* [getOffers() API 메서드](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclientgetoffers) 인수가 수정되었습니다( [여기에서](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)이전 메서드 선언 참조).
* API `getTargetCookieName()` 메서드가 접근자로 `TargetCookieName` 대체되었습니다. TargetClient [유틸리티 접근자를 참조하십시오](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclient-utility-accessors).
* API `getTargetLocationHintCookieName()` 메서드가 접근자로 `TargetLocationHintCookieName` 대체되었습니다.  TargetClient [유틸리티 접근자를 참조하십시오](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclient-utility-accessors).

### 제거됨

* Target BatchMbox v2 API 지원.
* getOffer() [API 메서드가](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) 제거되었습니다. 대신 [getOffers() API 메서드를](https://github.com/adobe/target-nodejs-sdk/blob/master/README.md#targetclientgetoffers) 사용하십시오.

