---
keywords: 글로벌 mbox;target classic;target classic의 글로벌 mbox 사용
description: Adobe에 이전 글로벌 mbox를 사용하는 방법을 알아봅니다 [!DNL Target] 활동은 기존 구현을 위해 페이지에 글로벌 mbox를 이미 만든 경우입니다.
title: 이전 구현에서 글로벌 mbox를 사용할 수 있습니까?
feature: at.js
role: Developer
exl-id: 1eb6836b-6b3c-4494-af67-cd72a4f357e2
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 36%

---

# 이전 구현에서 글로벌 mbox를 사용

기본적으로 [!DNL Target] 는 target-global-mbox라는 글로벌 mbox를 만들며, 이 mbox는에서 만든 활동을 실행하는 데 사용됩니다. [!DNL Target]. 하지만, 이미 페이지에서 이전 구현을 위한 mbox를 만든 경우, [!DNL Target] 활동에 이 mbox를 사용할 수 있습니다.

>[!NOTE]
>
>mbox 요청은 계정당 하나만 보유할 수 있습니다.

[!DNL Target]와 레거시 구현 둘 다에 기존 글로벌 mbox를 사용하려면, 몇 개의 매개 변수를 설정해야 합니다.

1. 이동 [!DNL Target]를 클릭한 다음 **[!UICONTROL 관리]** > **[!UICONTROL 구현]**.

   기본적으로 **[!UICONTROL 페이지 로드 활성화(글로벌 mbox 자동 만들기)]** 이 활성화되어 있고, 사용자 지정 글로벌 mbox의 이름이 지정됩니다. `target-global-mbox`.

1. 기존 mbox를 사용하려면 를 비활성화하십시오 **[!UICONTROL 페이지 로드 활성화(글로벌 mbox 자동 만들기)]**, 및에서 이전에 만든 글로벌 mbox의 이름을 지정합니다. **[!UICONTROL 글로벌 Mbox]** 필드.

   다음 [!UICONTROL 글로벌 Mbox] 드롭다운은 계정에 있는 모든 mbox를 나열합니다. 아직 존재하지 않는 mbox를 사용하려면, mbox를 만드십시오.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   계정에 대한 설정이 업데이트됩니다.

1. 새 at.js 파일을 다운로드하고 사이트에서 참조합니다.

   모든 기존 활동은 이전에 만들어서 구현한 활동을 포함하여, 지정된 글로벌 mbox를 사용하도록 업데이트됩니다.

## 글로벌 mbox 구현 문제 해결

다음 FAQ를 사용하여 글로벌 mbox 구현 문제를 해결할 수 있습니다.

### 글로벌 mbox가 로드되지 않거나 페이지 로드 시 글로벌 mbox 로드가 느려지는 이유는 무엇입니까?

at.js 참조가 페이지에서 첫 번째 JavaScript 호출인지 확인합니다. 이 문제에 대한 다른 해결 방법은 [글로벌 mbox 자주 묻는 질문](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
