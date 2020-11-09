---
keywords: variables;profiles;parameters;built in profiles;methods;url variables;geo profiles;third party profiles;mbox variables;campaign variables;customer attributes
description: 이 페이지에는 프로필 스크립트에 유용한 프로필, 변수 및 매개 변수가 나열됩니다.
title: 프로필 및 변수 용어집
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 92%

---


# 프로필 및 변수 용어집{#profile-and-variable-glossary}

이 페이지에는 프로필 스크립트에 유용한 프로필, 변수 및 매개 변수가 나열됩니다.

## 내장 프로필 {#section_2B694370003C4F8E8E29E0B2F6E52045}

| 프로필 | 참고 |
|--- |--- |
| user.activeActivities<br>user.activeCampaigns | 사용자가 현재 세션에서 캠페인/활동과 상호 작용하지 않더라도 사용자가 참여하는 모든 캠페인/활동에 대한 캠페인 ID를 반환합니다. |
| user.pcId |  |
| user.sessionId |  |
| user.categoryAffinity |  |
| user.categoryAffinities | 방문자가 채운 다수의 관심 사항을 반환합니다. |
| user.isFirstSession |  |
| user.isNewSession |  |
| user.daysSinceLastVisit |  |
| user.browser | 사용자 에이전트 |
| user.header | mbox 요청 헤더 데이터의 모든 `user.header` 프로필이 내장되어 있습니다. |
| user.header(&#39;x-forwarded-for&#39;) | 방문자가 켜져 있는 네트워크 연결의 공개 IP 주소입니다.<br>예를 들어 [whatismyip.com](https://www.whatismyip.com/)/과 같은 여러 가지 방법으로 주소를 얻을 수 있습니다. IP 주소는 10., 192.168. 또는 172.으로 시작하는 NAT 주소(내부 주소)가 아닙니다.<br>참고:user.header(&#39;x-cluster-client-ip&#39;)는 더 이상 사용되지 않습니다. |
| user.header(&#39;host&#39;) | 웹 사이트 호스트 이름 |
| user.header(&#39;cookie&#39;) | 방문자 쿠키 데이터 |
| user.header(&#39;user-agent&#39;) | 방문자 브라우저 사용자-에이전트 |
| user.header(&#39;accept-language&#39;) | 방문자 언어 |
| user.header(&#39;accept-encoding&#39;) | 방문자 문자 인코딩 |
| user.header(&#39;accept&#39;) | 방문자 언어 및 문자 인코딩 |
| user.header(&#39;connection&#39;) | 서버 연결. 예: keep-live |
| user.header(&#39;referrer&#39;) | 방문자 현재 페이지의 웹 사이트 URL. Internet Explorer에 대해 작동하지 않습니다. |
| user.getLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.setLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.get(&#39;param_name&#39;) |  |
| user.parameter | 프로필 스크립트에서 만든 지속적 프로필 속성입니다. 지리적 위치, 방문 수 등과 같은 &quot;시스템&quot; 프로필도 참조합니다. |
| profile.get(&#39;param_name&#39;) | 프로필 스크립트에서 사용할 프로필 매개 변수를 가져오는 올바른 방법은 profile.get(&#39;param_name&#39;) 메서드입니다. |
| profile.param(&#39;param_name&#39;); |  |
| profile.parameter(&#39;parameter_name&#39;); | profile.  prefix로 인해 영구적으로 지정되는 Mbox 매개 변수입니다. |
| profile.browserTime | 방문자의 로컬 브라우저 시간. 시스템 시간의 경우 프로필 스크립트에서 새로운 날짜 개체를 만듭니다. |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
| parameter= | mbox와 함께 제공되는 (일반적으로 이름/값 쌍으로) 추가 값에 대한 일반 용어입니다. `profile.parameter`나 `user.parameter`로 설정되지 않는 한, 지속적이지 않습니다. |

## URL 변수 {#section_8F25958273164EBAA6DC659302993FD3}

| `landing` | `referrer` | `page` |
|---|---|---|
| `landing.url` | `referrer.url` | `page.url` |
| `landing.domain` | `referrer.domain` | `page.domain` |
| `landing.protocol` | `referrer.protocol` | `page.protocol` |
| `landing.param` | `referrer.param` | `page.param` |
| `landing.query` | `referrer.query` | `page.query` |

## 지역 및 모바일 통신사 프로필 {#section_08441DA42E7346918FBB345818854997}

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`
* `profile.geolocation.latitude`
* `profile.geolocation.longitude`

## mbox 변수 {#section_C42F0D33BD8044BE812FA0B7905CC0ED}

| 변수 | 참고 |
|--- |--- |
| `mbox.name` |  |
| mbox.param(&#39;param_name&#39;) |  |
| 모든 요청을 통해 자동 전달된 매개 변수:<ul><li>mbox.param(&#39;browserHeight&#39;)</li><li>mbox.param(&#39;browserTimeOffset&#39;)</li><li>mbox.param(&#39;browserWidth&#39;)</li><li>mbox.param(&#39;colorDepth&#39;)</li><li>mbox.param(&#39;mboxXDomain&#39;)</li><li>mbox.param(&#39;mboxTime&#39;)</li><li>mbox.param(&#39;screenHeight&#39;)</li><li>mbox.param(&#39;screenWidth&#39;)</li></ul> |
| 주문 mbox를 통해 전달된 매개 변수:<ul><li>mbox.param(&#39;orderId&#39;)</li><li>mbox.param(&#39;orderTotal&#39;)</li><li>mbox.param(&#39;productPurchasedId&#39;)</li></ul> |
| mbox3rdPartyId | 고객 ID를 Target의 mboxPCID와 동기화하는 mbox 매개 변수입니다. 고객 ID는 회사에서 방문자를 추적하는 데 사용하는 CRM ID, 멤버십 ID 또는 유사한 ID입니다. 그런 후 이 ID를 사용하여 프로필 API 및 [고객 속성](/help/c-target/c-visitor-profile/working-with-customer-attributes.md). |
| mboxPageValue | 각 mbox 호출에서 페이지는 값을 지정받습니다. |
| mboxDebug | 디버그 정보로만 사용됩니다. mbox.js가 이 정보를 찾는 페이지 URL에 추가됩니다. |
| mboxOverride.browserIp | 다른 위치에서는 어떻게 보이는지 테스트할 수 있도록 실제 위치가 아닌 다른 지역을 설정합니다.<br>**참고:** mboxOverride 매개 변수는 프로덕션 환경이 아닌, 활동을 테스트할 때만 사용하는 것이 좋습니다. mboxOverride 매개 변수를 사용하면 [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T)을 사용할 때 불일치가 보고될 수 있습니다. 활동을 라이브 환경에 푸시하기 전에 활동이 예상대로 작동하는지 확인하려면 테스트할 때 [활동 QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)를 사용해야 합니다. |

## 고객 속성{#section_62B4821EB6564FF4A14159A837AD4EDB}을 통해 정보를 추가할 수 있습니다 

고객 속성이 `crs.get('<Datasource Name>.<Attribute name>')`.

이러한 속성이 프로필 스크립트에서 토큰으로 사용되거나 프로필 스크립트가 없어도 오퍼에서 직접 토큰으로 사용될 수도 있습니다. 토큰은 `${crs.datasourceName.attributeName}` 형식이어야 합니다. API 호출에서 공백이 제거되어야 `datasourceName` 합니다.
