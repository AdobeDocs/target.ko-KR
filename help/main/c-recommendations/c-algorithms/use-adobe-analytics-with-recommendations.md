---
keywords: 동작 데이터 소스;분석;권장 사항;기준;제품 변수
description: '사용 방법 알아보기 [!DNL Adobe Analytics] 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 행동 데이터 소스로 [!DNL Analytics] 위치: [!DNL Target Recommendations].'
title: 사용 방법 [!DNL Adobe Analytics] 포함 [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 2%

---

# 사용 [!DNL Adobe Analytics] 포함 [!DNL Recommendations]

사용 [!DNL Adobe Analytics] as the behavioral data source를 사용하면 클라이언트는에서 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 수 있습니다. [!DNL Analytics] 위치: [!DNL Adobe Target] [!DNL Recommendations] 활동. 이 기능은 특히 [!DNL Target Recommendations] 설정이 새롭고, [!DNL Analytics] 에는 사용할 수 있는 많은 내역 데이터가 있습니다.

사용 [!DNL Analytics] 행동 데이터 소스는 사용자 행동에 대한 정보의 풍부한 소스로 작용할 수 있습니다. 이 정보에는 서드파티 소스 또는 피드에서 공유된 데이터만 포함될 수 있습니다. [!DNL Analytics].

While [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) 위치: [!DNL Recommendations]에는 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 버튼이 있습니다. [!UICONTROL mbox] 또는 [!UICONTROL 분석]. 기준을 만들려면 다음을 클릭하십시오. [!UICONTROL Recommendations] > [!UICONTROL 기준] > [!UICONTROL 기준 만들기] > [!UICONTROL 기준 만들기]. 자세한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

![동작 데이터 소스 단추](assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 단추가 계정에 표시되지 않으면 다음 위치로 이동하십시오. [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Target의 Analytics 데이터에 대한 사용 사례

사용 [!DNL Analytics] recommendations에 대한 동작 데이터 소스로 을 사용하면 모든 와 함께 엔티티 페이지에 태그를 지정할 필요 없이 특정 사용 사례를 배포할 수 있습니다. [!DNL Target] 엔티티 매개 변수. 이를 위해서는 특정 사전 요구 사항이 적용되어야 하지만 해당 기능이 원활하게 작동하려면 &quot;제품 변수&quot;의 가용성이 가장 중요합니다. 일반 eVar 및 Prop만으로는 이 핸드셰이크가 다음 사이에 자동으로 발생하지는 않습니다. [!DNL Analytics] 및 [!DNL Target].

다음을 사용할 수 있습니다. [!DNL Analytics] 동작 데이터 소스로 사용:

* 을 사용하여 지난 달에 같은 범주에서 다른 사용자가 구매한 내용에 따라 제품 세부 사항 페이지의 사용자에게 소매 사이트의 권장 사항을 표시합니다. [!DNL Analytics] 데이터.
* 를 기반으로 현재 트렌드가 있는 특정 카테고리에서 가장 인기 있는 콘텐츠의 미디어 사이트 홈 화면에 콘텐츠를 표시합니다. [!DNL Analytics] 데이터.

## 에서 구현 [!DNL Analytics]

다음 섹션에서 이 기능을 구현하는 데 도움이 됩니다. [!DNL Analytics] 옆이요.

### 사전 요구 사항:에서 제품 변수 설정 [!DNL Analytics]

에서 제품 변수 구현 [!DNL Analytics] 에 필요한 필수 속성을 사용하여 [!DNL Target Recommendations].

A [!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 가이드 역할을 합니다. 나중에 이러한 값은 내에서 &quot;매핑&quot;되어야 합니다. [!DNL Target] 해당 UI [!DNL Target] 엔티티 값.

>[!NOTE]
>
>콘텐츠 사이트인 경우 해당 콘텐츠 조각을 &quot;제품&quot;으로 취급하고 해당 콘텐츠에 대한 관련 속성을 속성으로 전달해야 합니다. 이러한 속성에는 작성자 이름, 게시 날짜, 콘텐츠 제목, 릴리스 월 등이 포함될 수 있습니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항에 따라 비즈니스에서 결정해야 합니다.

제품 변수를 설정하는 방법에 대한 자세한 내용은 [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) 다음에서 *Adobe Analytics 구현* 가이드. 해당 설명서의 일부 참고에는 이 설명서를 배포하는 팀의 재량이 필요합니다(예: 범주). 항상 상의하는 것이 좋다 [!DNL Adobe] 이 활동을 수행하기 전에

### 고려 사항

[!DNL Analytics] 데이터는 일일 피드를 통해 전송됩니다. 행동 결과는 사이트의 권장 사항 결과 내에 반영되기까지 최대 24시간이 걸릴 수 있습니다. 모두와 마찬가지로 [!DNL Recommendations] 기준 설정. 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

사용할 데이터 소스에 대한 신속한 의사 결정을 위해, 사용자가 매일 생성하는 유기 데이터가 많고 내역 데이터에 많은 종속성이 필요하지 않은 경우 [!DNL Target] 동작 데이터 소스로서의 mbox가 적합할 수 있습니다. 최근에 생성된 유기 데이터의 가용성이 낮은 경우 다음을 확인하고자 하는 경우 [!DNL Analytics] 데이터, 사용 [!DNL Analytics] 는 동작 데이터 소스가 적합하므로 다음과 같습니다.

이제 이 변수를에 매핑할 차례입니다. [!DNL Target] 동작 데이터의 지속적인 공급을 위한 side입니다.

## 에서 구현 [!DNL Target]

1. 위치 [!DNL Target], 클릭 **[!UICONTROL Recommendations]**&#x200B;을(를) 클릭하고 **[!UICONTROL 피드]** 탭.

   ![피드](/help/main/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. 클릭 **[!UICONTROL 피드 만들기]**.

1. 선택 **[!UICONTROL Analytics 분류]**&#x200B;그런 다음 보고서 세트를 지정합니다.

   ![Analytics 분류 옵션](/help/main/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. 클릭 **[!UICONTROL 다음]** 로 이동 **[!UICONTROL 예약]** 설정, 피드에 대한 빈도 기간 선택:

   * [!UICONTROL 일별]
   * [!UICONTROL 주별]
   * [!UICONTROL 2주마다]
   * [!UICONTROL 절대 안 함]

   피드가 처리할 시간을 선택할 수도 있습니다.

1. 클릭 **[!UICONTROL 다음]** 로 이동  **[!UICONTROL 매핑]** 설정을 지정한 다음 필드 열 헤더를 해당 필드에 매핑합니다 [!UICONTROL Recommendations] 필드 이름.

   ![매핑 섹션](/help/main/c-recommendations/c-algorithms/assets/mapping.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 자주 묻는 질문

사용할 때 다음 FAQ를 고려하십시오 [!DNL Analytics] 포함 [!DNL Target]:

### 다음 `entity.id` 및 `entity.categoryId` 내에 전달해야 하는 값 [!DNL Target] mbox 호출?

예, 이 두 값은 여전히 필수입니다. 나머지 속성은 다음을 통해 전달할 수 있습니다. [!DNL Analytics] 이 문서에 설명된 대로 피드 를 참조하십시오.

### 다음을 사용하여 프로필 속성과 일치하는 엔티티 매개 변수와 같은 동적 포함 규칙을 사용할 수 있습니까? [!DNL Analytics] 피드 접근 방식?

네, 가능합니다. 메서드는 을 사용할 때와 유사합니다 [!DNL Target] 독립 실행형. 그러나 이 경우 타이밍 요인에 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 훨씬 나중에 페이지에 표시될 수 있는 데이터 레이어에 따라 다릅니다.
