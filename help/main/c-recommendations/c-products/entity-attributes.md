---
keywords: 엔티티;엔티티 속성;Recommendations로 정보 전달;행동 데이터;데이터 카운터;상대 URL 정의;재고 수준 표시;가격 정의;수익 마진 정의;사용자 지정 속성
description: 엔터티 특성을 사용하여 제품 또는 콘텐츠 정보를  [!DNL Target] Recommendations에 전달하는 방법을 알아봅니다.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
title: 엔티티 속성은 어떻게 사용합니까?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: b6697eee5925cb8fa3b2fa2e107af0c617d30f94
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 48%

---

# 엔티티 속성

엔터티 특성을 사용하여 제품 또는 콘텐츠 정보를 [!DNL Adobe Target Recommendations]에 전달합니다.

엔티티는 추천할 항목을 나타냅니다. 엔티티에는 제품, 콘텐츠(문서, 슬라이드쇼, 이미지, 동영상 및 TV 프로그램), 구인 및 구직 정보, 식당 등이 포함될 수 있습니다.

[!DNL Recommendations]이(가) 알고리즘에 사용되는 `productId` 또는 `productPurchasedId`(코드에서는 `entity.id`이라고 함)을(를) 보냅니다.

다음 사항을 고려하십시오.

* `entity.id`은(는) 주문 확인 페이지에 전송된 `productPurchasedId`과(와) [!DNL Adobe Analytics] 제품 보고서에 사용된 `productId`과(와) 일치해야 합니다.
* [!DNL Recommendations]에 전달하는 엔터티 특성 값은 61일 후에 만료됩니다. Adobe은 카탈로그의 각 항목에 대해 매월 최소 한 번씩 각 엔터티 특성의 최신 값을 [!DNL Recommendations]에 전달하는 것을 권장합니다.

대부분의 사전 정의된 매개 변수는 단일 값만 허용하며 새 값이 이전 값을 덮어씁니다. `categoryId` 매개 변수에는 해당 제품을 포함하는 각 카테고리의 쉼표 구분 값 목록이 사용됩니다. 새 `categoryId` 값이 기존 값을 덮어쓰지 않지만, 대신 엔티티 업데이트(250자 제한) 중에 첨부됩니다.

일반적으로 at.js 1을 사용하는 경우 표시 정보 mbox는 다음 예와 비슷합니다.*x*(`mboxCreate` 포함). 모든 엔티티 매개 변수 속성은 대소문자를 구분합니다.

>[!NOTE]
>
>at.js 2를 사용 중인 경우 입니다.*x*, `mboxCreate`(다음 예제에서 사용됨)은 더 이상 지원되지 않습니다. at.js 2를 사용하여 [!DNL Recommendations]에 제품 또는 콘텐츠 정보를 전달합니다.*x*, [targetPageParams](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html){target=_blank}을(를) 사용합니다. 예를 들어 [Recommendations 계획 및 구현](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}을 참조하세요.

```javascript
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=/help/baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=/help/baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>권장 사항은 사이트의 모든 환경에서 전송되는 데이터를 수신하므로 `pageUrl` 및 `thumbnailUrl`에는 절대 URL보다 상대 URL이 선호됩니다. 상대 URL을 사용하면 스테이징 서버나 개발 서버에 대한 하드코딩된 링크가 사용되지 않습니다.

mbox가 제품 페이지에 있는 경우, 제품 ID와 카테고리 ID를 모두 포함시킬 수 있습니다. 선택한 알고리즘에 따라 표시되는 내용이 결정됩니다. 제품 ID는 친화성 알고리즘에 사용되고 카테고리 ID는 카테고리 알고리즘에 사용됩니다.

## 사용 가능한 변수

다음 목록에서는 사용 가능한 변수를 설명합니다.

### entity.id

Singe 값만 사용합니다.

이 필수 매개 변수는 제품을 식별합니다. 항목을 인식하고 그에 대한 데이터를 공유하려면 다양한 제품에 사용된 모든 [!DNL Adobe Experience Cloud] 제품([!DNL Analytics] 포함)에서 이 영숫자 ID가 동일해야 합니다.

`entity.id` 값은 REST API 호출에 전달될 때 URL 인코딩이 필요한 공백, 슬래시, 앰퍼샌드, 물음표, 백분율 기호, 쉼표 또는 기타 구두점 문자를 포함하지 *않아야*&#x200B;합니다. 하이픈 및 밑줄을 사용할 수 있습니다. `entity.id` 값에 올바르지 않은 구두점을 포함하면 일부 [!DNL Recommendations] 기능에 오류가 발생합니다.

예: `'entity.id=67833'`

### entity.name

단일 값만 가능합니다.

제품이 권장될 때 웹 사이트에 표시되는 제품 이름

예: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

다중 값(쉼표로 구분된 목록)을 지원합니다.

현재 페이지의 카테고리. entity.categoryID에는 카디건 하위 섹션(예: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`)과 같은 여러 범주가 포함될 수 있습니다. 여러 카테고리는 쉼표로 구분해야 합니다.

`categoryId` 값은 250자로 제한됩니다.

>[!NOTE]
>
>카테고리를 기반으로 한 권장 사항을 [!UICONTROL Category] 페이지에 표시하기 위해 한 개의 `categoryId`만 특정 권장 사항을 표시하는 데 사용되는 mbox에 전달할 수 있습니다. `categoryId` 값은 [!UICONTROL Product Detail] 페이지에서 전달된 `entity.categoryId` 값과 정확히 일치해야 합니다.

