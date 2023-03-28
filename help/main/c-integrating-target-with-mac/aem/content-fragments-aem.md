---
keywords: 경험;json;aem;adobe experience manager;adobe target으로 내보내기;컨텐츠 조각;조각;CF;cf
description: 사용 방법 알아보기 [!DNL Adobe Experience Manager] [!UICONTROL 컨텐츠 조각] in [!DNL Adobe Target] 활동.
title: 사용 방법 [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 컨텐츠 조각]?
feature: Integrations
source-git-commit: cdb0e3f3e1ebb2f9076d3994aed533bd7c296fad
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 2%

---

# AEM [!UICONTROL 컨텐츠 조각]

사용 [!UICONTROL 컨텐츠 조각] (CF를에서 생성) [!DNL Adobe Experience Manager] (AEM)에서 [!DNL Target] 최적화 또는 개인화를 지원하기 위한 활동.

>[!NOTE]
>
>AEM에서 작업할 때 다음 사항을 고려하십시오 [!UICONTROL 컨텐츠 조각] in [!DNL Target]:
> 
>* 이 기능을 사용하려면 다음을 수행해야 합니다 [!DNL Adobe Experience Manager] (AEM) 고객. 자세한 내용은 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A) 아래의 제품에서 사용할 수 있습니다.
>
>* 이 기능은 다음 활동 유형에 사용할 수 있습니다. [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 Target], [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 경험 타깃팅] (XT). 이 기능은 [!UICONTROL 다변량 테스트] (MVT) 및 [!UICONTROL Recommendations] 활동.
>
>* 소비할 수 있습니다 [!UICONTROL 컨텐츠 조각] in [!DNL Target] 를 사용하여 활동 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 전용. 소비할 수 없습니다 [!UICONTROL 컨텐츠 조각] 사용 [!UICONTROL 시각적 경험 작성기] (VEC).


