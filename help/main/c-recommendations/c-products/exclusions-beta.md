---
keywords: 제외
description: ' [!DNL Target Recommendations] 에서 제외를 만들어 제품 또는 콘텐츠를 방문자에게 추천하지 않도록 하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL Recommendations] 활동에서 제외를 사용하려면 어떻게 합니까?'
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: fb3c63b4-08be-4dac-b5a1-c6c1ecd4c4b3
source-git-commit: b7c7e8d85f7f39024ed5e57177e5c9f628460e9c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 14%

---

# 제외

제품 또는 콘텐츠가 방문자에게 추천되지 않도록 하려면 [!DNL Adobe Target Recommendations]에서 제외를 만드십시오. 제외는 방문자에게 권장해서는 안 되는 제품 또는 콘텐츠의 하위 집합입니다.

제외는 전체 계정에서 사용할 수 있습니다. [!UICONTROL Recommendations] 활동을 만들 때 각 경험에 대해 특정 컬렉션을 지정하는 컬렉션과 달리 계정의 모든 활동에는 제외가 적용됩니다. 활동을 만드는 동안 제외 그룹을 할당할 수 있는 옵션이 없습니다.

제외를 사용하는 몇 가지 예는 다음과 같습니다.

* 단종된 제품
* 가을 및 겨울 카탈로그는 이제 온라인에 표시되어야 하는 유일한 카탈로그입니다. 여름 카탈로그의 모든 항목은 더 이상 구매할 수 없습니다.
* 대부분의 페이지 또는 화면에서 권장하기에 부적절할 수 있는 항목(성인용품, NC-17 영화 등).
* 메타데이터 필드가 완료되지 않은 제품(썸네일, 가격 또는 기타 중요한 메타데이터 누락).
* 권장해서는 안 되는 제품(시스템에 특정 용도로 SKU가 있을 수 있지만 구매 가능한 항목은 아닙니다. 또는 QA 팀이 실제로 주문 등을 하지 않고 구매를 시뮬레이션하는 것은 가짜 SKU일 수 있습니다.

>[!IMPORTANT]
>
>제외 규칙은 모든 [환경](/help/main/administrating-target/environments.md)에 전체적으로 적용됩니다.
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

## 제외 만들기

1. 기존 제외 목록을 표시하려면 **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Exclusions] 목록 보기의 각 제외에 대해 보고된 &quot;항목 수&quot;는 구성된 기본 Recommendations [호스트 그룹](/help/main/administrating-target/hosts.md)(환경) 내에서 해당 제외에 대한 규칙과 일치하는 제품의 수입니다. 기본 호스트 그룹을 변경하는 방법에 대한 자세한 내용은 *Adobe Target 개발자 안내서*&#x200B;의 [계획 및 구현 [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank}을 참조하십시오.

1. (조건부) 제외를 만들거나 업데이트하여 해당 환경에서 제외 콘텐츠를 미리 보는 동안 **[!UICONTROL Show Filters]** 아이콘(![필터 표시 아이콘](/help/main/assets/icons/Filter.svg))을 클릭한 다음 **[!UICONTROL Environment]** 드롭다운 목록에서 원하는 [환경](/help/main/administrating-target/environments.md)을(를) 선택합니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

1. **[!UICONTROL Create Exclusion]** 아이콘을 클릭합니다.

1. 제외 **[!UICONTROL Name]**&#x200B;을(를) 입력하고 선택적 설명을 입력하십시오.

1. 규칙 빌더를 사용하여 제외 항목을 만듭니다.

   [!UICONTROL Rules] 목록에서 매개 변수를 선택하고 연산자를 선택한 다음 하나 이상의 값을 입력하여 제품을 식별하십시오. 여러 값을 입력할 경우에는 쉼표로 구분합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## 제외 편집, 복사 또는 삭제

목록에서 원하는 제외 옆에 있는 추가 작업 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg))을 클릭한 다음 해당 아이콘([!UICONTROL Edit], [!UICONTROL Copy] 또는 [!UICONTROL Delete])을 클릭합니다.

기존 제외를 복사하여 수정할 수 있는 중복 제외를 생성할 수 있습니다. 이 옵션을 사용하면 적은 노력으로 유사한 제외를 만들 수 있습니다.

제외는 전체 계정에서 사용할 수 있습니다. 제외를 삭제하기 전에 이 주의 사항을 고려해야 합니다. 삭제된 제외는 복구할 수 없습니다.

## 교육 비디오: Recommendations(7:05)에서 컬렉션 및 제외 만들기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 컬렉션 만들기
* 제외 만들기

>[!VIDEO](https://video.tv.adobe.com/v/27689)
