---
keywords: 권장 사항 피드, 피드, SAINT, ftp, csv, 분류, 분석 분류
description: 피드가 CSV 파일,  [!DNL Adobe Target] [!DNL Recommendations]피드 형식 및  [!DNL Google Product Search] 제품 분류를 사용하여  [!DNL Analytics] 에 엔티티를 가져오는 방법에 대해 알아봅니다.
title: '[!UICONTROL Feeds]에서  [!DNL Target Recommendations]을(를) 사용하는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 7b336a9e-23f4-4b09-9c8f-b9cb68162b1b
source-git-commit: 5a8b4006a2c43c9cac2d22e7663aa21043f98d9a
workflow-type: tm+mt
source-wordcount: '2613'
ht-degree: 35%

---

# 피드

피드를 사용하여 [!DNL Adobe Target] [!DNL Recommendations]&#x200B;(으)로 가져온 엔터티를 가져옵니다. 엔터티는 CSV 파일, [!DNL Google Product Search] 피드 형식 및 [!DNL Adobe Analytics] 제품 분류를 사용하여 보낼 수 있습니다.

## 피드 개요 {#concept_D1E9C7347C5D4583AA69B02E79607890}

피드를 사용하면 [엔터티](/help/main/c-recommendations/c-products/products.md)를 전달하거나 페이지에서 사용할 수 없거나 페이지에서 직접 보내기에는 안전하지 않은 정보가 있는 mbox 데이터를 보강할 수 있습니다. 예를 들어 마진, COGS(매출 원가) 등이 있습니다.

피드를 사용하면 제품 ID, 범주, 이름, 메시지 및 기타 특성과 같은 자세한 항목 정보를 [!DNL Recommendations]에 전달할 수 있습니다.

[!DNL Target] 제품 분류 파일 또는 [!DNL Google Product Search] 파일에서 [!DNL Recommendations] 서버로 보낼 열을 선택할 수 있습니다.

각 항목에 대한 이러한 데이터 조각을 사용하여 다음을 수행할 수 있습니다.

* 디자인에 값 표시
* 기준 포함 규칙 정의
* 항목을 다른 컬렉션으로 정렬
* 권장 사항에 제외 적용

항목 설명은 피드 또는 mbox를 사용하여 [!DNL Target]에 전달할 수 있습니다. [!DNL Target]이(가) 엔터티 피드와 mbox를 모두 사용하여 데이터를 수집하면 가장 최근 데이터가 성공합니다. 일반적으로 가장 최근의 데이터는 mbox가 더 자주 조회되므로 mbox에서 옵니다. 드물지만 개체 피드 데이터와 mbox 데이터가 동시에 조회되는 경우 mbox 데이터가 사용됩니다.

[!UICONTROL Feeds] 목록( **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]**)에는 만들어진 피드에 대한 정보가 있습니다.

[!UICONTROL Feeds] 페이지에 다음 열이 포함되어 있습니다.

* **이름**: 만드는 중에 지정된 피드의 이름입니다. 피드의 이름을 편집하려면 피드 자체를 편집해야 합니다. 피드를 새 이름으로 저장하면 피드가 새로 고쳐집니다.
* **상태**: 피드의 현재 [상태](/help/main/c-recommendations/c-products/feeds.md#concept_E475986720D1400999868B3DFD14A7A0)입니다.
* **유형**: 유형에는 [CSV](/help/main/c-recommendations/c-products/feeds.md#section_65CC1148C7DD448FB213FDF499D35FCA), [[!DNL Google Product Feed]](/help/main/c-recommendations/c-products/feeds.md#section_8EFA98B5BC064140B3F74534AA93AFFF) 및 [Analytics 분류](/help/main/c-recommendations/c-products/feeds.md#section_79E430D2C75443BEBC9AA0916A337E0A)가 포함됩니다.
* **항목**: 피드에 있는 항목의 수를 표시합니다.
* **일정**: [!UICONTROL Daily], [!UICONTROL Weekly], [!DNL Every 2 Weeks] 또는 [!UICONTROL Never] 피드의 업데이트 일정을 표시합니다.
* **마지막 업데이트**: 피드를 마지막으로 업데이트한 날짜와 시간, 피드를 업데이트한 사람의 이름을 표시합니다.

[!UICONTROL Customize Table] 아이콘(![표 사용자 지정 아이콘](/help/main/assets/icons/ColumnSetting.svg))을 클릭하여 표시할 열을 선택하거나 선택 취소합니다.

[!UICONTROL Information] 아이콘(![정보 아이콘](/help/main/assets/icons/InfoOutline.svg))을 클릭하여 마지막 업로드 날짜와 피드의 URL을 표시하는 카드를 표시합니다.

[!UICONTROL More Actions] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg) )을 클릭하여 [!UICONTROL Deactivate], [!DNL Edit], [!UICONTROL Copy] 및 [!UICONTROL Delete] 작업에 액세스합니다.

