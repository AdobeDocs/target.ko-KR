---
keywords: 경험;json;aem;adobe experience manager;adobe target에 내보내기;경험 조각;조각;XF
description: ' [!DNL Adobe Target] 활동에서  [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments]을(를) 사용하는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]을(를) 사용하는 방법'
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: b29614680b27c9c33f11eed85d8ab4feebc28b0d
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 27%

---

# AEM [!UICONTROL Experience Fragments]

최적화 및 개인화를 지원하기 위해 [!DNL Target] 활동의 [!DNL Adobe Experience Manager]&#x200B;(AEM)에서 만든 [!UICONTROL Experience Fragments]&#x200B;(XF)을(를) 사용합니다.

## 고려 사항

[!DNL Target]에서 AEM [!UICONTROL Experience Fragments]을(를) 사용하여 작업할 때 다음 사항을 고려하십시오.

* 이 기능을 사용하려면 [!DNL Adobe Experience Manager] (AEM) 고객이어야 합니다. 자세한 내용은 아래의 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.
* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 있습니다.

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization]&#x200B;(AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting]&#x200B;(XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 없습니다.

   * [[!UICONTROL Multivariate Test]&#x200B;(MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC) 및 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 [!DNL Target] 활동에서 [!UICONTROL Experience Fragments]을(를) 사용할 수 있습니다.

AEM [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]에 대한 자세한 내용은 [AEM [!UICONTROL Experience Fragments] 및 콘텐츠 조각 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md)를 참조하십시오.

## 요구 사항 {#requirements}

[!DNL Target] 내에서 [!UICONTROL Experience Fragments] 기능을 사용하여 프로비전해야 합니다. 또한 [!DNL AEM] as a Cloud Service 또는 [!DNL AEM] 6.4 이상을 사용하고 있어야 합니다. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard] 또는 [!DNL Adobe Target Premium] 계정

[!DNL Adobe Experience Manager] 6.3 및 6.4는 서비스 종료되어 더 이상 지원되지 않습니다(추가 지원을 구매한 고객 제외).

[Adobe Target 고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 통합을 활성화하고 인증 세부 사항을 제공받으십시오.

## [!DNL AEM]에서 [!UICONTROL Experience Fragments] 만들기 및 구성 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

[!DNL Target]에서 [!DNL AEM] [!UICONTROL Experience Fragments]을(를) 사용하려면 다음 단계를 수행해야 합니다.

### 1단계: [!DNL AEM]을 [!DNL Target]과 통합

자세한 내용은 다음 문서를 참조하십시오.

* **AEM as a Cloud Service**: *Experience Manager as a Cloud Service* 안내서의 [Adobe Target과 통합](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank}
* **Adobe Developer**: *관리 사용 안내서* 설명서에서 [Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html?lang=ko){target=_blank}을(를) 사용하여 Adobe Target과 통합
* **[!DNL AEM]6.5**: *Adobe Experience Manager 6.5* 설명서의 [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=ko){target=_blank}.
* **[!DNL AEM]6.4**: *Adobe Experience Manager 6.4* 설명서의 [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=ko){target=_blank}.

### 2단계: 경험 조각 만들기

[!UICONTROL Experience Fragments]이(가) [!DNL AEM]에 만들어졌습니다. 자세한 내용은 다음 문서를 참조하십시오.

* *AEM as a Cloud Service as a Cloud Service* 안내서의 **Experience Manager**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=ko){target=_blank}.
* *Adobe Experience Manager 6.5* 설명서의 **[!DNL AEM]6.5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=ko){target=_blank}
* *Adobe Experience Manager 6.4* 설명서의 **[!DNL AEM]6.4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=ko){target=_blank}

### 3단계: [!DNL Target]과(와) [!UICONTROL Experience Fragment]을(를) 공유하도록 [!DNL AEM] 구성

1. [!DNL AEM] 내에서 원하는 [!UICONTROL Experience Fragment] 또는 포함된 폴더를 선택한 다음 **[!UICONTROL Properties]**&#x200B;을(를) 클릭합니다.
2. **[!UICONTROL Cloud Services]** 탭을 클릭한 다음 **[!UICONTROL Cloud Service Configuration]** 드롭다운 목록에서 **[!UICONTROL Adobe Target]**&#x200B;을(를) 선택합니다.

   이전 단계에서는 사용자 조직의 누군가가 [!DNL Adobe Target] 구성을 작성했다고 가정합니다.

