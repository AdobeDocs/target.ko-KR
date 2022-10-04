---
keywords: 카탈로그 검색;카탈로그;검색;제외;컬렉션;필터
description: Recommendations 카탈로그 검색을 사용하여 제품 또는 콘텐츠를 찾고, 컬렉션이나 제외를 만들고, 카탈로그에서 항목을 제거하는 방법을 알아봅니다.
title: Recommendations 카탈로그 검색을 사용하려면 어떻게 해야 합니까?
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 22%

---

# ![PREMIUM](/help/main/assets/premium.png) 카탈로그 검색

다음 [!UICONTROL 카탈로그 검색] 페이지 [!DNL Adobe Recommendations] 은 카탈로그에서 제품이나 콘텐츠를 찾는 데 도움이 됩니다. 이 페이지에서 수행할 수 있는 가장 기본적인 작업은 항목을 검색하는 것입니다. 또한 환경을 변경하고, 검색 결과를 컬렉션이나 제외에 저장하고, 필터 패싯을 추가하고, 테이블의 열을 수정하고, 새 검색 패싯을 추가하는 등의 작업을 수행할 수 있습니다.

카탈로그는 전체 제품 세트(엔티티)를 나타냅니다. 카탈로그에 많은 컬렉션이 포함될 수 있으며 이는 제품을 논리 버킷으로 구성하는 방법입니다.

## 카탈로그 검색 액세스

에 액세스하려면 [!UICONTROL 카탈로그 검색] 페이지를 클릭한 다음 **[!UICONTROL Recommendations]** > **[!UICONTROL 카탈로그 검색]**.

![카탈로그 검색 페이지](/help/main/c-recommendations/c-products/assets/catalog-search.png)

## 항목 검색

단순 검색 또는 고급 검색을 사용하여 카탈로그에서 항목을 찾을 수 있습니다.

### 단순 검색 수행

1. 에 검색어를 입력합니다. **[!UICONTROL 제품 검색]** 필드.

1. (선택 사항) 검색 필드에서 아래쪽 화살표를 클릭하면 표시되는 옵션 메뉴에서 검색 옵션을 선택하여 검색을 개선할 수 있습니다.

   ![searchproductsmenu 이미지](assets/searchproductsmenu.png)

   검색 옵션에는 다음이 포함됩니다.

   * ALL - OR 논리를 사용하여 기타 모든 검색 기준으로 검색합니다.
   * 이름
   * 브랜드
   * 카테고리
   * ID
   * 메시지

