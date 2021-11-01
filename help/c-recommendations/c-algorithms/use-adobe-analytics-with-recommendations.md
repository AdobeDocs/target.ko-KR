---
keywords: 행동 데이터 소스;analytics;권장 사항;기준;제품 변수
description: Adobe Analytics을 Analytics에서 보기 기반 및/또는 구매 기반 행동 데이터를 사용하기 위해 동작 데이터 소스로 사용하는 방법을 알아봅니다. [!DNL Target] Recommendations.
title: 과 함께 Adobe Analytics을 어떻게 사용합니까? [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2a4cae206bf634bf3fbec65c5c4b289aadefede1
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 1%

---

# Recommendations와 함께 Adobe Analytics 사용

사용 [!DNL Adobe Analytics] 을 동작 데이터 소스로 사용하면 클라이언트가 [!DNL Analytics] in [!DNL Adobe Target] 권장 사항 활동. 이 기능은 [!DNL Target Recommendations] 새 설정이며 [!DNL Analytics] 는 활용할 이전 데이터가 많습니다.

사용 [!DNL Analytics] 는 동작 데이터 소스가 사용자 행동에 대한 풍부한 정보 소스 역할을 할 수 있습니다. 여기에는 타사 소스 또는 피드와만 공유되는 데이터가 포함될 수 있습니다 [!DNL Analytics].

While [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md) Recommendations에는 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 단추가 있습니다. [!UICONTROL mbox] 또는 [!UICONTROL Analytics].

![동작 데이터 소스 단추](assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 단추가 계정에 표시되지 않으면 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Target의 Analytics 데이터에 대한 사용 사례

사용 [!DNL Analytics] 권장 사항에 대한 동작 데이터 소스는 또한 다음을 모두 사용하여 엔티티 페이지에 태깅하지 않고 특정 사용 사례를 배포하는 기능을 제공합니다 [!DNL Target] 엔티티 매개 변수. 이렇게 하려면 특정 전제 조건을 충족해야 하지만 &quot;제품 변수&quot;의 가용성은 해당 기능이 원활하게 작동하려면 가장 중요한 기능입니다. 일반 eVar 및 Prop로 인해 이 핸드셰이크가 다음 사이 자동으로 수행되지는 않습니다 [!DNL Analytics] 및 [!DNL Target].

다음을 사용할 수 있습니다 [!DNL Analytics] 행동 데이터 소스로 다음 작업을 수행할 수 있습니다.

* Analytics 데이터를 사용하여 지난 달 동일한 카테고리에서 다른 사용자가 구매한 항목을 기반으로, PDP 페이지의 사용자에게 소매 사이트의 권장 사항을 표시합니다.
* 미디어 사이트의 홈 화면에 현재 트렌드를 나타내는 특정 카테고리의 가장 인기 있는 콘텐츠에 대한 컨텐츠를 표시합니다 [!DNL Analytics] 데이터.

## Analytics의 구현

다음 섹션에서는 [!DNL Analytics] 합니다.

### 전제 조건: analytics에서 제품 변수 설정

에서 제품 변수를 구현해야 합니다 [!DNL Analytics] 에 필요한 속성을 사용하여 [!DNL Target Recommendations].

A [!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 안내서를 처리합니다. 나중에 이러한 값은 [!DNL Target] 각 UI에 대해 [!DNL Target] 엔티티 값.

>[!NOTE]
>
>컨텐츠 사이트인 경우 각 컨텐츠 조각을 해당 컨텐츠에 대한 &quot;제품&quot; 및 관련 속성으로 처리해야 합니다(예: 작성자 이름, 게시 날짜, 컨텐츠 제목, 릴리스 월 등) 는 특성으로 전달해야 합니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항을 기반으로 비즈니스에 의해 결정되어야 합니다.

제품 변수를 설정하는 방법에 대한 자세한 내용은 다음을 참조하십시오 [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) 에서 *Analytics 구현 안내서*. 해당 설명서의 일부 노트에는 배포하고 있는 팀의 재량이 필요합니다(예: 카테고리). 이 활동을 수행하기 전에 항상 Adobe과 상의하는 것이 좋습니다.

### 고려 사항

[!DNL Analytics] 데이터는 일별 피드를 통해 전송됩니다. 동작 결과는 사이트의 권장 사항 결과 내에 반영되려면 최대 24시간이 걸립니다. 모든 경우의 [!DNL Recommendations] 기준 설정, 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

사용할 데이터 소스를 신속하게 결정하려면 사용자가 매일 생성하는 유기 데이터가 많은 경우 기록 데이터에 의존하지 않고 데이터를 사용해야 합니다. [!DNL Target] 행동 데이터 소스로서의 mbox가 적합할 수 있습니다. 최근에 생성된 유기 데이터의 가용성이 낮은 경우 다음을 고려하려는 경우 [!DNL Analytics] 데이터, 사용 [!DNL Analytics] 행동 데이터 소스가 적합합니다.

이제 이러한 변수를 [!DNL Target] 를 참조하십시오.

## Target에서 구현

1. Target에서 **[!UICONTROL Recommendations]**&#x200B;를 클릭한 다음 **[!UICONTROL 피드 를 참조하십시오]** 탭.

   ![피드](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. 클릭 **[!UICONTROL 피드 만들기]**.

1. 선택 **[!UICONTROL Analytics 분류]**&#x200B;를 입력한 다음 보고서 세트를 지정합니다.

   ![Analytics 분류 옵션](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. 클릭 **[!UICONTROL 매핑]**&#x200B;그런 다음 필드 열 헤더를 적절한 위치에 매핑합니다 [!UICONTROL Recommendations] 필드 이름.

   ![매핑 섹션](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## FAQ

사용 시 다음 FAQ를 고려하십시오 [!DNL Analytics] with [!DNL Target]:

### 은 `entity.id` 및 `entity.categoryId` 내에 전달해야 하는 값 [!DNL Target] mbox 호출?

예, 이 두 값은 여전히 필요합니다. 나머지 속성은 를 통해 전달할 수 있습니다 [!DNL Analytics] 피드, 이 문서에서 설명한 대로 사용할 수 있습니다.

### 엔티티 매개 변수 일치 프로필 속성 과 같은 동적 포함 규칙을 [!DNL Analytics] 피드 접근 방식?

네, 가능합니다. 메서드는 를 사용할 때 비슷합니다 [!DNL Target] 독립. 그러나 이 경우 타이밍 인자에 대해 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 페이지에서 훨씬 나중에 표시될 수 있는 데이터 레이어에 따라 다릅니다.