>[!IMPORTANT]
>
>업로드된 엔티티 및 엔티티 속성은 61일 후에 만료됩니다. 이것은 다음을 의미합니다.
>
>* 피드는 카탈로그 콘텐츠가 만료되지 않도록 최소 매월 실행해야 합니다.
>* 피드 파일에서 항목을 제거해도 카탈로그에서 해당 항목이 제거되지 않습니다. 카탈로그에서 항목을 제거하려면 [!DNL Target] UI 또는 API를 통해 항목을 수동으로 삭제하십시오. 또는 품목 속성(예: 재고)을 수정하여 품목이 고려 대상에서 제외되도록 합니다.

## Source 유형

엔터티는 CSV 파일, [!DNL Google Product Search] 피드 형식 및 [!DNL Adobe Analytics] 제품 분류를 사용하여 보낼 수 있습니다.

### CSV로 내보내기 {#section_65CC1148C7DD448FB213FDF499D35FCA}

[!DNL Adobe] 소유 CSV 업로드 형식을 사용하여 .csv 파일을 만들 수 있습니다. 파일에는 제품용으로 예약된 속성과 사용자 지정 속성에 대한 표시 정보가 들어 있습니다. 사용하는 구현에 대한 속성을 업로드하려면 헤더 행의 `CustomN`을 사용하려는 속성의 이름으로 바꾸십시오. 이 아래 예에서는 `entity.Custom1`이 `entity.availability`로 교체되었습니다. 그런 다음 파일을 [!DNL Recommendations] 서버에 벌크로 업로드할 수 있습니다.

.csv 형식을 사용하면 [!DNL Google] 피드 형식보다 다음과 같은 이점이 있습니다.

* .csv 형식에는 필드 매핑이 필요하지 않습니다.
* .csv 형식은 다중 값 특성을 지원합니다(아래 예 참조).
* .csv 형식은 최대 100개의 사용자 지정 특성을 지원합니다. 100개가 넘는 사용자 지정 속성이 필요한 경우에는 다른 사용자 지정 속성 세트가 지정된 부가적 피드 파일을 작성할 수 있습니다.

페이지에 mbox가 없거나 사이트에서 사용할 수 없는 항목으로 표시 정보를 보완하려는 경우 벌크 업로드 방법을 사용하여 표시 정보를 보냅니다. 예를 들어 사이트에 게시되지 않았을 수 있는 재고 정보를 전송할 수 있습니다.

.csv 파일, Google 제품 피드 또는 [!DNL Analytics] 제품 분류 피드를 사용하여 업로드한 모든 데이터는 데이터베이스의 기존 엔터티 특성 값을 덮어씁니다. mbox 요청을 통해 가격 정보를 보내고 파일에 다른 가격 값을 보내는 경우 파일의 값은 mbox 요청에 설정된 값을 덮어씁니다. 최대 250자까지 덮어쓰는 대신 카테고리 값을 추가한 `categoryId` 엔티티 속성은 예외입니다.

>[!IMPORTANT]
>
>.csv 파일에서 의도된 것이 아니라면 값을 큰따옴표(&quot;)로 묶지 마십시오. 값을 큰따옴표로 묶으면 다른 큰따옴표로 묶어서 이스케이프 처리를 해야 합니다. 큰따옴표를 이스케이프 처리를 하지 않으면 추천 피드가 제대로 로드되지 않습니다.

예를 들어, 다음 구문은 올바르지 않습니다.

```
"Apples "Bananas" Grapes"",
```

다음 구문은 올바릅니다.

```
"Apples ""Bananas"" Grapes""",
```

>[!NOTE]
>
>기존 값을 빈 값으로 덮어쓸 수 없습니다. 기존 값을 덮어쓰려면 다른 값을 그 위치에 전달합니다. 판매 가격의 경우 일반적인 해결 방법은 실제 &quot;NULL&quot; 또는 다른 메시지를 전달하는 것입니다. 그런 다음 템플릿 규칙을 작성하여 해당 값이 포함된 항목을 제외할 수 있습니다.

