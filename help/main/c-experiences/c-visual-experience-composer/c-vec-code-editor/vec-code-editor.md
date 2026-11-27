---
keywords: css 선택기;사용자 지정 코드;코드 편집기;모바일 웹 경험 편집기
description: Adobe [!DNL Target]의 수정 사항 패널을 사용하여 페이지 수정 사항을 보고 추가 수정 사항(CSS 선택기, Mbox 및 사용자 지정 코드)을 추가하는 방법에 대해 알아봅니다.
title: 내 페이지를 어떻게 수정할 수 있습니까?
feature: Visual Experience Composer (VEC)
exl-id: 23456a4b-9457-4f05-989e-a7c39ce17cc2
TQID: 'https://experienceleague.adobe.com/sOgNlejLNcnSwKf46-AHRXTLkM5Y6laB7QMLu5oYBUU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '2194'
ht-degree: 22%
---
# 수정 사항 시작 {#vec-code-editor}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)의 **[!UICONTROL 수정 사항]** 패널에서 보고, 편집하고, 삭제하고, 수정 사항을 추가하는 방법과 사용자 지정 코드를 사용하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL 수정 사항]** 패널에는 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)에서 페이지에 적용된 모든 변경 사항이 표시되며, 페이지의 각 요소를 클릭하고 [작업을 선택](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)하여 추가 변경을 허용합니다. 각 변경 내용은 **[!UICONTROL 수정]** 목록에 별도의 동작 또는 요소로 표시됩니다. CSS 선택기, Mbox 및 사용자 지정 코드 유형의 수정 사항을 바로 추가할 수도 있습니다.

## 수정 사항 개요 {#modifications-overview}

**[!UICONTROL 수정 사항]** 페이지는 VEC가 콘텐츠 전달 방식을 구성할 때 [!DNL Target]이(가) 선택하는 선택기를 약간 변경합니다. 콘텐츠 또는 HTML 속성을 변경할 수 있습니다. 코드를 편집하여 mbox 내에 HTML 오퍼와 동등한 오퍼를 만들 수도 있습니다.

![수정 사항 패널이 오른쪽에 있고 경험 B의 작업이 나열된 시각적 경험 작성기](../assets/vec_modif_1.png)

**[!UICONTROL 수정 사항]** 페이지를 사용하여 다음을 수행할 수 있습니다.

* 시각적 작성기에서 수행된 작업 보기.

  ![HTML 설정, 배경색 변경, HTML 설정 등 세 가지 작업을 나열하는 수정 패널](assets/codeeditor_viewchange.png)

