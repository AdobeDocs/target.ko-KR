---
keywords: 자동 타겟 만들기;A/B 테스트;자동 타겟 활동;새 a/b 활동;자동 타겟;개인화된 경험에 대한 자동 타겟;개인화된;최적화
description: '[!UICONTROL Visual Experience Composer] (VEC)을(를) 사용하여 [!UICONTROL Auto-Target] A/B 테스트 활동을 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Auto-Target] 활동을 만드는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 18%

---

# [!UICONTROL Auto-Target] 활동 만들기

[!DNL Target]을(를) 사용할 수 있는 페이지에서 바로 [!UICONTROL Auto-Target] [!UICONTROL A/B Test] 활동을 만들고 [!DNL Target] 내에서 해당 페이지의 부분을 수정하려면 [!DNL Adobe Target]의 [!UICONTROL Visual Experience Composer] (VEC)를 사용하십시오.

>[!NOTE]
>
>[!UICONTROL Auto-Target]은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md)을 참조하십시오.

[!UICONTROL Auto-Target] 활동을 만들려면:

1. **[!UICONTROL Activities]** 목록에서 **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**&#x200B;을(를) 클릭합니다.

1. 필요한 경우 [!UICONTROL Create A/B Test Activity] 대화 상자에서 **[!UICONTROL Visual]**&#x200B;을(를) 선택합니다.

   [!UICONTROL Form-Based Experience Composer]을(를) 사용하려면 [!UICONTROL Form]을(를) 선택하십시오. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL Form-Based Experience Composer] 외에 [!DNL Target]에서 [!UICONTROL Single Page Application] VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [Target Premium 고객](/help/main/c-intro/intro.md#premium)인 경우 **[!UICONTROL Choose Workspace]** 드롭다운 목록에서 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을(를) 선택하십시오.

   [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 옵션은 [Target Premium](/help/main/c-intro/intro.md) 기능이며 조직에 [!UICONTROL Target Standard] 라이선스가 있는 경우 표시되지 않을 수 있습니다.

1. **[!UICONTROL Enter Activity URL]** 상자에서 [활동 URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을 지정하십시오.

   계정이 [기본 URL로 구성](/help/main/administrating-target/visual-experience-composer-set-up.md)된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

   [!UICONTROL Visual Experience Composer]이(가) 열리고 URL에 지정된 페이지가 표시됩니다.

1. **[!UICONTROL Rename]** 아이콘(![이름 바꾸기 아이콘](/help/main/assets/icons/MoreSmallListVert.svg))을 클릭하고 **[!UICONTROL Rename]**&#x200B;을 클릭한 다음 활동의 이름을 지정하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   활동 이름은 다음 문자로 시작할 수 없습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

   활동 이름에는 다음 문자 시퀀스를 사용할 수 없습니다.

   | 문자 시퀀스 | 설명 |
   |--- |--- |
   | ;= | 세미콜론, 다음과 같음 |
   | ;+ | 세미콜론, 플러스 |
   | ;- | 세미콜론, 빼기 |
   | ;@ | 세미콜론, @ 기호 |
   | ,= | 쉼표, 같음 |
   | ,+ | 쉼표, 더하기 |
   | ,- | 쉼표, 빼기 |
   | ,@ | 쉼표, @ 기호 |
   | `[`&quot; | 대괄호 열기, 큰따옴표 |
   | &quot;`]` | 큰따옴표, 대괄호 닫기 |

1. 페이지의 요소를 변경하여 새 경험을 만듭니다.

   새 활동을 만든 후 [!UICONTROL Visual Experience Composer]의 왼쪽에 두 개의 탭([!UICONTROL Experience A] 및 [!UICONTROL Experience B])이 표시됩니다. [!UICONTROL Experience A]은(는) 제어 경험입니다. 포커스는 원하는 대로 수정할 수 있는 [!UICONTROL Experience B] 탭에 있습니다. [!UICONTROL Experience B]은(는) 테스트에 추가할 수 있는 대체 경험입니다. [!UICONTROL Experiences] 창 상단의 [!UICONTROL Add] 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg))을 클릭하여 테스트에 여러 경험을 추가할 수 있습니다. 기본 사이트 경험을 옵션으로 포함하지 않으려면 활동에서 경험 A를 삭제할 수도 있습니다.

   [!UICONTROL Visual Experience Composer]에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00)를 참조하십시오. 경험 B를 수정하려면 2단계부터 시작하십시오.

