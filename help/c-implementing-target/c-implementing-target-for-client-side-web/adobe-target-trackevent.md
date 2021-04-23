---
keywords: adobe.target.이벤트 추적;이벤트 추적;이벤트 추적;이벤트 추적;at.js;함수;함수;기본값 방지;기본 방지;기본 방지
description: Adobe [!DNL Target] at.js JavaScript 라이브러리에 대해 adobe.target.trackEvent() 함수를 사용하여 사이트에서 클릭 및 전환과 같은 사용자 작업을 보고하라는 요청을 실행합니다.
title: adobe.target.trackEvent() 함수를 어떻게 사용합니까?
feature: at.js
role: Developer
exl-id: 36005236-ce18-4845-b4fb-e52056018bc7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 70%

---

# adobe.target.trackEvent(옵션)

이 함수는 클릭 및 전환과 같은 사용자 작업을 보고하라는 요청을 실행하며, 응답에 있는 활동을 전달하지는 않습니다.

그런 후에 이러한 이벤트 추적 mbox 호출을 사용하여 활동의 지표를 정의할 수 있습니다. 자세한 내용은 [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) 및 [전환 추적](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)을 참조하십시오.

다음은 API 세부 사항입니다.

| 키 | 유형 | 필수 | 설명 |
|--- |--- |--- |--- |
| mbox | 문자열 | 예 | mbox 이름&#x200B;<br>**참고**:trackEvent() 호출이 페이지에서 이미 실행된 mbox 이름으로 실행되는 경우 trackEvent()의 SDID가 재설정되며 페이지의 Target 호출과 다릅니다. 그러나 다른 mbox 이름으로 trackEvent() 호출을 실행하면 trackEvent() 호출의 SDID가 페이지의 페이지 로드 요청/triggerView() 호출과 일관되게 유지됩니다. |
| selector | 문자열 | 아니오 | HTML 요소를 찾는 데 사용되는 CSS 선택기입니다. 이벤트 리스너는 발견된 요소에 첨부됩니다. |
| 유형 | 문자열 | 아니오 | 등록된 이벤트 유형을 나타냅니다. HTML 알려진 이벤트(예: click, mousedown 등)일 수도 있고 사용자 지정 HTML 이벤트일 수도 있습니다. |
| preventDefault | 부울 | 아니오 | 이벤트 리스너 콜백에서 `event.preventDefault()`를 사용할지 여부를 나타냅니다. 기본값은 false입니다.<br>**참고**: `form[submit] and `a[click]`만 지원됩니다. 복잡성 및 지원할 시나리오 양이 많기 때문에 기타 시나리오는 지원되지 않습니다. |
| params | 개체 | 아니오 | Mbox 매개 변수입니다. 다음 구조를 가진 키 - 값 쌍의 개체입니다.<br>`{ "param1": "value1", "param2": "value2"}` |
| timeout | 숫자 | 아니오 | 시간 초과(밀리 초)입니다. <br>지정하지 않으면 기본값이 사용됩니다.<br>`...timeoutInSeconds: 0.15...}` |
| 성공 | 함수 | 아니오 | 이벤트가 보고되었음을 신호로 알리는 데 사용되는 콜백 함수입니다. |
| 오류 | 함수 | 아니오 | 이벤트를 보고할 수 없음을 신호로 알리는 데 사용되는 콜백 함수입니다. |

## 예

```javascript
<a href="https://asite.com">click me!</a> 
```

여기에 `trackEvent`을 지정하기 위한 javaScript 코드가 추가됩니다.

```javascript
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

또는:

```javascript
adobe.target.trackEvent({ 
    "mbox": "clicked-cta", 
    "params": { 
        "param1": "value1" 
    } 
});
```

>[!NOTE]
>
>필수 필드가 설정되지 않은 경우 요청이 실행되지 않고 오류가 발생합니다.
