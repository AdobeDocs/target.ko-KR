---
keywords: 글로벌 mbox;글로벌 mbox 사용자 지정;at.js 편집;at.js;at.js 구현
description: Adobe Target의 관리 구현 페이지에서 at.js에 대한 글로벌 mbox를 사용자 지정하는 방법을 알아봅니다.
title: 글로벌 mbox를 사용자 지정하는 방법
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: fb0a62ecc5609e7b8ef5f6a4fb5a94f8ba025fec
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 22%

---

# 글로벌 mbox 사용자 지정

at.js에 대해 글로벌 mbox를 사용자 지정하는 데 도움이 되는 정보입니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 페이지 로드가 활성화됨(글로벌 mbox 자동 만들기)]**&#x200B;을 비활성화한 다음, [!DNL Target]에서 활동을 전달하는 데 사용할 사용자 지정 글로벌 mbox의 이름을 추가합니다.

   >[!IMPORTANT]
   >
   >다른 글로벌 mbox를 선택하면 변경 사항이 자동으로 저장됩니다.

   이 사용자 지정 mbox도 클릭 추적에 사용됩니다.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. 사이트에서 [!DNL at.js] 라이브러리를 구현합니다.

   자세한 내용은 [at.js를 배포하는 방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md)을 참조하십시오.

1. 전환 시간을 릴리스에 맞춰 지정합니다.

   [!DNL Target] 이후에 모든 활동에 대해 글로벌 mbox 사용을 시작할 준비가 되면 이 단계를 계속 진행할 수 있습니다.

   위의 2단계에서 사용되는 이름과 일치하도록 사용자 지정 글로벌 mbox의 이름을 업데이트합니다.

   >[!IMPORTANT]
   >
   >계정 동기화에 있는 모든 활동이 이 mbox와 동기화됩니다. 이 mbox가 사용자의 사이트에 없는 경우 모든 활동이 더 이상 작동하지 않습니다.
