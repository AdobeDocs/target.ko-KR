---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: 이 주제에서는 활동 설정과 Analytics를 Target의 보고 소스로 사용(A4T)하는 것과 관련하여 자주 묻는 질문에 대한 답을 제공합니다.
title: 활동 설정 - A4T FAQ
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 208196b8c0cf11367ad37121c4792a015b396dc7
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 35%

---


# 활동 설정 - A4T FAQ

This topic contains answers to questions that are frequently asked about activity setup and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## 어느 활동 유형이 보고 소스로서 Analytics(A4T)를 지원합니까?{#section_5E4F58CD25A5424E869E6FE0803968EF}

전체 목록이 필요하면 [Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE)에서 &quot;지원되는 활동 유형&quot;을 참조하십시오.

## 방금 활동을 만들었습니다. 수신되는 데이터가 표시되지 않는 이유는 무엇입니까? {#section_9F8092BE4225442896F926540292F221}

When an activity is created, [!DNL Target] sends a classification file to [!DNL Analytics]. Although [!DNL Analytics] is capturing the and processing the data, it does not show in the reports until the classification file has been updated. 데이터가 표시되려면 24시간이 걸릴 수 있습니다. 48시간 후에도 데이터가 표시되지 않으면 [Client Care에 문의](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)하십시오. 또는 활동을 실행할 시기를 알고 있는 경우 며칠 전에 활동을 미리 만들면 활동이 저장될 때 분류가 전송됩니다. 이렇게 하면 활동이 실행될 때 데이터가 보고서에 표시됩니다. Please note that it takes 45-90 minutes for data to be processed in [!DNL Analytics].

## 새 활동을 만들 때 Analytics를 보고 소스로 선택할 수 없는 이유는 무엇입니까? {#section_9F4F69C3085F4C2480AF439127EB27CD}

You can change your [!UICONTROL Reporting Settings] options in [!UICONTROL Administration].

1. 에서 [관리] [!DNL Target]를 **[!UICONTROL 클릭합니다]**.
1. **[!UICONTROL 보고에 사용된 Experience Cloud 솔루션]** 드롭다운 목록에서 **[!UICONTROL 활동당 선택]**&#x200B;을 클릭합니다.

![](assets/select-per-activity.png)

**[!UICONTROL 보고 소스]** 드롭다운 목록이 **[!UICONTROL 목표 및 설정 화면에서 활성화되어 활동을 만들고 편집할 수 있습니다.]**

To always use [!DNL Analytics] as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in [!UICONTROL Administration].

## 방문자가 A4T를 사용하는 자동 Target 활동에서 서로 다른 방문에서 타깃팅된 경험과 제어된 경험 간을 전환할 수 있습니까?

visitorId가 방문 간 방문자에 대해 변경되지 않는다고 가정할 때 다음 사항이 적용됩니다.

트래픽 할당 비율이 중간 활동을 조정하면 방문자가 타깃팅된 경험과 제어 경험 간에 이동할 수 있습니다.

비율이 중간 활동을 조정하지 않으면 처음에 컨트롤을 본 방문자가 항상 제어하도록 전송됩니다. 타깃팅된 경험으로 전송되는 방문자는 항상 타깃팅된 경험으로 전송됩니다.

* 트래픽의 타깃팅된 &quot;버킷&quot;에 참여한 후, 기계 학습 모델에서 새 방문에 대해 다른 경험이 적절하다고 판단하는 경우 방문자를 방문에서 방문으로 다른 경험으로 보낼 수 있습니다.
* 경험 할당은 방문자 visitorId의 결정적 의사 임의 해시를 기반으로 하므로 트래픽의 &quot;버킷&quot; 컨트롤에 할당되면 방문자는 항상 동일한 경험을 보게 됩니다.

## 모델이 빌드될 때까지 90(Control)/10(Targeted) 분할이 있는 자동 Target 및 A4T에 사용자 정의 모델을 사용하는 것이 권장됩니까?

최적의 트래픽 할당은 달성하고자 하는 사항에 따라 달라집니다.

가능한 많은 트래픽을 개인화하는 것이 목표인 경우 활동의 평생 동안 90%의 타깃팅과 10%의 제어를 유지할 수 있습니다. 사용자 지정 알고리즘과 컨트롤의 효과를 비교하는 실험을 실행하는 것이 목표인 경우 50/50 분할이 가장 적합합니다.

