---
keywords: adobe.target.getOffer;getOffer;getoffer;get offer;at.js;functions;function
description: Adobe Target at.js JavaScript 라이브러리에 대한 adobe.target.getOffer(options) 함수 정보입니다.
title: adobe.target.getOffer(옵션)
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 8789d750e9e0245d88d54a8d3fe342e5b2e616fc
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 97%

---


# adobe.target.getOffer(옵션)

이 함수는 Target 오퍼를 가져오는 요청을 실행합니다.

`adobe.target.applyOffer()`와 함께 사용하여 응답을 처리하거나 자체적인 성공 처리를 사용할 수 있습니다. 옵션 매개 변수는 필수이며 다음 구조를 갖습니다.

| 키 | 유형 | 필수 | 설명 |
|--- |--- |--- |--- |
| mbox | 문자열 | 예 | Mbox 이름 |
| params | 개체 | 아니오 | Mbox 매개 변수입니다. 다음 구조를 가진 키 - 값 쌍의 개체입니다.<br>`{ "param1": "value1", "param2": "value2"}` |
| 성공 | 함수 | 예 | 서버에서 응답을 받았을 때 실행할 콜백입니다. 성공 콜백 함수는 오퍼 개체의 배열을 나타내는 단일 매개 변수를 수신합니다. 다음은 성공 콜백 예입니다.<br>`function handleSuccess(response){......}`<br>자세한 내용은 아래의 &quot;응답&quot;을 참조하십시오. |
| 오류 | 함수 | 예 | 오류가 발생한 경우 실행할 콜백입니다. 오류가 있는 것으로 간주되는 몇 가지 경우가 있습니다.<ul><li>HTTP 상태 코드가 200 정상이 아닙니다.</li><li>응답을 구문 분석할 수 없습니다. 예를 들어, JSON이 잘못 구성되었거나 JSON 대신 HTML이 구성되었습니다.</li><li>응답에 &quot;오류&quot; 키가 포함되어 있습니다. 예를 들어, 요청을 제대로 처리할 수 없다는 예외가 에지에서 발생했습니다. mbox가 차단되어 컨텐츠를 검색할 수 없는 등의 경우 오류가 발생했습니다. 오류 콜백 함수는 두 개의 매개 변수(status 및 error)를 수신합니다. 다음은 오류 콜백 예제입니다. `function handleError(status, error){......}`</li></ul>자세한 내용은 오류 응답을 참조하십시오. |
| timeout | 숫자 | 아니오 | 시간 초과(밀리 초)입니다. 지정하지 않으면 at.js의 기본 시간 초과가 사용됩니다.<br>기본 시간 초과는 관리 > 구현의 [!DNL Target] UI에서 설정할 수 [!UICONTROL 있습니다]. |

## 예 {#section_97C2D2E03E6549BEA7F4873E3F5E4A0D}

getOffer()와 함께 매개 변수 추가 및 성공 처리를 위해 applyOffer() 사용

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

getOffer()와 함께 매개 변수 및 프로필 매개 변수 추가, 성공 처리를 위해 applyOffer() 사용

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2, 
     "profile.age": 27, 
     "profile.gender": "male" 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

getOffer()와 함께 사용자 지정 시간 초과 및 사용자 지정 성공 처리 사용:

&quot;YOUR_OWN_CUSTOM_HANDLING_FUNCTION&quot;은 고객이 정의하는 함수의 자리 표시자입니다.

```
adobe.target.getOffer({     
  "mbox": "target-global-mbox",   
  "success": function(offer) { 
    YOUR_OWN_CUSTOM_HANDLING_FUNCTION(offer);   
  }, 
  "error": function(status, error) {                 
    console.log('Error', status, error);   
  },   
  "timeout": 2000 
});
```

## 응답 {#section_CF9FD236EF794620BCBF84EB80160183}

성공 콜백에 전달되는 응답 매개 변수는 작업의 배열입니다. 작업은 개체로, 일반적으로 다음 형식을 갖습니다.

| 이름 | 유형 | 설명 |
|--- |--- |--- |
| action | 문자열 | 식별된 요소에 적용할 작업 유형입니다. |
| selector | 문자열 | Sizzle 선택기를 나타냅니다. |
| cssSelector | 문자열 | 요소 사전 숨기기에 사용되는 DOM 네이티브 선택기입니다. |
| 콘텐츠 | 문자열 | 식별된 요소에 적용할 컨텐츠입니다. |

## 예

```
{ 
    "sessionId": "1444512212156-384616", 
    "tntId": "1444512212156-384616.17_35", 
    "offers": [{ 
        "plugins": ["<script type=\"text/javascript\">\r\n/*mboxHighlight+ (1of2) v1 ==> Response Plugin*/\r\nwindow.ttMETA=(typeof(window.ttMETA)!='undefined')?window.ttMETA:[];window.ttMETA.push({'mbox':'target-global-mbox','campaign':'at: redirect ootb','experience':'Experience B','offer':'/at_redirect_ootb/experiences/1/pages/0/1442082890250'});window.ttMBX=function(x){var mbxList=[];for(i=0;i<ttMETA.length;i++){if(ttMETA[i].mbox==x.getName()){mbxList.push(ttMETA[i])}}return mbxList[x.getId()]}\r\n</script>"], 
        "actions": { 
            "content": [{ 
                "passMboxSession": false, 
                "selector": "body", 
                "action": "redirect", 
                "url": "https://example.com/04.html", 
                "includeAllUrlParameters": true 
            }] 
        } 
    }] 
}
```

## 오류 응답 {#section_1ACCE79AF2CB4FA2AD1371EA06AF129F}

오류 콜백에 전달되는 &quot;status&quot; 및 &quot;error&quot; 매개 변수의 형식은 다음과 같습니다.

| 이름 | 유형 | 설명 |
|--- |--- |--- |
| status | 문자열 | 오류 상태를 나타냅니다. 이 매개 변수는 다음 값을 가질 수 있습니다.<ul><li>timeout: 요청 시간이 초과되었음을 나타냅니다.</li><li>parseerror: 응답을 구문 분석할 수 없음을 나타냅니다. JSON 대신 HTML 또는 일반 텍스트가 수신된 경우가 여기에 해당됩니다.</li><li>error: 200 정상이 아닌 HTTP 상태가 수신된 것과 같은 일반적인 오류를 나타냅니다.</li></ul> |
| 오류 | 문자열 | 예외 메시지와 같은 추가 데이터나 문제 해결에 도움이 될 수 있는 기타 항목이 포함됩니다. |