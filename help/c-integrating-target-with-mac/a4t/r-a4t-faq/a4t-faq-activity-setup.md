---
keywords: faq;자주 묻는 질문;analytics for target;a4T;활동 설정
description: Analytics for [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] 활동을 사용할 때 활동 설정에 대한 질문에 대한 답변을 찾으십시오.
title: A4T를 사용하는 활동 설정에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 15ca5e92af5ebc66caa52ffc1dc04e1fbcbb2ed3
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 20%

---

# 활동 설정 - A4T FAQ

이 주제에서는 활동 설정과 [!DNL Analytics] 을 [!DNL Target](A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## 어느 활동 유형이 보고 소스로서 Analytics(A4T)를 지원합니까? {#section_5E4F58CD25A5424E869E6FE0803968EF}

전체 목록이 필요하면 [Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE)에서 &quot;지원되는 활동 유형&quot;을 참조하십시오.

## 목표 지표를 구성하는 동안 고급 설정에 액세스할 수 없는 이유는 무엇입니까?

[!DNL Analytics]을 보고 소스(A4T)로 사용하는 활동의 경우, 목표 지표는 &quot;[!UICONTROL 증분 카운트 및 사용자를 활동]&quot; 및 &quot;[!UICONTROL 모든 노출 시]&quot; 설정을 사용합니다. 이러한 설정은 *구성할 수 없습니다*.

자세한 내용은 &quot;목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유&quot;를 참조하십시오. [지표 정의 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md)에 있습니다.

## 방금 활동을 만들었습니다. 수신되는 데이터가 표시되지 않는 이유는 무엇입니까? {#section_9F8092BE4225442896F926540292F221}

활동이 만들어지면 [!DNL Target]이(가) 분류 파일을 [!DNL Analytics]에 보냅니다. [!DNL Analytics] 은 데이터를 캡처하고 처리하고 있지만 분류 파일이 업데이트되기 전까지는 보고서에 표시되지 않습니다. 이 프로세스는 최대 24시간이 걸릴 수 있습니다. 48시간 후에도 데이터가 표시되지 않으면 [Client Care에 문의](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)하십시오. 또는 활동을 시작하는 것을 알고 있는 경우, 며칠 전에 활동을 만들 수 있으며 활동을 저장할 때 분류가 전송됩니다. 이렇게 하면 활동이 실행될 때 데이터가 보고서에 표시됩니다. [!DNL Analytics]에서 데이터를 처리하는 데 45-90분이 소요됩니다.

## 활동을 만들 때 Analytics를 보고 소스로 선택할 수 없는 이유는 무엇입니까? {#section_9F4F69C3085F4C2480AF439127EB27CD}

[!UICONTROL 관리]에서 [!UICONTROL 보고 설정] 옵션을 변경할 수 있습니다.

1. [!DNL Target]에서 **[!UICONTROL 관리]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 보고에 사용된 Experience Cloud 솔루션]** 드롭다운 목록에서 **[!UICONTROL 활동당 선택]**&#x200B;을 클릭합니다.

![](assets/select-per-activity.png)

**[!UICONTROL 보고 소스]** 드롭다운 목록이 **[!UICONTROL 목표 및 설정 화면에서 활성화되어 활동을 만들고 편집할 수 있습니다.]**

항상 [!DNL Analytics]을 보고 소스로 사용하려면 [!UICONTROL 관리]의 드롭다운 목록에서 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택하십시오.

## 방문자가 A4T를 사용하는 자동 Target 활동에서 서로 다른 방문에서 타깃팅된 경험과 제어된 경험 간을 전환할 수 있습니까?

방문 간 방문자에 대해 visitorId가 변경되지 않는다고 가정할 때 다음 사항이 적용됩니다.

트래픽 할당 비율이 중간 활동에서 조정되면 방문자가 타깃팅된 경험과 제어 경험 간에 이동할 수 있습니다.

백분율이 중간 활동에서 조정되지 않으면 처음에 컨트롤을 본 방문자는 항상 제어하도록 전송됩니다. 타깃팅된 경험으로 전송되는 방문자는 항상 타깃팅된 경험으로 전송됩니다.

* 트래픽의 타깃팅된 &quot;버킷&quot;에 있었던 후 기계 학습 모델이 새 방문에 대해 다른 경험이 관련성이 있다고 판단하는 경우 방문자를 방문과 다른 경험으로 보낼 수 있습니다.
* 트래픽 &quot;버킷&quot; 제어에 할당되면 경험 할당은 방문자 visitorId의 결정론적 의사 랜덤 해시를 기반으로 하므로 방문자는 항상 동일한 경험을 보게 됩니다.


## [!UICONTROL 자동 할당] 활동에서 최적화 목표로 세그먼트가 적용된 쌍방향 [!DNL Analytics] 지표를 사용할 수 있습니까? {#binomial}

[!UICONTROL 자동 할당] 활동에서 최적화 목표로 세그먼트가 적용된 상태로 [!DNL Analytics] 지표를 사용할 수 없습니다. 해결 방법으로 동일한 목표를 달성하고 목표 지표와 함께 사용하는 사용자 지정 이벤트를 정의할 수 있습니다.