---
keywords: 자동 타겟 만들기;A/B 테스트;자동 타겟 활동;새 a/b 활동;자동 타겟;개인화된 경험에 대한 자동 타겟;개인화된;최적화
description: '[!UICONTROL 시각적 경험 작성기](VEC)를 사용하여 [!UICONTROL 자동 타겟] A/B 테스트 활동을 만드는 방법을 알아봅니다.'
title: '[!UICONTROL 자동 타겟] 활동을 만드는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
TQID: 'https://experienceleague.adobe.com/qbt-h-4C4uVz6r6xmwKmSeU-RuBdWikmtDQq40dBq9k'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: 9f1aaf5c0b172b4bbe89266800708881306e4592
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 12%
---
# [!UICONTROL 자동 타겟] 활동 만들기 {#create-auto-target-activity}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 **[!UICONTROL 자동 타겟]** 활동을 만드는 방법을 알아봅니다. 경험을 빌드하고, 타깃팅을 설정하고, 자동 타겟 트래픽 할당 방법을 선택한 다음 목표와 설정을 구성합니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL 시각적 경험 작성기]**(VEC)를 사용하여 [!DNL Target]이(가) 활성화된 페이지에서 직접 **[!UICONTROL 자동 타겟]** **[!UICONTROL A/B 테스트]** 활동을 만들고 [!DNL Target] 내에서 해당 페이지의 부분을 수정합니다.

>[!NOTE]
>
>**[!UICONTROL 자동 타겟]**&#x200B;은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md)을 참조하십시오.

활동은 VEC의 안내가 있는 3단계 워크플로우를 따릅니다.

