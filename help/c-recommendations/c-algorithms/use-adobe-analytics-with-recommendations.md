---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: 행동 데이터 소스로 Adobe Analytics을 사용하면 클라이언트가 Adobe Recommendations의 Analytics에서 제공하는 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 수 있습니다.
title: Adobe Analytics과 Target Recommendations 사용
feature: criteria
translation-type: tm+mt
source-git-commit: 9bf30d6397fefdc85e51e2bd431ba163b10f6c09
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Recommendations과 Adobe Analytics 사용

행동 데이터 소스 [!DNL Adobe Analytics] 로 사용하면 클라이언트가 [!DNL Analytics] 추천 활동에서 보기 기반 및/또는 구매 기반 행동 데이터 [!DNL Adobe Target] 를 사용할 수 있습니다. 이 기능은 특히 설정이 새로운 [!DNL Target Recommendations] 경우이고 활용할 수 있는 많은 내역 데이터가 [!DNL Analytics] 있는 경우에 유용합니다.

행동 데이터 소스 [!DNL Analytics] 로 사용하면 사용자 동작에 대한 풍부한 정보의 소스로 사용할 수 있습니다. 여기에는 타사 소스 또는 피드와 공유된 데이터가 포함될 수 [!DNL Analytics]있습니다.

Recommendations [에서 기준을](/help/c-recommendations/c-algorithms/create-new-algorithm.md) 만드는 동안 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 단추가 있습니다. [!UICONTROL mbox] 또는 [!UICONTROL Analytics].

![행동 데이터 소스 버튼](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 개의 단추가 계정에 표시되지 않으면 [고객 지원 센터에 문의하십시오](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## 사용 사례

권장 사항에 대한 행동 데이터 소스 [!DNL Analytics] 로 사용하면 모든 개체 매개 변수를 사용하여 개체 페이지에 태그를 지정할 필요 없이 특정 사용 사례를 배포할 수 [!DNL Target] 있습니다. 특정 전제 조건을 충족해야 하지만 &quot;제품 변수&quot;의 사용 가능 여부는 해당 기능이 완벽하게 작동되려면 가장 중요합니다. 일반 eVar 및 Prop로는 이 핸드셰이크가 [!DNL Analytics] 및 사이 [!DNL Target]에 자동으로 발생하기에 충분하지 않습니다.

행동 데이터 소스 [!DNL Analytics] 로 사용하여 다음을 수행할 수 있습니다.

* Analytics 데이터를 사용하여 지난 달 같은 카테고리에서 다른 사용자가 구매한 항목을 기준으로 소매 사이트의 사용자를 PDP 페이지 사용자에게 추천합니다.
* 미디어 사이트의 홈 화면에 현재 트렌드를 나타내는 특정 카테고리의 가장 인기 있는 컨텐츠에 대한 컨텐츠를 [!DNL Analytics] 데이터에 따라 표시합니다.

## Analytics의 구현

다음 섹션에서는 이 기능을 [!DNL Analytics] 측면에서 구현하는 데 도움이 됩니다.

### 전제 조건:Analytics의 제품 변수

제품 변수 [!DNL Analytics] 를 필요한 속성과 함께 구현해야 합니다 [!DNL Target Recommendations].

샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 안내서로 작동합니다. [!DNL Target Recommendations] 이후 해당 값은 각 엔티티 값에 대해 [!DNL Target] UI 내에 &quot;매핑&quot;되어야 [!DNL Target] 합니다.

>[!NOTE]
>
>컨텐트 사이트일 경우 해당 컨텐트에 대한 관련 속성 및 &quot;제품&quot;으로 취급되어야 합니다(예:작성자 이름, 게시 날짜, 컨텐츠 제목, 릴리스 월 등) 는 특성으로 전달되어야 합니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항에 따라 비즈니스에 의해 결정됩니다.

제품 변수 설정 방법에 대한 자세한 내용은 [Analytics 구현 안내서에서](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) 제품 *을 참조하십시오*. 해당 설명서의 일부 메모는 배포하려는 팀의 재량이 필요합니다(예:카테고리). 이 활동을 하기 전에 항상 Adobe과 상의하는 것이 좋습니다.

### 고려 사항

[!DNL Analytics] 데이터는 일별 피드를 통해 전송됩니다. 사이트의 추천 결과에 반영되는 데 최대 24시간이 소요됩니다. 모든 [!DNL Recommendations] 기준 설정과 마찬가지로 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

어떤 데이터 소스를 사용할지 빠르게 결정하려면, 사용자가 매일 생성하는 많은 유기적 데이터가 있고 내역 데이터에 그다지 의존할 필요가 없는 경우, 행동 데이터 소스로 [!DNL Target] mbox를 사용하는 것이 적절할 수 있습니다. 최근 생성된 유기적 데이터의 가용성이 부족한 경우, [!DNL Analytics] 데이터를 기반으로 처리하려는 경우, 행동 데이터 소스 [!DNL Analytics] 로 사용하는 것이 적절합니다.

### 고객 지원 센터에 연락하여 데이터 피드 만들기

모든 사전 이수 조건이 적절하다고 가정할 경우 [고객](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 지원 센터에 연락하여 데이터 피드를 생성하도록 하십시오.

## Target에서 구현

1. Target에서 **[!UICONTROL Recommendations]**&#x200B;를 클릭한 다음 피드 **[!UICONTROL 탭을]** 클릭합니다.

   ![피드](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. 피드 **[!UICONTROL 만들기를 클릭합니다]**.

1. Analytics **[!UICONTROL 분류를]**&#x200B;선택한 다음 보고서 세트를 지정합니다.

   ![분석 분류 옵션](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. 매핑 **[!UICONTROL 을]**&#x200B;클릭한 다음 필드 열 헤더를 적절한 [!UICONTROL Recommendations] 필드 이름에 매핑합니다.

   ![매핑 섹션](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## FAQ

다음과 같은 FAQ를 사용하는 [!DNL Analytics] 것이 좋습니다. [!DNL Target]

### mbox 호출 내에서 `entity.id` 및 `entity.categoryId` 값을 전달해야 [!DNL Target] 합니까?

예. 이러한 두 값은 여전히 필요합니다. 이 문서에서 설명한 대로 나머지 속성은 [!DNL Analytics] 피드를 통해 전달할 수 있습니다.

### 개체 매개 변수가 피드 접근 방법을 사용하여 프로필 속성과 일치하는 동적 포함 규칙을 사용할 수 [!DNL Analytics] 있습니까?

네, 가능합니다. 이 방법은 독립 실행형 사용 시 [!DNL Target] 비슷합니다. 그러나 이 경우 타이밍 인자에 대해 주의를 기울여야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 페이지에서 훨씬 나중에 나타날 수 있는 데이터 레이어에 따라 달라집니다.

