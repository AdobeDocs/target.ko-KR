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
source-git-commit: 540367e4c49c712df98dc132bccf4f29b4d6f095

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target 플랫폼(2019년 10월 31일)

| 기능/향상 | 설명 |
| --- | --- |
| Java SDK | Java [!DNL Target] SDK를 사용하여 [!DNL Target] 서버측을 배포할 수 있습니다. 이 Java SDK를 사용하면 [!DNL Target] 및 [!DNL Adobe Experience Cloud] 같은 다른 솔루션과 쉽게 통합할 수 [!DNL Adobe Experience Cloud Identity Service][!DNL Adobe Analytics][!DNL Adobe Audience Manager]있습니다.<br>Java SDK는 Adobe의 전달 API를 [!DNL Target] 통해 통합할 때 모범 사례를 도입하고 복잡성을 제거하여 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 합니다. 다음은 최신 버전에서 소개된 주요 기능입니다.<ul><li>캐싱을 통해 성능을 최적화할 수 있도록 프리페치 및 알림을 지원합니다.</li><li>웹 페이지와 서버측 모두에서 [!DNL Target] 하이브리드 통합이 있는 경우 성능 최적화를 지원합니다. at.js 2.2가 더 이상 경험을 검색하기 위해 추가 서버 호출을 하지 않도록 서버측을 통해 검색되는 경험이 `serverState` 채워지는 설정이라는 설정을 소개합니다. 이 방법은 페이지 로드 성능을 최적화합니다.</li><li>새로운 배달 API에서 가능한 Java SDK를 통해 VEC에서 생성된 활동 검색 지원</li><li>개발자가 Target Java SDK에 기여할 수 있도록 오픈 [소싱됩니다](https://github.com/adobe/target-java-sdk).</li></ul>자세한 내용은 릴리스 노트 - [Target Java SDK를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md). |

## Target Standard/Premium 19.10.2(2019년 10월 31일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 다중 값 속성 | 다중 값 필드로 작업하려는 경우가 있습니다. 다음 예를 생각해 보십시오.<ul><li>사용자에게 동영상을 제공합니다. 특정 영화에는 여러 배우가 출연한다.</li><li>콘서트 티켓을 팔아요 지정된 사용자는 여러 개의 즐겨찾기 밴드를 가지고 있습니다.</li><li>옷을 팔아요 셔츠는 여러 크기로 제공됩니다.</li></ul>이러한 시나리오에서 권장 사항을 처리하려면 다중 값 데이터를 Target Recommendations로 전달하고 특수 다중 값 연산자를 사용할 수 있습니다.<br>자세한 내용은 다중 값 [속성을](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md)사용한 작업을 참조하십시오. |

## Target Standard/Premium 19.10.1(2019년 10월 22일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 사용자 기반 권장<br>사항(2019년 10월 24일) | 각 방문자의 탐색, 보기 및 구매 내역을 기반으로 항목을 권장합니다. 이러한 항목을 일반적으로 "권장"이라고 합니다.<br>이 기준을 사용하면 신규 방문자와 재방문자 모두에게 개인화된 컨텐츠와 경험을 제공할 수 있습니다. 권장 사항 목록은 방문자의 최근 활동에 가중치가 적용되며, 세션 중에 업데이트되며 방문자가 사이트를 탐색할 때 더 개인화됩니다.<br>자세한 내용은 기준/알고리즘의 "사용자 기반 권장 사항" [을 참조하십시오](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

### Adobe Experience Cloud 내비게이션

* 에 로그인하면 [!DNL Adobe Experience Cloud]새 헤더 탐색으로 이동합니다. 맨 위에 검정색 막대가 있는 이전 탐색과 매우 유사해 보이지만 다음과 같은 향상된 기능을 제공합니다.

   * IMS( [!DNL Identity Management System] Easily Switching) 조직 간 또는 다른 솔루션으로 전환
   * 향상된 사용자 도움말:검색 결과에는 [!DNL Target] 제품 설명서의 결과뿐만 아니라 커뮤니티 포럼 및 기타 비디오 컨텐츠가 포함되어 있으므로 더 많은 컨텐츠에 손쉽게 액세스하여 최대한 활용할 수 [!DNL Target]있습니다. 또한 도움말 메뉴에 바로 피드백 메커니즘을 추가하여 [!UICONTROL 문제를] 보고하거나 아이디어를 공유할 수 있습니다.

   * NPS(Net Promoter Score) 피드백 기능이 개선되어 설문 조사 모달 기능이 작업 흐름을 방해하지 않습니다.
   * 로그인 흐름이 개선되었습니다. 이전에는 모든 [!DNL Target] 고객이 헤더의 [!DNL Target] 아이콘을 클릭한 후 Target 랜딩 페이지에 도달했습니다. 이 페이지에서는 고객이 아래 [!DNL Target Standard/Premium]보듯이, [!DNL Search&Promote]또는 [!DNL Recommendations Classic]계속 진행할 수 있도록 했습니다.

      ![랜딩 페이지](/help/r-release-notes/assets/landing.png)

      모든 고객을 위해 이 랜딩 페이지를 제거했습니다. 이제 새 헤더 탐색 막대에서 [!UICONTROL 아이콘을 클릭하면] [!DNL Target] 항상 활동 목록 페이지로 바로 이동합니다.

      를 사용하는 [!DNL Recommendations Classic]경우 솔루션으로 바로 이동하거나 아래와 같이 Recommendations [!UICONTROL 탭에서 만든 짧은 링크를] 이동할 수 있습니다.

      ![Recs Classic 딥 링크](/help/r-release-notes/assets/recs-classic.png)

      사용하는 [!DNL Search&Promote]경우 Search&amp;Promote URL(https://center.atomz.com/center/?ims=1) [로](https://center.atomz.com/center/?ims=1) 직접 이동해야 합니다. The path to reach [!DNL Search&Promote] from in of [!DNL Adobe Target] the inside.

   * 알림은 현재 헤더의 알림 [!DNL Target] 드롭다운에서  사용할 수 없습니다.
   >[!NOTE]
   >
   >이러한 기능은 한 번에 롤아웃되지 않으며 모든 고객에게 롤아웃되지 않습니다. 다음 몇 주 동안 19.10.1(2019년 10월 22일) [!DNL Target Standard/Premium] 릴리스부터 이러한 기능을 제공할 예정입니다.
   >
   >새 내비게이션 막대의 롤아웃의 일부로 일부 URL이 변경된 것을 확인할 수 있습니다. 이전에 책갈피가 표시된 모든 링크는 계속 작동하지만 새 링크를 책갈피로 설정하여 빠르게 열 수 있습니다.

## at.js 버전 2.2 및 1.8(2019년 10월 10일)

| 기능/향상 | 설명 |
| --- | --- |
| at.js 버전 2.2<br><br>및 at.js 버전 1.8 | at.js의 이러한 버전은 다음과 같습니다.<ul><li>웹 페이지에서 Experience Cloud ID 서비스(ECID) v4.4 및 at.js 2.2 또는 at.js 1.8을 모두 사용할 때의 성능이 개선되었습니다.</li><li>이전에는, at.js가 경험을 가져오기 전에 ECID가 두 개의 차단 호출을 수행했습니다. 이는 단일 호출로 감소하여 성능이 크게 향상되었습니다.</li></ul> 이러한 성능 향상을 활용하려면 ECID 라이브러리 v4.4.<br>at.js 2.2와 함께 at.js 2.2 또는 at.js 1.8로 업그레이드하십시오.<ul><li>**serverState**:Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있는 at.js v2.2+에서 사용할 수 있는 설정입니다. 하이브리드 통합이란 클라이언트측에서 at.js v2.2+를 사용하고 서버측에서 제공 API 또는 Target SDK를 모두 사용하여 경험을 전달하는 것을 의미합니다. `serverState` 는 at.js v2.2+를 통해 서버 측에서 가져온 컨텐츠에서 직접 경험을 적용하고 제공되는 페이지의 일부로 클라이언트로 돌아오는 기능을 제공합니다.<br>자세한 내용은 targetGlobalSettings의 "serverState"를 [참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).</li></ul> |

## Target 플랫폼(2019년 10월 9일)

| 기능/향상 | 설명 |
| --- | --- |
| Node.js SDK 버전 1.0 | Target Node.js SDK를 사용하여 Target 서버측을 배포할 수 있습니다.<br>Node.js SDK를 사용하면 Adobe Experience Cloud Identity Service, Adobe Analytics 및 Adobe Audience Manager와 같은 다른 Experience Cloud 솔루션과 Target을 쉽게 통합할 수 있습니다.<br>Node.js SDK는 엔지니어링 팀이 비즈니스 로직에 집중할 수 있도록 Adobe Target과 통합할 때 모범 사례를 도입하고 복잡성을 제거합니다. 다음은 최신 버전에서 소개된 주요 기능입니다.<ul><li>캐싱을 통해 성능을 최적화할 수 있도록 프리페치 및 알림을 지원합니다.</li><li>웹 페이지와 서버측에서 모두 Target을 혼합하여 통합한 경우 성능 최적화를 지원합니다. at.js 2.2가 더 이상 경험을 검색할 추가 서버 호출을 하지 않도록 서버측을 통해 검색되는 경험이 채워지는 `serverState` 설정이라는 설정을 소개합니다. 이 방법은 페이지 로드 성능을 최적화합니다.</li><li> 새 배달 API에서 가능한 Node.js SDK를 통해 VEC에서 생성된 활동 검색 지원</li><li>개발자가 Node.js SDK에 기여할 수 있도록 오픈 소싱됩니다.</li></ul><br>자세한 내용은 릴리스 [노트 - Target Node.js SDK를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md). |
| 배달 API | 완전히 새로운 전달 API 끝점(/v1/delivery)은 프로덕션에서 사용할 수 있습니다. 주요 기능은 다음과 같습니다.<ul><li>하나 이상의 mbox에 대한 경험을 검색할 수 있는 하나의 끝점입니다.</li><li>API 파섹</li><li>단일 페이지 애플리케이션(SPA) 및 모바일 애플리케이션에 사용되는 보기라는 완전히 새로운 객체를 지원합니다.</li></ul><br>자세한 내용은 릴리스 [정보 - Target 서버측 API를 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |

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
