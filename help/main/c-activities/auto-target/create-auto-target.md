---
keywords: 자동 타겟 만들기;A/B 테스트;자동 타겟 활동;새 a/b 활동;자동 타겟;개인화된 경험에 대한 자동 타겟;개인화된;최적화
description: Adobe에서 시각적 경험 작성기(VEC)를 사용하는 방법에 대해 알아봅니다 [!DNL Target] 에서 직접 자동 Target A/B 테스트 활동을 만들려면 [!DNL Target]-enabled 페이지.
title: 자동 Target 활동을 만들려면 어떻게 해야 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 48%

---

# 자동 타겟 활동 만들기

사용 [!UICONTROL 시각적 경험 작성기] (VEC) 위치 [!DNL Adobe Target] 다음을 만들려면: [!UICONTROL 자동 Target] [!UICONTROL A/B 테스트] 에서 바로 활동 [!DNL Target]-enabled page 및 내에서 페이지 일부 수정 [!DNL Target].

>[!NOTE]
>
>[!UICONTROL 자동 타겟]은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md)을 참조하십시오.
>
>이외에도 [!UICONTROL 자동 Target] [!UICONTROL A/B 테스트] 활동(이 문서에서 설명됨), [!DNL Target] 는 두 가지 다른 유형의 [!UICONTROL A/B 테스트] 활동: [!UICONTROL 수동(기본값)] 및 [!UICONTROL 자동 할당].
>
>다음을 참조하십시오 [A/B 테스트 활동 유형](/help/main/c-activities/t-test-ab/test-ab.md#types) 위치: *A/B 테스트 개요*.

을(를) 만들려면 [!UICONTROL 자동 Target] 활동:

1. 다음에서 **[!UICONTROL 활동]** 목록, 클릭 **[!UICONTROL 활동 만들기]** > **[!UICONTROL A/B 테스트]**.

   ![활동 만들기 드롭다운 목록](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어, [!UICONTROL 자동 Target] 및 [!UICONTROL Recommendations] 은(는) [Target Premium 기능](/help/main/c-intro/intro.md#premium).
   >
   >다양한 활동 유형에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md) 및 [Target 활동 안내서](/help/main/c-activities/target-activities-guide.md)를 참조하십시오.

1. 필요한 경우 **[!UICONTROL 시각적(기본값)]**&#x200B;을 선택합니다.

   ![A/B 테스트 활동 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   을(를) 사용하려면 [!UICONTROL 양식 기반 경험 작성기], 선택 [!UICONTROL 양식]. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL 양식 기반 경험 작성기], [!DNL Target] 는 단일 페이지 애플리케이션 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >이전 그림에서 [[!UICONTROL 작업 공간 선택]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 선택 사항은 [Target Premium](/help/main/c-intro/intro.md) 기능입니다. 조직에 [!UICONTROL Target Standard] 이 옵션이 표시되지 않으면 라이센스를 부여하십시오.

1. 선택 [작업 영역](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [활동 URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을 지정한 후, **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   계정이 기본 URL로 구성된 경우 기본적으로 해당 URL이 표시됩니다. 기본값에서 다른 URL로 변경할 수 있습니다.

   [!UICONTROL 시각적 경험 작성기]가 열리고 URL에 지정된 페이지가 표시됩니다.

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

   다음 [!UICONTROL 시각적 경험 작성기] 활동을 만든 후 왼쪽에 경험 A와 경험 B, 이렇게 두 개의 탭이 표시됩니다. 경험 A는 제어 경험입니다. 포커스는 원하는 대로 수정할 수 있는 경험 B 탭에 있습니다. 경험 B는 테스트에 추가할 수 있는 대체 경험입니다. 테스트에 여러 경험을 추가할 수 있습니다. 기본 사이트 경험을 옵션으로 포함하지 않으려면 활동에서 경험 A를 삭제할 수도 있습니다.

   [!UICONTROL 시각적 경험 작성기]에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md)를 참조하십시오. 경험 B를 수정하려면 3단계부터 시작하십시오.

1. **[!UICONTROL 시각적 경험 작성기]**&#x200B;의 맨 위에서 [!UICONTROL 타깃팅]을 클릭하여 3단계 안내가 워크플로우에서 다음 단계로 이동합니다.

   흐름 다이어그램이 열립니다.

   ![A/B 테스트 타깃팅 단계](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   흐름 다이어그램은 활동의 대상을 선택하고, 경험을 설정하는 단계를 안내합니다.

1. 다음에서 [!UICONTROL 대상자] 상자에서 편집 아이콘(3개의 수직 줄임표)을 클릭하고 **[!UICONTROL 대상 바꾸기]**, 그런 다음 [대상자 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) 을 참조하십시오.

   기본적으로 대상자는 [!UICONTROL 모든 방문자].

1. 활동을 입력하려는 자격 있는 방문자의 비율을 선택합니다.

   ![대상 비율](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아&quot; 대상의 45%로 제한할 수 있습니다.

1. 트래픽 할당을 설정합니다.

   동일한 대상에 대해 여러 경험을 표시할 수 있습니다. 다이어그램에 선택한 대상과 활동에 추가한 경험이 표시됩니다. 

   원하는 트래픽 할당 방법을 선택합니다. 을(를) 만들려면 [!UICONTROL 자동 Target] 활동, 선택 **[!UICONTROL 개인화된 경험에 대한 자동 Target]**.

   세 가지 유형의 트래픽 할당은 아래에 설명되어 있습니다.

   * **[!UICONTROL 수동(기본값)]**: 각 경험을 보게 하려는 참여자의 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. 자세한 내용은 [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL 최고 경험에 자동 할당]**: 대부분의 활동 참여자가 자동으로 더 높은 성과를 보이는 경험으로 이동됩니다. 일부 방문자는 경험을 탐색하고 실적 동향 변화를 인식하기 위해 모든 경험에 할당됩니다. 자세한 내용은 [자동 할당 개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL 개인화된 경험에 대한 자동 Target]**: [!DNL Target] 에서는 고급 머신 러닝을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별한 후, 개별 고객 프로필 및 유사한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 조정된 경험을 제공함으로써 콘텐츠를 개인화하고 전환을 유도합니다.
   다음을 클릭할 수도 있습니다. **[!UICONTROL 추가]** 활동에 다른 경험을 추가합니다.

1. 대상, 경험 선택 사항 및 트래픽 할당 선택 사항이 만족스러우면 다음을 클릭하십시오. **[!UICONTROL 다음]** 안내가 있는 3단계 워크플로우의 세 번째 단계로 이동합니다.

1. 활동에 대한 [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)을 지정합니다.

   ![A/B 활동 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

   >[!NOTE]
   >
   >을(를) 사용하려면 [Target 분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) 이 활동을 사용하는 경우에서 중요 정보를 참조하십시오. [자동 할당 및 자동 Target 활동에 대한 A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. 클릭 **[!UICONTROL 저장 및 닫기]** 또는 **[!UICONTROL 저장]**.

활동을 만든 후 [!UICONTROL 개요] 탭에는 활동의 다이어그램을 포함하여 활동에 대한 정보가 표시됩니다.

## 교육 비디오: A/B 테스트 만들기(8:36) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에서는 [!DNL Target]의 안내가 있는 3단계 워크플로우를 사용하여 A/B 테스트를 만드는 방법을 보여 줍니다.

* 만들기 [!UICONTROL A/B 테스트] 의 활동 [!DNL Adobe Target]
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391)
