---
keywords: 대상;대상 규칙;대상 만들기;대상 작성;대상 타깃팅;보고 대상;보고서 대상;세그먼트;사용자 지정 프로필 매개 변수;대상 정의;대상 목록
description: 에서 대상을 사용하는 방법을 알아봅니다. [!DNL Adobe Target].
title: 대상 목록을 사용하려면 어떻게 해야 합니까?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1505'
ht-degree: 23%

---

# 대상자 만들기

의 대상 [!DNL Adobe Target] 타깃팅된 활동에서 콘텐츠 및 경험을 보는 사용자를 결정합니다.

대상은 타깃팅이 가능한 모든 곳에서 사용됩니다. 활동을 타깃팅할 때 다음 선택 사항이 있습니다.

* 에서 재사용 가능한 대상을 선택합니다 [!UICONTROL 대상] list
* [활동별 대상 만들기](/help/main/c-target/creating-activity-only-audience.md) 타겟팅하고
* [여러 대상 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) 임시 대상을 만들려면

에 의해 수집된 대상 데이터를 사용할 수도 있습니다 [!DNL Adobe Analytics] 의 실시간 타깃팅 및 개인화를 위해 [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 응용 프로그램. 자세한 내용은 [Experience Cloud 대상](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=ko-KR) 에서 *Experience Cloud 중앙 인터페이스 구성 요소* 안내서.

에는 두 가지 유형의 대상이 있습니다 [!DNL Target]:

* **타깃팅 대상:** 다양한 유형의 방문자에게 다양한 콘텐츠를 전달하는 데 사용됩니다.
* **보고 대상:** 테스트 결과를 분석할 수 있도록 다양한 유형의 방문자가 동일한 콘텐츠에 어떻게 반응하는지를 판별하는 데 사용됩니다.

   [!DNL Target]에서는 [!DNL Target]을 보고 소스로 사용하는 경우에만 보고 대상을 구성할 수 있습니다. [ Adobe Analytics를 보고 소스](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)로 사용하는 경우에는 [!DNL Analytics]에서 보고 대상을 구성해야 합니다.

## 를 사용하십시오 [!UICONTROL 대상] list {#use-list}

[!UICONTROL 대상자] 목록에 액세스하려면 맨 위 메뉴 막대에서 **[!UICONTROL 대상자]**&#x200B;를 클릭하십시오.

![대상 목록](assets/audiences_list.png)

다음 [!UICONTROL 대상] 목록에는 활동에서 사용할 수 있는 대상이 포함되어 있습니다. 를 사용하십시오 [!UICONTROL 대상] 대상을 만들기, 편집, 복제, 복사 또는 결합할 목록입니다. 대상이 만들어진 소스도 이 목록에 표시됩니다.

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >다음 [!DNL Adobe Experience Platform] 모든 사용자가 소스를 사용할 수 있습니다. [!DNL Target] 고객이 [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}. 에서 사용할 수 있는 대상 [!DNL Adobe Experience Platform] 는 그대로 또는 로 사용할 수 있습니다. [기존 대상과 결합](/help/main/c-target/combining-multiple-audiences.md).
   >
   >사용자에게 [!UICONTROL 승인자] 또는 위 상태 [!DNL Target] 를 [!DNL Target] [!UICONTROL 대상] AEP/RTCDP의 카드([!DNL Real-time Customer Data Platform]).
   >
   >자세한 내용은 [Adobe Experience Platform의 대상 사용](#aep).

사전 정의된 대상(예: &quot;)[!UICONTROL 새 방문자 수]&quot; 및 &quot;[!UICONTROL 재방문자],&quot;의 이름은 변경할 수 없습니다.

원래 에서 만들어진 대상으로 작업하는 경우 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform], [!DNL Target] 에서 대상을 참조하는 경우 경고 표시 [!DNL Target] 나중에 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform].

