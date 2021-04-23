---
keywords: 행동 데이터 소스;분석;권장 사항;기준;제품 변수
description: Adobe Analytics을 행동 데이터 소스로 사용하여 Analytics의  [!DNL Target] Recommendations에서 보기 기반 및/또는 구매 기반 행동 데이터를 사용하는 방법을 알아봅니다.
title: 'Adobe Analytics을 Recommendations과 함께 사용하려면 어떻게 해야 합니까? [!DNL Target] '
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 1%

---

# Recommendations과 함께 Adobe Analytics 사용

행동 데이터 소스로 [!DNL Adobe Analytics]을 사용하면 클라이언트가 [!DNL Adobe Target] 추천 활동의 [!DNL Analytics]에서 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 수 있습니다. 이 기능은 특히 [!DNL Target Recommendations] 설정이 새로 설치되고 [!DNL Analytics]에 활용할 내역 데이터가 많이 있는 경우에 유용합니다.

행동 데이터 소스로 [!DNL Analytics]을 사용하면 사용자 행동에 대한 풍부한 정보 소스로 사용할 수 있습니다. 여기에는 [!DNL Analytics]와만 공유되는 제3자 소스 또는 피드의 데이터가 포함될 수 있습니다.

Recommendations에서 [기준](/help/c-recommendations/c-algorithms/create-new-algorithm.md)을 만드는 동안 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 단추가 있습니다.[!UICONTROL mbox] 또는 [!UICONTROL Analytics].

![행동 데이터 소스 버튼](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 개의 단추가 계정에 표시되지 않으면 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

## Target의 Analytics 데이터에 대한 사용 사례

권장 사항에 대한 행동 데이터 소스로 [!DNL Analytics]을 사용하면 모든 [!DNL Target] 개체 매개 변수를 사용하여 개체 페이지에 태그를 지정할 필요 없이 특정 사용 사례를 배포할 수도 있습니다. 이 경우 특정 전제 조건을 충족해야 하지만 &quot;제품 변수&quot;의 사용 가능 여부는 해당 기능이 원활하게 작동하기 위해 가장 중요합니다. 일반 eVar 및 Prop로는 이 핸드셰이크가 [!DNL Analytics]과 [!DNL Target] 사이에 자동으로 발생하기에 충분하지 않습니다.

행동 데이터 소스로 [!DNL Analytics]을 사용하여 다음을 수행할 수 있습니다.

* Analytics 데이터를 사용하여 지난 달 같은 카테고리에서 다른 사용자가 구매한 항목을 기준으로 소매 사이트의 권장 사항을 PDP 페이지에 표시합니다.
* [!DNL Analytics] 데이터를 기반으로 현재 트렌드를 보이고 있는 특정 카테고리의 가장 인기 있는 컨텐츠에 대한 미디어 사이트의 홈 화면에 컨텐츠를 표시합니다.

## Analytics에서의 구현

다음 섹션에서는 [!DNL Analytics] 측에서 이 기능을 구현하는 데 도움이 됩니다.

### 사전 요구 사항:Analytics에서 제품 변수 설정

[!DNL Target Recommendations]에 필요한 특성을 사용하여 [!DNL Analytics]에 제품 변수를 구현해야 합니다.

[!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 안내서로 작동합니다. 이후 해당 값은 각 [!DNL Target] 엔티티 값에 대해 [!DNL Target] UI 내에 &quot;mapped&quot;여야 합니다.

>[!NOTE]
>
>컨텐트 사이트인 경우 해당 컨텐트에 대한 관련 속성(예:작성자 이름, 게시 날짜, 컨텐츠 제목, 릴리스 월 등) 는 특성으로 전달되어야 합니다. 사용 사례 요구 사항에 따라 카테고리 수준 또는 카테고리 유형의 세부기간을 비즈니스에 따라 결정해야 합니다.

제품 변수 설정 방법에 대한 자세한 내용은 *Analytics 구현 안내서*&#x200B;의 [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html)을 참조하십시오. 해당 문서의 일부 메모는 배포하려는 팀의 재량이 필요합니다(예:카테고리). 이 활동을 하기 전에 항상 Adobe과 상의하는 것이 좋습니다.

### 고려 사항

[!DNL Analytics] 데이터는 일별 피드를 통해 전송됩니다. 행동 결과를 사이트의 추천 결과에 반영하려면 최대 24시간이 소요됩니다. 모든 [!DNL Recommendations] 기준 설정과 마찬가지로 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

사용할 데이터 소스를 신속하게 결정하려면 사용자가 매일 생성하는 유기적 데이터가 많고 내역 데이터에 많은 종속성이 필요하지 않은 경우 행동 데이터 소스로 [!DNL Target] mbox를 사용하는 것이 좋습니다. 최근 생성된 유기적 데이터의 사용 가능성이 적은 경우, [!DNL Analytics] 데이터를 고려하려는 경우 행동 데이터 소스로 [!DNL Analytics]을(를) 사용하는 것이 좋습니다.

이제 행동 데이터의 지속적인 공급을 위해 이러한 변수를 [!DNL Target] 측에 매핑할 때입니다.

## Target에서 구현

1. Target에서 **[!UICONTROL Recommendations]**&#x200B;을 클릭한 다음 **[!UICONTROL 피드]** 탭을 클릭합니다.

   ![피드](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. **[!UICONTROL 피드 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 분석 분류]**&#x200B;를 선택한 다음 보고서 세트를 지정합니다.

   ![분석 분류 옵션](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. **[!UICONTROL 매핑]**&#x200B;을 클릭한 다음 필드 열 헤더를 적절한 [!UICONTROL Recommendations] 필드 이름에 매핑합니다.

   ![매핑 섹션](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## FAQ

[!DNL Target]에서 [!DNL Analytics]을(를) 사용할 때 다음 FAQ를 고려하십시오.

### `entity.id` 및 `entity.categoryId` 값이 [!DNL Target] mbox 호출 내에 전달되어야 합니까?

예. 이 두 값은 여전히 필요합니다. 이 문서에서 설명한 대로 나머지 속성은 [!DNL Analytics] 피드를 통해 전달할 수 있습니다.

### [!DNL Analytics] 피드 접근 방법을 사용하여 개체 매개 변수가 프로필 속성과 일치하는 동적 포함 규칙을 사용할 수 있습니까?

네, 가능합니다. 이 메서드는 [!DNL Target] 독립 실행형 사용 시 유사합니다. 그러나 이 경우 시간 요소에 대해 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 페이지에서 훨씬 나중에 나타날 수 있는 데이터 레이어에 따라 달라집니다.
