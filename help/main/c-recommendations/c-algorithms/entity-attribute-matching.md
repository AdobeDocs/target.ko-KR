---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;엔티티 속성 일치
description: 잠재적 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 [!DNL Target Recommendations]에서 동적으로 필터링하는 방법에 대해 알아봅니다.
title: 엔티티 속성 일치
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
TQID: 'https://experienceleague.adobe.com/2cBSfWXS96u7iumehPd7enxPjQcebkQCdSBSHWOUcJg'
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
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 5%
---
# 엔티티 속성 일치 {#entity-attribute-matching}

>[!BEGINSHADEBOX]

**이 페이지에서:** 잠재적 권장 항목 풀을 방문자가 상호 작용한 특정 항목과 비교하여 [!DNL Adobe Target Recommendations]에서 권장 사항을 동적으로 필터링하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

**[!UICONTROL 엔터티 특성 일치]**&#x200B;에서는 방문자가 상호 작용한 항목의 특성과 일치하는 항목만 권장합니다. 기준 및 프로모션에 대한 포함 규칙을 만들고 사용하는 프로세스는 사용 사례 및 예와 비슷합니다. 자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)을 참조하세요.

## 엔티티 속성 일치 예

**[!UICONTROL 엔터티 특성 일치]**&#x200B;은(는) 일치하는 항목만 추천할 수 있습니다. 예:

* 방문자가 현재 보고 있는 항목의 속성
* 방문자가 가장 최근에 본 항목
* 방문자가 가장 최근에 구매한 항목입니다
* 방문자가 가장 자주 본 항목
* 방문자 프로필의 사용자 지정 속성에 저장된 항목

### 브랜드를 기반으로 항목 추천

엔티티 속성 규칙이 빌드되면 페이지에 전달된 엔티티 값과 일치하지 않는 속성이 있는 모든 권장 사항을 필터링합니다. 이 프로세스를 수행하려면 페이지의 mbox에 `entity.brand` 값을 전달해야 합니다.

이러한 유형의 동적 포함 규칙을 사용하면 각 브랜드 이름에 대한 컬렉션이나 정적 필터 대신 모든 브랜드 페이지에서 관련 브랜드 결과를 반환하도록 하나의 권장 사항 규칙만 지정해야 합니다.

예를 들어 Brand A 제품을 사용하는 페이지가 표시되면 `entity.brand` 매개 변수의 값이 &quot;BrandA&quot;로 설정됩니다. 브랜드 랜딩 페이지에서 mbox는 `entity.brand=brandA`을(를) 반환합니다.

![Target 호출 예](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

그런 다음 페이지의 권장 사항에는 브랜드 A 제품만 포함됩니다.

![권장 사항 브랜딩](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Brand B 제품 페이지가 표시되면 `entity.brand` 값이 &quot;BrandB&quot;로 다시 설정되고 Brand B 제품만 권장됩니다. 마찬가지로 브랜드 B의 브랜드 랜딩 페이지에서 브랜드 B 제품만 반환됩니다.

![브랜드 B 권장 사항](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### 더 비싼 제품에 상향 판매

방문자가 더 높은 가격을 고려하도록 장려하기 위해, 따라서 더 수익성 있는 항목을 고려하도록 &quot;equals&quot;(다음과 같음)와 &quot;is between&quot;(다음 사이) 연산자는 동일한 카테고리 및 동일한 브랜드의 더 비싼 항목을 프로모션할 수 있습니다. 예를 들어, 신발 retailer은 다음 샘플처럼, 운동화를 보고 있는 방문자에게 더 비싼 운동화를 판촉하여 상향 판매를 제공할 수 있습니다.

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

동적 필터와 정적 필터를 혼합하여 비공개 레이블 제품을 프로모션할 수 있습니다. 예를 들어 다음 샘플과 같이 사무실 공급 회사는 토너를 보는 방문자에게 보다 수익성 있는 판매를 유도하기 위해 회사 사택 브랜드의 토너 카트리지를 홍보하고 펜을 보는 방문자에게 회사 사택 브랜드의 펜을 홍보할 수 있습니다.

![회사 브랜드](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
