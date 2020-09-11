---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: 기준 및 프로모션을 위해 Adobe Target Recommendations에서 포함 규칙을 만들고 더 나은 결과를 얻기 위해 동적 또는 정적 필터링 규칙을 추가하는 방법에 대한 정보입니다.
title: Adobe Target Recommendations에서 동적 및 정적 포함 규칙 사용
feature: criteria
mini-toc-levels: 3
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
translation-type: tm+mt
source-git-commit: 381c405e55475f2474881541698d69b87eddf6fb
workflow-type: tm+mt
source-wordcount: '1478'
ht-degree: 54%

---


# ![PREMIUM](/help/assets/premium.png) 동적 및 정적 포함 규칙 사용{#use-dynamic-and-static-inclusion-rules}

Adobe Target에서 기준 및 판촉 행사에 대한 포함 규칙 만들기와 권장 사항에 대한 더 나은 결과를 얻기 위해 추가적인 동적 또는 정적 필터링 규칙을 추가하는 방법에 대한 정보입니다.

기준 및 프로모션에 대한 포함 규칙을 만들고 사용하는 프로세스는 사용 사례 및 예와 비슷합니다. 기준 및 프로모션과 포함 규칙의 사용은 모두 이 주제에서 다룹니다.

## 기준에 필터링 규칙 추가 {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

[기준을 만들려면](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) **[!UICONTROL 포함 규칙]** 아래의 **[!UICONTROL 필터링 규칙 추가]**&#x200B;를 클릭하십시오.

![](assets/inclusion_options_new.png)

사용 가능한 선택 사항은 선택한 업계 카테고리와 권장 사항 키에 따라 다릅니다.

## 프로모션에 필터링 규칙 추가 {#section_D59AFB62E2EE423086281CF5D18B1076}

[프로모션을 만들려면](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) **[!UICONTROL 속성별 프로모션]**&#x200B;을 선택한 다음, **[!UICONTROL 필터링 규칙 추가]**&#x200B;를 클릭하십시오.

![](assets/inclusion_options.png)

## 필터 유형 {#section_0125F1ED10A84C0EB45325122460EBCD}

다음 표에는 기준과 프로모션 모두에 대한 필터링 선택 사항의 유형이 나열되어 있습니다.

### 동적 필터링

동적 필터링에 사용할 수 있는 옵션은 다음과 같습니다.

#### 엔티티 속성 일치

잠재적 추천 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 동적으로 필터링합니다.

예를 들어 현재 항목의 브랜드와 일치하는 항목만 추천합니다.

사용 가능한 연산자:

* equals
* 다음과 같지 않음
* 다음 사이
* 다음 포함
* 다음을 포함하지 않음
* 다음으로 시작
* 다음으로 끝남
* 값이 있음
* 값이 없음
* 다음보다 크거나 같음
* 다음보다 작거나 같음

#### 프로필 속성 일치

사용자 프로필의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

예를 들어 현재 항목의 브랜드와 일치하는 항목만 추천합니다.

사용 가능한 연산자:

* equals
* 다음과 같지 않음
* 다음 포함
* 다음을 포함하지 않음
* 다음으로 시작
* 다음으로 끝남
* 다음보다 크거나 같음
* 다음보다 작거나 같음
* 다음 사이

#### 매개 변수 일치

요청(API 또는 mbox)의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

예를 들어, &quot;업계&quot; 페이지 매개 변수와 일치하는 컨텐츠만 추천합니다.

중요: 활동이 2016년 10월 31일 이전에 만들어진 경우 &quot;매개 변수 일치&quot; 필터를 사용하면 전달이 실패합니다. 이 문제를 해결하려면 다음을 수행하십시오.

* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.

사용 가능한 연산자:

* equals
* 다음과 같지 않음
* 다음 포함
* 다음을 포함하지 않음
* 다음으로 시작
* 다음으로 끝남
* 다음보다 크거나 같음
* 다음보다 작거나 같음
* 다음 사이

### 값별 필터링

동적 필터링에 다음 옵션을 사용할 수 있습니다.

#### 정적 필터

필터링할 정적 값을 하나 이상 수동으로 입력합니다.

