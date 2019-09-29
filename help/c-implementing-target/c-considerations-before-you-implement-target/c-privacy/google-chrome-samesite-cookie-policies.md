---
description: Google Chrome 버전 76부터 사용되는 Target 및 SameSite IETF 표준에 대한 정보입니다.
keywords: google;samesite쿠키;크롬 80;ietf
seo-description: Google Chrome 버전 80부터 도입되는 Adobe Target 및 SameSite IETF 표준에 대한 정보입니다.
seo-title: Adobe Target 및 Google의 SameSite 쿠키 정책
solution: Target
subtopic: 시작하기
title: Google Chrome samesite 쿠키 정책
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Google Chrome samesite 쿠키 정책

Google은 기본적으로 2020년 초에 릴리스될 Chrome 80부터 시작하는 사용자에 대해 새로운 쿠키 정책을 부과하기 시작합니다. 이 문서에서는 새로운 SameSite 쿠키 정책에 대해 알아야 할 모든 사항, 이러한 정책을 [!DNL Adobe Target] 지원하는 방법, Google Chrome의 새로운 SameSite 쿠키 정책을 준수하는 [!DNL Target] 데 사용할 수 있는 방법에 대해 설명합니다.

Chrome 80부터 웹 개발자는 웹 사이트에서 사용할 수 있는 쿠키를 명시적으로 지정해야 합니다. 이것은 구글이 웹상의 프라이버시와 보안을 개선하기 위해 계획하고 있는 많은 발표 중 첫 번째 입니다.

