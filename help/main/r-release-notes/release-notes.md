---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 693b862bc39fc3b1b7d93988bd80cdd51657354b
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 19%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 25.11.1(2025년 11월 10일)


**Analytics for Target (A4T)**

+++세부 정보 보기
* 업데이트된 UI에서 보고 소스로 **[!UICONTROL Goals & Settings]을(를) 사용할 때 [!DNL Adobe Analytics] 오류 메시지가 표시됩니다.** 업데이트된 [!UICONTROL Overview] UI에서 목표 섹션에 &quot;문제가 발생했습니다. 요청을 완료할 수 없습니다. 보고 소스로 [!DNL Adobe Client Care]&#x200B;(A4T)을(를) 선택했을 때 문제가 지속되면 [!DNL Adobe Analytics]에 문의하십시오. 이제 목표가 [!UICONTROL Adobe Analytics] 지표와 함께 올바르게 표시되므로 보고 소스 간에 일관적인 가시성이 보장됩니다. (TGT-54021)

+++

**대상자**

+++세부 정보 보기
* **업데이트된 UI에서 여러 보고 대상을 선택할 수 없습니다.** 사용자가 활동을 편집할 때 새로 만든 보고 대상을 동시에 여러 개 선택할 수 없는 업데이트된 UI의 문제를 해결했습니다. 이제 여러 대상을 한 번에 할당할 수 있으므로 보고 설정의 유연성과 효율성을 높일 수 있습니다. (TGT-53253)

+++

**의사 결정 오퍼**

+++세부 정보 보기
* **업데이트된 UI에서 의사 결정 오퍼를 편집하거나 바꿀 수 없습니다.** 업데이트된 UI에서 [!UICONTROL Modifications] 패널을 통해 의사 결정 오퍼를 편집하거나 바꿀 수 없고 오퍼 이름이 비어 있는 문제를 해결했습니다. 이제 Decisioning 오퍼에 완전히 액세스하고 편집할 수 있으므로 기존 UI와의 패리티를 복원하고 고객이 활동 내에서 오퍼를 직접 관리할 수 있습니다. (TGT-53884)

+++

**로컬라이제이션**

