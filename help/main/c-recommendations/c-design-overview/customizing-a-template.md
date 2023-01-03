---
keywords: 사용자 지정 디자인;속도;소수점;쉼표;디자인 사용자 지정
description: 오픈 소스 Velocity 디자인 언어를 사용하여 Adobe에서 권장 사항 디자인을 사용자 지정하는 방법을 알아봅니다 [!DNL Target] Recommendations.
title: Velocity를 사용하여 디자인을 사용자 지정하려면 어떻게 합니까?
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
source-git-commit: e93747d07b980aa29a8985c3872fd704d520e0cd
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 46%

---

# ![PREMIUM](/help/main/assets/premium.png) Velocity를 사용하여 디자인 사용자 지정

공개 소스인 Velocity 디자인 언어를 사용하여 권장 사항 디자인을 사용자 지정할 수 있습니다 [!DNL Adobe Target Recommendations].

## 속도 개요 {#section_C431ACA940BC4210954C7AEFF6D03EA5}

Velocity에 대한 정보는 [](https://velocity.apache.org)https://velocity.apache.org에서 알 수 있습니다.

모든 Velocity 로직, 구문 등을 권장 사항 디자인에 사용할 수 있습니다. 이것은 JavaScript가 아닌 Velocity를 사용하여 *for* 루프, *if* 구문 및 기타 코드를 만들 수 있음을 의미합니다.

에 보낸 엔티티 속성 [!DNL Recommendations] 에서 `productPage` mbox 또는 CSV 업로드는 &quot;다중 값&quot; 속성을 제외하고 디자인에 표시할 수 있습니다. 모든 유형의 속성을 전송할 수 있습니다. 하지만 [!DNL Target] 에서는 &quot;multi-value&quot; 유형의 속성을 템플릿을 반복할 수 있는 배열로 전달하지 않습니다(예: `entityN.categoriesList`).

이러한 값은 다음 구문으로 참조합니다.

```
$entityN.variable
```

엔티티 속성 이름은 선행 표기법으로 구성된 속도 축약법을 따라야 합니다 *$* 문자 뒤에 VTL(Velocity Template Language) 식별자가 옵니다. VTL 식별자는 알파벳 문자(a-z 또는 A-Z)로 시작해야 합니다.

속도 엔티티 속성 이름은 다음 유형의 문자로 제한됩니다.

* 알파벳(a-z, A-Z)
* 숫자(0-9)
* 하이픈 ( - )
* 밑줄( _ )

다음 속성은 Velocity 배열로 사용할 수 있습니다. 따라서 색인을 통해 반복하거나 참조할 수도 있습니다.

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

Velocity 변수(특성)에 대한 자세한 내용은 [https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

디자인에서 프로필 스크립트를 사용하는 경우, 스크립트 이름 앞에 있는 $는 \으로 이스케이프 처리해야 합니다. 예, `\${user.script_name}`.

>[!NOTE]
>
>하드 코딩되거나 루프를 통해 디자인에서 참조할 수 있는 최대 개체 수는 99개입니다. 템플릿 스크립트 길이는 최대 65,000자까지 포함할 수 있습니다.

예를 들어 다음과 유사한 내용을 표시하는 디자인을 원하는 경우,

![velocity_example 이미지](assets/velocity_example.png)

다음 코드를 사용할 수 있습니다.

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
>속성 이름을 나타내는 태그 앞에 속성 값 뒤에 텍스트를 추가하려는 경우 공식 표기법을 사용하여 속성 이름을 묶을 수 있습니다. 예: `${entity1.thumbnailUrl}.gif`.

를 사용할 수도 있습니다 `algorithm.name` 및 `algorithm.dayCount` 디자인에서 엔티티 속성으로, 하나의 디자인을 사용하여 여러 기준을 테스트하고 기준 이름을 디자인에 동적으로 표시할 수 있습니다. 이는 방문자에게 자신이 &quot;최상위 판매자&quot; 또는 &quot;이 항목을 본 사용자가 구매한 항목&quot;을 검토 중임을 보여줍니다. 이러한 속성을 사용하여 `dayCount` (지난 2일 동안 최상위 판매자 등과 같이 기준에 사용된 데이터의 일 수)

## Velocity 템플릿에서 숫자 작업

기본적으로 속도 템플릿은 모든 엔티티 속성을 문자열 값으로 처리합니다. 수학 작업을 수행하거나 다른 숫자 값과 비교하기 위해 엔티티 속성을 숫자 값으로 처리할 수 있습니다. 엔티티 속성을 숫자 값으로 처리하려면 다음 단계를 수행합니다.

1. 더미 변수를 선언하고 임의의 정수 또는 double 값으로 초기화합니다.
1. 사용하려는 엔티티 속성이 비어 있지 않은지 확인합니다(에 필요) [!DNL Target Recommendations]&#39; 템플릿 구문 분석기를 사용하여 템플릿을 확인하고 저장합니다.)
1. 엔티티 속성을에 전달 `parseInt` 또는 `parseDouble` 1단계에서 만든 더미 변수의 메서드를 사용하여 문자열을 정수 또는 double 값으로 변환합니다.
1. 새 숫자 값에 대해 수학 연산을 수행하거나 비교를 수행합니다.

### 예: 할인 가격 계산

할인을 적용하려면 품목의 표시된 가격을 $0.99만큼 줄이려고 한다고 가정합니다. 다음 접근 방식을 사용하여 이 결과를 얻을 수 있습니다.

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### 예: 항목의 등급에 따라 표시할 별 수 선택

항목의 평균 고객 등급에 따라 적절한 수의 별 수를 표시한다고 가정합니다. 다음 접근 방식을 사용하여 이 결과를 얻을 수 있습니다.

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

### 예: 항목의 길이(분)를 기반으로 시간 및 분 단위 계산

동영상 길이를 분 단위로 저장하지만 시간 및 분 단위로 표시하려고 한다고 가정합니다. 다음 접근 방식을 사용하여 이 결과를 얻을 수 있습니다.

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## 추천 제품에 키 항목 표시 {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

다른 추천 제품과 함께 키 항목을 표시하도록 디자인을 수정할 수 있습니다. 예를 들어, 권장 사항 항목 옆에 참조할 수 있도록 현재 항목을 표시할 수 있습니다.

이렇게 하려면 `$entity` 속성이 아니라, 권장 사항의 기반이 되는 `$key` 속성을 사용하는 열을 디자인에 작성하십시오. 예를 들어, 키 열용 코드는 다음과 같습니다.

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

![rec_key 이미지](assets/rec_key.png)

[!DNL Recommendations] 활동을 만들 때, &quot;마지막으로 구매한 항목&quot;과 같은 방문자 프로필에서 키 항목을 가져오는 경우 [!DNL Target]에는 [!UICONTROL 시각적 경험 작성기] (VEC)에 무작위 제품이 표시됩니다. 이것은 활동을 설계하는 동안에는 프로필을 사용할 수 없기 때문입니다. 방문자가 페이지를 볼 때에는 예상되는 키 항목이 표시됩니다.

## 문자열 값에서 대체 수행 {#section_01F8C993C79F42978ED00E39956FA8CA}

디자인을 수정하여 문자열 내의 값을 바꿀 수 있습니다. 예를 들어, 미국에서 사용되는 소수점 구분 기호를 유럽 및 기타 국가에서 사용되는 쉼표 구분 기호로 바꿉니다.

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
```

## 템플릿 크기 사용자 지정 및 빈 값 확인 {#default}

다음 템플릿은 속도 스크립트를 사용하여 엔티티 디스플레이의 동적 크기 조정을 제어하므로, [!DNL Recommendations]에서 반환된 일치하는 엔티티가 충분하지 않은 경우 빈 HTML 요소를 생성하지 않도록 일대다 결과를 사용합니다. 이 스크립트는 백업 권장 사항이 적합하지 않고 [!UICONTROL 부분 템플릿 렌더링]이 활성화되어 있는 시나리오에 가장 적합합니다.

다음 HTML 코드 조각은 4x2 기본 디자인에서 기존 HTML 부분을 대체합니다(간결성을 위해 CSS가 여기에 포함되지 않음).

* 다섯 번째 엔티티가 존재하는 경우 스크립트는 닫는 div를 삽입하고 `<div class="at-table-row">`가 포함된 새 행을 엽니다.
* 4x2를 사용하면 표시되는 최대 결과는 8이지만, 이 경우 `$count <=8`을 수정하여 더 작거나 더 큰 목록을 사용자 지정할 수 있습니다.
* 로직이 여러 행에 엔티티의 균형을 맞추지 않습니다. 예를 들어 5개 또는 6개의 엔티티를 표시하려는 경우 동적으로 맨 위에 3개, 맨 아래에 2개(또는 맨 위에 3개, 맨 아래에 3개)가 되지 않습니다. 상단 행에는 두 번째 행이 시작되기 전에 네 개의 항목이 표시됩니다.

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
