---
keywords: advanced mbox.js settings;client;server domain;xdomain;compression level;client session id support;secureOnly;client pc id support;pass page;referring url;traffic level;traffic duration;mboxParameters() function body;mboxSupported() function body;mboxCookieDomain() function body;Extra JavaScript;SiteCatalyst plug-in;Get mbox.js as self-extracting JavaScript;flicker;body hiding;hide body
description: mbox.js 설정 페이지에서 여러 설정을 지정하는 데 도움이 되는 정보입니다.
title: mbox.js 구성
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 91%

---


# mbox.js 구성{#configure-mbox-js}

mbox.js 설정 페이지에서 여러 설정을 지정하는 데 도움이 되는 정보입니다.

[!DNL mbox.js] 함수 라이브러리의 기본 설정은 대부분의 [!DNL Target] 고객 요구 사항을 처리합니다.

필요한 경우 [!DNL mbox.js] 설정을 변경하려면 계정 담당자에게 문의하십시오.

다음 설정을 사용할 수 있습니다.

## 고객

계정에 대한 클라이언트 코드입니다.

When viewing [!UICONTROL Administration > Implementation], the Client at the top is the client code for your account.

## 시간 초과

Target 요청 시간 제한입니다.

[ [!UICONTROL 관리] > [구현]]을 볼 때 [시간 초과(초)] 설정은 Target 요청 시간 초과입니다. 기본적으로 이 값은 15초로 설정되지만 2초~5초 사이의 값으로 설정하는 것이 좋습니다.

## XDomain

브라우저가 고유한 도메인(퍼스트 파티 쿠키), Target 도메인 또는 둘 다에 쿠키를 설정하는지를 결정합니다.

이 설정을 변경하면 mbox.js 및 at.js 둘 다에 영향을 미칩니다.

## 압축 수준

mbox.js 라이브러리 파일이 얼마나 압축되는지를 결정합니다. 압축 수준을 늘리면 페이지 로드 시간이 줄어듭니다.

## mboxParameters() 함수 본문

각 mbox 호출에 전달할 추가 매개 변수를 반환합니다.

예:

return &quot;test=123&quot;;

## mboxSupported() 함수 본문

특정 사용자를 제외하기 위해 false를 반환합니다.

예:

return !navigator.userAgent.indexOf(&#39;Safari&#39;) != -1;

다음 브라우저는 허용되거나 제외될 수 있습니다.

* IE 5.0 이상(Windows)
* Netscape 5.0 이상(Mac, Windows, Linux)
* Safari 1.2.4 이상(Mac)
* Mozilla Firefox 1.0 이상(Mac, Windows, Linux)

## mboxCookieDomain() 함수 본문

퍼스트 파티 쿠키를 설정할 도메인을 설명하는 문자열을 반환합니다.

예:

return &quot;YOUR-DOMAIN&quot;;

## 추가 JavaScript

각 페이지에서 실행할 추가 JavaScript를 모두 포함합니다.

## SiteCatalyst 플러그인

Analytics Target 플러그인을 활성화합니다.

활성화된 경우 Analytics 플러그인은 mbox.js에서 플러그인 코드를 생성합니다. 이 플러그인은 Analytics 태그가 지정된 모든 페이지에서 Analytics 태그 정보를 mbox 요청으로 Target 서버에 보냅니다.

Analytics 플러그인은 페이지에서 계속 참조됩니다.

## secureOnly

mbox.js에서 HTTPS만 사용되는지 또는 페이지 프로토콜을 기준으로 HTTP와 HTTPS 간을 전환할 수 있는지를 나타냅니다. 이것은 기본값이 False인 고급 설정입니다.