---
keywords: 자동 할당 만들기;A/B 테스트;자동 할당 활동;새 a/b 활동;자동 할당;최고 경험에 자동 할당;할당;자동 할당
description: '[!UICONTROL Visual Experience Composer]의  [!DNL Adobe Target] (VEC)을(를) 사용하여 [!UICONTROL Auto-Allocate] A/B 테스트 활동을 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Auto-Allocate] 활동을 만드는 방법'
feature: Auto-Allocate
exl-id: 30bc95e0-4f5e-4d1f-bad2-7b20b8f3c7d2
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 36%

---

# [!UICONTROL Auto-Allocate] 활동 만들기

[!UICONTROL Visual Experience Composer]을(를) 사용할 수 있는 페이지에서 바로 [!DNL Adobe Target] [!UICONTROL Auto-Allocate] 활동을 만들고 [!UICONTROL A/B Test] 내에서 해당 페이지의 부분을 수정하려면 [!DNL Target]의 [!DNL Target]&#x200B;(VEC)를 사용하십시오.

[!UICONTROL Auto-Allocate]은(는) [!UICONTROL A/B Test] [!DNL Target] 활동(이 문서에서 설명됨) 외에도 두 가지 유형의 [!UICONTROL A/B Test] 활동을 추가로 제공합니다. [!UICONTROL Manual (Default)] 및 [!UICONTROL Auto-Target]. [A/B 테스트 개요](/help/main/c-activities/t-test-ab/test-ab.md#types)에서 *A/B 테스트 활동 유형*&#x200B;을 참조하세요.

[!UICONTROL Auto-Allocate] 활동을 만들려면:

1. **[!UICONTROL Activities]** 목록에서 **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**&#x200B;을(를) 클릭합니다.

   ![활동 만들기 드롭다운 목록](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL Recommendations]은(는) [Target Premium 기능](/help/main/c-intro/intro.md#premium)입니다. 다양한 활동 유형에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md) 및 [Target 활동 안내서](/help/main/c-activities/target-activities-guide.md)를 참조하십시오.

1. 필요한 경우 **[!UICONTROL Create A/B Test Activity]** 대화 상자에서 **[!UICONTROL Visual]**&#x200B;을(를) 선택합니다.

   [!UICONTROL Form-Based Experience Composer]을(를) 사용하려면 [!UICONTROL Form]을(를) 선택하십시오. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL Form-Based Experience Composer] 외에 [!DNL Target]에서 단일 페이지 응용 프로그램 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [Target Premium 고객](/help/main/c-intro/intro.md#premium)인 경우 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 선택합니다.

1. [활동 URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을(를) 지정한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   계정이 기본 URL로 구성된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

   [!UICONTROL Visual Experience Composer]이(가) 열리고 URL에 지정된 페이지가 표시됩니다.

   ![VEC](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. 제공된 공간에 활동의 이름을 입력합니다.

   ![이름 필드](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   활동 이름은 다음 문자로 시작할 수 없습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

1. 페이지의 요소를 변경하여 모든 경험을 만듭니다.

   새 활동을 만든 후 [!UICONTROL Visual Experience Composer]의 왼쪽에 경험 A와 경험 B, 이렇게 두 개의 탭이 표시됩니다. 경험 A는 제어 경험입니다. 포커스는 원하는 대로 수정할 수 있는 경험 B 탭에 있습니다. 경험 B는 테스트에 추가할 수 있는 대체 경험입니다. 테스트에 여러 경험을 추가할 수 있습니다. 기본 사이트 경험을 옵션으로 포함하지 않으려면 활동에서 경험 A를 삭제할 수도 있습니다.

   [!UICONTROL Visual Experience Composer]에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md)를 참조하십시오. 경험 B를 수정하려면 2단계부터 시작하십시오.

1. 안내가 있는 3단계 워크플로우에서 다음 단계로 이동하려면 **[!UICONTROL Targeting]**&#x200B;의 맨 위에서 [!UICONTROL Visual Experience Composer]을(를) 클릭합니다.

   흐름 다이어그램이 열립니다.

   ![A/B 테스트 타깃팅 단계](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   흐름 다이어그램은 활동의 대상자를 선택하고, 경험을 설정하는 단계를 안내합니다.

1. [!UICONTROL Audience] 상자에서 편집 아이콘(세로 줄임표)을 클릭하고 **[!UICONTROL Replace Audience]**&#x200B;을 클릭한 다음 [활동에 대한 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)합니다.

   기본적으로 대상은 [!UICONTROL All Visitors]&#x200B;(으)로 설정됩니다.

1. 활동을 입력하려는 자격 있는 방문자의 비율을 선택합니다.

   ![대상자 비율](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아인&quot; 대상자의 45%로 제한할 수 있습니다.

1. 트래픽 할당 방법을 설정합니다.

   동일한 대상에 대해 여러 경험을 표시할 수 있습니다. 선택한 대상과 활동에 추가한 경험을 보여주는 다이어그램이 표시됩니다.

   원하는 트래픽 할당 방법을 선택합니다. [!UICONTROL Auto-Allocate] 활동을 만들려면 **[!UICONTROL Auto-Allocate to best experience]**&#x200B;을(를) 선택합니다.

   세 가지 유형의 트래픽 할당은 아래에 설명되어 있습니다.

   * **[!UICONTROL Manual (Default)]**: 각 경험을 보게 하려는 참여자의 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. 자세한 내용은 [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)를 참조하십시오.

   * **[!UICONTROL Auto-allocate to best experience]**: 대부분의 활동 참여자가 자동으로 더 높은 성과를 보이는 경험으로 이동됩니다. 일부 방문자는 경험을 탐색하고 성능 트렌드의 변화를 인식하기 위해 모든 경험에 할당됩니다.

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target]은(는) 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험을 식별한 후 개별 고객 프로필 및 유사한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 맞춤 설정된 경험을 제공함으로써 콘텐츠를 개인화하고 전환을 유도합니다. 자세한 내용은 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 참조하세요.

   **[!UICONTROL Add]**&#x200B;을(를) 클릭하여 활동에 다른 경험을 추가할 수도 있습니다.

1. 대상, 경험 선택 사항 및 트래픽 할당 선택 사항이 만족스러우면 **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 안내가 있는 3단계 워크플로의 세 번째 단계로 이동합니다.

1. 활동에 대한 [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)을 지정합니다.

   >[!NOTE]
   >
   >이 활동에 [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)을 사용하려면 자동 할당 및 자동 타겟 활동에 대한 [A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)의 중요 정보를 참조하십시오.

1. **[!UICONTROL Save & Close]** 또는 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

활동을 만든 후 [!UICONTROL Overview] 탭에는 활동의 다이어그램을 포함하여 활동에 대한 정보가 표시됩니다.

## 교육 비디오: A/B 테스트 만들기(8:36)

이 비디오에서는 [!DNL Target]의 안내가 있는 3단계 워크플로를 사용하여 A/B 테스트를 만드는 방법을 보여 줍니다.

* [!UICONTROL A/B Test]에서 [!DNL Adobe Target] 활동 만들기
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391)