1. 안내가 있는 3단계 워크플로우에서 다음 단계로 이동하려면 [!UICONTROL Visual Experience Composer]의 맨 위에서 **[!UICONTROL Targeting]**&#x200B;을(를) 클릭합니다.

   흐름 다이어그램이 열립니다.

   ![A/B 테스트 타깃팅 단계](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   흐름 다이어그램은 대상과 해당 트래픽 비율을 할당하고, 트래픽 할당 방법을 선택하고, 활동의 각 경험에 대한 트래픽 할당을 지정하는 단계를 안내합니다.

1. (조건부) **[!UICONTROL All Visitors]** 컨트롤을 클릭하여 활동에 대한 다른 대상을 선택합니다.

   [!UICONTROL All Visitors] 대상이 기본값으로 설정됩니다. 다른 대상을 선택하면 해당 이름이 가장 왼쪽 컨트롤에 표시됩니다.

   오른쪽 프레임이 표시되어 대상을 추가 또는 삭제하고 활동에 대한 방문자 비율을 할당할 수 있습니다.

   1. 대상을 변경하려면 오른쪽 프레임에서 **[!UICONTROL Replace]아이콘**(![바꾸기 아이콘](/help/main/assets/icons/Retweet.svg))을 클릭합니다.
   1. [!UICONTROL Add Audience] 대화 상자에서 [원하는 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)한 다음 **[!UICONTROL Assign Audience]**&#x200B;을(를) 클릭합니다.

      **대상 결합**&#x200B;을 클릭하여 [여러 대상을 결합하는 대상을 만들 수 있습니다](/help/main/c-target/combining-multiple-audiences.md).

      [!UICONTROL Audience Library]에 없는 새 대상을 만들어야 하는 경우 **대상 만들기**&#x200B;를 클릭합니다. [대상자 만들기 워크플로](/help/main/c-target/c-audiences/audiences.md) 동안 다음 옵션 중에서 선택할 수 있습니다.

      * **[!UICONTROL Audience Library]**: [!UICONTROL Audience Library]에 저장된 온디맨드 대상을 만들어 다른 활동에서 다시 사용할 수 있습니다.
      * **[!UICONTROL This activity only]**: [!UICONTROL Audience Library]에 저장되지 않고 현재 활동에서만 사용할 수 있는 [활동별 대상](/help/main/c-target/creating-activity-only-audience.md)을 만듭니다.

   1. 오른쪽 프레임에서 **[!UICONTROL Visitor Percentage]**&#x200B;을(를) 클릭한 다음 활동을 시작할 자격 있는 방문자의 비율을 선택합니다.

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아인&quot; 대상자의 45%로 제한할 수 있습니다.

1. **[!UICONTROL Traffic Allocation]** 컨트롤을 클릭한 다음 오른쪽 창에서 원하는 트래픽 할당 방법을 선택합니다. 이 시나리오에서는 **[!UICONTROL Auto-Taget for personalized experiences]**&#x200B;을(를) 클릭합니다.

   ![트래픽 할당 메서드 설정](/help/main/c-activities/assets/auto-target.png)

   다음 트래픽 할당 방법을 사용할 수 있습니다.

   * **[!UICONTROL Manual (Default)]**: 각 경험을 보게 하려는 참여자의 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. 

   * **[!UICONTROL Auto-Allocate to best experience]**: 대부분의 활동 참여자가 자동으로 더 높은 성과를 보이는 경험으로 이동됩니다. 일부 방문자는 경험을 탐색하고 성과 동향 변화를 인식하기 위해 모든 경험에 할당됩니다. 자세한 내용은 [[!UICONTROL Auto-Allocate] 개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)를 참조하십시오.

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target]은(는) 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험을 식별한 후 개별 고객 프로필 및 유사한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 맞춤 설정된 경험을 제공함으로써 콘텐츠를 개인화하고 전환을 유도합니다. 자세한 내용은 [자동 타겟 개요](/help/main/c-activities/auto-target/auto-target-to-optimize.md)를 참조하십시오.

1. 오른쪽 창에서 **[!UICONTROL Experiences]**&#x200B;을(를) 클릭한 다음 각 경험에 대해 원하는 트래픽 할당을 지정합니다.

1. 대상, 경험 선택 사항 및 트래픽 할당 선택 사항이 만족스러우면 **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 안내가 있는 3단계 워크플로의 세 번째 단계로 이동합니다.

1. 활동에 대한 [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)을 지정합니다.

   >[!NOTE]
   >
   >이 활동에 [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)을 사용하려면 자동 할당 및 자동 타겟 활동에 대한 [A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)의 중요 정보를 참조하십시오.

1. **[!UICONTROL Save & Close]** 또는 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

활동을 만든 후 [!UICONTROL Overview] 탭에는 활동의 다이어그램을 포함하여 활동에 대한 정보가 표시됩니다.
