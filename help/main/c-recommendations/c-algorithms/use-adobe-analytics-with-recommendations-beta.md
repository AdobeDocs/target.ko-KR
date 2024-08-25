---
keywords: 동작 데이터 소스;분석;권장 사항;기준;제품 변수
description: ' [!DNL Target Recommendations]에서 동작 데이터 소스로  [!DNL Adobe Analytics] 을(를) 사용하는 방법을 알아보세요.'
title: ' [!DNL Adobe Analytics] with [!DNL Target Recommendations]을(를) 사용하려면 어떻게 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 818c5dc6-c9b1-4596-8608-1842c9620dc2
source-git-commit: 22b0ba18efb736b291f9b7951acd9f706beedbe1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# [!DNL Recommendations]과(와) 함께 [!DNL Adobe Analytics] 사용

[!DNL Adobe Analytics]을(를) 동작 데이터 소스로 사용하면 클라이언트가 [!DNL Adobe Target Recommendations] 활동에서 [!DNL Analytics]의 보기 기반 및 구매 기반 동작 데이터를 사용할 수 있습니다. 이 기능은 [!DNL Target Recommendations] 설정이 처음이고 [!DNL Analytics]에 사용할 내역 데이터가 많은 경우 특히 유용합니다.

[!DNL Analytics]을(를) 동작 데이터 원본으로 사용하면 사용자 동작에 대한 풍부한 정보 원본으로 사용할 수 있습니다. 이 정보에는 [!DNL Analytics]과(와) 공유된 서드파티 원본 또는 피드의 데이터가 포함될 수 있습니다.

[!DNL Recommendations]에서 [기준을 만드는 중](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)에 사용할 데이터 원본을 선택할 수 있는 라디오 단추가 두 개 있습니다. [!UICONTROL mboxes] 또는 [!UICONTROL Analytics]. 기준을 만들려면 [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria]을(를) 클릭합니다. 자세한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오.

>[!NOTE]
>
>이 두 단추가 계정에 표시되지 않으면 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하세요.

## [!DNL Target]의 [!DNL Analytics] 데이터에 대한 사용 사례

[!DNL Analytics]을(를) 권장 사항에 대한 동작 데이터 소스로 사용하면 모든 [!DNL Target] 엔티티 매개 변수와 함께 엔티티 페이지에 태그를 지정할 필요 없이 특정 사용 사례를 배포할 수도 있습니다. 이를 위해서는 특정 사전 요구 사항이 적용되어야 하지만 해당 기능이 원활하게 작동하려면 &quot;제품 변수&quot;의 가용성이 가장 중요합니다. 일반 eVar 및 Prop으로는 이 핸드셰이크가 [!DNL Analytics]에서 [!DNL Target] 사이에 자동으로 발생하지 않습니다.

동작 데이터 소스로 [!DNL Analytics]을(를) 사용하여 다음을 수행할 수 있습니다.

* [!DNL Analytics] 데이터를 사용하여 지난 달의 동일한 범주에서 다른 사용자가 구매한 내용에 따라 제품 세부 사항 페이지의 사용자에게 소매 사이트의 권장 사항을 표시합니다.
* [!DNL Analytics] 데이터를 기반으로 현재 트렌드가 있는 특정 범주의 인기 있는 콘텐츠에 대한 미디어 사이트의 홈 화면에 콘텐츠를 표시합니다.

## [!DNL Analytics]의 구현

다음 섹션은 [!DNL Analytics]측에서 이 기능을 구현하는 데 도움이 됩니다.

### 필수 구성 요소: [!DNL Analytics]에서 제품 변수를 설정합니다.

[!DNL Target Recommendations]에 필요한 필수 특성을 사용하여 [!DNL Analytics]에서 제품 변수를 구현합니다.

[!DNL Target Recommendations] 샘플 피드 형식은 제품 변수에서 모든 특성을 정의해야 하는 가이드 역할을 합니다. 나중에 해당 값은 각 [!DNL Target] 엔터티 값에 대해 [!DNL Target] UI 내에서 &quot;매핑&quot;되어야 합니다.

>[!NOTE]
>
>콘텐츠 사이트인 경우 해당 콘텐츠 조각을 &quot;제품&quot;으로 취급하고 해당 콘텐츠에 대한 관련 속성을 속성으로 전달해야 합니다. 이러한 속성에는 작성자 이름, 게시 날짜, 콘텐츠 제목, 릴리스 월 등이 포함될 수 있습니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항에 따라 비즈니스에서 결정해야 합니다.

제품 변수를 설정하는 방법에 대한 자세한 내용은 *Adobe Analytics 구현* 안내서에서 [제품](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html)을 참조하십시오. 해당 설명서의 일부 참고에는 이 설명서를 배포하는 팀의 재량이 필요합니다(예: 범주). 이 활동을 수행하기 전에 항상 [!DNL Adobe]과(와) 상담하는 것이 좋습니다.

### 고려 사항

[!DNL Analytics] 데이터가 매일 피드를 통해 전송됩니다. 행동 결과는 사이트의 권장 사항 결과 내에 반영되기까지 최대 24시간이 걸릴 수 있습니다. 모든 [!DNL Recommendations] 기준 설정과 마찬가지로 이 데이터 원본을 테스트할 수 있으며 테스트해야 합니다.

사용할 데이터 소스에 대한 신속한 의사 결정을 위해, 사용자가 매일 생성하는 유기 데이터가 많고 내역 데이터에 필요한 종속성이 많지 않은 경우 [!DNL Target] mbox를 동작 데이터 소스로 사용하는 것이 좋습니다. 최근에 생성된 유기 데이터의 가용성이 낮은 경우 [!DNL Analytics] 데이터를 기준으로 뱅킹하려면 [!DNL Analytics]을(를) 동작 데이터 소스로 사용하는 것이 좋습니다.

이제 동작 데이터의 지속적인 공급을 위해 이러한 변수를 [!DNL Target]측에 매핑할 차례입니다.

## [!DNL Target]에서 구현

1. [!DNL Target]에서 **[!UICONTROL Recommendations]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Feeds]** 탭을 클릭합니다.

1. **[!UICONTROL Create Feed]** 아이콘을 클릭합니다.

1. **[!UICONTROL Analytics Classifications]**&#x200B;을(를) 선택한 다음 보고서 세트를 지정합니다.

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 **[!UICONTROL Schedule]** 설정으로 이동한 다음 피드의 빈도 기간을 선택하십시오.

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   피드가 처리할 시간을 선택할 수도 있습니다.

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 **[!UICONTROL Mapping]** 설정으로 이동한 다음 필드 열 헤더를 적절한 [!UICONTROL Recommendations] 필드 이름에 매핑합니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 자주 묻는 질문

[!DNL Target]에서 [!DNL Analytics]을(를) 사용할 때 다음 FAQ를 고려하십시오.

### [!DNL Target] mbox 호출 내에 `entity.id` 및 `entity.categoryId` 값을 전달해야 합니까?

예, 이 두 값은 여전히 필수입니다. 나머지 속성은 이 문서에서 설명한 대로 [!DNL Analytics] 피드를 통해 전달할 수 있습니다.

### [!DNL Analytics] 피드 접근 방식을 사용하여 프로필 속성과 일치하는 엔티티 매개 변수와 같은 동적 포함 규칙을 사용할 수 있습니까?

네, 가능합니다. 메서드는 [!DNL Target] 독립 실행형을 사용할 때와 비슷합니다. 그러나 이 경우 타이밍 요인에 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 훨씬 나중에 페이지에 표시될 수 있는 데이터 레이어에 따라 다릅니다.
