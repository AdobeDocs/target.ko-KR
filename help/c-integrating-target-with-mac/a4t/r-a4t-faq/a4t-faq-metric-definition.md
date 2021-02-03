---
keywords: faq;자주 묻는 질문;analytics for target;a4T;지표;지표 정의
description: 이 주제에서는 지표 정의와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
title: 지표 정의 - A4T FAQ
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 67%

---


# 지표 정의 - A4T FAQ

이 주제에서는 지표 정의와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## 활동 멤버십이 만료되는 시기는 언제입니까? 방문자가 활동에 참여한 후 활동이 표시되지 않을 경우 활동에서 방문자의 동작이 카운트되는 시기는 언제입니까? {#section_41B4958F33534E4B96DEE0C981227A79}

기본적으로 방문자가 마지막으로 활동과 상호 작용한 후 90일이 지나면 해당 활동이 만료됩니다. 이 기간은 필요에 따라 ClientCare에서 조정할 수 있습니다. 이 설정값은 모든 활동에 적용되지만 하나의 사례에 맞게 조정하지 않아야 합니다.

## 목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유는 무엇입니까?{#adv-settings}

[!UICONTROL 고급 설정] 옵션은 보고 소스(A4T)로 [!DNL Analytics]를 사용하는 활동에는 사용할 수 없습니다.

A4T를 사용하는 활동의 경우, 목표 지표는 항상 &quot;[!UICONTROL 활동 개수 및 사용자 유지]&quot; 및 &quot;[!UICONTROL 모든 임프레션 시]&quot; 설정을 사용합니다. 이 값은 *구성할 수 없습니다.*

A4T가 아닌 활동의 경우 [고급 설정 옵션](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B)을 사용하여 성공을 측정하는 방법을 관리할 수 있습니다. 옵션에는 종속성 추가, 사용자를 활동에 유지할지 또는 제거할지 여부 선택, 참가자당 한 번 또는 모든 임프레션에서 지표를 계산할지 여부 선택 등이 있습니다. 아래에서 보듯이, 세로 줄임표 > [!UICONTROL 고급 설정]을 클릭하여 A4T 이외의 활동에서 [!UICONTROL 고급 설정] 옵션에 액세스합니다.

![고급 설정](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

## 계산된 지표는 무엇이며 이전에 사용했던 SiteCatalyst:Event mbox를 어떻게 대체합니까? {#section_D59F4719E6B94758A2187427C17F8EF3}

계산된 지표를 사용하면 세그먼트 또는 수학 계산에서 파생되는 사용자 지정 지표를 만들 수 있습니다. 이전에는 `SiteCatlayst:Event` mbox를 사용했으며 여기서 `evar27=shoes`이고 이벤트는 `purchase`입니다. 이제는 `evar27=shoes`인 세그먼트를 만들고 이 세그먼트를 적용하여 이벤트가 `purchase`인 계산된 지표를 만듭니다. 이 방법의 이점은 활동이 진행 중이더라도 이러한 지표를 언제든지 만들 수 있다는 점입니다. 그런 다음 Analytics의 모든 보고서에서 사용할 수 있습니다.

## A4T의 전환은 여러 캠페인에서 비롯됩니까?  {#section_7F15C727206440CD86B3A8CE77087DF9}

예. 이 작업은 &quot;전체 할당&quot; 설정을 통해 수행됩니다.
