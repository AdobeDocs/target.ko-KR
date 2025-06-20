---
keywords: 릴리스 노트;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트,현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: d87f1fbe78512363d4fe30935cbb4f2556b4a06b
workflow-type: tm+mt
source-wordcount: '1935'
ht-degree: 19%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 업데이트됨: [!DNL Target] UI 버전 전환 중단(2025년 6월 17일) {#revised}

2025년 6월 17일부터 모든 IMS 조직은 새 경험 테스트를 시작하려면 특정 사용자 또는 조직 전체에 대해 업데이트된 [!DNL Target] UI에 대해 활성화되어야 합니다.

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 [!DNL Target] 팀이 사용 중단 타임라인을 조정했습니다.

* **2025년 6월 30일**: [업데이트됨 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md)는 UI 버전 전환을 사용하도록 설정한 모든 IMS 조직의 기본 환경이 됩니다.

   * 현재 기존 UI가 표시되는 고객은 기본적으로 이제 로그인 시 업데이트된 UI를 보게 됩니다.
   * UI 버전 토글 기능은 7월 말까지 계속 사용할 수 있으며, 필요한 경우 다시 전환할 수 있습니다.

  >[!IMPORTANT]
  >
  > [!DNL Adobe]은(는) 업데이트된 [!DNL Target] UI를 사용할 것을 강력히 권장합니다. 차단 문제가 발생하는 경우에만 레거시 UI로 다시 전환하십시오. 전환에 대한 중요 정보는 이전 릴리스의 릴리스 정보에서 [[!DNL Target] UI 버전 전환 중단(2025년 5월 23일)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle)을 참조하십시오.

* **7월 15일부터 2025년 7월 30일까지**: UI 버전 토글이 단계적으로 영구적으로 비활성화됩니다. 영향을 받는 IMS 조직은 더 이상 기존 UI로 되돌릴 수 없습니다.

   * 예외는 사안별로 검토할 것입니다.
   * 전환 중단 지연은 차단 문제가 해결되는 동안 잠시(며칠) 동안만 부여됩니다.

문제가 있거나 이 전환 중에 문제가 예상되는 경우 [Adobe 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)에 문의하십시오.

## [!DNL Target Standard/Premium] 25.6.2 (2025년 6월 12일 금요일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 업데이트된 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결하기 위해 [새 FAQ 문서](/help/main/c-intro/updated-ui-faq.md)을 추가했습니다.
* [!UICONTROL Page Delivery]의 &quot;[!UICONTROL URL - does not contain]&quot; 규칙이 작동하지 않아 콘텐츠를 차단해야 하는 경우에도 표시할 수 있는 문제가 해결되었습니다. (TGT-52754)
* [!UICONTROL Page Delivery]에 오류 메시지가 잘못 표시되는 문제가 해결되었습니다. &quot;중복된 페이지 URL은 허용되지 않습니다. (TGT-52765)
* 경험 조각이 포함된 [!UICONTROL Page Delivery]개의 URL에 대한 대상이 #에서 잘못 추가된 문제를 해결했습니다. (TGT-52786)
* [!UICONTROL Goals and Settings] 페이지에서 활동을 복사하고 설정을 편집하면 [!DNL Target] UI가 응답하지 않는 문제를 해결했습니다. (TGT-52797)
* [!UICONTROL A/B Test] 활동의 추가 페이지를 동일한 URL로 잘못 리디렉션할 수 있는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)의 문제를 해결했습니다. (TGT-51838)
* 활동을 편집할 때 [!UICONTROL Goals and Settings] 페이지의 지표 변경 사항이 저장되지 않던 문제를 수정했습니다. (TGT-52799)
* 웹 편집기를 로드하는 동안 새 경험을 추가하면 새 경험이 이전 경험의 콘텐츠를 복제하는 문제가 해결되었습니다. (TGT-51397)
* 기존 Target UI에서 이전에 사용할 수 있었던 기능인 `<head>` 태그 외부에서 사용자 지정 코드를 사용하는 기능을 복원했습니다. (TGT-52304 및 TGT-52300)
* 활동을 만드는 동안 기본 작업 영역을 선택할 때 불필요한 유효성 검사가 제거되었습니다. 필수 속성 유효성 검사는 더 이상 기본 작업 영역에 적용되지 않지만, 기본값이 아닌 작업 영역에는 그대로 유지됩니다. (TGT-52449)
* 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 `triggerView()` 호출이 검색되지 않는 문제를 해결했습니다. (TGT-52575)
* 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 사용자가 [!UICONTROL Single Page Application]&#x200B;(SPA) 보기에 수정 사항을 추가하지 못하는 문제를 해결했습니다. (TGT-52556)
* 업데이트된 [!DNL Target] UI에서 고객이 오퍼 세부 정보를 볼 수 없는 문제를 해결했습니다. (TGT-52607)
* [!UICONTROL Offers Library]의 오퍼에 대한 업데이트가 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 반영되지 않는 문제를 해결했습니다. (TGT-52637)
* 활동을 만드는 동안 오퍼 섹션이 제대로 표시되지 않는 문제를 해결했습니다. (TGT-52773)
* `optionGroups`에서 참조된 모든 `optionLocalIds`이(가) 옵션 배열에 있는지 확인하기 위해 유효성 검사를 추가했습니다. 잘못된 참조는 활동을 만드는 동안 자동으로 제거됩니다. (TGT-52687)
* 새 오퍼를 추가한 후 보고 그룹 및 제외가 유지되지 않던 문제를 수정했습니다. (TGT-52728)
* [!UICONTROL Activity QA] 단추가 없는 활동에 빈 옵션 선택기가 표시되는 문제가 해결되었습니다. (TGT-52733)
* QA 링크가 콘텐츠를 제대로 렌더링하지 못하는 문제를 해결했습니다. (TGT-52718)
* 요소를 경험 조각으로 바꾸면 QA 환경에서 변경 사항이 올바르게 반영되지 않는 문제를 해결했습니다. (TGT-52762)
* 사용자가 경험 조각을 추가하려고 할 때 &quot;잘못된 입력&quot; 오류가 발생하는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)의 문제를 해결했습니다. (TGT-52701)
* 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 대상 타깃팅을 편집할 때 &quot;대상 편집&quot; 모달이 비어 있는 것으로 표시되는 문제가 해결되었습니다. (TGT-52749)
* 선택한 작업 영역에서 엔티티에 액세스할 수 없는 경우 사용자에게 알리는 메시지가 추가되었습니다. (TGT-52767)
* UI에서 조건에 환경 ID를 수동으로 할당할 수 없었던 문제가 해결되었습니다. 대신 기본적으로 [!UICONTROL Product Catalog Search] 호스트 그룹의 ID가 사용됩니다. 이 수정 사항은 이제 기본값뿐만 아니라 모든 환경에 기준 변경 사항이 적용되도록 합니다. (TGT-52817)
* 권장 사항이 있는 [!UICONTROL Experience Targeting] (XT) 활동에 대해 &quot;[!UICONTROL Download Recommendations data]&quot; 옵션이 누락되는 문제를 해결했습니다. (TGT-52730 및 TGT-52756)

