---
description: Target을 사용할 수 있는 페이지에서 바로 테스트를 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target의 시각적 경험 작성기를 사용하십시오.
keywords: A/B 만들기;A/B 테스트;A/B 활동;새 a/b 활동
seo-description: Target을 사용할 수 있는 페이지에서 바로 테스트를 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target의 시각적 경험 작성기를 사용하십시오.
seo-title: A/B 테스트 만들기
solution: Target
title: A/B 테스트 만들기
topic: 고급,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# A/B 테스트 만들기{#create-an-a-b-test}

Target을 사용할 수 있는 페이지에서 바로 테스트를 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 Target의 시각적 경험 작성기를 사용하십시오.

1. [!UICONTROL 활동] 목록에서 **[!UICONTROL 활동 만들기]** &gt; **[!UICONTROL A/B 테스트]** 를 클릭합니다.

   ![활동 만들기 드롭다운 목록](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. For example, [!UICONTROL Recommendations] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For information about the various activity types, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) and the [Target activities guide](/help/c-activities/target-activities-guide.md).

   ![A/B 테스트 Actity 만들기](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   양식 기반 경험 작성기를 사용하려면 [!UICONTROL 양식을 선택합니다]. See [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >Target는 VEC 및 양식 기반 Experience Composer 외에도 단일 페이지 애플리케이션 VEC와 모바일 앱용 VEC를 제공합니다. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >The [!UICONTROL [Choose Workplace](/help/administrating-target/c-user-management/property-channel/property-channel.md) option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. 이 옵션이 표시되지 않는 경우 조직에 Target Standard 라이선스가 있습니다.]

1. (조건부) Target Premium 고객인 경우 작업 영역을 선택합니다.

1. [활동 URL](../../../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)를 지정하고 다음을 클릭합니다 **[!UICONTROL ]**.

   계정이 기본 URL로 구성된 경우 기본적으로 해당 URL이 표시됩니다. 기본값에서 다른 URL로 변경할 수 있습니다.

   [!UICONTROL 시각적 경험 작성기]가 열리고 URL에 지정된 페이지가 표시됩니다.

   ![vec](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. 제공된 공간에 활동의 이름을 입력합니다.

   ![이름 필드](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   다음 문자는 활동 이름에서 허용되지 않습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `/` | 슬래시 |
   | `?` | 물음표 |
   | `#` | 숫자 기호 |
   | `:` | 콜론 |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

1. 페이지의 요소를 변경하여 새 경험을 만듭니다.

   새 활동을 만든 후에 [!UICONTROL 시각적 경험 작성기] 왼쪽에 두 개의 탭(경험 A 및 경험 B)이 표시됩니다. 경험 A는 제어 경험입니다. 포커스는 경험 B 탭에 놓이므로 원하는 대로 수정할 수 있습니다. 경험 B는 테스트에 추가할 수 있는 대체 경험입니다. 테스트에 여러 경험을 추가할 수 있습니다. 기본 사이트 경험을 옵션으로 포함하지 않으려면 활동에서 경험 A를 삭제할 수도 있습니다.

   [!UICONTROL 시각적 경험 작성기]에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](../../../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00)를 참조하십시오. 경험 B를 수정하려면 3단계부터 시작하십시오.

1. Click **[!UICONTROL Targeting]** at the top of the [!UICONTROL Visual Experience Composer] to move to the next step in the three-step guided workflow.

   흐름 다이어그램이 열립니다.

   ![A/B 테스트 타깃팅 단계](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   흐름 다이어그램은 활동의 대상을 선택하고, 경험을 설정하는 단계를 안내합니다.
1. [!UICONTROL 대상] 상자에서 편집 아이콘을 클릭한 후, 활동에 대한 [대상을 선택합니다](../../../c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087).

   기본적으로 대상은 모든 방문자로 설정됩니다.

1. 활동을 입력하려는 자격 있는 방문자의 비율을 선택합니다.

   ![고객 백분율](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아&quot; 대상의 45%로 제한할 수 있습니다.

1. 트래픽 할당을 설정합니다.

   동일한 대상에 대해 여러 경험을 표시할 수 있습니다. 다이어그램에 선택한 대상과 활동에 추가한 경험이 표시됩니다. 

   원하는 트래픽 할당 방법을 선택합니다.

   * **[!UICONTROL 수동 (기본값)]**: 각 경험을 볼 참가자 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. 

   * **[!UICONTROL 최적의 경험에 자동 할당]**: 대부분의 활동 참가자는 자동으로 성과가 높은 경험으로 연결됩니다. 일부 방문자는 경험을 탐색하고 실적 동향 변화를 인식하기 위해 모든 경험에 할당됩니다. [자동화된 트래픽 할당](../../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)을 참조하십시오.

   * **[!UICONTROL 개인화된 경험을 위한 자동 타깃팅]**: Target는 고급 머신 러닝 알고리즘을 사용하여 방문자를 최적의 경험으로 자동으로 타겟팅하여 목표를 극대화합니다. 자세한 내용은 [자동 타겟으로 최적화](../../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)를 참조하십시오.
   **[!UICONTROL 경험 추가]를 클릭하여 활동에 다른 경험을 추가할 수도 있습니다.**

1. 선택한 대상 및 경험이 만족스러우면 **[!UICONTROL 다음]** 을 클릭하여 안내가 있는 3단계 워크플로우의 세 번째 단계로 이동합니다.

1. 활동에 대한 [목표 및 설정](../../../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)을 지정합니다.

   ![A/B 활동 설정](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. **[!UICONTROL 저장을 클릭합니다]**.

활동을 만든 후 개요 탭에는 활동의 다이어그램을 포함하여 활동에 대한 정보가 표시됩니다.

## 교육 비디오: A/B 테스트 만들기(8:36)

이 비디오에서는 [!DNL Target]의 안내가 있는 3단계 워크플로우를 사용하여 A/B 테스트를 만드는 방법을 보여 줍니다.

* Adobe Target에서 A/B 활동 만들기
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391?captions=kor)
