---
keywords: 경험;json;aem;adobe experience manager;adobe target으로 내보내기;경험 구성요소;구성요소;XF
description: 사용 방법 알아보기 [!DNL Adobe Experience Manager] 경험 조각 [!DNL Adobe Target] 활동.
title: 사용 방법 [!DNL Adobe Experience Manager] (AEM) 경험 구성요소?
feature: Experiences and Offers
exl-id: 3dd811a4-c7be-443d-a5ad-5b9adcaf1a2c
source-git-commit: b4c64f3fbc266b86cfffa6e5526a074b76b8b6ee
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 14%

---

# AEM 경험 구성요소

에서 만든 경험 조각 사용 [!DNL Adobe Experience Manager] (AEM)에서 [!DNL Target] 최적화 또는 개인화를 지원하기 위한 활동.

>[!NOTE]
>
>이 기능을 사용하려면 다음을 수행해야 합니다 [!DNL Adobe Experience Manager] (AEM) 고객. 자세한 내용은 [요구 사항](#section_AE6F0971E1574B3AA324003599B96E5A) 아래의 제품에서 사용할 수 있습니다.

에서 만들어진 경험 조각 사용 [!DNL AEM] in [!DNL Target] 활동을 통해 사용 편의성과 기능을 결합할 수 있습니다 [!DNL AEM] 의 강력한 AI(인공 지능) 및 ML(기계 학습) 기능 사용 [!DNL Target] 경험을 규모에 맞게 테스트 및 개인화합니다.

[!DNL AEM] 모든 콘텐츠 및 자산을 중앙 위치에 가져와서 개인화 전략을 실행합니다. [!DNL AEM] 코드를 작성하지 않고도 한 위치에서 데스크톱, 태블릿 및 모바일 장치의 콘텐츠를 쉽게 만들 수 있습니다. 모든 장치를 위해 페이지를 만들 필요가 없습니다. [!DNL AEM] 콘텐츠를 사용하여 각 경험을 자동으로 조정합니다.

[!DNL Target] 을 사용하면 행동, 컨텍스트 및 오프라인 변수를 통합하는 규칙 기반 기계 학습 접근 방식과 AI 기반 기계 학습 접근 방식을 조합하여 규모에 맞게 개인화된 경험을 제공할 수 있습니다. 사용 [!DNL Target], 쉽게 설정 및 실행할 수 있습니다. [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) 및 [다변량](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) 활동을 통해 최상의 오퍼, 콘텐츠 및 경험을 파악합니다.

경험 조각은 콘텐츠/경험 작성자 및 관리자를 을 사용하여 비즈니스 결과를 이끄는 최적화 및 개인화 전문가에게 연결하기 위한 매우 큰 단계를 나타냅니다 [!DNL Target].

## 요구 사항 {#section_AE6F0971E1574B3AA324003599B96E5A}

내에서 경험 조각 기능을 프로비저닝해야 합니다 [!DNL Target]. 또한 [!DNL AEM] 6.3(해당 서비스 팩 또는 [!DNL AEM] 6.4 이상 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* [!DNL Adobe Experience Manager] 6.5.
* [!DNL Adobe Experience Manager] 6.4.
* [!DNL Adobe Experience Manager] 6.3 SP2 이상
* [!DNL Adobe Target Standard] 또는 [!DNL Adobe Target Premium] 계정이 필요합니다.

연락처 [Adobe Target 고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 통합을 활성화하고 인증 세부 정보를 제공합니다.

## 에서 경험 조각 만들기 및 구성 [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

를 사용하려면 [!DNL AEM] 경험 조각 [!DNL Target]로 지정하는 경우 다음 단계를 수행해야 합니다.

### 1단계: 통합 [!DNL AEM] with [!DNL Target]

자세한 내용은 다음 문서를 참조하십시오.

* **Adobe I/O**: [Adobe I/0을 사용하여 Adobe Target과 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html) 에서 _관리 사용 안내서_ 설명서.
* **[!DNL AEM]6.3**: [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html) 에서 _Adobe Experience Manager 6.3_ 설명서.
* **[!DNL AEM]6.4**: [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html) 에서 _Adobe Experience Manager 6.4_ 설명서.
* **[!DNL AEM]6.5**: [Adobe Analytics 및 Adobe Target 선택](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=en) 에서 *Adobe Experience Manager 6.5* 설명서.

### 2단계: 경험 구성요소 만들기

경험 조각은에서 만들어집니다. [!DNL AEM]. 자세한 내용은 다음 문서를 참조하십시오.

* **[!DNL AEM]6.3**: [경험 조각](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html) 에서 *Adobe Experience Manager 6.3* 설명서.
* **[!DNL AEM]6.4**: [경험 조각](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=en) 에서 *Adobe Experience Manager 6.4* 설명서.
* **[!DNL AEM]6.5**: [경험 조각](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=en) 에서 *Adobe Experience Manager 6.5* 설명서.

### 3단계: 구성 [!DNL AEM] 경험 조각을 [!DNL Target]

1. 내 [!DNL AEM]를 클릭하고 원하는 경험 구성요소 또는 상위 폴더를 선택한 다음 를 클릭합니다 **[!UICONTROL 속성]**.
2. **[!UICONTROL 클라우드 서비스]** 탭을 클릭한 다음, **[!UICONTROL 클라우드 서비스 구성]** 드롭다운 목록에서 **[!UICONTROL Adobe Target]**&#x200B;을 선택합니다.

   >[!NOTE]
   >
   >이전 단계에서는 사용자 조직의 누군가가 [!DNL Adobe Target] 구성.

3. **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭합니다.

### 4단계: 경험 조각을 게시하여 [!DNL Target]

사용자 [!DNL AEM] 버전에 대한 단계별 지침은 다음 링크를 참조하십시오.

* **[!DNL AEM]6.3**: [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html) 에서 *Adobe Experience Manager 6.3* 설명서.
* **[!DNL AEM]6.4**: [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html) 에서 *Adobe Experience Manager 6.4* 설명서.
* **[!DNL AEM]6.5**: [Target으로 경험 조각 내보내기](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en) 에서 *Adobe Experience Manager 6.5* 설명서.

## 에서 경험 조각 사용 [!DNL Target] 활동 {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

이전 작업을 수행하면 경험 조각이 [!UICONTROL 오퍼] 페이지 [!DNL Target].

>[!NOTE]
>
>* [!DNL Target] 현재 는 10분마다 가져올 경험 구성요소를 찾습니다. 가져온 경험 조각은 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.
>
>* 경험 조각을 로 가져옵니다 [!DNL Target] HTML 오퍼로서 사용할 수 있습니다. 해당 경험 조각 &quot;기본&quot; 버전은 [!DNL AEM]. 에서 경험 조각을 편집할 수 없습니다 [!DNL Target].


마우스로 목록의 경험 구성요소를 가리킨 다음, [!UICONTROL 보기] 아이콘 ![보기 아이콘](assets/icon_info.png) 공개 오퍼 게재 URL 및 해당 오퍼를 포함하여 경험 조각에 대한 추가 정보를 보려면 [!DNL AEM] 경로.

에서 경험 조각을 사용할 수 있습니다. [!DNL Target] 를 사용하여 활동 [시각적 경험 작성기](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>를 완전히 사용하려면 [!DNL Target] AI 및 ML 기능을 선택하여 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) a/B 테스트를 만드는 동안 오류가 발생했습니다.

**VEC를 사용하여 경험 조각을 사용하려면**

1. in [!DNL Target]에서 경험을 만들거나 편집하는 동안 [시각적 경험 작성기](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)를 클릭하고, 삽입할 페이지의 위치를 클릭합니다. [!DNL AEM] 컨텐츠를 만든 다음 원하는 옵션을 선택하여 [!UICONTROL 경험 조각 선택] 목록.

   * [!UICONTROL 다음 항목 전에 삽입]
   * [!UICONTROL 다음 항목 뒤에 삽입]
   * [!UICONTROL 경험 구성요소로 교체]

   다음 [!UICONTROL 경험 조각] 목록에는 생성된 컨텐츠가 표시됩니다. [!DNL AEM] 이제 내에서 기본적으로 사용할 수 있습니다 [!DNL Target].

   >[!NOTE]
   >
   >[!UICONTROL 경험 구성요소로 교체] 선택 사항은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   ![](assets/experience_fragment_list.png)

1. 원하는 경험 조각을 선택하고 을 클릭합니다 **[!UICONTROL 완료]**.
1. 활동 구성을 완료합니다.

   다양한 활동 유형의 구성에 대한 자세한 내용은 다음 항목을 참조하십시오.

   * **A/B 테스트:** [A/B 테스트 만들기](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **자동 할당:** [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **자동 Target:** [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md)
   * **AP(자동화된 개인화):**[자동화된 개인화 활동 작성](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **경험 타깃팅(XT):** [경험 타깃팅 활동 만들기](/help/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **다변량 테스트(MVT):** [다변량 테스트 만들기](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **권장 사항:** [권장 사항 활동 만들기](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**양식 기반 경험 작성기를 사용하여 경험 조각을 사용하려면:**

1. in [!DNL Target]에서 경험을 만들거나 편집하는 동안 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)를 클릭하고, 삽입할 페이지에서 위치를 선택합니다. [!DNL AEM] 컨텐츠, **[!UICONTROL 경험 조각 변경]** 를 [!UICONTROL 경험 조각 선택] 목록.

   ![](assets/experience_fragment_list.png)

   다음 [!UICONTROL 경험 조각] 목록에는 생성된 컨텐츠가 표시됩니다. [!DNL AEM] 이제 내에서 기본적으로 사용할 수 있습니다 [!DNL Target].

1. 원하는 경험 조각을 선택하고 **[!UICONTROL 저장을 클릭합니다]**.
1. 활동 구성을 완료합니다.

## 고려 사항 {#considerations}

* [!DNL Target] 현재 는 10분마다 가져올 경험 구성요소를 찾습니다. 가져온 경험 조각은 [!DNL Target] 10분 안에, 이 기간은 앞으로 단축될 것입니다.
* 경험 조각을 로 가져옵니다 [!DNL Target] HTML 오퍼로서 사용할 수 있습니다. 경험 조각 &quot;기본&quot; 버전은 에 유지됩니다. [!DNL AEM]. 에서 경험 조각을 편집할 수 없습니다 [!DNL Target].
* 을 사용하여 경험 조각을 만들 수 없습니다 [!DNL Adobe I/O]. 위에서 설명한 대로 AEM을 사용하여 경험 조각을 만듭니다.

## 교육 비디오: AEM 경험 구성요소 사용 [!DNL Adobe Target]

다음 비디오에서는 경험 조각을 설정하고 사용하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>다음 [!DNL AEM] 4:54에 설명된 딥 링크 기능이 제거되었습니다.

자세한 내용은 [Adobe Target에서 경험 조각 사용](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) on *AEM Sites 비디오 및 Tutorials* 페이지.
