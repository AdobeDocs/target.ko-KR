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
source-git-commit: 05ea5145619e0ac629bd93cf11f9d1fae3f376c9

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트: 2019년 10월 17일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target Standard/Premium 19.10.1(2019년 10월 22일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 사용자 기반 권장 사항 | 각 방문자의 탐색, 보기 및 구매 내역을 기반으로 항목을 권장합니다. 이러한 항목을 일반적으로 "권장"이라고 합니다.<br>이 기준을 사용하면 신규 방문자와 재방문자 모두에게 개인화된 컨텐츠와 경험을 제공할 수 있습니다. 권장 사항 목록은 방문자의 최근 활동에 가중치가 적용되며, 세션 중에 업데이트되며 방문자가 사이트를 탐색할 때 더 개인화됩니다. |

### 개선 사항, 수정 사항 및 변경 사항

* 셸의 [!DNL Experience Cloud] 변경 사항.

   Adobe는 모든 [!DNL Experience Cloud] [!DNL Adobe Experience Cloud] 솔루션에서 경험을 통합하고 개선하기 위해 기존 셸(솔루션 상단에 있는 검은색 막대)을 업데이트하고 있습니다.

   현재 워크플로우는 변경되지 않으며, 보기에 간단한 이러한 변경 사항은 작지만 중요한 방식으로 보다 손쉽게 작업할 수 있도록 고안되었습니다.

   에 로그인하면 [!DNL Adobe Experience Cloud]새 셸로 이동합니다. 맨 위에 검정 막대가 있는 이전 셸과 매우 유사해 보이지만 다음과 같은 향상된 기능을 제공합니다.

   * IMS(Identity Management System) 조직 또는 다른 Experience Cloud [!E솔루션으로 보다] 간편하게 전환할 수 있습니다.
   * 향상된 사용자 도움말:검색 결과에는 [!DNL Target] 제품 설명서의 결과뿐만 아니라 커뮤니티 포럼 및 기타 비디오 컨텐츠가 포함되어 있으므로 더 많은 컨텐츠에 손쉽게 액세스하여 최대한 활용할 수 [!DNL Target]있습니다. 또한 도움말 메뉴에 바로 피드백 메커니즘을 추가하여 문제를 보고하거나 아이디어를 공유할 수 있습니다.
   * NPS(순 추천 점수) 기능이 개선되었습니다. 때때로 일부 고객은 우리가 의도한 것보다 더 높은 빈도로 설문 조사를 [!DNL Target] 보았습니다. 또한 작업 흐름을 방해하는 데 사용된 설문 조사 모달 더 이상 방해가 되지 않는 소규모 설문 조사가 되도록 이 기능을 완전히 업데이트했습니다. 또한 새로운 디자인을 통해 설문 조사 빈도를 효과적으로 제어할 수 있습니다.
   * 로그인 흐름이 개선되었습니다. 이전에는 모든 [!DNL Target] 고객이 셸의 [!DNL Target] 아이콘을 클릭한 후 Target 랜딩 페이지에 도달했습니다. 그런 다음 이 페이지에서 고객이 Recommendations Classic [!DNL Target Standard/Premium]또는 [!DN아래와 같이]계속 진행할 수 있도록 [!DNL Search&Promote]했습니다.

      ![랜딩 페이지](/help/r-release-notes/assets/landing.png)

      모든 고객을 위해 이 랜딩 페이지를 제거했습니다. 이제 항상 [!UICONTROL 아이콘을 클릭하여 활동 목록] [!DNL Target] 페이지로 바로 이동합니다.

      를 사용하는 [!DNL Recommendations Classic]경우 솔루션으로 바로 이동하거나 아래와 같이 Recommendations [!UICONTROL 탭에서 만든 짧은 링크를] 이동할 수 있습니다.

      ![Recs Classic 딥 링크](/help/r-release-notes/assets/recs-classic.png)

      사용하는 [!DNL Search&Promote]경우 링크로 직접 이동해야 합니다. The path to reach [!DNL Search&Promote] from in of [!DNL Adobe Target] the inside.
   * 에 [!DNL Target] 대한 알림은 현재 셸의 [!UICONTROL 알림] 드롭다운에서 표시되지 않습니다.
   >[!NOTE]
   >
   >이러한 기능은 한 번에 롤아웃되지 않으며 모든 고객에게 롤아웃되지 않습니다. 다음 며칠 동안 19.10.1(2019년 10월 22 [!DNL Target Standard/Premium] 일) 릴리스를 통해 이러한 기능을 제공할 예정입니다.
   >
   >새 셸의 롤아웃의 일부로, 일부 URL 변경 사항도 확인할 수 있습니다. 이전에 책갈피가 표시된 모든 링크는 계속 작동하지만 새 링크를 책갈피로 설정하여 빠르게 열 수 있습니다.

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
