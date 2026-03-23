---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 62d33419f2cbad93d99b29cef58e99f4d84a98f6
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 47%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 26.3.2(2026년 3월 10일)

**활동**

+++세부 정보 보기

* **경험의 직접 오퍼 변경 내용이 저장되지 않습니다.** 이 수정 사항은 활동 경험 내에서 직접 오퍼에 대한 수정 사항이 저장되지 않는 문제를 해결합니다. 이전에는 사용자가 직접 오퍼를 열고 변경한 후 저장하면 변경 사항이 처음에 반영되었지만 오퍼를 다시 열 때는 손실되었습니다. 이 수정 사항은 오퍼가 다시 열릴 때 직접 오퍼에 대한 변경 사항이 제대로 저장되고 유지되도록 합니다. (TGT-54653)

+++

**구현**

+++세부 정보 보기

* **구현 화면에서 깜박임 관리 추가 토글** 깜박임 관리 설정의 활성화를 제어하기 위해 [!UICONTROL Implementation] 화면에 새로운 토글이 추가되었습니다. 이 토글을 사용하면 관리자가 구현 화면에서 직접 플리커 관리를 구성할 수 있습니다. (TGT-52247)

+++

**개요**

+++세부 정보 보기

* **개요 페이지에 대상자와 경험의 전체 이름을 표시합니다.** 이 개선 사항은 [!UICONTROL Overview] 페이지를 업데이트하여 대상 및 경험의 전체 이름을 표시합니다. 이전에는 긴 이름이 잘리고 완전히 표시되지 않았으므로 사용자가 모든 텍스트를 세 번 클릭하여 전체 이름을 볼 수 있도록 선택해야 했습니다. 업데이트에서는 전체 대상 및 경험 이름이 표시되므로 사용자가 활동 구성을 보다 쉽게 식별하고 검토할 수 있습니다. (TGT-53323)

+++


## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
