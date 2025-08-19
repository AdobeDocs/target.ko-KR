---
keywords: 시각적 경험 작성기 선택 사항;경험 작성기 선택 사항;경험 선택 사항;텍스트 편집;html 편집;텍스트/html 편집;배경색 편집;배경색;요소 삽입;링크 편집;링크;시각적 경험 작성기 링크;css 클래스 편집;오퍼 바꾸기;오퍼 바꾸기;이미지 교체;이미지 바꾸기;항목 제거;항목 제거;항목 숨기기;항목 숨기기;재배열;요소 이동;요소 이동;요소 크기 조정;요소 크기 조정;요소;선택 확장;이 링크로 이동;링크 탐색;링크 탐색;탐색;링크;실행 취소;다시 실행;실행 취소/다시 실행;사용자 지정 이벤트;웹 구성 요소;오퍼 결정;오퍼 의사 결정
description: ' [!DNL Adobe Target] [!UICONTROL Visual Experience Composer](VEC)에서 사용할 수 있는 옵션을 살펴보십시오.'
title: '[!UICONTROL Visual Experience Composer]​(VEC) 옵션을 사용하려면 어떻게 해야 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '2667'
ht-degree: 56%

---

# 시각적 경험 작성기 옵션

[!DNL Adobe Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 페이지 요소를 클릭하면 메뉴에 해당 요소 유형에 사용할 수 있는 옵션이 표시됩니다. 또한 페이지 구조를 쉽게 탐색할 수 있는 DOM 경로가 페이지 하단에 표시됩니다.

다양한 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 작업은 작업을 보다 빠르고 효율적으로 수행할 수 있도록 적절한 메뉴 옵션으로 그룹화됩니다.

![VEC 선택 사항 메뉴](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>사용 가능한 옵션은 만들거나 편집하는 활동 유형에 따라 다릅니다.

## [!UICONTROL Edit]

다음 옵션을 사용할 수 있습니다.

### [!UICONTROL Text/HTML] {#edit-text-html}

텍스트 영역, 단추 또는 링크의 텍스트 등의 요소에 대한 HTML 코드를 변경합니다.

HTML 코드 외에도, 사용자 지정 자바스크립트를 편집하고 삽입할 수 있습니다.

[!UICONTROL A/B] 및 [!UICONTROL Experience Targeting] 활동에 대해 텍스트와 HTML을 편집할 때 여러 서식 있는 텍스트 서식 옵션을 사용할 수 있습니다. 글꼴을 선택하고, 글꼴 스타일을 선택하고, 텍스트 정렬을 변경하고, 기타 표준 텍스트 서식 옵션을 사용할 수 있습니다. HTML을 수정할 때 HTML의 코드 보기와 서식 편집 보기 간을 전환할 수 있습니다.

다음 HTML5 태그를 중첩할 수 있습니다.

| 태그 | 허용된 중첩 태그 |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

### [!UICONTROL Background Color]

색상 피커를 사용하여 배경색을 선택하거나 구성하십시오. 색상 견본을 선택하고 RGB 값 또는 색상 16진수 코드를 사용하여 조정할 수 있습니다. 색상 피커의 빨간색 x는 배경을 투명하게 만듭니다.

**참고:** 이 옵션은 배경 이미지가 설정된 요소에는 사용할 수 없습니다.

### [!UICONTROL Styles] {#styles}

[!UICONTROL Styles] 패널을 사용하여 선택한 요소의 기존 스타일 값을 보거나 편집합니다. 스타일을 추가할 수도 있습니다.

[!UICONTROL Styles] 패널에 액세스하려면 VEC 내에서 페이지 요소를 클릭한 다음 **[!UICONTROL Edit]** > **[!UICONTROL Styles]**&#x200B;을(를) 클릭합니다.

[!UICONTROL Styles] 패널이 VEC 오른쪽에 표시됩니다. 이 패널에는 선택한 요소를 편집하거나 선택한 요소에 추가할 수 있는 스타일 목록이 포함되어 있습니다. CSS(Cascading Style Sheet)를 사용하는 데 익숙하거나 개발자로부터 코드를 받은 경우 실시간 CSS 편집기를 사용하면 변경 사항을 보고 스타일을 추가할 수 있습니다.

![스타일 패널](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

다른 스타일을 적용할 때 섹션을 변경한 후 [!UICONTROL Revert] 패널의 오른쪽 상단 모서리에 표시되는 [!UICONTROL Styles] 아이콘을 클릭하여 언제든지 변경 사항을 되돌릴 수 있습니다. [!UICONTROL Revert] 아이콘을 클릭하면 현재 섹션의 패널에서 변경한 모든 내용을 되돌립니다.

아래 설명된 대로 각 섹션을 확장하여 스타일을 편집하거나 추가합니다. 변경 사항을 저장하려면 패널 상단에 있는 [!UICONTROL Back] 아이콘을 클릭하여 패널의 주 표시로 돌아간 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

기본 패널과 여러 섹션 패널의 각 옵션 옆에 있는 파란색 점은 해당 스타일이 변경되었음을 나타냅니다. 이 시각적 표시기를 사용하면 [!UICONTROL Save]을(를) 클릭하기 전에 변경 내용을 쉽게 검토할 수 있습니다.

>[!NOTE]
>
>레이아웃 변경, 배경색, 크기 조정 및 이동에 대한 빠른 작업은 VEC 메뉴에서 별도의 동작으로 사용할 수도 있습니다. 이러한 옵션은 별도의 작업으로 사용하거나 여기에 설명된 대로 스타일 메뉴를 사용할 수 있습니다.

* **[!UICONTROL Background]**

  배경색 및 이미지를 변경합니다.

   * 색상(색상 코드 지정 또는 색상 선택기 사용)
   * 이미지(이미지 선택기에서 이미지 선택)
   * 이미지 소스(외부 URL 지정)
   * 첨부 파일
      * 맨 위 드롭다운 목록을 클릭하여 스크롤, 고정 또는 로컬 선택
      * 맨 아래 드롭다운 목록을 클릭하여 repeat, repeat-x, repeat-y, no-repeat, space 또는 round 선택
   * 클립
      * 맨 위 드롭다운 목록을 클릭하여 테두리 상자, 패딩 상자, 콘텐츠 상자 또는 텍스트 선택
      * 맨 아래 드롭다운 목록을 클릭하여 자동 오디오 또는 오디오 선택

* **[!UICONTROL Typography]**

  요소의 타이포그래피를 변경합니다. 타이포그래피 편집은 빠르고 간단합니다.

  서식 있는 텍스트 편집기(텍스트 편집/HTML)를 미세 조정에 사용할 수 있지만, 이 옵션을 통해 전체 요소를 변경하는 빠른 작업을 사용할 수 있습니다. 타이포그래피 변경 사항을 텍스트의 한 부분(전체 텍스트 아님)에만 적용하려면 [서식 있는 텍스트 편집기](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md)를 사용합니다.

  다음과 같은 타이포그래피 스타일을 편집할 수 있습니다.

   * [!UICONTROL Font size]
   * [!UICONTROL Font weight]
   * [!UICONTROL Font style]
   * [!UICONTROL Color]&#x200B;(색 코드 지정 또는 색 선택기 사용)
   * [!UICONTROL Word spacing]
   * [!UICONTROL Line height]
   * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

  선택한 요소에 대한 여백을 변경합니다. 왼쪽, 오른쪽, 아래쪽 및 위쪽 여백을 변경할 수 있습니다.

  각 여백에 대한 드롭다운 아이콘을 클릭하여 다음 옵션 중에서 선택합니다.

   * [!UICONTROL Auto]
   * [!UICONTROL Value]&#x200B;(슬라이더를 드래그하여 여백을 설정하거나 각 여백에 대한 픽셀 수 지정)

  여백은 양수 및 음수 값을 지원합니다.

  Target은 rem, pc, em과 같은 다른 크기 단위도 지원합니다. 이러한 단위에 대한 자세한 내용은 [웹 스타일 시트 CSS 팁과 트릭](https://www.w3.org/Style/Examples/007/units.en.html)을 참조하십시오.

* **[!UICONTROL Padding]**

  선택한 요소에 대한 패딩을 변경합니다. 왼쪽, 오른쪽, 아래쪽 및 위쪽 패딩을 변경할 수 있습니다.

  슬라이더를 드래그하여 패딩을 설정하거나 각 패딩에 대한 픽셀 수 지정합니다.

  패딩은 폭 조절을 0부터 지원합니다.

  Target은 rem, pc, em과 같은 [다른 크기 단위](https://www.w3.org/Style/Examples/007/units.en.html)도 지원합니다.

* **[!UICONTROL Border]**

  패널 맨 위에 있는 테두리 아이콘을 클릭하여 선택한 요소의 테두리를 변경합니다.

  각 테두리(위쪽, 오른쪽, 아래쪽, 왼쪽)에 대한 다음 스타일을 편집할 수 있습니다.

   * [!UICONTROL Border style]&#x200B;(없음, 숨김, 점선, 파선, 단색 또는 이중)
   * [!UICONTROL Border color]&#x200B;(색 코드 지정 또는 색 선택기 사용)
   * [!UICONTROL Border width]&#x200B;(슬라이더를 드래그하여 테두리 폭을 선택하거나 폭을 픽셀 단위로 지정)

  테두리는 폭 조절을 0부터 지원합니다.

  Target은 rem, pc, em과 같은 [다른 크기 단위](https://www.w3.org/Style/Examples/007/units.en.html)도 지원합니다.

* **[!UICONTROL Position]**

  선택한 요소를 해당 현재 위치에서 이동합니다. 요소의 위쪽, 아래쪽, 왼쪽, 오른쪽 및 [Z-색인](https://www.w3schools.com/cssref/pr_pos_z-index.asp) 위치를 변경할 수 있습니다.

  [!UICONTROL Static] 드롭다운 목록을 클릭하여 다음 위치 옵션 중에서 선택하십시오.

   * [!UICONTROL Static]
   * [!UICONTROL Relative]
   * [!UICONTROL Absolute]
   * [!UICONTROL Sticky]
   * [!UICONTROL Fixed]

  각 위치에 대한 드롭다운 아이콘을 클릭하여 다음 옵션 중에서 선택합니다.

   * [!UICONTROL Auto]
   * [!UICONTROL Value]&#x200B;(슬라이더를 드래그하여 요소를 배치하거나 요소를 이동할 픽셀 수 지정)

  위치는 양수 및 음수 값을 지원합니다.

  Target은 rem, pc, em과 같은 [다른 크기 단위](https://www.w3.org/Style/Examples/007/units.en.html)도 지원합니다.

* **[!UICONTROL Size]**

  선택한 요소의 폭과 높이를 변경합니다.

  [!UICONTROL Width] 및 [!UICONTROL Height] 옆에 있는 드롭다운 아이콘을 클릭하여 다음 옵션 중에서 선택합니다.

   * [!UICONTROL Auto]
   * [!UICONTROL Value]&#x200B;(슬라이더를 드래그하여 요소의 크기를 지정하거나 각 차원의 픽셀 수 지정)

* **[!UICONTROL Filter]**

  각 필터 옵션에 대한 슬라이더를 드래그하거나 원하는 백분율 지정:

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

  CSS(Cascading Style Sheet)를 사용하는 데 익숙하거나 개발자로부터 코드를 받은 경우 실시간 CSS 편집기를 사용하면 변경 사항을 보고 스타일을 추가할 수 있습니다.

  CSS 편집기에 스타일 패널에서 변경한 내용이 표시됩니다. 아래 그림에 표시된 대로 글꼴 크기, 위쪽 테두리 및 이미지 크기가 변경되었습니다.

  ![변경 사항이 표시된 CSS 편집기](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  이전 그림에서 [!UICONTROL Typography], [!UICONTROL Border] 및 [!UICONTROL Size] 옵션 옆에 파란색 점이 있습니다. 이러한 점은 이러한 섹션을 변경했음을 나타냅니다. 이러한 섹션 패널을 열면 변경한 특정 옵션 옆에 파란색 점이 표시됩니다.

  [!UICONTROL Styles]에서 원하는 스타일을 기본적으로 사용할 수 없는 경우 직접 코드를 입력할 수 있습니다.

  CSS 편집기에는 현재 세션에 대한 세부 사항만 표시됩니다. 변경 사항을 저장한 다음 편집기를 다시 열면 동일한 요소를 다시 선택하더라도 이전 변경 사항에 대한 세부 사항이 편집기에 표시되지 않습니다.

  >[!IMPORTANT]
  >
  >CSS 편집기를 사용하여 배경 이미지를 적용할 수 있지만 깜박임이 발생할 수 있습니다. 배포하기 전에 변경 사항을 테스트합니다.

### [!UICONTROL CSS Class]

요소에 사용될 사전 정의된 CSS 클래스를 지정합니다. 둘 이상의 요소가 선택된 경우 여러 CSS 클래스를 공백으로 구분합니다.

[!UICONTROL A/B], [!UICONTROL Automated Personalization] 및 [!UICONTROL Multivariate Test] 활동에 사용 가능합니다.

### [!UICONTROL Link]

링크의 URL을 변경합니다.

링크 편집을 사용하여 동일한 이미지 요소를 가리키도록 선택기를 업데이트합니다. 그러나 다른 이미지 요소에 링크하는 것은 지원되지 않습니다. 다른 이미지 요소에 연결하려면 코드 편집기에서 원래 작업을 삭제하고 [!UICONTROL Visual Experience Composer]을(를) 사용하여 다른 이미지 요소에 작업을 적용하십시오.

## [!UICONTROL Insert Before]

다음 옵션을 사용할 수 있습니다.

### [!UICONTROL Offer Decision]

Offer Decisioning을 사용하여 고객에게 최상의 혜택과 경험을 제공하려면 [ [!DNL Adobe Journey Optimizer]에서 만든 ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank}오퍼를 추가하십시오.

**참고:** 이 옵션은 [수동 [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) 또는 [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md)(XT) 활동을 편집하거나 만들 때만 사용할 수 있습니다. 이 옵션은 다른 활동 유형에는 사용할 수 없습니다.

자세한 내용은 [오퍼 결정 사용](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md)을 참조하세요.

### [!UICONTROL Image], [!UICONTROL HTML] 및 [!UICONTROL Text]

기존 콘텐츠를 수정하는 것 외에도 페이지에 모든 종류의 요소를 추가합니다. 텍스트, 코드, 목록 등을 추가하여 테스트할 완전히 다른 경험을 만들 수 있습니다.

페이지에서 요소를 선택한 다음 [!UICONTROL Insert Before]을(를) 클릭하고 이미지, HTML 또는 텍스트 중 어떤 항목을 삽입할지 선택합니다. 삽입된 요소는 선택한 요소 앞에 나타납니다.

삽입된 요소의 동작은 페이지의 구조, CSS 및 기타 페이지 구성 옵션에 따라 다릅니다. 페이지를 올바르게 표시하려면 유효한 HTML이 필요합니다. 항목을 삽입한 후 항상 페이지를 테스트하여 예상대로 표시되는지 확인합니다.

[!UICONTROL Recommendations]은(는) DIV, SECTION 및 ARTICLE 태그의 콘텐츠에 대한 [!UICONTROL Insert Before]을(를) 지원합니다.

**참고:** 이미지를 삽입하려면 이미지 라이브러리에 액세스할 수 있도록 [!DNL Adobe Scene7 Publishing System]이 활성화되어야 합니다.

### 권장 사항

A/B 테스트(자동 할당 및 자동 타겟 포함)와 경험 타깃팅(XT) 활동 내에 권장 사항을 포함하십시오. 자세한 내용은 [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

### [!UICONTROL Experience Fragment]

최적화 또는 개인화를 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager] (AEM)에서 작성된 경험 구성요소를 삽입합니다. 자세한 내용은 [AEM 경험 구성요소](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)를 참조하십시오.

## [!UICONTROL Insert After]

다음 옵션을 사용할 수 있습니다.

### [!UICONTROL Offer Decision]

Offer Decisioning을 사용하여 고객에게 최상의 혜택과 경험을 제공하려면 [ [!DNL Adobe Journey Optimizer]에서 만든 ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank}오퍼를 추가하십시오.

**참고:** 이 옵션은 [수동 [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) 또는 [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md)(XT) 활동을 편집하거나 만들 때만 사용할 수 있습니다. 이 옵션은 다른 활동 유형에는 사용할 수 없습니다.

자세한 내용은 [오퍼 결정 사용](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md)을 참조하세요.

### [!UICONTROL Image], [!UICONTROL HTML] 및 [!UICONTROL Text]

기존 콘텐츠를 수정하는 것 외에도 페이지에 모든 종류의 요소를 추가합니다. 텍스트, 코드, 목록 등을 추가하여 테스트할 완전히 다른 경험을 만들 수 있습니다.

페이지에서 요소를 선택한 다음 [!UICONTROL Insert After]을(를) 클릭하고 이미지, HTML 또는 텍스트 중 어떤 항목을 삽입할지 선택합니다. 삽입된 요소는 선택한 요소 뒤에 나타납니다.

삽입된 요소의 동작은 페이지의 구조, CSS 및 기타 페이지 구성 옵션에 따라 다릅니다. 페이지를 올바르게 표시하려면 유효한 HTML이 필요합니다. 항목을 삽입한 후 항상 페이지를 테스트하여 예상대로 표시되는지 확인합니다.

[!UICONTROL Recommendations]은(는) DIV, SECTION 및 ARTICLE 태그의 콘텐츠에 대한 [!UICONTROL Insert After]을(를) 지원합니다.

**참고:** 이미지를 삽입하려면 이미지 라이브러리에 액세스할 수 있도록 [!DNL Adobe Scene7 Publishing System]이 활성화되어야 합니다.

### 권장 사항

A/B 테스트(자동 할당 및 자동 타겟 포함)와 경험 타깃팅(XT) 활동 내에 권장 사항을 포함하십시오. 자세한 내용은 [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

### [!UICONTROL Experience Fragment]

최적화 또는 개인화를 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager] (AEM)에서 작성된 경험 구성요소를 삽입합니다. 자세한 내용은 [AEM 경험 구성요소](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)를 참조하십시오.

## [!UICONTROL Replace Content]

다음 옵션을 사용할 수 있습니다.

### [!UICONTROL Offer Decision]

Offer Decisioning을 사용하여 고객에게 최상의 혜택과 경험을 제공하려면 [ [!DNL Adobe Journey Optimizer]에서 만든 ](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank}오퍼를 추가하십시오.

**참고:** 이 옵션은 [수동 [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) 또는 [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md)(XT) 활동을 편집하거나 만들 때만 사용할 수 있습니다. 이 옵션은 다른 활동 유형에는 사용할 수 없습니다.

자세한 내용은 [오퍼 결정 사용](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md)을 참조하세요.

### [!UICONTROL Image]

콘텐츠 라이브러리에서 다른 이미지를 선택합니다. 교체할 수 있는 이미지에는 Experience Cloud 자산 폴더에 업로드된 이미지 또는 Target의 콘텐츠 라이브러리에서 업로드된 이미지가 포함됩니다.

초기 활동 생성 동안 표시되는 URL은 게재에 사용되는 URL이 아닙니다. 활동을 동기화하면 해당 URL이 프로덕션 Scene7 URL로 업데이트됩니다.

예를 들어, 초기 URL은 다음 예제와 유사할 수 있습니다.

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

활동 동기화 후 게재 URL은 다음 예제와 유사할 수 있습니다.

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

추천은 DIV, SECTION 및 ARTICLE 태그의 다음으로 바꾸기를 지원합니다.

**참고:** 이미지를 교체하려면 Adobe Scene7 Publishing System 계정이 필요합니다.

### [!UICONTROL HTML Offer]

[!UICONTROL Content Library]에서 다른 오퍼를 선택하십시오.

**참고:**[!DNL Target] HTML 오퍼는 서버에 저장됩니다.

HTML 오퍼는 최대 256KB까지 가능합니다.

### 권장 사항

A/B 테스트(자동 할당 및 자동 타겟 포함)와 경험 타깃팅(XT) 활동 내에 권장 사항을 포함하십시오. 자세한 내용은 [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

### [!UICONTROL Experience Fragment]

최적화 또는 개인화를 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager] (AEM)에서 작성된 경험 구성요소를 삽입합니다. 자세한 내용은 [AEM 경험 구성요소](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)를 참조하십시오.

## [!UICONTROL Layout]

다음 옵션을 사용할 수 있습니다.

### [!UICONTROL Rearrange]

요소를 동일한 부모 요소 또는 DIV 내의 다른 위치로 드래그합니다. 다른 요소는 재배열된 요소를 위한 공간을 만들기 위해 위치를 옮깁니다.

**참고**: 재배열된 항목에 대해서는 클릭 추적이 작동하지 않습니다.

현재 [!UICONTROL Rearrange] 및 [!UICONTROL Move]과(와) 같은 특정 VEC 작업에서는 원본 및 대상 부모 요소의 형제 요소가 완전히 로드되었다고 가정합니다. 상위 DOM 요소(소스 또는 대상)에서 소극적 로드가 발생하면 이러한 VEC 작업이 일관되지 않은 동작을 초래할 수 있습니다. VEC 작업이 지연 로드된 DOM 요소에서 작동하도록 하는 보다 안정적인 방법을 개발하고 있습니다. 임시 해결 방법으로 이러한 시나리오에서 [!UICONTROL Custom Code]을(를) 사용하여 경험을 렌더링할 수 있습니다.

### [!UICONTROL Resize]

페이지에 있는 요소의 크기를 조정합니다. [!UICONTROL Resize]을(를) 선택하면 요소의 오른쪽 아래 모서리에 핸들이 표시되어 해당 모서리를 드래그하여 크기를 조정할 수 있습니다. 동일한 종횡비를 유지하려면 Shift 키를 길게 누릅니다.

**참고:** 인라인 요소의 크기를 조정할 수 없습니다.

### [!UICONTROL Move] {#move}

페이지에서 요소를 이동합니다. [!UICONTROL Rearrange] 옵션과 달리 [!UICONTROL Move]은(는) 이동할 요소를 위한 공간을 만들기 위해 다른 요소를 이동하지 않습니다. 화살표 키를 사용하여 이동을 미세 조정하십시오. (향상된 예정: 이동된 요소가 다른 요소 뒤에 숨겨지지 않도록 지원합니다.)

CSS 제한 때문에 요소가 상위 요소 내에 남아 있어야 하는 것과 같은 특정 상황에서는 요소를 상위 요소 외부로 이동할 수 없습니다. 요소는 다음 CSS 속성 `overflow: hidden`을 갖는 컨테이너 외부로 이동할 수 없습니다.

DOM 요소의 소극적 로드로 인해 [!UICONTROL Rearrange] 및 [!UICONTROL Move] 작업과 일관되지 않은 동작에 대한 자세한 내용은 위의 [!UICONTROL Rearrange]을(를) 참조하십시오.

### [!UICONTROL Hide]

요소를 숨깁니다. 공백은 남아 있지만 콘텐츠는 제거됩니다.

### [!UICONTROL Remove]

요소를 제거합니다. 이미지 뒤의 공백은 제거되고 요소가 있던 공간은 축소됩니다.

**참고:** &quot;클래식&quot; mbox(Target Classic 캠페인 내에서 만든 mbox) 내의 항목은 이 옵션을 사용하여 제거할 수 없습니다.

## [!UICONTROL Expand Section]

원래 선택된 요소 외에 상위 요소를 선택합니다. 상위 요소를 선택하면 이 요소의 모든 하위 요소가 자동으로 선택됩니다. 선택 요소를 여러 번 확장할 수 있습니다.

## [!UICONTROL Navigate to Link]

링크의 대상을 엽니다.

## [!UICONTROL Undo]/[!UICONTROL Redo]

편집 세션 동안 활동에 대해 변경한 내용을 실행 취소합니다. 이전에 실행 취소한 변경 사항을 다시 실행할 수도 있습니다.

## 고려 사항 {#considerations}

* 오퍼에 HTML 콘텐츠가 포함되어 있는 경우, 자세한 내용은 [at. js 작동 방식](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank}에서 &#39;at.js가 HTML 콘텐츠에서 오퍼를 렌더링하는 방법&#39;을 참조하십시오.

## 사용자 지정 요소 지원 {#custom}

VEC는 사용자 지정 요소 및 사용자 지정 요소 내부의 요소에 대해 개인화된 경험과 오퍼를 만들고 테스트할 수 있도록 [웹 구성 요소](https://developer.mozilla.org/en-US/docs/Web/Web_Components)를 지원합니다. 이 기능은 VEC에서 모든 [!DNL Target] 활동 유형에 사용할 수 있습니다.

>[!NOTE]
>
>사용자 지정 요소에 대한 VEC 지원은 [at.js 버전](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} 2.7.0 이상{target=_blank}에서 지원됩니다. 웹 사이트에 필요한 버전이 배포되어 있는지 확인합니다. [시각적 경험 작성기 Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 사용하는 경우 필요한 at.js 버전도 배포되어 있어야 합니다. 위에 설명된 VEC 옵션은 표시되지 않으며 at.js의 지원되지 않는 버전에서 사용할 수 있습니다.
>
>사용자 지정 요소에 대한 VEC 지원은 현재 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}에서 지원되지 않습니다.

대부분의 VEC 작업은 다음 예외를 제외하고 사용자 지정 이벤트 및 사용자 지정 이벤트 내에서 지원됩니다.

사용자 지정 요소에서는 다음 작업을 사용할 수 없습니다.

* [!UICONTROL Edit]
   * [!UICONTROL Text/HTML]
   * [!UICONTROL Link]
   * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

사용자 지정 요소 내에서는 다음 작업을 사용할 수 없습니다.

* [!UICONTROL Layout]
   * [!UICONTROL Rearrange]

## DOM 경로를 사용하여 요소 탐색 {#dom-path}

페이지에서 요소를 클릭하면 VEC 옵션 메뉴가 표시됩니다. 또한 요소를 클릭하면 해당 DOM 경로가 페이지 하단에 표시됩니다.

![DOM 경로](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path.png)

DOM 경로를 사용하여 선택한 요소(유형, ID 및 클래스)에 대한 정보를 빠르게 확인하고, DOM 경로로 위 또는 아래로 이동하여 원하는 요소를 선택할 수 있습니다.

DOM 경로를 가리키면 파란색 상자가 VEC에서 해당 요소를 강조 표시합니다. 요소를 클릭하면 위에 설명된 대로 주황색 상자가 요소를 강조 표시하고 VEC 옵션 메뉴가 표시됩니다.

DOM 경로를 사용하여 VEC 내에서 상위 요소, 동일 수준의 요소 또는 하위 요소로 손쉽게 이동할 수 있습니다.

DOM 경로 기능은 [클릭 추적](/help/main/c-activities/r-success-metrics/click-tracking.md)을 설정할 때도 사용할 수 있습니다.
