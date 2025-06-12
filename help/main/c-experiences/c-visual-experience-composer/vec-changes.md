---
keywords: 시각적 경험 작성기;vec;wysiwyg
description: Adobe Target 25.2.1 릴리스(2025년 2월 17일)에서 VEC(시각적 경험 작성기)에 도입된 변경 사항을 이해합니다.
title: 새로운 시각적 경험 작성기 (VEC)에는 어떤 변경 사항이 도입됩니까?
feature: Visual Experience Composer (VEC)
exl-id: 4c7a5657-93d9-4355-9d2b-c992b36bcb50
source-git-commit: 3dab3c070eecb415136d880ab1a4326dfe8856d8
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer]개 변경

[!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 이전 버전과 업데이트된 버전의 차이점에 대해 설명합니다.

>[!IMPORTANT]
>
>업데이트된 [!UICONTROL Visual Editing Composer]에는 [!DNL Chrome Web Store]에서 사용할 수 있는 [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper] 확장 ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)이(가) 필요합니다.

VEC는 기존 활동을 작성하거나 편집할 때 표시됩니다.

![VEC(시각적 경험 작성기)](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## VEC에 대한 주요 변경 사항

다음 섹션에서는 이전 버전과 비교하여 업데이트된 VEC의 주요 변경 사항에 대해 설명합니다.

### [!UICONTROL Experiences] 레일

이전 버전과 마찬가지로 [!UICONTROL Experiences] 레일은 VEC 왼쪽에 남아 있습니다. [!UICONTROL Experiences] 레일을 축소할 수 없습니다.

![경험 레일](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

[!UICONTROL Experiences] 레일을 사용하여 경험을 만들거나 이름을 바꾸거나 제거할 수 있습니다. 새 경험을 추가하려면 **[!UICONTROL Add]** 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg))을 클릭하십시오. 경험을 복제, 삭제 또는 리디렉션하려면 [!UICONTROL More Actions] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭하십시오.

### [!UICONTROL Components] 레일(신규)

새 [!UICONTROL Components] 레일을 사용하여 웹 페이지에 여러 구성 요소를 추가하고 필요에 따라 편집할 수 있습니다.

