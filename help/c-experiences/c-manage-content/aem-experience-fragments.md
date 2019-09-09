---
description: 최적화 또는 개인화를 지원하기 위해 Target 활동의 AEM(Adobe Experience Manager)에서 작성된 경험 구성요소 사용에 관해 설명합니다.
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
seo-description: 최적화 또는 개인화를 위해 Adobe Target 활동에서 AEM (Adobe Experience Manager) 에서 만든 경험 조각을 사용하는 방법에 대한 정보입니다.
seo-title: Adobe Target의 AEM (Adobe Experience Manager) 경험 조각
solution: Target
title: AEM 경험 구성요소
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# AEM 경험 구성요소{#aem-experience-fragments}

Information about using experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>This feature requires that you are an [!DNL Adobe Experience Manager] (AEM) customer. 자세한 내용은 아래의 [요구 사항](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.

## 개요 {#section_95A91830530F493B81C5C9CDB9B783EA}

[!DNL Target] 활동에 AEM에서 만든 경험 조각을 사용하면 AEM의 사용 편의성 및 강력한 기능을 강력한 자동화된 지능 (AI) 및 머신 러닝 (ML) 기능과 결합하여 경험을 [!DNL Target] 테스트하고 개인화할 수 있습니다.

AEM에서는 모든 콘텐츠 및 자산을 중앙 위치에 가져와서 개인화 전략을 실행합니다. AEM을 사용하면 코드를 작성하지 않고도 한 위치에서 데스크톱, 태블릿 및 휴대 장치의 콘텐츠를 쉽게 만들 수 있습니다. 모든 디바이스용 페이지를 만들 필요가 없습니다. AEM는 컨텐츠를 사용하여 각 경험을 자동으로 조정합니다.

[!DNL Target] 행동, 컨텍스트 및 오프라인 변수를 통합하는 규칙 기반의 AI 기반 머신 러닝 접근 방식을 기반으로 개인화된 경험을 제공할 수 있습니다. With [!DNL Target] you can easily set up and run [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activities to determine the best offers, content, and experiences.

Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using [!DNL Target].

## 요구 사항 {#section_AE6F0971E1574B3AA324003599B96E5A}

You must be provisioned with the experience fragments functionality within [!DNl Target]. 또한 해당하는 AEM 6.3 서비스 팩 또는 AEM 6.4 이상을 사용 중이어야 합니다. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* Adobe Experience Manager 6.4 이상
* Adobe Experience Manager 6.3 SP2 이상
* Adobe Target Standard 또는 Adobe Target Premium 계정
* Contact [Adobe Target Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## AEM에서 경험 조각 만들기 및 구성 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use AEM experience fragments in [!DNL Target], you must perform the following steps:

### 1단계: AEM을 Target과 통합

자세한 내용은 다음 문서를 참조하십시오.

* **AEM 6.3**: [Adobe Experience Manager](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) _6.3_ 설명서에서 Adobe Analytics 및 Adobe Target 으로의 옵트아웃
* **AEM 6.4**: [Adobe Experience Manager](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) _6.4_ 문서에서 Adobe Analytics 및 Adobe Target 으로의 옵트아웃
* **AEM 6.5**: [Adobe Experience Manager](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) *6.5* 문서에서 Adobe Analytics 및 Adobe Target 으로의 옵트아웃

### 2단계: 경험 구성요소 만들기

경험 조각은 AEM에서 만들어집니다. 자세한 내용은 다음 문서를 참조하십시오.

* **AEM 6.3**: [Adobe Experience Manager](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) *6.3* 설명서의 경험 조각을 참조하십시오.
* **AEM 6.4**: [Adobe Experience Manager](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) *6.4* 설명서의 경험 조각을 참조하십시오.
* **AEM 6.5**: [Adobe Experience](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) Manager *6.5* 설명서의 경험 조각

### 3단계: 경험 구성요소를 Target과 공유하도록 AEM 구성

1. AEM 내에서 원하는 경험 구성요소 또는 상위 폴더를 선택한 다음 **[!UICONTROL 속성을 클릭합니다]**.
2. **[!UICONTROL 클라우드 서비스]** 탭을 클릭한 다음, **[!UICONTROL 클라우드 서비스 구성]** 드롭다운 목록에서 **Adobe Target[!UICONTROL 을 선택합니다]**.

   >[!NOTE]
   >
   >The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. **[!UICONTROL 저장 및 닫기를 클릭합니다]**.

### 4단계: 경험 구성요소를 게시하고 Target으로 내보내기

AEM 버전에 따라 단계별 지침을 보려면 다음 링크를 참조하십시오.

* **AEM 6.3**: [Adobe Experience Manager](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) *6.3* 설명서의 Target로 경험 조각 내보내기.
* **AEM 6.4**: [Adobe Experience Manager](https://docs.adobe.com/content/help/en/experience-manager-64/administering/integration/experience-fragments-target.html) *6.4* 설명서의 Target로 경험 조각 내보내기.
* **AEM 6.5**: [Adobe Experience Manager](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) *6.5* 설명서의 Target로 경험 조각 내보내기.

## Target 활동에서 경험 조각 사용 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

앞의 작업을 수행하면 경험 조각이 Target의 [!UICONTROL 오퍼] 페이지에 표시됩니다.

>[!NOTE]
>
>[!DNL Target] 현재 10 분마다 가져올 경험 조각을 찾습니다. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

>[!IMPORTANT]
>
>The experience fragment is currently imported into [!DNL Target] as an HTML offer. 경험 조각 "마스터" 버전은 AEM에 남습니다. 이 경험 조각을 Target에서 편집할 수는 없습니다.

You can hover over an experience fragment in the list, then click the View icon ![View icon](assets/icon_info.png) to see additional information about the experience fragment, including its public offer delivery URL, its AEM path, and a deep link to open the experience fragment inside of AEM.

You can consume Experience Fragments in [!DNL Target] activities using the [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) or the [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>[!DNL Target] AI 및 ML 기능을 완전히 활용하려면 A/B 테스트를 만드는 동안 [자동 할당](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 할당을](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 선택할 수 있습니다.

**VEC를 사용하여 경험 조각을 소비하려면 다음을 수행하십시오.**

1. 에서 [!DNL Target][시각적 경험 작성기에서](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)경험을 만들거나 편집하는 동안 AEM 컨텐츠를 삽입하려는 페이지에서 위치를 클릭한 다음 원하는 옵션을 선택하여 경험 [!UICONTROL 조각] 선택 목록을 표시합니다.

   * [!UICONTROL 다음 항목 전에 삽입]
   * [!UICONTROL 다음 항목 뒤에 삽입]
   * [!UICONTROL 경험 조각으로 바꾸기]
   [!UICONTROL 경험 조각] 목록은 기본적으로 내에서 사용할 수 [!DNL Target]있는 AEM에서 만든 모든 컨텐츠를 표시합니다.

   >[!NOTE]
   >
   >[!UICONTROL 경험 구성요소로 교체] 선택 사항은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   ![](assets/experience_fragment_list.png)

1. Select the desired experience fragment, then click **[!UICONTROL Done]**.
1. 활동 구성을 완료합니다.

   다양한 활동 유형의 구성에 대한 자세한 내용은 다음 항목을 참조하십시오.

   * **A/B 테스트:** [A/B 테스트 만들기](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **자동 할당:** [자동 할당](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **자동 타겟:** [개인화된 경험에 대한 자동 타겟](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **AP(자동화된 개인화):**[자동화된 개인화 활동 작성](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **경험 타깃팅(XT):** [경험 타깃팅 활동 만들기](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **다변량 테스트(MVT):** [다변량 테스트 만들기](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **권장 사항:** [권장 사항 활동 만들기](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**양식 기반 경험 작성기를 사용하여 경험 조각을 사용하려면 다음을 수행하십시오.**

1. [!DNL Target]에서 [양식 기반 경험 작성기에서](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)경험을 만들거나 편집하는 동안 AEM 컨텐츠를 삽입하려는 페이지에서 위치를 선택한 다음 경험 조각 **[!UICONTROL 변경을 선택하여]** 경험 [!UICONTROL 조각] 선택 목록을 표시합니다.

   ![](assets/experience_fragment_list.png)

   [!UICONTROL 경험 조각] 목록은 기본적으로 내에서 사용할 수 [!DNL Target]있는 AEM에서 만든 모든 컨텐츠를 표시합니다.

1. 원하는 경험 조각을 선택하고 **[!UICONTROL 저장을 클릭합니다]**.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target] 현재 10 분마다 가져올 경험 조각을 찾습니다. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The experience fragment is currently imported into [!DNL Target] as an HTML offer. 경험 조각 "마스터" 버전은 AEM에 남습니다. You cannot edit the experience fragment in [!DNL Target].
* 경험으로 JSON 오퍼를 [!DNL Target]가져올 수 있습니다. 그러나 이러한 오퍼는 HTML 오퍼로 가져옵니다. JSON 오퍼 (경험 조각) 는 [!DNL Target] 현재 UI에서 완전히 지원되지 않습니다.

## 교육 비디오: Adobe Target에서 AEM 경험 구성요소 사용 {#section_C0EDC54063464F41A182492D2045BC64}

[Adobe Target에서 AEM 경험 구성요소 사용](https://helpx.adobe.com/experience-manager/kt/sites/using/experience-fragment-target-feature-video-use.html) 비디오는 경험 구성요소를 설정하고 사용하는 방법을 보여 줍니다.
