---
keywords: 타깃팅;analytics;추적 서버;analytics for target;a4t
description: '[!DNL Adobe Analytics]을(를) 보고 원본(A4T)으로 사용하도록 [!DNL Adobe Target]에서 활동을 구성하는 방법에 대해 알아봅니다.'
title: '[!DNL Target]에서 [!DNL Analytics] 데이터를 사용하려면 어떻게 해야 합니까?'
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
TQID: 'https://experienceleague.adobe.com/x38YsYI4a6-92oOr6Fs3RfKrJHbSaLNj0cki5CInPPg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 891742a5-242d-5099-966a-ca76c17cd2d2
    internal-label: Analytics for Target (A4T)
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%
---
# [!DNL Adobe Analytics] 데이터 사용 중 {#create-a4t}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Analytics]을(를) 보고 원본(A4T)으로 사용하도록 활동을 구성하는 방법, 시작하기 전에 준비하는 방법, 활동의 목표를 선택하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

Analytics for Target(A4T)은 [!DNL Adobe Analytics]의 데이터 및 지표를 사용하여 [!DNL Adobe Target] 활동 결과를 측정합니다. A4T를 사용하려면 [!DNL Analytics]이(가) 해당 보고 소스가 되도록 활동을 구성하십시오. [!DNL Target]의 데이터 소스로 [!DNL Analytics]을(를) 설정하는 방법에 대한 자세한 내용은 [Adobe Target의 보고 Source으로 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을(를) 참조하십시오.

## 시작하기 전에 {#before-you-begin}

>[!NOTE]
>
>**[!UICONTROL Adobe Analytics]** 옵션은 [!DNL Adobe Experience Cloud] 계정이 [!DNL Analytics]과(와) [!DNL Target] 모두에 연결되어 있을 때 사용할 수 있습니다. 계정에 대해 [!DNL Target]과(와) [!DNL Analytics] 간의 통합이 설정되지 않은 경우에도 사용할 수 있습니다.

활동을 만들기 전에 예를 들어 방문자당 매출(RPV) 향상 또는 장바구니로의 클릭 수 증가를 목표로 설정합니다. 그런 다음 이 목표를 측정하는 최종 성공 지표를 선택합니다. [!DNL Analytics]에서 언제든지 추가 지표를 선택할 수 있지만 이 테스트가 영향을 줄 것으로 예상되는 지표를 지정해야 합니다.

## Analytics를 보고 소스로 선택 {#select-reporting-source}

>[!NOTE]
>
>at.js 버전 0.9.1 이상을 사용하는 경우 [!DNL Adobe Analytics]을(를) 보고 소스로 사용하는 활동을 만들 때 추적 서버를 지정할 필요가 없습니다. at.js 라이브러리는 추적 서버 값을 [!DNL Target]에 자동으로 보냅니다. **[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 추적 서버]** 필드는 비어 있을 수 있습니다.

활동의 **[!UICONTROL 목표 및 설정]** 페이지에서 보고 소스가 선택됩니다. 이 페이지에서 [!DNL Target] 활동 데이터를 받는 [!DNL Analytics] 회사와 보고서 세트를 선택하고 추적 서버를 확인합니다.

➡️ 단계, 보고서 세트 요구 사항 및 추적 서버 세부 정보는 [Source 보고](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source)를 참조하십시오.

[!DNL Analytics]이(가) 보고 소스인 경우 이 활동에서는 보고 대상을 설정할 수 있는 옵션을 제공하지 않습니다. [!DNL Analytics] 세그먼트는 대신 [!DNL Target] **[!UICONTROL 활동]** 보고서에서 사용할 수 있습니다.

## 활동의 목표 설정 {#set-goal}

각 활동의 목표에는 성공 지표가 필요합니다. 목표는 성공적인 활동을 알리는 전환 활동입니다. [!DNL Analytics] 지표 선택기에서 사용할 수 있는 모든 지표를 사용할 수 있습니다. 특정 방식으로 개선하려는 목표 없이 테스트를 실행하지 않는 것이 좋습니다.

목표를 설정한다고 해서 테스트 결과를 평가하기 위해 다른 지표를 사용하는 것을 막을 수는 없습니다. 그러나 이 목표는 테스트를 통해 개선하려는 한 가지 사항을 식별합니다.

방문자가 목표를 완료한 후에는 해당 방문자는 더 이상 활동에 포함되지 않습니다. 활동을 완료한 후 방문자가 다시 활동을 시작하면 해당 방문자는 새 방문자로 계산됩니다.
