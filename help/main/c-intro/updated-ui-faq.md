---
keywords: target 사용자 인터페이스;사용자 인터페이스;ui;자주 묻는 질문;faq
description: 업데이트된  [!DNL Target]t 사용자 인터페이스에 대한 질문과 대답입니다.
title: 업데이트된 [!DNL Target] UI에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Overview
exl-id: 75db4791-ca51-472d-99dd-583f7a74b222
source-git-commit: 6cba2e93d61d3044d1bf7ce2f5bb6cc1f2d71e4a
workflow-type: tm+mt
source-wordcount: '1875'
ht-degree: 1%

---

# [!DNL Target] UI 업데이트 FAQ

2025년에 새로 설계된 [!DNL Adobe Target] 사용자 인터페이스는 모든 사용자에게 보다 깨끗하고 직관적인 환경을 제공합니다. 이 FAQ에서는 탐색 변경, 기능 배치 및 임시 UI 토글 제거를 포함하여 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 주요 업데이트를 다룹니다. 마케터, 개발자 또는 관리자이든, 원활한 전환과 스마트한 워크플로우에 대한 안내서입니다.

## Target UI 버전 사용 중단 토글 타임라인이 업데이트되었습니까?

+++세부 정보 보기
[!DNL Target] 팀은 토글 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능을 제공하고 있습니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다.

![Target UI 버전 전환](/help/main/r-release-notes/assets/toggle.png)

롤아웃이 완료되면 토글이 제거되고 모든 사용자가 업데이트된 UI로 영구적으로 전환됩니다. [!DNL Adobe]은(는) 이 기능이 곧 단계적으로 중단될 예정이므로 미리 계획하는 것이 좋습니다.

### 사용 중단 타임라인

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

### UI 전환 동작 제한 사항 {#limitations}

다음 정보는 버전 토글을 사용할 때 알아 두어야 할 제한 사항에 대해 설명합니다.

* **새 활동의 가시성**: 기존 UI로 다시 전환하면 업데이트된 UI에서 만들어진 활동이 표시되지 않습니다.
* **기존 활동 편집**: 업데이트된 UI를 사용하는 동안 기존 활동(원래 기존 UI에서 만들어짐)에 대한 변경 사항이 웹 사이트에 게시됩니다. 그러나 다시 전환하는 경우 이러한 업데이트가 이전 UI에 표시되지 않습니다. 이전 UI에서 수행한 마지막 업데이트만 표시됩니다.
* **활동 세부 정보의 일관성**: 사용하는 UI에 관계없이 가장 최근의 변경 내용이 라이브 웹 사이트에 반영됩니다. 하지만 기존 UI에는 해당 버전 내에서 변경된 최신 변경 사항만 표시됩니다. 업데이트된 UI에서 편집된 활동이 기존 UI에 표시되는 것과 다른 경우 이 상황이 혼동을 일으킬 수 있습니다.

### 업데이트된 UI에 대해 알아볼 수 있는 추가 리소스

* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.
* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!DNL Target], [!UICONTROL Activities] 및 [!UICONTROL Recommendations]&#x200B;(VEC)에 대한 [!UICONTROL Visual Experience Composer]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!DNL Target]에 대한 [!UICONTROL Offers Library]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.
* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.
* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

+++

## 업데이트된 [!DNL Target] UI에 대한 자세한 정보는 어디에서 찾을 수 있습니까?

+++세부 사항
다음 리소스는 업데이트된 [!DNL Target] UI에 대한 자세한 정보를 제공합니다.

* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!DNL Target]에 대한 [!UICONTROL Offers Library]의 주요 UI 변경 사항에 대한 요약을 제공합니다.

* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.

* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.

* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

+++

## 업데이트된 UI를 현재 모든 [!DNL Target] 고객, [!UICONTROL Standard] 및 [!UICONTROL Premium]이(가) 사용할 수 있습니까?

+++세부 사항
업데이트된 UI는 모든 [!DNL Target] 고객, [!UICONTROL Standard] 및 [!UICONTROL Premium]에서 사용할 수 있습니다. 업그레이드된 라이센스나 SKU는 필요하지 않습니다.

