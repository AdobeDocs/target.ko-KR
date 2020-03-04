---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 669160af359972cace9c298aa061fcfa2af69072

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!NOTE]
>
>* **TLS 지원 변경 사항**:2020년 3월 1일부터 Target은 TLS 1.1 및 TLS 1.0 암호화를 지원하지 않습니다. TLS(전송 계층 보안)는 네트워크를 통해 데이터를 안전하게 교환해야 하는 웹 브라우저 및 애플리케이션에서 현재 사용되는 가장 널리 배포된 보안 프로토콜입니다. 이 변경 사항은 일반적으로 받아들여지는 TLS 1.2 이상의 보안 규정 준수 표준을 충족하기 위해 필요합니다. 현재 사용 중인 TLS 버전을 확인합니다. 버전이 1.2보다 낮은 경우 Target을 예상대로 계속 사용하려면 2020년 3월 1일 이전에 필요한 변경 사항을 구현하십시오.
   >
   >   
   가능한 영향 및 구현을 업데이트하는 데 필요한 단계에 대한 자세한 내용은 TLS(전송 [레이어 보안) 암호화 변경을](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)참조하십시오.
   >
   >
* **mbox.js 사용 중단**:2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하려면 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 마이그레이션할 것을 권장합니다. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   현재 mbox.js가 지원되지만 2017년 7월 이후로 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외 다른 혜택 중 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고 보안을 향상시키며 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.
   >
   >
* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.


## Target Standard/Premium 20.2.1(2020년 3월 3일)

>[!IMPORTANT]
>
>mbox.js 사용 중단에 대한 위의 정보를 참조하십시오.

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 카탈로그 검색을 수행할 때 고객이 컬렉션을 선택할 수 없는 문제를 해결했습니다. (TGT-36230)
* API를 통해 생성되었지만 타겟 UI에서 만든 활동에서 참조되지 않는 기준이 UI에서 잘못 삭제되는 문제를 수정했습니다. (TGT-35917)
* CSP(Content Security Policy)에 대한 보안 개선 사항을 구현했습니다. (TGT-36190)
* 속성 가중치 백분율 막대를 왼쪽으로 밀면 &quot;NaN%&quot;가 표시되는 문제를 해결했습니다. (TGT-36211)
* 다양한 언어의 UI 텍스트가 올바로 표시되도록 현지화 문제를 해결했습니다.
* 다음 Adobe Analytics 지표는 2020년 3월 Target 릴리스부터 Analytics for Target(A4T)에서 더 이상 지원되지 않습니다.
   * averagevisdepth
   * 보트
* 다음 지표는 더 이상 지원되지 않으며 사용자가 지표를 포함하는 활동을 처음 수정할 때 동일한 지표의 새 버전으로 자동 변환됩니다.

   | 가치 하락 지표 | 새 지표 |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (참고:초 대신 분 단위 측정) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

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
