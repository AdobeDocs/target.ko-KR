---
keywords: at.js faq;at.js 자주 묻는 질문;faq;깜박임;로더;페이지 로더;교차 도메인;파일 크기;파일크기;x-domain;at.js 및 mbox.js;x 전용;교차 도메인;safari;단일 페이지 앱;누락된 선택기;선택기;단일 페이지 애플리케이션;tt.omtrdc.net;spa;Adobe Experience Manager;AEM;ip 주소;httponly;HttpOnly;보안;ip;쿠키 도메인
description: Adobe에 대해 자주 묻는 질문에 대한 답변 읽기 [!DNL Target] at.js JavaScript 라이브러리.
title: at.js에 대한 일반적인 질문과 답변은 무엇입니까?
feature: at.js
role: Developer
exl-id: 937f880a-1842-4655-be44-0a5614c2dbcc
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '2604'
ht-degree: 53%

---

# at.js FAQ

에 대한 FAQ 답변 [!DNL Adobe Target] at.js JavaScript 라이브러리.

## mbox.js와 비교하여 at.js를 사용할 때의 장점은 무엇입니까? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

다음 [!DNL at.js] 라이브러리 대체 [!DNL mbox.js]. 다음 [!DNL mbox.js] 라이브러리가 더 이상 지원되지 않습니다. 하지만 대부분의 사용자에게 [!DNL at.js]는 [!DNL mbox.js]보다 나은 이점을 제공합니다.

여러 가지 이점 중에서 [!DNL at.js]는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다.

다음 다이어그램은 mbox.js를 사용할 때의 페이지 로드 성능과 at.js를 사용할 때의 페이지 로드 성능을 보여줍니다.

![](assets/atjs_vesus_mboxjs.png)

위에서 보듯이 mbox.js를 사용하는 페이지 콘텐츠는 [!DNL Target] 호출이 완료되었습니다. 반면에 at.js를 사용하는 페이지 콘텐츠는 [!DNL Target] 호출이 시작되면 로드가 시작되며 호출이 완료될 때까지 기다리지 않습니다.

## at.js 및 mbox.js가 페이지 로드 시간에 미치는 영향을 무엇입니까? {#page-load}

많은 고객과 컨설턴트는 특히 새 사용자와 재방문 사용자의 컨텍스트에서 비교하여 페이지 로드 시간에 대한 [!DNL at.js]와 [!DNL mbox.js]의 영향을 알고 싶어 합니다. 안타깝게도, 제각각의 고객 구현으로 인해 [!DNL at.js]나 [!DNL mbox.js]가 어떻게 페이지 로드 시간에 영향을 주는지에 대한 구체적 수치를 측정하고 제공하기는 어렵습니다.

그러나 방문자 API가 페이지에 있다면 [!DNL Target] 더 잘 이해할 수 있는 방법 [!DNL at.js] 및 [!DNL mbox.js] 은 페이지 로드 시간에 영향을 줍니다.

>[!NOTE]
>
>방문자 API와 [!DNL at.js] 또는 [!DNL mbox.js]는 글로벌 mbox를 사용하는 경우에만 페이지 로드 시간에 영향을 미칩니다(본문 숨기기 기법으로 인해). 지역 mbox는 방문자 API 통합의 영향을 받지 않습니다.

다음 섹션에서는 새 방문자와 재방문자에 대한 작업 시퀀스를 설명합니다.

### 새 방문자 수

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js/mbox.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 생성 기능이 활성화되어 있을 경우, Target JavaScript 라이브러리는

   * 방문자 개체를 인스턴스화합니다.
   * 다음 [!DNL Target] 라이브러리는 검색을 시도합니다. [!DNL Experience Cloud Visitor ID] 데이터.
   * 이 방문자는 새로운 방문자이므로 방문자 API는 demdex.net에 대한 도메인 간 요청을 실행합니다.
   * 후 [!DNL Experience Cloud Visitor ID] 데이터가 검색되고 [!DNL Target] 이(가) 실행되었습니다.

### 재방문자

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js/mbox.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 만들기가 활성화되어 있으면, [!DNL Target] JavaScript 라이브러리:

   * 방문자 개체를 인스턴스화합니다.
   * 다음 [!DNL Target] 라이브러리는 검색을 시도합니다. [!DNL Experience Cloud Visitor ID] 데이터.
   * 방문자 API는 쿠키의 데이터를 검색합니다.
   * 후 [!DNL Experience Cloud Visitor ID] 데이터가 검색되고 [!DNL Target] 이(가) 실행되었습니다.

