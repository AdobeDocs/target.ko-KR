---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 391653c7a45a48c311c6a6cff358bd077f8c47b7
workflow-type: tm+mt
source-wordcount: 652
ht-degree: 41%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 26.6.1(2026년 6월 4일)

**활동**

+++세부 정보 보기

* **[!UICONTROL 활동 개요]의 활동 URL이 완전하지 않습니다.** [!UICONTROL 활동 개요]에 활동에 대한 전체 URL이 표시되지 않는 문제가 해결되었습니다. (TGT-54029)

* **활동 보고서에 지역화되지 않은 날짜 형식입니다.** **[!UICONTROL 미리 설정된 날짜 범위]** 드롭다운 목록에서 **마지막 X일** 옵션을 선택한 경우 **[!UICONTROL 보고서]** 탭에서 날짜 형식이 현지화되지 않는 문제를 해결했습니다. (TGT-51637)

* **특정 GB18030 문자가 있는 양식 기반 활동을 [!UICONTROL Location]에 저장할 수 없습니다.** **[!UICONTROL Location]** 필드에 특정 GB18030 문자가 포함되어 있을 때 양식 기반 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-46980)

+++

**[!UICONTROL 대상자]**

+++세부 정보 보기

* **중국어 간체 및 번체 중국어에 대한 대상 흐름을 만들 때 지역화되지 않은 일정.** 대상 만들기 흐름 동안 **[!UICONTROL 기간]** 특성의 **[!UICONTROL 시작]** 및 **[!UICONTROL 끝]** 필드에 있는 달력이 중국어(간체) 및 중국어(번체) 로케일에서 현지화되지 않던 문제를 해결했습니다. (TGT-50619)

+++

**[!UICONTROL 시각적 경험 작성기](VEC)**

+++세부 정보 보기

* **업데이트된 Activity Builder에서 현지화되지 않은 도구 설명.** 업데이트된 [!UICONTROL 시각적 경험 작성기] 활동 빌더에서 **[!UICONTROL 개선]** 및 **[!UICONTROL 콘텐츠]** 정보 도구 설명이 현지화되지 않은 현지화 문제를 해결했습니다. (TGT-53721)

* [!UICONTROL 경험 대상]에서 **지역화되지 않은 [!UICONTROL 모든 방문자].** 왼쪽 레일의 **[!UICONTROL 경험 대상]**&#x200B;에 있는 **[!UICONTROL 모든 방문자]** 문자열이 [!UICONTROL 시각적 경험 작성기]에서 현지화되지 않는 문제를 해결했습니다. (TGT-50086)

+++

**[!UICONTROL 보고서]**

+++세부 정보 보기

* [!UICONTROL 사전 설정 만들기] 창에서 **지역화되지 않은 날짜 형식입니다.** **[!UICONTROL 사전 설정 만들기]** 창의 **[!UICONTROL 날짜 범위]** 필드에 있는 날짜 형식이 현지화되지 않은 문제가 수정되었습니다. (TGT-49239)

+++

**로컬라이제이션**

+++세부 정보 보기

* **GB18030 문자가 여러 영역에 표시됩니다.** 일부 개인 사용 영역 문자가 **[!UICONTROL 대상]** UI, **[!UICONTROL 관리]** > **[!UICONTROL 속성]**, 모바일 뷰포트 구성 및 알림 알림에서 문자로 잘못 표시되는 문제가 해결되었습니다. (TGT-49622, TGT-49623, TGT-49624, TGT-49625)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 노트](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