## [!DNL Target Standard/Premium] 25.6.1 (2025년 6월 6일 토요일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* QA 링크가 연결된 활동에 대한 올바른 경험을 전달하지 못했던 문제를 수정했습니다. (TGT-52163 및 TGT-52790)
* QA 링크에 관련 대상 ID가 누락되는 문제를 해결했습니다. (TGT-52722)
* 구성된 페이지 전달 URL 조건이 정확하게 충족될 때만 경험이 전달되도록 하는 문제가 수정되었습니다. (TGT-52696)
* 고객이 [!DNL Recommendations] 디자인 템플릿을 만들 수 없는 문제를 해결했습니다. 템플릿을 만들려고 하면 &quot;스크립트 내에 최소 1개의 엔티티 변수가 사용되어야 합니다.&quot; 오류가 트리거되었습니다. (TGT-52395)
* Velocity 배열을 사용하여 [!DNL Recommendations] 디자인을 저장할 수 없는 문제를 해결했습니다. &quot;스크립트 내에 최소 1개의 엔티티 변수가 사용되어야 합니다.&quot; 오류 메시지가 잘못 트리거되었습니다. (TGT-52734)
* 내부 웹 페이지에 대해 페이지를 로드하지 못했을 때 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 수정 사항에 액세스할 수 없는 문제를 해결했습니다. (TGT-52488 &amp;TGT-52470)
* VEC의 더 작은 화면 크기에서 [!UICONTROL Modifications] 패널이 표시되지 않는 문제를 해결했습니다. (TGT-52470)
* 업데이트된 VEC에서 [!UICONTROL Browse] 모드에서 [!UICONTROL Design] 모드로 다시 전환하면 콘솔 오류가 발생하여 더 이상 상호 작용하지 못하는 문제가 해결되었습니다. (TGT-52532)
* VEC에서 특정 요소를 클릭하면 의도하지 않게 크기가 확장되는 문제를 해결했습니다. (TGT-52497)
* 특정 페이지 요소가 VEC에서 로드되지 않거나 인식되지 않아 버튼 또는 배너를 선택하는 등의 상호 작용을 방지하고 활동에서 정확한 이벤트 추적을 중단하는 문제를 해결했습니다. (TGT-52663)
* 고객이 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 오퍼를 삭제하거나 제거할 수 없는 문제를 해결했습니다. (TGT-52690)
* 다중 페이지 활동에서 일관되지 않은 활동 자격 동작을 발생시킨 문제를 수정했습니다. (TGT-52694)
* 활동의 [!UICONTROL Overview] 페이지에 [!UICONTROL Activity Location]에 대한 잘못된 URL이 표시되는 문제를 해결했습니다. (TGT-52695)
* 업데이트된 [!DNL Target] UI에서 활동 위치에 대한 중복 항목이 표시되는 문제를 해결했습니다. (TGT-52693)
* 고객이 활동을 편집하거나 복사할 수 없도록 `getAudiencesV3` 오류를 트리거하는 문제를 해결했습니다. (TGT-52709)
* [!UICONTROL Experience Fragments] 또는 HTML 오퍼를 활동에 추가할 때 잘못된 페이로드 오류가 발생하는 문제를 해결했습니다. (TGT-52779 및 TGT-52773)
* 잘못된 입력 오류로 인해 E[!UICONTROL xperience Fragments]이(가) 올바르게 표시되지 않는 업데이트된 [!DNL Target] UI의 문제를 해결했습니다. (TGT-52701)
* 잘못된 사용자 오류로 인해 고객이 [!UICONTROL Form-based Experience Composer]에서 활동을 편집할 수 없는 문제를 해결했습니다. (TGT-52470)
* 이전 번역이 기본 다국어 평면 외부의 문자를 사용하던 한국어의 현지화 문제를 해결했습니다. 업데이트된 번역문은 의도된 의미를 정확하게 전달하는 적절한 문자를 사용한다. (TGT-52508 및 TGT-52509)
* 활동에 대한 시작 및 종료 날짜를 선택할 때 &quot;날짜&quot;에 대한 번역이 일관되지 않았던 한글의 현지화 문제를 해결했습니다. (TGT-52510)

