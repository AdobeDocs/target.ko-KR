---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: 기준 및 프로모션을 위해 Adobe Target Recommendations에서 포함 규칙을 만들고 더 나은 결과를 얻기 위해 동적 또는 정적 필터링 규칙을 추가하는 방법에 대한 정보입니다.
title: Adobe Target Recommendations에서 동적 및 정적 포함 규칙 사용
feature: criteria
mini-toc-levels: 3
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
translation-type: tm+mt
source-git-commit: 2d7435c420326a7eb1a59c95befa87b06c7614c8
workflow-type: tm+mt
source-wordcount: '2125'
ht-degree: 33%

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

동적 포함 규칙은 정적 포함 규칙보다 강력하며 더 나은 결과와 참여를 제공합니다. 다음 사항을 고려하십시오.

* 동적 포함 규칙은 사용자 프로필 매개 변수 또는 mbox 호출에서 특성을 일치시켜 권장 사항을 제공합니다.

   예를 들어 가장 방문 빈도가 높은 기준 권장 사항을 만든 다음 반환된 권장 사항 세트의 권장 사항을 사용자가 권장 사항이 표시되는 페이지에 액세스할 때 전달된 속성에 대해 실시간으로 필터링합니다.

* 정적 규칙을 사용하여 컬렉션 대신 권장 사항에 포함할 항목을 제한합니다.

* 필요한 만큼 동적 포함 규칙을 만들 수 있습니다. 포함 규칙들은 AND 연산자로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

동적 필터링에 사용할 수 있는 옵션은 다음과 같습니다.

#### 엔티티 속성 일치

잠재적 추천 항목 풀을 사용자가 상호 작용한 특정 항목과 비교하여 동적으로 필터링합니다.

예를 들어 다음 예제와 같이 현재 항목의 브랜드와 일치하는 항목만 권장합니다.

브랜드 랜딩 페이지의 mbox가 반환되는 `entity.brand=Nike`경우 Nike 제품만 반환되고 해당 페이지에 표시됩니다. 마찬가지로 아디다스 브랜드 랜딩 페이지에서 아디다스 제품만 반환됩니다. 이러한 유형의 동적 포함 규칙을 사용할 경우 사용자는 각 브랜드 이름에 맞게 컬렉션이나 정적 필터를 지정하는 대신 모든 브랜드 페이지에 걸쳐 관련 브랜드 결과를 반환하는 하나의 추천 규칙만 지정해야 합니다.

#### 프로필 속성 일치

사용자 프로필의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

크기 또는 [!UICONTROL 즐겨찾기] 브랜드와 같이 방문자의 프로필에 저장된 값과 일치하는 권장 사항을 표시하려면 프로필 속성 일치를 사용합니다.

다음 시나리오에서는 프로필 속성 일치를 사용할 수 [!UICONTROL 있는 방법을 보여줍니다].

* 안경을 판매하는 회사는 방문객이 가장 좋아하는 프레임 색상을 호두라고 저장합니다. 특정 방문자의 경우 &quot;호두&quot; 색상에 일치하는 안경 프레임만 반환하도록 권장 사항이 설정됩니다.
* 프로필 매개 변수는 방문자가 회사의 웹 사이트를 탐색할 때 방문자의 옷 크기(예: 작은, 보통 또는 큰)에 대해 정의할 수 있습니다. 해당 프로필 매개 변수와 일치하도록 권장 사항을 설정하고 사용자가 선호하는 옷 크기에만 해당하는 제품을 반환합니다.

