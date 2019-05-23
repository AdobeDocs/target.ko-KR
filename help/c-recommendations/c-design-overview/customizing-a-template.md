---
description: 공개 소스인 Velocity 디자인 언어를 사용하여 권장 사항 디자인을 사용자 지정할 수 있습니다.
keywords: 사용자 지정 디자인;속도;소수점;쉼표;디자인 사용자 지정
seo-description: 공개 소스인 Velocity 디자인 언어를 사용하여 권장 사항 디자인을 사용자 지정할 수 있습니다.
seo-title: Velocity를 사용하여 디자인 사용자 지정
solution: Target
title: Velocity를 사용하여 디자인 사용자 지정
title-outputclass: premium
topic: Premium
uuid: 80701a15-c5eb-4089-a92e-117eda11faa2
badge: premium
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

---


# ![PREMIUM](/help/assets/premium.png) Velocity를 사용하여 디자인 사용자 지정{#customize-a-design-using-velocity}

공개 소스인 Velocity 디자인 언어를 사용하여 권장 사항 디자인을 사용자 지정할 수 있습니다.

## 속도 개요 {#section_C431ACA940BC4210954C7AEFF6D03EA5}

Velocity에 대한 정보는 [](https://velocity.apache.org)https://velocity.apache.org에서 알 수 있습니다.

모든 Velocity 로직, 구문 등을 권장 사항 디자인에 사용할 수 있습니다. 이것은 JavaScript가 아닌 Velocity를 사용하여 *for* 루프, *if* 구문 및 기타 코드를 만들 수 있음을 의미합니다.

`productPage` mbox나 CSV 업로드에서 [!DNL Recommendations]로 보내지는 모든 변수는 디자인에 표시할 수 있습니다. 이러한 값은 다음 구문으로 참조합니다.

```
$entityN.variable
```

변수 이름은 선행 *$* 문자, VTL(Velocity 템플릿 언어) 식별자로 구성되는 Velocity 축약 표기법을 따라야 합니다. VTL 식별자는 알파벳 문자(a-z 또는 A-Z)로 시작해야 합니다.

Velocity 변수 이름은 다음 유형의 문자로 제한됩니다.

* 알파벳(a-z, A-Z)
* 숫자(0-9)
* 하이픈(-)
* 밑줄( _ )

다음 변수는 Velocity 배열로 사용할 수 있습니다. 따라서 색인을 통해 반복하거나 참조할 수도 있습니다.

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

Velocity 변수에 대한 자세한 내용은 [https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables)를 참조하십시오.

디자인에서 프로필 스크립트를 사용하는 경우, 스크립트 이름 앞에 있는 $는 \으로 이스케이프 처리해야 합니다. 예, `\${user.script_name}`.

>[!NOTE]
>
>하드 코딩되거나 루프를 통해 디자인에서 참조할 수 있는 최대 개체 수는 99개입니다. 템플릿 스크립트 길이는 최대 65,000자까지 포함할 수 있습니다.

예를 들어 다음과 유사한 내용을 표시하는 디자인을 원하는 경우,

![](assets/velocity_example.png)

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

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>변수값 뒤에 정보를 추가하려는 경우 공식 표기법을 사용할 수 있습니다. 예: `${entity1.thumbnailUrl}.gif`.

사용자는 또한 디자인에서 `algorithm.name` 및 `algorithm.dayCount`를 변수로 사용할 수 있으며, 하나의 디자인을 사용해서 여러 기준을 테스트하고 해당 기준 이름을 디자인에 동적으로 표시할 수 있습니다. 이는 방문자에게 자신이 &quot;최상위 판매자&quot; 또는 &quot;이 항목을 본 사용자가 구매한 항목&quot;을 검토 중임을 보여줍니다. 이러한 변수를 사용해서 `dayCount`(&quot;지난 2일 동안 최상위 판매자&quot; 등과 같이 기준에 사용된 데이터의 일 수)를 표시할 수도 있습니다.

## 시나리오: 추천 제품에 키 항목 표시 {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

다른 추천 제품과 함께 키 항목을 표시하도록 디자인을 수정할 수 있습니다. 예를 들어, 권장 사항 항목 옆에 참조할 수 있도록 현재 항목을 표시할 수 있습니다.

이렇게 하려면 `$entity` 속성이 아니라, 추천의 기반이 되는 `$key` 속성을 사용하는 열을 디자인에 작성하십시오. 예를 들어, 키 열용 코드는 다음과 같습니다.

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

![](assets/rec_key.png)

[!DNL Recommendations] 활동을 만들 때, &quot;마지막으로 구매한 항목&quot;과 같은 방문자 프로필에서 키 항목을 가져오는 경우 [!DNL Target]에는 [!UICONTROL 시각적 경험 작성기](VEC)에 무작위 제품이 표시됩니다. 이것은 활동을 설계하는 동안에는 프로필을 사용할 수 없기 때문입니다. 방문자가 페이지를 볼 때에는 예상되는 키 항목이 표시됩니다.

## 시나리오: 판매 가격의 소수점을 쉼표 구분 기호로 바꾸기 {#section_01F8C993C79F42978ED00E39956FA8CA}

미국에서 사용되는 소수점 구분 기호를 유럽 및 기타 국가에서 사용되는 쉼표 구분 기호로 바꾸도록 디자인을 수정할 수 있습니다.

다음 코드는 조건부 판매 가격 책정 예제의 한 줄을 보여 줍니다.

```
<span class="price">$entity1.value.replace(".", ",") €</span><br>
```

다음 코드는 판매 가격에 대한 완전한 조건부 예제입니다.

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") €</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") €<br> #else 
    <span class="price">$entity1.value.replace(".", ",") €</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
```