* 대상이 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform], 두 창에서 모두 경고 아이콘 [!UICONTROL Audience] 목록 및 대상 선택기가 표시됩니다. 도구 설명 [!DNL Target] 또한 UI는 대상자가 [!DNL Experience Cloud] 또는 [!DNL Adobe Experience Platform].
* 삭제된 대상으로 여러 대상을 결합하려고 시도하거나 삭제된 대상을 참조하는 활동을 저장하려고 하면 경고 메시지가 표시됩니다.

사용자 지정 프로필 매개 변수와 `user.` 매개 변수를 타깃팅할 수도 있습니다. 대상을 만들 때 활동을 타깃팅하는 데 사용할 속성을 대상 빌더 창으로 드래그합니다. 원하는 속성이 표시되지 않으면 mbox에서 속성이 실행되지 않았습니다. 다른 사용자 지정 mbox 매개 변수는 [!UICONTROL 사용자 지정 매개 변수] 드롭다운 목록에서 사용할 수 있습니다.

를 사용하십시오 [!UICONTROL 필터] 단추를 필터링합니다. [!UICONTROL 대상] 소스별 목록: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud], 및 [!DNL Adobe Experience Platform].

![의 필터 옵션 [!UICONTROL 대상] list](assets/filters.png)

를 사용하십시오 [!UICONTROL 대상 검색] 검색 상자 [!UICONTROL 대상] 목록. 대상 이름의 일부를 검색하거나 특정 문자열을 따옴표로 묶을 수 있습니다.

대상 이름이나 마지막 수정 날짜별로 [!UICONTROL 대상자] 목록을 정렬할 수 있습니다. 이름이나 날짜별로 정렬하려면 열 헤더를 클릭한 다음, 대상을 오름차순이나 내림차순으로 표시하도록 선택하십시오.

## 대상 정의 보기 {#section_11B9C4A777E14D36BA1E925021945780}

의 다양한 위치에서 팝업 카드에 대한 대상 정의 세부 사항을 볼 수 있습니다 [!DNL Target] 대상을 열지 않은 UI. 이 기능은에서 만든 대상에적용됩니다. [!DNL Target Standard/Premium] 및 [!DNL Target Classic] 또는 API를 통해 만들어집니다.

예를 들어, 다음 대상 정의 카드는 [!UICONTROL 세부 사항 보기] 원하는 대상의 아이콘:

![활동 > 대상 정의](assets/audience_definition_list.png)

다음 대상 정의 카드는 [!UICONTROL 세부 사항 보기] 활동의 아이콘 [!UICONTROL 개요] 페이지:

![활동 > 대상 정의](assets/view-details-activity-overview.png)

대상 정의 카드는 대상자의 유형, 소스 및 속성을 보여줍니다. 클릭 **[!UICONTROL 전체 세부 사항 보기]** 추가 가능한 경우 해당 대상을 참조하는 다른 활동을 표시합니다. 활동의 대상 정의 카드를 보는 경우 [!UICONTROL 개요] 페이지를 클릭한 다음 **[!UICONTROL 대상 사용]**.