3. **[!UICONTROL Save & Close]** 아이콘을 클릭합니다.

### 4단계: [!UICONTROL Experience Fragment]을(를) 게시하고 [!DNL Target]&#x200B;(으)로 내보내기

[!DNL AEM] 버전에 따른 단계별 지침은 다음 링크를 참조하십시오.

* **AEM as a Cloud Service**: *Experience Manager as a Cloud Service* 안내서에서 [Adobe Target으로 [!UICONTROL Experience Fragments] 내보내기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank}
* **[!DNL AEM]6.5**: *Adobe Experience Manager 6.5* 설명서의 [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=ko){target=_blank}.
* **[!DNL AEM]6.4**: *Adobe Experience Manager 6.4* 설명서의 [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=ko){target=_blank}.

## [!DNL Target] 활동에서 [!UICONTROL Experience Fragments] 사용 중 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행하면 [!UICONTROL Experience Fragment]이(가) [!DNL Target]의 [!UICONTROL Offers] 페이지에 표시됩니다.

[!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL Experience Fragments]을(를) 찾습니다. 가져온 [!UICONTROL Experience Fragment]은(는) 10분 이내에 [!DNL Target]에서 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.

[!UICONTROL Experience Fragment]을(를) HTML 또는 JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL Experience Fragment] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL Experience Fragment]을(를) 편집할 수 없습니다.

[!DNL Target]&#x200B;(으)로 내보내는 [!UICONTROL Experience Fragment] 형식을 구분할 수 있도록 [!UICONTROL HTML XFs] 및 [!UICONTROL JSON XFs]&#x200B;(으)로 필터링하고 검색할 수 있습니다.

