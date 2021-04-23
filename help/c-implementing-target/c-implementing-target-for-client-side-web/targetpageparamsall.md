---
keywords: 타겟 페이지 매개변수 전체;타겟 페이지 매개변수 모두;페이지 매개변수 모두;페이지 매개 변수 모두;페이지 매개 변수;페이지 매개 변수;at.js;함수;함수
description: Adobe [!DNL Target] at.js JavaScript 라이브러리에 대한 targetPageParamsAll() 함수를 사용하여 요청 코드 외부의 모든 mbox에 매개 변수를 첨부합니다.
title: targetPageParamsAll() 함수를 사용하려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 58fbb62e-30da-486f-b771-6452ad5e27e6
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 72%

---

# targetPageParamsAll()

이 방법을 사용하면 요청 코드의 외부에서 모든 mbox에 매개 변수를 첨부할 수 있습니다.

이 메서드는 여러 mbox 호출에 대해 동일한 매개 변수 집합을 포함하는 데 매우 유용합니다. 이 함수는 고객이 정의해야 합니다. 페이지의 모든 mbox 요청에 전달될 매개 변수 배열을 반환해야 합니다. 이 함수는 at.js를 로드하기 전에 정의하거나 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 편집]** > **[!UICONTROL 코드 설정]** > **[!UICONTROL 라이브러리 헤더]**&#x200B;에서 정의할 수 있습니다.

다음 방법 중 하나로 targetPageParamsAll() 함수를 사용하여 target-global-mbox에 매개 변수를 전달할 수 있습니다.

* 앰퍼샌드로 구분된 목록
* 배열
* JSON 개체

## 예

Ampersand-delimited 목록(값은 URL으로 인코딩되어야 함):

```javascript
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

배열(값은 URL으로 인코딩될 필요가 없음):

```javascript
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON(값은 URL으로 인코딩될 필요가 없음):

```javascript
targetPageParamsAll = function() { 
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
