---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 4efaf7ce039aabb26fc130e541fb6057115a3c7e
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 11%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**최근 업데이트: 2020년 8월 31일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>* **Adobe, 개인화 엔진 부문 Gartner Magic Quadrant에서 리더로 선정**:Adobe은 2020년 발표된 3분기 Gartner Magic Quadrant에서 리더로 다시 선정되었습니다. Gartner Magic Quadrant의 개인화 엔진 평가 결과,비전의 완전성과 실행 능력. [Adobe 블로그에서 확인할 수 있습니다](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js 사용 중단**:2021년 1월 18일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더를 참조하십시오.개발자 채팅에서 Adobe Target의 mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**:Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.8.1(2020년 9월 2일)

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 조직을 전환한 후 새 [!UICONTROL 관리] 페이지를 로드할 때 오류가 표시되는 문제를 해결했습니다. (TGT-37730)
* 잘못된 클라이언트 코드가 [!UICONTROL 관리 > 구현] 페이지에 표시되던 표시 문제를 수정했습니다. (TGT-37849)
* 때때로 사용자가 VEC를 성공적으로 로드한 후 [!UICONTROL VEC] (Visual Experience Composer)의 편집 기능을 사용할 수 없는 문제를 수정했습니다. (TGT-37162)
* VEC 도우미 확장이 설치되어 있어도 VEC 및 EEC(Enhanced Experience Composer)에서 페이지를 로드할 수 없는 문제를 해결했습니다. 이는 Google Chrome 80+의 변경 때문입니다. 업데이트된 VEC [도우미 확장을 다운로드합니다](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893)
* 조직을 전환한 후 때때로 사용자가 [!UICONTROL 관리 > 구현] 페이지에서 at.js를 다운로드할 수 없는 문제를 해결했습니다. (TGT-37668)
* 이제 사용자가 다운로드 단추를 여러 번 클릭하는 경우 여러 요청을 전송할 수 없도록 로드 중에 at.js 다운로드 단추 [!DNL Target] 가 비활성화됩니다. (TGT-37633)
* 장시간 동안 경험이 &quot; [!UICONTROL 결과] &quot;를 표시하는 XT(경험 타깃팅) 활동의 문제를 수정했습니다. (TGT-37684)
* 키보드 전용 사용자를 위한 탐색 및 기능이 개선되었습니다. (TGT-34479 및 TGT-34473)
* 보조 기술을 사용하는 사용자에게 도움이 되는 레이블을 UI에 추가했습니다. (TGT-34480)
* 활동에 현재 사용되는 모바일 뷰포트를 삭제할 때 오류 메시지가 개선되었습니다. 이제 오류 메시지가 표시됩니다.&quot;이 뷰포트는 현재 하나 이상의 활동과 연결되어 있습니다. 삭제하기 전에 해당 활동에서 뷰포트를 제거해야 합니다.&quot; (TGT-37030)
* 페이지에서 둘 이상의 요소와 일치하는 css 선택기에서 클릭 추적을 허용하는 VEC에 지원을 추가했습니다. (TGT-37323)
* 특정 사용자가 [!UICONTROL 활동] 목록을 표시하지 못하는 문제를 해결했습니다. 다음 오류 메시지가 표시되었습니다.&quot;URL제안을 가져올 수 없습니다.&quot; Adobe 백엔드 시스템의 FirstName(FirstName/r/n)에서 캐리지 리턴을 사용하는 사용자에 대해 오류가 발생했습니다. (TGT-37330)
* 작업 공간 이름(Enterprise용 [!UICONTROL Adobe Admin Console에] 지정)에 아포스트로피가 포함되어 있는 경우 사용자가 [!UICONTROL 활동]페이지를 표시할 수 없는 문제를 해결했습니다. (TGT-37709)
* 보고서 세트가 이미 지정된 [!UICONTROL 경우에도 오류 메시지가 사용자에게 보고서 세트를 선택하라고 잘못 알렸던 최적화 및 전환 지표를 선택하는] 동안 자동 할당 활동의 문제를 수정했습니다. (TGT-37689)
* 타깃팅 페이지로 이동한 후 [!UICONTROL 돌아온 후 종종 목표 및 설정] 페이지의 지표가 [!UICONTROL 비어 있는] 문제를 해결했습니다. (TGT-37691)
* 기준에 대해 잘못된 최종 수정 값을 초래했던 문제를 [!DNL Recommendations] 수정했습니다. (TGT-37666)
* mbox 이름 대신 mbox 드롭다운 목록에 mbox ID가 표시되는 문제를 해결했습니다. (TGT-37739)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
