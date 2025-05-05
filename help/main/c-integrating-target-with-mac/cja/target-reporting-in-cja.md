---
keywords: 고객 여정 분석;target용 고객 여정 분석;고객 여정 분석 보고 소스;target용 보고 소스로서의 고객 여정 분석;cja의 target 보고;Customer Journey Analytics의 target 보고
description: ' [!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics] 를 사용하여 [!DNL Customer Journey Analytics] 전환 지표 및 대상 세그먼트를 기반으로 하는 활동을 만들고 [!DNL Customer Journey Analytics] 보고서를 사용하여 결과를 검사하십시오.'
title: ' [!DNL Adobe Customer Journey Analytics]에서  [!DNL Target] 보고 중'
feature: Integrations
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 52f11998149cddeb4245a0f07280562d79332a04
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 54%

---

# [!DNL Adobe Customer Journey Analytics]의 [!DNL Target] 보고

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank}과(와) [!DNL Target] 간의 통합은 최적화 프로그램에 강력한 분석과 시간 절약에 유용한 도구를 제공합니다.

[!DNL Customer Journey Analytics]를 [!DNL Target]에 대한 보고 소스로 사용하는 경우의 주요 이점은 다음과 같습니다.

* 마케터가 언제든지 [!DNL Customer Journey Analytics] 성공 지표 또는 보고 세그먼트를 [!DNL Target] 활동 보고서에 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 마케터는 [실험 패널](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}과 같은 [!DNL Customer Journey Analytics] 기능을 사용하여 웹 사이트 개인화를 추가로 분석할 수 있습니다.
* 마케터는 [!DNL Adobe Journey Optimizer] 및 [!DNL Target]에 대한 단일 보고 소스를 가질 수 있습니다. 두 개인화 제품 모두 [!DNL Customer Journey Analytics]에 연결하여 웹 개인화를 보다 전체적으로 살펴볼 수 있습니다.

## 고려 사항

[!DNL Customer Journey Analytics] 및 [!DNL Target] 통합을 사용하기 전에 다음 정보를 고려하십시오.

