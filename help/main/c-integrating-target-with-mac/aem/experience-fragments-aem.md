---
keywords: 경험;json;aem;adobe experience manager;adobe target으로 내보내기;경험 구성요소;구성요소;XF
description: 사용 방법 알아보기 [!DNL Adobe Experience Manager] [!UICONTROL 경험 조각] in [!DNL Adobe Target] 활동.
title: 사용 방법 [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 경험 조각]?
feature: Integrations
source-git-commit: 0135831b56c48b0adca49e843c5ddd6574358aa4
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 10%

---

# AEM [!UICONTROL 경험 조각]

사용 [!UICONTROL 경험 조각] (XFs)가에 작성되었습니다. [!DNL Adobe Experience Manager] (AEM)에서 [!DNL Target] 최적화 또는 개인화를 지원하기 위한 활동.

>[!NOTE]
>
>AEM에서 작업할 때 다음 사항을 고려하십시오 [!UICONTROL 경험 조각] in [!DNL Target]:
> 
>* 이 기능을 사용하려면 다음을 수행해야 합니다 [!DNL Adobe Experience Manager] (AEM) 고객. 자세한 내용은 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A) 아래의 제품에서 사용할 수 있습니다.
>* 이 기능은 다음 활동 유형에 사용할 수 있습니다. [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 Target], [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 경험 타깃팅] (XT). 이 기능은 [!UICONTROL 다변량 테스트] (MVT) 및 [!UICONTROL Recommendations] 활동.
>
>* 소비할 수 있습니다 [!UICONTROL 경험 조각] in [!DNL Target] 를 사용하여 활동 [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md).