* 기존 작업 편집. 고급 메뉴에 액세스하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.

  ![첫 번째 작업 옆에 편집 아이콘이 강조 표시된 수정 패널](assets/codeeditor_edit.png)

  변경합니다.

  ![HTML 설정 작업, CSS 요소 선택기 #default_content 및 컨텐츠 필드가 있는 수정 패널](assets/codeeditor_changechange1.png)

* 기존 작업을 삭제합니다. 고급 메뉴에 액세스하고 **[!UICONTROL 수정 삭제]**&#x200B;를 선택합니다.

  ![첫 번째 작업 옆에 삭제 아이콘이 강조 표시된 수정 패널](assets/codeditor_delete.png)

* 새 수정 사항을 추가합니다. **[!UICONTROL 수정 사항]** 메뉴의 고급 메뉴에 액세스하고 **[!UICONTROL 수정 사항 추가]**&#x200B;를 선택한 다음 [수정 사항 추가](#add-modifications)에 설명된 대로 변경 사항을 지정하십시오.

  ![수정 유형, CSS 요소 선택기, 작업 유형 및 컨텐츠 필드가 있는 수정 패널](assets/codeeditor_new.png)

## 수정 사항 추가 {#add-modifications}

VEC에서 선택한 경험에 대한 **[!UICONTROL 수정 사항]** 패널에서 수정 사항이 추가됩니다.

1. **[!UICONTROL 수정 사항]**&#x200B;을 표시하려면 **[!UICONTROL 수정 사항 표시]**&#x200B;를 클릭합니다.

   ![시각적 경험 작성기의 도구 모음에 강조 표시된 수정 아이콘](assets/codeeditor_icon_big.png)

   양식 기반 경험 작성기에서 **[!UICONTROL 수정 사항]** 패널을 열려면 HTML 오퍼를 만들거나 편집하십시오. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

1. 수정 사항을 추가하려면 다음을 수행하십시오.

   * 경험에 대한 이전 수정 사항이 없으면 **[!UICONTROL 수정 사항]** 패널에서 **[!UICONTROL 수정 사항 추가]**&#x200B;를 클릭하십시오.
   * 경험에 대한 이전 수정 사항이 있는 경우 **[!UICONTROL 수정 사항]** 메뉴의 고급 메뉴에 액세스하고 **[!UICONTROL 수정 사항 추가]**&#x200B;를 선택하십시오.

   **[!UICONTROL 수정 사항]** 패널이 표시됩니다.

   ![오른쪽에 수정 사항 패널이 열려 있는 시각적 경험 작성기에 수정 유형, CSS 요소 선택기, 작업 유형 및 콘텐츠 필드가 표시됩니다](assets/codeeditor_page_mods_add.png)

1. **[!UICONTROL 수정 유형]** 드롭다운 목록에서 원하는 유형을 선택합니다.

   | 수정 유형 | 세부 사항 |
   |--- |--- |
   | CSS 선택기 | **[!UICONTROL CSS 요소 선택기]** 상자에서 수정할 CSS 요소를 지정하고, 작업 유형(**[!UICONTROL 콘텐츠 설정]** 또는 **[!UICONTROL 속성 설정]**)을 선택한 다음 필수 정보와 원하는 콘텐츠를 입력합니다. |
   | Mbox | mbox 이름과 원하는 컨텐츠를 지정합니다. |
   | 사용자 지정 코드 | 원하는 대로 **[!UICONTROL `<HEAD>` 섹션에 코드 추가]** 확인란을 선택하거나 선택 취소한 다음 사용자 지정 코드를 추가합니다. 자세한 내용은 [사용자 지정 코드](#custom-code)를 참조하세요. |

   >[!NOTE]
   >
   >Mbox는 at.js 2.*x*&#x200B;을 사용하는 페이지의 VEC에서 더 이상 지원되지 않습니다. 해결 방법으로:
   >
   >* at.js 2.*x*&#x200B;을(를) 사용하는 경우 Mbox 수정 사항 대신 CSS 선택기 수정 사항을 추가한 다음 mbox가 사용 중인 선택기에 콘텐츠를 추가합니다.
   >* 양식 기반 활동 사용(mbox 및 at.js 1.*x* 및 at.js 2.*x*&#x200B;에서 작동).
   >* VEC에서 at.js 1.*x*&#x200B;을(를) 사용합니다.

1. 필요에 따라 수정 사항을 추가하십시오.

## 사용자 지정 코드 {#custom-code}

사용자 지정 코드에서는 VEC, 양식 기반 경험 작성기 및 HTML 오퍼 편집기 내에서 새로운 작업을 보고 편집하고 추가할 수 있는 비시각적 인터페이스를 사용할 수 있습니다. 이 패널에서는 경험의 코드 보기를 제공하여 더 복잡한 경험을 빌드하고, 기존 경험을 미세 조정하고, 문제를 해결하는 데 도움이 됩니다.

사용자 지정 코드는 HTML, JavaScript 및 CSS에 익숙한 고급 사용자를 위한 것입니다. 코드 보기를 통해 변경 내용을 조정하거나 미세 조정하거나 선택기 문제를 해결할 수 있습니다. 새로운 사용자 지정 코드 및 작업을 추가하는 데 사용할 수도 있습니다. 두 개 이상의 사용자 지정 코드를 추가할 수 있으며 각 코드에 선택적으로 이름을 지정할 수 있습니다.

사용자 지정 코드 수정 유형, 이름 Color Blue, Add code in the head section 확인란 및 코드가 있는 ![수정 패널](assets/codeeditor_custom.png)

사용자 지정 코드는 다음과 같이 동작합니다.

* **[!UICONTROL `<HEAD>` 섹션에 코드 추가]**&#x200B;를 선택하면 사용자 지정 코드가 `<head>` 섹션에 추가되며 본문 또는 페이지 로드 이벤트를 기다리지 않고 실행됩니다. `<script>` 및 `<style>` 요소만 추가하십시오. `<div>`개 태그 및 기타 요소를 추가하면 나머지 `<head>`개 요소가 `<body>`에 들어갈 수 있습니다. at.js를 사용하는 경우 모든 오퍼가 비동기적으로 전달됩니다.
* **[!UICONTROL `<HEAD>` 섹션에 코드 추가]**&#x200B;를 선택 취소하면 `<body>` 태그 바로 다음에 사용자 지정 코드가 바로 실행됩니다. DOM 구조를 유지하려면 단일 `<div>`의 모든 코드를 줄바꿈하십시오. at.js를 사용하는 경우 모든 오퍼가 비동기적으로 전달됩니다.
* `<BODY>`의 HTML에 `<SCRIPT>` 및 `<DIV>`이(가) 포함된 경우 `<DIV>`이(가) `<BODY>`에 추가되고 `<SCRIPT>`이(가) `<HEAD>`에서 실행됩니다. 외부 파일을 로드하는 `<SCRIPT>`도 `<HEAD>`에 추가됩니다.
* 스크립트는 비동기적으로 실행됩니다. 즉, `document.write` 및 유사한 스크립트 메서드를 사용할 수 없습니다.
* 사용자 지정 코드는 현재 A/B 및 경험 타깃팅(XT) 활동에만 사용할 수 있습니다. 사용자 지정 코드는 오버레이에 사용할 수 없으며, 리디렉션이 적용되는 경우에도 사용할 수 없습니다.

사용자 지정 코드는 다음과 같이 사용하는 경우 지원합니다.

* 페이지 맨 위에서 실행할 사용자 지정 JavaScript, HTML 또는 CSS 추가
* 수정 후 VEC에서 생성된 코드 보기 또는 편집
* 선택기에 대한 HTML 컨텐츠 설정(CSS 선택기만 해당)
* HTML 요소에 속성 설정
* 지역 mbox에서 전달할 오퍼 컨텐츠 추가
* DOM Ready 시 교체, jQuery 사용
* DOM Ready 시 교체, jQuery 없음(Internet Explorer 8을 지원하지 않음)
* &quot;elementOnLoad&quot; 플러그인을 통해 DOM 폴링으로 교체
* 사용자 지정 리디렉션

사용자 지정 코드는 다음을 제공합니다.

* 유용성 개선을 위한 라인 번호.
* HTML 오퍼에 대한 잘못된 구문을 방지하는 데 도움이 되는 구문 강조 표시입니다.
* 여러 사용자 지정 코드를 작성하고 각각에 대한 선택적 이름을 제공하는 기능입니다. 여러 사용자 지정 코드를 만들면 이후에 디버깅이 쉬워집니다. 예를 들어, 여러 수정 사항을 수행하기 위해 단일 사용자 지정 코드를 만드는 대신 설명하는 이름을 사용하여 각 수정 사항에 대해 별도의 사용자 지정 코드를 만들 수 있습니다. 별도의 사용자 지정 코드를 통해 보다 모듈화되고 관리 가능한 수정 사항이 제공됩니다. 활동에서 여러 사용자 지정 코드를 실행하는 것은 만들어진 시퀀스에서 보장되지 않습니다.

**[!UICONTROL 수정 사항]** 패널은 화면을 시각적 모드와 코드 모드 간에 분할합니다. 두 모드는 동기화된 채 유지됩니다. 시각적으로 수행된 모든 수정 사항에는 해당하는 행이 코드 보기에 있습니다. 마찬가지로 코드 보기에서 수행된 모든 변경 사항은 시각적 경험에 표시됩니다. 코드 보기에서 행을 클릭하면 시각적 페이지에서 해당 요소가 선택됩니다.

사용자 지정 코드는 HTML, 스크립트 및 스타일을 지원합니다. 모든 유효한 HTML 코드나 스크립트는 추가하거나 편집할 수 있습니다.

## 사용자 지정 코드 예 {#custom-code-examples}

**[!UICONTROL 사용자 지정 코드]** 패널에는 페이지 로드 시작 시 실행되는 코드가 있습니다. JavaScript 코드는 `<head>` 태그에서 실행할 수 있습니다. 코드 실행은 `<body>` 태그가 DOM에 존재할 때까지 기다리지 않습니다. 이어지는 시각적 작업을 위한 선택기는 이 탭에 추가된 HTML 요소에 따라 다릅니다.

**[!UICONTROL 사용자 지정 코드]** 패널은 일반적으로 페이지 맨 위에 JavaScript 또는 CSS를 추가하는 데 사용됩니다.

다음 작업을 수행하려면 **[!UICONTROL 사용자 지정 코드]** 탭을 사용하십시오.

* 외부 JavaScript 파일에 JavaScript 인라인 또는 링크 사용

  예를 들어 요소의 색상을 변경하려면 다음을 수행합니다.

  ```javascript
  <script type="text/javascript"> 
  document.getElementById("element_id").style.color = "blue"; 
  </script> 
  ```

* 외부 스타일 시트에 스타일 인라인 또는 링크 구성

  예를 들어, 오버레이 요소를 위한 클래스를 정의하려는 경우 다음과 같습니다.

  ```html
  <style> 
  .overlay 
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; } 
  </style> 
  ```

* HTML 코드 조각을 추가하여 새 요소 정의

  예를 들어, 위에 정의된 CSS 클래스를 사용하는 오버레이 `<div>`을(를) 만들려면 다음 HTML 코드 조각을 사용하십시오.

  ```html
  <div class="overlay"></div>
  ```

* DOM Ready 시 교체, jQuery 사용

  다음 예제에서는 [!DNL Target]이(가) 오퍼를 실행할 때 고객의 웹 사이트가 페이지에서 사용할 수 있는 jQuery를 가지고 있다고 가정합니다.

  ```javascript
  <style>#default_content {visibility:hidden;}</style> 
  <script> 
  jQuery( document ).ready(function() { 
      jQuery("#default_content").html( "<span style='color:red'>Hello <strong>Again</strong></span>" ); 
      jQuery("#default_content").css("visibility","visible"); 
  }); 
  </script> 
  ```

* DOM Ready 시 교체, jQuery 없음(Internet Explorer 8을 지원하지 않음)

  ```javascript
  <style>#default_content {visibility:hidden;}</style> 
  <script> 
  document.addEventListener("DOMContentLoaded", function(event) {  
      document.getElementById("default_content").innerHTML = "<span style='color:red'>Hello <strong>Again</strong></span>"; 
      document.getElementById("default_content").style.visibility="visible"; 
  }); 
  </script> 
  ```

* 기존 매개 변수, `s_tnt` 매개 변수(Analytics와의 기존 통합용), 레퍼러 매개 변수 및 mbox 세션을 전달하는 사용자 지정 리디렉션

  ```javascript
  <style type="text/css">body{display:none!important;}</style> 
  <script type="text/javascript"> 
   var qs='';window.location.search?qs=window.location.search+'&':qs='?'; 
   window.location.replace('//www.mywebsite.com/'+qs+'s_tnt=${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}&s_tntref='+encodeURIComponent(document.referrer)+'&mboxSession='+mboxFactoryDefault.getSessionId().getId()+''+window.location.hash+''); 
  </script> 
  ```

* 사용자 지정 코드에서 사용할 [!DNL Adobe Target] 경험 템플릿 추가

  경험 템플릿은 구성 가능한 입력이 있는 사전 코딩된 샘플로서, 일반적인 마케터 사용 사례를 실행하는 데 사용됩니다. VEC 또는 양식 기반 경험 작성기를 통해 일반적인 사용 사례를 실행할 수 있는 시작점으로 개발자와 마케터에게 무료로 제공됩니다. 사용 사례에는 라이트박스, 회전 메뉴, 카운트다운 등이 있습니다. 자세한 내용은 [경험 템플릿](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md)을 참조하십시오.

## 사용자 지정 코드 우수 사례 {#custom-code-best-practices}

* **항상 하나의 요소에 사용자 지정 코드를 래핑합니다.**

  예:

```html
<div id="custom-code"> 
// My Code goes here 
</div>
```

수정이 필요한 경우 이 컨테이너 내에서 변경합니다. 사용자 지정 코드가 더 이상 필요하지 않은 경우 이 컨테이너를 비워 두되 제거하지 마십시오. 이렇게 하면 다른 경험 수정 사항에는 영향을 주지 않습니다.

* **코드 편집기에서 만든 페이지에 대한 수정 사항에 요소 ID &quot;CDQID&quot;를 사용하지 마십시오.**

  [!DNL Target]은(는) 값이 &quot;CDQID&quot;인 새 요소 ID를 [!DNL Target]에 의해 수정된 페이지의 모든 요소에 적용합니다. 이 ID는 [!DNL Target]에서 적용되므로 코드 편집기에서 더 이상 수정하거나 조정하는 데 사용해서는 안 됩니다.

* **사용자 지정 코드 스크립트에서 `document.write` 작업을 수행하지 마십시오.**

  스크립트는 비동기적으로 실행됩니다. 이로 인해 종종 `document.write` 작업이 페이지의 잘못된 위치에 나타납니다. 사용자 지정 코드에서 생성된 스크립트에는 `document.write`를 사용하지 않는 것이 좋습니다.

* **요소를 만든 다음 수정하면 원래 요소를 삭제하지 마십시오.**

  각 변경 사항은 **[!UICONTROL 수정 사항]** 패널에 새 요소를 만듭니다. 두 번째 작업은 요소 1을 수정하므로, 요소 1이 삭제되면 해당 작업에는 더 이상 수정할 사항이 없으며 변경 사항이 더 이상 작동하지 않습니다. 자세한 내용은 [사용자 지정 코드 문제 해결](#troubleshooting-custom-code)을 참조하십시오.

* **동일한 URL을 대상으로 하는 두 활동에 사용자 지정 코드 기능을 사용할 때는 주의하십시오.**

  사용자 지정 코드 기능이 동일한 URL을 대상으로 하는 두 활동에 사용되는 경우, JavaScript이 두 활동의 페이지에 삽입됩니다. [!DNL Target]은(는) 전달된 콘텐츠의 순서를 자동으로 결정합니다. 코드가 배치에 따라 달라지지 않는지 확인하십시오. 코드 작성자는 코드에 충돌이 없는지 확인할 책임이 있습니다.

## 사용자 지정 코드 문제 해결 {#troubleshooting-custom-code}

+++ `triggerView`을(를) 사용할 때 사용자 지정 코드가 실행되지 않는 이유는 무엇입니까?

VEC의 사용자 정의 코드 오퍼는 `triggerView()` 가 `{page: false}` 를 통해 옵션으로 호출되는 경우 다시 렌더링되지 않습니다.

+++

+++ 페이지의 구조적 변경 사항으로 인해 작업을 적용할 수 없다는 경고는 무엇을 의미합니까?

이 메시지는 활동이 마지막으로 저장된 이후 페이지 구조가 변경되었음을 나타냅니다.

![활동을 마지막으로 저장한 후 페이지 구조가 변경되었다는 경고 메시지](assets/code_editor_2.png)

찾아보기 모드를 사용하여 누락된 선택기에 도달할 수 있습니다. Adobe에서는 경고 메시지에 표시된 대로 컨텐츠가 예상대로 표시되도록 각 경험을 삭제한 다음 다시 만드는 것이 좋습니다.

+++

+++ &quot;이 작업을 삭제하면 후속 작업에 영향을 줄 수 있습니다&quot;라는 경고는 무엇을 의미합니까?

예를 들어 다음 두 가지 작업이 수행되었을 수 있습니다.

* 요소 1에 클래스 추가
* 요소 1에 대한 HTML 편집

각 변경 사항은 **[!UICONTROL 수정 사항]** 패널에 새 요소를 만듭니다. 두 번째 작업은 요소 1을 수정하므로, 요소 1이 삭제되면 두 번째 작업에는 더 이상 수정할 사항이 없으며 변경 사항이 더 이상 작동하지 않습니다.

즉, 요소가 텍스트와 함께 추가되고 요소가 별도의 작업에서 다른 텍스트로 편집되는 경우 **[!UICONTROL 수정]** 패널에 두 작업이 모두 별도의 요소로 표시됩니다. 요소를 편집하면 원래 요소를 수정하고 편집된 텍스트를 포함하는 새 요소가 만들어집니다. 원래 요소가 삭제되면 편집된 텍스트는 편집된 요소를 찾을 수 없으며 표시되지 않습니다. 두 번째 요소는 요소 목록에 남아 있지만, 변경되는 요소가 더 이상 존재하지 않으므로 페이지에 영향을 주지 않습니다.

+++

+++ 스크립트에서 `document.write`(으)로 만든 요소가 필요한 위치에 표시되지 않는 이유는 무엇입니까?

스크립트는 비동기적으로 실행됩니다. 이로 인해 종종 `document.write` 작업이 페이지의 잘못된 위치에 나타납니다. 따라서 사용자 지정 코드에서 작성된 스크립트에서는 `document.write`를 사용하지 않는 것이 좋습니다.

+++

+++ JavaScript에서 사용자 지정 코드에 오류를 표시하는 이유는 무엇입니까?

유효한 JavaScript이 아닌 모든 인라인 JavaScript에 사용자 지정 코드에 오류가 표시됩니다.

+++

+++ 사용자 지정 코드의 변경 내용이 실행 취소되지 않는 이유는 무엇입니까?

현재 **[!UICONTROL 수정 사항]** 패널 및 사용자 지정 코드에서 편집 및 삭제 작업에 대한 실행 취소는 지원되지 않습니다. 이 작업 중 하나를 실행 취소하면 VEC에 있는 경험이 사용자 지정 코드에 표시되는 실제 작업과 다르게 나타날 수 있습니다. 하지만 사용자 지정 코드의 작업은 올바른 상태이며 전달에는 영향을 주지 않습니다. 이것은 UI 문제입니다. 경험을 새로 고치려면 경험을 저장하고 다시 열거나, 다음 단계로 이동했다가 돌아오십시오. 이러한 작업 중 하나는 경험을 다시 로드하므로 예상대로 표시되고 **[!UICONTROL 수정]** 패널의 작업과 일치합니다.

+++

+++ 사용자 지정 코드가 Internet Explorer 8에서 예상한 결과를 생성하지 않는 이유는 무엇입니까?

[!DNL Target]은(는) 더 이상 Internet Explorer 8을 지원하지 않습니다.

+++
