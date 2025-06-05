---
keywords: 시각적 경험 작성기;시각적 경험 작성기 우수 사례;시각적 경험 작성기 제한 사항;시각적 경험 작성기 주의 사항;vec 우수 사례;vec
description: '[!UICONTROL Visual Experience Composer]​(VEC)을 사용할 때 경험이 예상대로 작동하도록 하는 모범 사례를 알아봅니다.'
title: '[!UICONTROL Visual Experience Composer] 모범 사례 및 제한 사항은 무엇입니까?'
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
source-git-commit: 1f2c6bbabf0158672e5f926ffdf9662637cd8416
workflow-type: tm+mt
source-wordcount: '2435'
ht-degree: 37%

---

# [!UICONTROL Visual Experience Composer] 모범 사례 및 제한 사항

경험이 의도한 대로 작동하도록 하려면 [!DNL Adobe Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC)을 사용할 때 모범 사례를 따르십시오. 성능을 극대화하고 일반적인 문제를 방지하기 위한 주요 팁과 제한 사항을 알아 두십시오.

## 우수 사례 {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

다음은 VEC를 사용할 때의 모범 사례입니다.

### at.js 참조를 페이지의 `<head>` 섹션 맨 위에 놓습니다.

+++세부 정보 보기
[!UICONTROL Visitor API Service]도 사용하는 경우 at.js 위에 방문자 API 스크립트를 배치하십시오.

+++

### 계정 수준(계정에서 만든 모든 활동에 대해 활성화됨) 또는 개별 활동 수준에서 [!UICONTROL Enhanced Experience Composer]을(를) 활성화할 수 있습니다.

+++세부 정보 보기
계정 수준에서 [!UICONTROL Enhanced Experience Composer]을(를) 사용하려면 [!UICONTROL [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]]을(를) 클릭한 다음 [!UICONTROL Enable Enhanced Experience Composer] 스위치를 [켜짐] 위치로 전환하십시오.

[!UICONTROL Visual Experience Composer]에서 활동을 만드는 동안 활동 수준에서 [!UICONTROL Enhanced Experience Composer]을(를) 사용하려면 [!UICONTROL Configure > [!UICONTROL Page Delivery]]을(를) 클릭한 다음 [!UICONTROL Enable Enhanced Experience Composer] 스위치를 [켜짐] 위치로 전환하십시오.

+++

### 사이트의 보안 페이지에서 [!UICONTROL Enhanced Experience Composer]을(를) 로드할 수 없는 경우 허용 목록에 추가하다할 수 있습니다.

+++세부 정보 보기
다음 IP 주소를 허용 목록에 추가 하여 [!UICONTROL Enhanced Experience Composer]을(를) 로드하는 문제를 해결할 수 있습니다. 이러한 IP 주소는 [!UICONTROL Enhanced Experience Composer] 프록시에 사용되는 [!DNL Adobe] 서버용입니다. 활동 편집에만 필요합니다. 사이트 방문자는 이러한 IP 주소를 허용 목록에추가된으로 사용할 필요가 없습니다.

자세한 내용은 *고급 경험 작성기 관련 문제 해결*&#x200B;에서 [EEC가 공용 IP에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md)를 참조하십시오.

+++

### 최상위 레벨 요소 및 올바른 테스트/타깃팅 후보일 수 있는 기타 요소에 고유 ID를 사용하십시오.

+++세부 정보
본문 요소 내부에 있는 모든 즉시 고유한 ID가 있어야 합니다. 새 요소가 본문에 삽입되고 코드가 배치되면 적어도 상위 요소는 더 쉽게 인식할 수 있는 방법이 있습니다.

