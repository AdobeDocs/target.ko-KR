---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7976d43e43baeabdb68509373f1b0b72bbe723b3
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 49%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 26.4.4(2026년 4월 28일)

**활동**

+++세부 정보 보기

* **보고서의 대상 필터에 오류가 있습니다.** **[!UICONTROL Goals & Settings]** 내의 대상 필터를 변경하면 [!DNL Target] 사용자 인터페이스의 보고 섹션에 오류가 발생하는 문제가 해결되었습니다. (TGT-55006)

* **우선 순위별로 활동을 정렬합니다.** **[!UICONTROL Priority]** 열 헤더를 사용하여 작업 목록에 우선 순위별 정렬을 추가했습니다. 오름차순 및 내림차순은 정렬 가능한 다른 열과 일치합니다. (TGT-54948)

* **저장 후 추가 활동 속성이 유지되지 않습니다.** 활동을 저장하고 다시 연 후 특정 **[!UICONTROL Properties]** 선택이 지속되지 않던 문제를 수정했습니다. (TGT-53889)

+++

**로컬라이제이션**

+++세부 정보 보기

* [!UICONTROL Page Delivery] 규칙 연산자에 대한 **일본어 레이블.** 일본어 UI에서 페이지 전달 규칙 연산자 레이블에 대한 읽을 수 없거나 손상된 문자열을 수정했습니다. (TGT-53097)

+++

**API**

+++세부 정보 보기

* `segmentId`에 대한 **보고 [!DNL GraphQL] API 지원.** 보고 [!DNL GraphQL] API에 `segmentId`을(를) 추가했습니다. (TGT-55021)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++세부 정보 보기

* **편집기에서 잘못된 환경에 수정 사항이 표시되었습니다.** [!UICONTROL Visual Experience Composer]에서 경험 간에 전환한 후 잘못된 경험에 삭제 또는 기타 수정 사항이 나타날 수 있는 문제를 해결했습니다. (TGT-54955)

* **삽입 HTML을 삭제할 때 수정 사항이 제거되었습니다.** **[!UICONTROL Insert before]** 또는 **[!UICONTROL Insert after]**&#x200B;과(와) 함께 추가된 추가 **[!UICONTROL HTML]** 블록을 삭제하면 CSS 선택기가 없는 연결된 수정도 제거되던 문제를 해결했습니다. (TGT-54530)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)




**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

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
