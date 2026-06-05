---
keywords: 타깃팅;analytics;추적 서버;analytics for target;a4t
description: ' [!DNL Adobe Target] 에서  [!DNL Adobe Analytics] 을(를) 보고 소스(A4T)로 사용하도록 활동을 구성하는 방법에 대해 알아봅니다.'
title: ' [!DNL Target]에서  [!DNL Analytics] 데이터를 사용하려면 어떻게 해야 합니까?'
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
TQID: https://experienceleague.adobe.com/x38YsYI4a6-92oOr6Fs3RfKrJHbSaLNj0cki5CInPPg
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 19%

---

# [!DNL Adobe Analytics] 데이터 사용 중

[!DNL Adobe Analytics]을(를) 보고 원본(A4T)으로 사용하도록 [!DNL Adobe Target]에서 활동을 구성할 수 있습니다.

[!DNL Target]의 데이터 소스로 [!DNL Analytics]을(를) 설정하는 방법에 대한 자세한 내용은 [Adobe Target의 보고 Source으로 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을(를) 참조하십시오.

[!DNL Analytics]을(를) 보고 소스로 사용하는 활동을 설정하기 전에 방문자당 매출(RPV) 향상 또는 장바구니 클릭 수 증가와 같이 활동에 대한 목표를 설정하십시오. 활동의 최종 성공 지표를 선택합니다. [!DNL Analytics]에서 언제든지 추가 지표를 선택할 수 있지만 이 테스트가 영향을 줄 것으로 예상되는 특정 지표를 지정해야 합니다.

>[!NOTE]
>
>[!DNL Target]과(와) [!DNL Analytics] 간의 통합이 설정되지 않았더라도 [!DNL Adobe Experience Cloud] 계정을 [!DNL Analytics]과(와) [!DNL Target] 모두로 연결한 경우 [!DNL Adobe Analytics] 옵션을 사용할 수 있습니다.

[!DNL Target]에 대한 보고 소스로 [!DNL Analytics]을(를) 선택할 때 [!DNL Target] 활동 데이터를 받을 [!DNL Analytics] 보고서 세트를 선택합니다. 보고 소스를 지정하려면 먼저 사용자 계정이 연결된 [!DNL Analytics] 회사 중에서 선택한 다음 활동에 대한 보고서 세트를 선택합니다. [!DNL Adobe Target]에 연결하기 위해 제공된 보고서 세트만 선택할 수 있습니다. 예상한 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 [!DNL Adobe Experience Cloud]에 다시 로그인하여 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 고객 지원 센터에 문의하십시오.

[!UICONTROL Analytics for Target]&#x200B;(A4T)에는 결과를 올바로 보고하기 위한 추적 서버가 필요합니다. 기본 추적 서버가 [!UICONTROL 추적 서버] 필드에 표시됩니다. 추적 서버를 두 개 이상 사용하는 경우 이 필드에 올바른 추적 서버를 포함해야 합니다. 자세한 내용은 [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

>[!NOTE]
>
>[!DNL Adobe Analytics]을(를) 활동의 보고 소스로 사용하는 경우 at.js 버전 0.9.1 이상을 사용하는 경우 활동을 만드는 동안 추적 서버를 지정할 필요가 없습니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

[!DNL Analytics]을(를) 보고 소스로 설정한 후 활동을 설정할 때 보고 대상을 설정할 수 있는 옵션이 없습니다. [!DNL Analytics] 세그먼트는 [!DNL Target] [!UICONTROL 활동] 보고서에서 사용할 수 있습니다.

각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. [!DNL Analytics] 지표 선택기에서 사용 가능한 [!DNL Analytics] 지표를 선택할 수 있습니다.

목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 테스트를 개선할 점을 알 수 있습니다.

방문자가 목표를 완료한 후에는 해당 방문자는 더 이상 활동에 포함되지 않습니다. 방문자가 활동을 완료한 후 활동을 다시 시작하는 경우 해당 방문자는 새 방문자로 계산됩니다.
