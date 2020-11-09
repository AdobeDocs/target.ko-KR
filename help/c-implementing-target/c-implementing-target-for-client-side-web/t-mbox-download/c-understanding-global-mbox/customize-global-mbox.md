---
keywords: global mbox;customize global mbox;edit at.js;at.js;implement at.js
description: at.js에 대한 글로벌 mbox 사용자 지정에 도움이 되는 정보입니다.
title: 글로벌 mbox 사용자 지정
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---


# 글로벌 mbox 사용자 지정{#customize-a-global-mbox}

at.js에 대한 글로벌 mbox 사용자 지정에 도움이 되는 정보입니다.

1. 관리 **** > **[!UICONTROL 구현을 클릭합니다]**.

1. Disable **[!UICONTROL Page load enabled (Auto create global mbox)]**, then add the name of the custom global mbox that you would like to use to deliver activities from [!DNL Target].

   이 사용자 지정 mbox도 클릭 추적에 사용됩니다.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. Implement the [!DNL at.js] library on your site.

   자세한 [내용은 at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) 배포 방법을 참조하십시오.

1. 전환 시간을 릴리스에 맞춰 지정합니다.

   [!DNL Target] Standard/Premium에서 진행될 모든 활동에 대해 글로벌 mbox 사용을 시작할 준비가 되면 이 단계를 계속 진행할 수 있습니다.

   위의 2단계에서 사용되는 이름과 일치하도록 사용자 지정 글로벌 mbox의 이름을 업데이트합니다.

   >[!IMPORTANT]
   >
   >저장하면 계정 동기화에 있는 모든 활동이 이 mbox와 동기화됩니다. 이 mbox가 사용자의 사이트에 없는 경우 모든 활동이 더 이상 작동하지 않습니다.

