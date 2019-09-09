---
description: Google Chrome 버전 76부터 사용되는 Target 및 SameSite IETF 표준에 대한 정보입니다.
keywords: google;samesite; 쿠키; Chrome 80; IETF
seo-description: Google Chrome 버전 80부터 도입되는 Adobe Target 및 SameSite IETF 표준에 대한 정보입니다.
seo-title: Adobe Target 및 Google의 Samesite 쿠키 정책
solution: Target
subtopic: 시작하기
title: Google Chrome samesite 쿠키 정책
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Google Chrome samesite 쿠키 정책

Google는 2020 년 초에 출시될 예정인 Chrome 80 부터 사용자를 위해 기본적으로 새로운 쿠키 정책을 시행하기 시작합니다. 이 문서에서는 새로운 Samesite 쿠키 정책, 이러한 정책을 지원하는 방법 [!DNL Adobe Target] 및 Google Chrome의 새 Samesite 쿠키 정책을 준수하는 데 [!DNL Target] 사용하는 방법에 대해 알아보는 데 필요한 모든 사항을 설명합니다.

Chrome 80 부터는 웹 개발자가 웹 사이트에서 사용할 수 있는 쿠키를 명시적으로 지정해야 합니다. 이는 Google 이 웹상의 개인 정보 및 보안을 개선하기 위해 계획을 수립하는 많은 공지 사항 중 첫 번째 내용입니다.

Facebook 이 개인 정보 및 보안에 대한 핫시트에 존재했다는 사실을 감안할 때 Apple와 같은 다른 주요 플레이어는 이제 개인 정보 및 보안 챔피언으로 새로운 ID를 만들 수 있는 기회를 신속하게 활용할 수 있었습니다. Apple는 ITP 2.1 및 최근 ITP 2.2를 통해 올해 초 쿠키 정책에 대한 변경 사항을 처음으로 발표함으로써 팩을 주도했습니다. ITP 2.1에서 Apple는 타사 쿠키를 완전히 차단하며, 7 일 동안만 브라우저에서 쿠키를 유지합니다. ITP 2.2 에서는 쿠키가 하루 동안만 보관됩니다. Google의 공고는 Apple 만큼 공격적이지는 않지만, 동일한 최종 목표를 향한 첫 번째 단계입니다. Apple 정책에 대한 자세한 내용은 [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)를 참조하십시오.

## 쿠키란 무엇이며 어떻게 사용됩니까?

Google의 쿠키 정책에 대한 Google의 변경 사항을 조사하기 전에 쿠키가 무엇인지, 그리고 어떻게 사용되는지 살펴보겠습니다. 간단히 말하자면 쿠키는 사용자 속성을 기억하는 데 사용되는 웹 브라우저에 저장되는 작은 텍스트 파일입니다.

쿠키는 웹을 탐색하는 동안 사용자의 경험을 향상시키므로 매우 중요합니다. 예를 들어 전자 상거래 웹 사이트에서 쇼핑을 하고 있지만 장바구니에 어떤 것을 추가해도 해당 방문에서 로그인하거나 구매하지 않으면 쿠키는 항목을 기억하고 다음 방문 시 장바구니에 보관합니다. 또는 자주 사용하는 소셜 미디어 웹 사이트를 방문할 때마다 사용자 이름과 암호를 다시 입력해야 하는 경우 상상해 보십시오. 쿠키도 해당 문제를 해결합니다. 이러한 종류의 쿠키는 방문한 웹사이트에 의해 만들어지고 사용되므로 퍼스트 파티 쿠키라고 합니다.

타사 쿠키도 있습니다. 이를 더 잘 이해하려면 다음 예제를 고려하십시오.

" 친구 "라고 하는 가상의 소셜 미디어 회사는 친구 사용자가 친구 피드에서 사이트 컨텐츠를 공유할 수 있도록 다른 사이트가 구현하는 공유 단추를 제공합니다. 이제 사용자가 공유 단추를 사용하고 있는 뉴스 웹 사이트에서 뉴스 기사를 읽고 클릭하여 친구 계정에 자동으로 게시합니다.

이를 위해 브라우저는 뉴스 문서가 로드될 때 친구 `platform.friends.com` 공유 단추를 가져옵니다. 이 프로세스 내에서 브라우저는 사용자의 로그인한 자격 증명을 포함하는 친구 쿠키를 친구 서버에 요청합니다. 이렇게 하면 사용자가 로그인하지 않아도 친구가 사용자를 대신하여 피드에 뉴스 기사를 게시할 수 있습니다.

