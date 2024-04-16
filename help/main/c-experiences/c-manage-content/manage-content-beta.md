---
keywords: 컨텐츠;자산;컨텐츠 관리;오퍼;자산 관리;선택 모드 들어가기;선택 모드
description: 오퍼 라이브러리를 사용하여 코드 및 이미지 오퍼를 관리하는 방법을 알아봅니다.
title: 코드 및 이미지 오퍼를 관리하는 방법
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: cd8035d9e2a369b9503763474ce09c4fe2434ae9
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 17%

---

# 오퍼

사용 [!UICONTROL Offers] 라이브러리 [!DNL Adobe Target] 코드 및 이미지 오퍼 컨텐츠를 관리합니다.

>[!NOTE]
>
>이 문서에는 다음 업데이트 정보가 포함되어 있습니다. [!DNL Target] 현재 베타 프로그램의 일부인 사용자 인터페이스입니다. 다음 [!DNL Adobe Target] 팀은 종종 테스트 및 피드백 목적으로 일부 고객을 위해 새로운 기능을 활성화합니다. 테스트 기간이 완료되면 향후 모든 고객에 대해 이러한 기능이 활성화됩니다 [!DNL Target Standard/Premium] 릴리스 및 릴리스 정보에 발표됨.

다음을 클릭합니다. **[!UICONTROL Offers]** 맨 위에 있는 탭 [!DNL Target] 표시할 UI [!UICONTROL Offers] 라이브러리입니다.

