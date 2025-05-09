---
keywords: 시각적 경험 작성기 선택 사항;경험 작성기 선택 사항;경험 선택 사항;텍스트 편집;html 편집;텍스트/html 편집;배경색 편집;배경색;요소 삽입;링크 편집;링크;시각적 경험 작성기 링크;css 클래스 편집;오퍼 바꾸기;오퍼 바꾸기;이미지 교체;이미지 바꾸기;항목 제거;항목 제거;항목 숨기기;항목 숨기기;재배열;요소 이동;요소 이동;요소 크기 조정;요소 크기 조정;요소;선택 확장;이 링크로 이동;링크 탐색;링크 탐색;탐색;링크;실행 취소;다시 실행;실행 취소/다시 실행;사용자 지정 이벤트;웹 구성 요소;오퍼 결정;오퍼 의사 결정
description: ' [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)에서 사용할 수 있는 옵션을 살펴보십시오.'
title: '[!UICONTROL Visual Experience Composer]​(VEC) 옵션을 사용하려면 어떻게 해야 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: b1fb49d78b3a159c16e8ebb855ff175c26681da6
workflow-type: tm+mt
source-wordcount: '1861'
ht-degree: 9%

---

# 시각적 경험 작성기 옵션

[!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 업데이트된 UI 및 해당 옵션에 대해 설명합니다.

>[!TIP]
>
>업데이트된 VEC가 기존 VEC와 어떻게 다른지 알아보려면 [시각적 경험 작성기 변경 사항](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)을 참조하십시오.

>[!IMPORTANT]
>
>업데이트된 [!UICONTROL Visual Editing Composer]에는 [!DNL Chrome Web Store]에서 사용할 수 있는 [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper] 확장 ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)이(가) 필요합니다.

VEC는 기존 활동을 작성하거나 편집할 때 표시됩니다.

![VEC(시각적 경험 작성기)](/help/main/c-experiences/c-visual-experience-composer/assets/new-vec.png)

## VEC UI 개요

다음 섹션에서는 [!UICONTROL A/B Test] 활동에 대해 업데이트된 VEC에서 사용할 수 있는 옵션에 대해 설명합니다. 옵션은 활동 유형에 따라 다릅니다.

### [!UICONTROL Experiences] 레일

[!UICONTROL Experiences] 레일이 VEC의 왼쪽 레일에 표시됩니다.

![경험 레일](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

[!UICONTROL Experiences] 레일을 사용하여 경험을 보거나, 만들거나, 이름을 바꾸거나, 제거할 수 있습니다.

[!UICONTROL Experiences] 레일에서 다음 옵션을 사용할 수 있습니다.

* **경험 보기**: 경험을 보려면 원하는 경험을 클릭하여 [!UICONTROL Design] 캔버스에 표시하십시오.
* **경험 추가**: **[!UICONTROL Add]** 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg))을 클릭하여 새 경험을 추가합니다. 원하는 대로 새 경험을 구성합니다.
* **경험 이름 바꾸기**: **[!UICONTROL Rename]** 아이콘(![이름 바꾸기 아이콘](/help/main/assets/icons/Rename.svg))을 클릭하여 [!UICONTROL Rename Experience] 대화 상자를 표시합니다. 새 이름을 지정한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
* **경험 복제, 삭제 또는 리디렉션**: **[!UICONTROL More Actions]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]** 또는 **[!UICONTROL Redirect to URL]**&#x200B;을(를) 선택합니다.

### 활동 설정/구성 {#settings}

[!UICONTROL Design] 캔버스 위에 표시된 [!UICONTROL Configure] 아이콘(![구성 아이콘](/help/main/assets/icons/Setting.svg))을 클릭하여 활동 속성 메뉴를 표시합니다.