>[!NOTE]
>
>새 방문자의 경우 방문자 API가 있을 때 [!DNL Target] 그 일을 하려면 여러 번 전선으로 넘어가야 합니다 [!DNL Target] 요청 포함 [!DNL Experience Cloud Visitor ID] 데이터. 재방문자의 경우, [!DNL Target] 전선으로 넘어가 [!DNL Target] 을 입력하여 개인화된 컨텐츠를 검색합니다.

## 이전 버전의 at.js를 버전 1.0.0으로 업그레이드한 후 응답 속도가 느려진 것 같은 이유는 무엇입니까? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

[!DNL at.js] 버전 1.0.0 이상은 모든 요청을 동시에 실행합니다. 이전 버전은 요청을 순차적으로 실행합니다. 즉, 요청이 큐에 들어가고 [!DNL Target] 는 다음 요청으로 이동하기 전에 첫 번째 요청이 완료될 때까지 기다립니다.

이전 버전의 [!DNL at.js]가 요청을 실행하는 방식은 &quot;head of line blocking&quot;(HOL 블로킹)이라는 현상이 발생하기 쉽습니다. in [!DNL at.js] 1.0.0 이상 [!DNL Target] 병렬 요청 실행으로 전환되었습니다.

예를 들어 [!DNL at.js] 0.9.1에 대한 네트워크 탭 워터폴을 확인하면, 이전 요청이 완료되기 전까지 다음 Target 요청이 시작되지 않는 것을 보게 될 것입니다. [!DNL Target] 이 시퀀스는 [!DNL at.js] 기본적으로 모든 요청이 동시에 시작되는 1.0.0 이상.

응답 시간 관점에서 수학적으로 이 시퀀스를 다음과 같이 요약할 수 있습니다

<ul class="simplelist"> 
 <li> at.js 0.9.1: 모든 응답 시간 [!DNL Target] 요청 = 요청 응답 시간 합계 </li> 
 <li> at.js 1.0.0 이상: 모든 응답 시간 [!DNL Target] 요청 = 최대 요청 응답 시간 </li> 
</ul>

다음 [!DNL at.js] 라이브러리 버전 1.0.0은 요청을 더 빨리 완료할 수 있도록 지원합니다. 게다가, [!DNL at.js] 요청은 비동기적이므로 [!DNL Target] 페이지 렌더링을 차단하지 않습니다. 요청이 완료되기까지 수 초가 걸리는 경우에도 여전히 렌더링된 페이지가 표시되며, 이 페이지의 일부 부분만 공백으로 표시됩니다 [!DNL Target] 에서 응답을 가져옵니다. [!DNL Target] edge.

## 로드해도 되나요 [!DNL Target] 라이브러리를 비동기적으로 사용할 수 있습니까? {#section_AB9A0CA30C5440C693413F1455841470}

at.js 1.0.0 릴리스를 사용하면 [!DNL Target] 라이브러리를 비동기식으로 사용할 수 있습니다.

at.js를 비동기적으로 로드하려면 다음을 수행하십시오.

* 권장되는 방법은 의 태그를 사용하는 것입니다 [!DNL Adobe Experience Platform].
* at.js를 로드하는 스크립트 태그에 비동기 속성을 추가하여 at.js를 비동기로 로드할 수도 있습니다. 다음과 같은 코드를 사용하십시오.

   ```
   <script src="<URL to at.js>" async></script>
   ```

* 다음 코드를 사용하여 at.js를 비동기식으로 로드할 수도 있습니다.

   ```
   var script = document.createElement('script'); 
   script.async = true; 
   script.src = "<URL to at.js>"; 
   document.head.appendChild(script);
   ```

at.js를 비동기식으로 로드하는 것은 브라우저 렌더링이 차단되지 않도록 하는 좋은 방법입니다. 그러나 이 기법은 웹 페이지에서 플리커를 유발할 수 있습니다.

페이지(또는 지정된 부분)를 숨긴 다음 at.js 및 글로벌 요청이 로드된 후 표시하는 사전에 숨기는 코드 조각을 사용하여 플리커를 방지할 수 있습니다. at.js를 로드하기 전에 코드 조각을 추가해야 합니다.

