---
keywords: custom events;at.js;request failed;request succeeded;content rendering failed;content rendering succeeded;library loaded;request start;content rendering start;content rendering no offers;content rendering rediret
description: Adobe Target at.js JavaScript 라이브러리에 대한 사용자 지정 이벤트 정보입니다.
title: at.js 사용자 지정 이벤트
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 8789d750e9e0245d88d54a8d3fe342e5b2e616fc
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 96%

---


# at.js 사용자 지정 이벤트

mbox 요청 또는 오퍼가 실패하거나 성공하는 경우를 알려주는 `at.js custom events`에 대한 정보입니다.

이전에 mbox.js에서는 페이지에서 실행되는 다른 JavaScript 코드가 내부에서 진행되는 상황을 알지 못했습니다. at.js가 발전하면서 이 문제를 해결할 수 있는 기회가 생겼습니다.

고객에 따르면, 다음을 포함하여 알림을 받기 원하는 몇 가지 시나리오가 있습니다.

* 시간 초과, 잘못된 상태 코드, JSON 구문 분석 오류 등으로 인해 mbox 요청이 실패한 경우
* mbox 요청이 성공한 경우
* mbox 요소 누락, 선택기를 찾을 수 없음 등으로 인해 오퍼 렌더링이 실패한 경우
* 오퍼 렌더링이 성공한 경우 DOM 변경 사항이 적용된 경우

사전 정의된 이벤트에는 이벤트 유형에 따라 필수 데이터를 추출할 수 있는 구조가 있습니다.

다른 시나리오에서 이벤트를 사용할 수 있게 하도록 사용자 정의 이벤트에는 이벤트 개체(핸들러에 전달)의 detail 속성에 지정된 페이로드 개체가 있습니다. 또한 문자열을 이벤트 이름으로 전달하지 않도록 하기 위해 `adobe.target.event` 네임스페이스를 사용하여 이벤트가 상수로 표시됩니다.

## 구조 {#section_0E5C9A13DE234A5DAECBCBF9F23F94FE}

| 키 | 유형 | 설명 |
|--- |--- |--- |
| 유형 | 문자열 | at.js와의 상호 작용을 추적, 디버깅 및 사용자 지정하는 데 도움이 되도록 알림을 받으려는 몇 가지 시나리오가 있습니다.<br>아래에 나열된 각 사용자 지정 이벤트는 &quot;상수&quot; 및 &quot;문자열 값&quot;의 두 가지 형식을 갖습니다.<ul><li>**상수**: 앞에 `adobe.target.event.`를 추가하고, 모두 대문자로 표시하고 밑줄 문자를 포함합니다. at.js가 로드된 *후*, mbox 응답이 수신되기 *전에* 사용자 지정 이벤트에 가입하려면 상수를 사용하십시오.</li><li>**문자열 값**: 소문자로 나타내고 대시를 포함합니다. at.js가 로드되기 *전*&#x200B;에 사용자 지정 이벤트에 가입하려면 문자열 값을 사용하십시오.</li></ul>**요청이 실패했습니다**<br> Constant: `adobe.target.event.REQUEST_FAILED`<br>String value: `at-request-failed`<br>Description: An mbox request failed due to timeout, wrong status code, JSON parse error, etc.<br>**요청 성공**<br>&#x200B;상수: `adobe.target.event.REQUEST_SUCCEEDED`<br>문자열 값: `at-request-succeeded`<br>설명: mbox 요청이 성공했습니다.<br>**컨텐츠 렌더링 실패**<br>&#x200B;상수: `adobe.target.event.CONTENT_RENDERING_FAILED`<br>문자열 값: `at-content-rendering-failed`<br>설명: mbox 요소 누락, 선택기를 찾을 수 없음 등으로 인해 오퍼 렌더링이 실패했습니다.<br>**컨텐츠 렌더링 성공**<br>&#x200B;상수: `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`<br>문자열 값: `at-content-rendering-succeeded`<br>설명: 오퍼 렌더링이 성공했습니다. DOM 변경 사항이 적용된 경우&#x200B;<br>**라이브러리를 로드함**<br>&#x200B;상수: `adobe.target.event.LIBRARY_LOADED`<br>문자열 값: `at-library-loaded`<br>설명: 이 이벤트는 at.js가 완전히 로드된 시기를 추적하는 데 이상적입니다. 이 이벤트를 사용하여 글로벌 mbox 실행을 사용자 지정할 수 있습니다. 또한 이 이벤트를 사용하여 글로벌 mbox를 비활성화한 후 이 이벤트를 수신하여 나중에 글로벌 mbox를 실행할 수도 있습니다.<br>**요청 시작**<br>&#x200B;상수: `adobe.target.event.REQUEST_START`<br>문자열 값: `at-request-start`<br>설명: HTTP 요청이 실행되기 전에 이 이벤트가 실행됩니다. 리소스 시간 설정 API를 사용하는 성능 측정에 이 이벤트를 사용할 수 있습니다.<br>**컨텐츠 렌더링 시작**<br>&#x200B;상수: `adobe.target.event.CONTENT_RENDERING_START`<br>문자열 값: `at-content-rendering-start`<br>설명: 선택기 폴링이 시작되고 컨텐츠가 페이지에 렌더링되기 전에 이 이벤트가 실행됩니다. 이 이벤트를 사용하여 컨텐츠 렌더링 진행 상태를 추적할 수 있습니다.<br>**컨텐츠 렌더링 오퍼 없음**<br>&#x200B;상수: `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`<br>문자열 값: `at-content-rendering-no-offers`<br>설명: 반환된 오퍼가 없으면 이 이벤트가 실행됩니다.<br>**컨텐츠 렌더링 리디렉션**<br>&#x200B;상수: `adobe.target.event.CONTENT_RENDERING_REDIRECT`<br>문자열 값: `at-content-rendering-redirect`<br>설명: 오퍼가 리디렉션이고 Target이 다른 URL로 리디렉션될 때 이 이벤트가 실행됩니다. |
| mbox | 문자열 | mbox 이름 |
| message | 문자열 | 발생한 사항, 오류 메시지 등과 같이 사람이 읽을 수 있는 설명을 포함합니다. |
| tracking | 개체 | `sessionId` 및 `deviceId`를 포함합니다. 일부 경우에 `deviceId`이 에지 서버에서 검색할 수 없기 때문에 [!DNL Target]가 누락될 수 있습니다. |

## 사용 {#section_0500FF09D3A04450B5DC8F85C6F793E0}

```
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(event) { 
  console.log('Event', event); 
});
```

## 교육 비디오: 응답 토큰 및 at.js 사용자 지정 이벤트 ![자습서 배지](/help/assets/tutorial.png) {#section_ED304A7137DC42A4BDCD6D57C989F1FA}

다음 비디오를 시청하여 응답 토큰 및 at.js 사용자 지정 이벤트를 사용하여 Target에서 타사 시스템으로 프로필 정보를 공유하는 방법을 학습하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)