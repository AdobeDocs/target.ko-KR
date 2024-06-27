---
keywords: 제외
description: 에서 제외를 만드는 방법 알아보기 [!DNL Target Recommendations] 방문자에게 제품이나 콘텐츠를 추천하지 않도록 하려는 경우.
title: 에서 제외를 사용하는 방법 [!UICONTROL Recommendations] 활동?
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6eaf89ef71ea3448584dcdadc926c45dba77504
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 26%

---

# 제외

에서 제외 만들기 [!DNL Adobe Target Recommendations] 방문자에게 제품이나 콘텐츠를 추천하지 않도록 하려는 경우. 제외는 방문자에게 권장해서는 안 되는 제품 또는 콘텐츠의 하위 집합입니다.

제외는 전체 계정에서 사용할 수 있습니다. 를 만들 때 각 경험에 대해 특정 컬렉션을 지정하는 컬렉션과 달리 [!UICONTROL Recommendations] 활동, 제외는 계정의 모든 활동에 적용됩니다. 활동을 만드는 동안 제외 그룹을 할당할 수 있는 옵션이 없습니다.

제외를 사용하는 몇 가지 예는 다음과 같습니다.

* 단종된 제품
* 가을 및 겨울 카탈로그는 이제 온라인에 표시되어야 하는 유일한 카탈로그입니다. 여름 카탈로그의 모든 항목은 더 이상 구매할 수 없습니다.
* 대부분의 페이지 또는 화면에서 권장하기에 부적절할 수 있는 항목(성인용품, NC-17 영화 등).
* 메타데이터 필드가 완료되지 않은 제품(썸네일, 가격 또는 기타 중요한 메타데이터 누락).
* 권장해서는 안 되는 제품(시스템에 특정 용도로 SKU가 있을 수 있지만 구매 가능한 항목은 아닙니다. 또는 QA 팀이 실제로 주문 등을 하지 않고 구매를 시뮬레이션하는 것은 가짜 SKU일 수 있습니다.

>[!IMPORTANT]
>
>제외 규칙은 모든 항목에 전체적으로 적용됩니다 [환경](/help/main/administrating-target/environments.md).
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

## 제외 만들기

1. 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** 기존 제외 목록을 표시합니다.

   ![exclusions_list 이미지](assets/exclusions-list.png)

   의 각 제외에 대해 보고된 &quot;항목 수&quot; [!UICONTROL Exclusions] 목록 보기는 구성된 기본 Recommendations 내에서 해당 제외에 대한 규칙과 일치하는 제품의 수입니다 [호스트 그룹](/help/main/administrating-target/hosts.md) (환경). 다음을 참조하십시오 [계획 및 구현 [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank} 다음에서 *Adobe Target 개발자 안내서* 기본 호스트 그룹을 변경하는 방법에 대한 정보입니다.

1. (조건부) [!UICONTROL Filter] 아이콘을 클릭한 다음 원하는 아이콘을 선택합니다 [환경](/help/main/administrating-target/environments.md) 다음에서 **[!UICONTROL Environment]** 해당 환경에서 제외의 컨텐츠를 미리 보기 위해 제외를 만들거나 업데이트하는 동안 드롭다운 목록을 표시합니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

   ![제외 만들기](/help/main/c-recommendations/c-products/assets/choose-environment.png)

1. **[!UICONTROL Create Exclusion]** 아이콘을 클릭합니다.

   ![제외 만들기 대화 상자](/help/main/c-recommendations/c-products/assets/create-exclusion.png)

1. 제외 입력 **[!UICONTROL Name]** 원할 경우 설명을 입력합니다.

1. 규칙 빌더를 사용하여 제외 항목을 만듭니다.

   규칙 목록에서 매개 변수를 선택하고 연산자를 선택한 다음, 하나 이상의 값을 입력하여 제품을 식별하십시오. 여러 값을 입력할 경우에는 쉼표로 구분합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

## 고급 검색을 사용하여 제외 만들기

다음을 사용하여 제외를 만들 수도 있습니다. [!UICONTROL Advanced Search] 다음에 있음 [카탈로그 검색](/help/main/c-recommendations/c-products/catalog-search.md#save-as) 페이지 ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![다른 이름으로 저장 대화 상자](/help/main/c-recommendations/c-products/assets/save-as.png)

예를 들어 &quot;id > 포함&quot;을 사용하여 검색을 작성한 후 [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>다음 [!UICONTROL Advanced Search] 기능은 대소문자를 구분하지 않습니다. 그러나 배송 시 반환되는 제품은 대소문자를 구분하는 검색을 기반으로 합니다. 이러한 불일치로 인해 혼동이 발생할 수 있습니다. 따라서 고급 검색 기능을 사용하는 결과를 기반으로 제외를 작성할 때에는 대소문자 구분을 고려해야 합니다. 예를 들어, &quot;Holiday&quot;를 검색할 때 초기 검색 목록에는 &quot;Holiday&quot;와 &quot;holiday&quot;를 포함하는 결과가 나열됩니다. 그런 다음 &quot;holiday&quot;를 포함하는 제품을 제외할 의도로 제외를 만드는 경우 &quot;holiday&quot;를 포함하는 제품만 제외됩니다. &quot;Holiday&quot;를 포함하는 제품은 제외되지 않습니다.

## 제외 편집, 복사 또는 삭제

다음을 클릭합니다. **생략 부호** 목록에서 원하는 제외 옆에 있는 아이콘을 클릭한 다음 편집, 복사 또는 삭제와 같은 적절한 아이콘을 클릭합니다.

![옵션: 편집, 복사 및 삭제](/help/main/c-recommendations/c-products/assets/edit-copy-delete.png)

기존 제외를 복사하여 수정할 수 있는 중복 제외를 생성할 수 있습니다. 이 옵션을 사용하면 적은 노력으로 유사한 제외를 만들 수 있습니다.

제외는 전체 계정에서 사용할 수 있습니다. 제외를 삭제하기 전에 이 주의 사항을 고려해야 합니다. 삭제된 제외는 복구할 수 없습니다.

## 교육 비디오: Recommendations에서 컬렉션 및 제외 만들기(7:05) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 컬렉션 만들기
* 제외 만들기

>[!VIDEO](https://video.tv.adobe.com/v/27689)