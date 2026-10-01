---
keywords: AI 인사이트;Experimentation Accelerator;기회;활동 개요
description: Adobe Target 활동 개요에서 Experimentation Accelerator에서 AI가 생성한 인사이트 및 최적화 기회를 사용하는 방법을 알아봅니다.
title: 활동 개요의 AI 인사이트
feature: Activities
badge: label="Beta" type="Informative"
source-git-commit: 8d2b3af9942acbf30519c1f7b32fe79bed1f2eaa
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 27%
---
# AI 인사이트

>[!AVAILABILITY]
>
>AI 인사이트 기능은 현재 베타 기능으로 사용할 수 있습니다.
></br>
>**[!UICONTROL AI 인사이트]** 섹션은 **[!UICONTROL 수동]** 트래픽 할당이 있는 **[!UICONTROL A/B 테스트]** 활동에만 사용할 수 있습니다.

**[!UICONTROL 활동 개요]**&#x200B;의 **[!UICONTROL AI 인사이트]** 메뉴를 통해 인사이트 및 최적화 기회에 액세스할 수 있습니다. 이 탭을 사용하여 실험 학습을 검토하고, 처리를 비교하고, 전환율을 향상시킬 수 있는 변경 사항을 식별합니다.

## AI 인사이트 및 기회 설정

>[!CONTEXTUALHELP]
>id="target_ai_insights"
>title="통찰력"
>abstract="인사이트는 실험이 통계적 중요도에 도달하면 사용할 수 있는 AI 생성 검색 결과입니다."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="기본 지표"
>abstract="기본 지표는 보고 설정에서 자동으로 가져옵니다. 변경하려면 목표 및 설정에서 목표 지표를 수정하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="가설"
>abstract="가설은 실험의 예상 결과를 설명하기 위해 정의하는 진술입니다. 어떤 대상이 어디에서 변경되는지 설명한 후 어떤 지표가 어떻게 변경될 것으로 예상하는지 명시하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="경험 세부 정보"
>abstract="경험 세부 사항은 사용자가 자격을 얻을 때 경험의 모습을 보여 줍니다. 모든 실험에 대해 해당 이미지를 검토할 수 있습니다. 일부 실험에서는 이미지를 확인하거나 필요한 경우 교체하도록 요청할 수 있습니다."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="기본 지표"
>abstract="기본 지표는 보고 설정에서 자동으로 가져옵니다. 변경하려면 목표 및 설정에서 목표 지표를 수정하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="가설"
>abstract="가설은 실험의 예상 결과를 설명하기 위해 정의하는 진술입니다. 어떤 대상이 어디에서 변경되는지 설명한 후 어떤 지표가 어떻게 변경될 것으로 예상하는지 명시하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="기회"
>abstract="실험 기회는 AI가 실험 스크린샷과 결과에서 발견한 패턴을 기반으로 제안한 처리 아이디어입니다."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="처리 세부 정보"
>abstract="처리 세부 정보는 사용자가 처리 자격을 얻을 때 처리가 어떤 모습인지 보여 주는 이미지를 제공합니다. 모든 실험에 대해 해당 이미지를 검토할 수 있습니다. 일부 실험에서는 이미지를 확인하거나 필요한 경우 교체하도록 요청할 수 있습니다."

AI가 생성한 인사이트 및 기회에 액세스하려면 먼저 기본 지표, 가설 및 경험 스크린샷을 확인하여 활동을 설정해야 합니다.

기본 지표는 보고 설정에서 자동으로 가져오며 목표 및 설정을 설정하는 방법에 따라 달라집니다. AI 인사이트 패널에서 가설을 생성해야 합니다. [자세히 알아보기](../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)

1. [!DNL Adobe Target]에서 활동을 엽니다.

1. **[!UICONTROL AI 인사이트]** 메뉴를 선택하여 구성 패널을 엽니다.

1. 실험에 대한 가설을 만들려면 ![](assets/do-not-localize/Smock_Edit_18_N.svg)을(를) 클릭합니다.

   ![](assets/ai-insights-7.png)

1. 수행된 변경 사항과 기본 지표에 영향을 주는 방법을 설명하여 가설을 입력합니다.

   **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 경험 세부 정보]**&#x200B;에서 카드를 클릭하여 경험에 대한 스크린샷을 추가합니다.

   >[!NOTE]
   >일부 이미지는 이미 자동으로 캡처되었을 수 있습니다. 이 경우 **[!UICONTROL 확인]**&#x200B;을 클릭하여 스크린샷을 확인합니다.

   ![](assets/ai-insights-1.png)

1. **[!UICONTROL 이미지 업로드]**&#x200B;를 선택하여 각 경험에 대한 로컬 파일에서 선호하는 스크린샷을 업로드하십시오.

   ![](assets/ai-insights-2.png)

1. 미리보기 링크를 복사하거나 직접 열어 경험을 미리 봅니다.

1. 각 경험에 스크린샷이 있으면 세부 사항을 검토하고 **[!UICONTROL 확인]**&#x200B;을 클릭하여 설정을 완료합니다.

설정이 완료되면 활동이 기회를 생성할 준비가 되었습니다. 실험이 통계적 유효성 검사에 대한 충분한 데이터를 가지고 필요한 실험 세부 사항이 확인되면 통찰력을 사용할 수 있습니다.

## 통찰력 {#insights}

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="통찰력"
>abstract="실험 인사이트는 실험이 통계적 중요도에 도달하면 사용할 수 있는 AI 생성 학습입니다."

실험 인사이트는 이 실험에서 파생된 AI 생성 학습입니다. 이러한 통찰력은 실험이 통계적 중요도에 도달하면 사용할 수 있으며 성공에 기여한 부분에 대한 컨텍스트를 제공합니다. 이 섹션에서는 대조군과 구별되며 결과에 영향을 미칠 수 있는 우승 경험에 있는 주요 속성을 강조합니다.

1. 카드를 클릭하여 **[!UICONTROL 인사이트]** 메뉴에 액세스합니다.

   ![](assets/ai-insights-3.png)

1. AI가 생성한 인사이트를 탐색하여 실험 학습을 검토하고 우승 경험을 통제 경험과 비교합니다.

   ![](assets/ai-insights-4.png)

1. **[!UICONTROL 무엇이 이 경험을 성공하게 만들었습니까?]**&#x200B;에서 이 경험이 제어를 능가하는 이유를 자세히 살펴보십시오.

## 기회

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="기회"
>abstract="실험 기회는 실험 스크린샷 및 결과에서 발견된 AI의 패턴에 기반한 AI 제안 경험 아이디어입니다."

**[!UICONTROL 기회]** 패널에는 테스트 성능을 개선하고 더 광범위한 비즈니스 목표와 KPI에 맞게 설계된 AI가 생성한 권장 사항이 표시됩니다.

1. 제안된 영업 기회를 탐색하고 검토할 영업 기회를 선택합니다.

   ![](assets/ai-insights-5.png)

1. 영업 기회를 선택하여 Opportunity Details 창을 엽니다. 이 창에는 특정 Experience 또는 Variation이 요약되어 있습니다. 이 보기에는 다음이 포함됩니다.

   * 영업 기회를 생성하는 데 사용되는 현재 경험 이미지입니다.

   * 제안된 경험의 예상 결과와 이것이 성과를 향상시킬 수 있는 이유를 설명하는 AI 생성 가설입니다.

   * 경험에서 권장 사항을 구현하고 선택한 지표에 미치는 영향을 측정하는 방법에 대한 지침입니다.

   ![](assets/ai-insights-6.png)

