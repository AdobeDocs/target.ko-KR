---
keywords: 동적 데이터;자산;데이터;오퍼;개인화된 오퍼;개인 오퍼;토큰 바꾸기
description: ' [!DNL Adobe Target]의 오퍼에 동적 데이터를 전달하는 방법을 알아봅니다.'
title: 다이내믹 데이터를 오퍼에 전달하려면 어떻게 합니까?
feature: Experiences and Offers
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
source-git-commit: 2e607b92e9d3408c1e91abd4646fe8eb840f2c30
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 55%

---

# 오퍼에 동적 데이터 전달

[!DNL Adobe Target] 프로필에 저장된 방문자 정보를 동적으로 표시할 수 있습니다. 마찬가지로 활동 정보(예: 활동 이름 또는 경험 이름)를 사용하여 방문자의 관심 사항, 과거 동작 및 전체 프로필에 따라 개인화된 콘텐츠를 동적으로 반환하는 단일 오퍼를 생성할 수도 있습니다.

## 비즈니스 사례

* 구매한 마지막 제품의 &quot;리필&quot;하거나 &quot;갱신&quot;하도록 할인된 오퍼를 홍보합니다. 카탈로그의 모든 항목에 대해 별도의 오퍼를 만드는 대신, 프로필에서 &quot;마지막으로 구매한 제품&quot;을 읽고 오퍼에 링크를 표시하는 동적 텍스트가 포함된 오퍼를 만들 수 있습니다.
* 방문자가 `keyword=world` `cup`을 사용하여 랜딩 페이지에 도달합니다. 오퍼에 *World cup* 용어를 표시합니다.
* (1) 방문자의 장바구니에 추가된 마지막 항목(Nike Air Max 1000s), (2) 방문자의 색상 선호도(검정), (3) 방문자가 즐겨찾는 신발 이외의 카테고리(후드) 등의 정보로 권장 사항 레이블을 개인화합니다. 예: &quot;이 멋진 &#39;검정&#39; &#39;후드&#39;에 &#39;Nike Air Max 1000s&#39;를 착용하십시오.&quot;

## 기술적 장점

방문자별 환경 설정, 동작, 상태가 방문자의 프로필에 저장될 수 있으므로 다음 방문 시 이 메시지를 반복할 수 있습니다. 다이내믹 오퍼를 사용하면 모든 방문자에 대해 개인화된 메시지를 표시하는 활동 내에서 단일 오퍼를 설정할 수 있어 더 큰 규모의 확장이 가능합니다. 방문자의 의도가 바뀌면 웹 사이트 콘텐츠에 그러한 변경 내용이 자동으로 반영됩니다.

## 예

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML 오퍼 코드: `Get your ${profile.keyword} information here!`
* 방문자 보기: 여기에서 월드컵 정보를 얻으십시오!

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
| 과거 동작 | `${user.endpoint.lastPurchasedEntity}`, `${user.endpoint.lastViewedEntity}`, `${user.endpoint.mostViewedEntity}`, `${user.endpoint.categoryAffinity}` |

`${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}` 등 디버깅 목적에 대한 정보를 콘솔에 기록

[!DNL Recommendations] 디자인에 대해서는 [디자인 개요](/help/main/c-recommendations/c-design-overview/design-overview.md)의 추가 예제를 참조하십시오.

## 구현

mbox로 전달된 프로필 매개 변수의 경우 다음 구문을 사용합니다.

`${profile.parameter}`

프로필 스크립트에서 생성된 프로필 매개 변수의 경우 다음 구문을 사용합니다.

`${user.parameter}`

[!DNL Recommendations] 디자인에서 동적 특성을 사용할 때 동적 값이 제대로 렌더링되려면 달러 기호( $ ) 앞에 백슬래시( \ )를 삽입해야 합니다.

`\${user.endpoint.lastViewedEntity}`

이러한 변수는 서버 쪽의 값으로 대체되므로 제대로 표시되려면 따옴표나 다른 JavaScript가 필요합니다.

오퍼에 표시할 값에 대해 기본값을 지정할 수도 있습니다. 이 구문은 다음과 같습니다.

`${user.testAttribute default="All Items!"}`

`testAttribute`이(가) 없거나 비어 있으면 &quot;모든 항목&quot;이 표시됩니다. 작성되었습니다. 빈 프로필 속성 값이 유효하고 기본값을 표시하는 대신 해당 값을 쓰려는 경우 다음을 사용할 수 있습니다.

`${user.testAttribute default="All Items!" show_blank="true"}`

표시할 값을 escape하거나 escape 취소할 수도 있습니다. 예를 들어 값에 아포스트로피가 있는 경우 값을 이스케이프 처리할 수 있으므로 페이지의 JavaScript이 손상되지 않습니다. (오퍼는 JavaScript로 작성되므로 단일 아포스트로피가 따옴표와 혼동될 수 있습니다.) 예:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`

오퍼 콘텐츠에 사용되는 오퍼 매개 변수(offer.name, offer.id)의 경우:

해당 오퍼가 경험에 설정된 여러 오퍼 중 하나이면 마지막으로 추가된 오퍼의 값이 매개 변수의 값을 채웁니다. 즉, 이러한 매개 변수는 경험 수준에서 평가됩니다.