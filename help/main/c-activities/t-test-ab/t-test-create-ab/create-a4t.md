---
keywords: 타깃팅;analytics;추적 서버;analytics for target;a4t
description: 에서 활동을 구성하는 방법 알아보기 [!DNL Adobe Target] 사용 [!DNL Adobe Analytics] 를 보고 소스 (A4T) 로 사용하십시오.
title: 사용 방법 [!DNL Analytics] 데이터 입력 [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 19%

---

# 사용 [!DNL Adobe Analytics] 데이터

에서 활동을 구성할 수 있습니다. [!DNL Adobe Target] 사용 [!DNL Adobe Analytics] 를 보고 소스 (A4T) 로 사용하십시오.

설정에 대한 자세한 정보 [!DNL Analytics] 를 위한 데이터 소스로 사용 [!DNL Target], 참조 [Adobe Target용 보고 소스로서의 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

을 사용하는 활동을 설정하기 전에 [!DNL Analytics] 보고 소스로 RPV(방문자당 매출) 향상 또는 장바구니 클릭 수 증가와 같은 활동에 대한 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. 다음 기간 동안 언제든지 추가 지표를 선택할 수 있지만, [!DNL Analytics], 이 테스트가 영향을 미칠 것으로 예상하는 특정 지표를 계속 지정해야 합니다.

>[!NOTE]
>
>다음 [!DNL Adobe Analytics] 옵션을 연결한 경우 옵션을 사용할 수 있습니다. [!DNL Adobe Experience Cloud] 두 계정 모두 포함 [!DNL Analytics] 및 [!DNL Target], 다음 사이에 통합이 있더라도 [!DNL Target] 및 [!DNL Analytics] 이(가) 귀하의 계정에 대해 설정되지 않았습니다.

선택 시 [!DNL Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Target], 다음을 선택합니다. [!DNL Analytics] 받을 보고서 세트 [!DNL Target] 활동 데이터. 보고 소스를 지정하려면 먼저 다음 중 하나를 선택합니다 [!DNL Analytics] 계정이 연결된 회사 를 선택한 다음 활동에 대한 보고서 세트를 선택합니다. 연결할 수 있도록 프로비저닝된 보고서 세트만 [!DNL Adobe Target] 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 다음에 다시 로그인하십시오 [!DNL Adobe Experience Cloud] 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 고객 지원 센터에 문의하십시오.

[!UICONTROL Analytics for Target] (A4T)에서 결과를 올바로 보고하려면 추적 서버가 필요합니다. 기본 추적 서버가에 표시됩니다 [!UICONTROL 추적 서버] 필드. 추적 서버를 두 개 이상 사용하는 경우 이 필드에 올바른 추적 서버를 포함해야 합니다. 다음을 참조하십시오 [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) 추가 정보.

>[!NOTE]
>
>를 사용하는 경우 [!DNL Adobe Analytics] at.js 버전 0.9.1 이상을 사용하는 경우 활동의 보고 소스로 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 생성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

설정 후 활동을 설정할 때 [!DNL Analytics] 보고 소스로 보고 대상을 설정할 수 있는 옵션이 없습니다. [!DNL Analytics] 세그먼트는 다음 위치에서 사용할 수 있습니다. [!DNL Target] [!UICONTROL 활동] 보고서.

각 활동의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. 다음 중 하나를 선택할 수 있습니다. [!DNL Analytics] 에서 사용 가능한 지표 [!DNL Analytics] 지표 선택기.

목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 테스트를 개선할 점을 알 수 있습니다.

방문자가 목표를 완료한 후에는 해당 방문자는 더 이상 활동에 포함되지 않습니다. 방문자가 활동을 완료한 후 활동을 다시 시작하는 경우 해당 방문자는 새 방문자로 계산됩니다.
