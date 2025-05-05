---
keywords: faq;자주 묻는 질문;analytics for target;a4T;활동 설정
description: Analytics for [!DNL Target] (A4T)을(를) 사용할 때 활동 설정에 대한 질문에 대한 답변을 찾아보십시오. A4T를 사용하면  [!DNL Target] 활동에 대한 Analytics 보고를 사용할 수 있습니다.
title: A4T의 활동 설정에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 6%

---

# 활동 설정 - A4T FAQ

이 주제에서는 활동 설정과 [!DNL Analytics]을(를) [!DNL Target] (A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## 보고 소스로 [!DNL Analytics]을(를) 지원하는 활동 유형(A4T)은 무엇입니까? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++답변
전체 목록이 필요하면 [Adobe Analytics as the Reporting Source for Adobe Target(A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE)의 &quot;지원되는 활동 유형&quot;을 참조하십시오.

+++

## A4T 보고를 사용할 때 별도의 작업 공간에서 두 활동에 대해 동일한 활동 이름을 사용할 수 있습니까?

+++답변

A4T 보고를 사용하는 별도의 [작업 영역](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)의 두 활동에 동일한 활동 이름을 사용하지 마십시오.

[!DNL Target]을(를) 보고 소스로 사용하는 경우에는 이 기능이 지원되지만 [!UICONTROL Analytics for Target]을(를) 보고 소스로 사용하는 경우에는 두 활동에 동일한 활동 이름을 사용할 수 없습니다.

+++

## 목표 지표를 구성하는 동안 고급 설정에 액세스할 수 없는 이유는 무엇입니까?

+++답변
[!DNL Analytics]을(를) 보고 소스로 사용(A4T)하는 활동의 경우 목표 지표는 &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; 및 &quot;[!UICONTROL On Every Impression]&quot; 설정을 사용합니다. 이러한 설정은 *구성할 수 없습니다*.

자세한 내용은 &quot;목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유는 무엇입니까?&quot;를 참조하십시오. [지표 정의 - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md)에서.

+++

## 방금 활동을 만들었습니다. 수신되는 데이터가 표시되지 않는 이유는 무엇입니까? {#section_9F8092BE4225442896F926540292F221}


+++답변
활동이 만들어지면 [!DNL Target]에서 [!DNL Analytics] (으)로 분류 파일을 보냅니다. [!DNL Analytics]이(가) 데이터를 캡처하고 처리 중이지만 분류 파일이 업데이트될 때까지 보고서에 표시되지 않습니다. 이 프로세스를 완료하는 데 24~72시간이 걸릴 수 있습니다. 72시간 후에도 데이터가 표시되지 않으면 [Client Care에 문의](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)하세요. 또는 활동을 시작하는 것을 알고 있는 경우 며칠 전에 활동을 만들 수 있으며 활동이 저장되면 분류가 전송됩니다. 이렇게 하면 활동이 실행될 때 데이터가 보고서에 표시됩니다. [!DNL Analytics]에서 데이터를 처리하는 데 45~90분이 소요됩니다.

+++

## 활동을 만들 때 Analytics를 보고 소스로 선택할 수 없는 이유는 무엇입니까? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++답변
[!UICONTROL Administration]에서 [!UICONTROL Reporting Settings] 옵션을 변경할 수 있습니다.

1. [!DNL Target]에서 **[!UICONTROL Administration]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Experience Cloud solution used for reporting]** 드롭다운 목록에서 **[!UICONTROL Select per Activity]**&#x200B;을(를) 클릭합니다.

![활동당 이미지 선택](assets/select-per-activity.png)

**[!UICONTROL Goal & Settings]** 화면에서 **[!UICONTROL Reporting Source]** 드롭다운 목록을 사용하여 활동을 만들고 편집할 수 있습니다.

항상 [!DNL Analytics]을(를) 보고 소스로 사용하려면 [!UICONTROL Administration]의 드롭다운 목록에서 **[!UICONTROL Adobe Analytics]**&#x200B;을(를) 선택하십시오.

+++

## A4T를 사용하는 자동 타겟 활동의 여러 방문에서 방문자가 타겟팅과 통제 경험 사이를 전환할 수 있습니까?

+++답변
다음은 visitorId가 방문 사이에 방문자에 대해 변경되지 않는다는 가정 하에 true입니다.

활동 중간에 트래픽 할당 비율을 조정하면 방문자가 타겟팅된 경험과 제어 경험 사이를 이동할 수 있습니다.

백분율이 활동 중간에 조정되지 않으면 처음에 컨트롤을 본 방문자가 항상 컨트롤로 전송됩니다. 타겟팅된 경험으로 전송되는 방문자는 항상 타겟팅된 경험으로 전송됩니다.

* 트래픽의 타겟팅된 &quot;버킷&quot;에 있었던 방문자는 머신 러닝 모델에서 다른 경험이 새 방문과 관련이 있다고 판단되면 방문자가 방문과는 다른 경험으로 보내질 수 있습니다.
* 트래픽의 제어 &quot;버킷&quot;에 할당된 후 경험 할당은 방문자의 visitorId의 결정론적 의사 무작위 해시를 기반으로 하므로 방문자는 항상 동일한 경험을 보게 됩니다.

+++

## [!UICONTROL Auto-Allocate] 활동의 최적화 목표로 적용된 세그먼트로 이항 [!DNL Analytics] 지표를 사용할 수 있습니까? {#binomial}

+++답변
[!UICONTROL Auto-Allocate] 활동의 최적화 목표로 적용된 세그먼트에는 [!DNL Analytics] 지표를 사용할 수 없습니다. 해결 방법으로, 동일한 목표를 달성하는 사용자 정의 이벤트를 정의하고 이 이벤트를 최적화 목표 지표로 사용할 수 있습니다.

+++