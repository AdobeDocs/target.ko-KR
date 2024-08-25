---
keywords: 목표 및 설정;목표;우선순위;지속 기간
description: ' [!DNL Target]  Adobe에서 활동 설정을 사용하여 활동의 목표, 우선 순위 및 기간을 관리하는 방법을 알아봅니다.'
title: 활동 설정을 지정하는 방법
feature: Activities
exl-id: 7f34080b-d2ed-4fe5-80ff-3aba16961223
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 74%

---

# 활동 설정

[!DNL Adobe Target]의 [!UICONTROL Activity Settings]을(를) 사용하여 활동의 목표, 우선 순위 및 기간을 관리하십시오.

1. 활동의 목표에 대한 메모를 입력합니다.

   본인 또는 다른 팀 구성원이 쉽게 사용할 수 있도록 본인의 활동에 대한 정보를 입력합니다. [!UICONTROL Objective] 필드의 크기를 조정하려면 끕니다.
1. 활동 우선순위를 설정합니다.

   설정에 따라 [!UICONTROL Priority]의 UI 및 옵션이 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다.

   대상자가 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.

   이 옵션이 [!UICONTROL Administration] > [!UICONTROL Reporting](기본값)에서 활성화되지 않으면 우선순위를 낮음, Medium 또는 높음으로 지정하십시오.

   세분화된 우선 순위를 사용하려면 [!UICONTROL Administration] > [!UICONTROL Reporting]을(를) 클릭한 다음 [!UICONTROL Enable Fine-Grained Priorities] 옵션을 &quot;켜기&quot; 위치로 전환하십시오.

   이 옵션이 활성화되면 0에서 999 사이의 값을 지정하십시오.

   * 0 = 낮음
   * 999 = 높음

   이전 버전의 [!DNL Target Standard/Premium]에서 만든 활동의 경우, 낮음 우선순위는 0으로, 중간은 5로, 높음은 10으로 전환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.

   >[!NOTE]
   >
   >세분화된 우선순위를 사용한 후에 이 선택 사항을 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다.

1. 활동의 지속 기간을 설정하십시오.

   활동을 수동으로 활성화 및 비활성화하거나 활동 전달을 위한 날짜 및 시간을 지정할 수 있습니다. 시간 컨트롤은 24시간 형식을 사용하며 00:00은 자정을 나타냅니다. 해당 시간대는 브라우저에 구성된 시간대로 설정됩니다. 다른 시간대를 사용하려면 브라우저를 다른 시간대로 설정하고 브라우저를 다시 시작하십시오.

   >[!NOTE]
   >
   >활동을 스케줄링하여 활동의 전달 시간대를 제어합니다. 그러나 활동을 지정된 스케줄에 따라 전달하려면 먼저 활동을 명시적으로 활성화해야 합니다.

[!UICONTROL Goal & Settings] 페이지에는 만들고 있는 활동 유형에 따라 달라지는 추가 설정이 포함되어 있습니다. 이러한 설정에 대한 자세한 내용은 다음 활동 유형을 참조하십시오.

* [A/B 테스트](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [자동화된 개인화](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [경험 타깃팅](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [다변량 테스트](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Recommendations](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## 교육 비디오: 활동 설정 ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 활동 설정에 대한 정보가 포함되어 있습니다.

* 활동의 목표 입력
* 활동의 우선순위 수준 설정
* 활동 시작 및 종료 시간 예약
* 보고서 필터를 작성하기 위해 보고 대상 추가
* 활동에 대한 메모 입력

  >[!VIDEO](https://video.tv.adobe.com/v/17381)
