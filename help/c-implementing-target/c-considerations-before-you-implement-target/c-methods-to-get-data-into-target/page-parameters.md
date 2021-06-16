---
keywords: 구현;구현하기;설정하기;설정;페이지 매개 변수
description: 페이지 매개 변수를 사용하여 [!DNL Target] 에 데이터를 가져옵니다.
title: 페이지 매개 변수를 사용하여 [!DNL Target] 에 데이터를 가져오려면 어떻게 해야 합니까?
feature: 구현
role: Developer
exl-id: a285eadc-b71e-49a8-9071-397ada283baf
source-git-commit: c91465cccc244d79b6540004237a5ce7156233bb
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 46%

---

# 페이지 매개 변수

페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함)는 나중에 사용할 수 있도록 방문자의 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달되는 이름/값 쌍입니다.

페이지 매개 변수는 향후 타깃팅을 사용하기 위해 방문자의 프로필과 함께 저장할 필요가 없는 Target으로 페이지 데이터를 전송하는 데 유용합니다. 대신 이 값은 페이지나, 특정 페이지에서 사용자가 취하는 행동을 설명하는 데 사용됩니다.

## 형식

페이지 매개 변수는 서버 호출을 통해 문자열 이름/값 쌍으로 Target에 전달됩니다. 매개 변수 이름과 값은 사용자 지정할 수 있습니다(특정 용도로 &quot;예약된 이름&quot;도 있음).

### 예

* `page=productPage`

* `categoryId=homeLoans`

## 사용 사례 예

* **제품 페이지**:표시된 특정 제품에 대한 정보를 보냅니다(Recommendations 작동 방식).
* **주문 세부 사항**:주문 수집을 위해 주문 ID, orderTotal 등을 보냅니다.
* **카테고리 친화성**: 특정 사이트 카테고리에 대한 사용자의 친화성에 대한 지식을 구축하기 위해 본 카테고리 정보를 Target에 보냅니다.
* **타사 데이터**: 날씨 타깃팅 제공자, 계정 데이터(예: DemandBase), 인구 데이터(예: Experian) 등과 같은 타사 데이터 소스의 정보를 보냅니다.

## 방법의 이점

데이터는 실시간으로 Target으로 전송되고 데이터가 들어오는 데이터를 호출하는 동일한 서버 호출에서 사용할 수 있습니다.

## 주의 사항

* 페이지 코드 업데이트가 필요합니다(직접 또는 태그 관리 시스템 사용).
* 후속 페이지/서버 호출 시 타깃팅에 데이터를 사용해야 하는 경우 프로필 스크립트로 변환해야 합니다.
* 쿼리 문자열에는 [IETF(Internet Engineering Task Force) 표준](https://www.ietf.org/rfc/rfc3986.txt)에 대한 문자만 포함될 수 있습니다 .

   IETF 사이트에서 언급된 문자 외에도, Target은 쿼리 문자열에 다음과 같은 문자를 허용합니다.

   ```< > # % " { } | \ ^ [ ] ` ```

   다른 모든 문자는 URL로 인코딩해야 합니다. 이 표준에서는 아래 그림과 같이 다음 형식( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) )을 지정합니다.

   ![](assets/ietf1.png)

   또는 간단하게 전체 목록을 지정합니다.

   ![](assets/ietf2.png)

## 코드 예

targetPageParamsAll(매개 변수를 페이지의 모든 mbox 호출에 추가합니다.):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams(매개 변수를 페이지의 글로벌 mbox에 추가합니다.):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

mboxCreate 코드에 있는 매개 변수:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

## 관련 정보에 대한 링크

권장 사항: [페이지 유형에 따른 구현](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

주문 확인: [전환 추적](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

카테고리 친화성: [카테고리 친화성](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)