예:

* 제품 세부 정보 페이지 예: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`
* 예제 범주 페이지 스웨터: `womens:sweaters`
* 예제 카테고리 페이지 가디건: `womens:sweaters:cardigans`

카테고리 기반 권장 사항의 경우 쉼표로 카테고리 값을 구분합니다. 쉼표로 구분되는 모든 값은 카테고리가 됩니다. 콜론(:)과 같은 기타 구분 기호를 사용하여 카테고리 값 내의 하위 카테고리를 구분하도록 정의할 수도 있습니다.

예를 들어 다음 코드에서 여성의 카테고리는 여러 하위 카테고리로 나뉩니다.

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...', );
```

mbox 배달의 경우 키에 가장 긴 속성 이름이 사용됩니다. 연결이 있는 경우 마지막 속성이 사용됩니다. 위의 예에서 범주 키는 `Womens:Outerwear:Jackets:Caban`입니다.

### entity.brand

단일 값만 가능합니다.

항목의 브랜드 이름을 표시합니다.

예: `'entity.brand=brandxyz'`

### entity.pageUrl

단일 값만 가능합니다.

항목을 구입할 수 있는 페이지의 상대 URL을 정의합니다.

예: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### entity.thumbnailUrl

단일 값만 가능합니다.

항목과 함께 표시되는 썸네일 이미지에 대한 상대 URL을 정의합니다.

예: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### entity.message

단일 값만 가능합니다.

권장 사항에 표시되는 제품에 대한 메시지(예: &quot;판매 중&quot; 또는 &quot;세일&quot;)입니다. 메시지는 일반적으로 제품 이름보다 더 자세합니다. 템플릿에 제품과 함께 표시할 추가 정보를 정의하려면 entity.message를 사용합니다.

예: `'entity.message=Family&nbsp;special'`

### entity.inventory

단일 값만 가능합니다. 정수 또는 long 값이 필요합니다.

항목의 재고 수준을 표시합니다.

예: `'entity.inventory=1'`

**빈 재고 특성 처리:** 배달을 위해 포함 규칙, 컬렉션 규칙 또는 기준 설정이 `entity.inventory` > 0 또는 `entity.inventory` = 0이고 제품에 재고가 설정되어 있지 않은 경우 [!DNL Target]에서 이 값을 TRUE로 평가하고 재고가 설정되지 않은 제품을 포함합니다. 따라서 재고가 설정되지 않은 제품은 추천 결과에 표시됩니다.

마찬가지로, 글로벌 제외 규칙이 `entity.inventory` = 0으로 설정되어 있고 `entity.inventory`가 설정되지 않은 경우 [!DNL Target]은 이 규칙을 TRUE로 평가하고 제품을 제외합니다.

**알려진 문제:** 제품 검색이 설정되지 않은 재고 값 특성에 대한 게재와 일치하지 않습니다. 예를 들어, `entity.inventory` = 0인 규칙의 경우, 제품 검색 결과에 재고 값이 설정되지 않은 제품이 표시되지 않습니다.

### entity.value

단일 값만 가능합니다.

항목의 가격 또는 값을 정의합니다.

예: `'entity.value=15.99'`

entity.value는 십진수 형식만 지원합니다(예: 15.99). 쉼표 형식(15,99)은 지원되지 않습니다.

### entity.margin

단일 값만 가능합니다.

항목의 이윤 폭 또는 다른 가치

예: `'entity.margin=1.00'`

### 엔티티.*사용자 지정*

다중 값(JSON 배열)을 지원합니다.

항목에 대한 추가 정보를 제공하는 최대 100개의 사용자 지정 변수를 정의합니다. 각 사용자 지정 속성에 대해 미사용 속성 이름을 지정할 수 있습니다. 예를들어, `entity.genre`(이)라는 사용자 지정 특성을 만들어 책 또는 동영상을 정의할 수 있습니다. 티켓 공급업체는 스포츠 경기의 원정 팀이나 콘서트의 서막 같이, 보조 참여자를 위한 이벤트 장소에 대한 속성을 만들 수 있습니다.

제한 사항:

* 사용자 지정 엔티티 속성에는 사전 정의된 엔티티 속성 이름을 사용할 수 없습니다. 
* entity.environment 속성은 시스템에 의해 예약되어 있으므로 사용자 지정 엔티티 속성에 사용할 수 없습니다. targetPageParams, 피드 또는 API를 사용하여 entity.environment를 전달하려고 하면 무시됩니다.

예:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

사용자 지정 엔티티 속성은 다중 값을 지원합니다. 문자 및 값 제한에 대해서는 [사용자 지정 엔티티 속성](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits)을 참조하십시오.

예: `'entity.secondary=["band1",&nbsp;"band2"]'`

다중 값 사용자 지정 엔티티 속성에는 유효한 JSON 배열이 필요합니다. 올바른 구문 정보는 [사용자 지정 엔터티 특성](/help/main/c-recommendations/c-products/custom-entity-attributes.md)을 참조하십시오.

### entity.event.detailsOnly

단일 값만 가능합니다.

mbox 호출이 알고리즘에 대한 행동 데이터 카운터를 증분하지 못하게 하는 데 사용됩니다.

예: `'entity.event.detailsOnly=true'`

아래 예에서 첫 번째 mbox 호출은 카탈로그 및 동작 데이터를 업데이트합니다. 두 번째 mbox 호출은 카탈로그만 업데이트합니다.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [사용자 지정 엔티티 속성](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