대상 사용 정보는 대상을 편집하는 동안 다른 활동에 실수로 영향을 주지 않도록 하는 데 도움이 될 수 있습니다. 정보에는 다음이 포함됩니다 [!UICONTROL 라이브 활동], [!UICONTROL 비활성 활동], [!UICONTROL 보관된 활동], 및 [!UICONTROL 활동 동기화]. 이 기능은 모든 대상(라이브러리 대상 및 [활동 전용 대상](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

대상이 인 경우 [다른 대상과의 결합](/help/main/c-target/combining-multiple-audiences.md) 결합된 대상은 활동을 만드는 데 사용됩니다. 두 대상에 대한 사용 정보는 새로 생성된 활동을 나열합니다.

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

## 다음에서 대상 사용 [!DNL Adobe Experience Platform] {#aep}

[!DNL Adobe Experience Platform]에서 생성된 대상자를 사용하면 더 풍부한 고객 데이터를 제공하여 보다 효과적인 개인화를 실현할 수 있습니다. 다음 [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}(RTCDP), 구축 [!DNL Adobe Experience Platform]는 회사가 여러 엔터프라이즈 소스에서 알려진 데이터와 익명의 데이터를 통합하는 데 도움이 됩니다. 이 프로세스를 통해 모든 채널 및 장치에서 실시간으로 개인화된 고객 경험을 제공하는 데 사용할 수 있는 고객 프로필을 만들 수 있습니다.
[!DNL Target]+
을 [!DNL Real-time Customer Data Platform]에 연결함으로써 고객은 웹 방문의 첫 페이지에서 실시간 밀리초 개인화를 가능하게 하기 위해 이전에는 [!DNL Target]에 액세스할 수 없었던 새로운 세그먼트를 잠금 해제하여 웹 개인화를 강화할 수 있습니다. 에서 만들어진 대상 및 프로필 속성 사용 [!DNL Adobe Experience Platform] 더 풍부한 개인화를 위해 사용 가능한 데이터 포인트를 확장할 수 있습니다.

이러한 통합은 실시간 CDP를 사용하여 주요 사용 사례를 잠금 해제합니다.

* 동일 페이지/다음 히트 개인화
* 최초/알 수 없는 사용자 개인화

주요 기능은 다음과 같습니다.

* 실시간 CDP와 직접 Target 통합/[!DNL Adobe Experience Platform] Edge에 대한 종속성 제거 [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations 카드] 정부 및 정책 집행
* 실시간 CDP 세그먼트 및 공유 프로필 속성

실시간 CDP 프로필 속성 기능 제한 및 고려 사항:

* 주어진 오퍼 내의 속성은 동일한 AEP 샌드박스에서 가져와야 합니다. (즉, 오퍼는 다른 AEP 샌드박스의 속성을 포함할 수 없습니다.)
* 주어진 오퍼 내의 속성은 다른 소스에서 올 수 있습니다. 즉, Target 프로필과 AEP 프로필입니다.(다시 말해, Target에서 왔는지 아니면 AEP 프로필에서 가져왔는지 속성을 결합할 수 있습니다.)
* 오퍼를 정의할 때 속성에 명시적 값이 없는 경우 실시간 CDP 프로필 속성에 대한 기본값을 할당할 수 있습니다. 예를 들어, 동의 또는 거버넌스 정책이 개인화 서비스에서 사용되는 속성을 차단하는 경우 기본값을 대신 사용할 수 있습니다.
* 공유되면 실시간 CDP 프로필 속성이 자동 Target 및 Automated Personalization을 위한 인공 지능/시스템 학습 개인화 모델에서 사용됩니다.

>[!NOTE]
>
>실시간 CDP 프로필 속성 기능은 현재 베타 버전에서 HTML 오퍼 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md).


자세한 내용은 다음 주제를 참조하십시오.

* [대상 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations)의 {target=_blank} *Adobe Experience Platform 릴리스 노트*
* [동일 페이지 및 다음 페이지 개인화를 위한 개인화 대상 구성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)의 {target=_blank} *대상 개요* 안내서.
* [사용자 지정 개인화 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html)의 {target=_blank} *대상 개요* 안내서
* [Adobe Target 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html)의 {target=_blank} *대상 개요* 안내서
* [동일한 페이지 및 다음 페이지 개인화 사용 사례에 대한 개인화 대상 구성](https://www.adobe.com/go/destinations-edge-personalization-en)의 {target=_blank} *대상 개요* 안내서

### 추가 정보

다음에서 대상을 사용할 때 다음 정보를 고려하십시오 [!DNL Adobe Experience Platform]:

#### 개인화 사용 사례

다음 표는 를 사용할 때 사용할 수 있는 개인화 사용 사례 유형(다음 세션 또는 동일한 페이지)을 보여줍니다 [!DNL Adobe Experience Platform Web SDK] at.js를 사용하는 것과 반대됩니다.

| 구현 | 솔루션/사용 사례 사용 |
| --- | --- |
| at.js | **솔루션**:<ul><li>[!DNL Adobe Audience Manager] (AAM) 및 [!DNL Target]</li><li>[!DNL RTCDP] (Premium 또는 Ultimate) 및 [!DNL Target]</li><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul>**사용 사례**:<ul><li>다음 세션 개인화</li></ul> |
| [!DNL Platform Web SDK] 또는 [!DNL AEP Server-Side API] | **솔루션**:<ul><li>[!DNL RTCDP] (모든 SKU) 및 [!DNL Target]</li></ul>**사용 사례**:<ul><li>다음 세션 개인화</li><li>Edge를 통한 동일한 페이지 개인화</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul>**솔루션**:<ul><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul>**사용 사례**:<ul><li>다음 세션 개인화</li><ul><li>[!DNL AAM] 세그먼트</li><li>을 통해 타사 세그먼트 [!DNL AAM]</li></ul><li>Edge를 통한 동일한 페이지 개인화</li><ul><li>[!DNL RTCDP] 세그먼트</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul> |
| 혼합 [!UICONTROL at.js] 및 [!DNL Platform Web SDK] | **솔루션**:<ul><li>[!DNL RTCDP] (모든 SKU) 및 [!DNL Target]</li></ul>**사용 사례**:<ul><li>다음 세션 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!UICONTROL at.js]</li></ul><li>동일한 페이지 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!DNL Platform Web SDK]</li></ul></ul>**솔루션**:<ul><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul>**사용 사례**:<ul><li>다음 세션 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!UICONTROL at.js]</li><li>[!DNL AAM] 세그먼트</li><li>을 통해 타사 세그먼트 [!DNL AAM]</li></ul> |

