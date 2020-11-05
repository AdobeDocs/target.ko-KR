---
keywords: mbox.js changes;mbox.js versions
description: 이 페이지에는 각 mbox.js 버전에 대한 변경 사항이 표시됩니다.
title: mbox.js 버전 세부 정보
feature: null
subtopic: Getting Started
uuid: 5f8e0511-637b-4c17-bb19-aa7f4d7c98ea
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '2320'
ht-degree: 98%

---


# mbox.js 버전 세부 정보{#mbox-js-version-details}

이 페이지에는 각 mbox.js 버전에 대한 변경 사항이 표시됩니다.

>[!NOTE]
>
>모든 mbox.js 사용자가 버전 57 이상으로 업그레이드하는 것이 좋습니다. 일부 사용자의 경우 `target.js`를 로드할 수 없을 때 시간 초과 문제가 발생했습니다. 버전 57에서는 해당 문제가 해결되었습니다. 그러나 [!DNL Experience Cloud Visitor ID] 서비스를 사용하는 경우에는 버전 58 이상이 필요합니다.

Target이 페이지의 호출에 응답하는 방식은 사용 중인 Target 라이브러리 버전, 방문자 ID 구현이 존재하는지 여부, 방문자 ID가 있는지 여부에 따라 다릅니다. 자세한 내용은 [라이브러리 버전별 Target 호출 응답](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/call-responses-library-version.md#concept_A95A4758A1E7405D947E9B4BCB5D62F0)을 참조하십시오.

>[!NOTE]
>
>mbox.js 라이브러리는 더 이상 개발되지 않습니다. 모든 고객은 mbox.js에서 at.js로 마이그레이션해야 합니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오.

## mbox.js 버전 63 {#section_ED8EFCF653A845ED8927F759578C4A33}

**Target 릴리스:** 17.7.1

이제 [!DNL mbox.js] 버전 63을 사용할 수 있습니다. 자세한 내용은 [mbox.js 다운로드](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/target-download-config-mbox.md)를 참조하십시오.

다음 개선 사항 및 수정 사항이 [!DNL mbox.js] 버전 63에 포함되어 있습니다.

* `mboxDefine()`과 `mboxUpdate()`를 사용할 때 SDID 생성과 관련된 문제를 수정합니다. 이러한 사항은 페이지에서 방문자 API가 있는 클라이언트에만 영향을 줍니다.

## mbox.js 버전 62 {#section_723A9119FE204183847D3B0929A99B41}

* Google Chrome 브라우저에서 볼 때 리디렉션 활동에서 발생하는 깜박임 문제가 수정되었습니다.
* mbox.js에서 HTTPS만 사용되는지 또는 페이지 프로토콜을 기준으로 HTTP와 HTTPS 간을 전환할 수 있는지를 나타내는 `secureOnly` 설정이 추가되었습니다. 이것은 기본값이 False인 고급 설정입니다.

## mbox.js 버전 61 {#section_F3B59C5578B64883AE013B9342151193}

**Target 릴리스:** 16.7.2

**릴리스 날짜:** 2016년 7월 28일

mbox.js 버전 61에는 다음과 같은 향상된 기능이 포함되어 있습니다. 

* 이제 JavaScript Date API의 mboxSession ID 생성 알고리즘에서 타임스탬프와 임의 문자열을 사용하는 대신 무작위 문자열을 생성합니다.
* 다음 세부 사항은 페이지에 방문자 API가 있는 경우에만 적용됩니다.

   * [!DNL mbox.js] 버전 61은 방문자 API `loadTimeout` 속성을 재정의하지 않습니다. 클라이언트는 `visitorApiTimeout` + `visitorApiPageDisplayTimeout`을 사용하여 방문자 API 통합을 제어할 수 있습니다.
   * 향후 Adobe Experience Cloud 옵트아웃 기능을 지원하도록 `optoutEnabled` 설정이 추가되었습니다. 기본값은 false입니다. 이 속성이 활성화된 경우 버전 60과 마찬가지로 모든 요청이 [!DNL /ajax] 종단점에 대해 비동기적으로 실행됩니다.
   * 기본적으로 본문 숨기기는 비활성화됩니다. 글로벌 mbox 자동 만들기가 활성화되고 본문 숨기기가 활성화될 경우에만 Target에서 본문 숨기기가 사용됩니다.
   * Experience Cloud 방문자 ID 쿠키가 없는 경우 모든 요청은 첫 번째 페이지 로드 시 [!DNL /ajax]에 대해 비동기적으로 실행됩니다. 두 번째 페이지 로드에서는 방문자 ID 값이 이미 있으므로 Target에서 일반 흐름을 사용합니다.
   * Adobe Analytics를 활동의 보고 소스로 사용하는 경우, mbox.js 버전 61 이상 또는 at.js 버전 0.9.1 이상을 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

## mbox.js 버전 60 {#section_3BDAB885FA13444A8D35940A4BFF5825}

**Target 릴리스:** 16.4.1

**릴리스 날짜:** 2016년 4월 21일

기본적으로 페이지 컨텐츠는 숨겨지지 않습니다. 버전 60은 &quot;전역 mbox 자동 생성&quot; 옵션이 사용되도록 설정되어 있을 때만 페이지 컨텐츠를 숨깁니다. 또한 페이지 숨김을 위해 `display:none` 대신 CSS `opacity:0` 속성을 사용합니다. 이렇게 하면 응답하는 사이트로 적절히 전달되며 [!DNL at.js]에 맞게 조정됩니다.

다음 두 가지 설정을 사용하여 본문을 숨길 수 있습니다.

* `bodyHidingEnabled` 기본값은 false로, HTML BODY가 숨겨지지 않음을 의미합니다.

* bodyHiddenStyle

   기본값은 `body{opacity:0}`입니다. 이 값은 `body{display:none}`과 같은 다른 값으로 변경될 수 있습니다.

이러한 설정은 다음과 같은 내용을 포함하여 재정의할 수 있습니다.

```
<script> 
window.targetGlobalSettings = { 
 bodyHidingEnabled: true, 
 bodyHiddenStyle: "body{opacity:0}", 
 visitorApiPageDisplayTimeout: 2000 
}; 
</script>
```

페이지 숨기기 기술은 스타일 태그를 사용하여 스타일을 추가 및 제거합니다. 이 방법을 사용하면 페이지 숨기기 코드가 실행된 후 사이트의 스타일이 변경되지 않은 상태로 유지됩니다.

**DTM 사용자:** Target UI에는 위 구성을 저장할 방법이 없으므로 자동 가져오기 옵션을 사용하지 못합니다. 위의 지침을 따른 후 컨텐츠를 사용자 지정 호스팅 옵션의 코드 상자에 붙여넣어야 합니다.

또한 버전 60에서 Experience Cloud 방문자 ID 서비스를 위한 [!DNL visitorAPI.js] 파일이 존재하는 경우 AJAX 종단점을 통해 모든 mbox가 요청됩니다. 방문자 API 메서드는 비동기식이므로 이 방식이 필요합니다. 이 접근 방식의 한 가지 이점은 mbox 요청이 렌더링을 차단하지 않으므로 렌더링 시작 시간이 크게 단축된다는 것입니다. 그렇지만 모든 [!DNL Target] 오퍼 컨텐츠가 비동기식으로 실행되므로 모든 오퍼 코드를 그에 따라 작성해야 합니다. `document.write`를 포함하는 오퍼와 이것이 초기 페이지 로드 시 실행될 것임을 가정하는 다른 코드는 예상대로 실행되지 않습니다.

* V60 비동기 호출

   방문자 ID 서비스에서 v60을 사용하는 경우 모든 mbox 호출이 비동기적으로 수행됩니다. 이것은 mbox가 항상 작동했던 방식에서 달라진 것이므로 이 버전으로 업그레이드할 경우 주의하십시오. [ 설명서의 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#section_B586360A3DD34E2995AE25A18E3FB953)비동기 고려 사항[!DNL at.js] 섹션을 검토하여 몇 가지 위험 요소를 이해하십시오([!DNL at.js]에서도 비동기 호출이 사용됨)을 검토하십시오.
* 새 방문자 시나리오에서 깜박임이 발생할 수 있음

   방문자 ID 서비스에서 v58~v60을 사용할 경우 mbox 호출이 실행되기 전에 방문자 ID가 설정되기를 (또는 시간 초과가 발생할 때까지) 기다립니다. 이러한 현상은 새 방문자의 첫 번째 페이지 로드에서 발생합니다.

## mbox.js 버전 59 {#section_FF0E70C4C17E402D8374DE428C5D996E}

**Target 릴리스:** 16.2.1

**릴리스 날짜:** 2016년 2월 17일

mbox.js 버전 59에는 다음과 같은 향상된 기능이 포함되어 있습니다. 

* Mbox 비활성화 시간이 30분으로 감소되었습니다.
* 페이지 숨김/숨김 해제와 관련된 문제가 해결되었습니다.

   버전 58의 경우처럼 페이지를 숨기기 위해 `display:none`이 사용되지 않고 `opacity:0`이 사용됩니다. 이에 따라 페이지를 숨기는 데 사용된 이전 방법으로 인한 응답형 디자인 사이트의 문제가 해결됩니다.

## mbox.js 버전 58 {#section_5070B0D1C87F4937BB97727923DD36C7}

**Target 릴리스:** 15.7.1

**릴리스 날짜:** 2015년 7월 30일

이 버전의 mbox.js는 Target의 보고 소스로 Analytics를 사용하는 경우에 필요하며 Profiles 및 Audiences에서 권장됩니다.

버전 58의 mbox.js를 사용하면 Target 호출이 수행되기 전에 Experience Cloud 방문자 ID 서비스가 방문자 ID를 반환하게 됩니다. 따라서 Profiles 및 Audiences 핵심 서비스를 통해 공유되는 대상 데이터를 방문자 세션의 첫 번째 Target 호출에 사용할 수 있게 됩니다. 테스트 컨텐츠가 반환되기 전에 기본 컨텐츠가 깜박거리는 경우를 방지하기 위해 방문자 ID 서비스가 반환될 때까지 Target은 `<BODY>`를 숨깁니다. 페이지를 숨기는 데 `display:none`이 사용됩니다.

또한 이 업데이트는 Analytics를 Target의 보고 소스로 사용할 경우 Analytics에서 한 페이지만 포함된 방문에 대해 폭발적인 방문자 수가 보고되도록 하는 문제도 해결합니다.

방문자 ID 서비스가 반환되지 않을 경우 Mbox.js는 시간 제한 값을 설정합니다. 방문자 ID 서비스의 기본 시간 제한은 500ms(0.5초)입니다. 추가 시간 제한은 `<BODY>` 태그가 숨겨지는 기간의 상한을 설정합니다. 기본값은 500ms(0.5초)입니다. 이러한 시간 제한은 각 페이지에서 mbox.js 참조 앞에 다음 코드를 삽입하여 변경할 수 있습니다.

```
<script> 
window.targetGlobalSettings = { 
 visitorApiTimeout: 500, 
 visitorApiPageDisplayTimeout: 500 
}; 
</script> 
```

Mbox.js 버전 58 이상에서는 HTML `BODY` 태그가 제공된 직후에 글로벌 mbox에 대한 비 JavaScript 컨텐츠를 실행합니다. 글로벌 mbox에 대한 `<script>` 태그 내의 JavaScript 콘텐츠는 `DOMContentLoaded` 이벤트가 실행된 이후에 실행됩니다. 이 컨텐츠 전달 순서에 따라 글로벌 mbox에 대한 JavaScript 컨텐츠가 제대로 전달되고 렌더링될 수 있습니다.

## mbox.js 버전 57 {#section_6BA1CDBF75B14A94B59E8624ACF583D4}

**Target 릴리스:** 15.4.1

**릴리스 날짜:** 2015년 4월 21일

이 버전에서는 다음과 같은 부분이 변경되었습니다.

* Target Standard에 대해 자동 생성된 글로벌 mbox 응답이 더 이상 document.write()를 사용하거나 `<div>` 요소를 생성하지 않습니다.

   This removes the requirement for the mbox.js file to be the last item in the `<head>` of the page. 이 새 버전으로 업그레이드할 때는 강력한 QA가 권장됩니다.

   이러한 변경 사항 때문에 일부 오퍼 유형을 전달할 때의 동작이 달라질 수 있습니다. 다음은 고려해야 하는 특정 조건입니다.

   * &quot;플러그인 오퍼&quot;의 일부로 반환되는 HTML 컨텐츠가 제대로 렌더링되지 않지만 오퍼 내의 JavaScript는 예상대로 실행됩니다.
   * 글로벌 mbox로 반환되는 JavaScript 오퍼는 `<script>` 태그에 JavaScript 코드가 포함되거나 `src` 속성에 의해 참조될 수 있습니다.

      이를 수행하려면 다음과 같이 스크립트 호출에 `async` 속성을 추가하십시오.

      `<script src='external-url' async='true'></script>`

      `async` 속성은 Internet Explorer에서 지원이 제한되므로(세부 정보: [https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility](https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility)) 이전 IE 버전을 사용하는 방문자는 이러한 타사 스크립트를 포함하는 테스트에서 제외해야 합니다.

* mbox.js의 Extra JavaScript 섹션에서 수행된 변경 때문에 버전 56에서 보고된 문제가 해결되었습니다. Extra JavaScript 섹션의 모든 코드를 전역 범위에서 다시 사용할 수 있습니다.

다음 기능은 mbox.js 버전 57에서 지원되지 않습니다.

* Target Standard에서 생성된 자동 생성 전역 mbox는 Target Classic의 호스팅된 오퍼 유형에서 작동하지 않습니다. 호스팅된 오퍼 유형에는 &quot;사이트의 오퍼&quot; 및 &quot;Test&amp;Target 외부의 오퍼&quot;가 포함됩니다.

   즉, Target Classic에서는 이러한 오퍼 중 하나가 필요할 경우 Target Standard에서 자동 생성 전역 mbox를 선택하지 말아야 합니다.
* JavaScript 플러그인만 지원됩니다.

   플러그인의 오퍼가 JavaScript 코드 및 HTML과 결합되면 JavaScript 코드가 실행되지만 HTML 컨텐츠는 표시되지 않습니다.

mbox.js 버전 57에는 다음과 같은 중요한 수정 사항도 포함되어 있습니다.

* mbox.js v56에서SiteCatalyst 플러그인이 작동되지 않도록 하는 문제가 해결되었습니다.
* 범위 변경으로 인한 추가 JavaScript 오류를 야기하는 문제가 해결되었습니다.
* mboxFactory의 생성자에 대한 변경 사항을 되돌리십시오.

## mbox.js 버전 56 {#section_C4F4A53584B741FF9FD907D81CB7E164}

**Target 릴리스:** 15.1.2

**릴리스 날짜:** 2015년 2월 17일

>[!NOTE]
>
>일부 사용자의 경우 `target.js`를 로드할 수 없을 때 시간 초과 문제가 발생했습니다. 버전 57에서는 해당 문제가 해결되었습니다. 그러나 [!DNL Experience Cloud Visitor ID] 서비스를 사용하는 경우에는 버전 58 이상이 필요합니다.

이 버전에서는 다음과 같은 부분이 변경되었습니다.

* 전역 mbox로의 매개 변수 전달을 지원하기 위한 Premium Recommendations의 변경 사항
* target.js 로드 호출에 5초의 시간 제한이 추가됩니다. 드문 경우지만 파일이 로드되지 않을 경우 페이지는 렌더링되지만 Target Standard 활동은 표시되지 않습니다.
* &quot;extra JavaScript&quot;가 전역 mbox 이전에 실행되도록 이동됨

   v56+의 모든 설정은 네임스페이스됩니다. &quot;extra JavaScript&quot;에서 선언된 함수가 있는 경우 `window`를 접두사로 추가해야 합니다.

   예:

   `function foo {`

   `}`

   다음과 같이 변경:

   `window.foo = function() {`

   `}`

   전역적으로 액세스할 수 있어야 하는 모든 변수 앞에도 `window`를 붙여야 합니다.

* 전달 동안 target.js가 로드되지 못할 경우 mbox.js가 사용자에게 제공하는 &quot;em-disabled&quot;를 호출하는 쿠키가 추가되었습니다. 이 쿠키는 Visual Experience Composer를 사용하여 만든 오퍼가 사이트에서 렌더링되지 못하게 합니다. 이러한 쿠키가 있는 사용자는 테스트 컨텐츠를 보지 못하고 해당 활동 보고서에서 카운트되지도 않습니다. 다른 모든 오퍼 컨텐츠(예: Target Classic의 캠페인)는 계속 로드됩니다. 이 쿠키의 수명은 로드 실패 시간부터 30분입니다.

## mbox 버전 55

**Target 릴리스:** 15.1

**릴리스 날짜:** 2015년 1월 19일

IE 수정 사항으로 버전 53을 수정합니다.

## mbox 버전 54

**Target 릴리스:** 14.9.2

**릴리스 날짜:** 2014년 9월 30일

document.write에서 AJAX에 대한 전역 mbox 구현이 변경되었습니다. 따라서 mbox.js 파일이 페이지의 `<head>` 섹션에 있는 마지막 항목이 될 필요가 없습니다. 이 버전은 API를 통해서만 사용할 수 있습니다. 클라이언트는 이를 다운로드한 후 이 mbox.js 파일을 사용할 수 있습니다. 이 구현에 따라 일부 사이트 경험 컨텐츠가 깜박거리므로 사용자 사이트에서 이러한 통합을 확인하십시오.

## mbox 버전 53

**Target 릴리스:** 14.9.1

**릴리스 날짜:** 2014년 9월 14일

Target 페이지 매개 변수가 Internet Explorer에서 올바르게 실행되지 않는 문제가 해결되었습니다.

## mbox 버전 52

**Target 릴리스:** 14.8

**릴리스 날짜:** 2014년 8월 14일

이제 mboxParameter 함수가 Target Standard 및 Premium에서 작동합니다.

Analytics가 IE 9 및 11에서 추적을 수행하지 못하게 하는 문제가 해결되었습니다. 이러한 변경 사항은 Analytics 사용자에게만 영향을 미칩니다.

이제 targetPageParams() 함수를 사용하여 [매개 변수](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md)를 배열, JSON 개체 또는 쉼표로 구분된 목록(이전에 지원)으로 target-global-mbox에 전달할 수 있습니다.

M2PcId 및 VisitorId와 관련된 모든 항목의 이름이 변경되었습니다.

등록된 mbox의 defaultDiv를 지울 수 있습니다.

## mbox 버전 51

**Target 릴리스:** 14.6

**릴리스 날짜:** 2014년 6월 25일

최상위 도메인에 2개의 문자가 있는 사이트에서 잘못된 쿠키를 설정하던 버그가 수정되었습니다.

해시 태그 값이 반환되도록 하는 mbox.js의 경미한 버그가 수정되었습니다.

## mbox 버전 50

Target Standard와 Target Classic 간 동기화가 개선되었습니다.

## mbox 버전 49

중첩된 mbox에 대한 Internet Explorer 10 지원이 개선되었습니다.

## mbox 버전 48

Target용 보고 소스로서 Adobe Analytics에 대한 지원을 추가했습니다.

## mbox 버전 47

이제 mbox.js는 Target Standard의 사용자 지정 전역 mbox 이름 사용을 지원합니다.

## mbox 버전 46

Target Standard의 단일 코드 행 구현을 위해 Experience Cloud 방문자 ID 서비스에 대한 전체 지원을 추가했었습니다. 이에 따라 서버 측 Adobe Analytics 통합과 Experience Cloud 공유 프로필이 활성화됩니다.

IE10에서 문서 모드로 컨텐츠를 구현할 때의 문제를 수정했습니다.

## mbox 버전 45

Experience Cloud 방문자 ID 서비스에 대한 전체 지원을 추가했습니다. 이에 따라 서버 측 Adobe Analytics 통합과 Experience Cloud 공유 프로필이 활성화됩니다.

## mbox 버전 44

mboxVizTarget에 의해 URL에 다음과 같은 새 매개 변수가 추가되었습니다.

mboxDOMLoaded

## mbox 버전 43

Target Standard에 대한 지원을 추가했었습니다.

## mbox 버전 42

Experience Cloud 공유 방문자 ID 서비스에 대한 초기 지원을 추가했습니다.

## mbox 버전 41

* x-전용 설정이 있더라도 퍼스트 파티 쿠키를 비활성화하여 로드 시간을 줄이고 지속적인 페이지 새로 고침을 방지합니다.

   Target 호출이 제시간에 반환되지 못할 경우 시간 제한 쿠키가 설정됩니다. 타사 쿠키만 사용하는 것보다 이 방법이 더 빠른 효과를 가져옵니다. 타사 쿠키만 사용할 경우 Target 서버에서 적절한 응답을 기다리는 동안 페이지가 계속 새로 고쳐집니다.

* 트래픽 제한이 mbox.js가 활성화되어 있을 때에만 발생하도록 수정했습니다.

   이 문제는 고객이 해당 mbox.js에 트래픽 제한을 설정하여 시간 제한 설정이 작동되지 않도록 하는 경우에 발생했습니다. 이로 인해 Target 서버에서 적절한 응답을 기다리는 동안 페이지가 새로 고쳐집니다.

* SiteCalyst 플러그인이 항상 Ajax 페쳐를 사용하도록 수정했습니다.

   이러한 변경이 수행되기 전에는 Test&amp;Target에서 SiteCatalyst 플러그인을 사용할 때 플러그인이 로드되는 시기에 따라 페이지를 지우는 document.write가 트리거될 수 있는 상황이 발생했습니다.

## mbox 버전 38

페이지 기반 SiteCatalyst에 대한 지원을 Test&amp;Target 통합에 추가했습니다(활성화되어야 함).

## mbox 버전 37

URL 키를 인코딩했습니다.

## mbox 버전 36

mbox가 tt.omtrdc.net을 사용하도록 변경했습니다.

## mbox 버전 35

* 이제 mbox 디버그는 항상 원격입니다.
* mboxTime 매개 변수를 추가했습니다. 이 매개 변수는 epoch, GMT 이후 사용자가 보는 시간(ms)입니다. 이 값은 한 번만 계산됩니다.

## mbox 버전 34

* 캐시된 버전을 참조하는 대신 항상 최신 기본 div를 가져오려고 합니다.

   이렇게 하면 기본 div에 대한 컨텐츠를 제공했던 mboxUpdate로 인해, 캐시된 기본 컨텐츠 div가 DOM에 없게 되는 문제가 수정됩니다 .

* mbox.getDefaultDiv에는 새로운 선택 사항인 부울 매개 변수가 있습니다. true일 경우, 현재 기본 div를 반환합니다. false일 경우, 마지막으로 캐시한 기본 div를 반환합니다.
* Ajax 로드를 지원하도록 mbox.loaded를 업데이트했습니다.
* 이제 mboxURL 매개 변수는 escape가 아니라 encodeURIComponent를 사용하여 인코딩됩니다.
* 브라우저에서 encodeURIComponent를 지원하는지를 테스트하고 지원하지 않는 경우 기본 컨텐츠를 표시합니다. 또한 다음 mbox.js 구성 옵션도 제거했습니다.
   * encode\_mbox\_parameters
   * mbox\_signal\_support
