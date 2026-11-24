---
keywords: 카탈로그 검색;카탈로그;검색;제외;컬렉션;필터;권장 사항
description: '[!DNL Recommendations] [!UICONTROL 카탈로그 검색]을(를) 사용하여 제품 또는 콘텐츠를 찾고 카탈로그에서 항목을 제거하는 방법에 대해 알아봅니다.'
title: '[!DNL Recommendations] [!UICONTROL 카탈로그 검색]을 사용하려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
TQID: 'https://experienceleague.adobe.com/en3hkFsDjEE86Tc-3vPSiZFy0K47SftZMN6RW0INNic'
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 3883dc9752db0a2427f70cb3036fe060c440361a
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 7%
---
# [!UICONTROL 카탈로그 검색] {#catalog-search}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Recommendations]에서 카탈로그를 검색하여 제품이나 콘텐츠를 찾는 방법과 항목을 필터링, 보기 및 제거하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Recommendations]의 **[!UICONTROL 카탈로그 검색]** 페이지는 카탈로그에서 제품이나 콘텐츠를 찾는 데 사용됩니다. 이 페이지에서 가장 기본적인 작업은 항목을 검색하는 것입니다. 또한 이 페이지에서는 환경 변경, 패싯 필터링, 테이블의 열 수정 등을 수행할 수 있습니다.

카탈로그는 전체 제품 세트(엔티티)입니다. 제품을 논리 그룹으로 구성하는 여러 컬렉션을 포함할 수 있습니다.

첫 번째 피드가 업로드되면 카탈로그의 색인이 자동으로 만들어지고 [지정된 일정](/help/main/c-recommendations/c-products/feeds.md#steps)에 따라 새로 고쳐집니다.

피드 파일, API 또는 mbox 업데이트를 통해 업데이트가 수신되면 카탈로그가 자동으로 새로 고쳐집니다. 업데이트는 일반적으로 1시간 이내에 완료됩니다. 업데이트가 진행 중인 경우 가장 최근 업데이트가 시작된 시간이 표시됩니다. 진행 중인 업데이트가 없으면 가장 최근 업데이트가 시작되고 완료된 시간이 표시됩니다.

## 카탈로그 검색

검색 결과를 사용하여 카탈로그의 항목을 검토하고 필요한 경우 카탈로그에서 항목을 제거합니다.

1. **[!UICONTROL 권장 사항]** > **[!UICONTROL 카탈로그 검색]**&#x200B;을 클릭합니다.

1. (선택 사항) 결과를 필터링하려면 **[!UICONTROL 필터 표시]** 아이콘(![필터 표시 아이콘](/help/main/assets/icons/Filter.svg))을 클릭한 다음 적용할 필터를 선택합니다. 사용 가능한 필터는 **[!UICONTROL 환경]**, **[!UICONTROL 컬렉션]**, **[!UICONTROL 범주]**, **[!UICONTROL 브랜드]**, **[!UICONTROL 인벤토리]** 및 **[!UICONTROL 값]**&#x200B;입니다.

   [환경](/help/main/administrating-target/environments.md)은(는) 관리 및 개별 보고를 위해 사이트 및 사전 프로덕션 환경을 구성합니다. 환경을 변경하려면 **[!UICONTROL 환경]** 드롭다운 목록에서 원하는 환경을 선택하십시오.

   ![필터 패널이 강조 표시된 카탈로그 검색 페이지: 컬렉션, 카테고리, 브랜드, 인벤토리, 값 및 고급 검색](../assets/catalog_search.png)

1. **[!UICONTROL 검색 위치]** 필드에 검색어를 입력하십시오.

1. (선택 사항) **[!UICONTROL 검색 위치]** 필드의 아래쪽 화살표로 열리는 옵션 메뉴에서 검색 옵션을 선택하여 검색을 구체화합니다.

   검색 옵션에는 다음이 포함됩니다.

   * ID
   * 이름
   * 메시지

1. **[!UICONTROL 테이블 사용자 지정]** 아이콘( ![테이블 사용자 지정 아이콘](/help/main/assets/icons/ColumnSetting.svg))을 클릭하여 **[!UICONTROL 카탈로그 검색]** 페이지에서 활성 열을 수정합니다.

   ![테이블 사용자 지정 아이콘이 강조 표시된 카탈로그 검색 페이지](../assets/catalog_search_4.png)

1. 검색 결과의 항목을 스크롤하여 썸네일 및 기타 제품 정보를 확인합니다.

   >[!NOTE]
   >
   >숫자 값이 있는 사용자 지정 특성에 대한 카탈로그 검색에서 결과는 사용자 지정 특성을 숫자 값이 아닌 문자열 유형으로 처리합니다.
   >
   >속성의 유형은 현재 변경할 수 없습니다. 변경을 요청하려면 문자열에서 숫자로 형식을 변경해야 하는 특성을 참조하는 [고객 문제를 여십시오](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. ID, 이름, 메시지, 카테고리 등을 포함한 세부 정보를 보려면 검색 결과에서 항목을 클릭하십시오.

   ![ID, 범주, 여백 및 기타 특성을 표시하는 카탈로그 항목의 세부 정보](../assets/catalog_search_2.png)

1. 카탈로그에서 항목을 제거하려면 **[!UICONTROL 카탈로그에서 제거]**&#x200B;를 클릭하십시오.

   그런 다음 해당 항목에 대한 모든 정보가 카탈로그 색인에서 제거됩니다. 항목은 데이터 피드에 다시 추가되는 경우에만 카탈로그에 다시 포함됩니다. 삭제된 항목도 피드와 별도로 삭제해야 합니다.

   ![카탈로그에서 제거 단추가 강조 표시된 카탈로그 항목의 세부 정보](../assets/catalog_search_3.png)

<!--
### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.
-->

<!--
## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.
-->



<!--
## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.
-->