예를 들어, MPAA 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 컨텐츠만 추천합니다.

사용 가능한 연산자:

* equals
* 다음과 같지 않음
* 다음 포함
* 다음을 포함하지 않음
* 다음으로 시작
* 다음으로 끝남
* 값이 있음
* 값이 없음
* 다음보다 크거나 같음
* 다음보다 작거나 같음

>[!NOTE]
>
>Target 17.6.1 릴리스(2017년 6월) 이전에 포함 규칙이 구성되는 방식을 잘 알고 있다면, 일부 선택 사항과 연산자가 변경되었음을 알 수 있을 것입니다. 선택한 선택 사항에 적용 가능한 연산자만 표시되고, 일부 연산자의 이름은 더 일관되고 직관적이게 변경되었습니다(&quot;일치&quot;(matches)는 이제 &quot;다음과 같음&quot;(equals)임). 이 릴리스 이전에 만들어진 모든 기존 제외 규칙은 새 구조로 자동 마이그레이션됩니다. 여러분 쪽에서는 구조를 조정할 필요가 없습니다.

포함 규칙을 필요한 만큼 만들 수 있습니다. 포함 규칙들은 AND 연산자로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

## 동적 기준 및 프로모션 예

동적 기준과 프로모션은 정적 기준과 프로모션보다 훨씬 더 강력하며, 더 나은 결과와 참여를 만들어냅니다.

다음 예는 마케팅 작업에서 동적 프로모션을 사용할 수 있는 방법에 대한 아이디어를 제공할 것입니다.

### 다음과 같음

방문자가 웹 사이트의 항목(예: 제품, 아티클 또는 동영상)을 보고 있는 경우 동적 판촉 행사에서 &quot;같음&quot; 연산자를 사용하면 다음 제품에서 다른 항목을 홍보할 수 있습니다.

* 동일한 브랜드
* 동일한 카테고리
* 동일한 카테고리 AND 판매자 브랜드
* 동일한 스토어

### 같지 않음

방문자가 웹 사이트의 항목(예: 제품, 아티클 또는 동영상)을 보고 있는 경우 동적 판촉 행사에서 &quot;같지 않음&quot; 연산자를 사용하면 다음 제품에서 다른 항목을 홍보할 수 있습니다.

* 다른 TV 시리즈
* 다른 장르
* 다른 제품 시리즈
* 다른 스타일 ID

### 다음 사이

방문자가 웹 사이트의 항목(예: 제품, 아티클 또는 동영상)을 보고 있는 경우 동적 판촉 행사에서 &quot;사이&quot; 연산자를 사용하면 다음과 같은 다른 항목을 홍보할 수 있습니다.

* 더 비쌈
* 덜 비쌈
* 비용 더하기 또는 빼기 30%
* 동일한 시즌의 나중 에피소드
* 시리즈에서 앞부분 책

## Handling empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching] for exit criteria and promotions.

이전에는 값이 비어 있으면 결과가 반환되지 않았습니다. &quot;*x*&#x200B;이(가) 비어 있는 경우&quot; 드롭다운 목록에서는 다음 그림과 같이 기준에 빈 값이 있을 경우 수행할 적절한 작업을 선택할 수 있습니다.

![](assets/empty_value.png)

원하는 작업을 선택하려면 톱니바퀴 아이콘(![](assets/icon_gear.png))을 마우스로 가리킨 다음, 원하는 작업을 선택하십시오.

| 작업 | 사용 가능한 경우 | 세부 사항 |
|--- |--- |--- |
| 이 필터링 규칙 무시 | 프로필 속성 일치<br>매개 변수 일치 | 프로필 속성 일치와 매개 변수 일치에 대한 기본 작업입니다.<br>이 선택 사항은 규칙이 무시되도록 지정합니다. 예를 들어 세 개의 필터링 규칙이 있고 세 번째 규칙이 어떤 값도 전달하지 않는 경우, 결과를 반환하는 대신 빈 값으로 세 번째 규칙을 무시할 수 있습니다. |
| 항목 홍보 안 함 | 개체 특성<br>일치프로필 특성<br>일치매개 변수 일치 | 엔티티 속성 일치에 대한 기본 작업입니다.<br>이 작업은 이 옵션을 추가하기 전에 빈 값을 처리하는 방법입니다. [!DNL Target] 이 기준에 대해서는 결과가 표시되지 않습니다. |
| 정적 값 사용 | 엔티티 속성 일치<br>프로필 속성 일치<br>매개 변수 일치 | 값이 비어 있으면 정적 값을 사용하도록 선택할 수 있습니다. |

