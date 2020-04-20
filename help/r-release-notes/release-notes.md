---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 1befd131034805ba81e4d68e7e976fd290041d52

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!NOTE]
>
>* **mbox.js 사용 중단**:2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하려면 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 마이그레이션할 것을 권장합니다. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Adobe *Target 기술 빌더:개발자 채팅을 통해 Adobe Target의 mbox.js를 아래 at.js로* 마이그레이션하여 이 주제에 대한 향후 개발자 채팅 등록에 대한 정보를 확인하십시오.
   >
   >   
   현재 mbox.js가 지원되지만 2017년 7월 이후로 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외 다른 혜택 중 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고 보안을 향상시키며 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.


괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Adobe Target 스킬 빌더:개발자 채팅, Adobe Target의 mbox.js를 at.js로 마이그레이션 {#skill-builder}

Adobe Target 제품 관리자인 David Son과 함께 mbox.js를 at.js로 마이그레이션하는 것의 이점을 설명합니다. 최신 at.js 업데이트를 듣고, 향상된 기능 및 이러한 기능이 기술 환경의 더 큰 트렌드와 어떻게 일치하는지 알아보고, mbox.js에서 at.js로 마이그레이션할 때 Target에서 많은 가치를 추출할 수 있는 실용적인 팁을 확인하십시오. Adobe Target 개발자는 이러한 기회를 놓치지 않을 것입니다!

5월 5일 화요일, 8:00 - 9:00 AM (PDT)

[지금 등록하십시오!](https://atskillbuilder-devchat.experienceleague.adobeevents.com/)

## at.js 타깃팅(2020년 3월 25일)

다음 새 버전의 Target at.js JavaScript 라이브러리를 사용할 수 있습니다.

* at.js 버전 2.3.0
* at.js 버전 1.8.1

For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Target Standard/Premium 20.2.1(2020년 3월 23일)

>[!IMPORTANT]
>
>mbox.js 사용 중단에 대한 위의 정보를 참조하십시오.

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 카탈로그 검색을 수행할 때 고객이 컬렉션을 선택할 수 없는 문제를 해결했습니다. (TGT-36230)
* API를 통해 생성되었지만 타겟 UI에서 만든 활동에서 참조되지 않는 기준이 UI에서 잘못 삭제되는 문제를 수정했습니다. (TGT-35917)
* CSP(Content Security Policy)에 대한 보안 개선 사항을 구현했습니다. (TGT-36190)
* 속성 가중치 백분율 막대를 왼쪽으로 밀면 &quot;NaN%&quot;가 표시되는 문제를 해결했습니다. (TGT-36211)
* 다양한 언어의 UI 텍스트가 올바로 표시되도록 현지화 문제를 해결했습니다.
* 현재 버전의 Adobe Analytics API에서 지원되지 않는 Adobe Analytics 지표를 비활성화하여 Adobe Analytics for Target(A4T) 활동의 사용 가능한 지표 목록을 표준화했습니다. 이를 통해 향후 Adobe Target 릴리스에서 A4T 지원을 확장할 수 있습니다.

   다음 변경 사항이 적용되었습니다.

   * &quot;페이지에서 보낸 평균 시간&quot;이 &quot;사이트에서 보낸 평균 시간&quot;으로 대체되었습니다. 이 지표를 지표로 사용하는 모든 활동에는 &quot;사이트에서 보낸 평균 시간&quot;이 있습니다(참고:다음 번에 활동이 편집될 때 기본 목표 지표로 선택한 시간(초 단위)입니다.
   * &quot;방문자 수&quot;는 &quot;고유 방문자 수&quot;로 대체되었습니다. 이 지표를 기본 목표 지표로 사용하는 모든 활동은 다음에 활동을 편집할 때 기본 목표 지표로 선택됩니다.

* 다음 지표는 더 이상 사용되지 않으며 새 A4T 활동을 만들 때 기본 목표 지표로 선택할 수 없습니다.

   | 가치 하락 지표 | 제안된 대체 지표 |
   |--- |--- |
   | 일일 방문자, 시간별 방문자, 월별 방문자, 분기별 방문자, 주별 방문자, 연간 방문자 | 고유 방문자 수 |
   | 평균 방문 깊이 | n/a.기본 목표 지표로 제안되지 않음 |
   | 보트 | n/a.기본 목표 지표로 제안되지 않음 |
   | 모바일 충돌 비율, 모바일 평균 이전 세션 길이, 모바일 앱 스토어 평균 등급, 모바일 앱 성능 충돌 비율, 모바일 앱 스토어 평균 등급 | n/a.기본 목표 지표로 제안되지 않음 |

## Adobe Experience Cloud 내비게이션(2019년 2월 22일)

* 에 로그인하면 [!DNL Adobe Experience Cloud]새 헤더 탐색으로 이동합니다. 맨 위에 검정색 막대가 있는 이전 탐색과 매우 유사해 보이지만 다음과 같은 향상된 기능을 제공합니다.

   * IMS( [!DNL Identity Management System] Easily Switching) 조직 간 또는 다른 솔루션으로 전환
   * 향상된 사용자 도움말:검색 결과에는 [!DNL Target] 제품 설명서의 결과뿐만 아니라 커뮤니티 포럼 및 기타 비디오 컨텐츠가 포함되어 있으므로 더 많은 컨텐츠에 손쉽게 액세스하여 최대한 활용할 수 [!DNL Target]있습니다. 또한 도움말 메뉴에 바로 피드백 메커니즘을 추가하여 [!UICONTROL 문제를] 보고하거나 아이디어를 공유할 수 있습니다.

   * NPS(Net Promoter Score) 피드백 기능이 개선되어 설문 조사 모달 기능이 작업 흐름을 방해하지 않습니다.
   * 로그인 흐름이 개선되었습니다. 이전에는 모든 [!DNL Target] 고객이 헤더의 [!DNL Target] 아이콘을 클릭한 후 Target 랜딩 페이지에 도달했습니다. 이 페이지에서는 고객이 아래 [!DNL Target Standard/Premium]보듯이, [!DNL Search&Promote]또는 [!DNL Recommendations Classic]계속 진행할 수 있도록 했습니다.

      ![랜딩 페이지](/help/r-release-notes/assets/landing.png)

      모든 고객을 위해 이 랜딩 페이지를 제거했습니다. 이제 새 헤더 탐색 막대에서 [!UICONTROL 아이콘을 클릭하면] [!DNL Target] 항상 활동 목록 페이지로 바로 이동합니다.

      를 사용하는 [!DNL Recommendations Classic]경우 솔루션으로 바로 이동하거나 아래와 같이 Recommendations [!UICONTROL 탭에서 만든 짧은 링크를] 이동할 수 있습니다.

      ![Recs Classic 딥 링크](/help/r-release-notes/assets/recs-classic.png)

      를 사용하는 [!DNL Search&Promote]경우 Search&amp;Promote URL(https://center.atomz.com/center/?ims=1) [로](https://center.atomz.com/center/?ims=1) 직접 이동해야 합니다. The path to reach [!DNL Search&Promote] from in of [!DNL Adobe Target] the inside.

   * 알림은 현재 헤더의 알림 [!DNL Target] 드롭다운에서  사용할 수 없습니다.
   >[!NOTE]
   >
   >새 내비게이션 막대의 롤아웃의 일부로 일부 URL이 변경된 것을 확인할 수 있습니다. 이전에 책갈피가 표시된 모든 링크는 계속 작동하지만 새 링크를 책갈피로 설정하여 빠르게 열 수 있습니다.

## 추가 릴리스 노트 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보 - 대상 서버측 API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Adobe Target의 서버측 API와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Adobe Target의 Node.js SDK와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Adobe Target의 Java SDK와 관련된 릴리스 노트입니다. |
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
