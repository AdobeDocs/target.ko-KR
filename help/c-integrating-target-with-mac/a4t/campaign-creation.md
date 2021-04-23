---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe Analytics을 보고 소스(A4T)로 사용하는 Adobe [!DNL Target] 에서 활동을 구성하는 방법을 알아봅니다.
title: A4T를 사용하는 활동을 만들려면 어떻게 합니까?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 33%

---

# Analytics를 보고 소스로 사용하는 활동 만들기

[!DNL Adobe Target]에서 [!DNL Adobe Analytics]을 보고 소스(A4T)로 사용하도록 활동을 구성할 수 있습니다.

보고 소스로 [!DNL Analytics]을(를) 사용하는 활동을 설정하기 전에 방문자당 매출 향상(RPV) 또는 장바구니 클릭 수 증가 등 활동의 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. [!DNL Analytics]에서 언제든지 지표를 더 선택할 수 있지만 이 테스트가 영향을 줄 것으로 예상하는 특정 지표를 지정해야 합니다.

## 활동을 만듭니다

보고 소스로 [!DNL Analytics]을 사용하는 [!DNL Target] 활동을 만드는 것은 몇 가지 중요한 차이점과 함께 일반 [!DNL Target] 활동 설정과 비슷합니다. 예를 들어 활동을 만드는 동안 보고용 세그먼트를 선택할 수 없습니다. 보고서를 볼 때 [!DNL Analytics]에서 사용할 수 있는 모든 세그먼트를 적용할 수 있기 때문입니다.

1. **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Analytics]이(가) 보고 소스로 사용되는 경우 활동 이름은 &quot;%&quot; 문자를 포함할 수 없습니다.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.

   [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target] 활동을 만들려면 [자동 할당 및 자동 Target 활동에 대한 A4T 지원](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오.

1. 활동 만들기 흐름의 **[!UICONTROL 설정]** 부분으로 이동되면 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택하고 회사를 지정합니다.
1. 보고서 세트를 선택합니다.

   [!DNL Analytics]에서 사용할 수 있는 모든 보고서 세트를 선택할 수 있습니다. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 정의합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.

      [!DNL Analytics] 회사를 확인하십시오. [!DNL Adobe Experience Cloud] 계정이 둘 이상의 [!DNL Analytics] 회사에 연결되어 있으면 [!DNL Target]에서 로그아웃하고 올바른 회사 아래의 [!DNL Analytics]에 로그인합니다. 그런 다음 [!DNL Target]으로 돌아오면 보고서 세트가 로드됩니다.

   * 예상한 보고서 세트가 표시되지 않습니다.

      [!DNL Target]에 연결하도록 제공된 보고서 세트만 선택할 수 있습니다. 원하는 보고서 세트가 표시되지 않으면 먼저 [!DNL Adobe Experience Cloud]에서 로그아웃했다가 다시 로그인하여 다시 시도하십시오.
   목록에 하나 이상의 보고서 세트가 여전히 없는 경우 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다.
1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. [!DNL Analytics] 지표 선택기에서 사용할 수 있는 [!DNL Analytics] 지표를 선택할 수 있습니다.

   >[!NOTE]
   >
   >[!DNL Analytics] 데이터에만 의존하지 않고 사용자 지정 Target 기반 지표를 [!DNL Analytics]에 보낼 수 있습니다. 예를 들어 일반적으로 [!DNL Analytics]에 의해 추적되지 않는 페이지 클릭을 모니터링할 수 있습니다. 이 사용자 지정 지표는 [!DNL Target] 서버에서 자동으로 [!DNL Analytics]으로 전송되고 [!DNL Analytics]의 지표 선택기에 &quot;[!DNL Target] 전환&quot; 지표로 나타납니다. [!DNL Analytics] 지표를 사용하도록 선택하면 [!DNL Target] 전환 지표가 비어 있습니다.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 콘텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >[!DNL Analytics]을(를) 보고 소스로 설정한 후 활동을 설정할 때 보고 대상을 설정하는 옵션이 없습니다. [!DNL Analytics] 세그먼트는  [!DNL Target] 활동 보고서에서 사용할 수 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## A4T 및 자동 할당 및 자동 Target 활동

자세한 내용은 [자동 할당 및 자동 Target 활동에 대한 A4T 지원](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오.
