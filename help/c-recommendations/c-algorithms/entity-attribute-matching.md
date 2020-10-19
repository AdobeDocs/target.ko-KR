---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: 잠재적인 추천 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 Adobe Target Recommendations에서 동적으로 필터링합니다.
title: Adobe Target Recommendations의 동적 포함 규칙의 엔티티 속성 일치별 필터링
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) 엔티티 속성 일치

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

예를 들어 다음 예제와 같이 현재 항목의 브랜드와 일치하는 항목만 권장합니다.

브랜드 랜딩 페이지의 mbox가 반환되는 `entity.brand=Nike`경우 Nike 제품만 반환되고 해당 페이지에 표시됩니다. 마찬가지로 아디다스 브랜드 랜딩 페이지에서 아디다스 제품만 반환됩니다. 이러한 유형의 동적 포함 규칙을 사용할 경우 사용자는 각 브랜드 이름에 맞게 컬렉션이나 정적 필터를 지정하는 대신 모든 브랜드 페이지에 걸쳐 관련 브랜드 결과를 반환하는 하나의 추천 규칙만 지정해야 합니다.

## 엔티티 속성 일치 예

[!UICONTROL 엔티티 속성 일치를] 사용하면 일치하는 항목만 권장할 수 있습니다. 예:

* 사용자가 현재 보고 있는 항목의 속성
* 사용자가 가장 최근에 본 항목
* 사용자가 가장 최근에 구매한 항목
* 사용자가 가장 자주 본 항목
* 방문자 프로필의 사용자 지정 속성에 저장된 항목

### 더 비싼 제품으로 업셀링

귀하가 의류 소매업체이고 사용자에게 더 높은 가격을 고려하고, 따라서 더 수익성 높은 품목을 고려하도록 권장하려고 한다고 가정합니다. &quot;같음&quot; 및 &quot;사이&quot; 연산자를 사용하여 동일한 카테고리와 동일한 브랜드의 보다 비싼 항목을 홍보할 수 있습니다. 예를 들어 다음 코드 샘플에서와 같이 운동화를 찾는 방문자를 업셀링하기 위해 신발 소매업체는 더 비싼 런닝화를 홍보할 수 있습니다.

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

### 비공개 레이블 제품 홍보

동적 필터와 정적 필터를 혼합하여 비공개 레이블 제품을 홍보할 수 있습니다. 예를 들어, 사무용 공급 업체는 다음 코드 샘플에서와 같이 회사 주택 브랜드의 토너 카트리지를 홍보하여 토너를 보는 방문자에게 보다 수익성이 높은 매출을 올리고 회사 브랜드 펜의 펜을 홍보하여 펜을 보고 있는 방문자에게 보다 수익성 높은 매출을 올릴 수 있습니다.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
