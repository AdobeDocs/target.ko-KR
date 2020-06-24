---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: a6bcaac474927ddd0a14d4cb274c0460e6002a9b
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 15%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2020년 6월 24일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!NOTE]
>
>* **mbox.js 사용 중단**: 2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행 중인 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더: 개발자 채팅에서 Adobe Target mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**: Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.6.1(2020년 7월, 정확한 날짜 TBD)

이 릴리스에는 다음 개선 사항이 포함됩니다.

### Target(A4T) [!UICONTROL 자동 Target] 활동 지원 Analytics

[!UICONTROL 이제 자동 Target] 활동이 Target에 대한 [Analytics을 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t.md).

이 통합은 고급 머신 러닝을 사용하여 고성능의 마케터가 정의한 여러 경험 중에서 선택하여 컨텐츠를 개인화하고 전환율을 높입니다. 자동 타겟은 개별 고객 프로필 및 유사한 프로필을 갖는 이전 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공합니다.

A/B 테스트 활동 [에 사용하기 위해 A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) 를 이미 구현한 경우 모두 설정되어 있습니다.

### [!UICONTROL 관리] 섹션 UI 새로 고침

새로운 기술 스택을 사용하여 전체 [!DNL Target] UI를 점진적으로 재작성하고 있어 향상된 성능을 제공하고 새로운 기능을 출시할 때 필요한 유지 관리 시간을 단축하며 제품 전반의 사용자 경험을 향상시키고 있습니다. 새로 고친 첫 번째 섹션은 [!UICONTROL 설정] 섹션으로서, 이름이 [!UICONTROL 관리로 변경되었습니다].

이 새로 고침의 일부로, 다음과 같은 [!UICONTROL 관리] 섹션의 페이지를 사용하여 많은 작업을 쉽게 수행할 수 있습니다.

* 구현 탭( [!UICONTROL 관리] > 구현)에서 최신 at.js 파일을&#x200B;**** **[!UICONTROL 다운로드합니다]**.
* at.js 설정을 사용자 정의하고 변경 사항을 쉽게 검토할 수 있습니다(**[!UICONTROL 관리]** > **[!UICONTROL 구현]**).
* 기본 통화 및 표준 시간대, 보고에서 제외되도록 IP와 같은 향상된 보고 설정을 수정합니다. (**[!UICONTROL 관리]** > **[!UICONTROL 보고]**)
* 개인 정보 보호를 위해 방문자 IP 주소 난독화(**[!UICONTROL 관리]** > **[!UICONTROL 구현]**)
* Adobe Admin Console(**[!UICONTROL 관리]** > **[!UICONTROL 사용자]**)에서 관리하기 전에 작업 공간당 사용자 및 해당 역할의 기존 사용자 목록을 확인합니다.
* 관리 섹션에서 모든 테이블을 검색하고 [!UICONTROL 필터링합니다] .

중요한 변경 사항은 다음과 같습니다.

* **[!UICONTROL Visual Experience Composer]페이지&#x200B;**: 이 새 페이지(**[!UICONTROL 관리&#x200B;]****[!UICONTROL >]**시각적 경험 컴포저)에서는 다음을 수행할 수 있습니다.

   * VEC에 대한 일반 설정 구성(기본 URL 지정, [!UICONTROL 향상된 경험 작성기]활성화, 혼합 컨텐츠 로드, 활동 흐름 다이어그램에서 경험 스냅샷 생성)
   * 모바일 뷰포트 구성
   * CSS 선택기 구성

* **[!UICONTROL 보고]페이지&#x200B;**: 이 새 페이지(**[!UICONTROL 관리&#x200B;]****[!UICONTROL >]**보고[!DNL Target])에서는 전체[!DNL Target]계정에 적용되는 보고에 사용할 일반 설정을 구성할 수 있습니다.

   사용 가능한 설정은 다음과 같습니다.

   * 보고에 사용할 [!DNL Adobe Experience Cloud] 솔루션
   * 보고에 사용할 표준 시간대
   * 보고에 사용할 통화
   * 보고에서 제외할 IP 주소
   * 보고에서 예상 매출 증가를 표시할지 여부
   * 세부적으로 분류된 우선 순위를 사용할지 여부

* 이전 [!UICONTROL 호스트] 페이지가 두 개의 새 페이지로 분할되었습니다.

   * [!UICONTROL 호스트]
   * [!UICONTROL 환경]

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