개체를 성공적으로 업로드하고 약 2시간 후 관리 인터페이스에서 제품을 사용할 수 있습니다.

다음은 .csv 파일의 샘플 코드입니다.

```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches & Sport,Cutting edge titanium with round case,https://example.com/s7/na3456_Viewer,425,https://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches & Sport,Cutting edge matte black with round case,https://example.com/s7/na3457_Viewer,275,https://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```

### [!DNL Google] {#section_8EFA98B5BC064140B3F74534AA93AFFF}

[!DNL Google Product Search] 피드 형식은 [!DNL Google] 형식을 사용합니다. [!DNL Adobe] 소유 CSV 업로드 형식과 다릅니다.

기존 [!DNL Google Product Feed]이(가) 있는 경우 가져오기 파일로 사용할 수 있습니다.

>[!NOTE]
>
>[!DNL Google] 데이터를 사용할 필요는 없습니다. [!DNL Recommendations]은(는) [!DNL Google]과(와) 동일한 형식을 사용합니다. 이 방법을 사용하여 보유하고 있는 데이터를 업로드하고 사용 가능한 예약 기능을 이용할 수 있습니다. 그러나 파일을 설정할 때 미리 정의된 특성 이름 [!DNL Google]을(를) 유지해야 합니다.

대부분의 소매업체는 제품을 [!DNL Google]에 업로드하므로 방문자가 [!DNL Google] 제품 검색을 사용하면 해당 제품이 표시됩니다. [!DNL Recommendations]은(는) 정확히 엔터티 피드에 대해 [!DNL Google] 사양을 따릅니다. 엔터티 피드는 .xml, .txt 또는 .tsv를 통해 [!DNL Recommendations]에 전송될 수 있으며, Google에서 정의한 [특성을 사용할 수 있습니다](https://support.google.com/merchants/answer/188494?hl=en&topic=2473824&ctx=topic#US). 결과는 [[!DNL Google] 쇼핑 페이지](https://www.google.com/prdhp)에서 검색할 수 있습니다.

>[!NOTE]
>
>POST 메서드는 [!DNL Google] 피드 콘텐츠를 호스팅하는 서버에서 허용되어야 합니다.

[!DNL Recommendations]명의 사용자가 이미 URL 또는 FTP를 통해 [!DNL Google]에게 전송할 .xml 또는 .txt 피드를 구성했으므로, 엔터티 피드는 해당 제품 데이터를 수락하고 이를 사용하여 권장 사항 카탈로그를 만듭니다. 피드가 존재하며 권장 사항 서버가 데이터를 검색하는 위치를 지정합니다.

엔터티 피드 업로드에 [!DNL Google Product Search]을(를) 사용하는 경우, 권장 사항을 표시하거나 보기를 기반으로 알고리즘 전달을 위한 제품 보기를 추적하려면 페이지에 제품 페이지 mbox가 있어야 합니다.

[!DNL Google] 피드는 사용자 지정 특성에 대해 여러 값을 지원하지 않습니다.

피드는 저장하고 활성화할 때 실행됩니다. 피드를 저장할 때 실행된 다음 한 시간 후 매일 실행됩니다.

다음은 [!DNL Google Product Search] 피드 .xml 파일에 대한 샘플 코드입니다.

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="https://www.w3.org/2005/Atom" xmlns:ns2="https://base.google.com/ns/1.0" xmlns:ns3="https://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="https://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>https://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
```

다음은 [!DNL Google Product Search] 피드 .tsv 파일에 대한 샘플 코드입니다.

```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    https://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    https://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```

### [!DNL Analytics] 제품 분류 {#section_79E430D2C75443BEBC9AA0916A337E0A}

[!DNL Adobe Analytics] 제품 분류는 권장 사항에 사용할 수 있는 분류입니다. 이 분류 파일에 대한 자세한 내용은 [Analytics 구성 요소](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=ko) 안내서에서 *분류 정보*&#x200B;를 참조하십시오. 권장 사항에 필요한 일부 정보는 현재 구현에서 사용하지 못할 수 있으므로, 분류 파일에 추가할 경우 이 사용 안내서를 따르십시오.

>[!IMPORTANT]
>
>[!DNL Recommendations] 제품 분류를 사용하여 엔터티 데이터를 [!DNL Analytics]&#x200B;(으)로 가져오기 전에 이 방법이 기본 방법이 아니라는 것을 알아 두십시오.
>
> 다음 주의 사항에 유의하십시오.
>
>* 엔티티 속성에 대한 업데이트는 최대 24시간이 넘는 지연을 초래합니다.
>* [!DNL Target]은(는) [!UICONTROL Product Classifications]만 지원합니다. [!DNL Analytics] 제품 SKU는 [!DNL Recommendations] `entity.id`과(와) 동일한 수준에 매핑해야 합니다. 사용자 지정 [!DNL Analytics] 분류는 [!UICONTROL Adobe Consulting Services]을(를) 사용하여 제작할 수 있습니다. 질문이 있는 경우 계정 관리자에게 문의하십시오.

## 피드 만들기 {#steps}

[!DNL Recommendations]에 제품이나 서비스에 대한 정보를 삽입하는 피드를 작성합니다.

1. [!DNL Target] 인터페이스 내에서 **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]**&#x200B;을(를) 클릭합니다.

