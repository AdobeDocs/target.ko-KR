---
keywords: Targeting;analytics;tracking server
description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard에서 활동을 구성할 수 있습니다.
title: Analytics 데이터 사용
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 95%

---


# Analytics 데이터 사용{#using-analytics-data}

Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard에서 활동을 구성할 수 있습니다.

Analytics를 Target의 데이터 소스로 설정하는 방법에 대한 자세한 내용은 [Adobe Analytics을 Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md)의 보고 소스로 참조하십시오.

Analytics를 보고 소스로 사용하는 활동을 설정하기 전에 방문자당 매출액(RPV) 향상 또는 장바구니 클릭 수 증가 등과 같이 활동 목표를 설정합니다. 캠페인의 최종 성공 지표를 선택합니다. Analytics에서 언제든지 추가 지표를 선택할 수 있지만 이 테스트를 적용할 특정 지표는 지정해야 합니다.

>[!NOTE]
>
>사용자 계정에 대해 Target과 Analytics 간의 통합이 설정되지 않았더라도 Analytics 및 Target 둘 다에 Adobe Experience Cloud 계정을 연결한 경우 Adobe Analytics 선택 사항을 사용할 수 있습니다.

Target의 보고 소스로 Analytics를 선택하는 경우 Target 활동 데이터를 수신할 Analytics 보고서 세트를 선택합니다. 이렇게 하려면 먼저 사용자 계정이 연결된 Analytics 회사 중에서 선택한 다음 활동에 대한 보고서 세트를 선택합니다. Adobe Target에 연결하기 위해 제공된 보고서 세트만 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 Adobe Experience Cloud에서 로그아웃했다가 다시 로그인한 후 다시 시도하십시오. 보고서 세트가 목록에 여전히 표시되지 않으면 고객 지원 센터에 문의하십시오.

A4T(Analytics for Target)를 위해서는 결과를 올바르게 보고하기 위한 추적 서버가 필요합니다. 기본 추적 서버가 추적 서버 필드에 표시됩니다. 둘 이상의 추적 서버를 사용하는 경우 이 필드에 올바른 추적 서버가 포함되어 있는지 확인해야 합니다. 각 유형의 대상 규칙을 구성하는 방법에 대한 자세한 내용은 [Analytics 추적 서버 사용](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

>[!NOTE]
>
>Adobe Analytics를 활동의 보고 소스로 사용하는 경우, mbox.js 버전 61 이상 또는 at.js 버전 0.9.1 이상을 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

Analytics를 보고 소스로 설정한 후에 활동을 설정하면 보고 대상을 설정할 수 있는 옵션이 없습니다. Analytics 세그먼트는 Target 활동 보고서에서 사용할 수 있습니다.

각 테스트의 목표로 사용할 성공 지표를 선택해야 합니다. 캠페인 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. Analytics 지표 선택기에 있는 Analytics 지표를 선택할 수 있습니다.

목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 테스트를 개선할 점을 알 수 있습니다.

방문자는 목표를 완료한 후 더 이상 캠페인에 포함되지 않습니다. 방문자가 활동을 완료한 후 캠페인을 다시 시작하면 새 방문자로 카운트됩니다.