타사 쿠키를 사용하여 가능합니다. 이 경우 타사 쿠키가 브라우저에 저장되므로 사용자를 `platform.friends.com``platform.friends.com` 대신하여 친구 앱에서 게시물을 만들 수 있습니다.

서드 파티 쿠키 없이 이러한 사용 사례를 만드는 방법을 잠시 생각해 보는 경우 사용자는 수동 단계를 많이 수행해야 합니다. 첫째, 사용자가 뉴스 문서에 링크를 복사해야 합니다. 둘째, 친구 앱에 별도로 로그인해야 합니다. 그런 다음 사용자가 게시물 만들기 단추를 클릭합니다. 그런 다음 사용자가 텍스트 필드에 링크를 복사하여 붙여넣은 다음 마지막으로 게시를 클릭합니다. 사용자가 볼 수 있듯이 타사 쿠키는 수동으로 단계를 줄일 수 있으므로 사용자 경험을 크게 향상시킬 수 있습니다.

일반적으로 서드 파티 쿠키를 사용하면 사용자가 웹 사이트를 명시적으로 방문하지 않고도 사용자의 브라우저에 데이터를 저장할 수 있습니다.

## 보안 문제

쿠키는 사용자 경험과 파워 광고를 향상시키지만 크로스 사이트 요청 위조 (CSRF) 공격과 같은 보안 취약점을 도입할 수 있습니다. 예를 들어 사용자가 은행 사이트에 로그인하여 신용 카드로 로그인하여 로그아웃한 다음 동일한 세션에서 악성 사이트로 이동하면 CSRF 공격이 발생할 수 있습니다. 악성 사이트에는 페이지가 로드될 때 실행되는 은행 사이트에 요청을 하는 코드가 포함될 수 있습니다. 사용자가 여전히 은행 사이트에 인증되기 때문에 세션 쿠키를 사용하여 CSRF 공격을 실행하여 사용자의 은행 계정에서 자금 이체 이벤트를 시작할 수 있습니다. 이것은 사이트를 방문할 때마다 모든 쿠키가 HTTP 요청에 연결되기 때문입니다. 이러한 보안 문제로 Google는 이제 이러한 문제를 완화하려고 시도하고 있습니다.

## Target는 쿠키를 어떻게 사용합니까?

이 모두가 쿠키를 [!DNL Target] 사용하는 방법을 살펴보겠습니다. 먼저 사용하려면 [!DNL Target] 사이트에 [!DNL Target] JavaScript 라이브러리를 설치해야 합니다. 이렇게 하면 사이트를 방문하는 사용자의 브라우저에 퍼스트 파티 쿠키를 배치할 수 있습니다. 사용자가 웹 사이트와 상호 작용하면 사용자의 행동 데이터와 관심 데이터를 JavaScript 라이브러리를 [!DNL Target] 통해 전달할 수 있습니다. [!DNL Target] JavaScript 라이브러리는 퍼스트 파티 쿠키를 사용하여 사용자의 행동 및 관심 데이터에 매핑할 사용자에 대한 식별 정보를 추출합니다. 그런 다음 이 데이터를 [!DNL Target] 사용하여 개인화 활동을 강화할 수 있습니다.

Target도 타사 쿠키를 사용합니다. 서로 다른 도메인에 있는 여러 개의 웹 사이트를 소유하고 있으며 해당 웹 사이트에서 사용자 여정을 추적하려는 경우 도메인 간 추적을 활용하여 타사 쿠키를 사용할 수 있습니다. [!DNL Target] JavaScript 라이브러리에서 도메인 간 추적을 활성화하면 계정에서 타사 쿠키를 사용하게 됩니다. 한 도메인의 사용자가 다른 도메인으로 이동할 때 브라우저가의 백엔드 서버와 [!DNL Target]통신하며, 이 프로세스에서는 타사 쿠키가 만들어져 사용자의 브라우저에 배치됩니다. 사용자의 브라우저에 있는 타사 쿠키를 통해 단일 [!DNL Target] 사용자에 대해 다른 도메인에서 일관된 경험을 제공할 수 있습니다.

## Google의 새로운 쿠키 레시피

