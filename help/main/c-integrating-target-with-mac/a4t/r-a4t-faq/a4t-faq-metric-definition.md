---
keywords: faq;자주 묻는 질문;analytics for target;a4T;지표;지표 정의
description: 지표 정의 및 Analytics for [!DNL Target] (A4T) 사용에 대한 질문에 대한 답변을 찾아보십시오. A4T를 사용하면 Adobe [!DNL Target] 활동에 Analytics 보고를 사용할 수 있습니다.
title: A4T를 사용하여 지표 정의에 대한 정보는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 31%

---

# 지표 정의 - A4T FAQ

이 주제에서는 지표 정의와 [!DNL Adobe Analytics]을(를) [!DNL Adobe Target] (A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## 활동 멤버십이 만료되는 시기는 언제입니까? 방문자가 활동을 입력한 후 다시 표시되지 않는 경우 활동에서 활동이 카운트되는 기간은 얼마나 됩니까? {#section_41B4958F33534E4B96DEE0C981227A79}

+++답변
활동의 기본 만료일은 방문자가 활동과 마지막 상호 작용한 후 90일입니다. 이 설정은 필요한 경우 ClientCare에서 조정할 수 있습니다. 이 설정값은 모든 활동에 적용되지만 하나의 사례에 맞게 조정하지 않아야 합니다.

+++

## 목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유는 무엇입니까? {#adv-settings}

+++답변
[!DNL Analytics]을(를) 보고 소스로 사용(A4T)하는 활동에는 [!UICONTROL Advanced Settings] 옵션을 사용할 수 없습니다.

A4T를 사용하는 활동의 경우 목표 지표는 항상 &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; 및 &quot;[!UICONTROL On Every Impression]&quot; 설정을 사용합니다. 이러한 설정은 *구성할 수 없습니다*.

비 A4T 활동의 경우 [고급 설정 옵션](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B)을 사용하여 성공 측정 방법을 관리할 수 있습니다. 옵션에는 종속성 추가, 활동에 사용자를 유지할지 또는 제거할지 선택, 참가자 당 한 번 또는 노출 시마다 지표를 계산할지 여부가 포함됩니다. 아래와 같이 A4T가 아닌 활동에서 수직 줄임표 > [!UICONTROL Advanced Settings]을(를) 클릭하여 [!UICONTROL Advanced Settings] 옵션에 액세스합니다.

![고급 설정](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## 계산된 지표는 무엇이며 이전에 사용했던 SiteCatalyst:Event mbox를 어떻게 대체합니까? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++답변
계산된 지표를 사용하면 세그먼트 또는 수학 계산에서 파생된 사용자 지정 지표를 만들 수 있습니다. 이전에는 `SiteCatlayst:Event` mbox를 사용했으며 여기서 `evar27=shoes`이고 이벤트는 `purchase`입니다. 이제는 `evar27=shoes`인 세그먼트를 만들고 이 세그먼트를 적용하여 이벤트가 `purchase`인 계산된 지표를 만듭니다. 이러한 지표는 활동이 진행 중인 후에도 언제든지 만들 수 있습니다. 그런 다음 Analytics의 모든 보고서에서 사용할 수 있습니다.

+++

## A4T의 전환은 여러 캠페인에서 비롯됩니까? {#section_7F15C727206440CD86B3A8CE77087DF9}

+++답변
예. &quot;전체 할당&quot; 설정을 사용합니다.

+++