---
keywords: mbox 정의;mbox 정의;mbox 정의;mbox업데이트;mbox 업데이트;mbox 업데이트;at.js;함수;함수
description: Adobe에 mboxDefine() 및 mboxUpdate() 함수를 사용합니다 [!DNL Target] at.js JavaScript 라이브러리를 사용하여 mbox를 정의하거나 업데이트합니다. (at.js 1.x)
title: mboxDefine() 및 mboxUpdate() 함수를 사용하려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 48261be0-c4d0-4961-9712-ef7e0d2cb1c0
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 75%

---

# mboxDefine() 및 mboxUpdate() - at.js 1.x

Adobe Target에서 mbox를 정의하고 업데이트합니다.

>[!NOTE]
>
>이 함수들은 at.js 버전 1.*x*&#x200B;에만 사용할 수 있습니다. 이러한 함수는 at.js 2.x의 릴리스에서 더 이상 사용되지 않으며, at.js 2.x에서 사용하는 경우 기본 콘텐츠를 반환합니다.

`mboxDefine()` 및 `mboxCreate()`은 오퍼가 표시되어야 하는 HTML DIV 요소에 연결되어 있습니다. 이러한 HTML DIV 요소에는 `mboxDefault` 클래스가 있어야 합니다. HTML 요소에 이 클래스가 첨부되어 있지 않으면 깜박임이 느껴질 수 있습니다.

## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

nodeId와 mbox 이름 사이에 내부 매핑을 만들되, 요청을 실행하지 마십시오. `mboxUpdate()`와 함께 사용됩니다. 내장 [!DNL at.js] 대개 [!DNL mbox.js] (이제 사용되지 않음)에서으로 [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

요청을 실행하고 `nodeId`()의 `mboxDefine()`로 식별되는 요소에 오퍼를 적용합니다. `mboxCreate`로 시작된 mbox를 업데이트하는 데도 사용할 수 있습니다. 내장 [!DNL at.js] 대개 [!DNL mbox.js] (이제 사용되지 않음)에서으로 [!DNL at.js]. `mboxDefine()`/ `mboxUpdate()`는 선택기 옵션을 사용하여 [adobe.target.getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) 및 [adobe.target.applyOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md)로 대체할 수 있습니다.

## 예 {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
