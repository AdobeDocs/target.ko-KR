---
keywords: 제외
description: '[!DNL Target Recommendations]에서 제외를 만들어 제품 또는 콘텐츠를 방문자에게 추천하지 않도록 하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL 권장 사항] 활동에서 제외를 사용하는 방법은 무엇입니까?'
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
TQID: 'https://experienceleague.adobe.com/6-PWkqq5eXAwyLcGGbSqSZmFdJa85yU3x7FPNEt8-2o'
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
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 3883dc9752db0a2427f70cb3036fe060c440361a
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 6%
---
# 제외 {#exclusions}

>[!BEGINSHADEBOX]

**이 페이지에서:** 제품 또는 콘텐츠를 방문자에게 추천하지 않도록 [!DNL Adobe Target Recommendations]에서 제외를 만들고 관리하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

제외는 방문자에게 권장해서는 안 되는 제품 또는 콘텐츠의 하위 집합입니다. 제외는 전체 계정에서 사용할 수 있습니다. [!DNL Recommendations] 활동이 만들어질 때 각 경험에 대해 선택되는 컬렉션과 달리, 제외는 계정의 모든 활동에 적용되며 활동을 만드는 동안 제외 그룹을 할당할 수 없습니다.

제외는 일반적으로 다음 경우에 사용됩니다.

* 단종된 제품
* 더 이상 사용할 수 없는 카탈로그의 항목. 예를 들어 가을 및 겨울 카탈로그만 온라인 상태여야 하는 경우 여름 카탈로그의 모든 항목을 구입할 수 없습니다.
* 대부분의 페이지 또는 화면에서 권장하기에 부적절할 수 있는 항목(성인용품, NC-17 영화 등).
* 메타데이터 필드가 완료되지 않은 제품(썸네일, 가격 또는 기타 중요한 메타데이터 누락).
* 시스템에 존재하지만 구매 가능한 품목이 아닌 SKU 또는 QA 팀이 주문 없이 구매를 시뮬레이션하기 위해 사용하는 가짜 SKU와 같이 권장해서는 안 되는 제품입니다.

>[!IMPORTANT]
>
>제외 규칙은 모든 [환경](/help/main/administrating-target/environments.md)에 전체적으로 적용됩니다.
>
>정적 및 동적 제외 규칙에 대한 자세한 정보, 예제 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#inclusion-rules)을 참조하십시오.

## 제외 만들기

제외 규칙은 한 번 정의된 후 계정의 모든 [!DNL Recommendations] 활동에 적용됩니다.

1. 기존 제외 목록을 표시하려면 **[!UICONTROL 권장 사항]** > **[!UICONTROL 제외]**&#x200B;를 클릭하십시오.

   >[!NOTE]
   >
   >**[!UICONTROL 제외]** 목록 보기의 각 제외에 대해 보고된 &quot;항목 수&quot;는 구성된 기본 권장 사항 [호스트 그룹](/help/main/administrating-target/hosts.md)(환경)에서 해당 제외에 대한 규칙과 일치하는 제품의 수입니다. 기본 호스트 그룹을 변경하는 방법에 대한 자세한 내용은 *Adobe Target 개발자 안내서*&#x200B;의 [계획 및 구현 [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank}을 참조하십시오.


1. **[!UICONTROL 필터 표시]** 아이콘( ![필터 표시 아이콘](/help/main/assets/icons/Filter.svg) )을 클릭한 다음 **[!UICONTROL 환경]** 드롭다운 목록에서 원하는 [환경](/help/main/administrating-target/environments.md)을(를) 선택하여 해당 환경에서 제외의 내용을 미리 봅니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

   필터 패널이 열려 있고 환경 목록이 있는 ![제외 페이지](../assets/exclusions_2.png)

1. **[!UICONTROL 제외 만들기]**&#x200B;를 클릭합니다.

   ![제외 만들기 단추가 있는 제외 페이지](../assets/exclusions_1.png)

1. 제외 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오. 원할 경우 설명을 입력할 수도 있습니다.

1. 규칙 빌더를 사용하여 제외를 정의합니다.

   **[!UICONTROL 규칙]** 목록에서 매개 변수를 선택하고 연산자를 선택한 다음 하나 이상의 값을 입력하여 제품을 식별하십시오. 여러 값을 입력할 경우에는 쉼표로 구분합니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 목록에서 원하는 제외 옆의 추가 작업 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg) )을 클릭한 다음, 적절한 옵션(**[!UICONTROL 편집]**, **[!UICONTROL 복사]** 또는 **[!UICONTROL 삭제]**)을 클릭합니다.

   추가 작업 메뉴가 열려 편집, 복사 및 삭제를 표시하는 ![제외 목록](../assets/exclusions_3.png)

<!--
## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded.
-->


## 교육 비디오: 권장 사항(7:05)에서 컬렉션 및 제외 만들기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 컬렉션 만들기
* 제외 만들기

>[!VIDEO](https://video.tv.adobe.com/v/27689)
