---
keywords: 경험;json;aem;adobe experience manager;adobe target으로 내보내기;콘텐츠 조각;조각;CF;cf;headless;개인화;실험
description: ' [!DNL Adobe Target] 활동에서  [!DNL Adobe Experience Manager] [!UICONTROL 콘텐츠 조각]을 사용하는 방법을 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 콘텐츠 조각]을(를) 사용하는 방법'
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
TQID: https://experienceleague.adobe.com/tb500kFSZoR3czs10Gs3EIOWEX2ybnd7tSWwDmWSMWQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 775
ht-degree: 20%

---

# AEM [!UICONTROL 콘텐츠 조각]

Headless 개인화 및 실험을 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager]&#x200B;(AEM)에서 만든 [!UICONTROL 콘텐츠 조각]&#x200B;(CF)을 사용합니다.

## 고려 사항

[!DNL Target]의 AEM [!UICONTROL 콘텐츠 조각]을 사용하여 작업할 때 다음 사항을 고려하십시오.

* [!DNL Adobe Experience Manager as a Cloud Service] 고객만 이 기능을 사용할 수 있습니다. 자세한 내용은 아래의 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.
* [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]을(를) 다음 활동 유형에 사용할 수 있습니다.

   * [[!UICONTROL A/B 테스트]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL 자동 할당]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL 자동 타깃팅]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL 경험 타기팅] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]은(는) 다음 활동 유형에 사용할 수 없습니다.

   * [[!UICONTROL 다변량 테스트] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL 추천]](/help/main/c-recommendations/recommendations.md)

* [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다. *VEC([!UICONTROL 시각적 경험 작성기])를 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을(를) 사용할 수*&#x200B;없습니다.

AEM [!UICONTROL 콘텐츠 조각] 및 [!UICONTROL 경험 조각]에 대한 자세한 내용은 [AEM [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각] 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md)를 참조하십시오.

## 요구 사항 {#requirements}

[[!DNL AEM] as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html){target=_blank}을 사용하고 있어야 합니다. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

[Adobe Target 고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 통합을 활성화하고 인증 세부 사항을 제공받으십시오.

## [!DNL AEM]에서 [!UICONTROL 콘텐츠 조각] 구성 및 작업 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

[!DNL Target] 활동에서 사용할 [!UICONTROL 콘텐츠 조각]을 내보내려면 AEM에서 몇 가지 사전 단계를 수행해야 합니다. 자세한 내용은 *Adobe Target as a Cloud Service 설명서*&#x200B;에서 [Experience Manager으로 콘텐츠 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank}를 참조하십시오.

[!UICONTROL 콘텐츠 조각]의 디자인, 만들기, 조정 및 게시에 대한 자세한 내용은 [Experience Manager as a Cloud Service 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}에서 [[!UICONTROL 콘텐츠 조각]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=ko){target=_blank} 및 [콘텐츠 조각을 사용하여 작업](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank}을 참조하세요.

## [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각] 사용 중 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행하면 [!DNL Target]의 [!UICONTROL 오퍼] 페이지에 [!UICONTROL 콘텐츠 조각]이 표시됩니다.

[!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL 콘텐츠 조각]을(를) 찾습니다. 가져온 [!UICONTROL 콘텐츠 조각]은(는) [!DNL Target]에서 10분 이내에 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.

[!UICONTROL 콘텐츠 조각]을(를) JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL 콘텐츠 조각] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL 콘텐츠 조각]을(를) 편집할 수 없습니다.

[!UICONTROL HTML XF], [!UICONTROL JSON XF] 및 [!UICONTROL 콘텐츠 조각]을(를) 기준으로 필터링하고 검색하면 [!DNL Target]에 내보내는 서로 다른 오퍼 형식을 구분할 수 있습니다.

![콘텐츠 조각 유형별 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

목록의 [!UICONTROL 경험 조각] 위로 마우스를 가져간 다음 [!UICONTROL 보기] 아이콘 ![정보 아이콘](/help/main/assets/icons/InfoOutline.svg)을 클릭하여 [!UICONTROL 이름], [!UICONTROL 유형], [!UICONTROL 오퍼 ID], [!UICONTROL 오퍼 경로] 및 마지막 수정 정보를 포함한 [!UICONTROL 콘텐츠 조각]에 대한 추가 정보를 볼 수 있습니다. 이 오퍼를 참조하는 활동을 보려면 [!UICONTROL [!UICONTROL 전체 세부 정보 보기]]를 클릭하십시오.

[양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다. *VEC([시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md))를 사용하여 [!DNL Target] 활동에서 [!UICONTROL 콘텐츠 조각]을(를) 사용할 수*&#x200B;없습니다. [!UICONTROL 콘텐츠 조각]을(를) [!DNL Target]에서 JSON으로 내보냈으며 VEC를 사용하여 만든 활동에서는 사용할 수 없습니다.

>[!TIP]
>
>[!UICONTROL 콘텐츠 조각]에서 인공 지능, 머신 러닝 및 권장 사항 사용:
>
>* [!DNL Target] AI 및 ML 기능을 완전히 사용하려면 [!UICONTROL A/B 테스트] 활동을 만드는 동안 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 선택할 수 있습니다.
>
>* [!UICONTROL 콘텐츠 조각]은(는) [!DNL Recommendations] 활동에서 지원되지 않습니다. 그러나 권장 사항에 [!UICONTROL 콘텐츠 조각]을(를) 사용하려면 [!UICONTROL A/B 테스트] 활동([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 포함) 또는 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동을 만들고 [오퍼로 권장 사항을 포함](/help/main/c-recommendations/recommendations-as-an-offer.md)할 수 있습니다.

**[!UICONTROL 양식 기반 경험 작성기]를 사용하여 [!UICONTROL 콘텐츠 조각]을 사용하려면**

1. [!DNL Target]에서 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에서 경험을 만들거나 편집하는 동안 페이지에서 [!DNL AEM] 콘텐츠를 삽입할 위치를 선택한 다음 **[!UICONTROL 콘텐츠 조각 변경]**&#x200B;을 선택하여 [!UICONTROL 콘텐츠 조각 선택] 목록을 표시합니다.

   ![content_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   [!UICONTROL 콘텐츠 조각] 목록에는 이제 [!DNL Target] 내에서 기본적으로 사용할 수 있는 [!DNL AEM]에서 만들어진 콘텐츠가 표시됩니다.

1. 원하는 [!UICONTROL 콘텐츠 조각]을 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 활동 구성을 완료합니다.

## 추가 정보

* [!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL 콘텐츠 조각]을(를) 찾습니다. 가져온 [!UICONTROL 콘텐츠 조각]은(는) [!DNL Target]에서 10분 이내에 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.
* [!UICONTROL 콘텐츠 조각]을(를) JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL 콘텐츠 조각] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL 콘텐츠 조각]을(를) 편집할 수 없습니다.
* [!DNL Adobe I/O]을(를) 사용하여 [!UICONTROL 콘텐츠 조각]을(를) 만들 수 없습니다. 위에서 설명한 대로 AEM을 사용하여 [!UICONTROL 콘텐츠 조각]을 만듭니다.
* AEM에서 [!UICONTROL 콘텐츠 조각]을(를) 업데이트하는 경우 [!DNL Target]에서 최신 변경 사항을 사용할 수 있도록 [!UICONTROL 콘텐츠 조각]을(를) 게시하고 [!DNL Target]&#x200B;(으)로 다시 내보내야 합니다.