![구성 요소 레일](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

새 구성 요소를 추가하려면 삽입하려는 [!UICONTROL Components] 레일의 구성 요소를 [!UICONTROL Design] 캔버스의 기존 페이지 요소 위로 드래그합니다. 그런 다음 선택한 요소 뒤의 앞에 구성 요소를 삽입하도록 선택합니다.

이전 VEC 버전과 비교할 때 선택한 요소를 구성 요소로 바꿀 수 없습니다.

### [!UICONTROL Modifications] 레일

[!UICONTROL Modifications] 레일을 열려면 [!UICONTROL Components] 레일에서 [!UICONTROL Show Modifications] 아이콘(![수정 사항 레일 표시](/help/main/assets/icons/History.svg))을 클릭합니다. [!UICONTROL Modifications] 레일이 편집 캔버스의 오른쪽에서 왼쪽으로 위치가 변경되었습니다.

![수정 레일](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

[!UICONTROL Modifications] 레일에는 VEC에서 페이지에 적용된 모든 변경 내용이 표시되며, 이를 통해 CSS 선택기, Mbox 및 사용자 지정 코드와 같은 추가 변경 내용을 적용할 수 있습니다.

수정 사항을 추가하거나, 모든 수정 사항을 삭제하거나, 모든 잘못된 수정 사항을 삭제하려면 [!UICONTROL More Options] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭하십시오. 대량 작업을 수행하려면 [!UICONTROL Select]을(를) 클릭하십시오. [!UICONTROL Apply to All Pages] 또는 [!UICONTROL Delete].

[!UICONTROL Modifications] 레일을 다시 표시하려면 [!UICONTROL Modifications] 레일에서 [!UICONTROL Hide Modifications] 아이콘(![수정 사항 레일 표시](/help/main/assets/icons/History.svg))을 클릭하십시오.

### [!UICONTROL Properties] 레일(신규)

[!UICONTROL Properties] 레일을 사용하면 해당 요소가 HTML 요소인지 또는 [!DNL Target]과(와) 관련된 개체(예: 권장 사항 또는 오퍼)인지 여부에 관계없이 페이지에서 선택한 요소의 속성을 변경할 수 있습니다.

![속성 레일](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

레일 상단의 아이콘을 클릭하여 HTML 코드를 편집하거나 요소를 삭제, 복제 또는 숨깁니다. [!UICONTROL Modifications] 레일에 변경 내용이 나타납니다.

![속성 아이콘](/help/main/c-experiences/c-visual-experience-composer/assets/options-icons.png)

오른쪽 레일에서 [!UICONTROL Properties] 레일을 접을 수 있습니다. [!UICONTROL Properties] 레일을 축소하거나 표시하려면 레일의 오른쪽에 있는 [!UICONTROL Show/Hide Properties] 아이콘(![속성 아이콘](/help/main/assets/icons/Propertie.svg))을 클릭합니다.

### 활동 설정/구성

디자인 캔버스 위에 표시된 [!UICONTROL Configure] 아이콘(![구성 아이콘](/help/main/assets/icons/Setting.svg))을 클릭하여 활동 속성 메뉴를 표시합니다.

![활동 구성 옵션](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

다양한 옵션을 사용하여 속성을 지정하고, 페이지 전달 규칙을 편집하고, 사이트 환경 설정을 지정하고, 페이지를 추가로 추가하고, 다중 페이지 또는 여러 대상 활동을 활성화 또는 비활성화할 수 있습니다. [!UICONTROL Properties] 할당은 [[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) 기능입니다.

위치 및 기능은 이전 VEC UI와 유사합니다.

### [!UICONTROL Design]/[!UICONTROL Browse] 모드

[!UICONTROL Properties] 레일의 맨 위에 표시된 [!UICONTROL Design]/[!UICONTROL Browse] 전환기를 사용하여 디자인과 찾아보기 모드를 전환합니다.

![디자인 및 찾아보기 전환](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

[!UICONTROL Browse] 모드를 사용하여 사이트를 탐색하고 업데이트할 보기 또는 페이지를 선택하십시오. 변경 내용을 추가하거나 편집하려면 [!UICONTROL Design] 모드로 다시 전환하십시오.

### [!UICONTROL Undo]/[!UICONTROL Redo]

[!UICONTROL Undo] 아이콘(![실행 취소 아이콘](/help/main/assets/icons/Undo.svg))을 클릭하여 변경 내용을 실행 취소할 수 있습니다.

![VEC의 실행 취소 아이콘](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

작업을 다시 실행하려면 실행 취소/[!UICONTROL Redo] 단추 그룹을 확장하고 [!UICONTROL Redo]을(를) 선택합니다.

### [!UICONTROL Design] 캔버스

[!UICONTROL Design] 캔버스를 사용하면 화면 맞춤, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape] 및 [!UICONTROL Mobile Portrait]을(를) 포함한 뷰포트를 선택할 수 있습니다.

![뷰포트 옵션](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

또한 업데이트된 VEC를 사용하면 적절한 아이콘(![확대 아이콘](/help/main/assets/icons/ZoomIn.svg) 또는 ![축소 아이콘](/help/main/assets/icons/ZoomOut.svg))을 클릭하여 확대하거나 축소할 수 있습니다.

## UI 변경 사항을 보여 주는 시각적 일러스트레이션

다음 그림은 업데이트된 VEC에 대한 높은 수준의 UI 변경 사항을 보여줍니다. 그림 맨 위에는 업데이트된 VEC UI가 표시되고 맨 아래에 이전 UI가 표시됩니다. 화살표는 다양한 요소가 이동한 위치를 보여 줍니다.

이미지를 클릭하여 브라우저의 전체 너비로 확장합니다.

![VEC 비교-이전 UI에 대한 새로운 기능](/help/main/c-experiences/c-visual-experience-composer/assets/vec-comparison.png){width="600" zoomable="yes"}

## 업데이트된 UI에 대한 추가 정보

* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!UICONTROL Activities], [!UICONTROL Recommendations] 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.

* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!UICONTROL Offers Library]에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.

* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.

* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.

* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.