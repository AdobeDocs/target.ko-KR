---
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
description: Adobe에서 활동을 구성하는 방법 알아보기 [!DNL Target] Adobe Analytics을 보고 소스(A4T)로 사용합니다.
title: A4T를 사용하는 활동을 만들려면 어떻게 해야 합니까?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 30%

---

# Analytics를 보고 소스로 사용하는 활동 만들기

에서 활동을 구성할 수 있습니다. [!DNL Adobe Target] 사용 [!DNL Adobe Analytics] 를 보고 소스 (A4T) 로 사용하십시오.

을 사용하는 활동을 설정하기 전에 [!DNL Analytics] 보고 소스로 RPV(방문자당 매출) 향상 또는 장바구니 클릭 수 증가와 같은 활동에 대한 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. 다음 위치에서 언제든지 더 많은 지표를 선택할 수 있지만 [!DNL Analytics], 이 테스트가 영향을 미칠 것으로 예상하는 특정 지표를 계속 지정해야 합니다.

## 활동 만들기

만들기 [!DNL Target] 을 사용하는 활동 [!DNL Analytics] 보고 소스는 일반 설정 과 유사합니다 [!DNL Target] 활동(몇 가지 중요한 차이점이 있음) 예를 들어에서 사용할 수 있는 모든 세그먼트가 포함되어 있으므로 활동을 만드는 동안 보고할 세그먼트를 선택할 수 없습니다 [!DNL Analytics] 보고서를 볼 때 적용할 수 있습니다.

1. **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >다음과 같은 경우 활동 이름에 &quot;%&quot; 문자를 포함할 수 없습니다. [!DNL Analytics] 를 보고 소스로 사용합니다.
   >
   >별도의 두 활동에 동일한 활동 이름을 사용하지 마십시오 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) A4T 보고를 사용 중입니다.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.

   다음을 만들려면 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 타기팅] 활동, 참조 [자동 할당 및 자동 타겟 활동에 대한 A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) 추가 정보.

1. 에 도착하면 **[!UICONTROL 설정]** 활동 만들기 흐름의 일부에서 **[!UICONTROL Adobe Analytics]** 회사를 지정하십시오.
1. 보고서 세트를 선택합니다.

   에서 사용할 수 있는 모든 보고서 세트를 선택할 수 있습니다. [!DNL Analytics]. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 정의합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.

     다음을 확인: [!DNL Analytics] 회사. 다음의 경우 [!DNL Adobe Experience Cloud] 계정이 두 개 이상에 연결되어 있습니다. [!DNL Analytics] 회사, 로그아웃 [!DNL Target], 및에 로그인합니다 [!DNL Analytics] 알맞은 회사 아래에. 다음으로 돌아가기: [!DNL Target]및 보고서 세트가 로드됩니다.

   * 예상한 보고서 세트가 표시되지 않습니다.

     연결할 수 있도록 프로비저닝된 보고서 세트만 [!DNL Target] 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 다음에 다시 로그인하십시오 [!DNL Adobe Experience Cloud] 다시 시도하십시오.

   하나 이상의 보고서 세트가 여전히 목록에서 누락된 경우 [고객 지원 센터 문의](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다.
1. 활동 목표를 지정합니다.

   각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. 다음 중 하나를 선택할 수 있습니다. [!DNL Analytics] 에서 사용 가능한 지표 [!DNL Analytics] 지표 선택기.

   >[!NOTE]
   >
   >사용자 지정 Target 기반 지표를 로 보낼 수 있습니다. [!DNL Analytics] 에만 의존하지 않고 [!DNL Analytics] 데이터. 예를 들어 일반적으로 추적되지 않는 페이지 클릭을 모니터링할 수 있습니다. [!DNL Analytics]. 이 사용자 지정 지표는 (으)로 전송됩니다. [!DNL Analytics] 에서 자동으로 [!DNL Target] 서버이며, &quot;[!DNL Target] 의 지표 선택기에서 &quot;전환&quot; 지표 [!DNL Analytics]. 다음 [!DNL Target] 을 사용하도록 선택한 경우 전환 지표가 비어 있습니다. [!DNL Analytics] 지표.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 콘텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >설정 후 활동을 설정할 때 [!DNL Analytics] 보고 소스로 보고 대상을 설정할 수 있는 옵션이 없습니다. [!DNL Analytics] 세그먼트는 다음 위치에서 사용할 수 있습니다. [!DNL Target] 활동 보고서.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## A4T, 자동 할당 및 자동 타겟 활동

자세한 내용은 [자동 할당 및 자동 타겟 활동에 대한 A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