[!DNL Target]에는 ID가 필요하지 않지만 ID를 사용하면 경험 작성기로 만든 경험의 안정성이 향상됩니다. [!DNL Target]은(는) 경험이 전달될 때 CSS 선택기를 사용하여 콘텐츠를 수정합니다. 경험을 편집할 때 [!UICONTROL Visual Experience Composer]은(는) 수정되는 HTML 요소에 null이 아닌 ID 특성을 가진 가장 가까운 상위 항목에 선택기를 고정합니다. 따라서 HTML ID 속성을 설정하거나 수정하는 JavaScript 라이브러리를 포함한 어떤 메커니즘도 사용하지 않는 것이 좋습니다. [!DNL Target] 경험 작성기에서 해당 ID를 활동 생성에 사용할 수 있지만, JavaScript에서 ID를 수정하는 경우 경험이 생성될 때 사용된 ID는 경험이 실행될 때 사용할 수 없을 수 있습니다. ID를 사용할 수 없는 경우에는 ID에 앵커로 설정된 선택기가 실패합니다.

+++

### 쉽게 식별할 수 있도록 CSS 클래스의 이름을 지정합니다.

+++세부 정보
[!DNL Visual Experience Composer]에서 CSS 클래스를 편집할 때 설명하는 클래스 이름을 사용하여 클래스를 쉽게 식별할 수 있도록 하는 것이 유용합니다. 이렇게 하는 것은 올바른 CSS 클래스를 편집하고 페이지가 예상대로 표시되도록 하는 데 도움이 됩니다.

요소를 숨기거나 제거할 때 `!important` CSS 속성을 사용하지 마십시오.

`!important` CSS 속성이 있으면 전달 중 `target.js`에 의해 변경된 사항이 사이트의 CSS 규칙으로 인해 무시됩니다.

+++

### 페이지 레이아웃에 HTML 표를 사용하지 마십시오.

+++세부 정보
[!DNL Target]은(는) JavaScript을 사용하여 페이지 서식을 지정합니다. JavaScript로는 표 기반 레이아웃을 수정하기 어렵습니다. 또한 표 기반 레이아웃은 모든 브라우저에서 동일하게 표시되지 않을 수도 있습니다. 최상의 결과를 얻으려면 CSS를 사용하여 페이지 레이아웃을 작성하십시오.

+++

### iFrame의 사용을 최소화하십시오.

+++세부 정보
iFrame의 사용을 최소화하여 페이지 및 테스트 관리를 간소화하는 것이 좋습니다. 시각적 경험 작성기가 iFrame 내에 일부 작업을 적용할 수 있지만 크기 조정과 같은 일부 작업이 제대로 작동하지 않습니다. 여러 iFrame을 사용하는 페이지를 관리하고 페이지 크기를 조정하는 것은 어렵습니다. 따라서 iFrame을 많이 사용하는 페이지를 테스트하면 문제가 발생할 수 있습니다.

+++

### DOM이 준비된 후 가능한 한 빨리 모든 동적 DOM 수정 사항을 적용할 수 있도록 하십시오.

+++세부 정보
`target.js`까지 수정 사항이 경험 응용 프로그램 앞에 적용되지 않으면 콘텐츠 전달이 중단될 수 있습니다. 이런 일은 타깃팅된 요소의 계층 구조에 DOM 변경 사항이 있는 경우에만 발생합니다.

+++

### 앵커 요소에서는 일반 텍스트나 이미지 태그만 사용하십시오.

+++세부 정보
`<a>Anchor Text</a>`

또는

`<a href=""> <img src=""> </img> </a>`

+++

### 인라인 요소 내부에는 블록 수준 요소를 사용하지 마십시오.

+++세부 정보
블록 수준 요소는 앵커, 범위 등과 같은 인라인 요소 내에서 사용할 수 없습니다. 이렇게 하면 인라인 요소의 높이와 너비가 손실되므로 [!UICONTROL Visual Experience Composer]의 오버레이 도구가 예상대로 작동하지 않을 수 있습니다.

+++

### 웹 사이트에서 base 태그를 사용하여 URL 및 링크를 확인하지 마십시오.

+++세부 정보
VEC는 링크를 업데이트하는 프록시 서버를 사용하여 백그라운드에서 웹 사이트를 조작합니다. base 태그를 추가하는 경우, 프록시 서버에서 사용하는 URL은 브라우저에서 다시 확인되어 깨진 것처럼 표시됩니다.

+++

