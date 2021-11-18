---
keywords: 행동 데이터 소스;analytics;권장 사항;기준;제품 변수
description: 사용 방법 알아보기 [!DNL Adobe Analytics] as the behavioral data source to use the view-based and/or purchase-based behavioral data from [!DNL Analytics] in [!DNL Target Recommendations].
title: 사용 방법 [!DNL Adobe Analytics] with [!DNL Target Recommendations]?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2dc134d064b0707bcc8a24a08e9831e1cfa0b08e
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 2%

---

# ![PREMIUM](/help/assets/premium.png) 사용 [!DNL Adobe Analytics] with [!DNL Recommendations]

사용 [!DNL Adobe Analytics] 을 동작 데이터 소스로 사용하면 클라이언트가 [!DNL Analytics] in [!DNL Adobe Target] [!DNL Recommendations] 활동. 이 기능은 [!DNL Target Recommendations] 새 설정이며 [!DNL Analytics] 에는 사용할 많은 이전 데이터가 있습니다.

사용 [!DNL Analytics] 는 동작 데이터 소스가 사용자 행동에 대한 풍부한 정보 소스 역할을 할 수 있습니다. 이 정보에는 타사 소스 또는 피드의 데이터만 공유되는 데이터가 포함될 수 있습니다 [!DNL Analytics].

While [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations]에는 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 단추가 있습니다. [!UICONTROL mbox] 또는 [!UICONTROL Analytics]. 기준을 만들려면 [!UICONTROL Recommendations] > [!UICONTROL 기준] > [!UICONTROL 기준 만들기] > [!UICONTROL 기준 만들기]. 자세한 내용은 [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

![동작 데이터 소스 단추](assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 단추가 계정에 표시되지 않으면 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Target의 Analytics 데이터에 대한 사용 사례

사용 [!DNL Analytics] 를 권장 사항에 대한 동작 데이터 소스로 사용하면 모든 항목을 포함하는 엔티티 페이지에 태깅하지 않고 특정 사용 사례를 배포할 수도 있습니다 [!DNL Target] 엔티티 매개 변수. 이렇게 하려면 특정 전제 조건을 충족해야 하지만 &quot;제품 변수&quot;의 가용성은 해당 기능이 원활하게 작동하려면 가장 중요한 기능입니다. 일반 eVar 및 Prop로 인해 이 핸드셰이크가 다음 사이 자동으로 수행되지는 않습니다 [!DNL Analytics] 및 [!DNL Target].

다음을 사용할 수 있습니다 [!DNL Analytics] 행동 데이터 소스로 다음 작업을 수행할 수 있습니다.

* 를 사용하여 지난 달에 동일한 카테고리에서 다른 사용자가 구매한 항목을 기반으로, 제품 세부 사항 페이지의 사용자에게 소매 사이트의 권장 사항을 표시합니다 [!DNL Analytics] 데이터.
* 미디어 사이트의 홈 화면에 현재 트렌드를 나타내는 특정 카테고리의 가장 인기 있는 콘텐츠에 대한 컨텐츠를 표시합니다 [!DNL Analytics] 데이터.

## 의 구현 [!DNL Analytics]

다음 섹션에서는 [!DNL Analytics] 합니다.

### 전제 조건: 에서 제품 변수 설정 [!DNL Analytics]

에서 제품 변수 구현 [!DNL Analytics] 에 필요한 속성을 사용하여 [!DNL Target Recommendations].

A [!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 안내서를 처리합니다. 나중에 이러한 값은 [!DNL Target] 각 UI에 대해 [!DNL Target] 엔티티 값.

>[!NOTE]
>
>컨텐츠 사이트인 경우 각 컨텐츠 조각을 &quot;제품&quot;으로 처리하여 해당 컨텐츠에 대한 연관된 속성을 속성으로 전달해야 합니다. 이러한 속성에는 작성자 이름, 게시 날짜, 컨텐츠 제목, 릴리스 월 등이 포함될 수 있습니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항을 기반으로 비즈니스에 의해 결정되어야 합니다.

제품 변수를 설정하는 방법에 대한 자세한 내용은 다음을 참조하십시오 [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) 에서 *Adobe Analytics 구현* 안내서. 해당 설명서의 일부 노트에는 배포하고 있는 팀의 재량이 필요합니다(예: 카테고리). 항상 [!DNL Adobe] 이 활동을 수행하기 전에

### 고려 사항

[!DNL Analytics] 데이터는 일별 피드를 통해 전송됩니다. 동작 결과를 사이트의 권장 사항 결과 내에 반영하려면 최대 24시간이 걸릴 수 있습니다. 모든 경우의 [!DNL Recommendations] 기준 설정, 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

사용할 데이터 소스를 신속하게 결정하려면 사용자가 매일 생성하는 유기 데이터가 많거나 기록 데이터에 의존하지 않아도 되는 경우 [!DNL Target] 행동 데이터 소스로서의 mbox가 적합할 수 있습니다. 최근에 생성된 유기 데이터의 가용성이 낮은 경우 다음을 고려하려는 경우 [!DNL Analytics] 데이터, 사용 [!DNL Analytics] 행동 데이터 소스가 적합합니다.

이제 이러한 변수를 [!DNL Target] 를 참조하십시오.

## 에서 구현 [!DNL Target]

1. in [!DNL Target]를 클릭합니다. **[!UICONTROL Recommendations]**&#x200B;를 클릭한 다음 **[!UICONTROL 피드 를 참조하십시오]** 탭.

   ![피드](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. 클릭 **[!UICONTROL 피드 만들기]**.

1. 선택 **[!UICONTROL Analytics 분류]**&#x200B;를 입력한 다음 보고서 세트를 지정합니다.

   ![Analytics 분류 옵션](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. 클릭 **[!UICONTROL 다음]** 앞으로 나아가다 **[!UICONTROL 예약]** 설정, 피드의 빈도 기간을 선택합니다.

   * [!UICONTROL 일별]
   * [!UICONTROL 주별]
   * [!UICONTROL 2주마다]
   * [!UICONTROL 절대 안 함]

   피드를 처리할 시간을 선택할 수도 있습니다.

1. 클릭 **[!UICONTROL 다음]** 앞으로 나아가다  **[!UICONTROL 매핑]** 설정, 필드 열 헤더를 적절한 [!UICONTROL Recommendations] 필드 이름.

   ![매핑 섹션](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## FAQ

사용 시 다음 FAQ를 고려하십시오 [!DNL Analytics] with [!DNL Target]:

### 은 `entity.id` 및 `entity.categoryId` 내에 전달해야 하는 값 [!DNL Target] mbox 호출?

예, 이 두 값은 여전히 필요합니다. 나머지 속성은 를 통해 전달할 수 있습니다 [!DNL Analytics] 피드, 이 문서에서 설명한 대로 사용할 수 있습니다.

### 엔티티 매개 변수 일치 프로필 속성 과 같은 동적 포함 규칙을 [!DNL Analytics] 피드 접근 방식?

네, 가능합니다. 메서드는 를 사용할 때 비슷합니다 [!DNL Target] 독립. 그러나 이 경우 타이밍 인자에 대해 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 페이지에서 훨씬 나중에 표시될 수 있는 데이터 레이어에 따라 다릅니다.