## [!DNL Target] UI 버전 전환 사용 중단(2025년 5월 23일) {#toggle}

>[!IMPORTANT]
>
>[!DNL Target] 팀이 UI 버전 전환 사용 중단에 대한 타임라인을 조정했습니다. 자세한 내용은 [업데이트됨: [!DNL Target] UI 버전 전환 사용 중단(2025년 6월 17일)](#revised)을 참조하십시오.

새 [!DNL Target] 사용자 인터페이스의 롤아웃이 **2025년 5월 27일**&#x200B;까지 완료됩니다. 이 시점에서 모든 고객은 최신 UI 버전에 액세스할 수 있습니다.

**2025년 6월 22일**&#x200B;부터 UI 버전 토글이 제거됩니다. 모든 사용자는 이전 버전으로 되돌릴 옵션 없이 새 인터페이스로 영구적으로 전환됩니다.

>[!NOTE]
>
>6월 22일 이후에도 토글을 유지해야 하는 특별한 경우가 있는 고객은 Adobe 고객 지원 센터에 문의할 수 있습니다.

### UI 버전 전환에 대한 중요 정보

토글 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능을 제공하고 있습니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다.

![Target UI 버전 전환](/help/main/r-release-notes/assets/toggle.png)

롤아웃이 완료되면 토글이 제거되고 모든 사용자가 **2025년 6월 22일**&#x200B;에 업데이트된 UI로 영구적으로 전환됩니다. Adobe에서는 이 기능이 곧 단계적으로 중단되므로 미리 계획을 수립하는 것이 좋습니다.

### UI 전환 동작 제한 사항

* **새 활동의 가시성**: 기존 UI로 다시 전환하면 업데이트된 UI에서 만들어진 활동이 표시되지 않습니다.
* **기존 활동 편집**: 업데이트된 UI를 사용하는 동안 기존 활동(원래 기존 UI에서 만들어짐)에 대한 변경 사항이 웹 사이트에 게시됩니다. 그러나 다시 전환하는 경우 이러한 업데이트가 이전 UI에 표시되지 않습니다. 이전 UI에서 마지막으로 수행한 업데이트만 표시됩니다.
* **활동 세부 정보의 일관성**: 사용하는 UI에 관계없이 가장 최근의 변경 내용이 라이브 웹 사이트에 반영됩니다. 하지만 기존 UI에는 해당 버전 내에서 변경된 최신 변경 사항만 표시됩니다. 업데이트된 UI에서 편집된 활동이 기존 UI에 표시되는 것과 다른 경우 혼동을 일으킬 수 있습니다.

### 업데이트된 UI에 대한 추가 정보

* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!UICONTROL Activities], [!UICONTROL Recommendations] 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.

* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!UICONTROL Offers Library]에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.

* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.

* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.

* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.

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
