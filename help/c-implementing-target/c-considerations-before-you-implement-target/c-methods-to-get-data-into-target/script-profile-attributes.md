---
keywords: 구현;구현;설정;스크립트 프로필 특성;implementation;setting up;script profile attributes
description: 스크립트 프로필 특성을 사용하여 데이터를 [!DNL Target] 에 가져옵니다.
title: '스크립트 프로필 속성을 사용하여 데이터를 가져오려면 어떻게 합니까? [!DNL Target] '
feature: 구현
role: Developer
exl-id: c323fb4c-f263-43d4-8523-9f42c2913542
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 83%

---

# 스크립트 프로필 속성

스크립트 프로필 속성은 [!DNL Adobe Target] 솔루션에 정의된 이름/값 쌍입니다. 서버 호출에 대해 Target 서버에서 JavaScript 코드 조각을 실행하여 값을 결정합니다.

사용자는 mbox 호출에 대해 실행되는 작은 코드 조각을 작성한 다음 대상 및 활동 멤버십에 대해 방문자를 평가합니다.

## 형식

스크립트 프로필 속성은 Target의 대상 섹션에서 만들어집니다. 모든 속성 이름은 유효하며, 값은 Target 사용자가 작성한 JavaScript 함수의 결과입니다. 인페이지 프로필 속성과 구분할 수 있도록 속성 이름에는 Target에서 자동으로 &quot;user. &quot;가 접두사로 지정됩니다.

코드 조각은 Rhino JS 언어로 작성되며 토큰 및 기타 값을 참조할 수 있습니다.

## 사용 사례 예

* **장바구니 포기**: 방문자가 장바구니에 도달하면 프로필 스크립트를 1로 설정합니다. 방문자가 전환하면 0으로 재설정합니다. 값이 1이면 방문자의 장바구니에 항목이 있습니다.
* **방문 카운트**: 모든 신규 방문에서 카운트가 1씩 증가하여 방문자가 사이트를 재방문하는 빈도를 추적합니다.

## 방법의 이점

페이지 코드 업데이트가 필요하지 않습니다.

대상 및 활동 멤버십 결정 전에 실행되므로 이러한 프로필 스크립트 속성은 단일 서버 호출의 멤버십에 영향을 줄 수 있습니다.

매우 활발히 실행될 수 있습니다. 스크립트당 많은 수의 명령어를 실행할 수 있습니다.

## 주의 사항

JavaScript 지식이 필요합니다.

프로필 스크립트의 실행 순서는 보장할 수 없으므로 서로 의존할 수 없습니다.

디버깅하기가 어려울 수 있습니다.

## 코드 예제

프로필 스크립트는 매우 유연합니다.

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### 관련 정보에 대한 링크

[프로필 스크립트 속성](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)의 프로필 스크립트 정보 카드 보기 섹션을 참조하십시오
