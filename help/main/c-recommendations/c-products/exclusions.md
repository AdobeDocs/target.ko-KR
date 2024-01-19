---
keywords: 제외
description: Adobe에서 제외를 만드는 방법 알아보기 [!DNL Target] Recommendations을 사용하십시오.
title: Recommendations 활동에서 제외를 사용하려면 어떻게 합니까?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 34%

---

# 제외

에서 제외 만들기 [!DNL Adobe Target Recommendations] 방문자에게 제품이나 콘텐츠를 추천하지 않도록 하려는 경우. 제외는 방문자에게 권장해서는 안 되는 제품 또는 콘텐츠의 하위 집합입니다.

제외는 전체 계정에서 사용할 수 있습니다. 를 만들 때 각 경험에 대해 특정 컬렉션을 지정하는 컬렉션과 달리 [!UICONTROL Recommendations] 활동, 제외는 계정의 모든 활동에 적용됩니다. 활동을 만드는 동안 제외 그룹을 할당할 수 있는 옵션이 없습니다.

제외를 사용하는 몇 가지 예는 다음과 같습니다.

* 단종된 제품
* 가을/겨울 카탈로그는 이제 온라인에 표시되어야 하는 유일한 카탈로그입니다. 여름 카탈로그의 모든 항목은 더 이상 구매할 수 없습니다.
* 대부분의 페이지/화면에서 권장하기에 부적절할 수 있는 항목(성인용품, NC-17 영화 등)
* 메타데이터 필드가 완료되지 않은 제품(썸네일, 가격 또는 기타 중요한 메타데이터 누락)
* 권장해서는 안 되는 제품(시스템에 어떤 제품에 대한 SKU가 있지만 구매 가능한 항목이 아닐 수 있거나, QA 팀이 실제로 어떤 제품을 주문하지 않고 구매를 시뮬레이션할 수 있는 가짜 SKU일 수 있음 등)

>[!IMPORTANT]
>
>제외 규칙은 모든 환경에 전역적으로 적용됩니다.
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

## 제외 만들기

1. 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL 제외]** 기존 제외 목록을 표시합니다.

   ![exclusions_list 이미지](assets/exclusions_list.png)

   [!UICONTROL 제외] 목록 보기의 각 제외에 대해 보고된 &quot;항목 수&quot;는 구성된 기본 권장 사항 [호스트 그룹](/help/main/administrating-target/hosts.md)(환경)에서 해당 제외에 대한 규칙과 일치하는 제품의 수입니다. 다음을 참조하십시오 [설정](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 기본 호스트 그룹을 변경합니다.

1. 클릭 **[!UICONTROL 제외 만들기]**.

1. (조건부) **[!UICONTROL 환경]** 제외를 만들거나 업데이트하여 해당 환경에서 제외의 콘텐츠를 미리 보는 동안 필터링합니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

   ![제외 만들기](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. 제외 입력 **[!UICONTROL 이름]** 원할 경우 설명을 입력합니다.

1. 규칙 빌더를 사용하여 제외 항목을 만듭니다.

   규칙 목록에서 매개 변수를 선택하고 연산자를 선택한 다음, 하나 이상의 값을 입력하여 제품을 식별하십시오. 여러 값을 입력할 경우에는 쉼표로 구분합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 고급 검색을 사용하여 제외 만들기

다음을 사용하여 제외를 만들 수도 있습니다. [!UICONTROL 고급 검색] 다음에 있음 [카탈로그 검색](/help/main/c-recommendations/c-products/catalog-search.md#save-as) 페이지 ( [!UICONTROL Recommendations] > [!UICONTROL 카탈로그 검색] > [!UICONTROL 고급 검색]).

![다른 이름으로 저장 대화 상자](/help/main/c-recommendations/c-products/assets/save-as.png)

예를 들어 &quot;id > 포함&quot;을 사용하여 검색을 작성한 후 [!UICONTROL 다른 이름으로 저장] > [!UICONTROL 제외]를 클릭할 수 있습니다.

>[!IMPORTANT]
>
>다음 [!UICONTROL 고급 검색] 기능은 대소문자를 구분하지 않습니다. 그러나 배송 시 반환되는 제품은 대소문자를 구분하는 검색을 기반으로 합니다. 이러한 불일치로 인해 혼동이 발생할 수 있습니다. 따라서 고급 검색 기능을 사용하는 결과를 기반으로 제외를 작성할 때에는 대소문자 구분을 고려해야 합니다. 예를 들어, &quot;Holiday&quot;를 검색할 때 초기 검색 목록에는 &quot;Holiday&quot;와 &quot;holiday&quot;를 포함하는 결과가 나열됩니다. 그런 다음 &quot;holiday&quot;를 포함하는 제품을 제외할 의도로 제외를 만드는 경우 &quot;holiday&quot;를 포함하는 제품만 제외됩니다. &quot;Holiday&quot;를 포함하는 제품은 제외되지 않습니다.

## 제외 편집, 복사 또는 삭제

목록에서 원하는 제외 항목을 마우스로 가리킨 다음, 적절한 아이콘(편집, 복사 또는 삭제)을 클릭합니다.

![제외에 대한 마우스로 가리키기 아이콘](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

기존 제외를 복사하여 수정할 수 있는 중복 제외를 생성할 수 있습니다. 이를 통해 적은 노력으로 유사한 제외를 만들 수 있습니다.

제외는 전체 계정에서 사용할 수 있습니다. 제외를 삭제하기 전에 이를 고려하십시오. 삭제된 제외는 복구할 수 없습니다.

## 교육 비디오: Recommendations에서 컬렉션 및 제외 만들기(7:05) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 컬렉션 만들기
* 제외 만들기

>[!VIDEO](https://video.tv.adobe.com/v/27689)
