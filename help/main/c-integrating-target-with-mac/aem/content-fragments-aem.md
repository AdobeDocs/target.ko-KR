---
keywords: 경험;json;aem;adobe experience manager;adobe target으로 내보내기;콘텐츠 조각;조각;CF;cf;headless;개인화;실험
description: ' [!DNL Adobe Target] 활동에서  [!DNL Adobe Experience Manager] [!UICONTROL Content Fragments]을(를) 사용하는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments]을(를) 사용하는 방법'
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 21%

---

# AEM [!UICONTROL Content Fragments]

[!DNL Target] 활동의 [!DNL Adobe Experience Manager] (AEM)에서 만든 [!UICONTROL Content Fragments] (CF)를 사용하여 Headless 개인화 및 실험을 지원합니다.

## 고려 사항

[!DNL Target]에서 AEM [!UICONTROL Content Fragments]을(를) 사용하여 작업할 때 다음 사항을 고려하십시오.

* [!DNL Adobe Experience Manager as a Cloud Service] 고객만 이 기능을 사용할 수 있습니다. 자세한 내용은 아래의 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.
* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 있습니다.

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 없습니다.

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만 사용하여 [!DNL Target] 활동에서 [!UICONTROL Content Fragments]을(를) 사용할 수 있습니다. VEC([!UICONTROL Visual Experience Composer])를 사용하여 [!DNL Target] 활동에서 [!UICONTROL Content Fragments]을(를) *할 수 없습니다*.

AEM [!UICONTROL Content Fragments] 및 [!UICONTROL Experience Fragments]에 대한 자세한 내용은 [AEM [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments] 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md)를 참조하세요.

## 요구 사항 {#requirements}

[[!DNL AEM] as a Cloud Service를 사용하고 있어야 합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html){target=_blank}. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

[Adobe Target 고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 통합을 활성화하고 인증 세부 사항을 제공받으십시오.

## [!DNL AEM]에서 [!UICONTROL Content Fragments] 구성 및 작업 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

[!DNL Target] 활동에 사용할 [!UICONTROL Content Fragments]을(를) 내보내려면 AEM에서 몇 가지 사전 단계를 수행해야 합니다. 자세한 내용은 *Experience Manager as a Cloud Service 설명서*&#x200B;의 [Adobe Target으로 콘텐츠 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank}를 참조하십시오.

[!UICONTROL Content Fragments]의 디자인, 만들기, 조정 및 게시와 관련된 자세한 내용은 [콘텐츠 조각 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}에서 [[!UICONTROL Content Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=ko){target=_blank} 및 [Experience Manager as a Cloud Service 조각 작업](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank}을 참조하십시오.

## [!DNL Target] 활동에서 [!UICONTROL Content Fragments] 사용 중 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행하면 [!UICONTROL Content Fragment]이(가) [!DNL Target]의 [!UICONTROL Offers] 페이지에 표시됩니다.

[!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL Content Fragments]을(를) 찾습니다. 가져온 [!UICONTROL Content Fragment]은(는) 10분 이내에 [!DNL Target]에서 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.

[!UICONTROL Content Fragment]을(를) JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL Content Fragment] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL Content Fragment]을(를) 편집할 수 없습니다.

[!UICONTROL HTML XFs], [!UICONTROL JSON XFs] 및 [!UICONTROL Content Fragments] 기준으로 필터링하고 검색하면 [!DNL Target] (으)로 내보내는 다양한 오퍼 유형을 구분할 수 있습니다.

![콘텐츠 조각 유형별 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

마우스로 목록의 [!UICONTROL Content Fragment]을(를) 가리킨 다음 [!UICONTROL View] 아이콘 ![정보 아이콘](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png)을(를) 클릭하여 [!UICONTROL AEM path] 및 [!UICONTROL AEM deep link]을(를) 포함한 [!UICONTROL Content Fragment]에 대한 추가 정보를 볼 수 있습니다. 이 오퍼를 참조하는 활동을 보려면 [!UICONTROL Offer Usage] 탭을 클릭하십시오.

![콘텐츠 조각 정보 팝업](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

[양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만 사용하여 [!DNL Target] 활동에서 [!UICONTROL Content Fragments]을(를) 사용할 수 있습니다. *VEC([시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md))를 사용하여 [!DNL Target] 활동에서 [!UICONTROL Content Fragments]을(를) 사용할 수*&#x200B;없습니다. [!UICONTROL Content Fragments]은(는) [!DNL Target]에서 JSON으로 내보내지며 VEC를 사용하여 만든 활동에서 사용할 수 없습니다.

>[!TIP]
>
>[!UICONTROL Content Fragments]에서 인공 지능, 머신 러닝 및 권장 사항 사용:
>
>* [!DNL Target] AI 및 ML 기능을 완전히 사용하려면 [!UICONTROL A/B Test] 활동을 만드는 동안 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 선택할 수 있습니다.
>
>* [!UICONTROL Content Fragments]은(는) [!DNL Recommendations] 활동에서 지원되지 않습니다. 하지만 권장 사항에 [!UICONTROL Content Fragments]을(를) 사용하려면 [!UICONTROL A/B Test] 활동([!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 포함) 또는 [!UICONTROL Experience Targeting] (XT) 활동을 만들고 [오퍼로 권장 사항을 포함](/help/main/c-recommendations/recommendations-as-an-offer.md)할 수 있습니다.

**[!UICONTROL Form-based Experience Composer]을(를) 사용하여 [!UICONTROL Content Fragments]을(를) 사용하려면:**

1. [!DNL Target]에서 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에서 경험을 만들거나 편집하는 동안 페이지에서 [!DNL AEM] 콘텐츠를 삽입할 위치를 선택한 다음 **[!UICONTROL Change Content Fragment]**&#x200B;을(를) 선택하여 [!UICONTROL Choose a Content Fragment] 목록을 표시합니다.

   ![content_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   [!UICONTROL Content Fragment] 목록에는 이제 [!DNL Target] 내에서 기본적으로 사용할 수 있는 [!DNL AEM]에서 만들어진 콘텐츠가 표시됩니다.

1. 원하는 [!UICONTROL Content Fragment]을(를) 선택한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
1. 활동 구성을 완료합니다.

## 추가 정보

* [!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL Content Fragments]을(를) 찾습니다. 가져온 [!UICONTROL Content Fragment]은(는) 10분 이내에 [!DNL Target]에서 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.
* [!UICONTROL Content Fragment]을(를) JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL Content Fragment] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL Content Fragment]을(를) 편집할 수 없습니다.
* [!DNL Adobe I/O]을(를) 사용하여 [!UICONTROL Content Fragments]을(를) 만들 수 없습니다. 위에서 설명한 대로 AEM을 사용하여 [!UICONTROL Content Fragments]을(를) 만듭니다.
* AEM에서 [!UICONTROL Content Fragment]을(를) 업데이트하는 경우 [!DNL Target]에서 최신 변경 사항을 사용할 수 있도록 [!UICONTROL Content Fragment]을(를) 게시하고 [!DNL Target] (으)로 다시 내보내야 합니다.