+++세부 정보 보기
* **한국어 및 일본어 UI에서 몇 가지 현지화 오류를 수정했습니다.**(TGT-54003, TGT-54004, TGT-54006, TGT-54007, TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++세부 정보 보기
* 엔티티 특성이 일치하는 특성별 **프로모션을 활동 저장 후 권장 사항 키를 로드하지 못했습니다.** 활동을 저장한 후 편집할 때 규칙 유형이 [!UICONTROL Promotion by Attribute]인 유형 [!UICONTROL Entity Attribute Matching]의 프로모션이 권장 사항 키를 로드하지 않는 문제를 해결했습니다. `customKeyId`이(가) GraphQL을 통해 요청되지 않아 문제가 발생했습니다. 이제 프로모션을 편집하는 동안 권장 사항 키가 올바르게 로드됩니다. (TGT-53117)
* **권장 사항은 ExpB에서 ExpA로 전환할 때 시각적으로 유지됩니다.** 경험 B에서 추천을 삽입한 다음 경험 A로 전환하면 추천 오퍼 상자가 표시되는 문제가 해결되었습니다. 이는 시각적 비일관성으로만 제공되었습니다. 이제 경험 간에 전환할 때 수정 사항이 올바르게 렌더링되어 정확한 UI 동작이 보장됩니다. (TGT-53911)
* **이(가) 일치하는 [!UICONTROL Promotion by Attribute]에 대해 [!UICONTROL Entity Attribute]추천 키가 로드되지 않습니다.** 규칙 유형이 [!UICONTROL Promotion by Attribute]인 [!UICONTROL Entity Attribute Matching] 유형의 프로모션이 활동을 저장한 후 편집할 때 권장 사항 키를 로드하지 않는 문제를 해결했습니다. 이제 GraphQL을 통해 권장 사항 키를 올바르게 검색하므로 프로모션이 예상대로 표시되고 작동하도록 할 수 있습니다. (TGT-53917)
* **숨겨진 HTML 요소에 대한 권장 사항 편집이 업데이트된 UI에서 작동하지 않습니다.** [!UICONTROL New Create] 및 VEC UI에서 숨겨진 HTML 요소에 적용된 권장 사항 활동을 편집할 수 없는 문제를 해결했습니다. 이제 이 기능이 예상대로 작동하여 기존 UI와의 패리티를 복원하고 요소 가시성에 관계없이 권장 사항을 수정할 수 있습니다. (TGT-53953)
* **업데이트된 UI에서 숨겨진 HTML 요소에 대한 권장 사항 활동을 편집할 수 없습니다.** 업데이트된 UI에서 숨겨진 HTML 요소에 적용된 권장 사항 활동을 편집할 수 없는 문제를 해결했습니다. 이제 이 기능이 예상대로 작동하여 기존 UI와의 패리티를 복원하고 요소 가시성에 관계없이 권장 사항을 수정할 수 있습니다. (TGT-53951)
* **업데이트된 UI에서 추천 카탈로그에 특성 값이 간헐적으로 누락되었습니다.** 제품 피드에 있는 경우에도 카탈로그 검색 목록에 특정 특성 값(예: 메시지)이 간헐적으로 표시되지 않는 업데이트된 [!UICONTROL Recommendations] UI의 문제를 해결했습니다. 이제 속성 값이 열을 재구성하지 않고 검색 결과에 일관되게 로드되므로 카탈로그 관리의 안정성과 효율성이 향상됩니다. (TGT-52769)
* 업데이트된 UI에서 **[!UICONTROL Download Recommendations]활동에 대한 [!DNL Recommendations] 단추가 없습니다.** 업데이트된 [!DNL Recommendations] UI에서 권장 사항을 사용하는 A/B 활동에 대해 [!UICONTROL Download Recommendations] 단추가 표시되지 않는 문제를 해결했습니다. 이제 버튼이 올바르게 표시되어 사용자가 레거시 UI의 기능과 일관되게 권장 사항 데이터를 예상대로 내보낼 수 있습니다. (TGT-53768)
* 업데이트된 개요 UI에 **[!UICONTROL Download Recommendation Data]단추가 없습니다.** 업데이트된 [!UICONTROL Overview] UI에서 권장 사항이 포함된 활동에 대해 [!UICONTROL Download Recommendation Data] 단추가 표시되지 않는 문제를 해결했습니다. 이제 버튼이 올바르게 표시되어 사용자가 이전 UI로 다시 전환할 필요 없이 권장 사항 데이터를 직접 내보낼 수 있습니다. (TGT-53772)
* **활동 기준을 편집하면 업데이트된 UI에서 빈 화면이 표시되는 경우가 있습니다.** 업데이트된 UI에서 [!UICONTROL Edit Criteria in Experiences]을(를) 클릭하면 특정 활동에 대한 빈 화면이 표시되는 문제가 해결되었습니다. 이제 기준 편집기가 모든 활동에 안정적으로 로드되어 사용자가 중단 없이 편집할 수 있습니다. (TGT-53961)
* **업데이트된 UI에서 시퀀스 조건을 편집할 수 없습니다.** 업데이트된 UI에서 [!UICONTROL Sequence Criteria]을(를) 편집하려고 하면 기준 팝업이 로드 시 중단된 상태로 유지되어 빈 화면이 표시되는 문제를 해결했습니다. 이제 기준 편집기가 올바르게 로드되어 사용자가 중단 없이 시퀀스 기준을 편집하고 업데이트할 수 있습니다. (TGT-53985)

+++

**[!UICONTROL Reports]**

+++세부 정보 보기
* **[!UICONTROL Multivariate Test] (MVT) 위치 및 그래프 보고 문제로 인해 보고서를 생성할 수 없습니다.** MVT 활동이 Target UI에서 [!UICONTROL Location Contribution] 및 그래프 보고서를 생성하지 못하고 &quot;문제가 발생했습니다. 요청을 완료할 수 없습니다.&quot; 이제 보고서가 UI 내에서 올바르게 로드되어 전체 가시성이 보장됩니다. (TGT-53654)
* **기여 보고서 오류로 인해 [!UICONTROL Element]MVT 보고서가 로드되지 않습니다.** MVT 활동 보고서가 Target UI에서 로드되지 않고 &quot;요소 기여도 보고서를 가져올 수 없습니다.&quot;라는 오류가 표시되는 문제를 해결했습니다. 이제 보고서가 올바르게 표시되므로 요소 기여도를 완전히 볼 수 있습니다. (TGT-53691)
* **(XT) 활동에 대해 [!UICONTROL Experience Targeting]주문 세부 사항을 CSV 문제로 내보냅니다.** XT 활동에 대해 [!UICONTROL Export Order Details to CSV] 옵션이 잘못 표시되고 빈 파일이 반환되는 문제가 해결되었습니다. 이제 AP 활동에 대해서만 옵션이 표시되므로 정확한 내보내기 기능을 보장하고 혼동을 방지할 수 있습니다. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++세부 정보 보기
* **[!UICONTROL Delete Modification]단추 문제로 인해 활동 수정 사항을 제거할 수 없습니다.** [!UICONTROL Delete Modification] UI의 [!DNL Target] 단추가 작동하지 않아 사용자가 활동 내에서 수정 사항을 제거할 수 없는 문제가 해결되었습니다. 이제 버튼이 예상대로 작동하므로 수정 사항을 지연 없이 안정적으로 삭제할 수 있습니다. (TGT-53728)
* 업데이트된 UI에서 **기본 설정 선택기를 인식할 수 없습니다.** 업데이트된 UI에서 `data-target-component-id`과 같은 기본 설정 선택기가 VEC 내의 CSS 선택기 목록에 표시되지 않는 문제를 해결했습니다. 이제 사용자는 동적으로 생성된 클래스 이름 대신 기본 속성을 안정적으로 선택하여 SPA 페이지 업데이트 전반에 걸쳐 안정적인 타겟팅을 보장할 수 있습니다. (TGT-53908)
* **페이지와 [!UICONTROL Edit]페이지 사이에서 [!UICONTROL Overview]활동 위치 정렬이 일치하지 않습니다.** [!UICONTROL Overview] 페이지의 활동 위치 번호 매기기가 [!UICONTROL &#x200B; Edit Experience] 페이지의 업데이트와 일치하지 않는 문제를 해결했습니다. 이제 위치가 두 보기에서 일관되게 유지되므로 정확한 정렬을 보장하고 위치 누락 또는 번호가 잘못 지정되는 것을 방지할 수 있습니다. (TGT-53960 및 TGT-53954)
* **업데이트된 VEC에서 [!UICONTROL Design] 모드로 다시 전환할 수 없습니다.** 사용자가 [!UICONTROL Design] 모드에서 새 페이지로 이동한 후 [!UICONTROL Browse] 모드로 다시 전환할 수 없는 업데이트된 VEC UI의 문제를 해결했습니다. 이제 [!UICONTROL Design] 토글이 올바르게 작동하여 페이지 전체에 수정 사항을 매끄럽게 적용할 수 있습니다. (TGT-53988 및 TGT-53993)
* **쿼리 매개 변수가 활동 개요에 표시되지 않습니다.** 업데이트된 UI에서 활동에 대한 [!UICONTROL Overview] 페이지에 쿼리 매개 변수가 표시되지 않아 [!UICONTROL Overview]과(와) 페이지 배달 URL 간의 불일치가 발생하는 문제를 해결했습니다. 이제 쿼리 매개 변수가 올바르게 표시되므로 활동 위치가 보기 간에 완전히 표시되고 일관되게 표시됩니다. (TGT-53701)

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
