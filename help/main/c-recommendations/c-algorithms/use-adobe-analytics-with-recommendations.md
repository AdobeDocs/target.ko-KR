---
keywords: 동작 데이터 소스;분석;권장 사항;기준;제품 변수
description: '[!DNL Target Recommendations]에서 동작 데이터 원본으로 [!DNL Adobe Analytics]을(를) 사용하는 방법을 알아봅니다.'
title: 추천와 함께 Adobe Analytics 사용
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
TQID: 'https://experienceleague.adobe.com/2ryixOT-YoKjDlMbqs8g2DJElNVmlCUFhbdZzpfSnNs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 374d176c5c40826d958a8b87d220422466433690
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 1%
---
# [!DNL Recommendations]과(와) 함께 [!DNL Adobe Analytics] 사용 {#use-analytics-with-recommendations}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Target Recommendations] 활동에서 동작 데이터 원본으로 [!DNL Adobe Analytics]을(를) 사용하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Analytics]을(를) 동작 데이터 소스로 사용하면 [!DNL Adobe Target Recommendations] 활동에서 [!DNL Analytics]의 보기 기반 및 구매 기반 동작 데이터를 사용할 수 있습니다. 이 기능은 [!DNL Target Recommendations] 설정이 새롭고 [!DNL Analytics]에 사용할 내역 데이터가 많은 경우 유용합니다. 데이터에는 [!DNL Analytics]과만 공유되는 서드파티 소스 또는 피드의 정보도 포함될 수 있습니다.

[!DNL Recommendations]에서 [기준을 만드는 중](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source)(**[!UICONTROL Adobe Target]** 또는 **[!UICONTROL Analytics]**) 동안 **[!UICONTROL 동작 데이터 Source]** 옵션을 사용하여 데이터 원본을 선택했습니다.

>[!NOTE]
>
>이 두 옵션이 계정에 표시되지 않으면 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

## [!DNL Target]의 [!DNL Analytics] 데이터에 대한 사용 사례 {#use-cases}

[!DNL Analytics]을(를) 동작 데이터 소스로 사용하면 모든 [!DNL Target] 엔티티 매개 변수로 엔티티 페이지에 태그를 지정하지 않고 특정 사용 사례를 배포할 수도 있습니다. 이를 위해서는 특정 전제 조건이 필요하며, &quot;제품 변수&quot;의 가용성이 가장 중요합니다. [!DNL Analytics]과(와) [!DNL Target]이(가) 이 데이터를 자동으로 교환하는 데 일반 eVar 및 Prop이 충분하지 않습니다.

[!DNL Analytics]을(를) 동작 데이터 원본으로 사용하여 다음을 수행할 수 있습니다.

* [!DNL Analytics] 데이터를 사용하여 지난 달의 동일한 범주에서 다른 사용자가 구매한 내용에 따라 제품 세부 사항 페이지의 사용자에게 소매 사이트의 권장 사항을 표시합니다.
* [!DNL Analytics] 데이터를 기반으로 현재 트렌드가 있는 특정 범주의 인기 있는 콘텐츠에 대한 미디어 사이트의 홈 화면에 콘텐츠를 표시합니다.

## [!DNL Analytics]의 구현

### 필수 구성 요소: [!DNL Analytics]에서 제품 변수를 설정합니다. {#prerequisites}

