---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 78c2547a036d7c01348410a34010e57d36797e07
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 22%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2020년 5월 20일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!NOTE]
>
>* **mbox.js 사용 중단**: 2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). 자세한 내용은 *Adobe Target 기술 빌더를 참조하십시오. 개발자 채팅에서 자세한 내용을 보려면 Adobe Target의 mbox.js를* 아래 at.js로 마이그레이션하십시오.
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.


## Adobe Target 스킬 빌더: 개발자 채팅, Adobe Target의 mbox.js를 at.js로 마이그레이션 {#skill-builder}

2020년 8월 30일에 mbox.js의 사용 중단 사태가 임박하면서 Adobe Target 제품 관리자인 David Son은 최근 개발자 채팅을 열어 mbox.js를 at.js로 마이그레이션하는 것의 이점에 대해 논의했습니다. 이후 30일 동안 웨비나 레코딩 [을 볼 수 있습니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).

## Target Standard/Premium 20.6.1(2020년 6월 10일)

| 기능/향상 | 설명 |
| --- | --- |
| 게시자 역할 | 이 새 역할은 현재 옵저버 역할과 비슷합니다(활동은 볼 수 있지만 만들거나 편집할 수는 없습니다). 그러나 게시자 역할에는 활성 활동에 대한 추가 권한이 있습니다. |
| 관리<br>페이지이전에 &quot;설정&quot;이었습니다. | 설정 페이지의 이름이 &quot;관리&quot;로 변경되었으며 모든 메뉴 항목의 UI가 워크플로우 및 사용 편이성을 개선하기 위해 업데이트되었습니다.<br>사용 가능한 메뉴 항목은 다음과 같습니다.<ul><li>시각적 경험 작성기</li><li>보고</li><li>Scene7 설정</li><li>구현</li><li>속성</li><li>호스트</li><li>환경</li><li>응답 토큰</li><li>사용자</li></ul> |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