>[!IMPORTANT]
>
>이 통합은 [[!UICONTROL Adobe Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)과(와) 다릅니다. 구현 및 지원되는 활동 유형이 다릅니다. [!DNL Target] 활동에 이 통합을 사용하기 전에 이 문서를 완전히 읽어야 합니다.

* [!DNL Target]용 보고 소스로서의 [!DNL Customer Journey Analytics]를 사용하려면 귀하 및 귀사 모두 [!DNL Customer Journey Analytics] 및 [!DNL Target]에 대한 액세스 권한을 보유해야 합니다. 솔루션에 액세스해야 하는 경우 조직의 관리자 또는 계정 담당자에게 문의하십시오.
* [!DNL Customer Journey Analytics] 보고를 사용하여 [!DNL Target] 활동을 만들려면 [!DNL Target]에 &quot;[!UICONTROL Approver]&quot; 또는 &#39;[!UICONTROL Editor]&quot; 역할이 있어야 합니다.
   * [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) 계정이 있는 경우 *사용자*&#x200B;에서 [역할 및 권한 지정](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions)을 참조하십시오.
   * [Target Premium](/help/main/c-intro/intro.md#premium) 계정이 있는 경우 *Enterprise 사용자 권한*&#x200B;에서 [역할 및 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions)을 참조하십시오.

* 보고 소스로서 [!DNL Customer Journey Analytics]를 사용하는 [!DNL Target] 활동을 설정하는 [!DNL Adobe Experience Platform] 역할의 일부여야 합니다. 자세한 내용은 [*데이터 설계자 및 엔지니어 튜토리얼의*&#x200B;권한 구성&#x200B;*에서  [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions#add-a-role-in-adobe-experience-platform-requires-a-system-administrator-or-product-admin){target=_blank}의 역할 추가*&#x200B;를 참조하십시오.
* 설정에 따라 활동별로 또는 조직 수준에서 보고가 변경될 수 있습니다. *Target의 보고 구성*&#x200B;에서 [Cloud 솔루션 보고](/help/main/administrating-target/reporting.md#solution)를 참조하십시오.
* 하나의 보고 소스 또는 다른 보고 소스를 사용하십시오. 여러 보고 소스에서 한 활동에 대한 데이터를 수집할 수 없습니다.
* [!DNL Customer Journey Analytics]를 보고 소스로 설정하면 보고용 샌드박스를 지정하라는 메시지가 표시됩니다. 구성 중에는 액세스 권한이 있는 샌드박스만 표시됩니다.
* 기존의 모든 [!DNL Target] 활동은 [!DNL Target] 데이터 수집을 계속 사용하며 이 통합을 활성화해도 영향을 받지 않습니다.
* 이 통합을 사용하려면 기본 구현 메서드에 [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/experience-platform){target=_blank} 및 [!DNL Target]이(가) [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}을(를) 통해 구현되었습니다.

  현재 [!DNL Adobe Experience Platform Web SDK]이(가) 구현되지 않은 경우 [[!DNL Adobe Analytics] 소스 연결](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics)을 만들어 데이터를 [!DNL Adobe Experience Platform]&#x200B;(으)로 가져올 수도 있습니다. 이 메서드를 사용하려면 [!DNL Customer Journey Analytics]에서 사용하는 [!DNL Adobe Experience Platform] 샌드박스와 함께 [!DNL Analytics] 보고서 세트를 선택해야 합니다.

  ![보고 설정 대화 상자의 샌드박스 옵션](/help/main/c-integrating-target-with-mac/cja/assets/aep-sandbox.png)

  >[!NOTE]
  >
  >[!DNL Adobe Analytics] 원본 연결을 사용하는 경우 [!DNL Adobe Analytics]과(와) [!DNL Customer Journey Analytics]에 모두 보고서가 있습니다. 그러나 이 두 가지 솔루션 간에 알고리즘이 다르기 때문에 결과는 일치하지 않을 수 있습니다.

* 시간에 대한 질문이 있는 경우 *[!DNL Adobe Customer Analytics]안내서*&#x200B;의 *자주 묻는 질문*&#x200B;에서 [지연 고려 사항](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-faq#latency){target=_blank}을 참조하십시오.

## 지원되는 활동 유형 {#supported-activities}

다음 활동 유형은 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} 또는 [at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/overview){target=_blank} JavaScript 라이브러리를 사용할 때 지원됩니다.

| 활동 유형 | 지원됨? |
|--- |--- |
| [수동 트래픽 분할을 사용하는 A/B 활동](/help/main/c-activities/t-test-ab/test-ab.md) | 예 |
| [자동 할당을 사용하는 A/B 활동](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니요 |
| [자동 타겟팅을 사용하는 A/B 활동](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 아니요 |
| [경험 타겟팅(XT)](/help/main/c-activities/t-experience-target/experience-target.md) | 예 |
| [다변량 테스트(MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | 예 |
| [Automated Personalization(AP) 활동](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | 아니요 |
| [추천 활동](/help/main/c-recommendations/recommendations.md) | 예 |

## [!DNL Customer Journey Analytics]를 보고 소스로 사용하는 활동 만들기

[!DNL Customer Journey Analytics]를 보고 소스로 사용하는 [!DNL Target] 활동을 만드는 것은 일반 [!DNL Target] 활동을 설정하는 것과 유사합니다.

>[!TIP]
>
>[!DNL Target]이(가) 계정에서 만든 모든 활동에 대해 [!DNL Customer Journey Analytics]에서 보고를 사용하도록 지정할 수도 있습니다(**[!UICONTROL Administration]** > **[!UICONTROL Reporting]** > **[!UICONTROL Reporting Experience Cloud Solution]**). 자세한 내용은 [보고 구성 [!DNL Target]](/help/main/administrating-target/reporting.md#solution)에서 *Reporting Cloud 솔루션*&#x200B;을 참조하십시오.

1. **[!UICONTROL Activities]** 목록에서 **[!UICONTROL Create Activity]**&#x200B;을(를) 클릭한 다음 활동 유형(위의 [지원되는 활동 차트](#supported-activities)에 따라)을 선택하고 활동 설정을 시작합니다.
1. 세 부분으로 구성된 활동 만들기 워크플로의 **[!UICONTROL Goals & Settings]** 페이지로 이동하면 **[!DNL Customer Journey Analytics]**&#x200B;을(를) 보고 소스로 선택합니다.

   ![Customer Journey Analytics를 보고 소스로 사용하는 옵션](/help/main/c-integrating-target-with-mac/cja/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >[!DNL Target] 활동이 라이브로 전환된 후에는 보고 소스를 변경할 수 없습니다.

1. 샌드박스를 선택합니다.

   이 드롭다운 목록에는 액세스할 수 있는 샌드박스만 표시됩니다. 액세스 권한이 있는 샌드박스 중 하나 이상이 목록에서 누락된 경우 해당 샌드박스에 액세스할 수 있는지 확인하십시오. 문제가 지속되면 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

   ![샌드박스 옵션 선택](/help/main/c-integrating-target-with-mac/cja/assets/sandbox.png)

1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택합니다. [!DNL Target] 전환 지표 중 하나를 선택하거나 [!DNL Customer Journey Analytics] 지표를 사용할 수 있습니다.

   ![목표 지표에서 Customer Journey Analytics 지표 옵션 사용](/help/main/c-integrating-target-with-mac/cja/assets/goal-metric.png)

1. **[!UICONTROL Save & Close]** 아이콘을 클릭합니다.

## [!DNL Customer Journey Analytics] 연결 설정

[!DNL Target] 활동이 생성되면 [!DNL Customer Journey Analytics]에서 연결을 만들어야 합니다. 이미 연결이 있는 경우 기존 연결을 사용하여 아래 4단계로 건너뛸 수 있습니다. 해당 연결을 통해 [!DNL Customer Journey Analytics]가 보고를 위해 데이터 세트에서 데이터 가져오기를 시작할 수 있습니다.

1. [!DNL Customer Journey Analytics]의 **[!UICONTROL Connections]** 페이지에서 **[!UICONTROL Create a new connection]**&#x200B;을(를) 클릭합니다.

   [!DNL Customer Journey Analytics]![&#128279;](/help/main/c-integrating-target-with-mac/cja/assets/create-connection.png)에서 새 연결 링크 만들기

1. 올바른 정보를 사용하여 [연결 및 데이터 설정](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/overview){target=_blank}을 구성하십시오.
1. 데이터스트림을 구성할 때 사용한 이벤트 데이터 세트를 추가합니다.
1. **[!UICONTROL Adobe Target Classification Events]** 조회 데이터 세트를 추가한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

   ![Customer Journey Analytics의 데이터 세트 추가 대화 상자](/help/main/c-integrating-target-with-mac/cja/assets/add-datasets.png)

1. 이벤트 데이터 세트를 구성하십시오.

   자세한 내용은 *[!DNL Adobe Customer Journey Analytics]안내서*&#x200B;의 *연결 만들기*&#x200B;에서 [데이터 세트 추가 및 구성](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection#add-dataset){target=_blank}을 참조하십시오.

1. [!UICONTROL Key] 필드를 &quot;key&quot;로 사용하고 [!UICONTROL Matching] 키 필드를 다음 경로로 사용하여 조회 데이터 세트를 구성합니다.

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Customer Journey Analytics의 Adobe Target 분류 이벤트 대화 상자](/help/main/c-integrating-target-with-mac/cja/assets/classifications-events.png)

1. **[!UICONTROL Add datasets]**&#x200B;을(를) 클릭한 다음, 다음 화면에서 **[!UICONTROL Save]**&#x200B;을(를) 클릭하여 연결을 완료합니다.

## 데이터 보기 설정

[!DNL Customer Journey Analytics]에서 데이터 보기를 설정합니다. 데이터 보기는 연결의 데이터가 올바르게 사용될 수 있는지 보장합니다.

1. 데이터 보기를 설정하고 위에서 만든 연결을 가리키는지 확인합니다.

   자세한 내용은 *[!DNL Adobe Customer Journey Analytics]안내서*&#x200B;에서 [데이터 보기 만들기 또는 편집](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target=_blank}을(를) 참조하십시오.

1. [!DNL Customer Journey Analytics]에서 [!DNL Target] 데이터를 제대로 보려면 조회 데이터 세트에서 다음 필드를 차원으로 추가해야 합니다.

   * [!UICONTROL Experience Name]
   * [!UICONTROL Experience ID]
   * [!UICONTROL Activity Name]
   * [!UICONTROL Activity ID]

   ![Customer Journey Analytics의 이름 및 ID 옵션](/help/main/c-integrating-target-with-mac/cja/assets/names-and-ids.png){width="600" zoomable="yes"}

1. [!UICONTROL Experimentation] 패널에서 [!DNL Target] 차원을 사용하려면 다음 컨텍스트 레이블을 설정하십시오.

   * [!UICONTROL Activity Name]의 경우 &quot;실험&quot;을 사용하십시오.
   * [!UICONTROL Experience Name], &quot;실험 변형&quot;을 사용하십시오.

   ![실험 패널의 컨텍스트 레이블](/help/main/c-integrating-target-with-mac/cja/assets/context-labels.png){width="600" zoomable="yes"}

1. 다른 필드 설정을 완료한 다음, 완료되면 **[!UICONTROL Save and continue]**&#x200B;을(를) 클릭합니다.
