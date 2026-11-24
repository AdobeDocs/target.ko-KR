---
keywords: 권장 사항;자주 묻는 질문;faq
description: '[!DNL Target Recommendations] 디자인에 대한 FAQ 및 답변.'
title: 디자인 FAQ
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
TQID: 'https://experienceleague.adobe.com/xRu0XEnc8wX8PZngba7CO67mFdja7HALL-1OSnhAmuY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: d5030abcda38bbc6d33b88ce3bb5d64f69e4e492
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 10%
---
# 디자인 FAQ {#design-faq}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Target] [!DNL Recommendations] 디자인에 대한 FAQ에 대한 답변을 찾아보세요.

>[!ENDSHADEBOX]

+++ 권장 품목 가격은 소수점 오른쪽에 두 자릿수를 어떻게 표시할 수 있습니까?

기본적으로 디자인에 반환된 숫자 값(예: `entity.value`)은 소수점 뒤에 0이 표시되지 않습니다. 예를 들어 항목 비용이 $35.00인 경우 `entity.value`은(는) 35와 같으며 $35.00이 아닌 35만 페이지에 표시됩니다.

이 문제를 해결하기 위해 두 가지 옵션을 사용할 수 있습니다.

* 속도 스크립팅 또는 JavaScript은 반환된 값에 형식을 적용할 수 있습니다.

* 항목의 가격을 두 개의 별도 엔티티 속성으로 전달할 수 있습니다. 첫 번째 `entity.value`는 숫자 비교(예: 가격 비교 규칙 등)에 사용할 수 있습니다. 두 번째는 올바른 렌더링을 허용하는 문자열로 엔티티 값을 저장하는 사용자 지정 특성(예: `entity.displayValue`)이어야 합니다.

  예:

  `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

+++

+++ $entity1.categoryId를 사용할 때 디자인에 범주가 표시되지 않는 이유는 무엇입니까?

디자인에 카테고리 ID를 표시할 수 없습니다. 여러 카테고리를 저장할 수 있으므로 시스템이 표시할 카테고리를 알지 못합니다.

+++

+++ 설계를 변경하여 즉시 업데이트하려면 어떻게 해야 합니까?

현재 사용 중인 디자인을 변경하면 업데이트하는 데 시간이 걸립니다. 디자인을 즉시 변경하려면 새 디자인을 만들고 활동에서 선택한 다음, 권장 사항을 저장합니다.

+++

+++ 핵심 제품의 범주 등 주요 정보를 디자인에 어떻게 표시할 수 있습니까?

`$key` 매개 변수는 디자인 내에서 표시할 주요 제품의 정보 대부분을 캡처합니다. 예를 들어 주요 제품의 썸네일을 표시하려면 `$key.thumbnailURL`을(를) 사용합니다.

+++

+++ 어느 버전의 Velocity를 사용합니까?

추가 도구 또는 라이브러리가 추가되지 않은 버전 1.7. Velocity의 기본 기능을 사용할 수 있습니다.

+++

+++ 프로모션 종료 시 항목의 entity.message를 지워야 하는 등의 상황에서 기존 엔티티 값을 공백으로 대체하려면 어떻게 해야 합니까?

JavaScript 줄바꿈 없는 공백이 전송되면 이 작업이 수행됩니다. 개발자는 `\u00A0`을(를) 값으로 보냅니다(예: `entity.message=\u00A0`). null 대신 아무런 값이 표시되지 않을 때 해당 값을 기본값으로 사용하는 것도 고려할 수 있습니다.

+++

+++ [!DNL Recommendations] 디자인에서 프로필 스크립트를 사용할 수 있습니까?

예. [!DNL Recommendations] 디자인에서 프로필 스크립트를 사용하려면 `\${...}`에서 이름을 래핑하십시오. 예를 들어 프로필 스크립트의 이름이 `user.basket`인 경우 디자인에서 `\${user.basket}`(으)로 참조합니다. 백슬래시는 프로필 스크립트가 Velocity에 의해 렌더링되지 않았음을 의미하므로 Velocity 템플릿의 프로필 스크립트에 대해 어떤 작업도 수행할 수 없습니다. 값이 페이지에 직접 인쇄됩니다.

+++
