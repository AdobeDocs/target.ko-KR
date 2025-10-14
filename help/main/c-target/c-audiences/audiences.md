---
keywords: 대상자;대상자 규칙;대상자 만들기;대상자 작성;대상자 타기팅;보고 대상자;보고서 대상자;세그먼트;사용자 지정 프로필 매개 변수;대상자 정의;대상자 목록
description: ' [!DNL Adobe Target]에서 대상을 사용하는 방법을 알아봅니다.'
title: 대상 목록은 어떻게 사용합니까?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 22%

---

# 대상자 만들기

[!DNL Adobe Target]의 대상은 타깃팅된 활동에서 콘텐츠 및 경험을 보게 되는 사용자를 결정합니다.

대상은 타깃팅이 가능한 모든 곳에서 사용됩니다. 활동을 타깃팅할 때 다음과 같은 옵션이 있습니다.

* [!UICONTROL Audiences] 목록에서 재사용 가능한 대상 선택
* [활동별 대상 만들기](/help/main/c-target/creating-activity-only-audience.md) 및 타깃팅
* [여러 대상을 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)하여 임시 대상을 만듭니다.

[!DNL Adobe Analytics] 및 다른 [!DNL Target] 응용 프로그램에서 실시간 타깃팅 및 개인화에 [!DNL Adobe Experience Cloud]이(가) 수집한 대상 데이터를 사용할 수도 있습니다. [Experience Cloud 중앙 인터페이스 구성 요소](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=ko-KR) 안내서에서 *Experience Cloud 대상*&#x200B;을 참조하십시오.

[!DNL Target]에는 두 가지 유형의 대상이 있습니다.

* **타깃팅 대상:** 다양한 유형의 방문자에게 다양한 콘텐츠를 전달하는 데 사용됩니다.
* **보고 대상:** 테스트 결과를 분석할 수 있도록 다양한 유형의 방문자가 동일한 콘텐츠에 어떻게 반응하는지를 판별하는 데 사용됩니다.

  [!DNL Target]에서는 [!DNL Target]을 보고 소스로 사용하는 경우에만 보고 대상자를 구성할 수 있습니다. [Adobe Analytics을 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)하는 경우 [!DNL Analytics] 내에서 보고 대상을 구성해야 합니다.

## [!UICONTROL Audiences] 목록 사용 {#use-list}

[!UICONTROL Audiences] 목록에 액세스하려면 맨 위 메뉴 막대에서 **[!UICONTROL Audiences]**&#x200B;을(를) 클릭하십시오.

![[!UICONTROL Audiences] 목록](assets/audiences_list.png)

[!UICONTROL Audiences] 목록에는 활동에 사용할 수 있는 대상이 포함되어 있습니다. [!UICONTROL Audiences] 목록을 사용하여 대상자를 만들거나 편집하거나 복제하거나 결합하십시오. 대상이 만들어진 소스도 이 목록에 표시됩니다.

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

  >[!NOTE]
  >
  >[!DNL Adobe Experience Platform] 소스는 [!DNL Target]Adobe Experience Platform Web SDK[를 사용하는 모든 &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} 고객이 사용할 수 있습니다. [!DNL Adobe Experience Platform]에서 사용할 수 있는 대상은 그대로 사용하거나 [기존 대상과 결합](/help/main/c-target/combining-multiple-audiences.md)할 수 있습니다.
  >
  >AEP/RTCDP([!UICONTROL Approver])에서 [!DNL Target] [!DNL Target] 카드를 구성하려면 [!UICONTROL Destinations]에서 사용자가 [!DNL Real-time Customer Data Platform] 이상 상태여야 합니다.
  >
  >자세한 내용은 [Adobe Experience Platform의 대상 사용](#aep)을 참조하세요.

&quot;[!UICONTROL New Visitors]&quot; 및 &quot;[!UICONTROL Returning Visitors]&quot;과(와) 같이 미리 정의된 대상의 이름을 바꿀 수 없습니다.

원래 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 만들어진 대상자를 사용하여 작업할 때 [!DNL Target]은(는) [!DNL Target] 활동에서 나중에 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 삭제된 대상자를 참조하는 경우 알림을 보냅니다.

* 대상자가 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 삭제된 경우 [!UICONTROL Audience] 목록과 대상자 선택기에 모두 경고 아이콘이 표시됩니다. [!DNL Target] UI의 도구 설명은 대상자가 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform]에서 삭제되었음을 나타냅니다.
* 삭제된 대상으로 여러 대상을 결합하려고 시도하거나 삭제된 대상을 참조하는 활동을 저장하려고 하면 경고 메시지가 표시됩니다.

