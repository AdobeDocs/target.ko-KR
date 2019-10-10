---
description: 이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 정보;새 기능;릴리스;업데이트;업데이트;릴리스;개선;개선 사항;수정 사항;버그 수정
seo-description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
seo-title: 'Adobe Target 릴리스 노트(현재) '
solution: Target
title: Target 릴리스 노트(현재)
topic: 권장 사항
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: e11f8dfee9bcdfae530efc75b239f0d7af045005

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

## at.js 버전 2.2 및 1.8(2019년 10월 10일)

| 기능/향상 | 설명 |
| --- | --- |
| at.js 버전 2.2<br><br>및 at.js 버전 1.8 | at.js의 이러한 버전은 다음과 같습니다.<ul><li>웹 페이지에서 Experience Cloud ID 서비스(ECID) v4.4 및 at.js 2.2 또는 at.js 1.8을 모두 사용할 때의 성능이 개선되었습니다.</li><li>이전에는, at.js가 경험을 가져오기 전에 ECID가 두 개의 차단 호출을 수행했습니다. 이는 단일 호출로 감소하여 성능이 크게 향상되었습니다.</li></ul> 이러한 성능 향상을 활용하려면 ECID 라이브러리 v4.4.<br>at.js 2.2와 함께 at.js 2.2 또는 at.js 1.8로 업그레이드하십시오.<ul><li>**serverState**:Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있는 at.js v2.2+에서 사용할 수 있는 설정입니다. 하이브리드 통합이란 클라이언트측에서 at.js v2.2+를 사용하고 서버측에서 제공 API 또는 Target SDK를 모두 사용하여 경험을 전달하는 것을 의미합니다. `serverState` 는 at.js v2.2+를 통해 서버 측에서 가져온 컨텐츠에서 직접 경험을 적용하고 제공되는 페이지의 일부로 클라이언트로 돌아오는 기능을 제공합니다.<br>자세한 내용은 targetGlobalSettings의 "serverState"를 [참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).</li></ul> |

## Target 플랫폼(2019년 10월 9일)

| 기능/향상 | 설명 |
| --- | --- |
| Node.js SDK 버전 1.0 | Target Node.js SDK를 사용하여 Target 서버측을 배포할 수 있습니다.<br>Node.js SDK를 사용하면 Adobe Experience Cloud Identity Service, Adobe Analytics 및 Adobe Audience Manager와 같은 다른 Experience Cloud 솔루션과 Target을 쉽게 통합할 수 있습니다.<br>Node.js SDK는 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 Adobe Target과 통합할 때 모범 사례를 도입하고 복잡성을 제거합니다. 다음은 최신 버전에서 소개된 주요 기능입니다.<ul><li>캐싱을 통해 성능을 최적화할 수 있도록 프리페치 및 알림을 지원합니다.</li><li>웹 페이지와 서버측에서 모두 Target을 혼합하여 통합한 경우 성능 최적화를 지원합니다. at.js 2.2가 더 이상 경험을 검색할 추가 서버 호출을 하지 않도록 서버측을 통해 검색되는 경험이 채워지는 `serverState` 설정이라는 설정을 소개합니다. 이 방법은 페이지 로드 성능을 최적화합니다.</li><li> 새 배달 API에서 가능한 Node.js SDK를 통해 VEC에서 생성된 활동 검색 지원</li><li>개발자가 Node.js SDK에 기여할 수 있도록 오픈 소싱됩니다.</li></ul><br>자세한 내용은 릴리스 [노트 - Target Node.js SDK를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md). |
| 배달 API | 완전히 새로운 전달 API 끝점(/v1/delivery)은 프로덕션에서 사용할 수 있습니다. 주요 기능은 다음과 같습니다.<ul><li>하나 이상의 mbox에 대한 경험을 검색할 수 있는 하나의 끝점입니다.</li><li>API 파섹</li><li>단일 페이지 애플리케이션(SPA) 및 모바일 애플리케이션에 사용되는 보기라는 완전히 새로운 객체를 지원합니다.</li></ul><br>자세한 내용은 릴리스 [정보 - Target 서버측 API를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |

## Target Standard/Premium 19.9.2(2019년 9월 30일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* Visual Experience Composer(VEC)의 리치 텍스트 편집기(RTE)에 대한 보안 업데이트를 포함한 여러 보안 사항이 수정되었습니다. (TGT-35383)
* 이제 A/B 테스트 및 경험 타깃팅 활동에서 DIV(예: P, UL, H1) 이외의 요소에 Recommendations 오퍼를 추가할 수 있습니다. (TGT-34333)
* 이벤트 알림(타겟 UI의 벨 아이콘)은 더 이상 사용할 수 없습니다. 새로운 알림 기능이 곧 제공될 예정입니다.

## Target Standard/Premium 19.9.1(2019년 9월 10일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 엔터프라이즈 권한 | Target 2019년 9월 릴리스에서 엔터프라이즈 권한은 고객에게 다음과 같은 액세스 제어를 제공합니다.<UL><li>통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.</li><li>Adobe I/O 통합에 승인자, 편집자 또는 관찰자 역할을 적용할 수 있습니다.</li></ul>단계별 지침 및 추가 정보는 [작업 공간에 Adobe I/O 통합 액세스 권한을 부여하고 역할 할당](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)을 참조하십시오. |

## 추가 릴리스 노트 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보 - 대상 서버측 API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Adobe Target의 서버측 API와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Adobe Target의 Node.js SDK와 관련된 릴리스 노트입니다. |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Adobe Target at.js JavaScript 라이브러리의 각 버전에 대한 변경 사항에 대한 세부 정보입니다. |
| [mbox.js 버전 세부 정보](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | 이 페이지에는 각 mbox.js 버전에 대한 변경 사항이 표시됩니다.<br>mbox.js 라이브러리가 더 이상 개발되지 않습니다. 모든 고객은 mbox.js에서 at.js로 마이그레이션해야 합니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트 {#section_1BC5F5208DA548E9B4344A0836E4B943}

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](../r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 Experience Cloud [릴리스 노트를 참조하십시오](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
