---
keywords: 카탈로그 검색;카탈로그;검색;제외;컬렉션;필터;권장 사항
description: 사용 방법 알아보기 [!DNL Recommendations] [!UICONTROL Catalog Search] 제품 또는 콘텐츠를 찾으려면 카탈로그에서 항목을 제거하는 등의 작업을 수행하십시오.
title: 사용 방법 [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 6b0175b1-0eee-498d-8a08-513cf6695114
source-git-commit: 16a7c11e8b9b1a08b1e467519f997d0b05e47529
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 21%

---

# [!UICONTROL Catalog Search]

다음 [!UICONTROL Catalog Search] 페이지 위치 [!DNL Adobe Recommendations] 은 카탈로그에서 제품 또는 콘텐츠를 찾는 데 도움이 됩니다. 이 페이지에서 수행할 수 있는 가장 기본적인 작업은 항목을 검색하는 것입니다. 또한 환경을 변경하고 패싯을 필터링하고 테이블에서 열을 수정하고 새 검색 패싯을 추가하는 등의 작업을 수행할 수 있습니다.

카탈로그는 전체 제품 세트(엔티티)를 나타냅니다. 카탈로그에는 제품을 논리 버킷으로 구성하는 여러 컬렉션이 포함될 수 있습니다.

## 액세스 [!UICONTROL Catalog Search]

에 액세스하려면 [!UICONTROL Catalog Search] 페이지, 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![카탈로그 검색 페이지](/help/main/c-recommendations/c-products/assets/catalog-search-new.png)

## 단순 검색 수행

1. 에 검색어 입력 **[!UICONTROL Search In]** 필드.

1. (선택 사항) 의 아래쪽 화살표를 클릭할 때 표시되는 옵션 메뉴에서 검색 옵션을 선택하여 검색을 개선할 수 있습니다 [!UICONTROL Search In] 필드.

   검색 옵션에는 다음이 포함됩니다.

   * ID
   * 이름
   * 메시지

1. 검색 결과의 항목을 스크롤하여 썸네일 및 기타 제품 정보를 확인합니다.

   >[!NOTE]
   >
   > 숫자 값으로 사용자 지정 특성에 대한 카탈로그 검색을 수행할 때 결과는 사용자 지정 특성을 숫자 값 대신 문자열 유형으로 간주합니다.
   >
   >현재 속성 유형을 변경할 수 있는 기능이 없습니다. 변경하려면 문자열에서 숫자로 유형을 변경해야 하는 특성을 참조하는 [고객 문제를 여십시오](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

   필터를 사용하여 원하는 제품을 찾을 수도 있습니다. 예를 들어 **[!UICONTROL Show Filters]** 아이콘( ![필터 표시 아이콘](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ), 확장 [!UICONTROL Collections] facet을 선택한 다음 하나 이상의 컬렉션을 선택하면 카탈로그에서 선택한 컬렉션에 속하는 모든 제품이 표시됩니다.

<!-- ### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.-->

## 항목의 세부 사항 보기

ID, 이름, 메시지, 범주 등을 포함한 개별 항목의 세부 사항을 보면 해당 항목의 세부 사항을 볼 수 있습니다.

1. 세부 정보를 보려면 검색 결과에서 항목을 클릭하십시오.

## 카탈로그에서 항목 제거

1. 세부 정보를 보려면 검색 결과에서 항목을 클릭하십시오.

1. **[!UICONTROL Remove from Catalog]** 아이콘을 클릭합니다.

1. 항목을 제거할지 확인합니다.

해당 항목에 대한 모든 정보가 카탈로그 색인에서 제거됩니다. 항목은 데이터 피드에 다시 추가되는 경우에만 카탈로그에 포함됩니다. 삭제된 항목은 피드에서 별도로 삭제해야 합니다.

## 카탈로그 새로 고침

카탈로그의 색인은 첫 번째 피드를 업로드할 때 자동으로 만들어지고 다음에 따라 새로 고쳐집니다. [지정된 일정](/help/main/c-recommendations/c-products/feeds.md#steps).

피드 파일, API 또는 mbox 업데이트를 통해 업데이트가 수신되면 카탈로그가 자동으로 새로고침됩니다. 업데이트는 일반적으로 1시간 이내에 완료됩니다. 업데이트가 진행 중인 경우 가장 최근 업데이트가 시작된 시간이 표시됩니다. 진행 중인 업데이트가 없으면 가장 최근 업데이트가 시작되고 완료된 시간이 표시됩니다.

<!-- ## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.-->

## 환경 변경

[환경](/help/main/administrating-target/environments.md) 간편한 관리 및 개별 보고를 위해 사이트 및 사전 프로덕션 환경을 구성할 수 있습니다.

1. 필터 표시 아이콘( ![필터 표시 아이콘](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ).

1. 에서 원하는 환경을 선택합니다. **[!UICONTROL Environment]** 드롭다운 목록입니다.

<!-- ## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.-->

## 열 수정

에서 활성 열을 일시적으로 수정할 수 있습니다. [!UICONTROL Catalog Search] 페이지를 가리키도록 업데이트하는 중입니다.

1. 다음을 클릭합니다. **[!UICONTROL Customize Table]** 아이콘(  ![표 맞춤화 아이콘](/help/main/c-recommendations/c-products/assets/icon-customize-table.png) ).

1. 표시하거나 숨길 열을 선택하거나 선택 취소합니다.

변경한 내용은 현재 세션에만 적용됩니다.