![경험 조각 유형별 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

마우스로 목록의 [!UICONTROL Experience Fragment]을(를) 가리킨 다음 [!UICONTROL View] 아이콘 ![정보 아이콘](/help/main/assets/icons/InfoOutline.svg)을(를) 클릭하여 [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path] 및 마지막 수정 정보를 포함한 [!UICONTROL Experience Fragment]에 대한 추가 정보를 볼 수 있습니다. 이 오퍼를 참조하는 활동을 보려면 [!UICONTROL [!UICONTROL View Full Details]]을(를) 클릭하십시오.

![경험 조각 정보 팝업](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

[시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC) 및 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 [!DNL Target] 활동에서 [!UICONTROL Experience Fragments]을(를) 사용할 수 있습니다.

>[!TIP]
>
>[!UICONTROL Experience Fragments]에서 인공 지능, 머신 러닝 및 권장 사항 사용:
>
>* [!DNL Target]의 AI 및 ML 기능을 완전히 사용하려면 활동을 만드는 동안 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 타겟팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 선택하면 됩니다.
>
>* [!UICONTROL Experience Fragments]은(는) [!DNL Recommendations] 활동에서 지원되지 않습니다. 하지만 권장 사항에 [!UICONTROL Experience Fragments]을(를) 사용하려면 [!UICONTROL A/B Test] 활동([!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 포함) 또는 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동을 만들고 [오퍼로 권장 사항을 포함](/help/main/c-recommendations/recommendations-as-an-offer.md)할 수 있습니다.

**VEC를 사용하여 [!UICONTROL Experience Fragments]을(를) 사용하려면:**

1. [!DNL Target]에서 [시각적 경험 작성기](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)에서 경험을 만들거나 편집하는 동안 페이지에서 [!DNL AEM] 콘텐츠를 삽입할 위치를 클릭한 다음 **[!UICONTROL Replace Content]** > **[!UICONTROL Experience Fragment]**&#x200B;을(를) 클릭하여 [!UICONTROL Experience Fragment] 대화 상자를 표시합니다.

   [!UICONTROL Experience Fragment] 대화 상자에는 이제 [!DNL Target] 내에서 기본적으로 사용할 수 있는 [!DNL AEM]에서 만들어진 콘텐츠가 표시됩니다.

   >[!NOTE]
   >
   >[!UICONTROL Replace Content] 옵션은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   ![experience_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. 원하는 [!UICONTROL Experience Fragment]을(를) 선택한 다음 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 활동 구성을 완료합니다.

   다양한 활동 유형의 구성에 대한 자세한 내용은 다음 항목을 참조하십시오.

   * **A/B 테스트:** [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **자동 할당:** [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **자동 타겟팅:** [자동 타겟팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **AP(Automated Personalization):**&#x200B;[Automated Personalization 활동 작성](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **경험 타겟팅(XT):** [경험 타겟팅 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **A/B 테스트 또는 XT 활동의 추천:** [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!DNL Target]에서 JSON으로 내보낸 [!UICONTROL Experience Fragments]은(는) VEC를 사용하여 만든 활동에서 사용할 수 없습니다. HTML [!UICONTROL Experience Fragments]만 VEC 기반 활동에서 지원됩니다. JSON [!UICONTROL Experience Fragments]을(를) 사용하려면 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 만든 활동에서 사용하십시오.

**[!UICONTROL Form-based Experience Composer]을(를) 사용하여 [!UICONTROL Experience Fragments]을(를) 사용하려면:**

1. [!DNL Target]에서 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에서 경험을 만들거나 편집하는 동안 페이지에서 [!DNL AEM] 콘텐츠를 삽입할 위치를 선택하고 **[!UICONTROL More Details]** 아이콘(![자세히 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 **[!UICONTROL Change Experience Fragment]**&#x200B;을(를) 선택하여 [!UICONTROL Change Experience Fragment] 대화 상자를 표시합니다.

   ![experience_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   [!UICONTROL Experience Fragment] 대화 상자에는 이제 [!DNL Target] 내에서 기본적으로 사용할 수 있는 [!DNL AEM]에서 만들어진 콘텐츠가 표시됩니다.

1. 원하는 [!UICONTROL Experience Fragment]을(를) 선택한 다음 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 활동 구성을 완료합니다.

## 추가 정보

* [!DNL Target]은(는) 현재 10분마다 가져올 [!UICONTROL Experience Fragments]을(를) 찾습니다. 가져온 [!UICONTROL Experience Fragment]은(는) 10분 이내에 [!DNL Target]에서 사용할 수 있어야 하지만, 이 기간은 앞으로 더 짧아질 것입니다.
* [!UICONTROL Experience Fragment]을(를) HTML 또는 JSON 오퍼로 [!DNL Target]에 가져왔습니다. [!UICONTROL Experience Fragment] &quot;기본&quot; 버전이 [!DNL AEM]에 남아 있습니다. [!DNL Target]에서 [!UICONTROL Experience Fragment]을(를) 편집할 수 없습니다.
* [!DNL Adobe Developer]을(를) 사용하여 [!UICONTROL Experience Fragments]을(를) 만들 수 없습니다. 위에서 설명한 대로 AEM을 사용하여 [!UICONTROL Experience Fragments]을(를) 만듭니다.
* AEM에서 [!UICONTROL Experience Fragment]을(를) 업데이트하는 경우 [!DNL Target]에서 최신 변경 사항을 사용할 수 있도록 [!UICONTROL Experience Fragment]을(를) 게시하고 [!DNL Target]&#x200B;(으)로 다시 내보내야 합니다.

## [!UICONTROL Target]&#x200B;(으)로 내보낸 [!UICONTROL Experience Fragments]에서 clientlibs 및 관련 없는 HTML 제거

AEM에서 제공한 페이지에서 [!DNL Target]과(와) 함께 [!UICONTROL Experience Fragment] 오퍼를 사용할 때 타깃팅된 페이지에 필요한 클라이언트 라이브러리가 이미 포함되어 있습니다. 오퍼에 불필요한 HTML 요소도 필요하지 않습니다.

경우에 따라 전체 HTML 페이지가 [!UICONTROL Experience Fragment]을(를) 래핑하여 문제가 발생합니다. [!UICONTROL Experience Fragment]이(가) HTML, HEAD, BODY 등이 있는 전체 HTML 페이지가 아닌 작은 HTML 페이지인지 확인합니다.

자세한 내용은 블로그 게시물 [AEM 6.5: Target으로 내보낸 [!UICONTROL Experience Fragments]에서 clientlib 제거](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}를 참조하십시오.

## 교육 비디오: [!DNL Adobe Target]에서 AEM [!UICONTROL Experience Fragments] 사용

다음 비디오는 [!UICONTROL Experience Fragments]을(를) 설정하고 사용하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/34816?captions=kor)

>[!NOTE]
>
>4:54에서 논의된 [!DNL AEM] 딥 링크 기능이 제거되었습니다.

자세한 내용은 *Adobe Target 비디오 및 자습서* 페이지에서 [AEM Sites과 함께 [!UICONTROL Experience Fragments] 사용](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=ko)을 참조하십시오.
