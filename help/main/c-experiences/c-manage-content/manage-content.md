---
keywords: 컨텐츠;자산;컨텐츠 관리;오퍼;자산 관리;선택 모드 들어가기;선택 모드
description: Adobe Target의 오퍼 라이브러리를 사용하여 코드 및 이미지 오퍼를 관리하는 방법을 알아봅니다.
title: 코드 및 이미지 오퍼를 관리하는 방법
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: f93e33e91fb7be9c0d1772a2014864b46c1dfe47
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 16%

---

# 오퍼

사용 [!UICONTROL Offers] 라이브러리 [!DNL Adobe Target] 코드 오퍼 및 이미지 오퍼 컨텐츠를 관리합니다.

1. 클릭 **[!UICONTROL Offers]** 라이브러리를 엽니다.

   이 라이브러리에는 [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) 및 API를 통해 설정한 오퍼가 있습니다. [!DNL Target Classic] 또는 기타 솔루션에서 만든 오퍼는 [!DNL Target Standard/Premium]에서 편집할 수 있습니다.

   다음 [!UICONTROL Offers] 페이지에는 오른쪽에 두 개의 탭이 있습니다. [!UICONTROL Code Offers] 및 [!UICONTROL Image Offers] 을 사용하면 유형별로 오퍼를 볼 수 있습니다.

   ![코드 오퍼 및 이미지 오퍼 탭을 표시하는 오퍼 페이지](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (선택 사항) **[!UICONTROL Type]** 유형별로 오퍼를 필터링할 드롭다운 목록(HTML 오퍼, [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md), 및 [폴더](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![offers_filter 이미지](assets/offers_filter.png)

1. (선택 사항) **[!UICONTROL Source]** 소스(Adobe Target, Adobe Target Classic 및 Adobe Experience Manager)별로 오퍼를 필터링할 드롭다운 목록입니다.

1. (선택 사항) 의 원하는 오퍼 또는 폴더 위로 마우스를 가져간 후 추가 작업을 수행합니다 [!UICONTROL Code Offers] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

   ![코드 오퍼 옵션](assets/offer-picker-large.png)

   옵션은 다음과 같습니다.

   * 보기(자세한 내용은 [오퍼 정의 보기](#section_6B059DD121434E6292CAB393507D010E) 아래.)
   * 편집
   * 복사
   * 이동(예: 하나 이상의 항목을 폴더로 이동하려면 **[!UICONTROL Move]** 원하는 항목의 아이콘을 클릭하고 원하는 폴더를 클릭한 다음 **[!UICONTROL Drop]**.)
   * 삭제

   사용 권한에 따라 일부 옵션의 아이콘이 표시되지 않을 수 있습니다. (예: [!UICONTROL Observer] 권한에는 을(를) 사용할 수 있는 권한이 없습니다. [!UICONTROL Copy] 옵션을 선택합니다.

   오퍼 및 폴더에서 수행할 수 있는 작업에 대한 자세한 내용은 [자산 라이브러리에서 컨텐츠 작업](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (선택 사항) 의 원하는 이미지 오퍼 또는 폴더 위로 마우스를 가져간 후 추가 작업을 수행합니다 [!UICONTROL Image Offers] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

   ![이미지 오퍼 옵션](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   옵션은 다음과 같습니다.

   * 선택
   * 다운로드
   * 속성 보기
   * 편집
   * 주석 달기
   * 복사

   오퍼 및 폴더에서 수행할 수 있는 작업에 대한 자세한 내용은 [자산 라이브러리에서 컨텐츠 작업](/help/main/c-experiences/c-manage-content/assets-working.md).

   >[!NOTE]
   >
   >이미지 오퍼는 [Enterprise 사용자 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 모델.


## 오퍼 정의 보기 {#section_6B059DD121434E6292CAB393507D010E}

의 팝업 카드에서 오퍼 정의 세부 사항을 볼 수 있습니다. [!UICONTROL Offers] 오퍼를 열지 않은 라이브러리입니다.

예를 들어 HTML 오퍼에 대한 다음 오퍼 정의 카드는 정보 아이콘을 클릭하여 액세스할 수 있습니다.

![offer-card-html 이미지](assets/offer-card-html-new.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 오퍼 ID
* 유형
* 마지막 수정 날짜

다음을 클릭합니다. [!UICONTROL View Full Details] 코드 오퍼를 참조하는 활동 및 오퍼 콘텐츠를 보기 위한 링크입니다. 오퍼를 편집할 때 이 방법으로 다른 활동에 영향을 주는 일을 피할 수 있습니다. 정보는 다음과 같습니다. [!UICONTROL Live Activities] 및 [!UICONTROL Inactive Activities].

각 카드에 사용할 수 있는 정보는 오퍼 유형에 따라 다릅니다(HTML 오퍼, [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md), 또는 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md).

오퍼 세부 사항 기능은 이미지 오퍼에 적용되지 않습니다.

<!--

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the [!UICONTROL Visual Experience Composer]

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