[!DNL Target Recommendations]에 필요한 특성을 사용하여 [!DNL Analytics]에서 제품 변수를 구현합니다. [!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에 정의해야 하는 특성을 안내합니다. 이러한 값은 나중에 [!DNL Target] UI에서 해당 [!DNL Target] 엔터티 값에 &quot;매핑&quot;되어야 합니다.

>[!NOTE]
>
>콘텐츠 사이트인 경우 해당 콘텐츠 조각을 &quot;제품&quot;으로 취급하고 해당 콘텐츠의 관련 속성을 속성으로 전달해야 합니다. 이러한 속성에는 작성자 이름, 게시 날짜, 콘텐츠 제목, 릴리스 월 등이 포함될 수 있습니다. 비즈니스 팀은 사용 사례의 요구 사항에 따라 카테고리 수준 또는 카테고리 유형의 세부기간을 결정해야 합니다.

제품 변수를 설정하는 방법에 대한 자세한 내용은 *Adobe Analytics 구현* 안내서에서 [제품](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html?lang=ko)을 참조하십시오. 해당 설명서의 일부 참고 사항(예: 카테고리에 대한)은 배포하는 팀의 판단이 필요합니다. 이 활동이 권장되기 전에 [!DNL Adobe]을(를) 컨설팅 중입니다.

### 고려 사항 {#considerations}

[!DNL Analytics] 데이터가 매일 피드를 통해 전송됩니다. 행동 결과는 사이트의 권장 사항 결과에 반영되기까지 최대 24시간이 걸릴 수 있습니다. 모든 [!DNL Recommendations] 기준 설정과 마찬가지로 이 데이터 원본을 테스트해야 합니다.

데이터 소스를 선택하려면 다음을 수행하십시오.

* [!DNL Target] mbox는 사용자가 매일 많은 유기 데이터를 생성하고 이전 데이터에 거의 의존하지 않는 경우에 적합합니다.
* [!DNL Analytics]은(는) 최근에 유기적인 데이터가 덜 생성되었으며 [!DNL Analytics] 데이터를 사용해야 하는 경우에 적합합니다.

[!DNL Target] mbox 호출에서 `entity.id` 및 `entity.categoryId` 값을 계속 전달해야 합니다. 다른 특성은 이 페이지에 설명된 대로 [!DNL Analytics] 피드를 통해 전달할 수 있습니다.

[!DNL Analytics] 피드 접근 방식에서는 엔터티 매개 변수를 프로필 속성에 일치시키는 것과 같은 동적 포함 규칙을 사용할 수 있습니다. 메서드는 [!DNL Target] 독립 실행형 사용과 비슷하지만, 시기를 고려해야 합니다. 프로필 변수와 일치해야 하는 엔터티 변수는 데이터 계층에 따라 다르며, 나중에 페이지에 표시될 수도 있습니다.

## [!DNL Target]에서 구현 {#implement-target}

제품 변수는 동작 데이터를 지속적으로 제공하기 위해 [!DNL Target]에 매핑됩니다.

1. [!DNL Target]에서 **[!UICONTROL 권장 사항]**&#x200B;을 클릭한 다음 **[!UICONTROL 피드]** 탭을 클릭합니다.

1. **[!UICONTROL 피드 만들기]**&#x200B;를 클릭합니다.

   ![피드 만들기 단추가 강조 표시된 피드 페이지](../assets/feeds_1.png)

1. **[!UICONTROL 분석 분류]**&#x200B;를 선택한 다음 보고서 세트를 지정합니다.

1. **[!UICONTROL 다음]**&#x200B;을(를) 클릭하여 **[!UICONTROL 예약]** 설정으로 이동한 다음 피드의 빈도를 선택하십시오. **[!UICONTROL 매일]**, **[!UICONTROL 주별]**, **[!UICONTROL 2주마다]** 또는 **[!UICONTROL 절대]**. 피드가 처리되는 시간을 선택할 수도 있습니다.

   ![[매일], [주별], [2주마다] 및 [사용 안 함] 옵션이 있는 [피드 만들기] 대화 상자의 예약 단계 및 [시간] 필드](../assets/feeds_3.png)

1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 **[!UICONTROL 매핑]** 설정으로 이동한 다음 필드 열 헤더를 적절한 **[!UICONTROL 권장 사항]** 필드 이름에 매핑합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

피드 만들기에 대한 자세한 내용은 [피드 만들기](/help/main/c-recommendations/c-products/feeds.md#steps)를 참조하십시오.