#### 세그먼트 평가 시간

다음 표는 다른 구현 시나리오에서 발생하는 이벤트에 대한 세그먼트 평가 시간을 보여줍니다.

| 시나리오 | 에지 세그먼트(밀리초 평가) | 스트리밍 세그먼트(분 평가) | 배치 세그먼트 평가 |
| --- | --- | --- | --- |
| 이벤트/데이터 원본 [!DNL Adobe Experience Platform] SDK | 예 | 예 | 해당 사항 없음 |
| 이벤트 출처 [!UICONTROL at.js] | 아니요 | 예 | 해당 사항 없음 |
| 이벤트 출처 [!DNL Target Mobile] SDK | 아니요 | 예 | 해당 사항 없음 |
| 일괄 업로드에서 이벤트 | 아니오 | 아니요 | 예 |
| 오프라인 데이터(스트림)의 이벤트 | 아니요 | 예 | 예 |

### 비디오: 실시간 CDP와 [!DNL Adobe Target]{#RTCDP}

을 사용하여 다음 히트에 대해 개인화하는 방법을 알아봅니다. [!DNL Real-time Customer Data Platform] 및 [!DNL Adobe Target]. 다음 [!DNL Adobe Target] 대상 [!DNL Real-time CDP] 를 사용하면 [!DNL Experience Platform] 세그먼트 [!DNL Adobe Target] 거버넌스 및 개인 정보 지원을 통한 동일한 페이지 및 다음 페이지 개인화.

자세한 내용은 [실시간 CDP 및 Adobe Target을 사용한 다음 히트 개인화](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html)의 {target=_blank} *플랫폼 Tutorials* 안내서.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Adobe Target 블로그 및 비디오:

[[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] 및 [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}

## 교육 비디오: 대상 사용 ![튜토리얼 배지](/help/main/assets/tutorial.png)

다음 비디오에는 대상 사용에 대한 정보가 포함되어 있습니다.

* 용어 &quot;대상&quot; 설명
* 최적화에 대상을 사용하는 두 가지 방법 설명
* 대상자 목록에서 대상자 찾기
* 활동을 대상에 타기팅
* 활동에서 수동 보고에 대상 사용

>[!VIDEO](https://video.tv.adobe.com/v/17398)
