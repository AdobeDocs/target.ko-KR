---
description: Target Standard를 Adobe Dynamic Media Classic (이전 Scene 7) 와 통합하여 컨텐츠 라이브러리에서 DAM (Digital Asset Management) 를 제공할 수 있습니다.
seo-description: Target Standard를 Adobe Dynamic Media Classic (이전 Scene 7) 와 통합하여 컨텐츠 라이브러리에서 DAM (Digital Asset Management) 를 제공할 수 있습니다.
seo-title: Dynamic Media Classic 통합
solution: Target
subtopic: 시작하기
title: Dynamic Media Classic 통합
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: c6a59843c80017e6f072f65ffad822fe198ebb55

---


# Dynamic Media Classic integration{#scene-settings}

Target Standard를 Adobe Dynamic Media Classic (이전 Scene 7) 와 통합하여 컨텐츠 라이브러리에서 DAM (Digital Asset Management) 를 제공할 수 있습니다.

>[!NOTE]
>
>Target와 Dynamic Media Classic를 통합하면 Adobe Experience Cloud Assets 폴더에 업로드된 자산 (활동의 일부로) 배달을 사용할 수 있습니다. 이 통합은 Target 활동에 제공하기 위해 Dynamic Media Classic에 업로드된 모든 자산에 대한 액세스를 활성화하지 않습니다.

이미 Dynamic Media 계정이 있는 경우 기존 자격 증명을 제공할 수 있습니다. 계정이 없는 경우 Adobe 담당자의 추가 비용 없이 제한된 Dynamic Media Classic 계정을 요청할 수 있습니다. 이 계정은 Target용으로만 제한된 용도로 사용할 수 있습니다. 이 서비스는 이미지 대체 기능이 필요한 워크플로우의 고객이 사용할 수 있습니다.

이 설정이 구성되지 않은 경우, 활동 생성 워크플로우 내에서 이미지 오퍼 대체 옵션을 사용할 수 없습니다. 이 설정을 구성한 후에는 이미지 오퍼를 대체/변경하기 위한 옵션을 [VEC(시각적 경험 작성기) 및 양식 기반 경험 작성기](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) 둘 다에서 사용할 수 있습니다. 그런 다음, Target 활동에서 사용할 수 있도록 Adobe Experience Cloud에서 업로드한 이미지와 함께 이미지 오퍼를 활용할 수 있습니다.

활동 생성 중에 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 사용자 고유의 웹 서버에 배포하고 코드에서 자체 URL을 사용해야 합니다. Experience Cloud에 업로드된 이미지의 게재된 URL을 획득한 후 직접 사용하거나, Adobe Target을 사용하여 타깃팅 워크플로우 외부에서 사용할 수 있는 방법은 없습니다. 이 기능이 계약에 따라 허용되지는 않습니다.

다이내믹 미디어의 이미지 저장소 URL와 최종 게시 URL는 서로 다르며, 이러한 경우에는 이미지가 제대로 작동하지 않으므로 이미지 저장소 링크를 사용하여 오퍼를 만들어서는 안 됩니다. 도움말 설명서에 설명된 대로 이미지 오퍼 기능을 사용해야 합니다.

Dynamic Media Classic (Scene 7) 와 통합하려면 다음 정보를 지정해야 합니다.

1. **[!UICONTROL 설정]** &gt; **[!UICONTROL Scene7 설정]**&#x200B;을 클릭합니다.
1. 다음 Dynamic Media Classic 계정 정보를 지정합니다.

   **지역:** 다이내믹 미디어 계정 지역: 북아메리카, 유럽 또는 아시아

   **애드혹 폴더:** 대상 폴더 외부에 있고 수동으로 다이내믹 미디어에 업로드되는 콘텐트의 위치입니다.

   **이메일 주소:** Dynamic Media Classic (Scene 7) 에 로그인하는 데 사용되는 이메일 주소입니다.

   **암호:** Dynamic Media Classic (Scene 7) 에 로그인하는 데 사용되는 암호입니다.
1. **[!UICONTROL 제출을 클릭합니다]**.