### EDIT HTML을 사용하여 DOM 구조를 조작하면 선택기가 손상될 수 있습니다.

+++세부 정보
예를 들어 다음 두 가지 작업을 수행한 경우:

* 요소 1에 클래스 추가
* 요소 1에 대한 HTML 편집

각 변경 사항은 VEC에 새 요소를 만듭니다. 두 번째 작업은 요소 1을 수정하므로, 요소 1을 삭제하면 두 번째 작업에서는 더 이상 수정할 사항이 없게 되며, 따라서 변경이 더 이상 작동하지 않습니다.

다시 말해, 텍스트가 있는 요소를 추가하면, 다른 텍스트로 해당 요소를 편집하는 별도의 작업에서 코드 편집기에 두 작업이 모두 별도의 요소로 표시됩니다. 요소를 편집한 경우 편집된 텍스트를 포함하고 여러분이 만든 원본을 수정하는 새 요소가 만들어진 것입니다. 만약 원래 요소를 삭제하면 편집된 텍스트는 편집된 요소를 찾을 수 없으며 표시되지 않습니다. 두 번째 요소는 요소 목록에는 남아 있지만, 변경되는 요소가 더 이상 존재하지 않으므로 이 요소는 페이지에 영향을 주지 않습니다.

[!UICONTROL Visual Experience Composer][&#128279;](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337)에 사용된 요소 선택기를 참조하십시오.

+++

### 서식 있는 텍스트 편집기로 텍스트 요소에 스타일을 지정할 때 `<b>` 및 `<i>` 태그를 사용하십시오.

+++세부 사항
* 굵은 텍스트를 표시하려면 `<strong>`보다는 `<b>`를 사용하십시오.
* 기울임체 텍스트를 표시하려면 `<em>`보다는 `<i>`를 사용하십시오.

`<strong>`과 `<em>` 태그는 예상치 못한 결과를 초래할 수 있습니다.

+++

### 양식 필드를 제거할 때 주의하십시오.

+++세부 정보
특정 양식 필드는 제출에 필수일 수 있습니다. 따라서 해당 양식 필드를 제거하면 제출에 영향을 줄 수 있습니다.

+++

### 스크립트 내에 `mboxCreate`을(를) 포함하지 마십시오.

+++세부 정보
`mboxCreate`이(가) `document.write`을(를) 사용하므로 스크립트에 `mboxCreate`을(를) 포함하지 않는 것이 좋습니다. 대신, `mboxDefine` 및 `mboxUpdate`를 동일한 목적에 사용하십시오.

+++

### 초기화에 HTML 코드가 필요한 경우 [!DNL Target]을(를) 사용하여 JavaScript 코드 조각을 업데이트하지 마십시오.


+++세부 정보
작업(HTML 편집)이 페이지 구성 요소(예: 슬라이더, 회전 메뉴 등)에서 수행되면 게재가 손상될 수 있습니다. VEC는 JavaScript에 의해 페이지 구성 요소가 인스턴스화된 후 작업을 수행합니다.

그러나 페이지의 컨텐츠가 방문자에게 전달되면 조각 인스턴스화 전에 작업이 적용됩니다. 이 때문에 이 조각의 기능은 전달 시 깨질 수도 있고 깨지지 않을 수도 있습니다. 기능은 조각을 정의하기 위해 페이지에서 사용되는 스크립트의 특성에 따라 다릅니다.

전달 테스트를 수행하고 있고 이 전달이 처음 작동되는 경우라면 계속 작동하리라는 보장이 없습니다. 경합 조건이 있을 수도 있고 또는 없을 수도 있습니다.

* 경합 조건이 있는 경우 게재가 간헐적으로 작동합니다.
* 경합 조건이 없으면 항상 배달이 작동합니다.

페이지를 여러 번 테스트하여 전달이 예상대로 작동하는지 확인하십시오.

+++

### 웹 사이트에서 base 태그를 사용하여 URL 및 링크를 확인하지 마십시오.

+++세부 정보
[!UICONTROL Enhanced Experience Composer]을(를) 사용하면 모든 링크 URL을 업데이트하여 프록시에서 작동하도록 하는 프록시 서버에서 웹 사이트를 백그라운드에서 조작합니다. 기본 태그를 추가하면 이러한 URL이 모두 브라우저에 의해 확인되므로 손상된 것으로 표시됩니다.

+++

### 타깃팅에 사용할 수 있는 사이트의 중요한 텍스트는 요소 내에서 HTML 코드 안에 넣어야 합니다.

+++세부 정보
예를 들어 코드가 다음과 같은 경우 VEC에서 장바구니 텍스트를 타깃팅할 수 없습니다.

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart"> 
   <img alt="Shopping Cart"src="/images/ico-cart.gif"></img> 
   Shopping Cart: 
   <span id="HeaderCartQtyTotal">
      0 
  </span> 
  Items 
  <span id="HeaderCartPriceTotal"></span> 
</a>
```

이 예에서는 VEC에서 전체 앵커 요소가 선택되어 타깃팅이 수행될 경우 다른 요소에 부정적인 영향을 줍니다.

+++

### JavaScript 코드에서 `top` 또는 `self` 변수를 사용하지 마십시오.

+++세부 정보
[!UICONTROL Enhanced Experience Composer]이(가) 활성화되면 iframe 버스팅을 비활성화하도록 top 및 self 변수의 값이 업데이트됩니다. 사용자 지정 JavaScript 코드 대신 iframe 버스팅을 추가하려면 X-frame-options 헤더를 사용하십시오.

+++

### 페이지를 로드할 때 매개 변수가 추가되면 항상 웹 사이트를 테스트하십시오.

+++세부 정보
예를 들어 `www.abc.com`을(를) 열려면 다음 URL 매개 변수가 사용됩니다.

`www.abc.com?mboxEdit=1&mboxDisable=1`

이 매개 변수는 사용하면 iframe에서의 편집을 가능하게 해줍니다.

이러한 매개 변수를 추가한 후에는 웹 사이트가 예상대로 로드되는지 확인하십시오.

+++

### 페이지가 iframe에서 예상대로 열리는지 확인하십시오.

+++세부 정보
웹 사이트에서 iframe 버스팅 기술을 끄고 웹 사이트가 더미 페이지의 iframe 내에서 예상대로 열리는지 확인하십시오. 예:

```html
<!DOCTYPE 
<html> 
<html> 
<head> 
  <meta charset="utf-8"> 
  <meta name="viewport" content="width=device-width"> 
  <title>JS Bin</title> 
</head> 
<body> 
  <iframe src="https://www.homedepot.com"</iframe> 
</body> 
</html>
```

+++

## 주의 사항 {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

[!UICONTROL Visual Experience Composer]을(를) 사용하여 활동을 디자인할 때 다음 주의 사항을 고려하십시오.

### [!UICONTROL Move] 기능은 z-색인을 지원하지 않습니다.

+++세부 정보
z-색인 기능이 없으므로 이동된 요소는 다른 요소의 맨 위에서 이동할 수 없습니다. 자세한 내용은 [제한 사항](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721)을 참조하십시오.

+++

### 요소를 다시 정렬하는 것은 클릭 추적에 영향을 줍니다.

+++세부 정보
클릭 추적으로 표시된 요소가 재배열되면 재배열된 요소의 경로가 변경됩니다. 결과적으로, 원래 요소가 다시 배열되기 전에 있었던 위치에 있는 요소는 클릭이 추적되는 요소입니다.

이 문제는 활동 컨텐츠를 전달하기 위한 코드와 클릭을 추적하기 위한 코드가 모두 페이지에 전달되는 동일한 코드 조각에 포함되어 있기 때문에 발생합니다. 다른 페이지로 이동하고 클릭 추적을 설정한다면, 활동 컨텐츠 코드와 클릭 추적 코드가 해당 페이지에 전달됩니다. 클릭 추적 페이지의 페이지 구조가 테스트가 실행되는 페이지와 유사하다면, 테스트 컨텐츠가 클릭 추적 페이지에 표시될 수도 있습니다.

+++

### mbox인 `<div>`에서는 요소 삽입이 작동하지 않을 수 있습니다.

+++세부 정보
mbox에 오퍼가 포함된 경우 mbox가 잘못 구현되면 요소 삽입이 `insertAfter`이(가) 아닌 `insertBefore`(으)로 표시될 수 있습니다.

+++

### 상위 요소와 하위 요소를 모두 편집할 때 상위를 먼저 편집하십시오.

+++세부 정보
요소에서 이미지 작업을 교체한 다음, 상위 요소에서 텍스트 또는 HTML을 편집하면 게재 문제가 발생할 수 있습니다. 가장 좋은 워크플로우는 하위 요소의 이미지를 교체하기 전에 상위 요소를 편집하는 것입니다.

+++

### mbox가 하위 요소로 포함된 페이지 요소는 선택할 수 없습니다.

+++세부 정보
예를 들어 페이지에 다음이 포함되어 있는 경우:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

페이지에서 하드코딩된 mbox가 여전히 [!DNL Target]을(를) 호출하고 응답을 수신하므로 경험에서 외부 div를 선택하면 안 됩니다. 이 응답은 더 큰 페이지 요소용으로 수행되는 응답을 방해합니다.

+++

### 프록시 IP는 고객 환경에서 차단될 수 있습니다.

+++세부 정보
스테이징 환경과 같이 라이브가 아닌 사이트에서 [!UICONTROL Enhanced Experienced Composer]을(를) 사용하는 경우 사이트가 RIP를 차단하면 시간 초과와 액세스 거부 오류가 표시될 수 있습니다.

+++

## 제한 {#section_F33C2EA27F2E417AA036BC199DD6C721}

VEC를 사용할 때는 다음 제한 사항을 고려하십시오.

### [!DNL Chrome] 확장 정책 변경 사항과 VEC 호환성을 처리하는 중입니다. {#ext}

+++세부 정보
Google Chrome[&#128279;](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}의 업데이트된 V3 매니페스트 정책으로 인해 확장에서 브라우저에서 구문 분석하기 전에 원본 DOM을 더 이상 수정할 수 없습니다. 따라서 iframe 버스팅 구현과 같은 특정 보안 스크립트는 VEC에서 페이지가 로드되지 않도록 차단할 수 있습니다.

호환성을 보장하려면 페이지가 [!DNL Target] iframe 내부에 로드될 때 이러한 스크립트를 조건부로 비활성화해야 합니다. VEC 로드 중에 [!DNL Target]에서 삽입한 `window.adobeVecExtension` 개체가 있는지 확인하여 이 프로세스를 안전하게 수행할 수 있습니다.

다음 코드 조각은 웹 페이지가 VEC에 로드되지 않을 수 있는 iframe 버스팅 코드의 예입니다.

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

웹 페이지가 [!DNL Target] 내부에 임베드되었는지 확인하는 간단한 검사를 사용할 수 있습니다. 코드 조각은 다음과 같아야 합니다.

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

### 요소를 컨테이너 외부로 이동한 다음 CSS 속성을 이동할 수 없습니다.

+++세부 정보
요소는 뒤에 CSS 속성이 오는 컨테이너 외부로 이동할 수 없습니다.

+++

### 다시 정렬할 [!UICONTROL Button] 요소를 선택할 수 없습니다.

+++세부 정보
[!UICONTROL Button]개의 요소를 다시 정렬하기 위해 직접 선택할 수 없습니다. 재배치를 사용하려면 더 큰 컨테이너에 버튼을 배치하십시오.

+++

### 교체 오퍼만 mbox에서 사용할 수 있습니다.

+++세부 정보
mbox 내에서는 [!UICONTROL Edit Class] 및 [!UICONTROL Rearrange]과(와) 같은 작업을 사용할 수 없습니다.

+++

### 동일한 요소를 다시 배열하고 이동해서는 안 됩니다.

+++세부 정보
요소를 다른 위치로 이동한 후 상위 컨테이너를 선택하고 하위 요소를 다시 정렬하려고 하면 이동된 요소는 영향을 받지 않고 그대로 유지됩니다. 재배열이 원하는 대로 표시되지 않을 수 있습니다.

+++

### [!UICONTROL Change Image] 작업은 회전 메뉴에 있는 이미지에 작동하지 않습니다.

+++세부 정보
예를 들어 페이지에 6개의 이미지가 있는 회전 메뉴가 포함되어 있고 이미지를 회전 메뉴의 두 번째 이미지와 바꾸려는 경우 [!UICONTROL Change Image] 작업이 작동하지 않습니다.

해결 방법은 상위 컨테이너를 선택하고 [!UICONTROL Edit HTML] 작업을 사용하여 회전판의 HTML을 편집하여 원하는 이미지의 이미지 소스를 업데이트하는 것입니다.

+++

### mbox에서 이미지 크기를 조정할 수 없습니다.

+++세부 정보
mbox 요소에서 이미지를 교체한 다음, mbox 요소 크기에 따라 해당 이미지의 크기를 조정하려고 하면, 크기 조정이 허용되지 않습니다.

+++

### 이미지를 교체한 후에는 [!UICONTROL Edit] 작업을 선택할 수 없습니다.

+++세부 정보
이미지를 교체한 후에는 Scene7 URL을 편집할 수 없습니다.

+++

### 외부 소스가 있는 HTML 요소는 편집할 수 없습니다.

+++세부 정보
예: 비디오, 오디오 태그, embed, iFrames, 프레임

+++

### 일반 텍스트나 이미지 태그 이외의 항목을 포함하는 앵커 요소에 대해서는 클릭 추적이 작동하지 않습니다.

+++세부 정보
예를 들어 요소에 JavaScript이 포함되어 있으면 클릭 추적이 작동하지 않습니다.

+++

### VEC가 작동하려면 페이지가 URL 매개 변수를 허용해야 합니다.

+++세부 정보
일부 사이트는 페이지에 대한 URL 매개 변수를 모두 제거합니다. 그러나 VEC에는 이러한 매개 변수가 필요합니다.

+++

### 스크립트를 HTML의 일부로 사용하는 동안 외부에서 액세스하는 모든 변수 및 함수는 창 네임스페이스 아래에 선언되어야 합니다.

+++세부 정보
페이지가 로드된 후 `target.js` 범위 내에서 스크립트가 실행됩니다. 따라서 로컬로 선언된 변수나 함수는 스크립트 블록 외부에서 액세스할 수 없습니다.

*잘못된 코드:*

```html
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*올바른 코드:*

```html
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

+++

### [!UICONTROL Content] 라이브러리(Scene7)에서 이미지를 삽입하고 HTML을 편집하면 이미지 URL이 손상됩니다.

+++세부 정보
일부 더미 텍스트를 사용하여 &#39;customHeaderMessage&#39; div 내에 앵커 요소를 추가합니다.

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

[!UICONTROL Insert Element] 작업을 사용하여 이 div를 선택하여 이 더미 텍스트 div의 형제 이미지로 이미지를 삽입합니다.

이미지 삽입 후 모습은 다음과 같습니다.

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

더미 텍스트 span을 제거합니다.

+++

### VEC의 `customCode` 작업이 [!DNL Internet Explorer] 8에서 작동하지 않습니다.

+++세부 정보
스크립트 콘텐츠를 처리할 때 IE8 제한 사항으로 인해 `target.js`은(는) IE8에서 이를 지원하지 않습니다. 해결 방법으로, 페이지가 jQuery를 포함하고 창 개체에 전역적으로 노출되는 경우 `target.js`은(는) `customCode` 작업을 전달할 수 있습니다. `window.jQuery` 및 `window.jQuery.fn.prepend`이(가) 정의되어 있는지 확인하십시오.

+++

### 클릭 추적은 경험이 만들어진 페이지나 리디렉션된 페이지에서만 지원됩니다.

+++세부 정보
VEC에서 클릭 추적에 [!UICONTROL Browse] 모드를 사용할 수 있지만 [!UICONTROL Browse] 모드는 페이지에서 클릭 추적을 추가하는 데 사용할 수 없습니다.

+++