1. 이제 검색 결과의 항목을 스크롤하여 축소판 및 기타 제품 정보를 볼 수 있습니다.

   다음 그림은 모두 옵션을 사용하여 &quot;자전거&quot;에 대한 결과를 보여줍니다.

   ![자전거 카탈로그 검색](/help/main/c-recommendations/c-products/assets/bike-results.png)

   &quot;제품&quot; 옆에 표시되는 숫자는 지정된 환경에서 사용 가능한 전체 개수 중 검색어와 일치하는 제품의 수입니다.

   검색 자동 완성 기능을 사용할 수 있습니다. 다음 그림에서 &quot;bike&quot;를 입력하면 &quot;bike&quot;라는 단어가 포함된 모든 제품이 반환됩니다.

   ![검색 자동 완료](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >숫자 값으로 사용자 지정 특성에 대한 카탈로그 검색을 수행할 때 결과는 사용자 지정 특성을 숫자 값 대신 문자열 유형으로 간주합니다.
   >
   >현재 속성 유형을 변경할 수 있는 기능이 없습니다. 변경하려면 문자열에서 숫자로 유형을 변경해야 하는 특성을 참조하는 [고객 문제를 여십시오](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. 필터를 사용하여 원하는 제품을 찾을 수도 있습니다. 다음 예에서는 [!UICONTROL 컬렉션] 패싯을 선택하고 &quot;자전거 도구&quot;를 선택하면 카탈로그 디스플레이에 있는 모든 자전거 도구가 표시됩니다.

   ![자전거 도구](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. &quot;chain&quot;과 같은 검색어를 입력하여 결과 목록에서 더 자세히 검색할 수 있습니다.

   ![체인 검색](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### 고급 검색 수행 {#advanced-search}

다음을 사용할 수 있습니다 [!UICONTROL 고급 검색] 검색 결과를 세분화하거나 검색 결과를 [컬렉션](/help/main/c-recommendations/c-products/collections.md) 또는 [제외](/help/main/c-recommendations/c-products/exclusions.md).

1. 을(를) 클릭합니다. **[!UICONTROL 고급 검색]** 링크를 클릭합니다.

   ![고급 검색 페이지](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. 드롭다운 목록을 사용하여 검색할 매개 변수, 연산자 및 값을 지정합니다.

1. (선택 사항) **[!UICONTROL 규칙 추가]** 추가 검색 규칙을 추가하려면 다음을 수행하십시오.

   각 추가 검색 규칙은 AND 연산자로 연결됩니다.

1. **[!UICONTROL 검색]**&#x200B;을 클릭합니다.

1. (선택 사항) **[!UICONTROL 다른 이름으로 저장]**&#x200B;를 클릭한 다음 **[!UICONTROL 컬렉션]** 또는 **[!UICONTROL 제외]**.

   ![다른 이름으로 저장 옵션](/help/main/c-recommendations/c-products/assets/save-as.png)

   자세한 내용은 [고급 검색을 기반으로 컬렉션 또는 제외 만들기](#save-as) 아래의 제품에서 사용할 수 있습니다.

## 항목의 세부 사항 보기

ID, 이름, 메시지, 카테고리 등을 포함한 개별 항목의 세부 사항을 세부 사항을 확인하여 볼 수 있습니다.

1. 세부 사항을 보려면 검색 결과에서 항목을 클릭합니다.

   ![제품 세부 사항](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## 카탈로그에서 항목 제거

1. 세부 사항을 보려면 검색 결과에서 항목을 클릭합니다.

1. 클릭 **[!UICONTROL 카탈로그에서 제거]**.

1. 항목을 제거할지 확인합니다.

해당 항목에 대한 모든 정보가 카탈로그 색인에서 제거됩니다. 항목이 데이터 피드에 다시 추가되는 경우에만 카탈로그에 포함됩니다. 삭제된 항목은 피드에서 별도로 삭제해야 합니다.

## 카탈로그 새로 고침

첫 번째 피드를 업로드할 때 카탈로그의 색인이 자동으로 만들어져서 다음에 따라 새로 고침됩니다 [지정된 일정](/help/main/c-recommendations/c-products/feeds.md#steps).

피드 파일, API 또는 mbox 업데이트를 통해 업데이트가 수신되면 카탈로그가 자동으로 새로고침됩니다. 업데이트는 일반적으로 한 시간 내에 완료됩니다. 업데이트가 진행 중인 경우 가장 최근 업데이트가 시작된 시간이 표시됩니다. 진행 중인 업데이트가 없으면 가장 최근 업데이트가 시작되고 완료된 시간이 표시됩니다.

## 고급 검색을 기반으로 컬렉션 또는 제외 만들기 {#save-as}

카탈로그 검색 페이지의 고급 검색([](/help/main/c-recommendations/c-products/collections.md)[](/help/main/c-recommendations/c-products/exclusions.md)추천[!UICONTROL  > ]카탈로그 검색[!UICONTROL  > ]고급 검색[!UICONTROL )을 사용하여 ]컬렉션[!UICONTROL 이나 ]제외를 만들 수 있습니다.

1. 수행 [고급 검색](#advanced-search).

1. 클릭 **[!UICONTROL 다른 이름으로 저장]**&#x200B;를 클릭한 다음 **[!UICONTROL 컬렉션]** 또는 **[!UICONTROL 제외]**.

   ![다른 이름으로 저장 옵션](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >다음 [!UICONTROL 고급 검색] 기능은 대소문자를 구분하지 않습니다. 그러나 배송 시 반환되는 제품은 대/소문자를 구분하는 검색을 기반으로 합니다. 이러한 불일치로 인해 혼동이 발생할 수 있습니다. 를 사용하는 결과를 기반으로 컬렉션이나 제외를 작성할 때에는 대소문자 구분을 고려해야 합니다. [!UICONTROL 고급 검색] 기능을 사용할 수 있습니다. 예를 들어, &quot;Holiday&quot;를 검색할 때 초기 검색 목록에는 &quot;Holiday&quot;와 &quot;holiday&quot;를 포함하는 결과가 나열됩니다. 그런 다음 &quot;holiday&quot;를 포함하는 제품을 반환할 의도로 카탈로그를 만드는 경우 &quot;holiday&quot;를 포함하는 제품만 반환됩니다. &quot;Holiday&quot;를 포함하는 제품은 반환되지 않습니다. 제외도 유사한 방식으로 처리됩니다.

## 환경 변경

[환경](/help/main/administrating-target/environments.md) 쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성할 수 있습니다.

1. 환경 링크를 클릭합니다.

   ![환경 링크](/help/main/c-recommendations/c-products/assets/environment.png)

1. 원하는 환경을 선택합니다.

## 카탈로그 검색 페이지 수정(필터 및 열)

일시적으로 [!UICONTROL 카탈로그 검색] 현재 세션에 대한 페이지입니다.

### 필터 수정

필터 패싯을 [!UICONTROL 카탈로그 검색] 페이지.

1. 에서 **[!UICONTROL 필터]** 패널, **[!UICONTROL 수정]**.

   ![필터 수정 링크](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. 원하는 검색 패싯(ID, 이름, 메시지 등)을 선택한 다음 을 클릭합니다 **[!UICONTROL 저장]**.

   ![필터 추가](/help/main/c-recommendations/c-products/assets/add-filters.png)

추가 필터 패싯은 현재 세션에서만 사용할 수 있습니다.

### 열 수정

에서 활성 열을 일시적으로 수정할 수 있습니다 [!UICONTROL 카탈로그 검색] 페이지.

1. 을(를) 클릭합니다. **[!UICONTROL 열]** 링크를 클릭합니다.

   ![열 옵션](/help/main/c-recommendations/c-products/assets/columns.png)

1. (조건부) 활성 열의 순서를 변경하려면 **[!UICONTROL 활성 열]** 섹션을 원하는 순서로 표시합니다.

1. (조건부) **[!UICONTROL 활성 열]** 변환 후 **[!UICONTROL 비활성 열]** 원하는 대로 (또는 그 반대로) 선택할 수 있습니다.

   활성 섹션에서 비활성 섹션으로 이동할 열 옆에 있는 삭제 아이콘( x )을 클릭할 수도 있습니다.

변경한 사항이 현재 세션에만 적용됩니다.
