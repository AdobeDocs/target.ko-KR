---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6ecc59588b51da505b8f567a7e87ccef0f375477
workflow-type: tm+mt
source-wordcount: '1959'
ht-degree: 15%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]은(는) [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

+++세부 정보 보기
[!DNL Target] 팀은 토글 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능을 제공하고 있습니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다.

![Target UI 버전 전환](/help/main/r-release-notes/assets/toggle.png)

롤아웃이 완료되면 토글이 제거되고 모든 사용자가 업데이트된 UI로 영구적으로 전환됩니다. [!DNL Adobe]은(는) 이 기능이 곧 단계적으로 중단될 예정이므로 미리 계획하는 것이 좋습니다.

#### 사용 중단 타임라인

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 [!DNL Target] 팀이 사용 중단 타임라인을 조정했습니다.

* **2025년 6월 17일**: 모든 IMS 조직이 특정 사용자 또는 조직 전체에 대해 업데이트된 [!DNL Target] UI에 대해 활성화되어 새 경험 테스트를 시작합니다.

* **2025년 6월 30일**: [업데이트됨 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md)는 UI 버전 전환을 사용하도록 설정한 모든 IMS 조직의 기본 환경이 되었습니다.

   * 현재 기존 UI가 표시되는 고객은 기본적으로 이제 로그인 시 업데이트된 UI가 표시됩니다.
   * UI 버전 토글 기능은 7월 말까지 계속 사용할 수 있으며, 필요한 경우 다시 전환할 수 있습니다.

  >[!IMPORTANT]
  >
  > [!DNL Adobe]은(는) 업데이트된 [!DNL Target] UI를 사용할 것을 강력히 권장합니다. [전환 스위치 동작의 제한](#limitations) 때문에 차단기 문제가 발생하는 경우에만 레거시 UI로 다시 전환하십시오.

* **7월 15일부터 2025년 7월 30일까지**: UI 버전 토글이 단계적으로 영구적으로 비활성화됩니다. 영향을 받는 IMS 조직은 더 이상 기존 UI로 되돌릴 수 없습니다.

   * 예외는 사안별로 검토됩니다.
   * 전환 중단 지연은 차단 문제가 해결되는 동안 잠시(며칠) 동안만 부여됩니다.

문제가 있거나 이 전환 중에 문제가 예상되면 [Adobe 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)에 문의하십시오.

#### UI 전환 동작 제한 사항 {#limitations}

다음 정보는 버전 토글을 사용할 때 알아 두어야 할 제한 사항에 대해 설명합니다.

* **새 활동의 가시성**: 기존 UI로 다시 전환하면 업데이트된 UI에서 만들어진 활동이 표시되지 않습니다.
* **기존 활동 편집**: 업데이트된 UI를 사용하는 동안 기존 활동(원래 기존 UI에서 만들어짐)에 대한 변경 사항이 웹 사이트에 게시됩니다. 그러나 다시 전환하는 경우 이러한 업데이트가 이전 UI에 표시되지 않습니다. 이전 UI에서 수행한 마지막 업데이트만 표시됩니다.
* **활동 세부 정보의 일관성**: 사용하는 UI에 관계없이 가장 최근의 변경 내용이 라이브 웹 사이트에 반영됩니다. 하지만 기존 UI에는 해당 버전 내에서 변경된 최신 변경 사항만 표시됩니다. 업데이트된 UI에서 편집된 활동이 기존 UI에 표시되는 것과 다른 경우 이 상황이 혼동을 일으킬 수 있습니다.

#### 업데이트된 UI에 대해 알아볼 수 있는 추가 리소스

* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.
* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!DNL Target], [!UICONTROL Activities] 및 [!UICONTROL Recommendations]&#x200B;(VEC)에 대한 [!UICONTROL Visual Experience Composer]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!DNL Target]에 대한 [!UICONTROL Offers Library]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.
* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.
* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

+++

## [!DNL Target Standard/Premium] 25.8.1(2025년 8월 7일)

이 릴리스에는 다음 개선 사항 및 수정 사항이 포함되어 있습니다.

**활동**

+++세부 정보 보기
* 입력 값의 공백으로 인한 페이지 유형 삭제 시 오류, 작업 영역 간 신뢰할 수 없는 활동 복사, QA 환경에서 제대로 작동하지 않는 페이지 전달 규칙을 포함하여 업데이트된 UI와 관련된 여러 문제를 해결했습니다. (TGT-52703)
* 업데이트된 [!DNL Target] UI에서 [!UICONTROL Editor] 역할을 가진 사용자가 라이브 활동에 액세스하여 편집을 시도할 수 있는 문제를 해결했습니다. 이를 제한해야 합니다. 활동 목록 및 개요 화면에 라이브 활동에 대한 편집 옵션이 잘못 표시되어 의도하지 않은 변경이 발생할 수 있습니다. (TGT-53055)
* [!UICONTROL Advanced Search] UI에서 &quot;값이 있음&quot; 또는 &quot;값이 없음&quot; 연산자를 선택하면 피연산자를 입력하라는 메시지가 표시되는 문제가 해결되었습니다. 이러한 조건에는 피연산자가 필요하지 않습니다. (TGT-51961)
* 샌드박스 환경에서도 스테이징에서 프로덕션 작업 영역으로 활동을 복사하려는 시도가 일관되게 실패하는 업데이트된 UI 문제를 해결했습니다. 유효한 구성을 사용하고 적절한 작업 영역 권한이 있음에도 불구하고 고객에게 &quot;활동에서 이미 사용한 익명 대상&quot; 및 &quot;잘못된 대상 ID&quot;와 같은 다양한 오류 메시지가 발생했습니다. (TGT-52394)

+++

**경험 조각(XF)**

+++세부 정보 보기
* 컨텐츠 전달에서 올바르게 작동하지만 XF(경험 조각) 컨텐츠가 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 미리 보기에서 렌더링되지 않는 문제를 해결했습니다. (TGT-53318)

+++

**로컬라이제이션**

+++세부 정보 보기
* QA 테넌트의 여러 언어 환경에서 &quot;프로모션&quot; 섹션의 &quot;프로모션 추가&quot; 버튼이 현지화되지 않고 표시되는 현지화 문제를 해결했습니다. (TGT-53263)

+++

**오퍼**

+++세부 정보 보기
* VEC(시각적 경험 작성기)를 통해 기존 HTML 오퍼를 편집하면 컨텐츠 전달에서 모든 수정 사항이 제거되던 문제를 해결했습니다. 변경 사항은 수정 탭에 회색으로 표시되며, 기존 UI에 올바르게 적용되었더라도 QA 미리 보기에 반영되지 않습니다. (TGT-52863)
* [!DNL Target] 탭에서 다시 [!UICONTROL Visual Experience Composer]&#x200B;(으)로 이동한 후 [!UICONTROL Targeting]&#x200B;(VEC)에서 수정된 HTML 오퍼가 지속되지 않는 업데이트된 [!UICONTROL Experiences] UI의 문제를 해결했습니다. (TGT-52874)
* 업데이트된 [!DNL Target] UI에서 동일한 선택기의 앞에 한 개의 HTML 오퍼를 삽입하고 그 뒤에 다른 오퍼를 삽입하면 잘못된 위치가 생성되는 문제를 해결했습니다. 고객이 [!UICONTROL Targeting] 탭에서 [!UICONTROL Experience] 탭으로 돌아왔을 때 하나의 선택기만 유지되어 수정 내용이 손실되고 컨텐츠 전달이 중단되었습니다. 이 동작은 고유한 위치 식별자를 사용하여 두 수정 사항을 모두 올바르게 보존한 레거시 UI와 다릅니다. (TGT-52891)
* 업데이트된 [!DNL Target] UI에서 [!UICONTROL Modifications] 레일 내에서 추가된 오퍼를 클릭하면 오른쪽의 [!UICONTROL Configuration] 패널이 간헐적으로 나타났다가 사라져 오퍼 설정과 상호 작용하기 어려운 문제가 해결되었습니다. (TGT-53288)
* 활동 내의 대상별 변형에 추가된 HTML 오퍼가 수정 섹션에 일관되게 저장되거나 표시되지 않던 문제를 수정했습니다. 편집하는 동안 대상 간에 전환한 후 이전에 적용된 오퍼가 간혹 사라지거나 렌더링에 실패하여 유효성 검사가 중단되고 활동 준비가 지연될 수 있습니다. (TGT-53440)
* 오퍼를 포함한 활동을 복사하면 새 활동에서 중복 오퍼가 만들어지는 문제가 해결되었습니다. 이 동작은 특히 작업 영역 간에 활동을 이동할 때 불필요한 혼란과 혼동을 초래했습니다. 이 문제를 해결하면 [!DNL Target] 오퍼가 이제 복제 없이 대상 작업 영역에 올바르게 복사되어 활동 관리가 간소화되고 워크플로우 효율성이 향상됩니다. (TGT-53454)

+++

**단일 페이지 응용 프로그램(SPA)**

+++세부 정보 보기
* 업데이트된 VEC에서 고객이 [!UICONTROL Single Page Application]&#x200B;(SPA) 보기에 수정 사항을 적용하지 못하는 문제를 해결했습니다. 이전 UI에서 만든 활동이 보기별 타깃팅을 지원하지만, 새 UI는 보기 전환 컨트롤이 비활성화되어 표시된 상태에서 해당 보기에 대한 편집을 감지하거나 허용하지 못했습니다. (TGT-52556)

+++

**VEC(시각적 경험 작성기)**

+++세부 정보 보기
* [!UICONTROL Visual Experience Composer] 내의 경험에 대한 수정 사항이 표시되지 않거나 UI에 일관되지 않게 표시되는 문제가 해결되었습니다. (TGT-TGT-53381)
* 업데이트된 VEC에서 [!UICONTROL Manage Content] 섹션이 경험 썸네일에 대한 대체 텍스트를 표시하지 못하는 문제를 해결했습니다. 이 문제로 인해 사용자가 문서를 식별하는 데 어려움을 겪었습니다. 특히 파일 이름이 길거나 잘린 경우 더욱 그렇습니다. (TGT-52291)
* 고객이 VEC 활동에서 [!UICONTROL page delivery] 규칙을 구성할 때 잘못된 유효성 검사 오류가 발생하는 오류를 수정했습니다. 특히, 텍스트 값을 입력할 때 텍스트가 지원되어야 하지만 &quot;다음 중 1개 이상의 항목과 같음&quot; 및 &quot;다음 중 같은 항목 없음&quot;과 같은 연산자는 &quot;연산자 유형에 대한 잘못된 입력&quot;을 트리거했습니다. (TGT-52629)
* &quot;오퍼 선택&quot; 단추를 사용하여 오퍼를 선택할 때 업데이트된 UI의 [!UICONTROL Modifications] 패널에서 일관되지 않은 동작을 발생시킨 몇 가지 문제를 해결했습니다. 기존 오퍼를 바꾸는 대신 UI에서 중복을 추가하고 두 오퍼 중 하나와 상호 작용하려고 시도하면 `selectorNotFound`과(와) 같은 콘솔 오류가 발생했습니다. 또한 일부 오퍼에는 &quot;오퍼 선택&quot; 버튼이 표시되지 않고 편집 가능한 속성만 표시됩니다. (TGT-53321)
* 컨트롤 그룹에 대해 올바르게 저장되었는데도 활동 설정 중에 변경된 HTML 코드 변경 사항이 변형 페이지에서 지속되지 않는 업데이트된 [!DNL Target] UI의 문제를 해결했습니다. 페이지를 그룹화하지 않고 테스트를 여러 번 다시 만들려고 했지만, 변형 페이지가 수정 사항을 지속적으로 유지하지 못하여 콘텐츠 전달 및 QA 유효성 검사에 영향을 주었습니다. (TGT-53436)
* 업데이트된 VEC에서 페이지 전달 규칙의 &quot;다음 중 1개 이상의 항목과 같음&quot; 연산자가 입력 값을 수락하지 못하는 문제를 해결했습니다. 모든 mbox에 대해 고객 매개 변수를 구성할 때 이 연산자를 선택하면 &quot;잘못된 입력&quot; 오류가 발생하여 규칙이 생성되지 않습니다. (TGT-52623)

+++

**작업 공간**

+++세부 정보 보기
* 작업 영역 간 활동을 복사할 때 워크플로우가 개선되었습니다. 작업 영역 간 복사 활동으로 인해 이전에는 대상 누락 및 미할당 속성으로 인해 동기화 오류가 발생했습니다. 이 업데이트에서는 복사된 활동을 올바르게 구성하고 게시할 준비가 되도록 하는 보다 스마트하고 직관적인 워크플로우를 도입합니다. (TGT-47094)
* `copyActivityBatchOperations` 돌연변이의 실패로 인해 고객이 작업 영역 간 활동을 복사할 수 없는 문제가 해결되었습니다. 활동을 복제하려고 하면 서버 오류(500)와 null 응답 페이로드가 발생했습니다. (TGT-52405)
* 구성에서 참조된 오퍼를 선택한 작업 영역 내에서 액세스할 수 없을 때 활동을 동기화하지 못하는 문제를 해결했습니다. 이로 인해 게시 오류가 발생하고 활동이 실패 상태로 남았습니다. (TGT-52535)
* 업데이트된 [!DNL Target] UI에서 작업 영역 간에 활동을 복사할 때 여러 문제가 해결되었습니다. 사용자가 소스 및 대상 작업 영역 모두에서 &quot;[!UICONTROL Approver]&quot; 역할을 가지고 있더라도 고객 액세스, 특히 라이브 활동 및 잘못된 권한 유효성 검사와 관련된 오류가 발생했습니다. (TGT-53002)
* 업데이트된 UI에서 동일한 작업 영역 내의 활동을 복사하는 경우 관련 오퍼 및 대상이 불필요하게 중복되는 문제를 해결했습니다. (TGT-53457)
* 임시(익명) 대상이 기본이 아닌 작업 영역 간에 또는 기본이 아닌 작업 영역에서 기본 작업 영역으로 올바르게 복사되지 않는 문제를 해결했습니다. 이전 업데이트에서는 기본이 아닌 동일한 작업 영역 시나리오에 대해 적절한 중복을 보장했지만, 이 개선 사항은 여러 작업 영역에 걸쳐 있는 결합된 대상 구성을 유지하는 데 중점을 둡니다. 이 수정 사항은 모든 작업 영역 전환에서 일관된 대상 동작과 정확한 타겟팅을 보장합니다. (TGT-53268)

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