AEM에 대해 자세히 알아보려면 [!UICONTROL 경험 조각] 컨텐츠 조각과 관련된 내용은 [AEM [!UICONTROL 경험 조각] 및 컨텐츠 조각 개요](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## 요구 사항 {#requirements}

을 통해 [!UICONTROL 경험 조각] 기능 [!DNL Target]. 또한 [!DNL AEM] as a Cloud Service 또는 [!DNL AEM] 6.4 이상 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5.
* [!DNL Adobe Experience Manager] 6.4.
* [!DNL Adobe Target Standard] 또는 [!DNL Adobe Target Premium] 계정이 필요합니다.

[!DNL Adobe Experience Manager] 6.3 및 6.4는 수명이 종료되었으며 더 이상 지원되지 않습니다(확장 지원을 구입한 고객 제외).

연락처 [Adobe Target 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 통합을 활성화하고 인증 세부 정보를 제공합니다.

## 만들기 및 구성 [!UICONTROL 경험 조각] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

를 사용하려면 [!DNL AEM] [!UICONTROL 경험 조각] in [!DNL Target]로 지정하는 경우 다음 단계를 수행해야 합니다.

### 1단계: 통합 [!DNL AEM] with [!DNL Target]

자세한 내용은 다음 문서를 참조하십시오.

* **AEM as a Cloud Service**: [Adobe Target과 통합](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html){target=_blank} 에서 *as a Cloud Service Experience Manager* 안내서.
* **Adobe I/O**: [Adobe I/0을 사용하여 Adobe Target과 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html){target=_blank} 에서 *관리 사용 안내서* 설명서.
* **[!DNL AEM]6.5**: [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=en){target=_blank} 에서 *Adobe Experience Manager 6.5* 설명서.
* **[!DNL AEM]6.4**: [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html){target=_blank} 에서 *Adobe Experience Manager 6.4* 설명서.

### 2단계: 경험 조각 만들기

[!UICONTROL 경험 조각] 에서 작성됨 [!DNL AEM]. 자세한 내용은 다음 문서를 참조하십시오.

* **AEM as a Cloud Service**: [[!UICONTROL 경험 조각]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=en){target=_blank} 에서 *as a Cloud Service Experience Manager* 안내서.
* **[!DNL AEM]6.5**: [[!UICONTROL 경험 조각]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=en){target=_blank} 에서 *Adobe Experience Manager 6.5* 설명서.
* **[!DNL AEM]6.4**: [[!UICONTROL 경험 조각]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=en){target=_blank} 에서 *Adobe Experience Manager 6.4* 설명서.

### 3단계: 구성 [!DNL AEM] 경험 조각을 [!DNL Target]

1. 내 [!DNL AEM]를 클릭하고 원하는 경험 조각 또는 포함 폴더를 선택한 다음 를 클릭합니다 **[!UICONTROL 속성]**.
2. **[!UICONTROL 클라우드 서비스]** 탭을 클릭한 다음, **[!UICONTROL 클라우드 서비스 구성]** 드롭다운 목록에서 **[!UICONTROL Adobe Target]**&#x200B;을 선택합니다.

   이전 단계에서는 사용자 조직의 누군가가 [!DNL Adobe Target] 구성.

3. **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭합니다.

### 4단계: 경험 조각을 게시하여 [!DNL Target]

사용자 [!DNL AEM] 버전에 대한 단계별 지침은 다음 링크를 참조하십시오.

* **AEM as a Cloud Service**: [내보내기 [!UICONTROL 경험 조각] Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=en){target=_blank} 에서 *as a Cloud Service Experience Manager* 안내서.
* **[!DNL AEM]6.5**: [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en){target=_blank} 에서 *Adobe Experience Manager 6.5* 설명서.
* **[!DNL AEM]6.4**: [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html){target=_blank} 에서 *Adobe Experience Manager 6.4* 설명서.

## 사용 [!UICONTROL 경험 조각] in [!DNL Target] 활동 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행하면 경험 조각이 [!UICONTROL 오퍼] 페이지 [!DNL Target].

[!DNL Target] 현재 [!UICONTROL 경험 조각] 10분마다 가져옵니다. 가져온 경험 조각은 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.

경험 조각을 로 가져옵니다 [!DNL Target] 를 HTML 또는 JSON 오퍼로 사용할 수 있습니다. 해당 경험 조각 &quot;기본&quot; 버전은 [!DNL AEM]. 에서 경험 조각을 편집할 수 없습니다 [!DNL Target].

다음을 기준으로 필터링하고 검색할 수 있습니다 [!UICONTROL HTML XF] 및 [!UICONTROL JSON XF] 로 내보낸 경험 조각 유형을 구분하는 데 도움이 됩니다. [!DNL Target].

![경험 조각 유형별로 필터링: Target UI의 HTML 또는 JSON](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

마우스로 목록의 경험 구성요소를 가리킨 다음, [!UICONTROL 보기] 아이콘 ![정보 아이콘](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) 다음을 포함한 경험 조각에 대한 추가 정보를 보려면 다음을 수행하십시오 [!UICONTROL 이름], [!UICONTROL 유형], [!UICONTROL 오퍼 ID], [!UICONTROL 오퍼 경로], 및 마지막 수정 정보. 을(를) 클릭합니다. [!UICONTROL 오퍼 사용] 탭을 클릭하여 이 오퍼를 참조하는 활동을 확인합니다.

![경험 조각 정보 팝업](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

소비할 수 있습니다 [!UICONTROL 경험 조각] in [!DNL Target] 를 사용하여 활동 [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md).


>[!TIP]
>
>인공 지능, 머신 러닝 및 추천 사용 [!UICONTROL 경험 조각]:
>
>* 를 완전히 사용하려면 [!DNL Target] AI 및 ML 기능을 선택하여 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) a/B 테스트를 만드는 동안 오류가 발생했습니다.
>
>* [!UICONTROL 경험 조각] 에서 지원되지 않음 [!DNL Recommendations] 활동. 그러나 를 사용하려면 [!UICONTROL 경험 조각] 권장 사항용으로 만들기 [!UICONTROL A/B 테스트] 활동(포함) [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target]) 또는 [!UICONTROL 경험 타깃팅] (XT) 활동 및 [오퍼로 권장 사항 포함](/help/main/c-recommendations/recommendations-as-an-offer.md).


**VEC를 사용하여 경험 조각을 소비하려면 다음을 수행하십시오.**

1. in [!DNL Target]에서 경험을 만들거나 편집하는 동안 [시각적 경험 작성기](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)를 클릭하고, 삽입할 페이지의 위치를 클릭합니다. [!DNL AEM] 컨텐츠를 만든 다음 원하는 옵션을 선택하여 [!UICONTROL 경험 조각 선택] 목록.

   * [!UICONTROL 다음 항목 전에 삽입]
   * [!UICONTROL 다음 항목 뒤에 삽입]
   * [!UICONTROL 경험 구성요소로 교체]

   다음 [!UICONTROL 경험 조각] 목록에는 생성된 컨텐츠가 표시됩니다. [!DNL AEM] 이제 내에서 기본적으로 사용할 수 있습니다 [!DNL Target].

   >[!NOTE]
   >
   >[!UICONTROL 경험 구성요소로 교체] 선택 사항은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   ![experience_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. 원하는 경험 조각을 선택하고 을 클릭합니다 **[!UICONTROL 완료]**.
1. 활동 구성을 완료합니다.

   다양한 활동 유형의 구성에 대한 자세한 내용은 다음 항목을 참조하십시오.

   * **A/B 테스트:** [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **자동 할당:** [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **자동 Target:** [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **AP(자동화된 개인화):**[자동화된 개인화 활동 작성](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **경험 타깃팅(XT):** [경험 타깃팅 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **A/B 테스트 또는 XT 활동의 Recommendations:** [오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL 경험 조각] 에서 JSON으로 내보냅니다. [!DNL Target] vec를 사용하여 만든 활동에는 을 사용할 수 없습니다. HTML 전용 [!UICONTROL 경험 조각] 는 VEC 기반 활동에서 지원됩니다. JSON을 사용하려면 [!UICONTROL 경험 조각]를 사용하여 만든 활동에서 사용할 수 있습니다 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md).

**양식 기반 경험 작성기를 사용하여 경험 조각을 사용하려면 다음을 수행하십시오.**

1. in [!DNL Target]에서 경험을 만들거나 편집하는 동안 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)를 클릭하고, 삽입할 페이지에서 위치를 선택합니다. [!DNL AEM] 컨텐츠, **[!UICONTROL 경험 조각 변경]** 를 [!UICONTROL 경험 조각 선택] 목록.

   ![experience_fragment_list 이미지](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   다음 [!UICONTROL 경험 조각] 목록에는 생성된 컨텐츠가 표시됩니다. [!DNL AEM] 이제 내에서 기본적으로 사용할 수 있습니다 [!DNL Target].

1. 원하는 경험 조각을 선택하고 을 클릭합니다 **[!UICONTROL 저장]**.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target] 현재 [!UICONTROL 경험 조각] 10분마다 가져옵니다. 가져온 경험 조각은 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.
* 경험 조각을 로 가져옵니다 [!DNL Target] 를 HTML 또는 JSON 오퍼로 사용할 수 있습니다. 경험 조각 &quot;기본&quot; 버전은 에 유지됩니다 [!DNL AEM]. 에서 경험 조각을 편집할 수 없습니다 [!DNL Target].
* 만들 수 없습니다 [!UICONTROL 경험 조각] 사용 [!DNL Adobe I/O]. 만들기 [!UICONTROL 경험 조각] 위에서 설명한 대로 AEM 사용.
* AEM에서 경험 조각을 업데이트하는 경우 경험 조각을 게시하여 로 내보내야 합니다 [!DNL Target] 다시 [!DNL Target] 최신 변경 사항을 사용할 수 있습니다.

## 에서 ClientLibs 및 외부 HTML 제거 [!UICONTROL 경험 조각] 내보내기 대상 [!UICONTROL Target]

에서 경험 조각 오퍼를 사용할 때 [!DNL Target] AEM이 전달하는 페이지에서 타깃팅된 페이지에 이미 필요한 모든 클라이언트 라이브러리가 포함되어 있습니다. 또한 오퍼의 외부 HTML 요소도 필요하지 않습니다.

경우에 따라 전체 HTML 페이지가 경험 조각을 둘러싸며 문제를 발생합니다. 경험 조각 이 HTML, HEAD, BODY 등이 있는 전체 HTML 페이지가 아니라 작은 HTML 부분인지 확인합니다.

자세한 내용은 다음 블로그 게시물을 참조하십시오. [AEM 6.5: ClientLibs 제거 [!UICONTROL 경험 조각] Target으로 내보내기](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## 교육 비디오: AEM 사용 [!UICONTROL 경험 조각] with [!DNL Adobe Target]

다음 비디오는 설정 및 사용 방법을 보여 줍니다 [!UICONTROL 경험 조각]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>다음 [!DNL AEM] 4:54에 설명된 딥 링크 기능이 제거되었습니다.

자세한 내용은 [사용 [!UICONTROL 경험 조각] Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) on *AEM Sites 비디오 및 Tutorials* 페이지.