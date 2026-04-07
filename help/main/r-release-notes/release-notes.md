---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: ada5803424b4930d91dda735901390fe5073932f
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 39%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

<!--
## [!DNL Target Standard/Premium] 26.4.2 (April 7, 2026)

**Activities**

+++See details

* **Custom code preserved when applied to additional views.** Fixed an issue where custom code applied to one **[!UICONTROL View]** could be removed when adding or saving custom code for another **[!UICONTROL View]** in the same **[!UICONTROL Activity]**. (TGT-53933)

* **Reporting metrics column order.** The updated [!DNL Target] interface allows reporting metrics to be reordered without clearing the full selection and re-adding metrics in sequence. Previously, users were required to unselect all metrics and select them again in the desired order, which was time-consuming when many metrics were enabled and when adjusting column placement to limit horizontal scrolling. (TGT-53044)

+++

-->

## [!DNL Target Standard/Premium] 26.4.1 (2026년 4월 2일 금요일)

**활동**

+++세부 정보 보기

* **대상 특성이 활동 보기에 표시됩니다.** **[!UICONTROL Activity]**&#x200B;에서 본 대상 규칙 세부 정보에 **[!UICONTROL Audiences]** 섹션에서 동일한 대상을 열 때 나타나는 특정 특성이 표시되지 않던 문제를 수정했습니다. (TGT-54742)

* **활동 및 대상 목록 페이지에서 CSV를 내보냅니다.**&#x200B;에서 **[!UICONTROL Export CSV]** 작업을 추가했으므로 필터를 적용하는 시기를 비롯하여 일상적인 내보내기를 위해 API에만 의존하지 않고 사용자 인터페이스에서 활동 목록을 내보낼 수 있습니다. (TGT-51466)

* 선택기를 찾을 수 없을 때 **경험 수정 플래그가 지정되었습니다.** 경험 수정 사항에서 선택기 존재 확인을 실행합니다. 선택기를 페이지에서 찾을 수 없으면 수정 사항이 잘못된 것으로 플래그가 지정됩니다. (TGT-54815)

* **[!UICONTROL Automated personalization]개 활동.** 사용자가 자동화된 개인화 활동을 안정적으로 생성, 편집 또는 관리하지 못하게 하는 인터페이스 및 활동 로드 문제가 해결되었습니다. 이로 인해 캠페인 설정이 차단되고 개인화 사용 사례가 지연되었습니다. (TGT-54421)

+++

**대상자**

+++세부 정보 보기

* **활동에서 대상을 만들 때 대상 이름 및 설명이 표시됩니다.** 활동 흐름에서 대상을 만들거나 편집할 때 **[!UICONTROL Name]**&#x200B;에서 직접 대상을 만드는 것과 비교하여 대상 **[!UICONTROL Description]** 및 **[!UICONTROL Audiences]** 필드가 명확하게 두드러지지 않는 문제를 해결했습니다. (TGT-54837)

+++

**인사이트**

+++세부 정보 보기

* Insights의 **[!UICONTROL Live Activities]개수.** 인사이트 대시보드의 **[!UICONTROL Live Activities]** 지표가 **[!UICONTROL All Activities]**&#x200B;에 라이브로 표시된 활동 수보다 더 많은 합계를 보고할 수 있는 문제를 해결했습니다. (TGT-54788)

+++

**추천**

+++세부 정보 보기

* **의 [!UICONTROL Global Exclusions]긴 ID 목록.** **[!UICONTROL Global Exclusions]**&#x200B;의 긴 ID 목록을 붙여넣거나 입력하면 업데이트된 인터페이스에서 기존 ID와 비교하여 잘려서 불완전한 제외 목록이 발생하는 문제가 해결되었습니다. (TGT-54422)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++세부 정보 보기

* **의 EEC(고급 경험 작성기) 상태 표시기가 [!UICONTROL Visual Experience Composer]입니다.** EEC 표시기는 향상된 경험 작성기가 활성화되었는지 여부를 나타냅니다. 프레젠테이션이 비대화형 상태 표시로만 제공되므로 더 이상 대화형 토글과 유사하지 않도록 수정되었습니다. (TGT-54828)

* **에서 [!UICONTROL Visual Experience Composer]축소 가능한 왼쪽 레일입니다.** 이제 편집을 위해 활동을 여는 동안 왼쪽 레일을 축소할 수 있습니다. 이렇게 하면 작은 디스플레이를 포함하여 여러 대상 및 페이지를 포함하는 활동에 대한 **[!UICONTROL Components]** 및 **[!UICONTROL Properties]**&#x200B;에 대한 액세스가 향상됩니다. (TGT-54269)

+++


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
