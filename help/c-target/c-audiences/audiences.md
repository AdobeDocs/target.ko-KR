---
keywords: 대상;대상 규칙;대상 만들기;대상 작성;대상 타깃팅;보고 대상;보고서 대상;세그먼트;사용자 지정 프로필 매개 변수;대상 정의;대상 목록
description: ' [!DNL Adobe Target]에서 [!UICONTROL Audiences] 목록을 사용하는 방법을 알아봅니다.'
title: 대상 목록을 사용하려면 어떻게 해야 합니까?
feature: 대상자
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: f7d73de376c2345b628e3ebadb1d4ab4dc598693
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 31%

---

# 대상자 만들기

[!DNL Adobe Target]의 대상은 타깃팅된 활동에서 컨텐츠 및 경험을 보는 사용자를 결정합니다.

대상은 타깃팅이 가능한 모든 곳에서 사용됩니다. 활동을 타깃팅할 때 다음 선택 사항이 있습니다.

* [!UICONTROL 대상] 목록에서 재사용 가능한 대상을 선택합니다
* [활동별 대상을 ](/help/c-target/creating-activity-only-audience.md) 만들고 타깃팅합니다
* [여러 ](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) 대상을 결합 하여 임시 대상 만들기

[!DNL Adobe Analytics]에서 수집한 대상 데이터를 [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 애플리케이션에서 실시간 타깃팅 및 개인화에 사용할 수도 있습니다. *Experience Cloud 중앙 인터페이스 구성 요소* 안내서의 [Experience Cloud 대상](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=ko-KR)을 참조하십시오.

[!DNL Target]에는 두 가지 유형의 대상이 있습니다.

* **타깃팅 대상:** 다양한 유형의 방문자에게 다양한 콘텐츠를 전달하는 데 사용됩니다.
* **보고 대상:** 테스트 결과를 분석할 수 있도록 다양한 유형의 방문자가 동일한 콘텐츠에 어떻게 반응하는지를 판별하는 데 사용됩니다.

   [!DNL Target]에서는 [!DNL Target]을 보고 소스로 사용하는 경우에만 보고 대상을 구성할 수 있습니다. [ Adobe Analytics를 보고 소스](/help/c-integrating-target-with-mac/a4t/a4t.md)(A4T)로 사용하는 경우에는 [!DNL Analytics]에서 보고 대상을 구성해야 합니다.

## [!UICONTROL Audiences] 목록 사용

[!UICONTROL 대상자] 목록에 액세스하려면 맨 위 메뉴 막대에서 **[!UICONTROL 대상자]**&#x200B;를 클릭하십시오.

![대상 목록](assets/audiences_list.png)

[!UICONTROL 대상] 목록에는 활동에 사용할 수 있는 대상이 포함되어 있습니다. [!UICONTROL 대상] 목록을 사용하여 대상을 만들거나, 편집하거나, 복제하거나, 복사하고, 결합할 수 있습니다. 대상이 만들어진 소스도 이 목록에 표시됩니다.

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >[!DNL Adobe Experience Platform] 소스는 베타 테스트 프로그램에 있지만 [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)를 사용하는 모든 [!DNL Target] 고객이 사용할 수 있습니다. [!DNL Adobe Experience Platform]에서 사용할 수 있는 대상은 있는 그대로 또는 [에서 기존 대상](/help/c-target/combining-multiple-audiences.md)과 결합할 수 있습니다.

&quot;[!UICONTROL 새 방문자]&quot; 및 &quot;[!UICONTROL 재방문자]&quot;와 같이 사전 정의된 대상의 이름은 변경할 수 없습니다.

원래 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 만들어진 대상으로 작업하는 경우, [!DNL Target] 는 나중에 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 삭제된 [!DNL Target] 활동에서 대상을 참조하는 경우 경고합니다.

* [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 대상이 삭제된 경우 [!UICONTROL Audience] 목록 및 대상 선택기 모두에 경고 아이콘이 표시됩니다. [!DNL Target] UI의 도구 팁은 대상이 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 삭제되었음을 나타냅니다.
* 삭제된 대상으로 여러 대상을 결합하려고 시도하거나 삭제된 대상을 참조하는 활동을 저장하려고 하면 경고 메시지가 표시됩니다.

사용자 지정 프로필 매개 변수와 `user.` 매개 변수를 타깃팅할 수도 있습니다. 대상을 만들 때 활동을 타깃팅하는 데 사용할 속성을 대상 빌더 창으로 드래그합니다. 원하는 속성이 표시되지 않으면 mbox에서 속성이 실행되지 않았습니다. 다른 사용자 지정 mbox 매개 변수는 [!UICONTROL 사용자 지정 매개 변수] 드롭다운 목록에서 사용할 수 있습니다.

[!UICONTROL 필터] 단추를 사용하여 [!UICONTROL 대상] 목록을 소스별로 필터링합니다. [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] 및 [!DNL Adobe Experience Platform].

![대상 목록의 필터   옵션](assets/filters.png)

[!UICONTROL 대상 검색] 상자를 사용하여 [!UICONTROL 대상] 목록을 검색합니다. 대상 이름의 일부를 검색하거나 특정 문자열을 따옴표로 묶을 수 있습니다.

대상 이름이나 마지막 수정 날짜별로 [!UICONTROL 대상자] 목록을 정렬할 수 있습니다. 이름이나 날짜별로 정렬하려면 열 헤더를 클릭한 다음, 대상을 오름차순이나 내림차순으로 표시하도록 선택하십시오.

## 대상 정의 보기 {#section_11B9C4A777E14D36BA1E925021945780}

대상을 열지 않고 [!DNL Target] UI의 다양한 위치에서 팝업 카드에 대한 대상 정의 세부 사항을 볼 수 있습니다. 이 기능은 [!DNL Target Standard/Premium]에서 만들거나 [!DNL Target Classic]에서 가져오거나 API를 통해 만든 대상에 적용됩니다.

예를 들어 원하는 대상에 대해 [!UICONTROL 세부 정보 보기] 아이콘을 클릭하여 다음 대상 정의 카드에 액세스합니다.

![활동 > 대상 정의](assets/audience_definition_list.png)

다음 대상 정의 카드는 활동의 [!UICONTROL 개요] 페이지에서 [!UICONTROL 세부 정보 보기] 아이콘을 클릭하여 액세스합니다.

![활동 > 대상 정의](assets/view-details-activity-overview.png)

대상 정의 카드는 대상자의 유형, 소스 및 속성을 보여줍니다. 해당하는 경우 **[!UICONTROL 전체 세부 정보 보기]**&#x200B;를 클릭하여 해당 대상을 참조하는 다른 활동을 확인합니다. 활동의 [!UICONTROL 개요] 페이지에서 대상 정의 카드를 보는 경우 **[!UICONTROL 대상 사용]**&#x200B;을 클릭합니다.

대상 사용 정보는 대상을 편집하는 동안 다른 활동에 실수로 영향을 주지 않도록 하는 데 도움이 될 수 있습니다. 정보에는 [!UICONTROL 라이브 활동], [!UICONTROL 비활성 활동], [!UICONTROL 보관된 활동] 및 [!UICONTROL 활동 동기화]가 포함됩니다. 이 기능은 모든 대상(라이브러리 대상 및 [활동 전용 대상](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483))에 대해 사용할 수 있습니다.

대상이 [다른 대상](/help/c-target/combining-multiple-audiences.md)과 결합되고 결합된 대상을 사용하여 활동을 만드는 경우 두 대상에 대한 사용 정보는 새로 생성된 활동을 나열합니다.

![](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## 교육 비디오: 대상 사용 ![자습서 배지](/help/assets/tutorial.png)

다음 비디오에는 대상 사용에 대한 정보가 포함되어 있습니다.

* 용어 &quot;대상&quot; 설명
* 최적화에 대상을 사용하는 두 가지 방법 설명
* 대상자 목록에서 대상자 찾기
* 활동을 대상에 타기팅
* 활동에서 수동 보고에 대상 사용

>[!VIDEO](https://video.tv.adobe.com/v/17398)
