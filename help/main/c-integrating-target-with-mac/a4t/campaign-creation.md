---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe에서 활동을 구성하는 방법을 알아봅니다 [!DNL Target] 에서는 Adobe Analytics을 보고 소스로 사용(A4T)합니다.
title: A4T를 사용하는 활동을 만들려면 어떻게 합니까?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 36%

---

# Analytics를 보고 소스로 사용하는 활동 만들기

에서 활동을 구성할 수 있습니다 [!DNL Adobe Target] 를 [!DNL Adobe Analytics] 를 보고 소스로 사용(A4T)합니다.

를 사용하는 활동을 설정하기 전에 [!DNL Analytics] 보고 소스로서 방문자당 매출(RPV) 향상 또는 장바구니 클릭 수와 같은 활동에 대한 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. 그러나 언제든지 지표를 더 선택할 수 있습니다 [!DNL Analytics], 이 테스트가 영향을 줄 것으로 예상되는 특정 지표를 여전히 지정해야 합니다.

## 활동을 만듭니다

만들기 [!DNL Target] 를 사용하는 활동 [!DNL Analytics] 보고 소스는 일반 [!DNL Target] 활동. 몇 가지 중요한 차이점이 있습니다. 예를 들어에서 사용할 수 있는 모든 세그먼트가 있으므로 활동을 만드는 동안 보고할 세그먼트를 선택할 수 없습니다 [!DNL Analytics] 보고서를 볼 때 적용할 수 있습니다.

1. **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >활동 이름에는 &quot;%&quot; 문자를 포함할 수 없습니다. [!DNL Analytics] 를 보고 소스로 사용합니다.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.

   을(를) 만들려면 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target] 활동: [A4T에서 자동 할당 및 자동 Target 활동을 지원합니다](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) 추가 정보.

1. 활동 만들기 흐름의 **[!UICONTROL 설정]** 부분으로 이동되면 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택하고 회사를 지정합니다.
1. 보고서 세트를 선택합니다.

   에서 사용할 수 있는 보고서 세트를 선택할 수 있습니다 [!DNL Analytics]. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 정의합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.

      다음 문서를 확인하십시오. [!DNL Analytics] 회사입니다. 만약 [!DNL Adobe Experience Cloud] 계정이 두 개 이상에 연결되어 있습니다. [!DNL Analytics] 회사, 로그아웃됨 [!DNL Target], 및에 로그인합니다. [!DNL Analytics] 적절한 회사에서 그런 다음 로 돌아갑니다. [!DNL Target], 및 보고서 세트가 로드됩니다.

   * 예상한 보고서 세트가 표시되지 않습니다.

      연결할 보고서 세트만 제공됩니다 [!DNL Target] 을 선택할 수 있습니다. 예상한 보고서 세트가 표시되지 않으면 먼저 로그아웃한 후 다시 로그인하십시오 [!DNL Adobe Experience Cloud] 다시 시도하십시오.
   목록에서 하나 이상의 보고서 세트가 여전히 누락된 경우 [고객 지원 센터에 문의하십시오](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다.
1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. 원하는 항목을 선택할 수 있습니다 [!DNL Analytics] 다음에서 사용할 수 있는 지표 [!DNL Analytics] 지표 선택기.

   >[!NOTE]
   >
   >사용자 지정 Target 기반 지표를에 보낼 수 있습니다 [!DNL Analytics] 단지 [!DNL Analytics] 데이터. 예를 들어, 일반적으로 추적되지 않는 페이지 클릭을 모니터링할 수 있습니다 [!DNL Analytics]. 이 사용자 지정 지표는 로 전송됩니다 [!DNL Analytics] 에서 자동으로 [!DNL Target] server, 그리고 이 &quot;[!DNL Target] 의 지표 선택기에서 전환&quot; 지표 [!DNL Analytics]. 다음 [!DNL Target] 을 사용하도록 선택하면 전환 지표가 비어 있습니다 [!DNL Analytics] 지표 를 참조하십시오.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 콘텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >설정 후 활동을 설정할 때 [!DNL Analytics] 보고 소스로서 보고 대상을 설정할 수 있는 선택 사항이 없습니다. [!DNL Analytics] 세그먼트는 [!DNL Target] 활동 보고서.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## A4T 및 자동 할당 및 자동 Target 활동

자세한 내용은 [자동 할당 및 자동 타겟 활동에 대한 A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오.
