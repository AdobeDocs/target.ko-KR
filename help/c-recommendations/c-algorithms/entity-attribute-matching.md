---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;동적 필터링;동적 필터링;개체 특성 일치
description: 잠재적인 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 Adobe Target Recommendations에서 동적으로 필터링하는 방법을 알아봅니다.
title: Recommendations 활동에서 개체 속성 일치별로 필터링하려면 어떻게 합니까?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMnty 속성 일치

잠재적인 추천 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 [!DNL Adobe Target] [!DNL Recommendations]에서 동적으로 필터링합니다.

>[!NOTE]
>
>기준 및 판촉 행사에 대한 포함 규칙](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)을 만들고 사용하는 [프로세스는 사용 사례 및 예와 유사합니다.

예를 들어 다음 예제와 같이 현재 항목의 브랜드와 일치하는 항목만 권장합니다.

브랜드 랜딩 페이지의 mbox가 `entity.brand=brandA`을 반환하면 브랜드 A 제품만 반환되고 해당 페이지에 표시됩니다. 마찬가지로 브랜드 B의 브랜드 랜딩 페이지에서도 브랜드 B 제품만 반환됩니다. 이러한 유형의 동적 포함 규칙을 사용하면 각 브랜드 이름에 맞게 컬렉션이나 정적 필터를 지정하는 대신 모든 브랜드 페이지에 관련 브랜드 결과를 반환하는 권장 사항 규칙을 하나만 지정해야 합니다.

이 작업을 수행하려면 랜딩 페이지의 mbox에 `entity.brand`을 제공해야 합니다.

## 엔티티 속성 일치 예

[!UICONTROL 엔티티 속성 ] 일치를 사용하면 일치하는 항목만 권장할 수 있습니다. 예:

* 사용자가 현재 보고 있는 항목의 속성
* 사용자가 가장 최근에 본 항목
* 사용자가 가장 최근에 구매한 항목
* 사용자가 가장 자주 본 항목
* 방문자 프로필의 사용자 지정 속성에 저장된 항목

### 브랜드를 기반으로 하는 항목 추천

개체 속성 규칙이 빌드되면, 페이지에서 전달된 개체 값과 일치하지 않는 특성을 가진 모든 권장 사항을 필터링합니다.

다음 예는 페이지에 표시된 제품 브랜드와 일치하는 권장 사항을 보여줍니다.

브랜드 A 제품을 특징으로 하는 페이지를 방문하면 이 페이지는 `entity.brand` 매개 변수의 값을 &quot;BrandA&quot;로 설정합니다.

![Target 호출 예](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

페이지의 권장 사항에는 브랜드 A 제품만 표시됩니다.

![브랜드 A 추천](/help/c-recommendations/c-algorithms/assets/brandA.png)

그런 다음 브랜드 B 제품 페이지를 보면 `entity.brand` 값이 &quot;BrandB&quot;로 재설정되고 브랜드 B 제품 페이지에서 권장되는 브랜드 B 제품이 표시됩니다.

![브랜드 B 추천](/help/c-recommendations/c-algorithms/assets/brandB.png)

### 더 비싼 제품으로 업셀링

의류 소매업체이며 사용자에게 더 높은 가격을 고려하도록 권장하고, 따라서 수익성이 높은 품목을 고려하고 있다고 가정해 보십시오. &quot;같음&quot; 및 &quot;다음 사이&quot; 연산자를 사용하여 동일한 카테고리와 동일한 브랜드의 보다 비싼 항목을 홍보할 수 있습니다. 예를 들어 신발 소매업체는 다음 샘플에서와 같이 런닝화를 보고 있는 방문자를 업셀링하기 위해 더 비싼 런닝화를 홍보할 수 있습니다.

![업셀링](/help/c-recommendations/c-algorithms/assets/upsell.png)

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

동적 필터와 정적 필터를 혼합하여 비공개 레이블 제품을 홍보할 수 있습니다. 예를 들어, 사무용품 회사는 다음 샘플에서와 같이, 다음 샘플에서와 같이 토너를 보는 방문자에게 보다 수익성이 높은 판매량을 제공하기 위해 회사 주택 브랜드의 토너 카트리지를 홍보할 수 있으며, 펜을 보고 있는 방문자에게 보다 수익성 높은 판매를 유도할 수 있도록 회사 주택 브랜드의 펜 펜을 홍보할 수 있습니다.

![하우스 브랜드](/help/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
