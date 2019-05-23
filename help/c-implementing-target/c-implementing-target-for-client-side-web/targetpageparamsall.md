---
description: 'at. js에 대한 targetpageparamsall () 함수에 대한 정보입니다. '
keywords: adobe.target.notification;요소;선택기;알림;확장 프로그램
seo-description: . js JavaScript 라이브러리의 Adobe Target에 대한 targetpageparamsall () 함수에 대한 정보입니다.
seo-title: . js JavaScript 라이브러리의 Adobe Target에 대한 targetpageparamsall () 함수에 대한 정보입니다.
solution: Target
subtopic: 시작하기
title: targetPageParamsAll()
topic: Standard
translation-type: tm+mt
source-git-commit: d60f2d193fb9e157cb64f93f76d88f97b02a76e8

---


# targetPageParamsAll()

이 방법을 사용하면 요청 코드의 외부에서 모든 mbox에 매개 변수를 첨부할 수 있습니다.

이 메서드는 여러 mbox 호출에 대해 동일한 매개 변수 집합을 포함하는 데 매우 유용합니다. 이 함수는 고객이 정의해야 합니다. 페이지의 모든 mbox 요청에 전달될 매개 변수 배열을 반환해야 합니다. 이 함수는 at.js가 로드되기 전에 또는 **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]** &gt; **[!UICONTROL at.js 설정 편집]** &gt; **[!UICONTROL 코드 설정]** &gt; **[!UICONTROL 라이브러리 헤더]**에서 정의할 수 있습니다.

다음 방법 중 하나로 targetPageParamsAll() 함수를 사용하여 target-global-mbox에 매개 변수를 전달할 수 있습니다.

* 앰퍼샌드로 구분된 목록
* 배열
* JSON 개체

## 예

Ampersand-delimited 목록(값은 URL으로 인코딩되어야 함):

```
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

배열(값은 URL으로 인코딩될 필요가 없음):

```
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON(값은 URL으로 인코딩될 필요가 없음):

```
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