![Adobe Target의 오퍼 라이브러리](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

다음 [!UICONTROL Offers] 라이브러리에는 을 통해 설정된 오퍼가 포함되어 있습니다. [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) 및 API [!DNL Target Classic] 또는 기타 솔루션에서 만든 오퍼는 [!DNL Target Standard/Premium]에서 편집할 수 있습니다.

오퍼 라이브러리는 모든 코드 및 이미지 오퍼에 대한 개요를 제공하며 다양한 작업을 수행할 수 있도록 해 줍니다.

| 요소 | 설명 |
|--- |--- |
| 왼쪽 탐색 레일 | 목록 간 전환 [!UICONTROL Code Offers] 또는 [!UICONTROL Image Offers]. |
| [!UICONTROL Show filters] 아이콘<P>![필터 표시 아이콘](/help/main/c-activities/assets/show-filters-icon.png) | 다음을 클릭합니다. **[!UICONTROL Show filters]** 오퍼를 필터링할 아이콘 [!UICONTROL Type], [!UICONTROL Source], 및 [!UICONTROL AEM Type]<P>자세한 내용은 [오퍼 목록에 필터 적용](#filters) 아래요. |
| 필드 검색 | 사용 **[!UICONTROL Search in]** 오퍼를 빠르게 찾거나 오퍼에 표시되는 수를 줄이기 위한 필드 [!UICONTROL Offers] 라이브러리입니다. 다음을 기준으로 검색할 수 있습니다. [!UICONTROL Offer Name], [!UICONTROL AEM Paths], 또는 [!UICONTROL AEM Tags]. |
| [!UICONTROL Create Folder] | 폴더 만들기 를 클릭하여 [!UICONTROL Offer] 코드 오퍼, 이미지 오퍼와 다른 폴더를 포함하는 라이브러리를 사용하여 하위 폴더 구조를 만들 수 있습니다. 자세한 내용은 [오퍼 폴더 만들기](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | 오퍼를 만듭니다. 다양한 오퍼 유형 만들기에 대한 자세한 내용은 다음을 참조하십시오. <ul><li>HTML 오퍼</li><li>[JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| 대량 작업 확인란 | 모든 활동 또는 선택한 활동에 대해 일괄 작업을 수행합니다.<P>사용 가능한 작업 목록(권한 및 오퍼 상태에 따라)은 을 참조하십시오. [빠른 작업 수행](#quick-actions) 아래요. |
| [!UICONTROL Name] | 각 오퍼의 이름입니다.<P>다음을 클릭합니다. **[!UICONTROL Quick Info]** 아이콘 각 오퍼 이름 옆에 있는 아이콘을 클릭하여 오퍼 ID, 유형, 오퍼가 마지막으로 수정된 날짜 및 사용자 등을 포함하여 팝업 카드에서 해당 오퍼에 대한 자세한 정보를 확인합니다.<p>다음을 클릭합니다. **[!UICONTROL More actions]** 각 오퍼 이름 옆에 있는 아이콘(가로 줄임표)을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다. 사용 권한 및 오퍼 상태에 따라 다음 작업을 사용할 수 있습니다. [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], 및 [!UICONTROL Move]. 각 작업에 대한 자세한 내용은 [빠른 작업 수행](#quick-actions) 아래요.<P>테이블 헤더를 클릭하여 목록을 이름별로 오름차순 또는 내림차순으로 정렬합니다. |
| [!UICONTROL Type] | 오퍼 유형: HTML 오퍼, [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md), 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | 오퍼가 만들어진 위치를 표시합니다. [!DNL Adobe Target], [!DNL Adobe Target Classic], 및 [!DNL Adobe Experience Manager]. |

## 오퍼 라이브러리에 필터 적용 {#filters}

다음을 클릭합니다. **[!UICONTROL Show filters]** 아이콘( ![오퍼 페이지에 필터 아이콘 표시](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) )을 사용하여 오퍼를 필터링할 수 있습니다 [!UICONTROL Type], [!UICONTROL Source], 및 [!UICONTROL AEM Type].

![offers_filter 이미지](assets/offers-filter-new.png)

다음 **[!UICONTROL Show filters]** 아이콘을 사용하면 다음 카테고리별로 오퍼를 필터링할 수 있습니다.

* **유형**: HTML 오퍼, [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md), [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

* **소스**: [!DNL Adobe Target], [!DNL Adobe Target Classic], 및 [!DNL Adobe Experience Manager].

* **AEM 유형**: [컨텐츠 조각](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) 및 [경험 조각](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). 다른 조각 유형에 대한 자세한 내용은 [AEM 경험 조각 및 콘텐츠 조각 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## 빠른 작업 수행 {#quick-actions}

해당 아이콘을 클릭하여 다음 빠른 작업을 수행할 수 있습니다.

### 빠른 정보

다음을 클릭합니다. **[!UICONTROL Quick Info]** 아이콘 각 오퍼 이름 옆에 있는 아이콘을 클릭하여 오퍼 ID, 유형, 오퍼가 마지막으로 수정된 날짜 및 사용자 등을 포함하여 팝업 카드에서 해당 오퍼에 대한 자세한 정보를 확인합니다. 사용 가능한 옵션은 오퍼 유형에 따라 다릅니다. HTML 오퍼, [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md), [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md), [원격 오퍼](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### 추가 작업

코드 오퍼와 이미지 오퍼에 사용할 수 있는 작업은 약간 다릅니다. 다음 섹션에는 추가 정보가 포함됩니다.

#### [!UICONTROL Code Offer] 옵션

다음을 클릭합니다. **[!UICONTROL More actions]** 각 오퍼 이름 옆에 있는 아이콘(가로 줄임표)을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다. 사용 권한 및 오퍼 상태에 따라 다음 작업을 사용할 수 있습니다. [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], 및 [!UICONTROL Move].

![Target 오퍼 라이브러리의 추가 작업 옵션](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* 편집
* 복사
* 삭제
* 이동(예: 하나 이상의 항목을 폴더로 이동하려면 **[!UICONTROL Move]** 원하는 항목의 아이콘을 클릭하고 원하는 폴더를 클릭한 다음 **[!UICONTROL Drop]**.)

사용 권한에 따라 일부 옵션의 아이콘이 표시되지 않을 수 있습니다. (예: [!UICONTROL Observer] 권한에는 을(를) 사용할 수 있는 권한이 없습니다. [!UICONTROL Copy] 옵션을 선택합니다.

오퍼 및 폴더에서 수행할 수 있는 작업에 대한 자세한 내용은 [자산 라이브러리에서 컨텐츠 작업](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] 옵션

에서 원하는 이미지 오퍼 또는 폴더 위로 마우스를 가져간 후 추가 작업을 수행합니다. [!UICONTROL Image Offers] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

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
