---
keywords: experience preview;experience urls;generate urls;view experience urls
description: Target Automated Personalization 활동에 대한 경험 미리 보기 URL을 생성하여 활동이 미리 보기 및 QA용으로 라이브되기 전에 사이트에서 직접 경험 컨텐츠를 볼 수 있습니다. 경험 미리 보기 URL은 타깃팅을 무시하여 특정 경험을 강제로 봅니다.
title: 경험 미리 보기 URL을 사용하여 Automated Personalization 활동 미리 보기
feature: ap
topic: Standard
uuid: 2ef07b6c-086d-43ac-bf02-efe217652a3a
translation-type: tm+mt
source-git-commit: 6278a01928fcb9dd0b34d7a8b5313f09f1e8da0f
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 64%

---


# ![프리미엄](/help/assets/premium.png) 미리 보기 URL을 사용하여 Automated Personalization 활동 미리 보기{#share-experience-urls-to-preview-automated-personalization-outside-of-target}

Target Automated Personalization 활동에 대한 경험 미리 보기 URL을 생성하여 활동이 미리 보기 및 QA용으로 라이브되기 전에 사이트에서 직접 경험 컨텐츠를 볼 수 있습니다. 경험 미리 보기 URL은 타깃팅을 무시하여 특정 경험을 강제로 봅니다.

>[!NOTE]
>
>Automated Personalization에 대한 경험 미리 보기 URL은 활동 QA 모드와 다릅니다. 활동 QA 모드에서는 다른 유형의 활동에 대한 활동 URL을 만들 수 있습니다. 자세한 내용은 [활동 QA](/help/c-activities/c-activity-qa/activity-qa.md)를 참조하십시오.
>
>AP 활동에 대한 경험 미리 보기 URL은 at.js 1.x를 사용하는 경우에만 사용할 수 있습니다.AP 활동에 대한 경험 미리 보기 URL은 현재 at.js 2.x에서 지원되지 않습니다.

경험 미리 보기 URL을 사용하여 별도의 QA 활동을 만들지 않고도 다양한 브라우저와 환경에서 팀 멤버와 경험을 공유하고 QA 경험을 공유할 수 있습니다. 이 기능은 사이트가 복잡한 경우나 보안 정책 때문에 해당 사이트를 시뮬레이터에서 볼 수 없는 경우에 특히 유용합니다.

1. [자동화된 개인화 활동](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)을 만들거나 해당 활동을 클릭하여 엽니다.

   경험을 미리 보기 위해 활동이 라이브 상태일 필요는 없습니다.
1. 활동 요약 페이지에서 세 개의 세로 점을 클릭한 후 **[!UICONTROL 경험 URL 보기]**&#x200B;를 클릭합니다.
1. URL을 검토 및/또는 지정합니다.

   * 시각적 경험 작성기를 사용하는 경우 활동에 대해 지정한 기본 URL이 자동으로 입력되고, 활동의 각 경험에 대해 링크가 생성됩니다. 원할 경우 이 URL을 변경하고 다른 URL을 추가할 수 있습니다.
   * 양식 기반 경험 작성기를 사용하는 경우 기본 URL이 자동으로 입력되지 않습니다. If you haven&#39;t previously created experience preview URLs, click **Add New URL**. 미리 보려는 모든 URL과 각 URL의 이름을 지정해야 합니다.

   여러 URL을 추가할 수 있습니다. 이러한 기능은 다중 페이지 테스트 또는 템플릿 테스트를 실행하며 둘 이상의 페이지에서 활동을 미리 보려는 경우에 유용합니다.

   모달 창에는 Target의 시각적 경험 작성기 외부에서 경험을 &quot;실제로 미리 볼 수 있도록&quot; 사이트의 경험에 대한 링크가 표시됩니다. 미리 보기를 공유하려면 메시지에서 링크를 공유해야 합니다. URL에는 메시지의 링크에서 페이지에 액세스할 때만 페이지를 올바르게 표시하는 매개 변수가 포함되어 있으므로 링크를 클릭한 다음, 페이지에서 결과 URL을 복사할 수 없습니다. 대신 모달 창에서 텍스트를 복사하고 전체 텍스트를 팀에 이메일로 보냅니다.
1. **[!UICONTROL 모두 생성]**&#x200B;을 클릭한 다음, 각 경험을 클릭하여 미리 봅니다.

   If you then make changes to the experience, make sure to generate new preview links for your team by returning to the modal window and clicking **Renew Links** to get new links.

   **참고:** 미리 보기 링크는 새 탭에서 열리며 브라우저에서 팝업 차단 기능을 비활성화해야 사용할 수 있습니다.

1. 활동을 미리 보려면 각 경험 이름을 클릭합니다.

   활동을 표시하는 페이지가 열립니다.
1. 활동 요약으로 돌아가려면 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

## 고려 사항 {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**경험 미리 보기 URL 생성**

* 경험 미리 보기 URL은 경험 간의 트래픽 분리에 영향을 받지 않습니다.
* 대상 수준 타깃팅은 미리 보기에 영향을 주지 않습니다.
* 활동당 최대 300개의 경험 URL을 자동으로 생성할 수 있습니다. 그 후에는 URL을 수동으로 생성해야 합니다.
* 활동당 최대 300개의 경험 URL을 자동으로 생성할 수 있습니다. 그 후에는 URL을 수동으로 생성해야 합니다.
* 경험 수에 따라, URL을 생성하는 데 최대 5분이 걸릴 수 있습니다. 이 대화 상자는 닫지 마십시오. 닫으면 생성된 URL이 손실됩니다.
* 생성된 미리 보기 링크는 두 달 동안 유효합니다. 이 기간이 지나면 미리 보기 URL을 다시 생성해야 합니다.
* 경험이 변경되면 언제든지 재생성해야 합니다.

**경험 미리 보기 URL 공유**

* 타깃팅된 대상에 속하지 않더라도 경험을 미리 볼 수 있습니다.
* Adobe Target에 대한 액세스 권한이 없는 동료와 경험 미리 보기 URL을 공유할 수 있습니다.

**경험 미리 보기 URL을 사용하여 경험 보기**

* 페이지가 변경되지 않는 한, 저장된 활동을 미리 볼 수 있습니다.
* 활동이 활성 상태이든 비활성 상태이든 경험 미리 보기 URL을 사용할 수 있습니다.
* 초안 상태의 경험은 미리 볼 수 없습니다.
* 경험 미리 보기 URL을 보면 보고에 영향을 받지 않습니다.

**경험 미리 보기 URL 문제 해결**

* 새 탭에서 미리 보기를 볼 수 없는 경우(브라우저 캐시로 인해) 2~3번 새로 고치거나 링크를 복사한 후 새 브라우저, 새 세션 전용 브라우저 모드에서 엽니다.
