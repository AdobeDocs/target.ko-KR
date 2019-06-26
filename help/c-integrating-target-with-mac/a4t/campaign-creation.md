---
description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.
keywords: a4t;A4T;Analytics를 Target의 보고 소스로 사용
seo-description: Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.
seo-title: 활동 만들기
solution: Target
title: 활동 만들기
topic: 고급,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 활동 만들기{#activity-creation}

Adobe Analytics를 보고 소스(A4T)로 사용하도록 Target Standard/Premium에서 활동을 구성할 수 있습니다.

Analytics를 보고 소스로 사용하는 활동을 설정하기 전에 방문자당 매출액(RPV) 향상 또는 장바구니 클릭 수 증가 등과 같이 활동 목표를 설정합니다. 활동의 최종 성공 지표를 선택합니다. Analytics에서 언제든지 추가 지표를 선택할 수 있지만 이 테스트를 적용할 특정 지표는 지정해야 합니다.

Analytics를 보고 소스로 사용하는 Target Standard 활동을 만드는 방법은 일반 Target Standard 활동을 설정하는 방법과 비슷하지만 몇 가지 다른 점이 있습니다. 예를 들어, 활동을 만드는 동안에는 보고에 사용되는 세그먼트를 선택할 수 없습니다. Analytics에서 사용할 수 있는 모든 세그먼트는 보고서를 볼 때 적용되기 때문입니다.

1. **[!UICONTROL 활동 만들기를 클릭합니다]**.

   >[!NOTE]
   >
   >Analytics를 보고 소스로 사용하는 경우에는 활동 이름에 &quot;%&quot; 문자를 사용할 수 없습니다.

1. 활동 유형을 선택하고 활동 설정을 시작합니다.
1. 활동 만들기 흐름의 **[!UICONTROL 설정]** 부분으로 이동되면 **[!UICONTROL Adobe Analytics]** 를 선택하고 회사를 지정합니다.
1. 보고서 세트를 선택합니다.

   Adobe Analytics에서 사용할 수 있는 모든 보고서 세트를 선택할 수 있습니다. 보고서 세트는 수집된 데이터를 사용할 수 있는 위치를 규정합니다. 가상 보고서 세트는 보고서 세트 목록에 포함되지 않습니다.

   보고서 세트를 선택하는 동안 다음과 같은 두 가지 오류가 발생할 수 있습니다.

   * 사용 가능한 보고서 세트가 없는 오류가 표시되지만 계정이 제대로 설정되어 있습니다.
   Analytics 회사를 확인해야 할 수도 있습니다. Experience Cloud 계정이 둘 이상의 Analytics 회사에 연결되어 있으면 Target에서 로그아웃하고 올바른 회사에서 Analytics에 로그인하십시오. 그런 다음 Target으로 돌아오면 보고서 세트가 로드됩니다.

   * 예상한 보고서 세트가 표시되지 않습니다.
   Adobe Target에 연결하기 위해 제공된 보고서 세트만 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 Adobe Experience Cloud에서 로그아웃했다가 다시 로그인한 후 다시 시도하십시오.

   목록에 해당 보고서 세트가 여전히 없는 경우 [고객 지원 센터에 문의하십시오](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
1. 추적 서버를 지정합니다.

   [Analytics 추적 서버 사용](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

1. 경험을 정의합니다..
1. 활동 목표를 지정합니다.

   각 테스트의 목표로 사용할 성공 지표를 선택해야 합니다. 활동 목표는 성공적인 활동을 나타내는 전환 활동입니다. 몇 가지 특정 방법으로 개선할 목표가 없으면 테스트를 실행하지 않는 것이 좋습니다. Analytics 지표 선택기에 있는 Analytics 지표를 선택할 수 있습니다.

   >[!NOTE]
   >
   >Analytics 데이터에만 의존하지 않고 사용자 지정 Target 기반 지표를 Analytics에 보낼 수 있습니다. 예를 들어, Analytics에서는 일반적으로 추적되지 않는 페이지 클릭을 모니터링할 수 있습니다. 이 사용자 지정 지표는 Target 서버에서 Analytics로 자동 전송되며, Analytics의 지표 선택기에 &quot;Target 전환&quot; 지표로 표시됩니다. Analytics를 지표로 사용하도록 선택하면 Target 전환 지표가 비어 있게 됩니다.

   목표를 설정해도 테스트 결과를 평가할 때 다른 지표를 사용할 수 있습니다. 하지만 이 목표를 통해 활동에서 개선할 점을 알 수 있습니다.

   방문자는 목표에 도달한 후에 활동에 남아 있게 됩니다. 방문자에게는 계속해서 활동 컨텐츠가 표시되지만 새로운 활동 시작으로 카운트되지는 않습니다.

   >[!NOTE]
   >
   >Analytics를 보고 소스로 설정한 후에 활동을 설정하면 보고 대상을 설정할 수 있는 선택 사항이 없습니다. Analytics 세그먼트는 Target 활동 보고서에서 사용할 수 있습니다.

1. **[!UICONTROL 저장을 클릭합니다]**.

