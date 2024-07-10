---
keywords: 컬렉션;타깃팅
description: 에서 제품 또는 항목의 컬렉션을 사용하는 방법을 알아봅니다. [!DNL Target Recommendations].
title: Recommendations 활동에서 컬렉션을 사용하려면 어떻게 해야 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 31cf23a52c331eabad0e5f6423eeeca84df87625
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 26%

---

# 컬렉션

컬렉션은 권장 사항에 적합한 제품 또는 항목 세트입니다. 컬렉션의 일부가 되기 위해 항목에서 충족해야 하는 조건을 지정하여 컬렉션을 정의합니다.

일반적으로 컬렉션은 하나의 제품 컬렉션과 같이 유사하거나 관련성이 있는 항목들의 세트입니다. 그러나 어떤 항목이든 특정 가격 범위나 색상 또는 특정 지역에서 관심을 가질 수 있는 항목 등, 비즈니스에 의미가 있는 카테고리로 그룹화할 수 있습니다.

제품을 논리 버킷으로 구성하려면 컬렉션을 사용하십시오. 예를 들어 일부 항목을 한 지역에서는 사용할 수 있지만 다른 지역에서는 사용할 수 없는 경우 방문자의 지역에서 사용할 수 없는 항목을 제외하는 컬렉션을 만들 수 있습니다. 컬렉션을 사용하여 시즌별 항목을 구성하거나 비즈니스에 적용되는 다른 조직 매개 변수를 구성할 수도 있습니다.

[백업 권장 사항](/help/main/c-recommendations/c-algorithms/backup-recs.md) 권장 사항 내의 각 기준에 대해 생성된 항목도 이 컬렉션을 사용하므로, 해당 컬렉션의 항목만 백업 권장 사항에 포함됩니다. 컬렉션을 사용하여 특정 위치에 표시되는 것이 적합한 제품만 표시되게 할 수 있습니다.

컬렉션은 각 기준이 실행될 때마다 재구성 또는 업데이트됩니다.

항목을 카탈로그에 그룹화한 다음 각 컬렉션에 대한 개별 권장 사항을 만들 수 있습니다.

포함 기준을 사용하면 유사한 작업들을 컬렉션으로서 수행할 수 있지만 활동을 만들 때마다 이러한 작업들을 설정해야 합니다. 컬렉션을 사용하면 항목 세트를 한 번만 만든 다음 다시 설정하지 않고도 적절하게 사용할 수 있습니다.

를 만들거나 편집할 때 [!DNL Recommendations] 활동, 컬렉션 이름이 [!UICONTROL Criteria] 활동 다이어그램의 레이블입니다.

>[!NOTE]
>
>컬렉션은 [!UICONTROL Recently Viewed Items] 권장 사항 키.

## 컬렉션 만들기 {#task_1256DFF6842141FCAADD9E1428EF7F08}

컬렉션을 만들어 권장 사항에 표시할 제품 또는 콘텐츠를 구성합니다.

1. 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** 기존 컬렉션 목록을 표시합니다.

   ![컬렉션 목록](assets/collections-list.png)

   다음 [!UICONTROL Collections] 페이지에 기존 컬렉션 목록이 표시됩니다. 새 컬렉션은 [!UICONTROL Create Collection] 단추를 클릭합니다. 원하는 컬렉션 옆에 있는 줄임표 아이콘을 클릭한 다음 원하는 옵션을 클릭하여 기존 컬렉션을 편집, 복사 및 삭제할 수도 있습니다.

   의 각 컬렉션에 대해 &quot;항목 수&quot;가 보고됨 [!UICONTROL Collections] list view는 구성된 기본 Recommendations 내에서 해당 컬렉션에 대한 규칙과 일치하는 제품의 수입니다 [호스트 그룹](/help/main/administrating-target/hosts.md) (환경). 다음을 참조하십시오 [설정](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} 기본 호스트 그룹을 변경합니다.

1. **[!UICONTROL Create Collection]** 아이콘을 클릭합니다.

   ![컬렉션 만들기](/help/main/c-recommendations/c-products/assets/create-collection.png)

1. Type a **[!UICONTROL Name]** 컬렉션에 사용됩니다.

   선택 사항을 입력할 수도 있습니다 **[!UICONTROL Description]**.

1. (조건부) 다음을 선택합니다. [환경](/help/main/administrating-target/environments.md) 다음에서 **[!UICONTROL Environment]** 컬렉션을 만들거나 업데이트하여 해당 환경에서 컬렉션의 컨텐츠를 미리 보는 동안 필터링합니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

1. 컬렉션을 만드는 데 사용되는 규칙을 설정합니다.

   예를 들어 제품 ID 또는 카테고리, 순익 또는 목록의 기타 매개 변수를 기반으로 컬렉션을 만들 수 있습니다.

   여러 매개 변수를 사용하는 규칙을 추가하여 컬렉션을 정의할 수 있습니다. 여러 규칙은 AND 연산자로 연결됩니다. 컬렉션을 적용하려면 지정된 모든 규칙이 일치해야 합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

<!-- ## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. -->

## 컬렉션 편집, 복사 또는 삭제

다음을 클릭합니다. **생략 부호** 목록에서 원하는 컬렉션 옆에 있는 아이콘을 클릭한 다음, 해당 아이콘(편집, 복사 또는 삭제)을 클릭합니다.

![마우스로 가리키기 아이콘: 편집, 복사 및 삭제](/help/main/c-recommendations/c-products/assets/hover-icons-new.png)

기존 컬렉션을 복사하여 수정할 수 있는 중복 컬렉션을 만들 수 있습니다. 이를 통해 적은 노력으로 유사한 컬렉션을 만들 수 있습니다.

컬렉션은 전체 계정에서 사용할 수 있습니다. 컬렉션을 삭제하기 전에 이를 고려해야 합니다. 삭제된 컬렉션은 복구할 수 없습니다.

## 다음에서 컬렉션 사용 [!DNL Recommendations] 활동

1. 위에서 언급한 방법 중 하나를 사용하여 컬렉션을 만듭니다.

1. 클릭 **[!UICONTROL Activities]** 및 [새 Recommendations 만들기](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) 활동 또는 기존 활동을 편집합니다.

1. 기준과 디자인을 선택하면 [!UICONTROL Options] 원하는 컬렉션을 선택할 수 있는 페이지가 표시됩니다.

   ![컬렉션 옵션 선택](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (조건부) 기존 컬렉션 설정을 변경하려면 **[!UICONTROL Experiences]** 페이지(3단계 안내 워크플로의 2단계)에서 권장 사항을 배치한 위치를 클릭하고 **[!UICONTROL Change Collection]**&#x200B;를 클릭한 다음 원하는 컬렉션을 선택합니다.

   ![컬렉션 옵션 변경](/help/main/c-recommendations/c-products/assets/change-collection.png)