사용자 지정 프로필 매개 변수와 `user.` 매개 변수를 타깃팅할 수도 있습니다. 대상을 만들 때 활동을 타깃팅하는 데 사용할 속성을 대상 빌더 창으로 드래그합니다. 원하는 속성이 표시되지 않으면 mbox에서 속성을 실행하지 않은 것입니다. 다른 사용자 지정 mbox 매개 변수는 [!UICONTROL Custom Parameters] 드롭다운 목록에서 사용할 수 있습니다.

[!UICONTROL Filters] 단추를 사용하여 [!UICONTROL Audiences], [!DNL Adobe Target], [!DNL Adobe Target Classic] 및 [!DNL Experience Cloud] 원본별로 [!DNL Adobe Experience Platform] 목록을 필터링하세요.

![&#x200B; 목록의 [!UICONTROL Audiences]필터 옵션](assets/filters.png)

[!UICONTROL Search audiences] 상자를 사용하여 [!UICONTROL Audiences] 목록을 검색합니다. 대상 이름의 일부를 검색하거나 특정 문자열을 따옴표로 묶을 수 있습니다.

대상 이름이나 마지막으로 수정한 날짜별로 [!UICONTROL Audiences] 목록을 정렬할 수 있습니다. 이름이나 날짜별로 정렬하려면 열 헤더를 클릭한 다음, 대상자를 오름차순이나 내림차순으로 표시하도록 선택하십시오.

## 대상 정의 보기 {#section_11B9C4A777E14D36BA1E925021945780}

대상을 열지 않고도 [!DNL Target] UI의 다양한 위치에서 팝업 카드의 대상 정의 세부 사항을 볼 수 있습니다. 이 기능은 [!DNL Target Standard/Premium]에서 만든 대상과 [!DNL Target Classic]에서 가져오거나 API를 통해 만든 대상에게 적용됩니다.

예를 들어 원하는 대상의 [!UICONTROL View Details] 아이콘을 클릭하여 다음 대상 정의 카드에 액세스합니다.

![활동 > 대상자 정의](assets/audience_definition_list.png)

다음 대상 정의 카드는 활동의 [!UICONTROL View Details] 페이지에서 [!UICONTROL Overview] 아이콘을 클릭하여 액세스합니다.

![활동 > 대상자 정의](assets/view-details-activity-overview.png)

대상 정의 카드는 대상의 유형, 소스 및 속성을 보여 줍니다. 해당되는 경우 해당 대상자를 참조하는 다른 활동을 보려면 **[!UICONTROL View full details]**&#x200B;을(를) 클릭하십시오. 활동의 [!UICONTROL Overview] 페이지에서 대상 정의 카드를 보는 경우 **[!UICONTROL Audience Usage]**&#x200B;을(를) 클릭합니다.

대상 사용 정보는 대상을 편집하는 동안 다른 활동에 실수로 영향을 주지 않도록 하는 데 도움이 될 수 있습니다. 정보에는 [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities] 및 [!UICONTROL Syncing Activities]이(가) 포함됩니다. 이 기능은 모든 대상(라이브러리 대상 및 [활동 전용 대상](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483))에 사용할 수 있습니다.

대상이 [다른 대상과 결합](/help/main/c-target/combining-multiple-audiences.md)되고 결합된 대상이 활동을 만드는 데 사용되는 경우 두 대상의 사용 정보는 새로 만든 활동을 나열합니다.

![audience_definition_list_usage 이미지](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/main/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/main/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/main/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/main/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## [!DNL Adobe Experience Platform]의 대상자 사용 {#aep}

[!DNL Adobe Experience Platform]에서 만든 대상을 사용하면 더 풍부한 고객 데이터를 제공하여 보다 효과적인 개인화를 실현할 수 있습니다.

자세한 내용은 [대상 사용 [!DNL Adobe Experience Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#aep)을 참조하세요.

## 교육 비디오: 대상 ![튜토리얼 배지](/help/main/assets/tutorial.png) 사용

다음 비디오에는 대상 사용에 대한 정보가 포함되어 있습니다.

* 용어 &quot;대상&quot; 설명
* 최적화에 대상을 사용하는 두 가지 방법 설명
* 대상자 목록에서 대상자 찾기
* 활동을 대상자에 타기팅
* 활동에서 수동 보고에 대상 사용

>[!VIDEO](https://video.tv.adobe.com/v/30527?captions=kor)
