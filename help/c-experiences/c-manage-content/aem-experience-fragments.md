---
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Adobe Experience Manager(AEM)에서 만든 경험 조각을 최적화 또는 개인화를 돕기 위해 Adobe Target 활동에서 사용하는 방법에 대한 정보입니다.
title: Adobe Target의 Adobe Experience Manager(AEM) 경험 조각
feature: aem
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 14%

---


# AEM 경험 구성요소{#aem-experience-fragments}

Information about using experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>이 기능을 사용하려면 [!DNL Adobe Experience Manager] ([!DNL AEM]) 고객이어야 합니다. 자세한 내용은 아래의 [요구 사항](/help/c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.

## 개요 {#section_95A91830530F493B81C5C9CDB9B783EA}

Using experience fragments created in [!DNL AEM] in [!DNL Target] activities lets you combine the ease-of-use and power of [!DNL AEM] with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in [!DNL Target] to test and personalize experiences at scale.

[!DNL AEM] 모든 콘텐츠와 자산을 중앙에서 통합하여 개인화 전략에 도움이 됩니다. [!DNL AEM] 코드를 작성하지 않고도 한 위치에서 데스크탑, 태블릿 및 모바일 디바이스용 컨텐츠를 손쉽게 제작할 수 있습니다. 모든 디바이스에 맞는 페이지를 제작할 필요가 없습니다. [!DNL AEM] 컨텐츠를 사용하여 각 경험을 자동으로 조정할 수 있습니다.

[!DNL Target] 행동, 컨텍스트 및 오프라인 변수를 결합하는 규칙 기반의 머신 러닝 방식과 AI 기반의 머신 러닝 방식을 결합하여 개인화된 경험을 규모에 맞게 제공할 수 있습니다. With [!DNL Target] you can easily set up and run [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activities to determine the best offers, content, and experiences.

Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using [!DNL Target].

## 요구 사항 {#section_AE6F0971E1574B3AA324003599B96E5A}

You must be provisioned with the experience fragments functionality within [!DNL Target]. In addition, you must be using [!DNL AEM] 6.3 with the appropriate service pack or [!DNL AEM] 6.4 (or later). 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* [!DNL Adobe Experience Manager] 6.4(또는 이상).
* [!DNL Adobe Experience Manager] 6.3 SP2 이상
* [!DNL Adobe Target Standard] 또는 계정 [!DNL Adobe Target Premium] .
* Contact [Adobe Target Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Creating and configuring experience fragments in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use [!DNL AEM] experience fragments in [!DNL Target], you must perform the following steps:

### 1단계:통합 [!DNL AEM] 과 [!DNL Target]

자세한 내용은 다음 문서를 참조하십시오.

* **[!DNL AEM]6.3**: [Adobe Experience Manager 6.3](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) 설명서에서 Adobe Analytics과 Adobe Target에 __ 선택
* **[!DNL AEM]6.4**: [Adobe Experience Manager 6.4](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) 설명서에서 Adobe Analytics과 Adobe Target에 __ 선택
* **[!DNL AEM]6.5**: [Adobe Experience Manager 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) 설명서에서 Adobe Analytics과 Adobe Target에 ** 선택

### 2단계: 경험 구성요소 만들기

Experience fragments are created in [!DNL AEM]. 자세한 내용은 다음 문서를 참조하십시오.

* **[!DNL AEM]6.3**: [](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) Adobe Experience Manager 6.3 ** 설명서에서 경험 조각
* **[!DNL AEM]6.4**: [](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) Adobe Experience Manager 6.4 ** 설명서에서 경험 조각
* **[!DNL AEM]6.5**: [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) Adobe Experience Manager 6.5 ** 설명서에서 경험 조각

### Step 3: Configure [!DNL AEM] to share the experience fragment with [!DNL Target]

1. From within [!DNL AEM], select the desired experience fragment or its containing folder, then click **[!UICONTROL Properties]**.
2. **[!UICONTROL 클라우드 서비스]** 탭을 클릭한 다음, **[!UICONTROL 클라우드 서비스 구성]** 드롭다운 목록에서 **[!UICONTROL Adobe Target]**&#x200B;을 선택합니다.

   >[!NOTE]
   >
   >The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭합니다.

### Step 4: Publish the experience fragment and export it into [!DNL Target]

버전에 따라 [!DNL AEM] 단계별 지침을 보려면 다음 링크를 참조하십시오.

* **[!DNL AEM]6.3**: [](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) Adobe Experience Manager 6.3 *설명서에서 Target으로 경험 조각* 내보내기
* **[!DNL AEM]6.4**: [](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html) Adobe Experience Manager 6.4 *설명서에서 Target으로 경험 조각* 내보내기
* **[!DNL AEM]6.5**: [](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) Adobe Experience Manager 6.5 *설명서에서 Target으로 경험 조각* 내보내기

## Using experience fragments in Target activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the experience fragment displays on the [!UICONTROL Offers] page in [!DNL Target].

>[!NOTE]
>
>[!DNL Target] 현재 10분마다 경험 조각을 가져올 수 있습니다. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

>[!IMPORTANT]
>
>The experience fragment is currently imported into [!DNL Target] as an HTML offer. Note that the experience fragment &quot;primary&quot; version remains in [!DNL AEM]. You cannot edit the experience fragment in [!DNL Target].

목록의 경험 조각 위로 마우스를 가져간 다음 [!UICONTROL 보기] 아이콘 ![보기 아이콘](assets/icon_info.png) 을 클릭하여 해당 공개 오퍼 배달 URL 및 해당 [!DNL AEM] 경로를 포함하여 경험 조각에 대한 추가 정보를 볼 수 있습니다.

You can consume experience fragments in [!DNL Target] activities using the [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) or the [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>To fully utilize the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) while creating an A/B Test.

**VEC를 사용하여 경험 조각을 소비하려면**

1. 에서 [!DNL Target]Visual Experience Composer [에서 경험을 만들거나 편집하는 동안](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)컨텐츠를 삽입할 페이지의 위치를 클릭한 다음 원하는 옵션을 선택하여 경험 조각 [!DNL AEM] 선택 목록을 [!UICONTROL 표시합니다] .

   * [!UICONTROL 다음 항목 전에 삽입]
   * [!UICONTROL 다음 항목 뒤에 삽입]
   * [!UICONTROL 경험 조각으로 바꾸기]

   The [!UICONTROL Experience Fragment] list displays all of the content created in [!DNL AEM] that is now natively available from within [!DNL Target].

   >[!NOTE]
   >
   >[!UICONTROL 경험 구성요소로 교체] 선택 사항은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   ![](assets/experience_fragment_list.png)

1. Select the desired experience fragment, then click **[!UICONTROL Done]**.
1. 활동 구성을 완료합니다.

   다양한 활동 유형의 구성에 대한 자세한 내용은 다음 항목을 참조하십시오.

   * **A/B 테스트:** [A/B 테스트 만들기](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **자동 할당:** [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **자동 Target:**[자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md)
   * **AP(자동화된 개인화):**[자동화된 개인화 활동 작성](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **경험 타깃팅(XT):** [경험 타깃팅 활동 만들기](/help/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **다변량 테스트(MVT):** [다변량 테스트 만들기](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **권장 사항:** [권장 사항 활동 만들기](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**양식 기반 경험 작성기를 사용하여 경험 조각을 소비하려면**

1. 양식 기반 [!DNL Target]경험 작성기에서 경험을 만들거나 편집하는 동안 [페이지](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에서 [!DNL AEM] 컨텐츠를 삽입할 위치를 선택한 다음 경험 조각 **[!UICONTROL 변경]** 을 선택하여 [경험 조각 [!UICONTROL 선택]] 및 [경험 조각 선택] 목록을 표시합니다.

   ![](assets/experience_fragment_list.png)

   The [!UICONTROL Experience Fragment] list displays all of the content created in [!DNL AEM] that is now natively available from within [!DNL Target].

1. 원하는 경험 조각을 선택하고 **[!UICONTROL 저장을 클릭합니다]**.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target] 현재 10분마다 경험 조각을 가져올 수 있습니다. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The experience fragment is currently imported into [!DNL Target] as an HTML offer. Note that the experience fragment &quot;primary&quot; version remains in [!DNL AEM]. You cannot edit the experience fragment in [!DNL Target].
* JSON 오퍼를 경험 조각으로 가져올 수 [!DNL Target]있습니다. 하지만 이러한 오퍼는 HTML 오퍼로 가져옵니다. JSON 오퍼(경험 조각)는 현재 [!DNL Target] UI에서 완전히 지원되지 않습니다.
* Adobe IO를 사용하여 경험 조각을 만들 수 없습니다. 위에 설명된 대로 AEM을 사용하여 경험 조각을 만들어야 합니다.

## Training video: Using AEM experience fragments with Adobe Target ![Tutorial badge](/help/assets/overview.png) {#section_C0EDC54063464F41A182492D2045BC64}

다음 비디오에서는 경험 조각을 설정하고 사용하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>4:54에서 [!DNL AEM] 설명한 종료 기능이 제거되었습니다.

자세한 내용은 [AEM Sites 비디오 및 Tutorials](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) 페이지의 Adobe Target과 ** 함께 경험 조각 사용을 참조하십시오.
