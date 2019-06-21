---
description: mbox.js 설정 페이지에서 여러 설정을 지정하는 데 도움이 되는 정보입니다.
keywords: 고급 mbox.js 설정;클라이언트;서버 도메인;xdomain;압축 수준;클라이언트 세션 ID 지원;secureOnly;클라이언트 pc id 지원;페이지 전달;참조 url;트래픽 수준;트래픽 기간;mboxParameters() 함수 본문;mboxSupported() 함수 본문;mboxCookieDomain() 함수 본문;추가 JavaScript;SiteCatalyst 플러그인;mbox.js를 자동 압축 해제 JavaScript;깜박임;본문 숨김;본문 숨기기
seo-description: mbox.js 설정 페이지에서 여러 설정을 지정하는 데 도움이 되는 정보입니다.
seo-title: mbox.js 구성
solution: Target
title: mbox.js 구성
uuid: e79c7af7-f8bd-4e2b-8e67-b04eddf0c65d
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mbox.js 구성{#configure-mbox-js}

mbox.js 설정 페이지에서 여러 설정을 지정하는 데 도움이 되는 정보입니다.

[!DNL mbox.js] 함수 라이브러리의 기본 설정은 대부분의 [!DNL Target] 고객 요구 사항을 처리합니다.

필요한 경우 [!DNL mbox.js] 설정을 변경하려면 계정 담당자에게 문의하십시오.

다음 설정을 사용할 수 있습니다.

## 고객

계정에 대한 클라이언트 코드입니다.

[!UICONTROL 설정 &gt; 구현 &gt; Mbox.js 설정 편집]을 볼 때 맨 위에 있는 클라이언트가 계정의 클라이언트 코드입니다.

## 시간 초과

Target 요청 시간 제한입니다.

[!UICONTROL 설정 &gt; 구현 &gt; Mbox.js 설정 편집]을 볼 때 압축 수준 다음에 나오는 시간 제한이 Target 요청 시간 제한입니다. 기본적으로 이 값은 15초로 설정되지만 2초~5초 사이의 값으로 설정하는 것이 좋습니다.

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