자세한 예와 지침은 아래 [프로필 속성 일치 예를](#section_9873E2F22E094E479569D05AD5BB1D40) 참조하십시오.

#### 매개 변수 일치

요청(API 또는 mbox)의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

예를 들어 다음 예와 같이 &quot;업계&quot; 페이지 매개 변수 또는 장치 차원이나 지리적 위치 같은 기타 매개 변수와 일치하는 컨텐츠만 권장합니다.

* 화면 너비 및 높이에 대한 Mbox 매개 변수를 사용하여 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만을 권장할 수 있습니다.
* 지역 위치 매개 변수를 사용하여 겨울 동안 도구에 대한 권장 사항을 반환할 수 있습니다. 눈이 내리지 않는 지역은 눈이 내리는 곳으로 안내하는 눈이 내리는 사람을 미리 안내하는 것도 좋다.

>[!NOTE]
>
>2016년 10월 31일 이전에 활동이 생성된 경우 &quot;매개 변수 일치&quot; 필터를 사용하는 경우 활동이 배달되지 않습니다. 이 문제를 해결하려면 다음을 수행하십시오.
>
>* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
>* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
>* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.


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

### 예 3:방문자의 크기와 일치하는 옷 추천

예를 들어 방문자 프로필에 설정된 옷 크기와 일치하는 옷을 추천합니다.

제품 페이지는 mbox 호출 `entity.size` 을 전송합니다(아래 그림에서 빨간색 화살표).

방문자가 방문한 마지막 페이지에서 [프로필](/help/c-target/c-visitor-profile/profile-parameters.md) 속성과 값을 캡처하는 프로필 스크립트를 만들 수 있습니다.

예:

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

프로필 스크립트는 이름이 지정된 mbox의 `entity.size` 값을 캡처하고 이 값 `target-global-mbox` 을 프로필 속성 `user.size` (아래 그림에서 파란색 화살표)으로 반환합니다.

![mbox 호출 크기](/help/c-recommendations/c-algorithms/assets/size.png)

권장 사항 기준을 만들 때 필터링 규칙 [!UICONTROL 추가를]클릭한 다음 [!UICONTROL 프로필 속성 일치를 선택합니다].

![프로필 속성 일치 일러스트레이션](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

프로필을 불러온 `user.size` 경우 mbox 호출( [!DNL Target])에서 프로필 스크립트 이름(`size``user.size`)에 전달된 값과 일치하도록 규칙을 설정할 때 일치하는 항목을 찾기 위해 드롭다운에 표시됩니다.

그런 다음 프로필 속성 일치에 대해 &quot;user.size&quot;에 저장된 값/텍스트를 &quot;size&quot; &quot;equals&quot;를 선택할 수 있습니다.

프로필 속성 규칙이 빌드되면 방문자의 저장된 프로필 속성과 일치하지 않는 속성이 있는 모든 권장 사항을 필터링합니다.

### 예 4:크기에 따라 항목 추천

프로필 속성 일치가 권장 사항에 영향을 주는 방법에 대한 시각적 예를 보려면 팬을 판매하는 웹 사이트를 고려하십시오.

방문자가 이 웹 사이트에서 팬의 다양한 이미지를 클릭하면 각 페이지는 이미지의 팬 크기가 작은지 또는 큼인지에 따라 `entity.size` 매개 변수의 값을 설정합니다.

프로필 스크립트를 만들어 값 `entity.size` 이 작음 대 큼으로 설정된 횟수를 추적하고 카운트한다고 가정합니다.

이후 방문자가 홈 페이지로 돌아가는 경우 더 많은 소규모 팬 또는 큰 팬을 클릭했는지에 따라 필터링된 권장 사항이 표시됩니다.

Recommendations은 웹사이트에서 더 많은 작은 팬을 보는 것을 기준으로 합니다.

![소규모 팬 추천](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations은 웹사이트에서 더 많은 대규모 팬을 보는 것을 기준으로 합니다.

![대형 팬 추천](/help/c-recommendations/c-algorithms/assets/large-fans.png)

## 엔티티 속성 일치 예

[!UICONTROL 개체 속성 일치를] 사용하면 아래 예와 같이 사용자가 현재 보고 있는 항목의 속성과 일치하는 항목, 사용자가 가장 최근에 본 항목, 사용자가 가장 최근에 구입한 항목, 사용자가 가장 자주 본 항목 또는 방문자 프로필의 사용자 지정 속성에 저장된 항목에서 권장할 수 있습니다.

### 예제 5:더 비싼 제품으로 업셀링

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

### 예 6:비공개 레이블 제품 홍보

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
