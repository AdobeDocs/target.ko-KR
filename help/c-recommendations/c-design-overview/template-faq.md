---
keywords: recommendations;frequently asked questions;faq
description: Adobe Target 권장 사항 디자인에 대한 FAQ(자주 묻는 질문) 목록입니다.
title: 디자인 FAQ
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 87%

---


# ![PREMIUM](/help/assets/premium.png) 디자인 FAQ {#design-faq}

[!DNL Adobe Target] 추천 디자인에 대한 FAQ(자주 묻는 질문) 목록

## 권장 품목 가격이 소수점 오른쪽에 두 값을 모두 표시하지 않습니다. 어떻게 표시할 수 있습니까?

기본적으로 디자인 템플릿에서 반환되는 숫자 값(예: `entity.value`) 은 소수점 뒤에 0이 표시되지 않습니다. 예를 들어, 항목이 $35.00인 경우 `entity.value`은 35와 같으며 $35.00이 아닌 35만 페이지에 표시됩니다.

이 문제를 해결하기 위해 두 가지 옵션을 사용할 수 있습니다:

* 속도 스크립팅 또는 Javascript를 사용하여 반환된 값에 서식을 적용할 수 있습니다.

* 항목의 가격을 두 개의 별도 엔티티 속성으로 전달할 수 있습니다. 첫 번째 `entity.value`는 숫자 비교(예: 가격 비교 규칙 등)에 사용할 수 있습니다. 두 번째는 올바른 렌더링을 허용하는 문자열로 엔티티 값을 저장하는 사용자 지정 속성(예: `entity.displayValue`)이어야 합니다.

   예:

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## 디자인에 카테고리가 표시되지 않는 이유는 무엇입니까? $entity1.categoryId를 사용하고 있습니다.{#section_073309B8051049C7953D396A93EA0713}

카테고리 ID는 디자인에 표시할 수 없습니다. 여러 카테고리가 저장될 수 있으므로 시스템에서는 어느 카테고리를 표시할지 모르게 됩니다.

## 즉시 업데이트를 받으려면 디자인을 어떻게 변경해야 합니까? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

현재 사용 중인 디자인을 변경하면 업데이트하는 데 시간이 걸립니다. 디자인을 즉시 변경하려면 새 디자인을 만들고 활동에서 선택하고 권장 사항을 저장합니다.

## 디자인에서 표시할 주요 정보를 캡처할 수 있습니까? 예: 주요 제품 카테고리를 표시하려는 경우 Velocity 디자인에서 해당 값을 어떻게 코딩할 수 있습니까?  {#section_F08043B14BA24BC8815FEF25F4F84C39}

`$key. *`값`*`매개 변수가 디자인에서 표시할 주요 제품 정보 대부분을 캡처합니다. 예: 주요 제품 썸네일을 표시하려면 `$key.thumbnailURL`을 사용합니다.

## 어느 버전의 Velocity를 사용합니까? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

추가 도구 또는 라이브러리가 추가되어 있는 버전 1.7. Velocity의 기본 기능을 사용할 수 있습니다.

## 기존 개체 값을 빈 값으로 바꾸려면 어떻게 해야 합니까? 예를 들어 판촉 행사가 끝나면 항목의 entity.message를 지워야 합니다. {#section_B88F2C2925DC4508974B2F8B13F961CB}

JavaScript 줄바꿈 없는 공백으로 보내면 이렇게 되는 것 같습니다. 개발자가 값으로 `\u00A0`을 보내게 하십시오. 예: `entity.message=\u00A0`. Null 대신 아무런 값이 표시되지 않는 경우 해당 값이 기본값이 되는 것으로 간주할 수 있습니다.

## 권장 사항 디자인에서 프로필 스크립트를 사용할 수 있습니까? {#section_6BD55203984A4D80A0C6F241AD7806DF}

예. 하지만 프로필 스크립트 이름의 $ 앞에 백슬래시(\)를 추가해야 합니다.
