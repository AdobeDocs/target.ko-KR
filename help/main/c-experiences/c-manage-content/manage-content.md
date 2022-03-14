---
keywords: 컨텐츠;자산;컨텐츠 관리;오퍼;자산 관리;선택 모드 들어가기;선택 모드
description: Adobe Target에서 오퍼 라이브러리를 사용하여 코드 및 이미지 오퍼를 관리하는 방법을 알아봅니다.
title: 코드 및 이미지 오퍼를 관리하려면 어떻게 해야 합니까?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 37%

---

# 오퍼

를 사용하십시오 [!UICONTROL 오퍼] 라이브러리 [!DNL Adobe Target] 코드 오퍼 및 이미지 오퍼 콘텐츠를 관리하려면

1. 라이브러리를 열려면 **[!UICONTROL 오퍼]**&#x200B;를 클릭하십시오.

   이 라이브러리에는 [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) 및 API를 통해 설정한 오퍼가 있습니다. [!DNL Target Classic] 또는 기타 솔루션에서 만든 오퍼는 [!DNL Target Standard/Premium]에서 편집할 수 있습니다.

   다음 [!UICONTROL 오퍼] 페이지의 오른쪽에는 두 개의 탭이 있습니다. [!UICONTROL 코드 오퍼] 및 [!UICONTROL 이미지 오퍼] 유형별로 오퍼를 볼 수 있습니다.

   ![코드 오퍼 및 이미지 오퍼 탭을 보여주는 오퍼 페이지](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (선택 사항) **[!UICONTROL 유형]** 유형별로 오퍼를 필터링하는 드롭다운 목록(HTML 오퍼, [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md), 및 [폴더](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![](assets/offers_filter.png)

1. (선택 사항) **[!UICONTROL 소스]** 소스(Adobe Target, Adobe Target Classic 및 Adobe Experience Manager)별로 오퍼를 필터링하는 드롭다운 목록.

1. (선택 사항) 마우스를 페이지의 원하는 오퍼 또는 폴더로 가져간 후 추가 작업을 수행합니다 [!UICONTROL 코드 오퍼] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

   ![코드 오퍼 선택 사항](assets/offer-picker-large.png)

   옵션은 다음과 같습니다.

   * 보기 (자세한 내용은 [오퍼 정의 보기](#section_6B059DD121434E6292CAB393507D010E) 아래에 나열된 상태로 남아 있습니다.)
   * 편집
   * 복사
   * 이동(예: 하나 이상의 항목을 폴더로 이동하려면 **[!UICONTROL 이동]** 원하는 항목의 아이콘을 클릭하고 원하는 폴더를 클릭한 다음 **[!UICONTROL 드롭]**)
   * 삭제

   사용 권한에 따라, 일부 옵션에 대한 아이콘이 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL 관찰자] 사용 권한에는 [!UICONTROL 복사] 선택 사항입니다.

   오퍼 및 폴더에서 수행할 수 있는 작업에 대한 자세한 내용은 [자산 라이브러리에서 컨텐츠 작업](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (선택 사항)에서 원하는 이미지 오퍼 또는 폴더 위로 마우스를 가져간 후 추가 작업을 수행합니다 [!UICONTROL 이미지 오퍼] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

   ![이미지 오퍼 선택 사항](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   옵션은 다음과 같습니다.

   * 선택
   * 다운로드
   * 속성 보기
   * 편집
   * 주석 달기
   * 복사

   오퍼 및 폴더에서 수행할 수 있는 작업에 대한 자세한 내용은 [자산 라이브러리에서 컨텐츠 작업](/help/main/c-experiences/c-manage-content/assets-working.md).

## 오퍼 정의 보기 {#section_6B059DD121434E6292CAB393507D010E}

에서 팝업 카드에 대한 오퍼 정의 세부 사항을 볼 수 있습니다 [!UICONTROL 오퍼] 라이브러리를 엽니다.

예를 들어 HTML 오퍼에 대한 다음 오퍼 정의 카드는 를 마우스로 가리키면 액세스할 수 있습니다 [!UICONTROL 컨텐츠] 목록을 작성한 후 정보 아이콘을 클릭합니다.

![](assets/offer-card-html.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 소스
* 유형
* 오퍼 ID
* 오퍼 경로
* 마지막 수정 날짜

각 오퍼의 정의 팝업 카드에서 코드 오퍼를 참조하는 활동을 보려면 [!UICONTROL 오퍼 사용량] 탭을 클릭하십시오. 이 기능은 이미지 오퍼에는 적용되지 않습니다. 오퍼를 편집할 때 이 방법으로 다른 활동에 영향을 주는 일을 피할 수 있습니다. 정보에는 다음이 포함됩니다 [!UICONTROL 라이브 활동] 및 [!UICONTROL 비활성 활동].

![](assets/offer-card-usage.png)

다음 오퍼 정의 카드는 리디렉션 오퍼용입니다.

![](assets/offer-card-redirect.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 소스
* 유형
* 오퍼 ID
* 오퍼 경로
* 마지막 수정 날짜
* 리디렉션 URL
* 모든 URL 매개 변수 포함(설정 또는 해제)
* mbox 세션 ID 전달(설정 또는 해제)

다음 오퍼 정의 카드는 원격 오퍼용입니다.

![](assets/offer-card-remote.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 소스
* 유형
* 오퍼 ID
* 오퍼 경로
* 마지막 수정 날짜
* 리디렉션 URL 유형
* 절대 또는 상대 URL

## 교육 비디오: 콘텐츠 저장소 ![개요 배지](/help/main/assets/overview.png)

다음 비디오에는 오퍼 관리에 대한 정보가 포함되어 있습니다.

* [Experience Cloud 자산 라이브러리](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html)와 Target 컨텐츠 라이브러리 간 연결
* 사용자 지정 HTML 오퍼
* 시각적 경험 작성기의 사용자 지정 HTML 오퍼

>[!VIDEO](https://video.tv.adobe.com/v/17387)
