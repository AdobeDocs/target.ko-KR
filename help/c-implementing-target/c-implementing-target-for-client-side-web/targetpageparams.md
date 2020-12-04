---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;page params;page parameters;at.js;functions;function
description: Adobe Target at.js JavaScript 라이브러리에 대한 targetPageParams() 함수 정보입니다.
title: targetPageParams()
feature: client-side
translation-type: tm+mt
source-git-commit: a841c492e5d9e4bfedb20133ba32e37daf738c57
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 88%

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

이 방법을 사용하면 요청 코드의 외부에서 글로벌 mbox에 매개 변수를 첨부할 수 있습니다.

이 함수는 여러 mbox 호출에 대해 동일한 매개 변수 집합을 포함하는 데 매우 유용합니다. 이 함수는 고객이 정의해야 합니다. 글로벌 mbox 요청에만 전달될 매개 변수 배열을 반환해야 합니다. This function can be defined before at.js is loaded or in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Library Header]**.

다음 방법 중 하나로 `targetPageParams()` 함수를 사용하여 target-global-mbox에 매개 변수를 전달할 수 있습니다.

* 앰퍼샌드로 구분된 목록
* 배열
* JSON 개체

## 예

Ampersand-delimited 목록(값은 URL으로 인코딩되어야 함):

```javascript
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

배열(값은 URL으로 인코딩될 필요가 없음):

```javascript
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON(값은 URL으로 인코딩될 필요가 없음):

```javascript
targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
        "age": 26, 
        "country": { 
          "city": "San Francisco" 
        } 
      } 
  }; 
};
```
