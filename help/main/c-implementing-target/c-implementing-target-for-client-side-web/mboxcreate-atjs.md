---
keywords: mbox 생성;mbox 생성;mbox 만들기;at.js;함수;함수
description: Adobe에 mboxCreate() 함수 사용 [!DNL Target] mboxDefault 클래스 이름을 사용하는 가장 가까운 DIV에 오퍼를 적용할 at.js JavaScript 라이브러리입니다. (at.js 1.x)
title: mboxCreate() 함수를 사용하려면 어떻게 해야 합니까?
feature: at.js
role: Developer
exl-id: 821ad97a-345a-4e56-9be6-ab1c7d3a651d
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 73%

---

# mboxCreate(mbox,params) - at.js 1.x

요청을 실행하고 mboxDefault 클래스 이름을 사용하는 가장 가까운 DIV에 오퍼를 적용합니다.

>[!NOTE]
>
>이 함수는 at.js 버전 1.*x*&#x200B;에만 사용할 수 있습니다. 이 함수는 at.js 2.x의 릴리스에서 더 이상 사용되지 않으며, at.js 2.x에서 사용하는 경우 기본 콘텐츠를 반환합니다.

이 함수는 [!DNL at.js] 대개 [!DNL mbox.js] (이제 사용되지 않음)에서으로 [!DNL at.js]. `mboxCreate()`에 대한 최신 대안은 `adobe.target.getOffer()`/`adobe.target.applyOffer()` 또는 Angular 지시문입니다.

## 예

```javascript
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## 참고

`mboxCreate()`은 이제 &quot;standard&quot; 종단점 대신 &quot;json&quot; 엔드포인트를 사용하며 비동기식으로 실행됩니다. 이 때문에

* [디버깅](https://developer.adobe.com/target/implement/client-side/target-debugging-atjs/target-debugging-atjs/){target=_blank}은 약간 다릅니다.
* 동기식 호출 차단을 요구하는 오퍼 코드를 피해야 합니다.

   예를 들어, 페이지에서 뒷부분에 나오는 사이트 코드 또는 기타 mbox에 사용되는 JavaScript 변수를 설정하는 오퍼가 여기에 해당합니다.

* [!DNL at.js]에서 자동으로 추가해주지 않으므로 `mboxCreate()`을 호출하기 전에 `<div class="mboxDefault"></div>`가 있는지 확인해야 합니다.

* 비어 있는 페이지 맨 위 `mboxCreate()` 함수는 글로벌 mbox로 권장되지 않습니다.

   [!DNL at.js]의 자동 생성된 글로벌 mbox는 `<head>`에서 발생하고 일찍 컨텐츠를 반환할 수 있으므로 더 나은 선택 사항입니다.