사용자가 안전하게 사이트 간에 쿠키를 전송할 때 안전하게 보호해줄 수 있도록 Google 에서는 Samesite 라는 IETF 표준에 대한 지원을 추가하여 웹 개발자가 Set-Cookie 헤더에서 Samesite 속성 구성 요소를 사용하여 쿠키를 관리해야 합니다.

SameSite 속성으로 전달할 수 있는 Strict, Lax 또는 None값이 있습니다.

| 값 | 설명 |
| --- | --- |
| Strict | 이 설정을 사용하는 쿠키는 처음에 설정된 도메인을 방문할 때만 액세스할 수 있습니다. 즉, Strict는 쿠키를 사이트 간에 사용할 수 없게 차단합니다. 이 옵션은 은행과 같이 보안이 요구되는 애플리케이션에 가장 적합합니다. |
| Lax | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. 따라서 쿠키가 제 3 자에 의해 사용될 수 있는 경우 이 옵션을 사용하지만, 사용자가 CSRF 공격으로 피해를 당하지 않도록 보호하는 보안 혜택을 추가합니다. |
| 없음 | Cookies with this setting will work the same way as cookies work today. |

위의 사항을 염두에 두고 Chrome 80는 사용자에게 두 가지 독립적인 설정을 제공합니다. " 기본 쿠키별 Samesite "및" Samesite 없는 쿠키는 안전해야 합니다. " 이러한 설정은 Chrome 80에서 기본적으로 활성화됩니다.