## 프로필 속성 일치 예 {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL 프로필 속성 일치를] 사용하면 아래 예와 같이 방문자 프로필의 속성과 일치하는 항목만 권장할 수 있습니다.

### 예 1:사용자가 좋아하는 브랜드의 항목 추천

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. 이러한 규칙을 사용할 때, 방문자가 특정 브랜드의 육상용 반바지를 보고 있다면 해당 사용자가 자주 이용하는 브랜드(방문자 프로필의 `profile.favoritebrand`에 저장된 값)와 일치하는 권장 사항만 표시됩니다.

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### 예 2:구직자와 직장 일치

구직자들과 일자리를 맞추기 위해 노력한다고 가정합시다. 구직자와 같은 도시에 있는 일자리만 추천하고 싶은 것이다.

다음 예와 같이 포함 규칙을 사용하여 구직 방문자의 프로필에서 직무 목록까지의 위치를 일치시킬 수 있습니다.

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

## 엔티티 속성 일치 예

[!UICONTROL 개체 속성 일치를] 사용하면 아래 예와 같이 사용자가 현재 보고 있는 항목의 속성과 일치하는 항목, 사용자가 가장 최근에 본 항목, 사용자가 가장 최근에 구입한 항목, 사용자가 가장 자주 본 항목 또는 방문자 프로필의 사용자 지정 속성에 저장된 항목에서 권장할 수 있습니다.

### 예 3:더 비싼 제품으로 업셀링

귀하가 의류 소매업체이고 사용자에게 더 높은 가격을 고려하고, 따라서 더 수익성 높은 품목을 고려하도록 권장하려고 한다고 가정합니다. &quot;같음&quot; 및 &quot;사이&quot; 연산자를 사용하여 동일한 카테고리와 동일한 브랜드의 보다 비싼 항목을 홍보할 수 있습니다. 예를 들어 신발 소매업체는 런닝화를 보고 있는 방문자를 업셀링하기 위해 더 비싼 런닝화를 홍보할 수 있습니다.

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

### 예 4:비공개 레이블 제품 홍보

동적 필터와 정적 필터를 혼합하여 비공개 레이블 제품을 홍보할 수 있습니다. 예를 들어 사무용 공급 업체는 자사 브랜드에 있는 토너 카트리지를 홍보하여 토너를 보는 방문자에게 보다 수익성 높은 판매를 유도하고 회사 브랜드 펜의 펜을 홍보하여 펜을 보는 방문자에게 보다 수익성 높은 매출을 올릴 수 있습니다.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```

## 주의 사항 {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>&quot;equals&quot;(다음과 같음)와 &quot;does not equal&quot;(다음과 같지 않음) 연산자를 사용하는 런타임 동안 서로 다른 데이터 유형 속성이 동적 기준이나 프로모션에서 호환되지 않을 수 있습니다. You should use [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory], and [!UICONTROL Environment] values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.

![](assets/left_right.png)

다음 표는 유효 규칙과 런타임 중에 호환되지 않을 수 있는 규칙을 보여줍니다.

| 호환 규칙 | 호환되지 않는 규칙 |
|--- |--- |
| 값 - 다음 사이 - 현재 항목의 90%와 110% - salesValue | salesValue - 다음 사이 - 현재 항목의 90%와 110% - 값 |
| 값 - 다음 사이 - 현재 항목의 90%와 110% - 값 | clearancePrice - 다음 사이 - 현재 항목의 90%와 110% - 순익 |
| 순익 - 다음 사이 - 현재 항목의 90%와 110% - 순익 | storeInventory - 다음과 같음 - 현재 항목 - 재고 |
| 재고 - 다음과 같음 - 현재 항목 - 재고 |  |
