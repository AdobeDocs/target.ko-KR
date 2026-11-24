---
keywords: 사용자 지정 디자인;속도;소수점;쉼표;디자인 사용자 지정
description: 오픈 소스 [!DNL Velocity] 디자인 언어를 사용하여 [!DNL Target] 권장 사항에서 권장 사항 디자인을 사용자 지정하는 방법을 알아봅니다.
title: Velocity를 사용하여 디자인 사용자 지정
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
TQID: 'https://experienceleague.adobe.com/cccBRfwqqn-eL2hraSDAoJHPYSCkcA9tVne3OWDXxEU'
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
source-git-commit: f9c9c7b2b78ec020fcabae420686b8955e350a0e
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 12%
---
# [!DNL Velocity]을(를) 사용하여 디자인 사용자 지정 {#customize-design}

>[!BEGINSHADEBOX]

**이 페이지에서:** 오픈 소스 [!DNL Velocity] 디자인 언어를 사용하여 [!DNL Adobe Target Recommendations]에서 추천 디자인을 사용자 지정하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

## [!DNL Velocity] 개요 {#velocity-overview}

[!DNL Velocity]에 대한 정보는 [https://velocity.apache.org](https://velocity.apache.org)에 있습니다.

모든 [!DNL Velocity] 논리, 구문 등을 권장 사항 디자인에 사용할 수 있습니다. 즉, *for* 루프, *if* 문 및 기타 코드는 JavaScript 대신 [!DNL Velocity]을(를) 사용하여 만들 수 있습니다.

`productPage` mbox 또는 CSV 업로드에서 [!DNL Recommendations]&#x200B;(으)로 전송된 엔터티 특성은 &quot;다중 값&quot; 특성을 제외하고 디자인에 표시할 수 있습니다. 모든 유형의 특성을 보낼 수 있지만, [!DNL Target]은(는) 형식이 &quot;multi-value&quot;인 특성을 디자인을 반복할 수 있는 배열로 전달하지 않습니다(예: `entityN.categoriesList`).

이러한 값은 다음 구문으로 참조합니다.

```
$entityN.variable
```

엔터티 특성 이름은 선행 *$* 문자 뒤에 [!DNL Velocity] 템플릿 언어(VTL) 식별자가 있는 [!DNL Velocity] 줄임 표기법을 따라야 합니다. VTL 식별자는 알파벳 문자(a-z 또는 A-Z)로 시작해야 합니다.

[!DNL Velocity] 엔터티 특성 이름은 다음 문자 유형으로 제한됩니다.

* 알파벳(a-z, A-Z)
* 숫자(0-9)
* 하이픈 ( - )
* 밑줄( _ )

다음 특성은 [!DNL Velocity] 배열로 사용할 수 있습니다. 따라서 인덱스를 통해 반복하거나 참조할 수 있습니다.

* `entities`
* `entityN.categoriesList`

예:

```
#foreach ($category in $entity1.categoriesList) 
<br/>$category 
#end
```

또는

```
#if ($entities[0].categoriesList.size() >= 3 ) 
$entities[0].categoriesList[2] 
#end
```

[!DNL Velocity] 변수(특성)에 대한 자세한 내용은 [Velocity 설명서](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables)를 참조하십시오.

디자인에서 프로필 스크립트를 사용하는 경우 스크립트 이름 앞에 있는 $는 `\`(백슬래시)로 이스케이프해야 합니다. 예:

`\${user.script_name}`

>[!NOTE]
>
>하드 코딩되거나 루프를 통해 디자인에서 참조할 수 있는 최대 개체 수는 99개입니다. 디자인 스크립트는 최대 65,000자를 포함할 수 있습니다.

다음 그림과 유사한 것을 표시하는 디자인입니다.

![사진, 이름, 가격, 등급 및 거리를 각각 보여 주는 4개의 항목이 있는 &quot;기타 재미있는 활동&quot;이라는 제목의 4 x 1 디자인의 예](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

은 다음 코드를 사용할 수 있습니다.

```
<table style="border:1px solid #CCCCCC;"> 
<tr> 
<td colspan="3" style="font-size: 130%; border-bottom:1px solid  
#CCCCCC;"> You May Also Like... </td> 
</tr> 
<tr> 
<td style="border-right:1px solid #CCCCCC;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity1.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity1.id</a></div> 
By $entity1.message <a href="?x14=brand;q14=$entity1.message"> 
(More)</a><br/> 
sku: $entity1.prodId<br/> Price: $$entity1.value 
<br/><br/> 
</div> 
</td> 
<td style="border-right:1px solid #CCCCCC; padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;">  
<div class="search_title"><a href="$entity2.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity2.id</a></div> 
By $entity2.message <a href="?x14=brand;q14=$entity2.message"> 
(More)</a><br/> 
sku: $entity2.prodId<br/> 
Price: $$entity2.value 
<br/><br/> 
</div> 
</td> 
<td style="padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity3.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity3.id</a></div> 
By $entity3.message <a href="?x14=brand;q14=$entity3.message"> 
(More)</a><br/> 
sku: $entity3.prodId<br/> Price: $$entity3.value 
<br/><br/> 
</div> 
</td> 
</tr>  
</table>
```

>[!NOTE]
>
>속성 값 뒤에 텍스트를 추가하려면 속성 이름이 끝났음을 나타내는 태그 앞에 형식 표기법을 사용하여 속성 이름을 묶습니다. 예: `${entity1.thumbnailUrl}.gif`.

`algorithm.name` 및 `algorithm.dayCount`은(는) 디자인에서 엔터티 특성으로 사용할 수도 있으므로 하나의 디자인을 사용하여 여러 기준을 테스트할 수 있으며 기준 이름을 디자인에 동적으로 표시할 수 있습니다. 이는 방문자가 &quot;최상위 판매자&quot; 또는 &quot;이 항목을 본 사용자가 구매한 항목&quot;을 보고 있음을 방문자에게 보여 줍니다. `dayCount`(기준에 사용된 데이터의 일 수(예: &quot;지난 2일 동안 최상위 판매자&quot;)도 표시할 수 있습니다.

## [!DNL Velocity] 디자인의 숫자 작업 {#numbers}

기본적으로 [!DNL Velocity] 디자인은 모든 엔터티 특성을 문자열 값으로 처리합니다. 엔티티 속성은 수학 연산을 수행하거나 다른 숫자 값과 비교하기 위해 숫자 값으로 처리되어야 할 수 있습니다. 엔티티 속성을 숫자 값으로 처리하려면 다음 단계를 수행합니다.

1. 더미 변수를 선언하고 임의의 정수 또는 이중 값으로 초기화합니다.
1. 사용할 엔터티 특성이 비어 있지 않은지 확인합니다([!DNL Target Recommendations]의 디자인 파서가 디자인을 확인하고 저장하는 데 필요).
1. 1단계에서 만든 더미 변수의 `parseInt` 또는 `parseDouble` 메서드에 엔터티 특성을 전달하여 문자열을 정수 또는 이중 값으로 변환합니다.
1. 새 숫자 값에 대한 연산 또는 비교를 수행합니다.

### 예: 할인 가격 계산

품목의 표시 가격을 $0.99로 낮추어 할인을 적용하려면 다음 방법을 사용할 수 있습니다.

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### 예: 항목 등급에 따라 표시할 별 수 선택

품목의 수치 평균 고객 등급에 따라 적절한 수의 별표를 표시하려면 다음 접근 방법을 사용할 수 있습니다.

```
#set( $double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $double.parseDouble($entity1.get('rating')) )
    #if( $rating >= 4.5 )
        <img src="5_stars.jpg">
    #elseif( $rating >= 3.5 )
        <img src="4_stars.jpg">
    #elseif( $rating >= 2.5 )
        <img src="3_stars.jpg">
    #elseif( $rating >= 1.5 )
        <img src="2_stars.jpg">
    #else
        <img src="1_star.jpg">
    #end
#else
    <img src="no_rating_default.jpg">
#end
```

### 예: 항목의 길이를 분 단위로 기반으로 시간(시, 분) 계산

길이가 분 단위로 저장될 때 동영상 길이를 시간 및 분 단위로 표시하려면 다음 방법을 사용할 수 있습니다.

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## 추천 제품에 키 항목 표시 {#key-item}

디자인은 다른 권장 제품과 함께 키 항목을 표시할 수 있습니다. 예를 들어 현재 항목을 권장 사항 옆에 참조용으로 표시할 수 있습니다.

이렇게 하려면 `$entity` 특성 대신 권장 사항의 기반이 되는 `$key` 특성을 사용하는 열을 디자인에 만드십시오. 예를 들어 키 열의 코드는 다음과 같습니다.

```
<div class="at-table-column"> 
   <a href="$key.pageURL"> 
      <img src=$key.thumbnailUrl" class="at-thumbnail"/> 
      <br/><h3>$key.name</h3> 
      <br/><p class="at-light">$key.message</p> 
      <br/><p class="at-light">$key.value</p> 
   </a> 
</div>
```

결과는 다음과 같은 디자인입니다. 여기서는 한 열에 키 항목이 표시됩니다.

![열이 4개인 디자인입니다. 첫 번째 열에는 현재 제품으로 표시된 키 항목이 표시됩니다.](/help/main/c-recommendations/c-design-overview/assets/rec_key.png)

[!DNL Recommendations] 활동을 만들 때, &quot;마지막으로 구매한 항목&quot;과 같은 방문자의 프로필에서 키 항목을 가져오는 경우 [!DNL Target]은(는) **[!UICONTROL 시각적 경험 작성기]**(VEC)에 임의의 제품을 표시합니다. 활동을 디자인하는 동안에는 프로필을 사용할 수 없기 때문입니다. 방문자가 페이지를 볼 때 예상 키 항목이 표시됩니다.

## 문자열 값에서 대체 수행 {#replacements}

디자인은 문자열 내의 값을 대체할 수 있습니다. 예를 들어 미국에서 사용되는 소수점 구분 기호는 유럽 및 기타 국가에서 사용되는 쉼표 구분 기호로 대체할 수 있습니다.

다음 코드는 조건부 판매 가격 책정 예제의 한 줄을 보여 줍니다.

```
<span class="price">$entity1.value.replace(".", ",") &euro;</span><br>
```

다음 코드는 판매 가격에 대한 완전한 조건부 예제입니다.

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") &euro;</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") &euro;<br> #else 
    <span class="price">$entity1.value.replace(".", ",") &euro;</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
</div>
```

## 디자인 크기 사용자 지정 및 빈 값 확인 {#default}

[!DNL Velocity] 스크립트는 엔터티 표시의 동적 크기 조정을 제어할 수 있습니다. 다음 디자인은 [!DNL Recommendations]에서 일치하는 엔터티가 충분히 반환되지 않을 때 빈 HTML 요소를 만들지 않도록 일대다 결과를 수용합니다. 이 스크립트는 백업 권장 사항이 적합하지 않고 **[!UICONTROL 부분 디자인 렌더링]**&#x200B;이 활성화되어 있는 시나리오에 가장 적합합니다.

다음 HTML 코드 조각은 4x2 기본 디자인에서 기존 HTML 부분을 대체합니다(간결성을 위해 CSS가 여기에 포함되지 않음).

* 다섯 번째 엔티티가 존재하는 경우 스크립트는 닫는 div를 삽입하고 `<div class="at-table-row">`가 포함된 새 행을 엽니다.
* 4x2를 사용하면 표시되는 최대 결과 수는 8개이지만 `$count <=8`을(를) 수정하여 더 작거나 더 큰 목록을 사용자 지정할 수 있습니다.
* 로직은 여러 행의 엔티티 균형을 맞추지 않습니다. 예를 들어 5개 또는 6개의 엔티티를 표시하려는 경우 동적으로 맨 위에 3개, 맨 아래에 2개(또는 맨 위에 3개, 맨 아래에 3개)가 되지 않습니다. 맨 위 행에는 두 번째 행을 시작하기 전에 네 개의 항목이 표시됩니다.

```
<div class="at-table">
  <div class="at-table-row">
    #set($count=1) 
    #foreach($e in $entities)  
        #if($e.id != "" && $count < $entities.size() && $count <=8) 
            #if($count==5) 
                </div>
                <div class="at-table-row">
            #end
            <div class="at-table-column">
                <a href="$e.pageUrl"><img src="$e.thumbnailUrl" class="at-thumbnail" />
                    <br/>
                    <h3>$e.name</h3>
                    <br/>
                    <p class="at-light">$e.message</p>
                    <br/>
                    <p class="at-light">$$e.value</p>
                </a>
            </div>
            #set($count = $count + 1) 
        #end 
    #end
  </div>
</div>
```
