---
description: 기본적으로, Target Standard에서는 target-global-mbox라는 글로벌 mbox를 만들어 Target Standard에서 만들어진 활동들 실행하는 데 사용합니다. 하지만, 이미 페이지에서 레거시 구현에 대한 mbox를 만든 경우, Target Standard 활동에 이 mbox를 사용할 수 있습니다.
keywords: 글로벌 mbox;target classic;target classic의 글로벌 mbox 사용
seo-description: 기본적으로, Target Standard에서는 target-global-mbox라는 글로벌 mbox를 만들어 Target Standard에서 만들어진 활동들 실행하는 데 사용합니다. 하지만, 이미 페이지에서 레거시 구현에 대한 mbox를 만든 경우, Target Standard 활동에 이 mbox를 사용할 수 있습니다.
seo-title: 이전 구현에서 글로벌 mbox를 사용
solution: Target
subtopic: 시작하기
title: 이전 구현에서 글로벌 mbox를 사용
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 이전 구현에서 글로벌 mbox를 사용{#use-a-global-mbox-from-a-legacy-implementation}

기본적으로, Target Standard에서는 target-global-mbox라는 글로벌 mbox를 만들어 Target Standard에서 만들어진 활동들 실행하는 데 사용합니다. 하지만, 이미 페이지에서 레거시 구현에 대한 mbox를 만든 경우, Target Standard 활동에 이 mbox를 사용할 수 있습니다.

>[!NOTE]
>
>mbox 요청은 계정당 하나만 보유할 수 있습니다.

[!DNL Target Standard]와 레거시 구현 둘 다에 기존 글로벌 mbox를 사용하려면, 몇 개의 매개 변수를 설정해야 합니다.

1. [!DNL Target Standard]로 이동한 다음, **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]** 을 클릭합니다.

   기본적으로, [!UICONTROL 글로벌 mbox 자동 만들기]가 활성화되어 있고, 사용자 지정 글로벌 mbox의 이름은 `target-global-mbox`로 지정됩니다.
1. 기존 mbox를 사용하려는 경우, [!UICONTROL 글로벌 mbox 자동 만들기]를 비활성화하고, [!UICONTROL 사용자 지정 글로벌 mbox] 필드에 이전에 만든 글로벌 mbox의 이름을 지정하십시오.

   [!UICONTROL 사용자 지정 글로벌 mbox] 드롭다운에는 계정에 있는 모든 mbox가 나열됩니다. 아직 존재하지 않는 mbox를 사용하려면, Target Classic에서 mbox를 만드십시오.
1. **[!UICONTROL 저장을 클릭합니다]**.

   계정에 대한 mbox.js 설정이 업데이트됩니다.
1. 새 mbox.js 파일을 다운로드하고 사이트에서 참조합니다.

   새 mbox.js 파일로 프로덕션 사이트를 업데이트했다면, 이제 기본 설정을 지정할 수 있습니다.
1. **[!UICONTROL 설정]** &gt; **[!UICONTROL 환경 설정]** 을 클릭합니다.
1. [!UICONTROL 사용자 지정 글로벌 mbox] 필드에서, 구현 페이지에서 선택한 글로벌 mbox의 이름을 지정합니다.
1. **[!UICONTROL 제출을 클릭합니다]**.

   모든 기존 활동은 이전에 만들어서 구현한 활동을 포함하여, 지정된 글로벌 mbox를 사용하도록 업데이트됩니다.
   **글로벌 Mbox 구현 문제 해결** *글로벌 mbox가 로드되지 않거나 페이지 로드 시 글로벌 mbox 로드가 느려지는 이유는 무엇입니까?*

mbox.js가 페이지의 첫 번째 자바스크립트 호출인지 확인하십시오. 이 문제의 다른 해결 방법을 보려면 [mbox.js 구현](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)을 참조하십시오.
