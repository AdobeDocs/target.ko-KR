---
keywords: at.js;함수;javascript 라이브러리
description: Adobe Target에서 at.js JavaScript 라이브러리의 1.x 및 2.x 버전과 함께 사용할 수 있는 함수 목록을 봅니다.
title: at.js에서 사용할 수 있는 함수는 무엇입니까?
feature: at.js
role: Developer
exl-id: a386e478-16f4-4bf6-9771-6b1e75f2e362
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 78%

---

# at.js 함수

Adobe Target at.js JavaScript 라이브러리와 함께 사용할 수 있는 함수 목록. 자세한 내용 및 예를 보려면 함수 열의 링크를 클릭합니다.

| 함수 | 세부 사항 |
| --- | --- | 
| [adobe.target.getOffer(옵션)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/) | 이 함수는 Target 오퍼를 가져오는 요청을 실행합니다. `adobe.target.applyOffer()`와 함께 사용하여 응답을 처리하거나 자체적인 성공 처리를 사용할 수 있습니다. |
| [adobe.target.getOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/)<br>(at.js 2.x) | 이 함수를 사용하면 여러 mbox를 전달하여 여러 오퍼를 검색할 수 있습니다. 또한 활성 활동의 모든 보기에 대해 여러 오퍼를 검색할 수 있습니다.<br>**참고:** 이 함수는 at.js 2.x에서 도입되었으며, at.js 버전 1.*x*&#x200B;에는 사용할 수 없습니다. |
| [adobe.target.applyOffer(옵션)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/) | 이 함수는 응답 콘텐츠를 적용하는 데 사용됩니다. |
| [adobe.target.applyOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffers-atjs-2/)<br>(at.js 2.x) | 이 함수를 사용하면 adobe.target.getOffers()로 검색된 오퍼를 두 개 이상 적용할 수 있습니다.<br>**참고:** 이 함수는 at.js 2.x에서 도입되었으며, at.js 버전 1.*x*&#x200B;에는 사용할 수 없습니다. |
| [adobe.target.triggerView (viewName, options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-triggerview-atjs-2/)<br>(at.js 2.x) | 이 함수는 새 페이지를 로드할 때마다 또는 페이지의 구성 요소가 다시 렌더링될 때 호출할 수 있습니다.<br> VEC(시각적 경험 작성기)를 사용하여 A/B 테스트 및 경험 타깃팅(XT) 활동을 만들려면 SPA(단일 페이지 애플리케이션)에 대해 이 함수를 구현해야 합니다. |
| [adobe.target.trackEvent(옵션)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-trackevent/) | 이 함수는 클릭 및 전환과 같은 사용자 작업을 보고하라는 요청을 실행하며, 응답에 있는 활동을 전달하지는 않습니다. |
| [mboxCreate(mbox,params)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxcreate-atjs/)<br>(at.js 1.x) | 요청을 실행하고 mboxDefault 클래스 이름을 사용하는 가장 가까운 DIV에 오퍼를 적용합니다.<br>**참고:** 이 함수는 at.js 버전 1.*x*&#x200B;에만 사용할 수 있습니다. 이 함수는 at.js 2.x의 릴리스에서 더 이상 사용되지 않으며, at.js 2.x에서 사용하는 경우 기본 콘텐츠를 반환합니다. |
| [mboxDefine(options) 및 mboxUpdate(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxdefine-mboxupdate-atjs-1x/)<br>(at.js 1.x) | mbox를 정의하고 업데이트합니다.<br>**참고:** 이 함수는 at.js 버전 1.*x*&#x200B;에만 사용할 수 있습니다. 이 함수는 at.js 2.x의 릴리스에서 더 이상 사용되지 않으며, at.js 2.x에서 사용하는 경우 기본 콘텐츠를 반환합니다. |
| [targetGlobalSettings(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) | Target Standard/Premium UI에서 설정을 구성하거나 REST API를 사용하는 대신 `targetGlobalSettings()`를 사용하여 at.js 라이브러리의 설정을 재정의할 수 있습니다.<ul><li>데이터 공급자: 이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 타사 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다.</li></ul> |
| [targetPageParams(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/) | 이 방법을 사용하면 요청 코드의 외부에서 글로벌 mbox에 매개 변수를 첨부할 수 있습니다. |
| [targetPageParamsAll(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparamsall/) | 이 방법을 사용하면 요청 코드의 외부에서 모든 mbox에 매개 변수를 첨부할 수 있습니다. |
| [registerExtension(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/registerextension-atjs-1x/)<br>(at.js 1.x) | 특정 확장 기능을 등록하는 표준 방법을 제공합니다.<br>**참고:** 이 함수는 at.js 버전 1.*x*&#x200B;에만 사용할 수 있습니다. 이 함수는 at.js 2.x의 릴리스에서 더 이상 사용되지 않으며, at.js 2.x에서 사용하는 경우 기본 콘텐츠를 반환합니다. |
| [at.js 사용자 지정 이벤트](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-custom-events/) | at.js 사용자 지정 이벤트는 mbox 요청 또는 오퍼가 실패하거나 성공하면 알려줍니다. |
| [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/)<br>(at.js 2.1.0) | 이 함수는 `adobe.target.applyOffer()` 또는 `adobe.target.applyOffers()`를 사용하지 않고 경험을 렌더링할 때 Target Edge에 알림을 보냅니다.<br>**참고**: 이 함수는 at.js 2.1.0에서 처음 소개되었으며, 2.1.0 이상 버전에서 사용할 수 있습니다. |