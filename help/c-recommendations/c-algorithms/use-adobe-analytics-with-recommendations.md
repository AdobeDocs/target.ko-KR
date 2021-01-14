---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: 행동 데이터 소스로 Adobe Analytics을 사용하면 클라이언트는 Adobe Recommendations의 Analytics에서 제공하는 보기 기반 및/또는 구매 기반 행동 데이터를 사용할 수 있습니다.
title: Target Recommendations과 함께 Adobe Analytics 사용
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 3%

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

### 배포 단계

모든 사전 이수 과정을 적절히 활용한다고 가정할 때 [!DNL Adobe Target Recommendations] 팀에서 다음 작업을 수행해야 합니다.

>[!IMPORTANT]
>
>아래 단계는 실례만을 위한 것입니다. [!DNL Recommendations] 팀의 구성원은 현재 다음 단계를 수행해야 합니다. [자세한 내용은 고객 지원 센터에 문의하십시오.](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

1. [!DNL Target]에서 **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭하여 [!DNL Target] 클라이언트 코드를 가져옵니다.

   ![클라이언트 코드](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. [!DNL Analytics] 보고서 세트를 가져옵니다.

   [!DNL Analytics] 프로덕션 사이트 보고서 세트를 사용합니다. 이 보고서 세트는 [!DNL Recommendations]이(가) 배포된 사이트를 추적하는 보고서 세트입니다.

1. [!DNL Analytics]에서 **[!UICONTROL 관리]** > **[!UICONTROL 데이터 피드]**&#x200B;를 클릭합니다.

   ![설정 > 데이터 피드](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. **[!UICONTROL 추가]**&#x200B;를 클릭하여 새 피드를 만듭니다.

   ![피드 추가](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. 피드 정보 채우기:

   * **이름**:제품 피드 다시 작성
   * **보고서 세트**:미리 결정된 보고서 세트
   * **이메일**:관리자 사용자의 적절한 주소 지정
   * **피드 간격**:원하는 간격 선택
   * **처리 지연**:지연이 없습니다.
   * **시작 및 종료 날짜**:연속 피드

   ![피드 정보 섹션](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. **[!UICONTROL 대상]** 섹션의 세부 사항을 입력합니다.

   >[!NOTE]
   > 
   >이 단계를 수행하려면 먼저 [!DNL Adobe Analytics] 팀과 상의하십시오.

   * **유형**:FTP
   * **호스트**: `xxx.yyy.com`
   * **경로**:클라이언트  [!DNL Target] 코드
   * **사용자 이름**:사용자 이름 지정
   * **암호**:암호 지정

   스크린샷은 참조용으로만 사용됩니다. 배포에는 다른 자격 증명이 있습니다. 이 단계를 수행하는 동안 [!DNL Adobe Analytics] 팀 또는 고객 지원 센터에 문의하십시오.

   ![대상 섹션](/help/c-recommendations/c-algorithms/assets/destination.png)

1. **[!UICONTROL 데이터 열]** 정의를 채웁니다.

   * **압축 형식**:Gzip
   * **패키징 유형**:단일 파일
   * **매니페스트:** 완료 파일

      ![압축 형식, 패키징 유형 및 매니페스트 설정](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **포함된 열**:

      >[!IMPORTANT]
      >
      >여기에 설명된 것과 동일한 순서로 열을 추가해야 합니다. 다음 순서로 열을 선택하고 각 열에 대해 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![데이터 열 정의 섹션](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

이 경우 [!DNL Analytics]쪽에 설정된 설정이 완료됩니다. 이제 행동 데이터의 지속적인 공급을 위해 이러한 변수를 [!DNL Target] 측에 매핑할 때입니다.

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

### [!DNL Analytics] 피드 접근 방식을 사용하여 개체 매개 변수가 프로필 속성과 일치하는 동적 포함 규칙을 사용할 수 있습니까?

네, 가능합니다. 이 메서드는 [!DNL Target] 독립 실행형 사용 시 유사합니다. 그러나 이 경우 시간 요소에 대해 유의해야 합니다. 프로필 변수와 일치해야 하는 엔티티 변수는 페이지에서 훨씬 나중에 나타날 수 있는 데이터 레이어에 따라 달라집니다.