비동기식으로 at.js를 배포하는 경우 [!DNL Adobe Experience Platform] 구현하려면 구현 전에 페이지에 사전에 숨기는 코드 조각을 직접 포함해야 합니다 [!DNL Target] 사용 [!DNL Adobe Experience Platform] 포함 코드.

동기 DTM 구현을 통해 at.js를 배포하는 경우 페이지 상단에서 트리거된 페이지 로드 규칙을 통해 사전에 숨기는 코드 조각을 추가할 수 있습니다.

자세한 내용은 [at.js에서 플리커를 관리하는 방법](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/){target=_blank}.

## at.js가 [!DNL Adobe Experience Manager] 통합(Experience Manager)? {#section_6177AE10542344239753764C6165FDDC}

FP-11577을 사용하는 [!DNL Adobe Experience Manager] 6.2(또는 이상)에서는 이제 [!DNL at.js]Adobe Target 클라우드 서비스[!UICONTROL  통합을 통해 ] 구현을 지원합니다. 

## at.js를 사용하여 페이지 로드 플리커를 방지하려면 어떻게 합니까? {#section_4D78AAAE73C24E578C974743A3C65919}

Target에서는 페이지 로드 플리커를 방지하기 위한 여러 가지 방법을 제공합니다. 자세한 내용은 [at.js를 사용하여 플리커 방지](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/){target=_blank}.

## at.js의 파일 크기는 얼마입니까? {#section_6A25C9A14C66441785A7635FEF5C4475}

at.js 파일은 다운로드 시 약 109KB입니다. 그러나 대부분의 서버는 파일 크기를 줄이기 위해 파일을 자동으로 압축하므로, at.js는 서버에서 압축되고(GZIP 또는 다른 방법 사용) 사용자가 웹 사이트를 방문하여 로드될 때 약 34KB입니다. at.js를 설치한 서버의 압축 설정이 실제 압축 크기를 결정합니다.

## at.js가 mbox.js보다 큰 이유는 무엇입니까? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

at.js 구현은 단일 라이브러리([!DNL at.js])를 사용하는 반면, mbox.js 구현은 실제로 두 개의 라이브러리([!DNL mbox.js]와 [!DNL target.js])를 사용합니다. 따라서 공정한 비교는 at.js 대 mbox.js *와* `target.js`입니다. gzip으로 압축된 두 버전의 크기를 비교하면 at.js 버전 1.2는 34KB이고 mbox.js 버전 63은 26.2KB입니다. ``

at.js는 mbox.js와 비교하여 훨씬 더 많은 DOM 구문 분석을 수행하므로 더 adfd큽니다. 이것은 at.js가 JSON 응답에 있는 &quot;원시&quot; 데이터를 가져오고 이를 이해해야 하기 때문에 필요합니다. 사용된 mbox.js `document.write()` 모든 구문 분석은 브라우저가 수행했습니다.

파일이 큼에도 불구하고 테스트를 해보면 mbox.js에 비해 at.js를 사용할 때 페이지가 더 빨리 로드됩니다. 또한 at.js는 추가적인 파일을 동적으로 로드하거나 사용하지 않으므로 보안 관점에서 더 우수합니다 `document.write`.

## at.js 안에 jQuery가 있습니까? 이미 웹 사이트에 jQuery가 있으므로 at.js에서 이 부분을 제거할 수 있습니까? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

at.js는 현재 jQuery의 일부를 사용하므로 at.js의 맨 위에 MIT 라이센스 알림이 표시됩니다. jQuery가 노출되지 않았으며 이미 페이지에 있는 jQuery 라이브러리도 방해하지 않으므로 다른 버전일 수 있습니다. at.js 내의 jQuery 코드 제거는 지원되지 않습니다.

## at.js는 x 전용으로 설정된 교차 도메인과 Safari를 지원합니까? {#section_114EC271A6E045E1B2183B66F1B71285}

아니요. 교차 도메인이 x 전용으로 설정되어 있고 Safari에 타사 쿠키가 비활성화되어 있다면, 모두 [!DNL mbox.js] 및 at.js는 비활성화된 쿠키를 설정하며 해당 특정 클라이언트의 도메인에 대해 mbox 요청이 실행되지 않습니다.

Safari 방문자를 지원하기 위해 더 나은 X-Domain이 &quot;비활성화&quot;(퍼스트 파티 쿠키만 설정)되거나 &quot;활성화&quot;(Safari에서 퍼스트 파티 쿠키만 설정하고 기타 브라우저에서는 퍼스트 파티 쿠키와 타사 쿠키 설정)됩니다.

