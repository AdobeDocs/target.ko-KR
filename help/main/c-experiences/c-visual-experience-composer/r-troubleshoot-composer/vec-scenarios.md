---
keywords: 추천
description: VEC(시각적 경험 작성기)에서 페이지에 적용된 변경 사항이 Adobe Target의 경험 표시 기능에 어떻게 영향을 주는지를 보여 주는 일반적인 시나리오를 살펴봅니다.
title: 일반적인 페이지 수정 시나리오는 무엇입니까?
feature: Visual Experience Composer (VEC)
exl-id: 7a05fbf9-3427-436e-a54f-4f1dd16d885a
TQID: 'https://experienceleague.adobe.com/BI2SnUU5ilCf0auld15q1rpCrnLoPEwbe1fZO6G1quc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 4%
---
# 페이지 수정 시나리오 {#vec-scenarios}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Target] 외부의 페이지에 대한 변경 내용이 [!DNL Target]의 경험 표시 기능에 어떻게 영향을 미치는지 7가지 시나리오를 통해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Target] 선택기는 경험이 표시되는 위치를 결정합니다. 페이지가 [!DNL Target] 외부에서 수정되면 변경 내용은 [!DNL Target]이 해당 위치를 찾아 경험을 표시하는 기능에 영향을 줄 수 있습니다.

선택기는 항상 ID와 동등하지 않은 고유한 클래스에서 작동합니다. 요소에 지정된 클래스가 없으면 선택기는 동일한 태그 이름을 가진 이전 동위 멤버를 계산합니다.

>[!NOTE]
>
>시나리오에서는 목록 항목을 예로 사용하지만 개념은 모든 요소에 적용됩니다.

다음 표에서는 시나리오를 요약합니다. 모든 시나리오에서 선택기는 `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`입니다.

| 시나리오 | 액션 적용됨 | 이유 |
|---|---|---|
| 선택한 요소 앞에 다른 클래스 이름을 사용하는 요소를 삽입합니다. | 예 | `li.women-section:eq(0)`은(는) 영향을 받지 않습니다. |
| 선택한 요소와 동일한 클래스 이름을 사용하는 요소 삽입 | 아니요 | 새 요소는 선택기를 벗어나는 첫 번째 위치를 취합니다 |
| 선택한 요소 뒤에 요소 삽입 | 예 | 새 요소가 상위 요소를 기준으로 동일한 위치에 추가됩니다 |
| 선택한 요소 바로 앞에 있는 요소 제거 | 예 | 선택한 항목의 클래스는 변경되지 않습니다. |
| 선택한 요소 바로 다음에 있는 요소 제거 | 예 | 선택한 항목의 클래스는 변경되지 않습니다. |
| 선택한 요소 제거 | 예 | 요소가 정상적으로 제거되었습니다 |
| 선택한 요소의 클래스 이름 바꾸기 | 아니요 | `class`을(를) 찾을 수 없습니다. |

## 선택한 요소 앞에 다른 클래스 이름을 사용하는 요소를 삽입합니다.

새 요소가 [!DNL Target] 선택기에서 요소의 형제 요소로 삽입됩니다. JavaScript에서 요소의 첫 번째 클래스를 추가한 경우 게재가 실패하고 작업이 적용되지 않습니다.

**삽입된 요소:**

```html
<li class="kids-section">Kids</li>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** `li.women-section:eq(0)`은(는) 영향을 받지 않으므로 선택기가 예상대로 작동합니다.

**이전:**

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul>
</div>
```

**이후:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

## 선택한 요소와 동일한 클래스 이름을 사용하는 요소 삽입

목록의 항목을 선택하는 동안 목록이 삽입됩니다.

**삽입된 요소:**

```html
<ul class="nav">
   <li class="item"> Sale </li>
   <li class="item"> Offers </li>
</ul>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** 선택기가 작동하지 않습니다. 이제 `ul.nav:eq(0)`이(가) 동적으로 추가된 요소를 가리키므로 사용할 수 없으므로 작업이 적용되지 않습니다. 활동을 만든 후 동일한 클래스를 사용하는 유사한 목록 항목을 동적으로 또는 수동으로 추가하면 첫 번째 위치에 새 요소가 놓이므로 선택기가 중단됩니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

**후(시도됨):**

```html
<div id="wrap">
     <ul class="nav">
        <li class="item"> Sale</li>
        <li> class="item"> Offers</li>
     </ul>
     <ul class="nav">
       <li class="men-section"> Men</li>
       <li class="women-section">Women</li>
    </ul>
</div>
```

## 선택한 요소 뒤에 요소 삽입

선택한 목록 항목 뒤에 목록이 삽입됩니다.

**삽입된 요소:**

```html
<ul class="nav">
   <li class="men-section"> Men Clothes</li>
   <li class="women-section"> Women Clothes</li>
</ul>
```

**선택한 요소:**

`<li class="women-section">Women Shoes</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** 선택한 항목으로 끝나는 목록 뒤에 목록 삽입이 예상대로 작동합니다. 새 요소는 상위 요소를 기준으로 선택한 요소와 동일한 위치에 추가됩니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>       <li class="women-section">Women Shoes</li>
    </ul>
</div>
```

**이후:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>
        <li class="women-section">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## 선택한 요소 바로 앞에 있는 요소 제거

선택한 요소 앞의 목록 항목입니다.

**제거된 요소:**

```html
<li class="men-section"> Men </li>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** 선택한 항목의 클래스가 변경되지 않았으므로 요소가 제거되었습니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**이후:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## 선택한 요소 바로 다음에 있는 요소 제거

선택한 요소 다음의 목록 항목입니다.

**제거된 요소:**

```html
<li class="kids-section">Kids</li>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** 선택한 항목의 클래스가 변경되지 않았고 제거된 요소의 부모 하위 트리에 고유한 클래스가 있으므로 요소가 제거되었습니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Kids</li>
    </ul>
</div>
```

**이후:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## 선택한 요소 제거

선택한 목록 항목이 삭제되었습니다.

**제거된 요소:**

```html
<li class="women-section">Women</li>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** 요소가 제거되었습니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**이후:**

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## 선택한 요소의 클래스 이름 바꾸기

선택한 목록 항목의 클래스가 변경되었습니다.

**변경된 요소:**

```html
<li class="women-section">Women</li>
```

**선택한 요소:**

`<li class="women-section">Women</li>`

**선택기:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:** `class`을(를) 찾을 수 없으므로 클래스 이름을 바꿀 수 없습니다.

**이전:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**후(시도됨):**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div> 
```
