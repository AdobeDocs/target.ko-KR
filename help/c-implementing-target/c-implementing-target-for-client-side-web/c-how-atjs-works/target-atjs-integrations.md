---
keywords: at.js integration;supported integrations;unsupported integrations;third party integrations
description: Target과의 통합과 at.js 관련 지원 상태에 대한 정보입니다.
title: at.js 통합
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 91%

---


# at.js 통합{#at-js-integrations}

[!DNL Target]과의 통합과 at.js 관련 지원 상태에 대한 정보입니다.

여기에서 지원되지 않거나 언급되지 않은 통합에 대한 강력한 요구가 있는 경우에는 계정 담당자 또는 컨설턴트에게 문의하십시오.

## 지원되는 통합 {#section_3B44A970D3FB42D1973701452C868B55}

| 통합 | 세부 사항 |
|--- |--- |
| Analytics for Target (A4T) | [Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE)를 참조하십시오. |
| 프로필 및 대상(P&amp;A) | 핵심 [서비스 사용자](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) 안내서의 *대상을 참조하십시오*. |
| Experience Cloud ID 서비스 | [Adobe Experience Cloud ID 서비스 설명서](https://experienceleague.adobe.com/docs/id-service/using/home.html)를 참조하십시오. |
| Adobe Launch | Launch는 Adobe의 차세대 태그 관리 플랫폼이며 Adobe Target을 구현하는 데 권장되는 방법입니다. Launch는 관련 고객 환경을 향상하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.  [Adobe Launch를 사용하여 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25)을 참조하십시오. |
| DTM(다이내믹 태그 관리) | See the [Best Practices for Implementing Target Using Dynamic Tag Management guide](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html).   중요: [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25)는 Target 및 at.js 라이브러리를 구현하기 위해 선호되는 최신 방법입니다. 새로운 Target 구현의 경우, Launch를 사용하십시오. 다음은 DTM 구현을 사용하는 기존 클라이언트를 위한 가이드입니다.   DTM 통합을 사용할 때 다음 사항을 고려하십시오. <ul><li>라이브러리 관리: at.js를 사용하려면 &quot;사용자 지정&quot; 호스팅 옵션을 사용하십시오. &quot;자동&quot; 관리는 현재 지원되지 않습니다. </li></ul> |
| Adobe Experience Manager(AEM) 클라우드 서비스 | AEM 클라우드 서비스를 사용하면 AEM 작업 과정 내에서 A/B 테스트 및 경험 타깃팅 활동을 작성할 수 있습니다. FP-11577 이상의 Adobe Experience Manager 6.2로 at.js를 지원합니다. 자세한 정보는 [Adobe Target 통합](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html)을 참조하고 AEM 버전을 선택하십시오. |
| AEM 경험 구성요소 | Target 활동에 AEM에서 만든 경험 구성요소를 사용하면 AEM의 편의성과 기능을 Target의 강력한 AI(Automated Intelligence) 및 기계 학습(ML) 기능을 결합하여 경험을 다양한 규모로 테스트 및 개인화할 수 있습니다.  AEM에서는 모든 콘텐츠 및 자산을 중앙 위치에 가져와서 개인화 전략을 실행합니다. AEM을 사용하면 코드를 작성하지 않고도 한 위치에서 데스크톱, 태블릿 및 휴대 장치의 콘텐츠를 쉽게 만들 수 있습니다. 모든 장치를 위해 페이지를 만들 필요가 없이, 컨텐츠를 사용하여 각 경험이 자동으로 조정됩니다.  [AEM 경험 구성요소](/help/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8)를 참조하십시오. |

## 지원되지 않는 통합 {#section_8EFCAED418DC42E0B07F95924819EAC2}

| 통합 | 세부 사항 |
|--- |--- |
| [!DNL Legacy Target to SiteCatalyst Integration] | [!DNL SiteCatalyst] UI에서 보고를 수행할 수 있도록 페이지 호출을 통해 캠페인 및 레서피 ID를 [!DNL SiteCatalyst]에 전송하는 통합입니다. 이 기능은 A4T로 대체되었습니다. |
| [!DNL Legacy Target to SiteCatalyst Integration] | evar 및 prop를 기반으로 성공 지표와 사용자 프로필을 빌드할 수 있도록 `"SiteCatalyst: Event"` 및 `"SiteCatalyst: Purchase"`라는 mbox 호출을 수행하는 통합입니다. 이 기능은 A4T 및 P&amp;A로 대체되었습니다. |
| [!DNL Legacy Audience Manager (AAM) to Target Integration] | 프런트엔드 API 호출을 수행하여 AAM 세그먼트를 검색한 다음, 이 세그먼트들을 페이지의 모든 mbox 호출에서 mbox 매개 변수로서 전송하는 통합입니다. |

## 타사 통합 {#section_EE599839CCAD49DD97640E5EDAD9082E}

| 통합 | 세부 사항 |
|--- |--- |
| 기타 태그 관리자 | at.js는 비Adobe 태그 관리 플랫폼에서 작동해야 하지만 다른 공급업체가 개발한 사용자 지정 통합 기능을 사용하는 데에는 주의하십시오. 더 이상 at.js에 없는 내부 mbox.js 함수에 공급업체의 통합이 종속될 수 있습니다. |
| 타사 데이터 제공자(예: Demandbase, Bluekai, 날씨 API) | Target의 사용자 프로파일링을 보완하는 데 사용되는 다양한 타사 데이터 공급업체는 at.js [데이터 제공자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) 기능을 사용하여 통합할 수 있습니다. |