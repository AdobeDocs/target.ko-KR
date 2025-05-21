---
keywords: ai 도우미;인공 지능 도우미;콘텐츠 생성;콘텐츠 가속기;콘텐츠 생성;콘텐츠 생성
description: ' [!DNL AI Assistant]을(를) 사용하여 콘텐츠를 생성하는 방법에 대해 알아봅니다.'
title: ' [!DNL AI Assistant] in [!DNL Target] 을(를) 사용하여 콘텐츠를 생성하는 방법'
feature: Overview
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
exl-id: eb6f07d8-729e-4f94-ae7a-a054bf54b030
source-git-commit: 41889716a2793c846085d765d5e6f9db0fc70c30
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 2%

---

# 콘텐츠 생성에 [!DNL Adobe Target]의 [!DNL AI Assistant] 사용

[!DNL Adobe Target]의 [!DNL AI Assistant]을(를) 사용하면 텍스트 코드 조각을 맞춤화하고 대상자에게 직접 전달하는 인공 지능(AI)을 사용하여 이미지를 선택하여 참여와 상호 작용을 향상시켜 활동의 효과를 높일 수 있습니다.

[!DNL Adobe Target]의 [!DNL AI Assistant] 기능을 사용하여 생성 AI에 의해 제공되는 활동 콘텐츠를 높이십시오.

## 사전 요구 사항

1. [!DNL Adobe Target][&#128279;](/help/main/c-intro/enabling-ai-assistant.md)의 활성화 [!DNL Adobe Experience Platform] [!DNL AI Assistant]에서 필수 구성 요소 작업을 완료했는지 확인하십시오.

   * 조직은 먼저 법률 약관에 동의해야 합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.
   * 관리자가 [!DNL AI Assistant]에 액세스할 수 있는 충분한 권한을 부여해야 합니다.

## 텍스트 생성

[!DNL AI Assistant]을(를) 사용하여 텍스트를 생성하려면:

1. [[!DNL Target] [!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)(VEC) 내에서 VEC UI의 오른쪽 레일에 있는 **[!UICONTROL Show Content Assistant]**(![Show Content Assistant 아이콘](/help/main/assets/icons/MagicWand.svg)) 아이콘을 클릭합니다.

   ![Content Assistant 표시 아이콘](/help/main/c-intro/assets/ai-assistant-conntet-generation-icon.png)

1. [!DNL AI Assistant]을(를) 사용하여 수준을 올릴 텍스트 요소를 클릭합니다.

   예를 들어, 영웅 텍스트를 변경하려면 &quot;다음 도주 계획&quot;을 클릭하여 텍스트 옵션을 표시합니다.

   ![텍스트 설정 창](/help/main/c-intro/assets/ai-text-settings.png)

1. (선택 사항) **전체 화면 아이콘**( ![전체 화면 아이콘](/help/main/assets/icons/FullScreen.svg) )을 클릭하여 [!DNL AI Assistant]을(를) 확장합니다.

1. **[!UICONTROL Prompt]** 상자에 생성할 텍스트를 설명하십시오.

   예를 들어, 계절 휴가 판매의 경우, &quot;여름 휴가 기간 한정 판매 광고 매력적인 영웅 텍스트 작성&quot;을 입력할 수 있습니다.

1. **[!UICONTROL Text Settings]** 아이콘을 클릭하여 텍스트의 색조와 통신 전략을 지정합니다.

   * **커뮤니케이션 전략**: 생성된 텍스트에 가장 적합한 커뮤니케이션 스타일을 선택합니다.
   * **언어**: 텍스트에 사용할 언어를 선택합니다. [!DNL AI Assistant]은(는) 현재 영어로만 제공됩니다.
   * **음색**: 텍스트 음색이 대상자에게 울려 퍼집니다. [!DNL AI Assistant]이(가) 유익하거나, 흥미롭고, 장난스럽거나, 설득력 있게 들리도록 들릴지 여부에 관계없이 메시지를 적절히 조정할 수 있습니다.

1. 슬라이더를 사용하여 텍스트 길이([!UICONTROL Shorter Text] ~ [!UICONTROL Larger Text])를 선택하십시오.

1. 텍스트 변형 목록을 만들려면 **[!UICONTROL Generate]**&#x200B;을(를) 클릭합니다.

   ![AI 길잡이 텍스트 변형](/help/main/c-intro/assets/ai-variations-text.png)

1. **[!UICONTROL Apply]**&#x200B;을(를) 클릭하여 원하는 텍스트 변형을 선택합니다.

   **[!UICONTROL Preview]**&#x200B;을(를) 클릭하여 다른 변형을 볼 수도 있습니다. 원하는 변형을 클릭한 다음 **[!UICONTROL Select]**&#x200B;을(를) 클릭합니다.

   ![생성된 텍스트가 있는 AI 길잡이](/help/main/c-intro/assets/ai-text-done.png)

1. (조건부) 변경 내용을 취소하려면 [실행 취소] 아이콘(![실행 취소 아이콘](/help/main/assets/icons/Undo.svg))을 클릭합니다.

1. (선택 사항) AI Assistant에 피드백을 제공합니다.

   * Thumbs 위쪽 아이콘(![Thumbs 위쪽](/help/main/assets/icons/ThumbUp.svg)) 아이콘을 클릭하여 [!DNL AI Assistant]에게 변형을 좋아한다고 알립니다.
   * Thumbs Down( ![Thumbs Down 아이콘](/help/main/assets/icons/ThumbDown.svg)) 아이콘을 클릭하여 [!DNL AI Assistant]에게 변형을 좋아하지 않음을 알립니다.
   * [!UICONTROL Report Results]&#x200B;( ![결과 보고 아이콘](/help/main/assets/icons/Flag.svg)) 아이콘을 클릭하여 [!DNL AI Assistant]에 문제를 보고합니다.

## 교육 비디오

### 콘텐츠 생성을 위해 AI Assistant를 사용하여 콘텐츠 생성

>[!VIDEO](https://video.tv.adobe.com/v/3434635/?learn=on">https://video.tv.adobe.com/v/3434635/?learn=on)