## 다음 기능을 사용할 수 있습니까 [!DNL Target] 단일 페이지 애플리케이션에서 시각적 경험 작성기(VEC)를 사용할 수 있습니까? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

예. at.js 2.x를 사용하는 경우 SPA용 VEC를 사용할 수 있습니다. 자세한 내용은 [SPA(단일 페이지) 시각적 경험 작성기](/help/main/c-experiences/spa-visual-experience-composer.md).

## 다음 기능을 사용할 수 있습니까 [!DNL Adobe Experience Cloud] at.js 구현으로 디버거를 사용하시겠습니까? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

예. 디버깅 목적으로 mboxTrace를 사용하거나 브라우저의 개발자 도구를 사용하여 네트워크 요청을 검사하고, &quot;mbox&quot;로 필터링하여 mbox 통화를 가려낼 수도 있습니다.

## at.js를 사용하는 mbox 이름에 특수 문자를 사용할 수 있습니까? {#section_8E31D2E8A27642098934D7DACFB2A600}

예, mbox.js에서와 같습니다.

## 웹 페이지에서 mbox가 실행되지 않는 이유는 무엇입니까? {#section_4BA5DA424B734324AAB51E4588FA50F5}

[!DNL Target] 고객들이 테스트나 간단한 개념 입증 용도로 [!DNL Target]에 클라우드 기반 인스턴스를 사용하는 경우가 있습니다. 이러한 도메인 및 기타 많은 다른 도메인이 [공용 접미사 목록](https://publicsuffix.org/list/public_suffix_list.dat)에 나와 있습니다.

최신 브라우저에서는 을 사용자 지정하지 않는 한 이러한 도메인을 사용하는 경우 쿠키를 저장하지 않습니다 `cookieDomain` targetGlobalSettings() 를 사용하여 설정하는 중입니다. 자세한 내용은 [Target에서 클라우드 기반 인스턴스 사용](https://developer.adobe.com/target/implement/client-side/target-debugging-atjs/targeting-using-cloud-based-instances/){target=_blank}.

## at.js를 사용할 때 IP 주소를 쿠키 도메인으로 사용할 수 있습니까? {#section_8BEEC91A3410459D9E442840A3C88AF7}

예, [at.js 버전 1.2 이상](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}. [!DNL Adobe] 그러나 최신 버전을 사용하여 최신으로 유지하는 것이 좋습니다.

>[!NOTE]
>
>at.js 버전 1.2 이상을 사용하는 경우에는 다음 예가 필요하지 않습니다.

사용 방법에 따라 [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}. at.js를 다운로드한 후 코드를 추가로 수정해야 할 수 있습니다. 예를 들어, 다양한 웹 사이트에서 [!DNL Target] 구현들에 대해 약간씩 다르게 설정해야 하지만 이러한 설정을 사용자 지정 JavaScript를 사용하여 동적으로 정의할 수 없다면, 파일을 다운로드한 후 각 웹 사이트에 업로드하기 전에 이러한 사용자 지정을 수동으로 수행하십시오.

다음 예에서는 `targetGlobalSettings()` at.js 함수를 사용하여 IP 주소를 지원하는 코드 조각을 삽입할 수 있습니다.

이 예는 단일 IP 주소용입니다.

```
if (window.location.hostname === '123.456.78.9') { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

이 예는 IP 주소 범위용입니다.

```
if (/^123\.456\.78\..*/g.test(window.location.hostname)) { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

## &quot;누락된 선택기 관련 작업&quot;과 같은 경고 메시지가 표시되는 이유는 무엇입니까? {#section_C36BED5B16634361A1BA46FCB731489D}

이 메시지는 [!DNL at.js] 기능을 사용할 수 있습니다. [!DNL at.js] 라이브러리는 DOM에서 찾을 수 없는 모든 것을 보고합니다.

이 경고 메시지가 표시되는 경우 가능한 근본 원인은 다음과 같습니다.

* 페이지가 동적으로 작성되고 있으며 at.js가 요소를 찾을 수 없습니다.
* 느린 네트워크로 인해 페이지가 천천히 빌드되고 있으므로 at.js가 DOM에서 선택기를 찾을 수 없습니다.
* 를 활성화하는 페이지 구조[!UICONTROL y이(가) 실행 중입니다. 에서 활동을 다시 여는 경우 ]VEC(시각적 경험 작성기)에서 경고 메시지가 표시됩니다. 필요한 모든 요소를 찾을 수 있도록 활동을 업데이트합니다.
* 기본 페이지가 [!UICONTROL 단일 페이지 애플리케이션] (SPA) 또는 페이지에 페이지 및 [!DNL at.js] &quot;선택기 폴링 메커니즘&quot;이 해당 요소를 찾을 수 없습니다. `selectorsPollingTimeout`을 늘리는 것이 도움이 될 수 있습니다. 자세한 내용은 [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.
* 지표가 설정된 URL과 관계없이 모든 클릭 추적 지표가 모든 페이지에 추가되려고 시도합니다. 그 자체로 문제가 안 되더라도 이렇게 되면 많은 메시지가 표시됩니다.

   최상의 결과를 얻으려면 최신 버전의 [!DNL at.js]를 다운로드하여 사용하십시오. 자세한 내용은 [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} 및 [at.js 다운로드 를 참조하십시오](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/){target=_blank}.

## 도메인 tt.omtrdc.net이란 무엇입니까? [!DNL Target] 서버 호출이 로 연결됩니까? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net]은 Target에 대한 모든 서버 호출을 받는 데 사용되는 Adobe 에지 네트워크의 도메인 이름입니다.

## at.js가 항상 HttpOnly 및 Secure 쿠키 플래그를 사용하지 않는 이유는 무엇입니까? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly는 서버 측 코드를 통해서만 설정할 수 있습니다. [!DNL Target] mbox와 같은 쿠키는 JavaScript 코드를 통해 생성 및 저장되므로 [!DNL Target] HttpOnly 쿠키 플래그를 사용할 수 없습니다. [!DNL Target] 은 교차 도메인이 활성화될 때 서버 측에서 설정된 타사 쿠키에 대해 HttpOnly 설정을 사용합니다.

HTTPS를 통해 페이지를 로드한 경우에만 JavaScript를 통해 보안을 설정할 수 있습니다. 페이지가 처음에 HTTP를 통해 로드된 경우에는 JavaScript에서 이 플래그를 설정할 수 없습니다. 또한 보안 플래그를 사용하는 경우 HTTPS 페이지에서만 쿠키를 사용할 수 있습니다. HTTPS를 통해 로드된 페이지의 경우, [!DNL Target] 보안 및 SameSite=None 속성을 설정합니다.

확인 [!DNL Target] 쿠키가 클라이언트측에서 생성되므로, 사용자를 제대로 추적할 수 있습니다. [!DNL Target] 은 위에서 언급한 상황을 제외하고 이러한 플래그 중 하나를 사용하지 않습니다.

## at.js가 네트워크 요청을 얼마나 자주 실행합니까? {#section_57C5235DF7694AF093A845D73EABADFD}

[!DNL Target] 서버 측에서 모든 의사 결정을 실행합니다. 즉, at.js는 페이지가 다시 로드되거나 at.js 공용 API가 호출될 때마다 네트워크 요청을 실행합니다.

## 최상의 사례 시나리오에서 사용자가 콘텐츠를 숨기고, 대체하고, 표시하는 것과 관련된 페이지 로드에 가시적인 영향을 미치지 않을 것으로 기대할 수 있습니까? {#section_CB3C566AD61F417FAC0EC5AC706723EB}

at.js는 장기간 HTML BODY 또는 기타 DOM 요소를 사전에 숨기지 않으려고 시도하지만 이는 네트워크 조건 및 활동 설정에 따라 다릅니다. at.js에서 제공하는 [설정](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank} 본문 숨기기 CSS 스타일을 사용자 지정하는 데 사용할 수 있으므로 전체 HTML BODY를 공백으로 남기지 않고 페이지의 일부만 미리 숨길 수 있습니다. 이러한 부분에는 &quot;개인화&quot;해야 하는 DOM 요소가 포함될 것으로 예상됩니다.

## 사용자가 활동 자격이 있는 평균 시나리오의 이벤트 순서는 무엇입니까? {#section_56E6F448E901403FB77DF02F44C44452}

at.js 요청은 비동기 `XMLHttpRequest`이므로 다음 단계를 실행합니다.

1. 페이지가 로드됩니다.
1. at.js는 HTML BODY를 미리 숨깁니다. HTML BODY 대신 특정 컨테이너를 미리 숨길 수 있는 설정이 있습니다.
1. at.js 요청이 실행됩니다.
1. 다음 이후 [!DNL Target] 응답이 수신되었습니다. [!DNL Target] CSS 선택기를 추출합니다.
1. CSS 선택기 사용, [!DNL Target] 에서는 사용자 지정할 DOM 요소를 미리 숨길 스타일 태그를 만듭니다.
1. HTML BODY 미리 숨김 STYLE이 제거되었습니다.
1. [!DNL Target] DOM 요소에 대한 폴링을 시작합니다.
1. DOM 요소가 발견되면 [!DNL Target] DOM 변경 사항을 적용하고 요소 사전 숨김 STYLE이 제거됩니다.
1. DOM 요소를 찾을 수 없으면 글로벌 시간 제한은 페이지가 끊기지 않도록 요소를 숨기지 않습니다.

## at.js가 활동이 변경하는 요소를 최종적으로 숨기지 않을 때 페이지의 콘텐츠는 얼마나 자주 로드 및 표시됩니까? {#section_01AFF476EFD046298A2E17FE3ED85075}

위의 시나리오를 고려할 때, at.js가 활동이 변경하는 요소를 최종적으로 숨기지 않으면 페이지의 콘텐츠는 얼마나 자주 로드 및 표시됩니까? 다시 말해, 페이지는 활동 콘텐츠를 제외하고 완전히 표시되며, 나머지 콘텐츠는 잠시 후에 표시됩니다.

at.js는 페이지의 렌더링을 차단하지 않습니다. 사용자는 페이지에 사용자 지정된 요소를 나타내는 일부 빈 영역이 있음을 알 수 있습니다 [!DNL Target]. 적용할 콘텐츠에 SCRIPT 또는 IMG와 같은 원격 자산이 포함되지 않은 경우 모든 것을 빠르게 렌더링해야 합니다.

## 완전히 캐시된 페이지는 위의 시나리오에 어떻게 영향을 줍니까? 페이지의 나머지 콘텐츠를 로드한 후에 활동 콘텐츠가 눈에 더욱 잘 띄게 표시될 수 있습니까? {#section_CE76335A3E0B41CB8253DEE5E060FCDA}

사용자의 위치에 가깝지만 [!DNL Target] edge에서 사용할 수 있지만, 사용자에게 일부 지연이 발생할 수 있습니다. [!DNL Target] 모서리는 전 세계에 잘 분산되어 있으므로 대부분의 경우 문제가 되지 않습니다.

## 대표 이미지가 표시되고 잠시 지연된 뒤 교체될 수 있습니까? {#section_C25B07B25B854AAE8DEE1623D0FA62A3}

다음 시나리오를 고려하십시오.

다음 [!DNL Target] 시간 제한은 5초입니다. 사용자가 대표 이미지를 사용자 지정할 수 있는 활동이 포함된 페이지를 로드합니다. at.js는 적용할 활동이 있는지 확인하기 위한 요청을 보내지만 초기 응답이 없습니다. 에서 응답을 받지 않았기 때문에 사용자는 대표 이미지의 일반 콘텐츠를 볼 수 있다고 가정합니다 [!DNL Target] 관련 활동이 있는지 여부에 대해 설명합니다. 4초 후에 [!DNL Target] 은 활동 콘텐츠와 함께 응답을 반환합니다.

이 단계에서 대체 버전을 표시할 수 있습니까? 따라서 4초 후에 대표 이미지를 교체할 수 있으며 사용자가 이 이미지 교체를 알 수 있습니까?

처음에는 이미지 대표 DOM 요소가 숨겨져 있습니다. 의 응답 후 [!DNL Target] 가 수신되면 at.js는 DOM 변경 사항을 적용합니다(예: IMG를 대체하고 사용자 지정된 대표 이미지 표시).

## at.js에 필요한 HTML doctype은 무엇입니까?

at. s에는 HTML5 doctype이 필요합니다.

이 구문은 다음과 같습니다.

`<!DOCTYPE html>`

HTML5 doctype은 페이지가 표준 모드로 로드되도록 합니다. quirks 모드로 로드할 때 at.js가 사용하는 일부 JS API가 비활성화됩니다. [!DNL Target] quirks 모드에서 at.js를 비활성화합니다.
