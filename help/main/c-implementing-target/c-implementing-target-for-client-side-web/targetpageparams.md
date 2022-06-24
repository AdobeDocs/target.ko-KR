---
keywords: 타겟 페이지 매개변수;타겟 페이지 매개변수;페이지 매개 변수;페이지 매개변수;페이지 매개변수;페이지 매개변수;at.js;함수;함수
description: Adobe에 targetPageParams() 함수 사용 [!DNL Target] at.js JavaScript 라이브러리를 사용하여 요청 코드의 외부에서 글로벌 mbox에 매개 변수를 첨부합니다.
title: targetPageParams() 함수를 사용하려면 어떻게 해야 합니까?
feature: at.js
role: Developer
exl-id: 0772b400-626c-45d8-a4b5-a12691978cf3
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 72%

---

# targetPageParams()

이 방법을 사용하면 요청 코드의 외부에서 글로벌 mbox에 매개 변수를 첨부할 수 있습니다.

이 함수는 여러 mbox 호출에 대해 동일한 매개 변수 집합을 포함하는 데 매우 유용합니다. 이 함수는 고객이 정의해야 합니다. 글로벌 mbox 요청에만 전달될 매개 변수 배열을 반환해야 합니다. 이 함수는 at.js가 로드되기 전에 또는 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 편집]** > **[!UICONTROL 라이브러리 헤더]**.

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