임시 UI 버전 전환 롤아웃 및 사용 중단에 대한 자세한 내용은 [알아야 하는 시간에 민감한 업데이트](/help/main/r-release-notes/release-notes.md#time-sensitive)를 참조하십시오.

+++

## 기존 UI가 더 이상 사용되지 않기 전에 현재 버그 목록이 수정됩니까?

+++세부 사항
[!DNL Target] 팀이 새 UI 롤아웃과 관련된 문제를 적극적으로 해결하고 있습니다. 업데이트 및 지속적인 개선 사항은 릴리스 정보에 자세히 설명되어 있습니다.

임시 UI 버전 전환 롤아웃 및 사용 중단에 대한 자세한 내용은 [알아야 하는 시간에 민감한 업데이트](/help/main/r-release-notes/release-notes.md#time-sensitive)를 참조하십시오.

+++

## 고객이 기존 UI를 계속 사용하고자 하는 경우, UI 버전을 계정에 대해 유지되도록 전환할 수 있습니까?

+++세부 사항
UI 버전 전환은 전환 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능입니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다. 롤아웃이 완료되면 토글이 제거되고 모든 사용자가 업데이트된 UI로 영구적으로 전환됩니다.

UI 버전 토글을 사용하는 데에는 새 활동의 가시성, 기존 활동의 편집 및 활동 세부 사항의 일관성을 비롯한 몇 가지 제한 사항이 있습니다.

자세한 내용은 [알고 있어야 하는 시간에 민감한 업데이트](/help/main/r-release-notes/release-notes.md#time-sensitive)를 참조하십시오.

++++

## 전체 롤아웃이 완료될 때까지 [!DNL Adobe]에서 업데이트된 UI로의 마이그레이션을 연기할 수 있습니까?

+++세부 사항
[!DNL Target]은(는) UI 마이그레이션 타이밍을 지연하거나 사용자 지정하는 옵션을 제공하지 않습니다. 고객은 단계적으로 전환되며 [!DNL Adobe]에서 롤아웃 일정을 관리합니다. 최신 업데이트는 릴리스 노트를 참조하십시오.

UI 버전 토글을 사용하는 데에는 새 활동의 가시성, 기존 활동의 편집 및 활동 세부 사항의 일관성을 비롯한 몇 가지 제한 사항이 있습니다.

자세한 내용은 [알고 있어야 하는 시간에 민감한 업데이트](/help/main/r-release-notes/release-notes.md#time-sensitive)를 참조하십시오.

+++

## 업데이트된 VEC는 옵션의 재배열, 크기 조정, 이동, 숨기기 및 제거를 어떻게 처리하며 이러한 옵션은 기존 VEC와 어떻게 다릅니까? {#options}

+++세부 사항
**[!UICONTROL Rearrange*]*: 이전 VEC에서 다시 정렬 옵션은 오버레이를 사용하여 사용자가 해당 형제 그룹 내의 요소를 다시 배치할 수 있도록 했습니다. 움직임은 형제 요소 간의 순서를 바꾸는 것으로 한정되었다.

업데이트된 VEC에서 이 기능은 앞으로 이동 및 뒤로 이동 작업을 통해 간소화됩니다. 이러한 컨트롤은 겹침 순서에서 요소를 앞이나 뒤로 이동하여 레이아웃에서 요소의 위치를 가로와 세로 모두 조정합니다.

**크기 조정**: [!UICONTROL Resize] 기능은 [!UICONTROL Properties] 섹션 아래의 [!UICONTROL Size] 패널에 있습니다. 사용자는 요소의 너비와 높이를 직접 조정할 수 있습니다. 고급 설정에는 다음이 포함됩니다.

* 최소/최대 너비 및 높이 컨트롤
* 오버플로 비헤이비어 설정
* 미디어 요소에 대한 오브젝트 맞춤 옵션

이러한 도구를 사용하면 요소 치수 및 레이아웃 동작을 정밀하게 제어할 수 있습니다.

**이동**: [!UICONTROL Move] 옵션은 [!UICONTROL Properties] 섹션 아래의 [!UICONTROL Position] 패널에 있습니다. 이 옵션을 사용하면 다음과 같은 작업을 수행할 수 있습니다.

* 요소의 위치(예: 절대, 상대, 고정)를 설정합니다
* 계층화를 위한 z-색인 정의
* 위치 지정 유형 선택

업데이트된 [!UICONTROL Properties] 레일은 사용자 지정 인라인 스타일도 지원하므로 사전 설정 옵션이 레이아웃 요구 사항에 맞지 않을 때 유연성을 제공합니다.

**[!UICONTROL Hide]**: [!UICONTROL Hide] 기능은 [!UICONTROL Properties] 패널에 있습니다. 요소를 선택한 후 [!UICONTROL Hide Element]을(를) 클릭하여 삭제하지 않고 보기에서 제거합니다. 이 기능은 디자인 또는 미리 보기 중 가시성을 관리하는 데 유용합니다.

**[!UICONTROL Remove]**: [!UICONTROL Remove] 기능은 [!UICONTROL Properties] 패널을 통해 액세스할 수 있습니다. 요소를 선택한 후 요소 제거 를 클릭하여 페이지에서 요소를 삭제합니다. 이 작업은 레이아웃에서 요소를 영구적으로 제거합니다.

+++

## [!UICONTROL Components] 패널을 확대할 수 있도록 [!UICONTROL Modifications], [!UICONTROL Properties] 및 [!UICONTROL Design] 레일을 축소할 수 있습니까? {#collapse}

+++세부 사항

예. 이러한 레일을 축소하여 [!UICONTROL Design] 캔버스를 확장하면 보다 쉽게 편집할 수 있습니다. 방법은 다음과 같습니다.

>[!NOTE]
>
>[!UICONTROL Show Components] 아이콘(![구성 요소 표시 아이콘](/help/main/assets/icons/Add.svg))과 [!UICONTROL Show Modifications] 아이콘(![수정 사항 표시 레일](/help/main/assets/icons/History.svg))은 적절한 옵션을 표시하도록 전환합니다.

**[!UICONTROL Components] 레일 축소**

[!UICONTROL Components] 레일이 열려 있는 동안 [!UICONTROL Design] 레일을 축소하고 [!UICONTROL Components] 캔버스를 확대하려면 (![구성 요소 표시 아이콘](/help/main/assets/icons/Add.svg)) 아이콘을 클릭합니다.

**[!UICONTROL Modifications] 레일 축소**

[!UICONTROL Modifications] 레일이 열려 있는 동안 [!UICONTROL Design] 레일을 축소하고 [!UICONTROL Modifications] 캔버스를 확대하려면 [!UICONTROL Show Modifications] 아이콘(![수정 사항 레일 표시](/help/main/assets/icons/History.svg)) 아이콘을 클릭합니다.

**[!UICONTROL Properties] 레일 축소**

[!UICONTROL Properties] 레일을 축소하고 [!UICONTROL Design] 캔버스를 확대하려면 레일의 오른쪽에 있는 [!UICONTROL Show/Hide Properties] 아이콘(![속성 아이콘](/help/main/assets/icons/Propertie.svg))을 클릭하여 [!UICONTROL Properties] 레일을 축소하거나 표시합니다.

+++

## [!UICONTROL Save as Draft] 및 [!UICONTROL Syncing] 상태를 계속 사용할 수 있습니까?

+++세부 사항
사용자 인터페이스에 대한 최신 업데이트를 통해 [!UICONTROL Save as Draft] 및 [!UICONTROL Syncing] 상태를 더 이상 사용할 수 없습니다. 자세한 내용은 [의 &#x200B;](/help/main/c-activities/activities.md#filters)활동 목록에 필터 적용&#x200B;*[!UICONTROL Activities overview]* 아래의 상태를 참조하십시오.

+++

## 활동이 기존 UI 또는 업데이트된 UI에서 생성 또는 편집되었는지 어떻게 알 수 있습니까?

+++세부 사항
업데이트된 UI에서 만들어지거나 편집된 활동은 동일한 안내가 있는 3단계 워크플로우를 따르며 UI별 메타데이터 또는 레거시 생성 활동에 없는 서식이 포함될 수 있습니다. 인터페이스에 표시되는 태그나 레이블이 없지만 레이아웃, 구조 또는 사용 가능한 옵션(예: 향상된 타겟팅 또는 미리보기 기능)의 차이는 사용된 UI를 나타낼 수 있습니다. 자세한 식별은 활동의 변경 기록을 확인하거나 구현 로그를 참조하십시오.

+++

## 기존 UI에서 오퍼를 만드는 것과 업데이트된 UI의 차이점은 무엇입니까? 추가 속성이 필요합니까?

+++세부 사항
[!UICONTROL Offer Library] UI에는 모든 오퍼에 대해 일관된 특성 정의가 필요합니다. 활동 전용(애드혹) 오퍼를 생성할 때 사용자는 오퍼 이름도 지정해야 합니다. 이 정보는 [!UICONTROL Form-based Experience Composer]에 표시되므로 코드나 콘텐츠를 검토하지 않고도 오퍼를 보다 쉽게 식별할 수 있습니다.

+++

## 업데이트된 UI의 오퍼 미리보기 링크는 어떻게 됩니까?

+++세부 사항
선택한 조각에 해당하는 정보 아이콘([!UICONTROL Experience Fragment]정보 아이콘[!UICONTROL Quick Info] )을 클릭할 때 표시되는 ![&#x200B; 팝오버에서 &#x200B;](/help/main/assets/icons/InfoOutline.svg) 미리 보기 링크를 사용할 수 있습니다.

+++

## 업데이트된 UI로 기존 활동을 편집할 때 [!UICONTROL Enhanced Experience Composer]을(를) 비활성화해야 합니다. [!DNL Adobe]님이 다른 고객과 유사한 행동을 관찰했습니까?

+++세부 사항
예. [!DNL Adobe Experience Cloud] [!DNL Visual Editing Helper extension]을(를) 사용하는 경우 [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC) 을(를) 비활성화해야 할 수 있습니다.

추가 정보는 [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)을 참조하십시오.

+++

## 허용 목록에 추가를 위한 새로운 IP들의 세부사항을 알려주실 수 있나요?

+++세부 사항
허용 목록에 추가하다할 수 있는 IP 주소에 대한 자세한 내용은 다음 문서를 참조하십시오.

* **향상된 경험 작성기(EEC)**: [EEC가 공용 IP에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#section_D29E96911D5C401889B5EACE267F13CF)(*향상된 경험 작성기 관련 문제 해결*)
* **[!UICONTROL Recommendations]**: [권장 사항 피드 처리 서버에서 사용하는 IP 주소](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md)를 참조하세요.

+++

## 환경이 새 권장 사항 UI에서 기본적으로 스테이징으로 재설정됩니까?

+++세부 사항
이제 환경은 고객이 사용한 마지막 환경으로 기본 설정됩니다. 환경을 전환하려면 [!UICONTROL Environment] UI의 오른쪽 위 모서리에 있는 [!UICONTROL Catalog Search] 선택기를 사용하십시오.

![환경 스위치](/help/main/c-intro/assets/environmnent.png)

+++

## [!DNL Adobe Analytics] 또는 [!DNL Customer Journey Analytics]을(를) [!DNL Target]에 연결하는 것이 얼마나 복잡합니까?

+++세부 사항
[!DNL Adobe Analytics]&#x200B;(AA) 또는 [!DNL Customer Journey Analytics]&#x200B;(CJA)을(를) [!DNL Target]과(와) 통합하는 범위는 현재 설정에 따라 중간에서 고급 작업까지 다양할 수 있습니다. [!DNL Adobe Experience Platform]을(를) 사용하고 [!DNL Platform Web SDK]을(를) 구현한 경우 통합이 보다 간소화됩니다. 그러나 at.js 또는 AppMeasurement을 사용하는 기존 구현에는 다음을 포함한 추가 구성이 필요할 수 있습니다.

* [Analytics for Target(A4T) 통합 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)
* [[!DNL Target] 에서  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md)보고 통합.
* 보고서 세트 및 데이터 보기 매핑
* 일관된 ID 확인(ECID)
* 데이터 수집 및 속성 설정 유효성 검사

+++
