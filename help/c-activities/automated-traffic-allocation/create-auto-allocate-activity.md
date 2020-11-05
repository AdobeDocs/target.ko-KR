---
keywords: Create auto-allocate;A/B test;auto-allocate activity;new a/b activity;auto allocate;auto-allocate to best experience;allocate
description: Adobe Target의 시각적 경험 작성기를 사용하여 Target이 활성화된 페이지에서 직접 자동 할당 A/B 테스트 활동을 만들고 Target 내의 페이지 부분을 수정할 수 있습니다.
title: 자동 할당 활동 만들기
feature: ab
topic: Advanced,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: fb4f43eef067a24f58ab8b53a7c8aa9c09392c9e
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 59%

---


# 자동 할당 활동 만들기

VEC( [!UICONTROL Visual Experience Composer] )를 [!DNL Adobe Target] 사용하여 자동 할당  A/B 테스트 [!UICONTROL 활동을 테스트 사용 가능한 페이지에서 직접 만들고 페이지 내에서 페이지] 를 수정하여 수정합니다 [!DNL Target][!DNL Target].

>[!NOTE]
>
>자동 할당  A/B 테스트 [!UICONTROL 활동] (이 문서에 설명됨) 외에 [!DNL Target] 두 가지 추가 유형의 [!UICONTROL A/B 테스트] 활동을 제공합니다. [!UICONTROL 수동(기본값)] 및 [!UICONTROL 자동 Target].
>
>A/ [B 테스트 개요에서 A/B 테스트 활동](/help/c-activities/t-test-ab/test-ab.md#types) 유형을 *참조하십시오*.

자동 할당 [!UICONTROL 활동을] 만들려면

1. From the **[!UICONTROL Activities]** list, click **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![활동 만들기 드롭다운 목록](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL 권장 사항]은 [Target Premium 기능](/help/c-intro/intro.md#premium)입니다.
   >
   >다양한 활동 유형에 대한 자세한 내용은 [활동](/help/c-activities/activities.md) 및 [Target 활동 안내서](/help/c-activities/target-activities-guide.md)를 참조하십시오.

1. 필요한 경우 **[!UICONTROL 시각적(기본값)]**&#x200B;을 선택합니다.

   ![A/B 테스트 활동 만들기](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   If you prefer to use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. 자세한 내용은 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL 양식 기반 Experience Composer]외에도 [!DNL Target] 단일 페이지 애플리케이션 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/c-experiences/experiences.md)를 참조하십시오.
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >이전 그림에서 [[!UICONTROL 작업 공간 선택]](/help/administrating-target/c-user-management/property-channel/property-channel.md) 선택 사항은 [Target Premium](/help/c-intro/intro.md) 기능입니다. Your organization has a [!UICONTROL Target Standard] license if you do not see this option.

1. (조건부) [Target Premium 고객](/help/c-intro/intro.md#premium)인 경우 [작업 공간](/help/administrating-target/c-user-management/property-channel/property-channel.md)을 선택합니다.

1. [활동 URL](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을 지정한 후, **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   계정이 기본 URL로 구성된 경우 기본적으로 해당 URL이 표시됩니다. 기본값에서 다른 URL로 변경할 수 있습니다.

   [!UICONTROL 시각적 경험 작성기]가 열리고 URL에 지정된 페이지가 표시됩니다.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

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

   [!UICONTROL 시각적 경험 작성기]에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md)를 참조하십시오. 경험 B를 수정하려면 3단계부터 시작하십시오.

1. **[!UICONTROL 시각적 경험 작성기]**&#x200B;의 맨 위에서 [!UICONTROL 타깃팅]을 클릭하여 3단계 안내가 워크플로우에서 다음 단계로 이동합니다.

   흐름 다이어그램이 열립니다.

   ![A/B 테스트 타깃팅 단계](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   흐름 다이어그램은 활동의 대상을 선택하고, 경험을 설정하는 단계를 안내합니다.

1. 대상  상자에서 편집 아이콘(세 개의 세로 줄임표)을 클릭하고 대상 **[!UICONTROL 대체를]**&#x200B;클릭한 다음 [활동의 대상을](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) 선택합니다.

   By default, the audience is set to [!UICONTROL All Visitors].

1. 활동을 입력하려는 자격 있는 방문자의 비율을 선택합니다.

   ![대상 비율](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아&quot; 대상의 45%로 제한할 수 있습니다.

1. 트래픽 할당을 설정합니다.

   동일한 대상에 대해 여러 경험을 표시할 수 있습니다. 다이어그램에 선택한 대상과 활동에 추가한 경험이 표시됩니다. 

   원하는 트래픽 할당 방법을 선택합니다. 자동 [!UICONTROL 할당] 활동을 만들려면 **[!UICONTROL 최적의 경험에 자동 할당을 선택합니다]**.

   트래픽 할당의 세 가지 유형은 아래에 설명되어 있습니다.

   * **[!UICONTROL 수동(기본값)]**: 각 경험을 보게 하려는 참여자의 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. For more information, see [Create an A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL 최고 경험에 자동 할당]**: 대부분의 활동 참여자가 자동으로 더 높은 성과를 보이는 경험으로 이동됩니다. 일부 방문자는 경험을 탐색하고 실적 동향 변화를 인식하기 위해 모든 경험에 할당됩니다.

   * **[!UICONTROL 개인화된 경험을 위한 자동 타깃팅]**: [!DNL Target] 고급 머신 러닝을 사용하여 성과가 높은 마케터가 정의한 여러 경험을 파악하고 방문자의 개별 고객 프로파일과 과거 유사 방문자의 행동을 바탕으로 방문자에게 가장 적합한 경험을 제공하여 컨텐츠를 개인화하고 전환율을 높일 수 있습니다. 자세한 내용은 자동 [Target을 참조하십시오](/help/c-activities/auto-target/auto-target-to-optimize.md).
   You can also click **[!UICONTROL Add]** to add another experience to the activity.

1. When you are satisfied with your audience, experience choices, and traffic allocation choices, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

1. 활동에 대한 [목표 및 설정](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)을 지정합니다.

   ![A/B 활동 설정](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. 저장 **[!UICONTROL 및 닫기]** 또는 **[!UICONTROL 저장을 클릭합니다]**.

After you create the activity, the [!UICONTROL Overview] tab shows information about the activity, including a diagram of your activity.

## Training video: Creating A/B Tests (8:36) ![Tutorial badge](/help/assets/tutorial.png)

이 비디오에서는 [!DNL Target]의 안내가 있는 3단계 워크플로우를 사용하여 A/B 테스트를 만드는 방법을 보여 줍니다.

* A/ [!UICONTROL B 테스트] 활동을 [!DNL Adobe Target]
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391)