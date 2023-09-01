---
keywords: cja4t;고객 여정 분석;target용 고객 여정 분석;고객 여정 분석 보고 소스;target용 보고 소스로서의 고객 여정 분석
description: ' [!DNL Adobe Customer Journey Analytics] for [!DNL Target] (A4T)을 사용하여 [!DNL Customer Journey Analytics] 전환 지표 및 대상자 세그먼트를 기반으로 하는 활동을 생성하고 [!DNL Customer Journey Analytics] 보고서를 사용하여 결과를 검사할 수 있습니다.'
title: 이란? [!DNL Adobe Customer Journey Analytics] 대상 [!DNL Target] (CJA4T)?
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 13c899b656d9f15e7368d981ac25540c46caccb2
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 12%

---

# [!DNL Adobe Customer Journey Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Adobe Target] (CJA4T)

다음 [!DNL Customer Journey Analytics for Target] (CJA4T) 통합 [Adobe Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html){target=_blank} 및 [!DNL Target] 은 최적화 프로그램에 강력한 분석 및 시간 절약 도구를 제공합니다.

를 사용할 때의 주요 이점 [!DNL Customer Journey Analytics] 데이터 입력 [!DNL Target] 은(는)

* 마케터는 를 동적으로 적용할 수 있습니다 [!DNL Customer Journey Analytics] 성공 지표 [!DNL Target] 언제든지 활동 보고서를 작성할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 단일 데이터 소스는 두 개의 별도 시스템에서 데이터를 수집할 때 발생하는 분산을 최소화합니다.

## 고려 사항

CJA4T 통합을 사용하기 전에 다음 정보를 고려하십시오.

