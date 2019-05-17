---
description: 권장 사항 활동에 대한 FAQ 목록
keywords: 문제 해결;자주 묻는 질문;FAQ;FAQ;권장 사항;특수 문자;속성 가중치;컨텐츠 유사성
seo-description: 권장 사항 활동에 대한 FAQ 목록
seo-title: 권장 사항 FAQ
solution: Target
title: 권장 사항 FAQ
title-outputclass: premium
topic: Premium
uuid: 27752811-0ffe-4d60-83d1-39e18b1953d5
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) 권장 사항 FAQ{#recommendations-faq}

권장 사항 활동에 대한 FAQ 목록

## 특수 문자가 배열을 깨는 경우 어떻게 해야 합니까? {#section_D27214116EE443638A60887C7D1C534E}

Javascript에서 이스케이프 처리된 값을 사용하십시오. 따옴표(&quot;)는 배열을 깰 수 있습니다. 다음 코드 조각은 이스케이프 처리된 값의 예입니다.

```
#set($String='') 
#set($escaper=$String.class.forName('org.apache.commons.lang.StringEscapeUtils')) 
<script type="text/javascript"> 
console.log("$escaper.escapeJavaScript($entity1.name)") 
console.log("$escaper.escapeJavaScript($entity2.name)") 
console.log('$escaper.escapeJavaScript($entity3.name)') 
names.push("$escaper.escapeJavaScript($entity4.name)") 
</script>
```

## 권장 사항 활동을 만들 때 사용자 지정 기준을 포함한 일부 기준을 선택할 수 없는 이유는 무엇입니까? {#section_B2265AC8B8A94E0298D495A05C5D817F}

사용 가능한 기준은 현재 카테고리를 기반으로 합니다. 권장 사항 오퍼를 만드는 경우 알고리즘 선택기는 카테고리 ID를 기반으로 기준을 표시합니다.

이 기준을 적용하는 위치에 카테고리 ID가 없을 경우 알고리즘 선택기에서 특정 기준을 사용할 수 없습니다.

mbox에 카테고리 ID가 있는 위치를 사용하는 경우 기준 선택기는 적용 가능한 모든 기준을 포함합니다.

Target에는 알고리즘 선택기의 지능적 필터링을 제어하는 [호환되지 않는 기준 필터링](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) 설정이 있습니다.

>[!NOTE]
>
>이 설정은 시각적 경험 작성기(VEC)에서 만들어진 활동에만 적용되고, 양식 기반 경험 작성기에서 만들어진 활동에는 적용되지 않습니다(Target에는 위치 컨텍스트가 없습니다.).

[!UICONTROL 호환되지 않는 기준 필터링] 설정에 액세스하려면 [!UICONTROL 권장 사항] &gt; [!UICONTROL 설정]을 클릭하십시오.

![](assets/recs_settings_filter.png)

[!UICONTROL 호환되지 않는 기준 필터링] 설정이 활성화되어 있지 않으면 Target이 알고리즘 선택기에서 알고리즘을 필터링하지 않으며 모든 알고리즘이 표시됩니다.

[!UICONTROL 호환되지 않는 기준 필터링] 설정이 활성화되어 있으면 VEC 활동에서 Target은 선택한 위치로부터 entityId와 카테고리 ID를 읽은 다음 `currentItem|currentCategory`(각각의 값이 해당 위치에 있는 경우)를 기반으로 알고리즘을 표시합니다. 따라서 기본적으로 알고리즘 선택기에는 선택한 위치를 위한 호환되는 알고리즘만 표시됩니다.

[!UICONTROL 호환되지 않는 기준 필터링] 설정이 활성화되어 있으면 기준을 선택하는 동안 [!UICONTROL 호환] 확인란을 선택 취소하여 비호환 알고리즘을 계속 볼 수 있습니다.

![](assets/compatible_checkbox.png)

Target에서 [!UICONTROL 호환] 확인란이 표시되지 않는 특수한 경우는 아래와 같습니다.

* entityId와 카테고리 ID가 모두 해당 위치에 있으며 아무것도 필터링되지 않는 경우
* [!DNL mbox.js] 버전 55 이하를 사용하는 경우
* 페이지에서 mbox 호출이 실행되지 않는 경우(!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalMbox).
* Target 매개 변수가 정의되지 않은 경우

## 권장 사항의 컬렉션이 0(영)이 되는 경우 어떻게 해야 합니까? {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

이전에 0이 아니었던 컬렉션이 0이 된 것으로 표시되면 다음 정보를 고려하십시오.

* 컬렉션을 다시 저장하고 번호가 업데이트되는지 확인할 수 있습니다. 다시 저장하면 컬렉션이 해당 컬렉션을 사용하는 모든 알고리즘을 다시 실행합니다.
* 올바른 환경을 보고 있습니까? [!DNL /target/products.html#recsSettings]로 이동하여 아래와 같이 다시 확인합니다.

   ![](assets/product_catalog.png)

* 색인이 최신 상태입니까? [!DNL /target/products.html#productSearch]로 이동하여 색인이 몇 시간 경과되었는지 확인합니다(예를 들어, &quot;색인화된 후 3시간 경과&quot;). 필요에 따라 색인을 새로 고칠 수 있습니다.
* 엔티티가 더 이상 컬렉션 규칙과 일치하지 않도록 피드 또는 데이터 계층에서 변경한 것이 있습니까? 대소문자가 일치하는지 확인하십시오(대소문자 구분).
* 피드가 성공적으로 실행되었습니까? 누군가 FTP 디렉토리, 암호 등을 변경했습니까?
* Target은 최대한 빨리 전달(고객의 페이지/앱에서)이 업데이트되도록 합니다. 하지만 Adobe에서는 마케터용 UI에서 몇 가지 표현도 제공해야 합니다. UI 업데이트가 동기화될 때까지 기다리기 위해 전달 업데이트가 지연되지는 않습니다. [mboxTrace](https://marketing.adobe.com/resources/help/en_US/target/target/c_content_trouble.html#)를 사용하여 요청이 들어올 당시 시스템의 내용을 확인할 수 있습니다.

## 일반 속성 가중치와 컨텐츠 유사성별 속성 가중치 간의 차이는 무엇입니까? {#section_FCD96598CBB44B16A4C6C084649928FF}

속성 가중치는 &quot;표준 속성 가중치&quot;와 &quot;컨텐츠 유사성 속성 가중치&quot;, 이렇게 두 가지 형태로 존재합니다.

&quot;표준 속성 가중치&quot;는 모두는 아니지만 대부분의 기준 유형(컨텐츠 유사성뿐만 아니라)에 적용됩니다. 이 유형의 가중치는 특정 속성 값에 더 많은 가중치를 부여합니다. 다음 예에서 Nike 제품은 출력 권장 사항에서 문제가 생깁니다.

![](assets/attribute_weighting_example.png)

&quot;컨텐츠 유사성 속성 가중치&quot;는 컨텐츠 유사성 기준에만 적용됩니다.

이 유형의 가중치는 더 동적이며 현재 &quot;권장 사항 키&quot;(현재 보는 항목)를 기반으로 합니다. 다음 예에서(브랜드 x 16)는 방문자가 Nike 스니커즈를 보고 있다면 해당 방문자는 경쟁 업체의 스니커즈보다 다른 Nike 제품(반드시 스니커즈일 필요는 없음)을 추천받을 가능성이 더 큽니다. 방문자가 Adidas 스니커즈를 보고 있다면 이 방문자는 Adidas 제품을 추천받을 가능성이 더 큽니다.

![](assets/content_similarity_example.png)

## Target에서 권장 사항이 때때로 표시되지 않는 이유는 무엇입니까? {#section_DB3F40673AED42228E407C05437D99E9}

때로는 Target에서 사용 가능한 권장 사항 수가 적어서 권장 사항이 표시되지 않을 수 있습니다.

기준당 생성된 값의 수는 디자인에 지정된 엔티티 수의 5배입니다. 런타임 필터링(예: 재고, mbox 속성 일치)은 5x개의 값을 생성한 후에 적용되며, 따라서 전달 시 5x개보다 적은 수의 값으로 끝날 수 있습니다. 이 상황을 완화하려면 추가 엔티티를 숨겨서 디자인의 엔티티 수를 늘리십시오.

다음 JavaScript는 요청한 엔티티 수를 늘리기 위해 디자인의 시작 부분에서 사용할 수 있습니다. 이 예제에서 요청된 엔티티 수는 50(5x10)입니다.

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## 제품 삽입/업데이트에 대한 API 호출의 크기 제한이란 무엇입니까? 피드 대신 API를 사용하여 한 번의 호출로 50,000개의 제품을 업데이트할 수 있습니까? {#section_434FE1F187B7436AA39B7C14C7895168}

Target은 애플리케이션 수준에 50MB의 사후 제한을 지정합니다. 하지만 `application/x-www-form-urlencoded` 컨텐츠 유형 헤더를 전달하는 경우에만 해당됩니다.

단일 호출에서 50,000개 제품 전송을 시도할 수 있습니다. 실패할 경우 묶음으로 나누어야 합니다. 일반적으로 고객이 호출을 5,000 또는 10,000개의 제품 묶음으로 나누어 시스템 로드로 인한 시간 초과 가능성을 줄이는 것이 좋습니다.

## 권장 사항 기준, 프로모션 또는 템플릿 테스트 규칙을 생성할 때 mbox 이름을 지정해야 합니까? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

mbox 매개 변수를 기반으로 한 권장 사항, 기준, 프로모션 또는 템플릿 테스트 규칙을 만들 때 `mboxParameter`에 `mboxName`을 묻는 메시지가 더 이상 표시되지 않습니다. 이제 mbox 이름은 선택 사항입니다. 따라서 여러 mbox의 매개 변수를 사용하거나 가장자리에 아직 기록되지 않은 매개 변수를 참조할 수 있습니다.

원하는 매개 변수를 선택하려면 다음을 수행하십시오.

* 새 기준, 프로모션 또는 템플릿 테스트 규칙을 만드는 동안 목록에서 매개 변수 이름을 선택하고, 원하는 매개 변수 이름의 첫 글자를 입력하거나 전체 이름을 입력합니다.
* mbox 이름은 기억하지만, 매개 변수 이름을 기억하지 못하는 경우 원하는 매개 변수를 전달하는 알려진 mbox를 필터링할 확인란을 사용합니다.

어느 방법을 사용하든 mbox와 매개 변수 간에 링크가 없습니다. 기준, 프로모션 또는 템플릿 테스트 규칙은 해당 매개 변수를 전달하는 모든 mbox에서 매개 변수를 기준으로 하여 작동합니다.

기존 기준, 프로모션 또는 템플릿 테스트 규칙을 편집하는 경우 필터링 기준에는 작성 중에 제공된 mbox 이름이 함께 표시됩니다.

## 새 대상을 정의한 후 기존 권장 사항 활동을 저장할 수 없는 이유는 무엇입니까? {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

대상에 고유한 이름이 있는지 확인하십시오. 기존 대상과 동일한 이름을 지정했다면 기존 권장 사항 활동(2016년 10월 이전에 만든 권장 사항 활동)을 저장할 수 없습니다.

## 피드 업로드를 위한 CSV 파일의 최대 크기는 얼마입니까? {#section_20F1AF4839A447B9889B246D6E873538}

피드의 CSV 파일 업로드에 대한 행 수 또는 파일 크기에는 엄격한 제한이 없습니다. 그러나 파일 업로드 프로세스 중 실패를 방지하기 위해 CSV 파일 크기를 1GB로 제한하는 것이 좋습니다. 파일 크기가 1GB를 초과하는 경우 이상적으로 여러 피드 파일로 분할해야 합니다. 사용자 지정 속성 컬럼의 최대 수는 100개이며 사용자 지정 속성은 4096자로 제한됩니다. 필요한 열의 길이에 대한 추가 제한은 [Target 제한 사항 페이지](../../r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1)에서 참조할 수 있습니다.

## 동적으로 엔티티를 제외시킬 수 있습니까?

추천에서 제외할 개체에 대한 개체 ID를 쿼리 문자열에서 전달할 수 있습니다. 예를 들어 장바구니에 이미 있는 항목을 제외할 수 있습니다.

제외 기능을 활성화하려면 `excludedIds` mbox 매개 변수를 사용합니다. 이 매개 변수는 쉼표로 구분된 엔티티 ID 목록을 가리킵니다. 예, `mboxCreate(..., "excludedIds=1,2,3,4,5")`. 추천 요청 시 해당 값이 전송됩니다.

>[!NOTE]
>
>너무 많은 개체가 제외되면 추천 템플릿을 채울 충분한 개체가 없는 것처럼 추천이 작동합니다.

제외하려면 `entityIds`, 토큰을 오퍼 `&excludes=${mbox.excludedIds}` 컨텐츠 URL에 추가합니다. 컨텐츠 URL이 추출되면 필수 매개 변수는 현재 mbox 요청 매개 변수를 사용하여 대체됩니다.

기본적으로 이 기능은 새로 만든 추천에 대해 활성화됩니다. 동적으로 제외된 개체를 지원하기 위해 기존 권장 사항을 저장해야 합니다.
