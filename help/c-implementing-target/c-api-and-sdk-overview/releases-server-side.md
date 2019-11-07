---
keywords: at.js;api;release;updates;apis;sdks;server side;server side;server-side;api;delivery api
description: Adobe Target의 서버측 API와 관련된 릴리스 노트입니다.
title: Adobe Target의 서버측 API와 관련된 릴리스 노트입니다.
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# 릴리스 정보 - 대상 서버측 API

Adobe Target 서버측 [API와 관련된 릴리스 노트입니다](https://developers.adobetarget.com/api/delivery-api/).

## V1/배달(2019년 10월 9일)

완전히 새로운 배달 API 종단점이 출시되었습니다.

* New [documentation](https://developers.adobetarget.com/api/delivery-api/) is available.
* 하나 이상의 mbox에 대한 경험을 검색할 수 있는 하나의 끝점입니다.
* API 파섹

   VEC에서 만든 활동이 포함된 응답에는 개인화해야 하는 페이지 부분만 미리 숨기는 데 사용할 수 있는 선택기가 있습니다. 이를 통해 페이지의 첫 번째 컨텐츠 [페인트 지표를](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)최적화할 수 있습니다. 이는 Google PageRank 시스템에서 높은 점수를 얻기 위한 중요한 KPI [입니다](https://en.wikipedia.org/wiki/PageRank) .

* 단일 페이지 애플리케이션(SPA) 및 [모바일 애플리케이션에](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) [](/help/c-target-mobile-app/target-mobile-app.md)사용되는 보기라는 완전히 새로운 객체를 지원합니다.
* 뷰 및 mbox를 프리페치하여 캐싱을 통해 성능을 최적화할 수 있습니다.
* 프리페치된 보기 및 mbox에 대한 알림 전송을 지원합니다.

>[!IMPORTANT]
>
>기존 [/v1/mbox 및 /v2/batchmbox API 설명서에](https://developers.adobetarget.com/api/legacy-api/index.html) 계속 액세스할 수 있습니다. 하지만 새로운 기능은 새로운 전달 API에서 개발되며 레거시 API로 다시 포팅되지 않습니다.
