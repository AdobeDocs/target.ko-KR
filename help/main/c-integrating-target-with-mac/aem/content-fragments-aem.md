---
keywords: 경험;json;aem;adobe experience manager;adobe target에 내보내기;콘텐츠 조각;조각;CF;cf;headless;personalization;experimentation
description: ' [!DNL Adobe Target] 활동에서  [!DNL Adobe Experience Manager] [!UICONTROL 콘텐츠 조각]을 사용하는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 콘텐츠 조각]을 사용하려면 어떻게 해야 합니까?'
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Target Beta release features?"
feature: Integrations
source-git-commit: 01ade219f81bc1d43fd13321e8fc4f23b230856c
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 100%

---

# AEM [!UICONTROL 콘텐츠 조각]

Headless 개인화 및 실험을 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager](AEM)에서 생성된 [!UICONTROL 콘텐츠 조각]을 사용합니다.

Headless 개인화 및 실험을 위한 AEM 콘텐츠 조각

>[!NOTE]
>
>이 기능은 2023년 4월 6일에 출시될 예정입니다.

>[!NOTE]
>
>[!DNL Target]에서 AEM [!UICONTROL 콘텐츠 조각]을 사용하여 작업할 때 다음 사항을 고려하십시오.
> 
>* 이 기능을 사용하려면 [!DNL Adobe Experience Manager] (AEM) 고객이어야 합니다. 자세한 내용은 아래의 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.
>
>* 이 기능을 사용할 수 있는 활동 유형: [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 타겟팅], [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 경험 타겟팅] (XT). 이 기능은 [!UICONTROL 다변량 테스트] (MVT) 및 [!UICONTROL Recommendations] 활동에서 사용할 수 없습니다.
>
>* [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만을 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다. [!UICONTROL 시각적 경험 작성기](VEC)만을 사용하여 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다.


AEM [!UICONTROL 콘텐츠 조각] 및 [!UICONTROL 경험 조각]에 대해 자세히 알아보려면 [AEM [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각] 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md)를 참조하십시오.

## 요구 사항 {#requirements}

[!DNL Target] 내의 [!UICONTROL 콘텐츠 조각] 기능을 공급받아야 합니다. 또한 [!DNL AEM] as a Cloud Service를 사용하고 있어야 합니다. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

[Adobe Target 고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 통합을 활성화하고 인증 세부 사항을 제공받으십시오.

## [!DNL AEM]에서 [!UICONTROL 콘텐츠 조각] 구성 및 작업 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

[!DNL Target] 활동에서 사용하기 위해 [!UICONTROL 콘텐츠 조각]을 내보내려면 AEM에서 몇 가지 예비 단계를 수행해야 합니다. 자세한 내용은 *Experience Manager as a Cloud Service 설명서*&#x200B;의 [Adobe Target으로 콘텐츠 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank}를 참조하십시오. 이 링크는 출시일(2023년 4월 12일)에 사용할 수 있습니다.

[!UICONTROL 콘텐츠 조각]의 디자인, 생성, 조정 및 게시에 대한 내용은 [[!UICONTROL 콘텐츠 조각]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=ko){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}을 참조하십시오.

## [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각] 사용 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

앞의 작업을 수행하면 [!UICONTROL 콘텐츠 조각]이 [!DNL Target]의 [!UICONTROL 오퍼] 페이지에 표시됩니다.

[!DNL Target]은 현재 10분마다 가져올 [!UICONTROL 콘텐츠 조각]을 찾습니다. 가져온 [!UICONTROL 콘텐츠 조각]는 10분 이내에 [!DNL Target]에서 사용할 수 있으나, 이 시간대는 향후 단축될 것입니다.

[!UICONTROL 콘텐츠 조각]을 JSON 오퍼로서 [!DNL Target]으로 가져옵니다. [!UICONTROL 콘텐츠 조각] “기본” 버전은 [!DNL AEM]에 유지됩니다. [!UICONTROL 콘텐츠 조각]을 [!DNL Target]에서 편집할 수는 없습니다.

[!UICONTROL HTML XF], [!UICONTROL JSON XF] 및 [!UICONTROL 콘텐츠 조각]별로 필터링하고 검색하여 [!DNL Target]으로 내보내는 여러 오퍼 유형을 쉽게 구분할 수 있습니다.

![콘텐츠 조각 유형별 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

목록에서 [!UICONTROL 콘텐츠 조각]을 마우스로 가리킨 다음 [!UICONTROL 보기] 아이콘 ![정보 아이콘](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png)을 클릭하여 해당 [!UICONTROL AEM 경로] 및 [!UICONTROL AEM 딥 링크]를 포함해 [!UICONTROL 콘텐츠 조각]에 대한 추가 정보를 볼 수 있습니다. 이 오퍼를 참조하는 활동을 보려면 [!UICONTROL 오퍼 사용] 탭을 클릭합니다.

![콘텐츠 조각 정보 팝업](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

[양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만을 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다. [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC)를 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을 사용할 수 *없습니다*. [!UICONTROL 콘텐츠 조각]은 [!DNL Target]에서 JSON으로 내보내며 VEC를 사용하여 생성된 활동에서 사용할 수 없습니다.

>[!TIP]
>
>[!UICONTROL 콘텐츠 조각]과 함께 인공 지능, 기계 학습 및 추천 사용:
>
>* [!DNL Target]의 AI 및 ML 기능을 완전히 사용하려면 A/B 테스트를 작성하는 동안 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 타겟팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 선택하면 됩니다.
>
>* [!UICONTROL 콘텐츠 조각]은 [!DNL Recommendations] 활동에서 지원되지 않습니다. 단, 추천에 [!UICONTROL 콘텐츠 조각]을 사용하려면 [!UICONTROL A/B 테스트] 활동([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅] 포함) 또는 [!UICONTROL 경험 타겟팅] (XT) 활동을 만들고 [오퍼를 추천으로 포함](/help/main/c-recommendations/recommendations-as-an-offer.md)하면 됩니다.


**[!UICONTROL 양식 기반 경험 작성기]를 사용하여 [!UICONTROL 콘텐츠 조각]을 사용하는 방법:**

1. [!DNL Target]에서 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에 경험을 생성하거나 편집하는 동안 [!DNL AEM] 콘텐츠를 삽입할 페이지 위치를 선택한 다음 **[!UICONTROL 콘텐츠 조각 변경]**&#x200B;을 선택하여 [!UICONTROL 콘텐츠 조각 선택] 목록을 표시합니다.

   ![content_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   [!UICONTROL 콘텐츠 조각] 목록에는 이제 [!DNL Target] 내에서 기본적으로 사용할 수 있는 [!DNL AEM]에서 만들어진 모든 콘텐츠가 표시됩니다.

1. 원하는 [!UICONTROL 콘텐츠 조각]을 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target]은 현재 10분마다 가져올 [!UICONTROL 콘텐츠 조각]을 찾습니다. 가져온 [!UICONTROL 콘텐츠 조각]는 10분 이내에 [!DNL Target]에서 사용할 수 있으나, 이 시간대는 향후 단축될 것입니다.
* [!UICONTROL 콘텐츠 조각]을 JSON 오퍼로서 [!DNL Target]으로 가져옵니다. 해당 [!UICONTROL 콘텐츠 조각] “기본” 버전은 [!DNL AEM]에 유지됩니다. [!UICONTROL 콘텐츠 조각]을 [!DNL Target]에서 편집할 수는 없습니다.
* [!DNL Adobe I/O]. 를 사용하여 [!UICONTROL 콘텐츠 조각]을 만들 수 없습니다. 위에서 설명한 대로 AEM을 사용하여 [!UICONTROL 콘텐츠 조각]을 만듭니다.
* AEM에서 [!UICONTROL 콘텐츠 조각]을 업데이트하는 경우, [!DNL Target]에서 최신 변경 내용을 사용할 수 있도록 [!UICONTROL 콘텐츠 조각]을 [!DNL Target]에 게시하고 내보냅니다.