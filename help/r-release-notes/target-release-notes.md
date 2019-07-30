---
description: 최신 또는 예정된 [! DNL Adobe Target] 릴리스.
keywords: 릴리스 노트
seo-description: 최신 또는 예정된 [! DNL Adobe Target] 릴리스.
seo-title: Adobe Target 릴리스 노트 (베타 버전)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: f49c0c94afe6bf8aadbfb76930b57bf7cd5602dc

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트 날짜: 2019년 7월 24일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target Standard/Premium 19.7.1(2019년 7월 24일) {#tgt-19-7-1}

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 기능 / 개선 사항 | 설명 |
| --- | --- |
| 모바일 앱 시각적 경험 작성기 | 클릭추적을 위해 설정한 요소를 표시하는 새로운 수정 패널이 모바일 앱 VEC에 표시됩니다. (TGT-31741)<br> See [Set up click tracking in the Mobile App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
| ![프리미엄 Badgeresa/B](/help/assets/premium.png)<br>테스트 및 경험 타깃팅 (XT) 활동의 사용자 지정 | Recommendations 오퍼 (알고리즘) 상태는 Recommendations 오퍼가 포함된 A/B 테스트 및 XT 활동에 대한 개요 페이지에 표시됩니다. 상태: 결과 준비, 결과 준비 안 됨 및 피드 실패. (TGT-33649)<br>See [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Experience Cloud ID (ECID) 라이브러리를 통해 at. js 2.0 +에 대한 도메인 간 추적 지원 | 이전에는 도메인 간 추적이. js 2에서 지원되지 않았습니다.*x*&#x200B;에는 사용할 수 없습니다. 이 릴리스를 통해 at. js 2.0 이상을 사용하는 고객은 이제 ECID 라이브러리를 통한 도메인 간 추적을 활용할 수 있습니다. 크로스 도메인 추적을 수행하려면. js 2.0 이상 버전과 함께 페이지에 ECID 라이브러리를 설치해야 합니다. [Experience Cloud ID Library 4.3.0 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) 를 사용해야 합니다.<br>at. js 2. x에서 [도메인 간 추적 지원을 참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Experience Cloud ID (ECID) 라이브러리 4.3를 통해 Apple의 ITP 2.1 및 ITP 2.2에 대한 Target 지원 | 현재 타깃 고객은 Adobe의 CNAME 인증 프로그램을 활용하여 Apple의 ITP 2.1 및 ITP 2.2를 완화할 수 있습니다.<br>이번 릴리스에서는 Target 이 서버측 쿠키를 활용하여 ITP 2.1 및 ITP 2.2를 완화하는 ECID Library 4.3 과의 매끄러운 통합을 도입했습니다. Target 고객은 Target의 JavaScript 라이브러리와 [함께 ECID Library 4.3 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) 를 배포하여 향후 ITP 릴리스를 완화하는 것이 좋습니다. ECID 라이브러리는 브라우저에서 도입된 지속적인 쿠키 정책에 강력한 솔루션을 제공하는 향상된 기능을 지속적으로 출시합니다.<br>[Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)를 참조하십시오. |

## at. js 버전 2.1.1 (2019 년 7 월 24 일)

at. js의 이번 릴리스는 유지 관리 릴리스이며 다음 개선 사항 및 수정 사항을 포함합니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

* Visual Experience Composer (VEC) 의 목표 및 설정 페이지에서 클릭 추적 지표를 사용할 때 여러 개의 비콘이 실행되는 문제를 해결했습니다. (TNT-32812)
* Fixed an issue that caused `triggerView()` to not render offers more than once. (TNT-32780)
* Fixed an issue with `triggerView()` to ensure that the request contains Marketing Cloud ID (MCID) information. (TNT-32776)
* Fixed an issue that prevented the `triggerView()` notification to fire even if there are no saved views. (TNT-32614)
* URL에 잘못된 형식의 쿼리 문자열 매개 변수가 포함될 때 발생하는 decodeuricomponent 사용 오류로 인해 오류가 발생하던 문제를 수정했습니다. (TNT-32710)
* The beacon flag is now set to "true" in the context of delivery requests sent via the `Navigator.sendBeacon()` API. (TNT-32683)
* 일부 고객의 웹 사이트에서 Recommendations 오퍼가 표시되지 않는 문제를 해결했습니다. 고객은 배달 API 호출에서 오퍼 컨텐츠를 볼 수 있지만 오퍼는 웹 사이트에 적용되지 않았습니다. (TNT-32680)
* 여러 경험이 걸쳐 클릭추적이 예상대로 작동되지 않는 문제를 해결했습니다. (TNT-32644)
* 첫 번째 지표 렌더링이 실패한 후 at. js에서 두 번째 지표를 적용하지 못했던 문제를 수정했습니다. (TNT-32628)
* Fixed an issue when passing `mboxThirdPartyId` using the `targetPageParams` function that caused the request payload to not be present in either the query parameters or in the request payload. (TNT-32613)
* Chrome 기반 브라우저 (Google Chrome 포함) 에서 디스플레이 및 클릭 알림 응답이 차단되는 문제를 해결했습니다. (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

**개선 사항, 수정 및 변경 사항**

* 중복 값을 추가할 때 Recommendations 활동의 제외 값이 지워지지 않는 문제를 해결했습니다. (TGT-34996)
* 이제 타깃팅 페이지에서 추천 활동에서 디자인을 제거할 수 있습니다 (3 부분으로 구성된 안내 워크플로우 중 2 단계). 디자인을 제거하려면 두 개 이상의 디자인을 선택해야 합니다. (TGT-35118)
* 일부 고객이 타겟 UI에서 제대로 로드하거나 편집할 수 있도록 사용자 지정 기준 카드가 표시되지 않는 문제를 해결했습니다. (TGT-35170)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