1. 피드의 수사적 이름을 지정합니다.
1. **[!UICONTROL Source Type]** 선택.

   * [!UICONTROL CSV]
   * [!UICONTROL Google Product Feed]
   * [!UICONTROL Analytics Classifications]

   [!UICONTROL CSV] 및 [!UICONTROL Google Product Feed] 피드 유형에 대한 자세한 내용은 [피드 개요](/help/main/c-recommendations/c-products/feeds.md#concept_D1E9C7347C5D4583AA69B02E79607890)를 참조하십시오. [모델 CSV 가이드를 다운로드](/help/main/c-recommendations/c-products/assets/EntityFileUploadTemplate.csv)하여 피드의 형식을 올바르게 지정할 수도 있습니다.

1. (조건부) **[!UICONTROL CSV]** 또는 **[!UICONTROL Google Product Feed]**&#x200B;을(를) 선택한 경우 피드에 액세스할 수 있는 위치를 지정하십시오.

   * **FTP**: FTP를 선택하는 경우 FTP 서버 정보, 로그인 자격 증명, 파일 이름 및 FTP 디렉토리를 제공하십시오. 보다 안전한 업로드를 위해 SSL을 사용하는 FTP(FTPS)를 사용할 수 있습니다.

     지원되는 FTP 서버 설정:

      * FTP 및 FTPS는 수동 FTP를 사용하도록 설정되어야 합니다.
      * FTPS의 경우, 명시적 FTPS 연결을 허용하도록 서버를 구성합니다.
      * SFTP는 지원되지 않습니다.
      * 연결을 시작할 포트를 수동으로 지정할 수 있습니다(예: `ftp://ftp.yoursite.com:2121`). 포트를 지정하지 않으면 기본 FTP 또는 FTPS 포트가 사용됩니다.

   * **URL**: [!UICONTROL URL]을(를) 선택하는 경우 URL을 지정하십시오.

1. (조건부) **[!UICONTROL Analytics Classifications]**&#x200B;을(를) 선택한 경우 드롭다운 목록에서 보고서 세트를 선택합니다.

1. **[!UICONTROL Next]** 화살표를 클릭하여 [!UICONTROL Schedule] 옵션을 표시합니다.

1. 업데이트 선택 사항을 선택합니다. 

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 Weeks]
   * [!UICONTROL Never]: 업데이트를 예약하지 마십시오. 이 피드를 실행하지 않으려면 이 항목을 선택하십시오.

1. 피드를 실행할 시간을 지정합니다.

   이 선택 사항은 브라우저에서 사용되는 시간대를 기반으로 합니다. 다른 시간대의 시간을 사용하려면 시간대에 따라 시간을 계산해야 합니다.

1. **[!UICONTROL Next]** 화살표를 클릭하여 [!UICONTROL Mapping] 옵션을 표시한 다음 데이터를 [!DNL Target] 정의에 매핑하는 방법을 지정합니다.

1. (선택 사항) 피드가 환경(호스트 그룹)에 속하도록 하려면 호스트 그룹을 선택합니다.

   기본적으로 피드는 모든 호스트 그룹에 속합니다. 따라서 이 피드의 항목을 어떤 환경에서든 사용할 수 있습니다. 자세한 내용은 [호스트](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)를 참조하십시오.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

