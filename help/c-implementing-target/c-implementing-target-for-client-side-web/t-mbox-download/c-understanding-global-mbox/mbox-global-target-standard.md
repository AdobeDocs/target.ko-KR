---
keywords: global mbox;target classic;use global mbox from target classic
description: 기본적으로, Target Standard에서는 target-global-mbox라는 글로벌 mbox를 만들어 Target Standard에서 만들어진 활동들 실행하는 데 사용합니다. 하지만, 이미 페이지에서 레거시 구현에 대한 mbox를 만든 경우, Target Standard 활동에 이 mbox를 사용할 수 있습니다.
title: 이전 구현에서 글로벌 mbox를 사용
feature: null
subtopic: Getting Started
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: 6922b80c88cbd2947c3bfd0cc9d8409ff5dcdcd0
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 52%

---


# 이전 구현에서 글로벌 mbox를 사용{#use-a-global-mbox-from-a-legacy-implementation}

By default, [!DNL Target] creates a global mbox called target-global-mbox, which is used to run activities created in [!DNL Target]. 하지만, 이미 페이지에서 이전 구현을 위한 mbox를 만든 경우, [!DNL Target] 활동에 이 mbox를 사용할 수 있습니다.

>[!NOTE]
>
>mbox 요청은 계정당 하나만 보유할 수 있습니다.

[!DNL Target]와 레거시 구현 둘 다에 기존 글로벌 mbox를 사용하려면, 몇 개의 매개 변수를 설정해야 합니다.

1. Go to [!DNL Target], then click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   By default, **[!UICONTROL Page load enabled (Auto-create global mbox]** is enabled, and the custom global mbox is named `target-global-mbox`.

1. If you want to use an existing mbox, disable **[!UICONTROL Page load enabled (Auto-create global mbox]**, and specify the name of a previously created global mbox in the **[!UICONTROL Global Mbox]** field.

   The [!UICONTROL Global Mbox] drop-down lists all mboxes in your account. 아직 존재하지 않는 mbox를 사용하려면 mbox를 만듭니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   계정에 대한 mbox.js 설정이 업데이트됩니다.

1. 새로운 at.js 파일을 다운로드하여 사이트에서 참조합니다.

   모든 기존 활동은 이전에 만들어서 구현한 활동을 포함하여, 지정된 글로벌 mbox를 사용하도록 업데이트됩니다.

## 글로벌 mbox 구현 문제 해결

다음 FAQ를 사용하여 전역 mbox 구현 문제를 해결할 수 있습니다.

### 글로벌 mbox가 로드되지 않거나 페이지 로드 시 글로벌 mbox 로드가 느려지는 이유는 무엇입니까?

at.js 참조가 페이지의 첫 번째 JavaScript 호출인지 확인하십시오. 이 문제에 대한 다른 해결 방법은 [글로벌 mbox FAQ를 참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
