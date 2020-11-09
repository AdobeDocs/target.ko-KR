---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: 행동 데이터 소스로 Adobe Analytics을 사용하면 클라이언트가 Adobe Recommendations의 Analytics에서 제공하는 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 수 있습니다.
title: Adobe Analytics과 Target Recommendations 사용
feature: criteria
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 3%

---


# Recommendations과 Adobe Analytics 사용

행동 데이터 소스 [!DNL Adobe Analytics] 로 사용하면 클라이언트가 [!DNL Analytics] 추천 활동에서 보기 기반 및/또는 구매 기반 행동 데이터 [!DNL Adobe Target] 를 사용할 수 있습니다. 이 기능은 특히 설정이 새로운 [!DNL Target Recommendations] 경우이고 활용할 수 있는 많은 내역 데이터가 [!DNL Analytics] 있는 경우에 유용합니다.

행동 데이터 소스 [!DNL Analytics] 로 사용하면 사용자 동작에 대한 풍부한 정보의 소스로 사용할 수 있습니다. 여기에는 타사 소스 또는 피드와 공유된 데이터가 포함될 수 [!DNL Analytics]있습니다.

Recommendations [에서 기준을](/help/c-recommendations/c-algorithms/create-new-algorithm.md) 만드는 동안 사용할 데이터 소스를 선택할 수 있는 두 개의 라디오 단추가 있습니다. [!UICONTROL mbox] 또는 [!UICONTROL Analytics].

