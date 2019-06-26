---
description: Google Chrome 버전 76 부터 사용되는 Target 및 Samesite IETF 표준에 대한 정보입니다.
keywords: Google; Samesite
seo-description: Google Chrome 버전 76에 도입된 Adobe Target 및 Samesite IETF 표준에 대한 정보입니다.
seo-title: Adobe Target 및 Samesite 쿠키 정책
solution: Target
subtopic: 시작하기
title: Google Chrome samesite 쿠키 정책
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Google Chrome samesite 쿠키 정책

Google는 최근 Chrome 76 (2019 년 7 월 30 일 출시 예정) 부터 시작하여 웹 사이트에서 사용할 수 있는 쿠키와 사용자 추적 쿠키를 명시적으로 지정해야 한다고 발표했습니다.

## Samesite 개요

Google는 Google Chrome 76 (이상) 에서 &quot;Samesite&quot; 라는 IETF 표준에 대한 지원을 받을 수 있도록 여러 사이트에서 쿠키를 전송할 수 있을 때 안전하게 보호할 수 있도록 보호했습니다. SameSite requires web developers to manage cookies with the SameSite attribute component in the `Set-Cookie` header.

samesite 특성으로 전달할 수 있는 세 가지 다른 값은 다음과 같습니다. strict, lax 또는 none.

| 값 | 설명 |
| --- | --- |
| 엄격한 | 이 설정이 있는 쿠키는 처음에 설정된 도메인을 방문할 때만 액세스할 수 있습니다. 즉, strict는 쿠키를 사이트에서 사용하지 못하게 차단합니다. 이 옵션은 은행과 같이 보안이 요구되는 애플리케이션에 가장 적합합니다. |
| LAX | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, such as `HTTP GET`. Therefore, this option should be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery) (Cross-Site Request Forgery) attacks. |
| 없음 | 이 설정이 포함된 쿠키는 현재 쿠키와 동일한 방식으로 작동합니다. |

위의 사항을 염두에 두고 Chrome 76 (이상) 는 두 가지 설정을 도입했습니다. &quot; 기본 쿠키별 Samesite &quot;및&quot; Samesite 없는 쿠키는 안전해야 합니다. &quot; 사용자는 설정 또는 두 설정 모두 활성화할 수 있습니다.

| 설정 | 설명 |
| --- | --- |
| 기본 쿠키별 Samesite | When set, all cookies that don&#39;t specify the SameSite attribute are automatically forced with `SameSite = Lax`. |
| Samesite 없이 쿠키를 보호해야 하는 경우 | When set, cookies without the SameSite attribute or with `SameSite = None`, must be Secure. 이 컨텍스트에서 보안은 모든 브라우저 요청이 HTTPS 프로토콜을 따라야 한다는 것을 의미합니다. 이 요구 사항을 준수하지 않는 쿠키는 거부됩니다. |

