---
keywords: Recommendations
description: 이 주제의 시나리오에서는 페이지에 적용된 변경 내용이 경험을 표시하는 Target의 기능에 어떻게 영향을 주는지를 보여줍니다.
title: 페이지 수정 시나리오
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 100%

---


# 페이지 수정 시나리오 {#page-modification-scenarios}

이 주제의 시나리오에서는 페이지에 적용된 변경 내용이 경험을 표시하는 Target의 기능에 어떻게 영향을 주는지를 보여줍니다.

Target 선택기는 경험을 표시할 위치를 결정합니다. 페이지를 Target 외부에서 수정하는 경우, 변경 사항은 경험을 표시하는 Target의 기능에 영향을 줄 수 있습니다.

선택기를 사용할 때 고유한 클래스는 ID와 동등하지 않습니다. 선택기는 항상 고유한 클래스에서 작동합니다. 요소에 지정된 클래스가 없는 경우 선택기는 태그 이름이 동일한 이전의 동일 수준 요소의 수를 계산합니다.

>[!NOTE]
>
>이 시나리오들에서는 목록 항목을 예로 사용하지만 개념은 모든 요소에 적용됩니다.

## 시나리오: 선택한 요소 앞에 다른 클래스 이름을 사용하는 요소 삽입 {#section_298F661F72384F6AB957D5885A99D822}

이 예에서 새 요소는 Target 선택기에서 해당 요소와 동일한 수준의 요소로 삽입됩니다.

요소에 있는 첫 번째 클래스가 JavaScript에 의해 추가될 가능성이 있습니다. 이 경우 전달은 실패하고 작업이 적용되지 않습니다.

**삽입된 요소:**

```
<li class="kids-section">Kids</li>
```

**선택됨:**

`<li class="women-section">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

`li.women-section:eq(0)`은 영향을 받지 않으므로 선택기가 예상대로 작동합니다.

전:

```
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul> 
</div>
```

후:

```
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

## 시나리오: 선택한 요소와 동일한 클래스 이름을 사용하는 요소 삽입 {#section_0969B88C2F154E648D9969C8C85EF55A}

이 시나리오에서는 목록의 항목을 선택하면 목록을 삽입하려고 시도합니다.

**삽입된 요소:**

```
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```

**선택됨**

`<li class="women-section">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

`ul.nav:eq(0)`은 동적으로 추가된 요소를 제공하므로 선택기가 작동하지 않습니다. 요소를 사용할 수 없으며 작업이 적용되지 않습니다. 활동이 만들어진 후 동일한 클래스를 사용하는 유사한 목록 항목이 동적으로 또는 수동으로 추가되면 첫 번째 위치에 새 요소가 만들어집니다. 이렇게 되면 선택기가 끊깁니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

후(시도됨):

```
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

## 시나리오: 선택한 요소 뒤에 요소 삽입 {#section_15B07B84BEE94ED39D85BBBE0733E170}

이 시나리오에서는 선택한 요소 뒤에 목록 항목이 삽입됩니다.

**삽입된 요소:**

```
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```

**선택됨:**

`<li class="women-section">Women Shoes</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

이 경우, 선택한 목록 항목으로 끝나는 목록 뒤에 목록을 삽입하면 예상대로 작동합니다. 상위 요소와 관련하여 선택된 요소와 동일한 위치에 새 요소가 추가됩니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>       <li class="women">Women Shoes</li>
    </ul>
</div>
```

후:

```
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>
        <li class="women">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## 시나리오: 다른 요소의 바로 앞에 있는 요소 제거 {#section_F193674F04F84AA593EAA1137C880EBA}

이 시나리오에서는 선택한 요소 앞에 있는 목록 항목이 삭제됩니다.

**제거된 요소:**

```
<li class="men-section"> Men </li>
```

**선택됨:**

`<li class="women-section">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

선택한 항목의 클래스가 변경되지 않았으므로 요소가 제거되었습니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

후:

```
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## 시나리오: 다른 요소의 바로 뒤에 있는 요소 제거 {#section_F83B51BE54924FB58679D512DAF1EBB2}

이 시나리오에서는 선택한 요소 뒤에 있는 목록 항목이 삭제됩니다.

**제거된 요소:**

```
<li class="kids-section">Kids</li>
```

**선택됨:**

`<li class="women-section">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

선택한 항목의 클래스가 변경되지 않았으므로 요소가 제거되었습니다. 제거된 요소는 상위 서브 트리 내에 고유한 클래스를 포함합니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Women</li>
    </ul>
</div>
```

후:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## 시나리오: 선택한 요소 제거 {#section_1989CF1E2C344CC5963084ED83C18F9C}

이 시나리오에서는 선택한 목록 항목이 삭제됩니다.

**제거된 요소:**

```
<li class="women-shoes">Women</li>
```

**선택됨:**

`<li class="women-shoes">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

요소가 제거되었습니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```

후

```
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## 시나리오: 선택한 요소의 클래스 이름 변경 {#section_79D244C588BA452DB8E433D82B7F63EA}

이 시나리오에서는 선택한 목록 항목의 클래스가 변경됩니다.

**변경된 요소:**

```
<li class="women-section">Women</li>
```

**선택됨:**

`<li class="women-section">Women</li>`

선택기: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**결과:**

`class`를 찾을 수 없어서 요소 클래스의 이름을 변경할 수 없습니다.

전:

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

후(시도됨):

```
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```
