---
description: 최신 또는 예정된 Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;개선 사항;새 기능;수정 사항;release notes;updates;future release;enhancements;new features;fixes
seo-description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
seo-title: Adobe Target 베타 버전 정보
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 9fa095b910b85f244b626c34cacdf9f4a13a6929

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트: 2019년 10월 2일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## 타겟 플랫폼

| 기능/향상 | 설명 |
| --- | --- |
| Node.js SDK 버전 1.0<br>(2019년 10월 9일) | Target Node.js SDK를 사용하여 Target 서버측을 배포할 수 있습니다.<br>Node.js SDK를 사용하면 Adobe Experience Cloud Identity Service, Adobe Analytics 및 Adobe Audience Manager와 같은 다른 Experience Cloud 솔루션과 Target을 쉽게 통합할 수 있습니다.<br>Node.js SDK는 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 Adobe Target과 통합할 때 모범 사례를 도입하고 복잡성을 제거합니다. 다음은 최신 버전에서 소개된 주요 기능입니다.<ul><li>캐싱을 통해 성능을 최적화할 수 있도록 프리페치 및 알림을 지원합니다.</li><li>웹 페이지와 서버측에서 모두 Target을 혼합하여 통합한 경우 성능 최적화를 지원합니다. at.js 2.2가 더 이상 경험을 검색할 추가 서버 호출을 하지 않도록 서버측을 통해 검색되는 경험이 채워지는 `serverState` 설정이라는 설정을 소개합니다. 이 방법은 페이지 로드 성능을 최적화합니다.</li><li> 새 배달 API에서 가능한 Node.js SDK를 통해 VEC에서 생성된 활동 검색 지원</li><li>개발자가 Node.js SDK에 기여할 수 있도록 오픈 소싱됩니다.</li></ul>자세한 내용은 릴리스 [노트 - Target Node.js SDK를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md). |
| 배달 API<br>(2019년 10월 9일) | 완전히 새로운 전달 API 끝점(/v1/delivery)은 프로덕션에서 사용할 수 있습니다. 주요 기능은 다음과 같습니다.<ul><li>하나 이상의 mbox에 대한 경험을 검색할 수 있는 하나의 끝점입니다.</li><li>API 파섹</li><li>단일 페이지 애플리케이션(SPA) 및 모바일 애플리케이션에 사용되는 보기라는 완전히 새로운 객체를 지원합니다.</li></ul>자세한 내용은 릴리스 [정보 - Target 서버측 API를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |
| at.js 버전 2.2<br><br>and at.js 버전 1.8<br>(확인할 날짜) | at.js의 이러한 버전은 다음과 같습니다.<ul><li>웹 페이지에서 Experience Cloud ID 서비스(ECID) v4.4 및 at.js 2.2 또는 at.js 1.8을 모두 사용할 때의 성능이 개선되었습니다.</li><li>이전에는, at.js가 경험을 가져오기 전에 ECID가 두 개의 차단 호출을 수행했습니다. 이는 단일 호출로 감소하여 성능이 크게 향상되었습니다.</li></ul> 이러한 성능 향상을 활용하려면 ECID 라이브러리 v4.4와 함께 at.js 2.2 또는 at.js 1.8로 업그레이드하십시오. |


## Target Standard/Premium 19.10.1(2019년 10월 22일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 사용자 기반 권장 사항 | 각 방문자의 탐색, 보기 및 구매 내역을 기반으로 항목을 권장합니다. 이러한 항목을 일반적으로 "권장"이라고 합니다.<br>이 기준을 사용하면 신규 방문자와 재방문자 모두에게 개인화된 컨텐츠와 경험을 제공할 수 있습니다. 권장 사항 목록은 방문자의 최근 활동에 가중치가 적용되며, 세션 중에 업데이트되며 방문자가 사이트를 탐색할 때 더 개인화됩니다. |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
