---
keywords: 글로벌 mbox;글로벌 mbox 사용자 지정;at.js 편집;at.js;at.js 구현
description: Adobe Target의 관리 구현 페이지에서 at.js에 대한 글로벌 mbox를 사용자 지정하는 방법을 알아봅니다.
title: 글로벌 mbox를 사용자 지정하는 방법
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 17%

---

# 글로벌 mbox 사용자 지정

사용자 지정하는 데 도움이 되는 정보 [!DNL Adobe Target] at.js에 대한 글로벌 mbox입니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭합니다.

1. 비활성화 **[!UICONTROL 페이지 로드 활성화(글로벌 mbox 자동 만들기)]**&#x200B;를 입력한 후에 활동을 전달하는 데 사용할 사용자 지정 글로벌 mbox의 이름을 추가합니다 [!DNL Target].

   >[!IMPORTANT]
   >
   >다른 글로벌 mbox를 선택하면 변경 사항이 자동으로 저장됩니다.

   이 사용자 지정 mbox도 클릭 추적에 사용됩니다.

   ![custom-global-mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. 구현 [!DNL at.js] 라이브러리를 사용하십시오.

   자세한 내용은 [at.js를 배포하는 방법](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/how-to-deployatjs/) 추가 정보.

1. 전환 시간을 릴리스에 맞춰 지정합니다.

   준비가 되면 [!DNL Target] 향후에 모든 활동에 글로벌 mbox를 사용하기 시작하려면 이 단계를 계속 진행할 수 있습니다.

   위의 2단계에서 사용되는 이름과 일치하도록 사용자 지정 글로벌 mbox의 이름을 업데이트합니다.

   >[!IMPORTANT]
   >
   >계정 동기화에 있는 모든 활동이 이 mbox와 동기화됩니다. 활동이 계속 작동하도록 글로벌 mbox가 사이트에 있는지 확인합니다. 이 mbox와 동기화하는 VEC(시각적 경험 작성기)를 사용하여 만든 영향을 받는 활동을 편집하고 다시 저장해야 합니다. 양식 기반 경험 작성기에서 만들었거나 API를 통해 만든 활동을 다시 저장할 필요가 없습니다.

