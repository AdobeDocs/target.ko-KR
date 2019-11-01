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
source-git-commit: 5f05f218e5fdea26827b86cb7fbea05ac6349014

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트: 2019년 10월 31일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target 플랫폼(2019년 10월 31일)

| 기능/향상 | 설명 |
| --- | --- |
| Java SDK | Java [!DNL Target] SDK를 사용하여 [!DNL Target] 서버측을 배포할 수 있습니다. 이 Java SDK를 사용하면 [!DNL Target] 및 [!DNL Adobe Experience Cloud] 같은 다른 솔루션과 쉽게 통합할 수 [!DNL Adobe Experience Cloud Identity Service][!DNL Adobe Analytics][!DNL Adobe Audience Manager]있습니다.<br>Java SDK는 Adobe의 전달 API를 [!DNL Target] 통해 통합할 때 모범 사례를 도입하고 복잡성을 제거하여 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 합니다. 다음은 최신 버전에서 소개된 주요 기능입니다.<ul><li>캐싱을 통해 성능을 최적화할 수 있도록 프리페치 및 알림을 지원합니다.</li><li>웹 페이지와 서버측 모두에서 [!DNL Target] 하이브리드 통합이 있는 경우 성능 최적화를 지원합니다. at.js 2.2가 더 이상 경험을 검색하기 위해 추가 서버 호출을 하지 않도록 서버측을 통해 검색되는 경험이 `serverState` 채워지는 설정이라는 설정을 소개합니다. 이 방법은 페이지 로드 성능을 최적화합니다.</li><li>새로운 배달 API에서 가능한 Java SDK를 통해 VEC에서 생성된 활동 검색 지원</li><li>개발자가 Target Java SDK에 기여할 수 있도록 오픈 [소싱됩니다](https://github.com/adobe/target-java-sdk).</li></ul>자세한 내용은 릴리스 노트 - [Target Java SDK를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md).<br>새로운 Target Java SDK를 사용한 Adobe 기술 블로그 - [서버측 최적화에 대한 자세한 내용을 살펴보십시오](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2). |

## Target Standard/Premium 19.10.2(2019년 10월 31일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 다중 값 속성을 사용한 작업 | 다중 값 필드로 작업하려는 경우가 있습니다. 다음 예를 생각해 보십시오.<ul><li>사용자에게 동영상을 제공합니다. 특정 영화에는 여러 배우가 출연한다.</li><li>콘서트 티켓을 팔아요 지정된 사용자는 여러 개의 즐겨찾기 밴드를 가지고 있습니다.</li><li>옷을 팔아요 셔츠는 여러 크기로 제공됩니다.</li></ul>이러한 시나리오에서 권장 사항을 처리하려면 다중 값 데이터를 Target Recommendations로 전달하고 특수 다중 값 연산자를 사용할 수 있습니다. |

## Target Standard/Premium 20.1.1

Target Standard/Premium 20.1.1 릴리스는 2020년 1월에 제공될 예정입니다. 정확한 날짜, 기능 및 개선 사항은 여기에서 발표될 예정입니다.

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
