---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;엔티티 속성 일치
description: 잠재적 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여  [!DNL Target Recommendations] 에서 동적으로 필터링하는 방법에 대해 알아봅니다.
title: Recommendations 활동에서 엔티티 속성 일치로 필터링하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 57b8c214-6b18-4ab1-8548-906d02f162c5
source-git-commit: 22b0ba18efb736b291f9b7951acd9f706beedbe1
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 엔티티 속성 일치

잠재적 권장 사항 항목의 풀을 사용자가 상호 작용한 특정 항목과 비교하여 [!DNL Adobe Target Recommendations]에서 동적으로 필터링합니다.

>[!NOTE]
>
>기준 및 프로모션에 대한 [포함 규칙을 만들고 사용하기 위한 프로세스](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)는 사용 사례 및 예제와 유사합니다.

예를 들어 다음 예제와 같이 현재 항목의 브랜드와 일치하는 항목만 추천합니다.

브랜드 랜딩 페이지의 mbox가 `entity.brand=brandA`을(를) 반환하는 경우 브랜드 A 제품만 반환되고 해당 페이지에 표시됩니다. 마찬가지로 브랜드 B의 브랜드 랜딩 페이지에서 브랜드 B 제품만 반환됩니다. 이러한 유형의 동적 포함 규칙을 사용하면 사용자는 각 브랜드 이름과 일치하도록 컬렉션이나 정적 필터를 지정하는 대신 모든 브랜드 페이지에서 관련 브랜드 결과를 반환하는 권장 사항 규칙을 하나만 지정해야 합니다.

이 프로세스가 작동하려면 해당 랜딩 페이지의 mbox에 `entity.brand`을(를) 전달해야 합니다.

## 엔티티 속성 일치 예

[!UICONTROL Entity Attribute Matching]에서 일치하는 항목만 추천할 수 있습니다. 예:

* 사용자가 현재 보고 있는 항목의 속성
* 사용자가 가장 최근에 본 항목
* 사용자가 가장 최근에 구매한 항목
* 사용자가 가장 자주 본 항목
* 방문자 프로필의 사용자 지정 속성에 저장된 항목

### 브랜드를 기반으로 항목 추천

엔티티 속성 규칙이 빌드되면 페이지에 전달된 엔티티 값과 일치하지 않는 속성이 있는 모든 권장 사항이 필터링됩니다.

다음 예는 페이지에 표시된 제품 브랜드와 일치하는 권장 사항을 보여 줍니다.

Brand A 제품을 사용하는 페이지를 방문하면 `entity.brand` 매개 변수의 값이 &quot;BrandA&quot;로 설정됩니다.

![Target 호출 예](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

페이지의 권장 사항에는 브랜드 A 제품만 표시됩니다.

![권장 사항 브랜딩](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

그런 다음 Brand B 제품 페이지를 보면 `entity.brand` 값이 &quot;BrandB&quot;로 재설정되고 Brand B 제품 페이지에 권장되는 Brand B 제품이 표시됩니다.

![브랜드 B 권장 사항](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### 더 비싼 제품에 상향 판매

의류 소매업체이고 사용자가 더 높은 가격을 고려하고 따라서 더 수익성 있는 품목을 고려하도록 장려하고 싶다고 가정해 보겠습니다. &quot;equals&quot;(다음과 같음)와 &quot;is between&quot;(다음 사이) 연산자를 사용하여 동일한 카테고리 및 동일한 브랜드의 더 비싼 항목을 프로모션할 수 있습니다. 예를 들어, 신발 소매업체는 다음 샘플처럼 러닝 슈즈를 찾는 방문자에게 상향 판매를 하기 위해 더 비싼 러닝 슈즈를 홍보할 수 있습니다.

![업셀링](/help/main/c-recommendations/c-algorithms/assets/upsell-new.png)

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

동적 필터와 정적 필터를 혼합하여 비공개 레이블 제품을 프로모션할 수 있습니다. 예를 들어, 사무용품 회사는 토너를 보는 방문자에게 보다 수익성 있는 판매를 유도하기 위해 회사 집 브랜드의 토너 카트리지를 홍보할 수 있으며, 다음 샘플에서와 같이 펜을 보는 방문자에게 보다 수익성 있는 판매를 유도하기 위해 회사 집 브랜드의 펜을 홍보할 수 있습니다.

![회사 브랜드](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)
)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
