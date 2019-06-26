---
description: 최적화 또는 개인화를 지원하기 위해 Target 활동의 AEM(Adobe Experience Manager)에서 작성된 경험 구성요소 사용에 관해 설명합니다.
keywords: 경험;aem;adobe experience manager;adobe target에 내보내기;경험 구성요소;구성요소;XF
seo-description: 최적화 또는 개인화를 지원하기 위해 Target 활동의 AEM(Adobe Experience Manager)에서 작성된 경험 구성요소 사용에 관해 설명합니다.
seo-title: AEM 경험 구성요소
solution: Target
title: AEM 경험 구성요소
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# AEM 경험 구성요소{#aem-experience-fragments}

최적화 또는 개인화를 지원하기 위해 Target 활동의 AEM(Adobe Experience Manager)에서 작성된 경험 구성요소 사용에 관해 설명합니다.

## AEM 경험 구성요소{#topic_1E1E4EA01F074349B2CF8785387B5FE8}를 참조하십시오 

최적화 또는 개인화를 지원하기 위해 Target 활동의 AEM(Adobe Experience Manager)에서 작성된 경험 구성요소 사용에 관해 설명합니다.

>[!NOTE]
>
>AEM(Adobe Experience Manager) 고객만 이 기능을 사용할 수 있습니다. 자세한 내용은 아래의 [요구 사항](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A)을 참조하십시오.

## 개요 {#section_95A91830530F493B81C5C9CDB9B783EA}

Target 활동에 AEM에서 만든 경험 조각을 사용하면 AEM의 편의성과 기능을 Target의 강력한 AI(Automated Intelligence) 및 기계 학습(ML) 기능을 결합하여 경험을 다양한 규모로 테스트 및 개인화할 수 있습니다.

AEM에서는 모든 컨텐츠 및 자산을 중앙 위치에 가져와서 개인화 전략을 실행합니다. AEM을 사용하면 코드를 작성하지 않고도 한 위치에서 데스크톱, 태블릿 및 휴대 장치의 컨텐츠를 쉽게 만들 수 있습니다. 모든 장치를 위해 페이지를 만들 필요가 없이, 컨텐츠를 사용하여 각 경험이 자동으로 조정됩니다.

Target을 사용하면 행동 변수, 컨텍스트 변수 및 오프라인 변수를 통합하는 규칙 기반 및 AI 중심 기계 학습 접근 방식들의 결합을 기반으로 다양한 규모의 개인화된 경험을 제공할 수 있습니다.  Target을 사용하면 A/B와 MVT(다변량) 활동을 쉽게 설정 및 실행하여 최상의 오퍼, 컨텐츠 및 경험을 결정할 수 있습니다.

경험 조각은 컨텐츠/경험 작성자 및 관리자를 Target을 사용하여 비즈니스 결과를 이끄는 최적화 및 개인화 전문가에게 연결하기 위한 매우 큰 단계를 나타냅니다.

## 요구 사항 {#section_AE6F0971E1574B3AA324003599B96E5A}

Target 내의 경험 구성요소 기능을 공급받아야 합니다. 또한 해당하는 AEM 6.3 서비스 팩 또는 AEM 6.4 이상을 사용 중이어야 합니다. 계정 담당자는 사용자가 이 기능을 사용하기 위한 요구 사항을 충족하는지 확인할 수 있습니다.

* Adobe Experience Manager 6.4 이상
* Adobe Experience Manager 6.3 SP2 이상
* Adobe Target Standard 또는 Adobe Target Premium 계정
* Adobe Target 고객 지원에 연락하여 통합을 활성화하고 인증 세부 사항을 제공받으십시오.

## AEM에서 경험 조각 만들기 및 구성 {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Target에서 AEM 경험 구성요소를 사용하려면 다음 절차를 수행해야 합니다.

### 1단계: AEM을 Target과 통합

자세한 내용은 다음 문서를 참조하십시오.

* **AEM 6.3:**[Adobe Experience Manager 6.3](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) 설명서에서 _Adobe Analytics 및 Adobe Target 선택_
* **AEM 6.4:**[Adobe Experience Manager 6.4](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) 설명서에서 _Adobe Analytics 및 Adobe Target 선택_

### 2단계: 경험 구성요소 만들기

경험 조각은 AEM에서 만들어집니다. 자세한 내용은 다음 문서를 참조하십시오.

* **AEM 6.3:** [Adobe Experience Manager 6.3](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) 설명서의 *경험 구성요소*
* **AEM 6.4:**[Adobe Experience Manager 6.4](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) 설명서의 *경험 구성요소*

### 3단계: 경험 구성요소를 Target과 공유하도록 AEM 구성

1. AEM 내에서 원하는 경험 구성요소 또는 상위 폴더를 선택한 다음 [!UICONTROL 속성]을 클릭합니다.
2. [!UICONTROL 클라우드 서비스] 탭을 클릭한 다음, [!UICONTROL 클라우드 서비스 구성] 드롭다운 목록에서 [!UICONTROL Adobe Target]을 선택합니다.

   >[!NOTE]
   >
   >이전 단계에서는 사용자 조직의 누군가가 Adobe Target 구성을 작성했다고 가정합니다.