* [!DNL Target]용 보고 소스로서의 [!DNL Customer Journey Analytics]를 사용하려면 귀하 및 귀사 모두 [!DNL Customer Journey Analytics] 및 [!DNL Target]에 대한 액세스 권한을 보유해야 합니다. 두 솔루션 중 하나에 액세스해야 하는 경우 조직의 관리자 또는 계정 담당자에게 문의하십시오.
* 만들려면 [!DNL Target] 활동(포함) [!DNL Customer Journey Analytics] 보고 시 &quot;[!UICONTROL 승인자]&quot; 또는 &#39;[!UICONTROL 편집자]의 &quot;역할 [!DNL Target].
   * 다음 항목이 있는 경우: [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) account, 참조 [역할 및 권한 지정](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) 위치: *사용자*.
   * 다음 항목이 있는 경우: [Target Premium](/help/main/c-intro/intro.md#premium) account, 참조 [역할 및 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) 위치: *Enterprise 사용자 권한*.

* 설정에 따라 보고는 활동별로 또는 조직 수준에서 변경될 수 있습니다. 다음을 참조하십시오 [Reporting Cloud 솔루션](/help/main/administrating-target/reporting.md#solution) 위치: *Target에서 보고 구성*.
* 하나의 보고 소스 또는 다른 보고 소스를 사용하십시오. 단일 활동에 대한 데이터를 여러 보고 소스로 수집할 수 없습니다.
* 설정 시 [!DNL Customer Journey Analytics] 보고 소스로 보고할 샌드박스를 지정하라는 메시지가 표시됩니다. 구성하는 동안 액세스 권한이 있는 샌드박스만 표시됩니다.
* 모든 기존 항목 [!DNL Target] 활동은 계속 사용합니다. [!DNL Target] 데이터 수집이며 CJA4T 활성화의 영향을 받지 않습니다.
* CJA4T는 다음과 같은 경우에만 사용할 수 있습니다. [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. 지원 [!DNL Analytics Data Connector] 은(는) 미래를 위해 계획됩니다.
* 타이밍에 대한 질문이 있으면 다음을 참조하십시오. [지연 고려 사항](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#latency){target=_blank} 위치: *자주 묻는 질문* 다음에서 *Adobe Customer Analytics 안내서*.

## 지원되는 활동 유형 {#supported-activities}

을 사용할 때 지원되는 활동 유형은 다음과 같습니다. [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} or the [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} JavaScript 라이브러리:

| 활동 유형 | CJA4T 호환 여부 |
|--- |--- |
| [수동 트래픽 분할을 사용하는 A/B 활동](/help/main/c-activities/t-test-ab/test-ab.md) | 예 |
| [자동 할당을 사용하는 A/B 활동](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니요 |
| [자동 타겟을 사용하는 A/B 활동](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 아니요 |
| [경험 타겟팅(XT)](/help/main/c-activities/t-experience-target/experience-target.md) | 예 |
| [다변량 테스트(MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | 예 |
| [자동화된 개인화(AP) 활동](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | 아니요 |
| [권장 사항 활동](/help/main/c-recommendations/recommendations.md) | 예 |

## 다음을 사용하는 활동 만들기 [!DNL Customer Journey Analytics] 보고 소스로 사용

만들기 [!DNL Target] 을 사용하는 활동 [!DNL Customer Journey Analytics] 보고 소스는 일반 설정 과 유사합니다 [!DNL Target] 활동.

1. 다음에서 **[!UICONTROL 활동]** 목록, 클릭 **[!UICONTROL 활동 만들기]**&#x200B;에 따라 활동 유형을 선택합니다. [위의 지원되는 활동 차트](#supported-activities))을 클릭하여 활동 설정을 시작합니다.
1. 에 도착하면 **[!UICONTROL 목표 및 설정]** 세 부분으로 구성된 활동 만들기 워크플로의 페이지에서 **[!DNL Customer Journey Analytics]** 를 보고 소스로 사용합니다.

   ![보고 소스로 Customer Journey Analytics 옵션](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >보고 소스는 다음 날짜 이후에 변경할 수 없습니다. [!DNL Target] 활동이 실행됩니다.

1. 샌드박스 선택.

   이 드롭다운 목록에는 액세스할 수 있는 샌드박스만 표시됩니다. 액세스 권한이 있는 샌드박스 중 하나 이상이 목록에서 누락된 경우 샌드박스에 액세스할 수 있는지 확인하십시오. 연락처 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 계속 문제가 발생하는 경우

   ![샌드박스 옵션 선택](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택합니다. 다음 중 하나를 선택할 수 있습니다. [!DNL Target] 전환 지표 또는 사용 [!DNL Customer Journey Analytics] 지표.

   ![목표 지표에서 Customer Journey Analytics 지표 옵션 사용](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭합니다.

## 설정 [!DNL Customer Journey Analytics] 연결

다음 이후 [!DNL Target] 활동이 생성되었습니다. 다음 위치에 연결을 만들어야 합니다. [!DNL Customer Journey Analytics]. 이미 연결을 설정한 경우 기존 연결을 사용하고 아래 4단계로 건너뛸 수 있습니다. 연결이 허용함 [!DNL Customer Journey Analytics] 보고를 위해 데이터 세트에서 데이터를 가져오기 시작합니다.

1. 위치 [!DNL Customer Journey Analytics], **[!UICONTROL 연결]** 페이지, 클릭 **[!UICONTROL 새 연결 만들기]**.

   ![Customer Journey Analytics에서 새 연결 링크 만들기](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. 구성 [연결 및 데이터 설정](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html){target=_blank} 올바른 정보를 제공합니다.
1. 데이터 스트림을 구성할 때 사용한 이벤트 데이터 세트를 추가합니다.
1. 추가 **[!UICONTROL Adobe Target 분류 이벤트]** 데이터 세트를 조회한 다음 **[!UICONTROL 다음]**.

   ![Customer Journey Analytics의 데이터 세트 추가 대화 상자](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. 이벤트 데이터 세트를 구성합니다.

   자세한 내용은 [데이터 세트 추가 및 구성](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#add-dataset){target=_blank} 위치: *연결 만들기* 다음에서 *Adobe Customer Journey Analytics 안내서*.

1. 를 사용하여 조회 데이터 세트 구성 [!UICONTROL 키] 필드를 &quot;key&quot;로 사용하고 일치하는 키 필드를 다음 경로와 함께 사용합니다.

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Customer Journey Analytics의 Adobe Target 분류 이벤트 대화 상자](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. 클릭 **[!UICONTROL 데이터 세트 추가]**&#x200B;을 클릭한 다음 을 클릭합니다 **[!UICONTROL 저장]** 다음 화면에서 연결을 완료합니다.

## 데이터 보기 설정

에서 데이터 보기 설정 [!DNL Customer Journey Analytics]. 데이터 보기는 연결의 데이터를 올바르게 사용할 수 있도록 해줍니다.

1. 데이터 보기를 설정하고 위에서 만든 연결을 가리켜야 합니다.

   자세한 내용은 [데이터 보기 만들기 또는 편집](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target=_blank} 다음에서 *Adobe Customer Journey Analytics 안내서*.

1. 을(를) 올바르게 보려면 [!DNL Target] 데이터 입력 [!DNL Customer Journey Analytics], 조회 데이터 세트에서 다음 필드를 차원으로 추가해야 합니다.

   * 경험 이름
   * 경험 ID
   * 활동 이름
   * 활동 ID

   ![Customer Journey Analytics의 이름 및 ID 옵션](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. 다른 필드 설정을 완료한 다음 **[!UICONTROL 저장 및 계속]** 완료 시.