![Samesite 설정 페이지](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

## Target - Google의 보안 모범 사례

Adobe는 Target를 통해 업계 선도적인 보안 모범 사례를 항상 지원하므로 Target 이 Google Chrome 76에 도입된 새로운 보안 설정을 지원한다는 것을 기쁜 마음으로 알려드립니다.

방문자가 &quot;기본 쿠키 설정으로 Samesite&quot; 를 켜면 Target는 어떠한 영향도 주지 않고 어떠한 영향도 받지 않고 개인화를 계속 전달합니다. Target uses first-party cookies and will continue to function properly as the flag `SameSite = Lax` is applied by Google Chrome.

방문자가 &quot;Samesite 없는 쿠키 필요 없음&quot; 를 활성화하면 Target의 도메인 간 추적 기능에 대해 옵트인하지 않는 경우 Target의 퍼스트 파티 쿠키가 계속 작동합니다. However, when you opt-in to using cross-domain tracking to leverage Target across multiple domains, Google Chrome 76 (and later) requires `SameSite = None` and `Secure` flags to be used for third-party cookies. 즉, 사이트에서 HTTPS 프로토콜을 사용하도록 해야 합니다. Target&#39;s client-side libraries automatically use the HTTPS protocol and, in addition to that, attach the `SameSite = None` and `Secure` flags to Target’s third-party cookie to ensure all activities continue to deliver.

## 어떻게 해야 합니까?

Google Chrome 76 이상의 사용자에 대해 Target 이 계속 작동하도록 하려면 다음 표를 검토하십시오.

이 표에는 다음 열이 포함되어 있습니다.

* **대상 클라이언트측 라이브러리**: mbox. js를 사용 중인지 여부, at. js 1.*x*또는 at. js 2.*사이트의 X와* Google Chrome 설정이 사용자에게 미치는 영향
* **기본 쿠키 = enabled**: 방문자에게 Chrome 76 이상에서 &quot;기본적으로 쿠키 사용&quot; 이 활성화되어 있는 경우, 이것이 사용자에게 어떤 영향을 미치는지와 Target 이 계속 작동하도록 하는 데 필요한 모든 것이 있습니다.
* **Samesite 없는 쿠키는 보안 = enabled** 여야 합니다. Chrome 76 +에서 &quot;Samesite 없는 쿠키 필요 없음&quot; 이 활성화되어 있는 방문자의 경우, 어떤 결과가 사용자에게 영향을 미칩니까, 그리고 Target 이 계속 작동하도록 하는 데 필요한 모든 것이 있습니다.
* **Adobe Target의 교차 도메인 추적 = enabled**: 방문자에게 &quot;기본 쿠키로 동일한 사이트&quot; 가 활성화되어 있고 Chrome 76 +에서 &quot;Samesite 없는 쿠키&quot; 가 활성화되어 있고 도메인 간 추적을 위해 Target 이 사용 중인 경우, 타깃팅 작업을 계속 진행하기 위해 Target에 어떤 영향을 미칩니까?

| 클라이언트측 라이브러리 타깃팅 | Samesite by default cookies = enabled | Samesite 없는 쿠키는 보안 = enabled 여야 함 | Adobe Target의 교차 도메인 추적 = enabled |
| --- | --- | --- | --- |
| mbox.js | mbox. js는 퍼스트 파티 쿠키를 사용하므로 영향을 주지 않습니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | 고객은 사이트에 HTTPS 프로토콜을 활성화해야 합니다.<br>Target는 타사 쿠키를 사용하여 사용자와 Google를 추적하고, 사이트에서 HTTPS 프로토콜을 `SameSite = None` 사용하려면 타사 쿠키가 필요합니다. |
| at.js 1.*x*에는 사용할 수 없습니다 | at. js 1 이기 때문에 영향을 주지 않습니다.*X는* 퍼스트 파티 쿠키를 사용합니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | 고객은 사이트에 HTTPS 프로토콜을 활성화해야 합니다.<br>Target는 타사 쿠키를 사용하여 사용자와 Google를 추적하고 타사 쿠키가 있어야 사이트에서 `SameSite = None` HTTPS 프로토콜을 사용합니다. |
| at.js 2.*x*에는 사용할 수 없습니다 | at. js 2 이기 때문에 영향을 주지 않습니다.*X는* 퍼스트 파티 쿠키를 사용합니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | 크로스 도메인 추적은 at. js 2에서 지원되지 않습니다.*X* 때문에 고객에게 영향을 주지 않습니다. |

## Adobe가 해야 하는 작업

| 클라이언트측 라이브러리 타깃팅 | Samesite by default cookies = enabled | Samesite 없는 쿠키는 보안 = enabled 여야 함 | Adobe Target의 교차 도메인 추적 = enabled |
| --- | --- | --- | --- |
| mbox.js | mbox. js는 퍼스트 파티 쿠키를 사용하므로 영향을 주지 않습니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 1.*x*에는 사용할 수 없습니다 | at. js 1 이기 때문에 영향을 주지 않습니다.*X는* 퍼스트 파티 쿠키를 사용합니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 2.*x*에는 사용할 수 없습니다 | at. js 2 이기 때문에 영향을 주지 않습니다.*X는* 퍼스트 파티 쿠키를 사용합니다. | 고객이 도메인 간 추적을 사용하지 않으므로 영향을 주지 않습니다. | 크로스 도메인 추적은 at. js 2에서 지원되지 않습니다.*x*에는 사용할 수 없습니다 |

## 결론

소비자가 소비자를 위해 보다 안전한 웹을 만들기 위해 노력함에 따라 Target는 방문자의 개인 정보 보호 기대치를 충족시키는 동시에 개인화된 경험을 제공하기 위해 절대적으로 노력하고 있습니다.
