---
keywords: 구현;구현;설정;페이지 매개 변수
description: 페이지 내 프로필 속성을 사용하여 Target에 데이터를 가져옵니다.
title: 페이지 내 프로필 속성을 사용하여 데이터를 Target으로 가져오려면 어떻게 합니까?
feature: Implementation
role: Developer
exl-id: c6000720-a862-4e9c-96a5-055963a79544
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 56%

---

# 페이지 내 프로필 속성

[!DNL Adobe Target]의 페이지 내 프로필 속성(&quot;mbox 내부 프로필 특성&quot;이라고도 함)은 나중에 사용하기 위해 방문자의 프로필에 저장된 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.

인페이지 프로필 속성을 사용하면 나중에 타깃팅 및 세그멘테이션을 수행할 수 있도록 사용자별 데이터를 Target의 프로필에 저장할 수 있습니다.

## 형식

인페이지 프로필 속성은 서버 호출을 통해 속성 이름 앞에 접두사 &quot;profile.&quot;을 사용하는 문자열 이름/값 쌍으로 Target에 전달됩니다.

속성 이름과 값은 사용자 지정할 수 있습니다(특정 용도로 &quot;예약된 이름&quot;도 있음).

### 예

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

## 활용 사례 예

* **로그인 정보**: 사용자의 로그인을 기준으로 비PII(개인 식별 정보) 데이터를 Target에 공유합니다. 이 데이터는 멤버십 상태, 주문 내역 등이 될 수 있습니다.
* **스토어 정보**: 이 사용자의 기본 설정 위치가 되는 스토어를 추적합니다.
* **이전 상호 작용**: 향후 개인화할 때 알려주기 위해 이전에 사이트에서 수행한 작업을 추적합니다.

## 방법의 이점

데이터는 실시간으로 Target으로 전송되며 데이터가 들어오는 동일한 서버 호출에서 사용할 수 있습니다.

## 주의 사항

페이지 코드 업데이트가 필요합니다(직접 또는 태그 관리 시스템 사용).

속성 및 값은 서버 호출에 표시되므로 방문자가 값을 볼 수 있습니다. 신용 범위 또는 기타 잠재적인 개인 정보와 같은 정보를 공유하는 경우 이 방법이 가장 좋은 방법은 아닐 수 있습니다.

## 코드 예제

targetPageParamsAll(속성을 페이지의 모든 mbox 호출에 추가합니다.):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams(속성을 페이지의 글로벌 mbox에 추가합니다.):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

mboxCreate 코드에 있는 속성:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

## 관련 정보에 대한 링크

[프로필 속성](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[방문자 프로필](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)