페이스북이 사생활과 보안과 관련하여 인기 있는 위치에 있다는 사실을 고려했을 때, 애플과 현재 구글과 같은 다른 주요 선수들은 프라이버시와 보안 챔피언으로서 새로운 신분을 만들 기회를 재빨리 이용해 왔다. 애플은 올해 초 ITP 2.1과 최근 ITP 2.2를 통해 쿠키 정책 변경을 발표함으로써 이 팩을 주도했다.ITP 2.1에서 Apple은 서드 파티 쿠키를 완전히 차단하고 브라우저에서 만든 쿠키를 7일 동안만 보관합니다. ITP 2.2에서는 쿠키가 하루 동안만 보관됩니다. 구글의 이번 발표는 애플처럼 공격적이지는 않지만, 같은 목적을 향한 첫 번째 단계이다. Apple의 정책에 대한 자세한 내용은 Apple Intelligent Tracking [Prevention(ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)를 참조하십시오.

## 쿠키란 무엇이며 어떻게 사용됩니까?

쿠키 정책에 대한 Google의 변경 사항을 살펴보기 전에 쿠키가 무엇이고 쿠키가 어떻게 사용되는지 살펴보겠습니다. 간단히 말해 쿠키는 사용자 속성을 기억하는 데 사용되는 작은 텍스트 파일입니다.

쿠키는 웹을 탐색할 때 사용자의 경험을 향상시켜주기 때문에 중요합니다. 예를 들어 eCommerce 웹 사이트에서 장바구니에 항목을 추가하고 이 방문에서 로그인하거나 구매하지 않는 경우 쿠키는 항목을 기억하고 다음 방문 동안 장바구니에 보관합니다. 또는 자주 사용하는 소셜 미디어 웹 사이트를 방문할 때마다 사용자 이름과 암호를 다시 입력해야 한다고 가정합니다. 쿠키도 해당 문제를 해결합니다. 쿠키는 사이트에서 사용자를 식별하는 데 도움이 되는 정보를 저장하므로 이러한 종류의 쿠키는 귀하가 방문한 웹 사이트에서 만들고 사용하기 때문에 퍼스트 파티 쿠키라고 합니다.

타사 쿠키도 있습니다. 이러한 사례를 더 잘 이해하기 위해 다음 예를 생각해 보겠습니다.

"친구"라고 하는 가상 소셜 미디어 회사는 다른 사이트에서 친구 사용자가 사이트 컨텐츠를 친구 피드에서 공유할 수 있도록 구현하는 공유 단추를 제공한다고 가정해 봅시다. 이제 사용자는 공유 버튼을 사용하는 뉴스 웹 사이트에서 뉴스 기사를 읽고 이를 클릭하여 자신의 친구 계정에 자동으로 게시합니다.

For this to happen, the browser fetches the Friends Share button from  when the news article is loaded. `platform.friends.com` Within this process, the browser attaches Friends cookies, which contain the logged-in credentials of the user, to the request to Friends servers. This allows Friends to post the news article in its feed on the user’s behalf without requiring the user to log in.

This is all possible by using third-party cookies. In this case, the third-party cookie is saved on the browser for , so that  can make the post in the Friends app on the user’s behalf.`platform.friends.com``platform.friends.com`

If you imagine for a moment how to achieve this use case without third-party cookies, the user would have to follow a lot of manual steps. First, the user would have to copy the link to the news article. Second, the user would have to log into the Friends app separately. Then, the user would click on the Create Post button. Then the user would copy and paste the link in the text field, and finally click Post. As you can see, third-party cookies immensely help the user experience as manual steps can be drastically reduced.

More generally, third-party cookies make it possible for data to be stored on a user’s browser without requiring that user to explicitly visit a website.

## Security concerns

Although cookies enhance user experiences and power advertising, they can also introduce security vulnerabilities like Cross-Site Request Forgery (CSRF) attacks. 예를 들어 사용자가 은행 사이트에 로그인하여 신용 카드 결제를 위해 로그인하고 로그아웃하지 않고 사이트를 떠난 다음 동일한 세션에서 악성 사이트로 이동하면 CSRF 공격이 발생할 수 있습니다. The malicious site could include code that makes a request to the banking site that executes when the page loads. 사용자가 여전히 은행 사이트에 대해 인증되므로 세션 쿠키를 사용하여 CSRF 공격을 실행하여 사용자의 은행 계좌에서 자금 전송 이벤트를 시작할 수 있습니다. 이는 사이트를 방문할 때마다 모든 쿠키가 HTTP 요청에 첨부되기 때문입니다. 그리고 이러한 보안 문제 때문에 Google은 현재 이러한 문제를 완화하려고 노력하고 있습니다.

## Target은 쿠키를 어떻게 사용합니까?

이렇게 해서, 어떻게 쿠키를 [!DNL Target] 사용하는지 봅시다. 처음에 사용하려면 사이트에 JavaScript [!DNL Target] [!DNL Target] 라이브러리를 설치해야 합니다. 이렇게 하면 사이트를 방문하는 사용자의 브라우저에 퍼스트 파티 쿠키를 배치할 수 있습니다. 사용자가 웹 사이트와 상호 작용할 때 사용자의 행동 및 관심 데이터를 JavaScript 라이브러리를 [!DNL Target] 통해 전달할 수 있습니다. JavaScript [!DNL Target] 라이브러리는 자사 쿠키를 사용하여 사용자의 행동 및 관심 데이터에 매핑하기 위해 사용자에 대한 식별 정보를 추출합니다. 그러면 이 데이터를 사용하여 개인화 활동을 강화할 [!DNL Target] 수 있습니다.

Target은 (때때로) 타사 쿠키를 사용합니다. 다른 도메인에 존재하는 여러 개의 웹 사이트를 소유하고 있고 이러한 웹 사이트에서 사용자 경로를 추적하려는 경우 도메인 간 추적을 활용하여 타사 쿠키를 사용할 수 있습니다. JavaScript 라이브러리에서 도메인 간 추적을 [!DNL Target] 활성화하면 계정이 타사 쿠키 사용을 시작합니다. 사용자가 한 도메인에서 다른 도메인으로 이동할 때 브라우저는 백엔드 서버의 [!DNL Target]백엔드 서버와 통신하며 이 과정에서 타사 쿠키가 만들어져 사용자의 브라우저에 배치됩니다. 사용자의 브라우저에 상주하는 타사 쿠키를 통해 단일 사용자에 대해 여러 도메인에 일관된 경험을 제공할 [!DNL Target] 수 있습니다.

## Google의 새로운 쿠키 레서피

사용자가 보호될 수 있도록 쿠키를 사이트 간에 전송할 때 보안 기능을 제공하기 위해 Google은 SameSite라는 IETF 표준 지원을 추가할 계획입니다. 이 경우 웹 개발자가 Set-Cookie 헤더에서 SameSite 속성 구성 요소를 사용하여 쿠키를 관리해야 합니다.

SameSite 속성으로 전달할 수 있는 Strict, Lax 또는 None값이 있습니다.

| 값 | 설명 |
| --- | --- |
| Strict | 이 설정을 사용하는 쿠키는 처음에 설정된 도메인을 방문할 때만 액세스할 수 있습니다. 즉, Strict는 쿠키를 사이트 간에 사용할 수 없게 차단합니다. This option would be best for applications that require high security, such as banks. |
| Lax | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. 따라서 이 옵션은 타사에서 쿠키를 사용할 수 있지만 CSRF 공격의 피해를 당하지 않도록 하는 보안 혜택이 추가된 경우에 사용됩니다. |
| 없음 | Cookies with this setting will work the same way as cookies work today. |

상기에 유의하십시오. Chrome 80은 사용자에 대해 두 가지 독립 설정을 제공합니다."SameSite by default cookies" 및 "SameSite가 없는 쿠키는 안전해야 합니다." 이러한 설정은 Chrome 80에서 기본적으로 활성화됩니다.

![SameSite 대화 상자](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite by default cookies**:설정되면 SameSite 속성을 지정하지 않은 모든 쿠키는 자동으로 `SameSite = Lax`사용됩니다.
* **SameSite가 없는 쿠키는 보안되어야**&#x200B;합니다.설정되면 SameSite 특성이 없거나 보안이 `SameSite = None` 필요한 쿠키입니다. 이 컨텍스트에서 보호란 모든 브라우저 요청이 HTTPS 프로토콜을 따라야 한다는 것을 의미합니다. 이 요구 사항을 준수하지 않는 쿠키는 거부됩니다. 모든 웹 사이트는 이러한 요구 사항을 충족하기 위해 HTTPS를 사용해야 합니다.

## Google의 보안 모범 사례를 따르는 Target

Adobe는 항상 보안 및 개인 정보에 대한 업계 최신 모범 사례를 지원하고 싶습니다. Adobe는 Google에서 도입한 새로운 보안 및 개인 정보 설정을 [!DNL Target] 지원한다는 소식을 알려드립니다.

"SameSite by default cookies" 설정의 경우, [!DNL Target] 영향을 주지 않고 사용자의 개입 없이 개인화를 계속 제공할 것입니다. [!DNL Target] 퍼스트 파티 쿠키를 사용하고 플래그를 Google Chrome에 `SameSite = Lax` 적용할 때 계속 제대로 작동합니다.

"SameSite가 없는 쿠키는 안전해야 함" 옵션의 경우 에서 도메인 간 추적 기능을 옵트인하지 않으면 [!DNL Target]퍼스트 파티 쿠키는 [!DNL Target] 계속 작동합니다.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. 즉, 사이트에서 HTTPS 프로토콜을 사용해야 합니다. 의 클라이언트측 라이브러리는 자동으로 HTTPS 프로토콜을 사용하고 모든 활동이 계속 전달되도록 하기 [!DNL Target] 위해 타사 쿠키에 `SameSite = None` [!DNL Target] 및 보안 플래그를 연결합니다.

## 필요한 작업

Google Chrome 80+ 사용자를 위해 [!DNL Target] 계속 작업하기 위해 필요한 작업을 이해하려면 아래 표를 참조하십시오. 아래 열에는 다음 열이 표시됩니다.

* **타겟 JavaScript 라이브러리**:mbox.js를 사용하는 경우 at.js 1.*x* 또는 at.js 2 *x on your sites.*
* **SameSite by default cookies = Enabled**:사용자가 "기본 쿠키로 SameSite"를 활성화한 경우 쿠키가 사용자에게 어떤 영향을 미치며 작업을 계속 진행하기 위해 필요한 모든 것이 [!DNL Target] 있습니다.
* **SameSite가 없는 쿠키는 안전해야 함 = 활성화됨**:사용자가 "동일한 사이트가 없는 쿠키는 반드시 안전해야 함"을 사용하는 경우 쿠키가 어떤 영향을 미치며 [!DNL Target] 계속 작업하는 데 필요한 모든 것이 있어야 합니다.

| Target JavaScript Library | SameSite를 기본 쿠키로 지정 = 활성화됨 | SameSite가 없는 쿠키를 보호해야 함 = 활성화됨 |
| --- | --- | --- |
| mbox.js with first-party cookie only. | No impact. | 크로스 도메인 추적을 사용하지 않는 경우 영향을 주지 않습니다. |
| mbox.js with cross-domain tracking enabled. | No impact. | 사이트에 대해 HTTPS 프로토콜을 활성화해야 합니다.<br>[!DNL Target] uses a third-party cookie to track users and Google requires third-party cookies to have  and Secure flag. `SameSite = None` The Secure flag requires your sites must use the HTTPS protocol. |
| at.js 1.*x* with first-party cookie. | No impact. | No impact if you are not using cross-domain tracking. |
| at.js 1.*x* with cross-domain tracking enabled. | 효과 없음 | You must enable the HTTPS protocol for your site.<br>[!DNL Target] 타사 쿠키를 사용하여 사용자를 추적하고 Google을 사용하려면 타사 쿠키가 있어야 하며 `SameSite = None` 보안 플래그가 있어야 합니다. 보안 플래그를 사용하려면 사이트에서 HTTPS 프로토콜을 사용해야 합니다. |
| at.js 2.*x* | 효과 없음 | 효과 없음 |

## What does Target need to do?

그렇다면 새로운 Google Chrome 80+ SameSite 쿠키 정책을 준수하는 데 Adobe 플랫폼에서 어떻게 해야 합니까?

| 타겟 JavaScript 라이브러리 | SameSite를 기본 쿠키로 지정 = 활성화됨 | SameSite가 없는 쿠키를 보호해야 함 = 활성화됨 |
| --- | --- | --- |
| 퍼스트 파티 쿠키만 있는 mbox.js | 효과 없음 | No impact if you are not using cross-domain tracking. |
| 크로스 도메인 추적이 활성화된 mbox.js를 추가했습니다. | 효과 없음 | [!DNL Target] 서버가 호출될 `SameSite = None` 때 타사 쿠키에 [!DNL Target] 및 보안 플래그를 추가합니다. |
| at.js 1.*x* (퍼스트 파티 쿠키 포함) | 효과 없음 | 크로스 도메인 추적을 사용하지 않는 경우 영향을 주지 않습니다. |
| at.js 1.*x* 크로스 도메인 추적이 활성화되면 | 효과 없음 | at.js 1.*x* 크로스 도메인 추적이 활성화되면 |
| at.js 2.*x* | 효과 없음 | 효과 없음 |

## HTTPS 프로토콜을 사용하지 않으면 어떤 영향을 미칩니까?

영향을 줄 유일한 사용 사례는 mbox.js 또는 at.js 1에서 도메인 간 추적 기능을 사용하는 [!DNL Target] 경우입니다.*x*&#x200B;에는 사용할 수 없습니다. Google의 요구 사항인 HTTPS로 전환하지 않으면 Adobe가 사용하는 타사 쿠키가 Google에 의해 삭제되기 때문에 도메인에서 고유 방문자 수가 급증합니다. 또한 타사 쿠키가 삭제되기 때문에 사용자가 한 도메인에서 다른 도메인으로 이동할 때 해당 사용자에 대해 일관되고 개인화된 경험을 제공할 [!DNL Target] 수 없습니다. 타사 쿠키는 주로 사용자가 소유한 도메인 간을 탐색하는 단일 사용자를 식별하는 데 사용됩니다.

## 결론

업계에서 소비자의 보안 웹 제작을 위해 진일보하고 [!DNL Adobe] 있으므로, 최종 사용자의 보안 및 개인 정보 보호를 보장하는 방식으로 고객이 개인화된 경험을 전달할 수 있도록 최선을 다하고 있습니다. 앞서 언급한 모범 사례를 따르고 Google Chrome의 새로운 SameSite 쿠키 정책을 [!DNL Target] 준수하기 위해 활용하기만 하면 됩니다.