1. [경험 구축](#build-experiences)
1. [타깃팅 및 트래픽 할당 설정](#set-targeting)
1. [목표 및 설정 구성](#configure-goals-and-settings)

## 1단계: 경험 구축 {#build-experiences}

활동을 만든 다음, 컨트롤에 대해 테스트할 대체 경험을 디자인합니다.

### 활동 만들기 {#create-activity}

**[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 테스트할 페이지를 열고 활동의 이름을 지정합니다.

1. **[!UICONTROL 활동]** 목록에서 **[!UICONTROL 활동 만들기]** > **[!UICONTROL A/B 테스트]**&#x200B;를 클릭합니다.

   ![](../assets/create-ab-1.png)

1. **[!UICONTROL A/B 테스트 활동 만들기]** 대화 상자에서 경험 작성기를 선택합니다.

   * **[!UICONTROL Visual]**.
   * **[!UICONTROL 양식 기반 경험 작성기]**&#x200B;에서 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 **[!UICONTROL 양식 기반 경험 작성기]** 외에 [!DNL Target]에서 **[!UICONTROL 단일 페이지 애플리케이션]** VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [Target Premium 고객](/help/main/c-intro/intro.md#premium)인 경우 **[!UICONTROL Workspace 선택]** 드롭다운 목록에서 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 선택합니다.

1. **[!UICONTROL 활동 URL 입력]** 상자에서 [활동 URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을 지정하십시오.

   계정이 [기본 URL로 구성](/help/main/administrating-target/visual-experience-composer-set-up.md)된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. **[!UICONTROL 시각적 경험 작성기]**&#x200B;가 열리고 URL에 지정된 페이지가 표시됩니다.

1. 활동의 이름을 지정하려면 **[!UICONTROL 편집]** 아이콘(![편집 아이콘](/help/main/assets/icons/Edit.svg))을 클릭하고 활동에 대한 수사적 이름을 지정한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   {{activity-name-rules}}

   ![](../assets/create-ab-2.png)

### 경험 디자인 {#design-experiences}

페이지의 요소를 변경하여 새 경험을 만듭니다.

새 활동을 만들면 **[!UICONTROL 시각적 경험 작성기]**&#x200B;의 왼쪽에 경험 A와 경험 B, 이렇게 두 개의 탭이 표시됩니다.

* **경험 A**&#x200B;은(는) 제어 경험입니다. 기본 사이트 경험을 옵션으로 포함하지 않으려는 경우 삭제할 수 있습니다.
* **경험 B**&#x200B;은(는) 테스트에 추가하는 대체 경험입니다. 포커스는 이 탭에 있으며, 이 탭에서 원하는 대로 수정할 수 있습니다.

테스트에 더 많은 경험을 추가하려면 **[!UICONTROL 추가]** 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg))을 클릭하세요.

![](../assets/create-ab-3.png)

**[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 경험을 추가 및 수정하는 방법에 대한 자세한 내용은 [경험 추가](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#ab-add-experience)를 참조하십시오.

## 2단계: 타깃팅 및 트래픽 할당 설정 {#set-targeting}

**[!UICONTROL 타깃팅]** 메뉴에 액세스하면 흐름 다이어그램이 열립니다.

![A/B 테스트 타깃팅 단계](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

흐름 다이어그램은 대상과 해당 트래픽 비율을 할당하고, 트래픽 할당 방법을 선택하고, 활동의 각 경험에 대한 트래픽 할당을 지정하는 과정을 안내합니다.

1. (조건부) **[!UICONTROL 모든 방문자]** 컨트롤을 클릭하여 활동에 대한 다른 대상을 선택합니다.

   **[!UICONTROL 모든 방문자]** 대상이 기본값으로 설정됩니다. 다른 대상을 선택하면 해당 이름이 가장 왼쪽 컨트롤에 표시됩니다. 예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아인&quot; 대상자의 45%로 제한할 수 있습니다.

   +++ 다른 대상을 선택하는 절차

   오른쪽 프레임이 표시되어 대상을 추가 또는 삭제하고 활동에 대한 방문자 비율을 할당할 수 있습니다.

   1. 대상을 변경하려면 오른쪽 프레임에서 **[!UICONTROL 바꾸기]** 아이콘(![바꾸기 아이콘](/help/main/assets/icons/Retweet.svg))을 클릭하십시오.
   1. **[!UICONTROL 대상 추가]** 대화 상자에서 [원하는 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)한 다음 **[!UICONTROL 대상 할당]**&#x200B;을 클릭합니다.

      여러 대상을 결합하는 대상을 만들려면 **[!UICONTROL 대상 결합]**&#x200B;을 클릭합니다. 자세한 내용은 [여러 대상 결합](/help/main/c-target/combining-multiple-audiences.md)을 참조하십시오.

      **[!UICONTROL 대상 라이브러리]**&#x200B;에 없는 새 대상을 만들려면 **[!UICONTROL 대상 만들기]**&#x200B;를 클릭하십시오. [대상자 만들기 워크플로](/help/main/c-target/c-audiences/audiences.md)에서 다음 옵션 중 하나를 선택하십시오.

      * **[!UICONTROL 대상 라이브러리]**: **[!UICONTROL 대상 라이브러리]**&#x200B;에 저장되고 다른 활동에서 다시 사용할 수 있는 온디맨드 대상을 만듭니다.
      * **[!UICONTROL 이 활동만]**: **[!UICONTROL 대상 라이브러리]**&#x200B;에 저장되지 않고 현재 활동에서만 사용할 수 있는 [활동별 대상을 만듭니다](/help/main/c-target/creating-activity-only-audience.md).

   1. 오른쪽 프레임에서 **[!UICONTROL 방문자 비율]**&#x200B;을 클릭한 다음 활동을 시작할 자격 있는 방문자의 비율을 선택합니다.

   +++

1. **[!UICONTROL 트래픽 할당]** 컨트롤을 클릭한 다음 오른쪽 창에서 원하는 트래픽 할당 방법을 선택합니다. 이 시나리오에서는 **[!UICONTROL 개인화된 경험에 대한 자동 타기팅]**&#x200B;을 클릭합니다.

   ![트래픽 할당 메서드 설정](/help/main/c-activities/assets/auto-target.png)

   +++ 트래픽 할당 방법

   | 방법 | 기능 |
   |---|---|
   | **[!UICONTROL 수동(기본값)]** | 각 경험을 보게 하려는 참여자의 비율을 지정합니다. 이 비율을 모든 경험 간에 균일하게 분산하거나 각 경험에 대해 시간 비율을 더 높거나 낮게 지정할 수 있습니다. 모든 경험의 합계는 100%여야 합니다. |
   | **[!UICONTROL 최고 경험에 자동 할당]** | 대부분의 활동 참여자는 자동으로 더 높은 성과를 보이는 경험으로 이동됩니다. 일부 방문자는 경험을 탐색하고 성과 동향 변화를 인식하기 위해 모든 경험에 할당됩니다. 자세한 내용은 [**[!UICONTROL 자동 할당&#x200B;]**개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)를 참조하십시오. |
   | **[!UICONTROL 개인화된 경험에 대한 자동 타겟]** | [!DNL Target]은(는) 고급 기계 학습을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별한 후, 개별 고객 프로필 및 비슷한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 조정된 경험을 제공함으로써 콘텐츠를 개인화하고 전환을 유도합니다. 자세한 내용은 [자동 타겟 개요](/help/main/c-activities/auto-target/auto-target-to-optimize.md)를 참조하십시오. |

   +++

1. 오른쪽 창에서 **[!UICONTROL 경험]**&#x200B;을 클릭한 다음 각 경험에 대해 원하는 트래픽 할당을 지정합니다.

1. 대상, 경험 선택 사항 및 트래픽 할당 선택 사항이 만족스러우면 **[!UICONTROL 다음]**&#x200B;을 클릭하여 안내가 있는 3단계 워크플로의 세 번째 단계로 이동합니다.

## 3단계: 목표 및 설정 구성 {#configure-goals-and-settings}

**[!UICONTROL 목표 및 설정]** 페이지에서 [!DNL Target]에게 활동을 측정하는 방법을 알려 줍니다. 사용 가능한 설정은 [!DNL Target] 또는 [Analytics를 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)하는지에 따라 다릅니다.

1. 활동에 대한 [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)을 지정합니다. 페이지의 섹션을 검토하고 필요한 사항을 설정합니다.

   | 섹션 | 설정한 항목 |
   |---|---|
   | **[!UICONTROL 활동 설정]** | 선택적 목표인 **[!UICONTROL 우선 순위]**(여러 활동이 위치와 대상을 공유할 때 사용) 및 **[!UICONTROL 기간]**(시작 및 종료 날짜)입니다. |
   | **[!UICONTROL 보고 설정]** | 보고 소스, 목표 지표(예: **[!UICONTROL 전환]** 지표), 추가 지표, 보고 대상 및 통계 방법론입니다. |
   | **[!UICONTROL 고급 설정]** | 성공 지표, 방문자가 목표 지표에 도달한 후 수행되는 작업과 카운트가 증가하는 방법 간의 종속성. |
   | **[!UICONTROL 기타 메타데이터]** | 귀하 또는 다른 팀 멤버에게 유용한 활동에 대한 참고 사항입니다. |

   >[!NOTE]
   >
   >이 활동에 [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)을 사용하려면 자동 할당 및 자동 타겟 활동에 대한 [A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)의 중요 정보를 참조하십시오.

1. **[!UICONTROL 저장 및 닫기]** 또는 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

활동을 만든 후 **[!UICONTROL 개요]** 탭에는 활동의 다이어그램을 포함하여 활동에 대한 정보가 표시됩니다.