AEM에 대해 자세히 알아보려면 [!UICONTROL 컨텐츠 조각] 및 [!UICONTROL 경험 조각]를 참조하십시오. [AEM [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## 요구 사항 {#requirements}

을 통해 [!UICONTROL 컨텐츠 조각] 기능 [!DNL Target]. 또한 [!DNL AEM] as a Cloud Service. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

연락처 [Adobe Target 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 통합을 활성화하고 인증 세부 정보를 제공합니다.

## 구성 및 작업 [!UICONTROL 컨텐츠 조각] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

내보내려면 [!UICONTROL 컨텐츠 조각] 에서 사용 [!DNL Target] 활동을 수행하려면 AEM에서 몇 가지 사전 단계를 수행해야 합니다. 자세한 내용은 [컨텐츠 조각을 Adobe Target으로 내보내기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

디자인, 만들기, 조정 및 게시에 대한 자세한 내용 [!UICONTROL 컨텐츠 조각]를 참조하십시오. [[!UICONTROL 컨텐츠 조각]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=en){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

## 사용 [!UICONTROL 컨텐츠 조각] in [!DNL Target] 활동 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행한 후에는 [!UICONTROL 컨텐츠 조각] 에 표시 [!UICONTROL 오퍼] 페이지 [!DNL Target].

[!DNL Target] 현재 [!UICONTROL 컨텐츠 조각] 10분마다 가져옵니다. 가져온 [!UICONTROL 컨텐츠 조각] 는 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.

다음 [!UICONTROL 컨텐츠 조각] 로 가져옵니다. [!DNL Target] JSON 오퍼로서 의 경우: 그 [!UICONTROL 컨텐츠 조각] &quot;기본&quot; 버전은 [!DNL AEM]. 는 편집할 수 없습니다 [!UICONTROL 컨텐츠 조각] in [!DNL Target].

다음을 기준으로 필터링하고 검색할 수 있습니다 [!UICONTROL HTML XF], [!UICONTROL JSON XF], 및 [!UICONTROL 컨텐츠 조각] 로 내보낸 서로 다른 오퍼 유형을 구분하는 데 도움이 됩니다. [!DNL Target].

![컨텐츠 조각 유형별로 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

마우스로 아이콘을 가리키면 [!UICONTROL 컨텐츠 조각] 목록에서 [!UICONTROL 보기] 아이콘 ![정보 아이콘](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) 에 대한 추가 정보를 보려면 [!UICONTROL 컨텐츠 조각], 다음을 포함 [!UICONTROL AEM 경로] 및 [!UICONTROL AEM 딥 링크]. 을(를) 클릭합니다. [!UICONTROL 오퍼 사용] 탭을 클릭하여 이 오퍼를 참조하는 활동을 확인합니다.

![컨텐츠 조각 정보 팝업](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

소비할 수 있습니다 [!UICONTROL 컨텐츠 조각] in [!DNL Target] 를 사용하여 활동 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 전용. 사용자 *사용할 수 없음* 소비 [!UICONTROL 컨텐츠 조각] in [!DNL Target] 를 사용하여 활동 [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!UICONTROL 컨텐츠 조각] 에서 JSON으로 내보냅니다. [!DNL Target] 및 는 VEC를 사용하여 만든 활동에는 사용할 수 없습니다.

>[!TIP]
>
>인공 지능, 머신 러닝 및 추천 사용 [!UICONTROL 컨텐츠 조각]:
>
>* 를 완전히 사용하려면 [!DNL Target] AI 및 ML 기능을 선택하여 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) a/B 테스트를 만드는 동안 오류가 발생했습니다.
>
>* [!UICONTROL 컨텐츠 조각] 에서 지원되지 않음 [!DNL Recommendations] 활동. 그러나 를 사용하려면 [!UICONTROL 컨텐츠 조각] 권장 사항용으로 만들기 [!UICONTROL A/B 테스트] 활동(포함) [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target]) 또는 [!UICONTROL 경험 타깃팅] (XT) 활동 및 [오퍼로 권장 사항 포함](/help/main/c-recommendations/recommendations-as-an-offer.md).


**소비하려면 [!UICONTROL 컨텐츠 조각] 사용 [!UICONTROL 양식 기반 경험 작성기]:**

1. in [!DNL Target]에서 경험을 만들거나 편집하는 동안 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)를 클릭하고, 삽입할 페이지에서 위치를 선택합니다. [!DNL AEM] 컨텐츠, **[!UICONTROL 컨텐츠 조각 변경]** 를 [!UICONTROL 컨텐츠 조각 선택] 목록.

   ![content_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   다음 [!UICONTROL 컨텐츠 조각] 목록에는 생성된 컨텐츠가 표시됩니다. [!DNL AEM] 이제 내에서 기본적으로 사용할 수 있습니다 [!DNL Target].

1. 원하는 을 선택합니다 [!UICONTROL 컨텐츠 조각]를 클릭한 다음 **[!UICONTROL 저장]**.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target] 현재 [!UICONTROL 컨텐츠 조각] 10분마다 가져옵니다. 가져온 [!UICONTROL 컨텐츠 조각] 는 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.
* 다음 [!UICONTROL 컨텐츠 조각] 로 가져옵니다. [!DNL Target] JSON 오퍼로서 의 경우: 다음 [!UICONTROL 컨텐츠 조각] &quot;기본&quot; 버전은 [!DNL AEM]. 는 편집할 수 없습니다 [!UICONTROL 컨텐츠 조각] in [!DNL Target].
* 만들 수 없습니다 [!UICONTROL 컨텐츠 조각] 사용 [!DNL Adobe I/O]. 만들기 [!UICONTROL 컨텐츠 조각] 위에서 설명한 대로 AEM 사용.
* 을 업데이트한 경우 [!UICONTROL 컨텐츠 조각] AEM에서 [!UICONTROL 컨텐츠 조각] 에 게시하고 내보내야 합니다. [!DNL Target] 다시 [!DNL Target] 최신 변경 사항을 사용할 수 있습니다.