피드를 만들거나 편집한 후 피드가 즉시 실행됩니다. 그러면 피드는 사용자가 설정한 매개 변수에 따라 업데이트됩니다. 정보가 나오려면 시간이 좀 걸립니다. 먼저 피드를 동기화한 후에 처리하고 색인화해야만 게시하고 사용할 수 있게 됩니다. 현재 상태는 [ 목록의 ](/help/main/c-recommendations/c-products/feeds.md#status)피드 상태[!UICONTROL Feeds]에 표시됩니다. [!DNL Target]을 닫은 후에 프로세스를 완료하고 프로세스를 계속 진행할 수 있습니다.

색인화가 진행 중인 동안 개별 값이 색인화되기 전에 제품 및 피드 헤더가 표시됩니다. 이렇게 하면 색인화가 완료되기 전에 컬렉션, 제외, 디자인 및 활동을 만들 수 있도록 제품을 검색하고 볼 수 있습니다.

상태에 &quot;성공&quot;이 표시되면 이것은 파일을 찾았으며 올바로 구문 분석했음을 의미합니다. 파일이 색인화되기 전까지는 [!DNL Recommendations]에서 이 정보를 사용할 수 없습니다. 색인화는 파일의 크기에 따라 시간이 좀 걸릴 수 있습니다. 프로세스가 실패하면 파일을 찾을 수 없음을 의미합니다. 예를 들어 잘못된 URL을 사용했거나 FTP 정보가 잘못되었거나 구문 분석 오류가 있습니다.

## 피드 상태 및 표시기 {#concept_E475986720D1400999868B3DFD14A7A0}

가능한 피드 상태 및 해당 표시기에 대한 정보입니다.

### 피드 상태 {#status}

다음은 피드의 가능한 상태입니다.

| 상태 | 설명 |
|--- |--- |
| [!UICONTROL Syncing] | 피드 설정 세부 정보가 [!DNL Target]에 저장되고 있습니다. |
| [!UICONTROL Sync Failed] | 피드 설정 세부 정보를 [!DNL Target]에 저장할 수 없습니다. 다시 시도하십시오. |
| [!UICONTROL No Feed Run] | 피드를 만들었지만 예약하지 않았습니다(빈도가 사용 안 함으로 설정됨). |
| 예약 일시: *날짜 및 시간* | 피드가 실행되지 않았지만 지정된 날짜 및 시간에 실행되도록 예약되었습니다. |
| [!UICONTROL Waiting for Download] | [!DNL Target]이(가) 피드 파일 다운로드를 준비하는 중입니다. |
| [!UICONTROL Downloading Feed File] | [!DNL Target]이(가) 피드 파일을 다운로드하고 있습니다. |
| [!UICONTROL Importing Items] | [!DNL Target]이(가) 피드 파일에서 항목을 가져오는 중입니다. |
| 피드를 *시간 내에* 성공적으로 가져옴 | [!DNL Target]이(가) 피드 파일을 콘텐츠 전달 시스템으로 가져왔습니다. 항목 속성에 대한 변경 사항은 콘텐츠 전달 시스템에서 만들어졌으며, 곧 전달된 권장 사항에 반영될 예정입니다. 예상 변경 사항이 표시되지 않으면 다시 시도하여 권장 사항이 포함된 페이지를 새로 고치십시오.<br>메모:<ul><li>항목의 속성에 대한 변경 사항으로 인해 항목이 권장 사항에서 제외되는 경우 제외 사항이 즉시 반영됩니다. 항목이 새로 추가되거나 특성을 변경하면 해당 항목이 권장 사항에서 더 이상 제외되지 *않습니다*. 이 경우 24시간 내에 다음 알고리즘 업데이트가 발생할 때까지 반영되지 않습니다.</li><li>이 상태가 표시되면 업데이트가 [!UICONTROL Catalog Search] UI에 아직 반영되지 않았을 수 있습니다. 검색 가능한 카탈로그가 마지막으로 업데이트된 시간을 나타내는 별도의 상태가 [!UICONTROL Catalog Search]에 나열됩니다.</li></ul> |
| 부분 가져오기 실패 | 이전에는 모든 행이 업로드되지 않은 경우에도 피드가 성공으로 표시되었습니다. 따라서 피드가 성공적으로 표시되었을 때 모든 행이 업로드되었다는 잘못된 인상을 만듭니다.<P>다음은 부분 피드 가져오기가 발생할 수 있는 이유에 대한 시나리오입니다.<ul><li>프로덕션 환경에 대한 피드 파일(예: 100개 행)을 업로드했습니다.</li><li>피드가 실행되어 해당 행 중 80개를 업로드하고 잘못된 형식, 필드 초과 문자 등으로 인해 20개의 행을 삭제했습니다.</li><li>UI에서 피드가 성공으로 표시되어 100개의 행이 모두 업로드된 것처럼 보입니다.</li><li>활동 전달에 20개 제품 중 일부가 예상되지만 발생하지 않습니다.</li><li> 해당 제품에 대한 제품 세부 사항이 있는 피드를 업로드했기 때문에 이 시점에서 혼란스럽습니다. Entity API를 통해 쿼리할 때 백엔드에 표시되지 않는데, 이는 해당 API가 백엔드에 없음을 나타냅니다.</li></ul>이러한 혼동을 제거하기 위해 피드에 발생한 사항을 정확히 알 수 있도록 메시지가 개선됩니다. 성공으로 표시하기보다는 이제 부분 가져오기 실패로 표시됩니다. |
| [!UICONTROL Failed to Index] | 색인 작업에 실패했습니다. 다시 시도하십시오. |
| [!UICONTROL Server Not Found] | FTP 또는 URL 위치가 잘못되었거나 접속할 수 없습니다. |

피드를 업데이트하려면(예를 들어, 피드 구성이나 피드 파일 변경) 피드를 열고 원하는 대로 변경하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭하십시오.

>[!IMPORTANT]
>
>업로드된 엔티티는 61일 후에 만료됩니다. 즉, 권장 사항 활동이 중단되는 것을 방지하기 위해 적어도 60일마다 피드 파일을 업로드해야 합니다. 60일마다 한 번 이상 피드 파일(또는 다른 엔터티 업데이트 메서드)에 포함되지 않은 항목은 [!DNL Target]에서 더 이상 관련성이 없다고 유추하여 카탈로그에서 제거합니다.

### 피드 상태 표시기 {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

[!UICONTROL Status] 열에 다음 피드 상태 표시기가 표시됩니다.

| 상태 표시기 | 설명 |
|--- |--- |
| 녹색 상태 표시기 | 피드가 색인화를 성공적으로 완료하면 녹색 상태 점이 피드가 성공 상태임을 표시합니다. |
| 노란색 상태 표시기 | 피드 또는 피드 색인이 피드 주기의 25%만큼 지연되면 노란색 상태 점이 표시됩니다. 예를 들어 예약된 시간으로부터 6시간 후에도 색인이 완료되지 않으면 매일 실행되도록 설정된 피드에 대해 노란색 점이 표시됩니다. 참고: 피드 상태가 &quot;색인 큐 대기 중&quot;이면 새로 업데이트된 값을 전달 및 기준 처리에서 사용할 수 있습니다. |
| 흰색 상태 표시기 | 피드를 예약하지 않으면 흰색 상태 점이 피드가 아직 실행되지 않았음을 표시합니다. |
| 빨간색 상태 표시기 | 피드가 서버에 데이터를 업로드하지 못하면 빨간색 상태 표시기가 표시됩니다. |

다음 예를 생각해 보십시오.

**예제 1:**

* 1일: 매일 오전 9시(PST)에 피드 처리
* 2일째: 오후 3시 30분인데 피드가 어제 오전 9시 이후에 실행되지 않았습니다.

약 6.5시간 전에 색인이 실행되어야 했는데 그렇지 않으므로 상태는 노란색이어야 합니다. 6.5시간 +24는 피드 창의 127%입니다.

**예제 2:**

* 1월 1일: 매월 피드 프로세스는 오전 9시(PST)입니다.
* 2월 3일: 오전 10시이며 피드가 한 달, 하루, 한 시간 전에 실행되지 않습니다.

약 1일 1시간 전에 색인이 실행되어야 했는데 그렇지 않으므로 상태는 노란색이어야 합니다. 이것은 빈도 설정의 (31+(1/25))/30 = 1.03%에 불과하지만 하루 지연의 최대값을 초과했습니다.

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 권장 사항에서 피드 이해(3:01) ![개요 배지](/help/main/assets/overview.png)

이 비디오에는 다음 정보가 포함됩니다.

* 피드의 목적 이해
* 피드 값 이해

>[!VIDEO](https://video.tv.adobe.com/v/33985?captions=kor)

### 피드 만들기(6:44) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 피드 설정
* 사용할 피드 유형 파악

>[!VIDEO](https://video.tv.adobe.com/v/33984?captions=kor)
