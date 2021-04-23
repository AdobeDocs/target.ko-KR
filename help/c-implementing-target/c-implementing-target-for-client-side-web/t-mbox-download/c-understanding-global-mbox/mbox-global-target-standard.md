---
keywords: 글로벌 mbox;target classic;target classic의 글로벌 mbox 사용
description: 기존 구현에 대해 페이지에 글로벌 mbox를 이미 만든 경우 Adobe [!DNL Target] 활동에 기존 글로벌 mbox를 사용하는 방법을 알아봅니다.
title: 기존 구현에서 글로벌 mbox를 사용할 수 있습니까?
feature: at.js
role: Developer
exl-id: 1eb6836b-6b3c-4494-af67-cd72a4f357e2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 36%

---

# 기존 구현의 글로벌 mbox 사용

기본적으로 [!DNL Target]은 [!DNL Target]에서 만든 활동을 실행하는 데 사용되는 target-global-mbox라는 글로벌 mbox를 만듭니다. 하지만, 이미 페이지에서 이전 구현을 위한 mbox를 만든 경우, [!DNL Target] 활동에 이 mbox를 사용할 수 있습니다.

>[!NOTE]
>
>mbox 요청은 계정당 하나만 보유할 수 있습니다.

[!DNL Target]와 레거시 구현 둘 다에 기존 글로벌 mbox를 사용하려면, 몇 개의 매개 변수를 설정해야 합니다.

1. [!DNL Target]으로 이동한 다음 **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭합니다.

   기본적으로 **[!UICONTROL 페이지 로드가 활성화되어 있습니다(글로벌 mbox]** 자동 만들기 기능이 활성화되어 있고 사용자 지정 글로벌 mbox의 이름은 `target-global-mbox`입니다.

1. 기존 mbox를 사용하려면 **[!UICONTROL 페이지 로드가 활성화됨(글로벌 mbox]** 자동 만들기)을 비활성화하고 **[!UICONTROL 글로벌 mbox]** 필드에 이전에 만든 글로벌 mbox의 이름을 지정합니다.

   [!UICONTROL 글로벌 mbox] 드롭다운에는 계정의 모든 mbox가 나열됩니다. 아직 존재하지 않는 mbox를 사용하려면 mbox를 만듭니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   계정에 대한 mbox.js 설정이 업데이트됩니다.

1. 새 at.js 파일을 다운로드하여 사이트에서 참조합니다.

   모든 기존 활동은 이전에 만들어서 구현한 활동을 포함하여, 지정된 글로벌 mbox를 사용하도록 업데이트됩니다.

## 글로벌 mbox 구현 문제 해결

다음 FAQ를 사용하여 글로벌 mbox 구현 문제를 해결할 수 있습니다.

### 글로벌 mbox가 로드되지 않거나 페이지 로드 시 글로벌 mbox 로드가 느려지는 이유는 무엇입니까?

at.js 참조가 페이지에서 첫 번째 JavaScript 호출인지 확인합니다. 이 문제에 대한 다른 해결 방법은 [글로벌 mbox FAQ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md)를 참조하십시오.