![행동 데이터 소스 버튼](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>이 두 개의 단추가 계정에 표시되지 않으면 [고객 지원 센터에 문의하십시오](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Target의 Analytics 데이터에 대한 사용 사례

권장 사항에 대한 행동 데이터 소스 [!DNL Analytics] 로 사용하면 모든 개체 매개 변수를 사용하여 개체 페이지에 태그를 지정할 필요 없이 특정 사용 사례를 배포할 수 [!DNL Target] 있습니다. 특정 전제 조건을 충족해야 하지만 &quot;제품 변수&quot;의 사용 가능 여부는 해당 기능이 완벽하게 작동되려면 가장 중요합니다. 일반 eVar 및 Prop로는 이 핸드셰이크가 [!DNL Analytics] 및 사이 [!DNL Target]에 자동으로 발생하기에 충분하지 않습니다.

행동 데이터 소스 [!DNL Analytics] 로 사용하여 다음을 수행할 수 있습니다.

* Analytics 데이터를 사용하여 지난 달 같은 카테고리에서 다른 사용자가 구매한 항목을 기준으로 소매 사이트의 사용자를 PDP 페이지 사용자에게 추천합니다.
* 미디어 사이트의 홈 화면에 현재 트렌드를 나타내는 특정 카테고리의 가장 인기 있는 컨텐츠에 대한 컨텐츠를 [!DNL Analytics] 데이터에 따라 표시합니다.

## Analytics의 구현

다음 섹션에서는 이 기능을 [!DNL Analytics] 측면에서 구현하는 데 도움이 됩니다.

### 전제 조건:Analytics에서 제품 변수 설정

제품 변수 [!DNL Analytics] 를 필요한 속성과 함께 구현해야 합니다 [!DNL Target Recommendations].

샘플 피드 형식은 제품 변수에서 모든 속성을 정의해야 하는 안내서로 작동합니다. [!DNL Target Recommendations] 이후 해당 값은 각 엔티티 값에 대해 [!DNL Target] UI 내에 &quot;매핑&quot;되어야 [!DNL Target] 합니다.

>[!NOTE]
>
>컨텐트 사이트일 경우 해당 컨텐트에 대한 관련 속성 및 &quot;제품&quot;으로 취급되어야 합니다(예:작성자 이름, 게시 날짜, 컨텐츠 제목, 릴리스 월 등) 는 특성으로 전달되어야 합니다. 카테고리 수준 또는 카테고리 유형의 세부기간은 사용 사례 요구 사항에 따라 비즈니스에 의해 결정됩니다.

제품 변수 설정 방법에 대한 자세한 내용은 [Analytics 구현 안내서에서](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) 제품 *을 참조하십시오*. 해당 설명서의 일부 메모는 배포하려는 팀의 재량이 필요합니다(예:카테고리). 이 활동을 하기 전에 항상 Adobe과 상의하는 것이 좋습니다.

### 고려 사항

[!DNL Analytics] 데이터는 일별 피드를 통해 전송됩니다. 사이트의 추천 결과에 반영되는 데 최대 24시간이 소요됩니다. 모든 [!DNL Recommendations] 기준 설정과 마찬가지로 이 데이터 소스는 테스트할 수 있으며 테스트해야 합니다.

어떤 데이터 소스를 사용할지 빠르게 결정하려면, 사용자가 매일 생성하는 많은 유기적 데이터가 있고 내역 데이터에 그다지 의존할 필요가 없는 경우, 행동 데이터 소스로 [!DNL Target] mbox를 사용하는 것이 적절할 수 있습니다. 최근 생성된 유기적 데이터의 가용성이 부족한 경우, [!DNL Analytics] 데이터를 기반으로 처리하려는 경우, 행동 데이터 소스 [!DNL Analytics] 로 사용하는 것이 적절합니다.

### 배포 단계

모든 전제 조건이 충족되었다고 가정할 경우, 다음 작업은 [!DNL Adobe Target Recommendations] 팀에서 수행해야 합니다.

>[!IMPORTANT]
>
>아래 단계는 실례만을 위한 것입니다. 팀원은 [!DNL Recommendations] 현재 이러한 단계를 수행해야 합니다. [자세한 내용은 고객 지원 센터에 문의하십시오.](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

1. 에서 [!DNL Target]관리 **** > **[!UICONTROL 구현을]** 클릭하여 클라이언트 코드를 [!DNL Target] 획득합니다.

   ![클라이언트 코드](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. 보고서 세트를 [!DNL Analytics] 획득합니다.

   프로덕션 [!DNL Analytics] 사이트 보고서 세트를 사용합니다. 배포된 사이트를 추적하는 보고서 [!DNL Recommendations] 세트입니다.

1. 에서 관리 [!DNL Analytics]> 데이터 피드 **[!UICONTROL 를]** 클릭합니다 ****.

   ![설정 > 데이터 피드](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Click **[!UICONTROL Add]** to create a new feed.

   ![피드 추가](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. 피드 정보 입력:

   * **이름**:제품 피드 다시 작성
   * **보고서 세트**:사전 결정된 보고서 세트
   * **이메일**:관리자 사용자의 적절한 주소 지정
   * **피드 간격**:원하는 간격 선택
   * **처리 지연**:지연이 없습니다.
   * **시작 및 종료 날짜**:연속 피드

   ![피드 정보 섹션](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Fill in the details in the **[!UICONTROL Destination]** section:

   >[!NOTE]
   > 
   >이 단계를 수행하기 전에 [!DNL Adobe Analytics] 팀과 상의하십시오.

   * **유형**:FTP
   * **호스트**: `xxx.yyy.com`
   * **경로**:클라이언트 [!DNL Target] 코드
   * **사용자 이름**:사용자 이름 지정
   * **암호**:암호 지정

   스크린샷은 참조용으로만 사용됩니다. 배포의 자격 증명이 다릅니다. 이 단계를 수행하는 동안 [!DNL Adobe Analytics] 팀 또는 고객 지원 센터에 문의하십시오.

   ![대상 섹션](/help/c-recommendations/c-algorithms/assets/destination.png)

1. 데이터 열 **[!UICONTROL 정의를]** 입력합니다.

   * **압축 형식**:Gzip
   * **패키징 유형**: 단일 파일
   * **매니페스트:** 파일 마침

      ![압축 형식, 패키징 유형 및 매니페스트 설정](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **포함된 열**:

      >[!IMPORTANT]
      >
      >열은 여기에 설명된 것과 동일한 순서로 추가해야 합니다. 다음 순서로 열을 선택하고 각 열에 대해 **[!UICONTROL 추가를]** 클릭합니다.

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![데이터 열 정의 섹션](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

이렇게 하면 [!DNL Analytics] 측면의 설정이 완료됩니다. 이제 행동 데이터의 지속적인 공급을 위해 이러한 변수를 [!DNL Target] 나란히 매핑할 때입니다.

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

