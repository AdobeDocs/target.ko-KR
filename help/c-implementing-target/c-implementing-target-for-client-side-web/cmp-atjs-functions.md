---
description: at.js와 함께 사용할 수 있는 함수 목록입니다.
keywords: adobe.target.notification;요소;선택기;알림;확장 프로그램
seo-description: Adobe Target의 at.js JavaScript 라이브러리와 함께 사용할 수 있는 함수 목록.
seo-title: Adobe Target at.js 함수
solution: Target
subtopic: 시작하기
title: at.js 함수
topic: Standard
uuid: ec5f27a7-b22a-48c9-968c-9eb02830a2a6
translation-type: tm+mt
source-git-commit: c607b241afb535f324cd1357c8784a88fb183658

---


# at.js 함수{#at-js-functions}를 참조하십시오

Adobe Target at.js JavaScript 라이브러리와 함께 사용할 수 있는 함수 목록. 자세한 내용 및 예는 함수 열의 링크를 클릭합니다.

| 함수 | 세부 사항 |
| --- | --- | 
| [adobe.target.getOffer(옵션)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | 이 함수는 Target 오퍼를 가져오는 요청을 실행합니다. `adobe.target.applyOffer()`와 함께 사용하여 응답을 처리하거나 자체적인 성공 처리를 사용할 수 있습니다. |
| [Adobe. target. getoffer (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at. js 2. x) | 이 함수를 사용하면 여러 mbox를 전달하여 여러 오퍼를 검색할 수 있습니다. 또한 활성 활동의 모든 보기에 대해 여러 오퍼를 검색할 수 있습니다.<br>**참고:** 이 함수는 at. js 2. x에서 소개되었습니다. 이 함수는. js 버전 1에서 사용할 수 없습니다.*x*에는 사용할 수 없습니다. |
| [adobe.target.applyOffer(옵션)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | 이 함수는 응답 컨텐츠를 적용하는 데 사용됩니다. |
| [adobe. target. applyoffers (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at. js 2. x) | 이 함수를 사용하면 adobe. target. getoffers () 에 의해 검색된 오퍼를 두 개 이상 적용할 수 있습니다.<br>**참고:** 이 함수는 at. js 2. x에서 소개되었습니다. 이 함수는. js 버전 1에서 사용할 수 없습니다.*x*에는 사용할 수 없습니다. |
| [adobe. target. triggerview (viewname, options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at. js 2. x) | 이 함수는 새 페이지를 로드할 때마다 또는 페이지의 구성 요소가 다시 렌더링될 때 호출할 수 있습니다.<br> Visual Experience Composer (VEC) 를 사용하여 A/B 테스트 및 경험 타깃팅 (XT) 활동을 만들려면 단일 페이지 애플리케이션 (SPAS) 에 대해 이 함수를 구현해야 합니다. |
| [adobe.target.trackEvent(옵션)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | 이 함수는 클릭 및 전환과 같은 사용자 작업을 보고하라는 요청을 실행하며, 응답에 있는 활동을 전달하지는 않습니다. |
| [Mboxcreate (mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at. js 1. x) | 요청을 실행하고 mboxDefault 클래스 이름을 사용하는 가장 가까운 DIV에 오퍼를 적용합니다.<br>**참고:** 이 함수는. js 버전 1에서 사용할 수 있습니다.*x*에만 사용할 수 있습니다. 이 함수는 at. js 2. x의 릴리스에서 더 이상 사용되지 않습니다. 이 함수는. js 2. x와 함께 사용되는 경우 기본 컨텐트를 반환합니다. |
| [Mboxdefine (options) 및 mboxupdate (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at. js 1. x) | mbox를 정의하고 업데이트합니다.<br>**참고:** 이 함수는. js 버전 1에서 사용할 수 있습니다.*x*에만 사용할 수 있습니다. 이 함수는 at. js 2. x의 릴리스에서 더 이상 사용되지 않습니다. 이 함수는. js 2. x와 함께 사용되는 경우 기본 컨텐트를 반환합니다. |
| [Targetglobalsettings (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Target Standard/Premium UI에서 설정을 구성하지 `targetGlobalSettings()`않고 REST API를 사용하여 at. js 라이브러리의 설정을 무시할 수 있습니다.<ul><li>데이터 공급자: 이 설정을 사용하면 고객은 Demandbase, bluekai 및 사용자 지정 서비스와 같은 타사 데이터 공급자의 데이터를 수집하고 이 데이터를 전달하여 글로벌 mbox 요청에서 mbox 매개 변수로 Target를 전달할 수 있습니다.</li></ul> |
| [Targetpageparams (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | 이 방법을 사용하면 요청 코드의 외부에서 글로벌 mbox에 매개 변수를 첨부할 수 있습니다. |
| [Targetpageparamsall (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | 이 방법을 사용하면 요청 코드의 외부에서 모든 mbox에 매개 변수를 첨부할 수 있습니다. |
| [Registerextension (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at. js 1. x) | 특정 확장 기능을 등록하는 표준 방법을 제공합니다.<br>**참고:** 이 함수는. js 버전 1에서 사용할 수 있습니다.*x*에만 사용할 수 있습니다. 이 함수는 at. js 2. x의 릴리스에서 더 이상 사용되지 않습니다. 이 함수는. js 2. x와 함께 사용되는 경우 기본 컨텐트를 반환합니다. |
| [at.js 사용자 지정 이벤트](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | at. js 사용자 지정 이벤트를 사용하면 mbox 요청 또는 오퍼가 성공하거나 실패할 때를 알 수 있습니다. |
