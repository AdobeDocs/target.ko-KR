---
keywords: 컨텐츠;자산;컨텐츠 관리;오퍼;자산 관리;선택 모드 들어가기;선택 모드
description: 오퍼 라이브러리를 사용하여 코드 및 이미지 오퍼를 관리하는 방법을 알아봅니다.
title: 코드 및 이미지 오퍼를 관리하는 방법
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
source-git-commit: fb6383c86503ac9a8313aed65418e9564c93aa1c
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 29%

---

# 오퍼

사용 [!UICONTROL Offers] 라이브러리 [!DNL Adobe Target] 코드 오퍼 및 이미지 오퍼 컨텐츠를 관리합니다.

>[!NOTE]
>
>이 문서에는 다음에 대한 정보가 포함되어 있습니다. [!DNL Target] 현재 Beta 프로그램의 일부인 기능입니다. 다음 [!DNL Adobe Target] 팀은 종종 테스트 및 피드백 목적으로 일부 고객을 위해 새로운 기능을 활성화합니다. 테스트 기간이 완료되면 향후 모든 고객에 대해 이러한 기능이 활성화됩니다 [!DNL Target Standard/Premium] 릴리스 및 릴리스 정보에 발표됨.

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

예를 들어 HTML 오퍼에 대한 다음 오퍼 정의 카드는 의 오퍼 위로 마우스를 가져간 후 액세스합니다 [!UICONTROL Content] 을 나열한 다음 정보 아이콘을 클릭합니다.

![offer-card-html 이미지](assets/offer-card-html.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 소스
* 유형
* 오퍼 ID
* 오퍼 경로
* 마지막 수정 날짜

다음을 클릭합니다. [!UICONTROL Offer Usage] 탭으로 이동하여 각 오퍼의 정의 팝업 카드에서 코드 오퍼를 참조하는 활동을 볼 수 있습니다. 이 기능은 이미지 오퍼에는 적용되지 않습니다. 오퍼를 편집할 때 이 방법으로 다른 활동에 영향을 주는 일을 피할 수 있습니다. 정보는 다음과 같습니다. [!UICONTROL Live Activities] 및 [!UICONTROL Inactive Activities].

![offer-card-use 이미지](assets/offer-card-usage.png)

다음 오퍼 정의 카드는 리디렉션 오퍼용입니다.

![offer-card-redirect 이미지](assets/offer-card-redirect.png)

다음 정보를 사용할 수 있습니다.

* 이름
* 소스
* 유형
* 오퍼 ID
* 오퍼 경로
* 마지막 수정 날짜
* 리디렉션 URL
* 모든 URL 매개 변수 포함(켜기 또는 끄기)
* mbox 세션 ID 전달(켜기 또는 끄기)

다음 오퍼 정의 카드는 원격 오퍼용입니다.

![offer-card-remote 이미지](assets/offer-card-remote.png)

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