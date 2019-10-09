---
description: Adobe Target의 Node.js SDK와 관련된 릴리스 노트
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
seo-description: Adobe Target의 서버측 API와 관련된 릴리스 노트입니다.
seo-title: Adobe Target의 Node.js SDK와 관련된 릴리스 노트입니다.
solution: Target
title: 릴리스 노트 - Target Node.js SDK
topic: Standard
translation-type: tm+mt
source-git-commit: 434b103cee15e2e3efdb53febe15c689b5ccd48e

---


# 릴리스 노트 - Target Node.js SDK

Adobe Target의 [Node.js SDK와 관련된 릴리스 노트입니다](https://github.com/adobe/target-nodejs-sdk).

## 버전 1.0.0(2019년 10월 9일)

다음 섹션에서는 Target Node.js SDK 버전 1.0.0에 대한 자세한 정보를 제공합니다.

### Admin Console 도움말에

* Target View Delivery v1 API 지원(페이지 로드 및 미리 보기 프리페치 포함).
* VEC(Visual Experience Composer)에서 제작한 모든 유형의 오퍼를 제공할 수 있도록 지원합니다.
* 프리페치된 컨텐츠를 캐싱하여 성능 최적화를 위한 프리페치 및 알림 기능을 지원합니다.
* 서버측 및 클라이언트측에서 모두 배포되는 [!DNL Target] 경우 하이브리드 `serverState` [!DNL Target] 통합에서 성능을 최적화하기 위한 지원을 제공합니다.

   서버측을 통해 검색되는 경험이 `serverState` 포함된 설정이라는 설정을 소개합니다. 따라서 at.js v2.2+는 경험을 검색할 추가 서버 호출을 하지 않습니다. 이 방법은 페이지 로드 성능을 최적화합니다.

* GitHub에서 Target Node.js [SDK로 소싱된 파일을 엽니다](https://github.com/adobe/target-nodejs-sdk).
* getOffers()를 통해 프리페치된 컨텐츠에 [대해 표시/클릭한 알림을 전송하기 위한 새로운](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications) sendNotifications() API 메서드 [!DNL Target][](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers).
* 기본(예: `request.id``request.context`등)으로 내부 필드 자동 완성 기능을 사용하는 간편한 배달 API 요청 작성.
* SDK API 메서드 인수의 유효성 검사.
* README, 샘플 및 단위 테스트가 업데이트되었습니다.
* GitHub 동작을 사용하여 새로운 CI 흐름을 설정할 수 있습니다.
* CoC, 기여도 지침, PR 및 발행물 템플릿이 추가되었습니다.

### 변경됨

* 프로젝트 이름이 로 `target-nodejs-sdk`변경되었습니다.
* 주요 리팩토링, Target BatchMbox v2 API를 Target View Delivery v1 API로 바꿉니다.
* [create() API 메서드](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) 인수가 수정되어 중복되는 중첩을 제거했습니다( [여기에서](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)이전 메서드 선언 참조).
* [getOffers() API 메서드](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) 인수가 수정되었습니다( [여기에서](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)이전 메서드 선언 참조).
* API `getTargetCookieName()` 메서드가 `TargetCookieName` 접근자로 대체되었습니다. TargetClient [유틸리티 접근자를](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)참조하십시오.
* API `getTargetLocationHintCookieName()` 메서드가 `TargetLocationHintCookieName` 접근자로 대체되었습니다.  TargetClient [유틸리티 접근자를](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)참조하십시오.

### 제거됨

* Target BatchMbox v2 API 지원.
* getOffer() API [메서드가](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) 제거되었습니다. 대신 [getOffers() API 메서드를](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) 사용하십시오.

