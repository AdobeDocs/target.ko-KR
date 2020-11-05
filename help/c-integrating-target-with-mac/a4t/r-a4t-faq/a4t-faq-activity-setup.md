---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: 이 주제에서는 활동 설정과 Analytics를 Target의 보고 소스로 사용(A4T)하는 것과 관련하여 자주 묻는 질문에 대한 답을 제공합니다.
title: 활동 설정 - A4T FAQ
feature: a4t troubleshooting
topic: Standard
uuid: 3472ab3c-908b-40f8-81a6-512dccde64a6
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 89%

---


# 활동 설정 - A4T FAQ{#activity-settings-a-t-faq}

이 주제에서는 활동 설정과 Analytics를 Target의 보고 소스로 사용(A4T)하는 것과 관련하여 자주 묻는 질문에 대한 답을 제공합니다.

## 어느 활동 유형이 보고 소스로서 Analytics(A4T)를 지원합니까?{#section_5E4F58CD25A5424E869E6FE0803968EF}

전체 목록이 필요하면 [Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE)에서 &quot;지원되는 활동 유형&quot;을 참조하십시오.

## 방금 활동을 만들었습니다. 수신되는 데이터가 표시되지 않는 이유는 무엇입니까? {#section_9F8092BE4225442896F926540292F221}

활동이 만들어지면 Target은 Analytics에 분류 파일을 보냅니다. Analytics가 데이터를 캡처하고 처리하지만 분류 파일이 업데이트될 때까지는 보고서에 해당 데이터가 표시되지 않습니다. 데이터가 표시되려면 24시간이 걸릴 수 있습니다. 48시간 후에도 데이터가 표시되지 않으면 [Client Care에 문의](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)하십시오. 또는 활동을 실행할 시기를 알고 있는 경우 며칠 전에 활동을 미리 만들면 활동이 저장될 때 분류가 전송됩니다. 이렇게 하면 활동이 실행될 때 데이터가 보고서에 표시됩니다. Analytics에서 데이터가 처리되려면 45-90분이 소요됩니다.

## 새 활동을 만들 때 Analytics를 보고 소스로 선택할 수 없는 이유는 무엇입니까? {#section_9F4F69C3085F4C2480AF439127EB27CD}

관리에서 보고 설정 옵션을 변경할 수 있습니다.

1. In Adobe Target, click **[!UICONTROL Administration]**.
1. **[!UICONTROL 보고에 사용된 Experience Cloud 솔루션]** 드롭다운 목록에서 **[!UICONTROL 활동당 선택]**&#x200B;을 클릭합니다.

![](assets/select-per-activity.png)

**[!UICONTROL 보고 소스]** 드롭다운 목록이 **[!UICONTROL 목표 및 설정 화면에서 활성화되어 활동을 만들고 편집할 수 있습니다.]**

To always use Analytics as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in Administration.