3. [!UICONTROL 저장 및 닫기]를 클릭합니다.

### 4단계: 경험 구성요소를 게시하고 Target으로 내보내기

**AEM 6.3:**

1. AEM 내에서 원하는 경험 조각을 선택하고 [!UICONTROL 게시] 탭을 클릭한 다음, [!UICONTROL 게시] 단추를 클릭합니다.
2. AEM 내에서 원하는 경험 조각을 선택하고, [!UICONTROL Adobe Target으로 내보내기]를 클릭한 다음, [!UICONTROL 확인]을 클릭합니다.

   ![](assets/experience_fragment_export_to_target.png)

**AEM 6.4:**

1. AEM 내에서 원하는 경험 구성요소를 선택하고 [!UICONTROL Adobe Target으로 내보내기]를 클릭합니다.

   ![](assets/experience_fragment_export_to_target.png)

2. 표시되는 대화 상자에서 [!UICONTROL 게시]를 선택하여 경험 구성요소 내에 있는 모든 자산을 [!DNL Target]에 게시합니다.

## Using Experience Fragments in Target Activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

앞의 작업을 수행하면 경험 조각이 Target의 [!UICONTROL 오퍼] 페이지에 표시됩니다.

>[!NOTE]
>
>Target은 현재 10분마다 가져올 경험 구성요소를 찾습니다. 가져온 경험 구성요소는 10분 이내에 Target에서 사용할 수 있습니다. 이 시간은 향후 단축될 것입니다.

>[!IMPORTANT]
>
>경험 구성요소는 현재 HTML 오퍼로 Target에 가져왔습니다. 경험 조각 &quot;마스터&quot; 버전은 AEM에 남습니다. 이 경험 조각을 Target에서 편집할 수는 없습니다.

마우스로 목록의 경험 구성요소를 가리킨 다음, 보기 아이콘(![](assets/icon_info.png)

)을 클릭하여 공개 오퍼 게재 URL, 해당 AEM 경로 및 AEM 내부의 경험 구성요소를 여는 딥링크를 포함한 경험 구성요소에 대한 추가 정보를 볼 수 있습니다.

VEC(시각적 경험 작성기) 또는 양식 기반 경험 작성기를 사용하여 Target 활동에서 경험 조각을 사용할 수 있습니다.

>[!NOTE]
>
>Target의 AI 및 ML 기능을 완전히 활용하려면 A/B 테스트를 작성하는 동안 [자동 할당](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 또는 [자동화된 개인화](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)를 선택하면 됩니다.

**VEC를 사용하여 경험 조각을 소비하려면 다음을 수행하십시오.**

1. Target의 [시각적 경험 작성기](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)에서 경험을 만들거나 편집할 때 AEM 컨텐츠를 삽입하려는 페이지에서 해당 위치를 클릭한 다음, **[!UICONTROL 경험 조각으로 교체]** 를 선택하여 [!UICONTROL 경험 조각 선택] 목록을 표시합니다.

   >[!NOTE]
   >
   >[!UICONTROL 경험 구성요소로 교체] 선택 사항은 이미지에 사용할 수 없습니다. 이미지에 이 선택 사항을 사용하려면 원하는 이미지가 들어 있는 컨테이너 요소를 클릭하십시오.

   [!UICONTROL 경험 조각] 목록에는 이제 Target 내에서 기본적으로 사용할 수 있는 AEM에서 만들어진 모든 컨텐츠가 표시됩니다.

   ![](assets/experience_fragment_list.png)

1. 원하는 경험 조각을 선택하고 **[!UICONTROL 저장을 클릭합니다]**.
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

1. Target의 [양식 기반 경험 작성기](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)에서 경험을 만들거나 편집할 때 AEM 컨텐츠를 삽입하려는 페이지에서 해당 위치를 선택한 다음, **[!UICONTROL 경험 조각 변경]** 을 선택하여 [!UICONTROL 경험 조각 선택] 목록을 표시합니다.

   ![](assets/experience_fragment_list.png)

   [!UICONTROL 경험 조각] 목록에는 이제 Target 내에서 기본적으로 사용할 수 있는 AEM에서 만들어진 모든 컨텐츠가 표시됩니다.

1. 원하는 경험 조각을 선택하고 **[!UICONTROL 저장을 클릭합니다]**.
1. 활동 구성을 완료합니다.

## 교육 비디오: Adobe Target에서 AEM 경험 구성요소 사용 {#section_C0EDC54063464F41A182492D2045BC64}

[Adobe Target에서 AEM 경험 구성요소 사용](https://helpx.adobe.com/experience-manager/kt/sites/using/experience-fragment-target-feature-video-use.html) 비디오는 경험 구성요소를 설정하고 사용하는 방법을 보여 줍니다.
