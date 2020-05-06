---
keywords: troubleshooting;metric discrepancies;FAQ;reports
description: Adobe Target의 보고에 대한 FAQ 목록입니다.
title: Adobe Target에 대한 FAQ 보고
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: 7b57ef37f2764f5ec58c9a090edc295e81fdaaa9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 50%

---


# 보고 FAQ{#reporting-faq}

[!DNL Target]의 보고에 대한 FAQ 목록

## [!UICONTROL 경험 타깃팅](XT) 보고서에 제어 경험에 대한 지표가 포함되는 이유는 무엇입니까?

XT 활동에는 항상 제어 경험이 있어야 합니다. 매우 일반적인 시나리오인 [!UICONTROL A/B 테스트] 활동과 유사한 방식으로 XT 활동을 사용하는 경우 제어 경험 데이터가 유용합니다. 보고서에서 유용하지 않은 경우 제어 경험 데이터를 무시할 수 있습니다.

## 다른 [!DNL Target] 솔루션보다 [!DNL Adobe Experience Cloud]에서 방문 횟수가 더 적은 이유는 무엇입니까? {#section_7E626FDB417E41B8B58BBF30FB207409}

예를 들어 [!DNL Target]에 의해 보고된 방문 횟수와 같은 지표 수치는 다음과 같은 여러 가지 이유로 다른 [!DNL Experience Cloud] 솔루션에서 보고된 수치보다 항상 낮습니다.

* [!DNL Target]은 활동에 대해 자격이 되는 방문자에 대해서만 방문을 카운트하고, 다른 솔루션에서는 방문자를 페이지로 유도한 활동과 관계없이 페이지를 표시하는 방문자에 대한 방문을 카운트합니다.
* 서로 다른 활동이 한 곳에서 경합하는(함께 수행할 수 없는) 상황이 있을 수 있습니다. 그 결과, 방문자는 웹 페이지에 있는 [!DNL Target]에서 보고하는 지표 수치에 영향을 주는 다른 컨텐츠를 보게 됩니다.

## 내 활동의 보고서에 사용할 수 있는 데이터가 없는 이유는 무엇입니까? {#section_E4722F6445884130951DF79981C8289B}

활동의 콘텐츠가 사용자에게 전달되었지만 해당 보고서에 데이터가 들어 있지 않은 경우 보고서의 설정에 올바른 환경([호스트 그룹](/help/administrating-target/hosts.md))이 선택되어 있는지 확인하십시오.

개발 환경을 선택한 경우 &quot;선택한 보고서 설정에 사용 가능한 데이터가 없습니다&quot;라는 오류 메시지가 표시될 수 있습니다.

활동의 보고서에 대한 환경을 변경하려면 다음을 수행하십시오.

1. **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 원하는 활동을 클릭한 다음, **[!UICONTROL 보고서 탭을 클릭합니다.]**
1. 톱니바퀴 아이콘을 클릭하여 보고서 설정을 구성합니다.

   ![A/B 설정 대화 상자](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >톱니바퀴 아이콘은 [!UICONTROL 자동화된 개인화](AP) 보고서에 사용할 수 없습니다.

1. **[!UICONTROL 환경]** 드롭다운 목록에서 **[!UICONTROL 프로덕션]**&#x200B;을 선택합니다.

   개발 환경이 선택되어 있지 않은 경우에는 보고서 데이터를 사용하지 못할 수 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

환경에 대한 자세한 내용은 [호출](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)를 참조하십시오.

## 내 A/B 또는 MVT 활동에서 내 경험 간에 트래픽이 분리된 이유는 무엇입니까? {#uneven}

예를 들어, 트래픽 분할을 50/50 또는 25/25/25/25/25/25로 설정했지만 보고 내 경험 간에 매우 다른 분포를 보게 됩니다. 보고에는 불규칙한 방문자 수가 있는 다음과 같은 몇 가지 설명할 수 있는 이유가 [!DNL Target] 있습니다.

* 활동이 처음 실행되면 경험 전달을 최적화하는 데 사용하는 에지 노드 아키텍처로 인해 트래픽 배포 [!DNL Target] [!DNL Target] 가 고르지 않을 수 있습니다. 가장 좋은 방법은 활동을 잠시 시간을 내어 추가 데이터를 수집하고 분배가 표준화되는 것입니다. 아키텍처 및 [!DNL Adobe Target] 에지 노드에 대한 자세한 내용은 [Adobe Target 작동 방식을 참조하십시오](/help/c-intro/how-target-works.md).
* 방문 [!DNL Target] 지표를 사용 중인 [!DNL Analytics] 경우 **[!UICONTROL ,]** 방문 [!DNL Target] 지표는 방문자 기반 시스템이며 A/B 또는 MVT 테스트에 대한 트래픽 분배가 방문자 수준에서 지정된다는 점을 기억하십시오. 따라서 방문 횟수 지표를 사용하여 활동 결과 **[!UICONTROL 를]** 검사하면 특정 방문자가 여러 방문을 가질 수 있으므로 트래픽 분배가 고르지 않을 수 있습니다. 방문자는 활동 성과를 평가할 때 표준 표준화 지표입니다.
* A/B 및 MVT 테스트에 대한 우수 사례는 트래픽 분할을 유지하는 것입니다. 테스트 중 경험(예: 90/10/50/50) 간 트래픽 분포를 변경하면 경험 간에 방문자가 고르지 않을 수 있습니다. 낮은 트래픽 경험은 절대 &quot;따라잡기&quot;되지 않을 수 있습니다.
* 위의 우수 사례를 따르고 있고 트래픽 분할이 시간의 경과에 따라 표준화되지 않은 경우 다음을 확인해야 합니다.

   * 최신 at.js 라이브러리를 사용하고 계십니까? 현재 버전 및 관련 릴리스 노트에 대한 자세한 내용은 [at.js 버전 세부 정보를 참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * 리디렉션 테스트입니까? 페이지에서 태그를 실행하는 타이밍이 잘못되면 트래픽 분할이 고르지 않을 수 있습니다. 특히 활동에 대한 데이터 소스 [!DNL Analytics] 로 사용할 [!DNL Target] 때 그렇습니다. Analytics for Target(A4T)을 사용하여 리디렉션 활동에 대한 불규칙한 트래픽 배포를 개선하는 자세한 내용은 리디렉션 오퍼 - [A4T FAQ를 참조하십시오](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