![활동 구성 옵션](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

다음 옵션을 사용할 수 있습니다.

* **[!UICONTROL Properties]**: 활동에 속성을 할당하거나 활동에서 속성을 제거합니다. [!UICONTROL Properties]은(는) ([[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) 기능입니다. 자세한 내용은 [엔터프라이즈 사용자 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 참조하십시오.
* **[!UICONTROL Page Delivery]**: 사이트의 유사한 페이지에 동일한 경험을 포함하십시오. 페이지 템플릿을 사용하여 페이지에 구조를 제공하거나 페이지에 유사한 요소가 포함되어 있는 경우 유사한 구조의 페이지 요소에서 또는 전체 도메인에서 변형을 테스트할 수 있습니다. 자세한 내용은 [유사한 페이지에 동일한 경험 포함](/help/main/c-experiences/c-visual-experience-composer/temtest.md)을 참조하십시오.
* **[!UICONTROL Site Preferences]**: 사이트 환경 설정을 구성하여 [!DNL Target]에서 CSS 선택기를 생성하는 방법을 지정하십시오. 자세한 내용은 [구성 [!UICONTROL Visual Experience Composer]](/help/main/administrating-target/visual-experience-composer-set-up.md)의 _CSS 선택기_&#x200B;를 참조하십시오.
* **추가 페이지 추가**: 활동에 페이지를 추가하여 여러 페이지에 걸쳐 각 페이지별 디자인을 사용하여 스토리를 만들 수 있는 다중 페이지 활동을 만듭니다. 자세한 내용은 [다중 페이지 활동](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md)을 참조하세요.
* **단일 대상**: 활동에 단일 대상을 사용합니다.
* **여러 대상**: 활동에 여러 대상을 할당합니다. 대상자 추가 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg) )을 클릭한 다음, 목록에서 대상자를 하나 이상 선택합니다. [!UICONTROL Add Audiences] 대화 상자에서 [대상을 결합](/help/main/c-target/combining-multiple-audiences.md)하거나 [새 대상을 만들기](/help/main/c-target/c-audiences/create-audience.md)할 수도 있습니다.

### [!UICONTROL Design]/[!UICONTROL Browse] 모드

디자인 캔버스 위에 표시된 [!UICONTROL Design]/[!UICONTROL Browse] 전환을 사용하여 디자인과 찾아보기 모드 간에 전환합니다.

![디자인 및 찾아보기 전환](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

[!UICONTROL Browse] 모드를 사용하여 사이트를 탐색하고 업데이트할 보기 또는 페이지를 선택하십시오. 변경 내용을 추가하거나 편집하려면 [!UICONTROL Design] 모드로 다시 전환하십시오.

### [!UICONTROL Undo]/[!UICONTROL Redo]

[!UICONTROL Undo] 아이콘(![실행 취소 아이콘](/help/main/assets/icons/Undo.svg))을 클릭하여 변경 내용을 실행 취소할 수 있습니다.

![VEC의 실행 취소 아이콘](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

작업을 다시 실행하려면 실행 취소/[!UICONTROL Redo] 단추 그룹을 확장하고 [!UICONTROL Redo]을(를) 선택합니다.

### [!UICONTROL Components] 레일

새 [!UICONTROL Components] 레일을 사용하여 웹 페이지에 여러 구성 요소를 추가하고 필요에 따라 편집할 수 있습니다.

![구성 요소 레일](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

>[!NOTE]
>
>이 영역에 [!UICONTROL Components] 레일 대신 [!UICONTROL Modifications] 레일이 표시되면 **[!UICONTROL Show Components]** 아이콘(![구성 요소 표시 아이콘](/help/main/assets/icons/Add.svg))을 클릭합니다. [!UICONTROL Show Components] 아이콘(![구성 요소 표시 아이콘](/help/main/assets/icons/Add.svg))과 [!UICONTROL Show Modifications] 아이콘(![수정 사항 표시 레일](/help/main/assets/icons/History.svg))은 적절한 옵션을 표시하도록 전환합니다.

경험에 새 구성 요소를 추가하려면 다음 작업을 수행하십시오.

1. 추가하려는 구성 요소를 클릭하여 강조 표시합니다.

   사용 가능한 구성 요소는 논리 컨테이너로 그룹화됩니다.

   * [!UICONTROL Basic]
      * [!UICONTROL Divider]
      * [!UICONTROL HTML]
      * [!UICONTROL Image]
   * [!UICONTROL Text]
      * [!UICONTROL Heading]
      * [!UICONTROL Paragraph]
      * [!UICONTROL Link]
   * [!UICONTROL Dynamic]
      * [[!UICONTROL Recommendation]](/help/main/c-recommendations/recommendations-as-an-offer.md)
      * [[!UICONTROL Experience Fragment]](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md)
      * [[!UICONTROL HTML Offer]](/help/main/c-experiences/c-manage-content/manage-content.md)

1. 구성 요소를 [!UICONTROL Design] 캔버스의 기존 페이지 요소 위로 드래그합니다.
1. 선택한 요소 뒤에 구성 요소를 삽입하려면 선택합니다.

   이전 VEC 버전과 비교할 때 선택한 요소를 구성 요소로 바꿀 수 없습니다.

### [!UICONTROL Modifications] 레일

[!UICONTROL Modifications] 레일을 열려면 [!UICONTROL Components] 레일에서 [!UICONTROL Show Modifications] 아이콘(![수정 사항 레일 표시](/help/main/assets/icons/History.svg))을 클릭합니다.

![수정 레일](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

>[!NOTE]
>
>[!UICONTROL Show Components] 아이콘(![구성 요소 표시 아이콘](/help/main/assets/icons/Add.svg))과 [!UICONTROL Show Modifications] 아이콘(![수정 사항 표시 레일](/help/main/assets/icons/History.svg))은 적절한 옵션을 표시하도록 전환합니다.

[!UICONTROL Modifications] 레일에는 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 페이지에 적용된 모든 변경 내용이 표시되며 추가 변경을 수행할 수 있습니다(CSS 선택기, Mbox, 사용자 지정 코드 등).

수정 사항을 추가하거나, 모든 수정 사항을 삭제하거나, 모든 잘못된 수정 사항을 삭제하려면 레일 헤더의 **[!UICONTROL More Options]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭하십시오. 대량 작업을 수행하려면 [!UICONTROL Select]을(를) 클릭하십시오. [!UICONTROL Apply to All Pages] 또는 [!UICONTROL Delete].

각 수정 사항 옆의 **[!UICONTROL More Options]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg) )을 클릭하여 해당 정보를 보거나, 수정 사항을 삭제하거나, 수정 사항을 더 많은 보기에 적용합니다.

### [!UICONTROL Design] 캔버스

[!UICONTROL Design] 캔버스를 사용하면 화면 맞춤, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape] 및 [!UICONTROL Mobile Portrait]을(를) 포함한 뷰포트를 선택할 수 있습니다. 기본적으로 캔버스는 [관리](/help/main/administrating-target/visual-experience-composer-set-up.md) 섹션에 정의된 뷰포트와 함께 페이지에 맞게 화면에 표시됩니다.

![뷰포트 옵션](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

적절한 아이콘(![확대 아이콘](/help/main/assets/icons/ZoomIn.svg) 또는 ![축소 아이콘](/help/main/assets/icons/ZoomOut.svg))을 클릭하여 확대하거나 축소할 수도 있습니다.

[!UICONTROL Design] 캔버스에서 페이지 요소를 클릭하면 메뉴에 해당 요소 유형에 사용할 수 있는 옵션이 표시됩니다. 또한 페이지 구조를 쉽게 탐색할 수 있는 DOM 경로가 페이지 하단에 표시됩니다.

다양한 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 작업은 작업을 보다 빠르고 효율적으로 수행할 수 있도록 적절한 메뉴 옵션으로 그룹화됩니다.

![VEC 선택 사항 메뉴](/help/main/c-experiences/c-visual-experience-composer/assets/vec-options.png)

>[!NOTE]
>
>사용 가능한 옵션은 만들거나 편집하는 활동 유형과 요소에 따라 다릅니다. [!UICONTROL A/B Test] 활동에서 이미지 및 오퍼 편집에 대한 자세한 내용은 아래의 [캔버스를 사용하여 요소 편집](#design)을 참조하십시오.[!UICONTROL Design]

### [!UICONTROL Properties] 레일

[!UICONTROL Properties] 레일을 사용하면 해당 요소가 HTML 요소인지 또는 [!DNL Target]과(와) 관련된 개체(예: 권장 사항 또는 오퍼)인지 여부에 관계없이 페이지에서 선택한 요소의 속성을 변경할 수 있습니다.

![속성 레일](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

레일 상단의 아이콘을 클릭하여 HTML 코드를 편집하거나 요소를 삭제, 복제 또는 숨깁니다. [!UICONTROL Modifications] 레일에 변경 내용이 나타납니다.

오른쪽 레일에서 [!UICONTROL Properties] 레일을 접을 수 있습니다. [!UICONTROL Properties] 레일을 축소하거나 표시하려면 레일의 오른쪽에 있는 [!UICONTROL Show/Hide Properties] 아이콘(![속성 아이콘](/help/main/assets/icons/Propertie.svg))을 클릭합니다.

## [!UICONTROL Design] 캔버스를 사용하여 요소 편집 {#design}

다음 단원에서는 [!UICONTROL Design] 캔버스에서 이미지와 텍스트를 편집하는 방법을 보여 줍니다. 구성 요소, 수정 사항 및 속성 레일과 함께 디자인 캔버스에서는 활동을 위한 경험을 쉽게 만들 수 있는 강력한 도구를 제공합니다.

### 이미지 옵션

[!UICONTROL A/B Test] 활동에서 이미지를 클릭하면 VEC가 다음 그림과 유사합니다.

이미지가 선택된 ![VEC](/help/main/c-experiences/c-visual-experience-composer/assets/vec-image.png)

다음 요소를 삽입하려면 왼쪽의 [!UICONTROL Components] 프레임에서 구성 요소를 선택하십시오.

* 기본(구분선, HTML, 이미지).
* 텍스트(제목, 단락, 링크).
* 동적([권장 사항](/help/main/c-recommendations/recommendations-as-an-offer.md), [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML 오퍼).

이미지 맨 위에 있는 메뉴를 사용하여 다음을 수행할 수 있습니다.

* 링크를 삽입합니다( ![링크 삽입 아이콘](/help/main/assets/icons/Link.svg)).
* 이미지를 변경합니다(![이미지 선택 아이콘](/help/main/assets/icons/Images.svg)).
* 개인화 추가( ![Personalization 추가 아이콘](/help/main/assets/icons/PersonalizationField.svg) ).
* 이미지를 삭제합니다(![삭제 아이콘](/help/main/assets/icons/Delete.svg)).

오른쪽의 [!UICONTROL Properties] 창을 사용하면 이미지의 속성을 추가로 구성할 수 있습니다.

프레임 상단의 아이콘을 사용하면 다음 작업을 수행할 수 있습니다.

* HTML(![HTML 삽입 아이콘](/help/main/assets/icons/Code.svg) )를 편집합니다. 자세한 내용은 아래 [HTML 편집](#html)을 참조하십시오.
* 이미지를 복제합니다(![복제 아이콘](/help/main/assets/icons/Code.svg)).
* 이미지를 삭제합니다(![삭제 아이콘](/help/main/assets/icons/Delete.svg)).
* 이미지를 숨깁니다(![숨기기 아이콘](/help/main/assets/icons/VisibilityOff.svg)).

오른쪽 프레임의 옵션을 사용하면 다음 작업을 수행할 수 있습니다.

* CSS 클래스를 편집합니다.
* 이미지의 속성(소스, 제목, 대체 텍스트)을 구성합니다.
* 링크 URL을 편집합니다.
* 이미지의 크기(높이 및 너비)를 구성합니다. 이미지의 최소 및 최대 크기, 너비, 높이, 오버플로 및 개체 맞춤을 구성하려면 [!UICONTROL Show Advanced Options]을(를) 클릭하십시오.
* 페이지에서 이미지의 위치(절대, 고정, 상대, 정적 또는 고정)를 구성합니다.
* 여백 및 패딩을 포함하여 요소의 간격을 구성합니다.
* 요소의 효과(불투명도)를 구성합니다. 이미지의 세피아, 회색 음영, 대비, 밝기 및 흐림 값을 구성하려면 [!UICONTROL Show Advanced Options]을(를) 클릭합니다. 이미지를 반전하거나 회전할 수도 있습니다.
* 이미지의 인라인 스타일을 구성합니다.

### 텍스트 옵션

[!UICONTROL A/B Test] 활동에서 텍스트를 클릭하면 VEC가 다음 그림과 유사합니다.

텍스트가 선택된 ![VEC](/help/main/c-experiences/c-visual-experience-composer/assets/vec-text.png)

다음 요소를 삽입하려면 왼쪽의 [!UICONTROL Components] 프레임에서 구성 요소를 선택하십시오.

* 기본(구분선, HTML, 이미지).
* 텍스트(제목, 단락, 링크).
* 동적([권장 사항](/help/main/c-recommendations/recommendations-as-an-offer.md), [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML 오퍼).

[!UICONTROL Show Modifications] 아이콘(![수정 사항 표시 아이콘](/help/main/assets/icons/History.svg))을 클릭하여 경험에 대한 수정 사항을 표시합니다.

텍스트 요소의 맨 위에 있는 메뉴를 사용하여 다음을 수행할 수 있습니다.

* 텍스트 속성(제목 수준, 단락, 블록 인용 또는 고정 폭) 구성
* 텍스트 색상 선택(![텍스트 색상 아이콘](/help/main/assets/icons/TextColor.svg))
* 텍스트의 특성(굵게, 기울임꼴, 밑줄 또는 취소선)을 구성합니다(![텍스트 특성 선택 아이콘](/help/main/assets/icons/Text.svg)).
* 텍스트의 맞춤을 구성합니다(왼쪽, 가운데, 오른쪽, 양쪽 맞춤)(![텍스트 맞춤 아이콘](/help/main/assets/icons/TextAlignCenter.svg) ).
* 링크를 삽입합니다( ![링크 삽입 아이콘](/help/main/assets/icons/Link.svg)).
* 콘텐츠를 HTML 오퍼, [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) 또는 [권장 사항](/help/main/c-recommendations/recommendations-as-an-offer.md)(으)로 바꾸십시오.
* HTML(![HTML 삽입 아이콘](/help/main/assets/icons/Code.svg) )를 편집합니다.
* 개인화 추가( ![Personalization 추가 아이콘](/help/main/assets/icons/PersonalizationField.svg) ).
* 이미지를 삭제합니다(![삭제 아이콘](/help/main/assets/icons/Delete.svg)).

오른쪽의 [!UICONTROL Properties] 레일을 사용하여 텍스트의 속성을 추가로 구성할 수 있습니다.

프레임 상단의 아이콘을 사용하면 다음 작업을 수행할 수 있습니다.

* HTML(![HTML 삽입 아이콘](/help/main/assets/icons/Code.svg) )를 편집합니다. 자세한 내용은 아래 [HTML 편집](#html)을 참조하십시오.
* 텍스트를 복제합니다(![복제 아이콘](/help/main/assets/icons/Code.svg)).
* 텍스트를 삭제합니다(![삭제 아이콘](/help/main/assets/icons/Delete.svg)).
* 텍스트를 숨깁니다(![숨기기 아이콘](/help/main/assets/icons/VisibilityOff.svg)).

오른쪽 프레임의 옵션을 사용하면 다음 작업을 수행할 수 있습니다.

* CSS 클래스를 편집합니다.
* 텍스트의 배경색 및 이미지를 구성합니다.
* 텍스트의 타이포그래피(제목 스타일, 글꼴 크기, 글꼴 두께, 줄 높이, 정렬, 텍스트 색상, 텍스트 스타일(굵게, 기울임꼴, 밑줄 또는 취소선) 구성
* 글머리 기호, 번호 매기기 또는 A,B,C를 포함한 목록을 구성합니다.
* 테두리 색상을 선택합니다.
* 텍스트 상자의 크기(높이 및 너비)를 구성합니다. [!UICONTROL Show Advanced Options]을(를) 클릭하여 텍스트 상자의 최소 및 최대 크기, 너비, 높이, 오버플로 및 개체 맞춤을 구성합니다.
* 페이지에서 텍스트 상자의 위치(절대, 고정, 상대, 정적 또는 고정)를 구성하고 위쪽, 오른쪽, 아래쪽 및 왼쪽에서 픽셀 수를 설정합니다.
* 여백 및 패딩을 포함하여 요소의 간격을 구성합니다.
* 요소의 효과(불투명도)를 구성합니다. 이미지의 세피아, 회색 음영, 대비, 밝기 및 흐림 값을 구성하려면 [!UICONTROL Show Advanced Options]을(를) 클릭합니다. 텍스트를 반전하거나 회전할 수도 있습니다.
* 인라인 스타일을 구성합니다.

## HTML 편집

HTML 코드 외에도, 사용자 지정 자바스크립트를 편집하고 삽입할 수 있습니다.

[!UICONTROL A/B] 및 [!UICONTROL Experience Targeting] 활동에 대해 텍스트와 HTML을 편집할 때 여러 서식 있는 텍스트 서식 옵션을 사용할 수 있습니다. 글꼴을 선택하고, 글꼴 스타일을 선택하고, 텍스트 정렬을 변경하고, 기타 표준 텍스트 서식 옵션을 사용할 수 있습니다. HTML을 수정할 때 HTML의 코드 보기와 리치 편집 보기 간에 전환할 수 있습니다.

다음 HTML5 태그를 중첩할 수 있습니다.

| 태그 | 허용된 중첩 태그 |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

## DOM 경로를 사용하여 요소 탐색 {#dom-path}

페이지에서 요소를 클릭하면 VEC 옵션 메뉴가 표시됩니다. 또한 요소를 클릭하면 해당 DOM 경로가 페이지 하단에 표시됩니다.

![DOM 경로](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path-refresh.png)

DOM 경로가 표시되지 않으면 [!UICONTROL Show DOM] 아이콘(![DOM 아이콘 표시](/help/main/assets/icons/LayersBringToFront.svg))을 클릭합니다.

DOM 경로를 사용하여 선택한 요소(유형, ID 및 클래스)에 대한 정보를 빠르게 확인하고, DOM 경로로 위 또는 아래로 이동하여 원하는 요소를 선택할 수 있습니다.

<!--When you hover over the DOM path, a blue box highlights the corresponding element in the VEC. When you click the element, an orange box highlights the element and the VEC options menu displays, as explained above.-->

DOM 경로를 사용하여 VEC 내에서 상위 요소, 동일 수준의 요소 또는 하위 요소로 손쉽게 이동할 수 있습니다.

DOM 경로 기능은 [클릭 추적](/help/main/c-activities/r-success-metrics/click-tracking.md)을 설정할 때도 사용할 수 있습니다.

<!--## [!UICONTROL Edit]

The following options are available:

### [!UICONTROL Text/HTML] {#edit-text-html}

Change the HTML code for the element, such as the text for a text area, button, or link.

In addition to HTML code, you can edit and inject custom JavaScript.

Several rich text formatting options are available when editing text and HTML for [!UICONTROL A/B] and [!UICONTROL Experience Targeting] activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML.

The following HTML5 tags can be nested:

|Tag|Allowed Nested Tags|
| --- | --- |
|`<a>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>`|
|`<ins>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`|
|`<del>`|`<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>`|
|`<label>`|`<p>`|

### [!UICONTROL Background Color]

Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent.

**Note:** This option is not available for an element where a background image is set. 

### [!UICONTROL Styles] {#styles}

Use the [!UICONTROL Styles] panel to view or edit the value of existing styles for the selected element. You can also add additional styling.

To access the [!UICONTROL Styles] panel, click a page element from within the VEC, then click **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

The [!UICONTROL Styles] panel displays on the right side of the VEC. The panel contains a list of styles that lets you edit or add to the selected element. A real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

![Styles panel](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

As you apply different styles, you can always revert your changes by clicking the [!UICONTROL Revert] icon that displays at the top-right corner of the [!UICONTROL Styles] panel after you change any section. Clicking the [!UICONTROL Revert] icon reverts all changes on the current section's panel.

Expand each section to edit or add styles, as explained below. To save your changes, click the [!UICONTROL Back] icon at the top of the panel to return to the panel's main display, then click **[!UICONTROL Save]**. 

Blue dots on the main panel and next to each option on the various section panels indicate that you have changed the corresponding styles. This visual indicator makes it easy for you to review your changes before clicking [!UICONTROL Save].

>[!NOTE]
>
>Quick actions for layout changes, background color, resizing, and move are also available as separate actions in the VEC menu. These options can be used as separate actions or you can use the Styles menu, as explained here.

* **[!UICONTROL Background]**

  Change the background color and image.

  * Color (specify the color code or use the color picker)
  * Image (select an image from the image picker)
  * Image source (specify an external URL)
  * Attachment
    * Click the top drop-down list to select scroll, fixed, or local
    * Click the bottom drop-down list to select repeat, repeat-x, repeat-y, no-repeat, space, or round
  * Clip
    * Click the top drop-down list to select border-box, padding-box, content-box, or text
    * Click the bottom drop-down list to select auto audio or audio

* **[!UICONTROL Typography]**

  Change the typography of an element. Typography edits are quick and easy. 

  Although the rich text editor (Edit Text/HTML) is available for fine tuning, quick actions to change the entire element is available via this option. If you want to apply typography changes to only a part of the text (not to the full text), use the [rich text editor](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md). 

  You can edit the following typography styles:

  * [!UICONTROL Font size]
  * [!UICONTROL Font weight]
  * [!UICONTROL Font style]
  * [!UICONTROL Color] (specify the color code or use the color picker)
  * [!UICONTROL Word spacing]
  * [!UICONTROL Line height]
  * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

  Change the margin for the selected element. You can change the left, right, bottom, and top margins.

  Click the drop-down icon for each margin to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to set the margin or specify the number of pixels for each margin)

  Margin supports positive and negative values.

  Target also supports other size units, such as rem, pc, em. For more information about these units, see [Web Style Sheets CSS Tips and Tricks](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Padding]**

  Change the padding for the selected element. You can change the left, right, bottom, and top padding.

  Drag the slider to set the padding or specify the number of pixels for padding.

  Padding supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Border]**

  Click the border icons at the top of the panel to change the selected element's border.

  You can edit the following styles for each border (top, right, bottom, and left):

  * [!UICONTROL Border style] (none, hidden, dotted, dashed, solid, or double)
  * [!UICONTROL Border color] (specify the color code or use the color picker)
  * [!UICONTROL Border width] (drag the slider to select a border width or specify the width in pixels)

  Border supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Position]**

  Move the selected element from its current position. You can change the element's top, bottom, left, right, and [Z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) position.

  Click the [!UICONTROL Static] drop-down list to choose from the following position options:

  * [!UICONTROL Static]
  * [!UICONTROL Relative]
  * [!UICONTROL Absolute]
  * [!UICONTROL Sticky]
  * [!UICONTROL Fixed]

  Click the drop-down icon for each position to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to position the element or specify the number of pixels you want to move the element)

  Position supports positive and negative values.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Size]**

  Change the selected element's width and height.

  Click the drop-down icon next to [!UICONTROL Width] and [!UICONTROL Height] to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to size the element or specify the number of pixels for each dimension)

* **[!UICONTROL Filter]**

  Drag the slider for each filter option or specify the desired percentage:

  * [!UICONTROL Sepia]
  * [!UICONTROL Contrast]
  * [!UICONTROL Brightness]
  * [!UICONTROL GrayScale]
  * [!UICONTROL Blur]
  * [!UICONTROL Opacity]
  * [!UICONTROL Invert]
  *[!UICONTROL  Hue-rotate]
  * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

  The real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

  The CSS Editor displays any changes that you make in the Styles panel. As shown in the illustration below, the font size, top border, and image size have been changed:

  ![CSS editor with changes](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  Notice the blue dots next to the [!UICONTROL Typography], [!UICONTROL Border], and [!UICONTROL Size] options in the preceding illustration. These dots indicate that you have changed these sections. If you open these section panels, blue dots display next to the specific options that you changed.

  You can type your own code if your desired style is not available by default in the [!UICONTROL Styles].

  The CSS Editor shows details for the current session only. If you save changes and then reopen the editor, details about your previous change do not display in the editor, even if you select the same element again.

  >[!IMPORTANT]
  >
  >You can apply a background image using the CSS Editor, but it might cause flicker. Test your changes before deployment.

### [!UICONTROL CSS Class]

Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space.

Available for [!UICONTROL A/B], [!UICONTROL Automated Personalization], and [!UICONTROL Multivariate Test] activities.

### [!UICONTROL Link]

Change the URL in the link.

Use Edit Link to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the [!UICONTROL Visual Experience Composer] to apply the action on the other image element.

## [!UICONTROL Insert Before]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=ko){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert Before] and choose whether you want to insert an image, HTML, or text. The inserted element appears before the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert Before] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Insert After]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=ko){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert After] and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert After] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Replace Content]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=ko){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Select a different image from the Content Library. The images available for swapping include the images uploaded to the Experience Cloud assets folder or uploaded in the Content Library in Target.

During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL.

For example, the initial URL might look like the following example:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

After activity syncing, the delivery URL might look like the following example:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations supports Replace With in DIV, SECTION, and ARTICLE tags.

**Note:** Swapping images requires an Adobe Scene7 Publishing System Account.

### [!UICONTROL HTML Offer]

Select a different offer from the [!UICONTROL Content Library].

**Note:** HTML Offers are stored on [!DNL Target] servers.

An HTML offer can be up to 256 KB.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

The following options are available:

### [!UICONTROL Rearrange]

Drag the element to another location inside the same parent element or DIV. Other elements shift location to make space for the rearranged element.

**Note**: Click-tracking does not work on rearranged items.

Currently, certain VEC actions, such as [!UICONTROL Rearrange] and [!UICONTROL Move], assume that the sibling elements of the source and destination parent elements are completely loaded. If lazy loading occurs under the parent DOM elements (source or destination), these VEC actions can cause inconsistent behavior. We are working on a more reliable approach to make VEC actions work in lazy-loaded DOM elements. As a temporary workaround, you can use [!UICONTROL Custom Code] in these scenarios to render your experiences.

### [!UICONTROL Resize]

Resize an element on your page. When you select [!UICONTROL Resize], a handle appears in the bottom-right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio.

**Note:** Inline elements cannot be resized.

### [!UICONTROL Move] {#move}

Move elements on your page. Unlike the [!UICONTROL Rearrange] option, [!UICONTROL Move] does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support to ensure moved elements are not hidden behind other elements.)

In certain situations, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent. An element cannot be moved outside of a container that has following CSS property: `overflow: hidden`.

See [!UICONTROL Rearrange] above for more information about inconsistent behavior with the [!UICONTROL Move] and [!UICONTROL Rearrange] actions due to lazy loading of DOM elements.

### [!UICONTROL Hide]

Hide the element. The white space remains, but the content is removed.

### [!UICONTROL Remove]

Remove the element. The white space behind the image is removed and the space where the element was is collapsed.

**Note:** Items within a "classic" mbox (an mbox created within a Target Classic campaign) cannot be removed using this option.

## [!UICONTROL Expand Section]

Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.

## [!UICONTROL Navigate to Link]

Open the destination of the link.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone.

## Considerations {#considerations}

* If an offer contains HTML content, see "How at.js renders offers with HTML content" in [How at.js works](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=ko){target=_blank} for more information.

## Custom element support {#custom}

The VEC supports [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) to let you create and test personalized experiences and offers on custom elements and on elements inside custom elements. This functionality is available in the VEC for all [!DNL Target] activity types.

>[!NOTE]
>
>VEC support for custom elements is supported in [at.js version](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} 2.7.0 (or later){target=_blank}. Ensure that your website has the required version deployed. If you are using the [Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), it must also have the required version of at.js deployed. The VEC options described above are not visible and available for use with non-supported versions of at.js.
>
>VEC support for custom elements is currently not supported with the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=ko){target=_blank}.

Most VEC actions are supported on custom events and inside custom events, with the following exceptions: 

The following actions are not available on custom elements:

* [!UICONTROL Edit]
  * [!UICONTROL Text/HTML]
  * [!UICONTROL Link]
  * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

The following action is not available inside custom elements:

* [!UICONTROL Layout]
  * [!UICONTROL Rearrange]-->
