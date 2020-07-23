---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: fe68bfb124a5c8c58fbc6822d31b49257a0cfc0b
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 14%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2020년 7월 27일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>* **Adobe, 개인화 엔진 부문 Gartner Magic Quadrant에서 리더로 선정**: Adobe는 2020년 발표된 3분기 Gartner Magic Quadrant에서 리더로 선정되었습니다. Gartner Magic Quadrant의 개인화 엔진 평가 결과, 비전의 완전성과 실행 능력. [Adobe 블로그에서 확인할 수 있습니다](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js 사용 중단**: 2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더: 개발자 채팅에서 Adobe Target mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**: Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.7.1(2020년 7월 27일)

이 릴리스에는 다음 개선 사항이 포함됩니다.

### [!UICONTROL 관리] 섹션 UI 새로 고침

새로운 기술 스택을 사용하여 전체 [!DNL Target] UI를 점진적으로 재작성하고 있어 향상된 성능을 제공하고 새로운 기능을 출시할 때 필요한 유지 관리 시간을 단축하며 제품 전반의 사용자 경험을 향상시키고 있습니다. 새로 고친 첫 번째 섹션은 [!UICONTROL 설정] 섹션으로서, 이름이 [!UICONTROL 관리로 변경되었습니다].

이 새로 고침의 일부로, 다음과 같은 [!UICONTROL 관리] 섹션의 페이지를 사용하여 많은 작업을 쉽게 수행할 수 있습니다.

* 구현 탭( [!UICONTROL 관리] > 구현)에서 최신 at.js 파일을&#x200B;**** **[!UICONTROL 다운로드합니다]**.
* at.js 설정을 사용자 정의하고 변경 사항을 쉽게 검토할 수 있습니다(**[!UICONTROL 관리]** > **[!UICONTROL 구현]**).
* 기본 통화 및 표준 시간대, 보고에서 제외되도록 IP와 같은 향상된 보고 설정을 수정합니다. (**[!UICONTROL 관리]** > **[!UICONTROL 보고]**)
* 개인 정보 보호를 위해 방문자 IP 주소 난독화(**[!UICONTROL 관리]** > **[!UICONTROL 구현]**)
* Adobe Admin Console(**[!UICONTROL 관리]** > **[!UICONTROL 사용자]**)에서 관리하기 전에 작업 공간당 사용자 및 해당 역할의 기존 사용자 목록을 확인합니다.
* 관리 섹션에서 모든 테이블을 검색하고 [!UICONTROL 필터링합니다] .

자세한 내용은 Target 관리 [개요를 참조하십시오](/help/administrating-target/administrating-target.md).

### 개선 사항, 수정 사항 및 변경 사항

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 새로 고친 후 사이트 환경 설정을 유지할 수 없는 문제를 해결했습니다. (TGT-37239)
* SVG(Scalable Vector Graphics) 이미지 [!UICONTROL 에서] 이후 [!UICONTROL 삽입 >] 이미지기능이 제대로 작동하지 않는 문제를 해결했습니다. (TGT-37242)
* 초안 활동을 삭제할 수 없는 [!UICONTROL 게시자] 역할을 가진 사용자의 문제를 수정했습니다. (TGT-37358)
* 모든 내 작업 영역을 선택할 때 사용자가 활동 [!UICONTROL 을 편집할 수 없는] 문제를 수정했습니다. (TGT-37276)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