![Samesite 대화 상자](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **기본적으로 쿠키별**: 이 설정을 설정하면, Samesite 속성을 지정하지 않은 모든 쿠키가 자동으로 사용하도록 `SameSite = Lax`강제됩니다.
* **Samesite가 없는 쿠키는 안전해야 합니다. 설정된 경우, Samesite 속성 없이 또는 보안을 유지해야** 하는 쿠키가 필요합니다. `SameSite = None` 이 컨텍스트에서 보호란 모든 브라우저 요청이 HTTPS 프로토콜을 따라야 한다는 것을 의미합니다. 이 요구 사항을 준수하지 않는 쿠키는 거부됩니다. 모든 웹 사이트는 이 요구 사항을 충족하기 위해 HTTPS를 사용해야 합니다.

## Google의 보안 모범 사례를 따르는 Target

Adobe는 항상 보안 및 개인 정보를 위한 업계 최신 모범 사례를 지원하고 있습니다. Google에 의해 도입된 새로운 보안 및 개인 정보 설정을 [!DNL Target] 지원하는 기쁜 마음으로 알려드립니다.

" 기본 쿠키별 Samesite "설정의 [!DNL Target] 경우, 어떠한 영향력과 개입도 없이 개인화를 계속 제공할 것입니다. [!DNL Target] 퍼스트 파티 쿠키를 사용하며 Google Chrome에 의해 플래그가 `SameSite = Lax` 적용됨에 따라 계속 제대로 작동합니다.

" Samesite 없는 쿠키 필요 없음 "옵션의 경우, 에서 [!DNL Target]도메인 간 추적 기능에 대해 옵트인할 경우의 [!DNL Target] 퍼스트 파티 쿠키가 계속 작동합니다.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. 즉, 사이트에서 HTTPS 프로토콜을 사용하도록 해야 합니다. Client-side Libraries in [!DNL Target] will automatically use the HTTPS protocol and attach the `SameSite = None` and secure flags in third-party cookies in [!DNL Target] to third-party cookies to deliver.

## 필요한 작업

Google Chrome 80 + 사용자를 위해 [!DNL Target] 계속 작업하기 위해 수행해야 하는 작업을 이해하려면 아래 표를 참조하십시오. 이 중 다음 열이 표시됩니다.

* **대상 JavaScript 라이브러리**: mbox. js를 사용하는 경우 at. js 1.*x* 또는 at.js 2 *x* 를 참조하십시오.
* **기본 쿠키 = enabled**: 사용자에게 "기본 쿠키별 Samesite" 가 활성화되어 있는 경우, 어떠한 영향을 미치는지와 작업을 계속 진행하기 위해 필요한 [!DNL Target] 모든 것이 있습니다.
* **Samesite 없는 쿠키는 보안 = enabled**&#x200B;여야 합니다. 사용자에게 "Samesite가 없는 쿠키" 가 활성화되어 있는 경우, 어떠한 영향을 미치는지, 그리고 작업을 [!DNL Target] 계속 진행하기 위해 필요한 모든 것이 있다면 이를 이용하십시오.

| Javascript 라이브러리 대상 | SameSite를 기본 쿠키로 지정 = 활성화됨 | SameSite가 없는 쿠키를 보호해야 함 = 활성화됨 |
| --- | --- | --- |
| mbox. js (퍼스트 파티 쿠키에만 해당). | 아무런 영향 없이 | 도메인 간 추적을 사용하지 않는 경우에는 영향을 주지 않습니다. |
| 도메인 간 추적을 활성화한 mbox. js. | 아무런 영향 없이 | 사이트에 대한 HTTPS 프로토콜을 활성화해야 합니다.<br>[!DNL Target] 타사 쿠키를 사용하여 사용자와 Google를 추적하면 타사 쿠키가 포함되고 플래그가 `SameSite = None` 지정됩니다. 보안 플래그를 사용하려면 사이트가 HTTPS 프로토콜을 사용해야 합니다. |
| at.js 1.*x* 사용할 수 있습니다. | 아무런 영향 없이 | 도메인 간 추적을 사용하지 않는 경우에는 영향을 주지 않습니다. |
| at.js 1.*x* 도메인 간 추적을 활성화한 경우 | 아무런 영향 없이 | 사이트에 대한 HTTPS 프로토콜을 활성화해야 합니다.<br>[!DNL Target] 타사 쿠키를 사용하여 사용자와 Google를 추적하면 타사 쿠키가 포함되고 플래그가 `SameSite = None` 지정됩니다. 보안 플래그를 사용하려면 사이트가 HTTPS 프로토콜을 사용해야 합니다. |
| at.js 2.*x* | 아무런 영향 없이 | 아무런 영향 없이 |

## Target의 기능

그렇다면 새로운 Google Chrome 80 + Samesite 쿠키 정책을 준수하기 위해 플랫폼에서 수행해야 할 일은 무엇입니까?

| Javascript 라이브러리 대상 | SameSite를 기본 쿠키로 지정 = 활성화됨 | SameSite가 없는 쿠키를 보호해야 함 = 활성화됨 |
| --- | --- | --- |
| mbox. js (퍼스트 파티 쿠키에만 해당). | 아무런 영향 없이 | 도메인 간 추적을 사용하지 않는 경우에는 영향을 주지 않습니다. |
| 도메인 간 추적을 활성화한 mbox. js. | 아무런 영향 없이 | [!DNL Target] 서버가 `SameSite = None` 호출될 때 [!DNL Target] 타사 쿠키에 플래그를 추가하고 보호합니다. |
| at.js 1.*x* 사용할 수 있습니다. | 아무런 영향 없이 | 도메인 간 추적을 사용하지 않는 경우에는 영향을 주지 않습니다. |
| at.js 1.*x* 도메인 간 추적을 활성화한 경우 | 아무런 영향 없이 | at.js 1.*x* 도메인 간 추적을 활성화한 경우 |
| at.js 2.*x* | 아무런 영향 없이 | 아무런 영향 없이 |

## HTTPS 프로토콜을 사용하기 위해 이동하지 않으면 어떤 영향이 있습니까?

mbox. js 또는 at. js 1 [!DNL Target] 를 통해 크로스 도메인 추적 기능을 사용하는 경우에만 영향을 받습니다.*x*&#x200B;에는 사용할 수 없습니다. Google에 의한 요구 사항인 HTTPS로 이동하지 않으면, Adobe가 사용하는 타사 쿠키가 Google에 의해 삭제될 것이므로 도메인 전체에서 고유 방문자가 스파이크에 표시됩니다. 또한 타사 쿠키가 삭제되므로 사용자가 [!DNL Target] 한 도메인에서 다른 도메인으로 이동할 때 해당 사용자에 대해 일관되고 개인화된 경험을 제공할 수 없습니다. 타사 쿠키는 주로 소유한 도메인에서 탐색하는 단일 사용자를 식별하는 데 사용됩니다.

## 결론

업계에서 소비자를 위한 보다 안전한 웹을 구축하기 위해 노력하고 [!DNL Adobe] 있으므로, 고객은 최종 사용자를 위한 보안 및 개인 정보를 보장하는 방식으로 개인화된 경험을 제공할 수 있도록 최선을 다하고 있습니다. 앞에서 언급한 모범 사례를 따르고 Google Chrome의 새로운 [!DNL Target] Samesite 쿠키 정책을 준수하기만 하면 됩니다.
