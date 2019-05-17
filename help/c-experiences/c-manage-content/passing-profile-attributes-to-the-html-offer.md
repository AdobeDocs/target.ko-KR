---
description: 프로필 값과 활동 정보를 HTML 또는 JSON 오퍼에 직접 표시할 수 있습니다.
keywords: 동적 데이터; assets; 데이터; 오퍼; 개인화된 제안; 개인적 제안; 토큰 바꾸기
seo-description: 프로필 값과 활동 정보를 HTML 또는 JSON 오퍼에 직접 표시할 수 있습니다.
seo-title: 오퍼에 동적 데이터 전달
solution: Target
title: 오퍼에 동적 데이터 전달
topic: Premium
uuid: 1910a7f5-e4bd-413a-9875-e0b005407f50
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 오퍼에 동적 데이터 전달{#pass-dynamic-data-into-offers}

타겟 프로필에 저장된 방문자 정보를 동적으로 표시할 수 있습니다. 마찬가지로 활동 정보 (활동 이름 또는 경험의 이름 등) 를 사용하여 방문자의 관심사, 과거 행동 및 전체 프로필에 따라 개인화된 컨텐츠를 동적으로 반환하는 단일 오퍼를 만들 수도 있습니다.

**비즈니스 사례**

* 구매한 마지막 제품의 &quot;리필&quot; 또는 &quot;갱신&quot; 에 대한 할인 혜택을 홍보합니다. 카탈로그의 모든 항목에 대해 별도의 오퍼를 만드는 대신, 프로필에서 &quot;마지막으로 구매한 제품&quot; 를 읽고 오퍼에 링크를 표시하는 동적 텍스트가 포함된 오퍼를 만들 수 있습니다.
* 방문자가 `keyword=world` `cup`을 사용하여 랜딩 페이지에 도달합니다. 오퍼에 *World cup* 용어를 표시합니다.
* (1) 방문자의 장바구니에 추가된 마지막 항목 (Nike AIR MAX 1000 s), (2) 방문자의 색상 선호도 (검정) 및 방문자의 즐겨찾는 신발 카테고리 (Hoodies) 와 같은 정보가 포함된 추천 레이블을 개인화합니다. 예: &quot; Cool&#39;Black&#39;Hoodies &#39;! &quot;를 사용하여 Nike Air MAX 1000 s에 접근하십시오.&quot;


**기술적 장점**

사용자 특정 환경 설정, 비헤이비어, 상태 등을 사용자의 프로필에 저장할 수 있으며 다음 방문 시 이 메시지를 반복할 수 있습니다. 동적 오퍼를 사용하면 모든 방문자에 대해 개인화된 메시지를 표시하는 활동 내에서 하나의 오퍼를 설정할 수 있어 더 큰 규모의 확장이 가능합니다. 방문자의 의도가 변경되면 웹 사이트 컨텐츠가 해당 변경 사항을 자동으로 반영합니다.

**예**

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML 오퍼 코드: `Get your ${profile.keyword} information here!`
* 사용자가 보게 되는 내용: Get your World Cup information here!

다음 값은 &quot;토큰으로 대체&quot;될 수 있습니다.

| 값 | 예 |
|--- |--- |
| mbox 내부 프로필 매개 변수 | `${profile.age}` |
| 스크립트 프로필 매개 변수 | `${user.lifetimeSpend}` |
| mbox 매개 변수 | `${mbox.favoriteColor}` |
| 캠페인 정보 | `${campaign.name}`, `${campaign.recipe.name}`, `${campaign.id}`, `${campaign.recipe.id}` 및 `${campaign.recipe.trafficType}` |
| 고유 방문자 ID | `${user.pcId}` |
| 고유 세션 ID | `${user.sessionId}` |
| 방문자의 첫 번째 세션(true 또는 false) | `${user.isFirstSession}` |
| 과거 작동 | `{$user.endpoint.lastPurchasedEntity}`, `{$user.endpoint.lastViewedEntity}`, `{$user.endpoint.mostViewedEntity}`, `{$user.endpoint.categoryAffinity}` |

콘솔에서, 등의 디버깅 목적을 위해 정보를 `${campaign.name}``${campaign.id}``${campaign.recipe.name}``${campaign.recipe.id}``${offer.name}``${offer.id}`로그 `${campaign.name}`

Recommendations 디자인의 경우 디자인 개요의 [추가 예를 참조하십시오](/help/c-recommendations/c-design-overview/design-overview.md).

**구현**

mbox로 전달된 프로필 매개 변수의 경우 다음 구문을 사용합니다. `${profile.parameter}` 프로필 스크립트에서 만든 프로필 매개 변수의 경우 다음 구문을 사용합니다.

`${user.parameter}`

Recommendations 디자인에서 동적 속성을 사용하는 경우, 동적 값이 제대로 렌더링되려면 달러 기호 (&#39; $&#39;) 앞에 백슬래시 (&#39;\&#39;) 를 삽입해야 합니다. `\${user.endpoint.lastViewedEntity}`

이러한 변수는 서버 쪽의 값으로 대체되므로 제대로 표시되려면 따옴표나 다른 JavaScript가 필요합니다.

오퍼에 노출하려는 값에 대해 기본값을 지정할 수도 있습니다. 이 구문은 다음과 같습니다.

`${user.testAttribute default="All Items!"}`

`testAttribute`가 없거나 비어 있는 경우 &quot;&quot;모든 항목&quot;&quot;이 작성됩니다. 빈 프로필 속성 값이 유효하고 기본값을 표시하는 대신 해당 값을 쓰려는 경우 다음을 사용할 수 있습니다.

`${user.testAttribute default="All Items!" show_blank="true"}`

표시할 값을 escape하거나 escape 취소할 수도 있습니다. 예를 들어 값에 아포스트로피가 있는 경우 페이지의 JavaScript가 손상되지 않도록 값을 escape할 수 있습니다. (오퍼는 JavaScript로 작성되므로 단일 아포스트로피가 따옴표와 혼동될 수 있습니다.) 예:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`