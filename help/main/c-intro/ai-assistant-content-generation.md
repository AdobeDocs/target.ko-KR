---
keywords: ai 도우미;인공 지능 도우미;콘텐츠 생성;콘텐츠 가속기;콘텐츠 생성;콘텐츠 생성
description: ' [!DNL AI Assistant]을(를) 사용하여 콘텐츠를 생성하는 방법에 대해 알아봅니다.'
title: ' [!DNL AI Assistant] in [!DNL Target] 을(를) 사용하여 콘텐츠를 생성하는 방법'
feature: Overview
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
exl-id: eb6f07d8-729e-4f94-ae7a-a054bf54b030
source-git-commit: 5ad564e43cd6f66e7f31072348f17e52013ed759
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 1%

---

# 콘텐츠 생성에 [!DNL Adobe Target]의 [!DNL AI Assistant] 사용

[!DNL Adobe Target]의 [!DNL AI Assistant]을(를) 사용하면 텍스트 코드 조각을 맞춤화하고 대상자에게 직접 전달하는 인공 지능(AI)을 사용하여 이미지를 선택하여 참여와 상호 작용을 향상시켜 활동의 효과를 높일 수 있습니다.

[!DNL Adobe Target]의 [!DNL AI Assistant] 기능을 사용하여 생성 AI에 의해 제공되는 활동 콘텐츠를 높이십시오.

## 사전 요구 사항

1.  [!DNL Adobe Target]](/help/main/c-intro/enabling-ai-assistant.md)의 [활성화 [!DNL Adobe Experience Platform] [!DNL AI Assistant]에서 필수 구성 요소 작업을 완료했는지 확인하십시오.

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

   [!DNL AI Assistant]이(가) 흥미로운 NYC 모험을 위해 간단한 프롬프트를 매혹적이고 더 긴 형식의 광고 사본으로 변환하는 방법을 보려면 아래의 [예제 변형](#variations)을 참조하십시오.

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

## 예제 변형 {#variations}

영웅 텍스트를 바꾸는 것은 시작에 불과합니다. [!DNL Target]의 [!DNL AI Assistant]을(를) 사용하면 기본 편집으로 제한되지 않습니다. 전체 경험에서 콘텐츠를 만들고, 세분화하고, 개선할 수 있는 권한이 있습니다. 변형을 브레인스토밍하거나, 메시지를 최적화하거나, 즉석에서 새 복사본을 만드는 경우 [!DNL AI Assistant]은(는) 생성 AI의 기능을 사용하여 몇 초 안에 매력적이고 영향력이 큰 콘텐츠를 만들 수 있습니다.

다음 프롬프트 및 변형은 [!DNL AI Assistant]의 기능을 보여 줍니다.

**[!UICONTROL Prompt]**: 최고의 대상을 방문하려면 NYC로 3일 동안 여행하는 흥미로운 광고를 만드십시오.
**[!UICONTROL Text Settings]**: FOMO, 영어, 설득력, Medium 길이.
* **[!UICONTROL Variation 1]**: 3일 간의 특별 여행을 통해 NYC의 매력에 대해 알아보십시오! 타임스 스퀘어, 센트럴 파크, 자유의 여신상 같은 상징적인 광경에 빠져보세요. 잠들지 않는 도시의 스릴과 아름다움을 이미 경험한 수많은 사람들과 함께하세요. 잊지 못할 추억을 놓치지 마세요. 오늘 당신의 모험을 예약하고 흥분의 일부가 될 것입니다! 사용 가능한 공간이 제한되어 있습니다!
* **[!UICONTROL Variation 2]**: 3일 간의 특별 휴가를 통해 NYC의 매력에 대해 알아보십시오! 타임스 스퀘어(Times Square)와 센트럴 파크(Central Park)와 같은 상징적인 랜드마크를 방문해 세계 최고 수준의 요리와 엔터테인먼트를 즐겨보십시오. 잊지 못할 이 모험을 놓치지 마세요. 공간은 한정되어 있고, 모든 사람들은 그들의 놀라운 경험에 대해 격찬하고 있습니다. 지금 예약하여 전 세계 여행객들을 매료시키는 즐거움의 일부가 되세요!
* **[!UICONTROL Variation 3]**: 우상적인 랜드마크가 기다리고 있는 NYC로 스릴 넘치는 3일 간의 도피를 시작해 보세요! 맨해튼(Manhattan)의 타임스 스퀘어(Times Square)의 전경을 감상하고 맛있는 요리를 맛보십시오. 엠파이어 스테이트 빌딩(Empire State Building)에서 아름다운 전망을 감상해 보십시오. 지금 행동하고 그들의 꿈을 사는 수많은 모험가들과 함께하세요. 절대 잠들지 않는 도시에서 잊지 못할 추억을 만드는 것을 놓치지 마세요. 사용 가능한 공간이 제한되어 있습니다. 오늘 모험을 예약하세요!
* **[!UICONTROL Variation 4]**: 3일간 NYC 모험을 지금 예약하여 전에 없던 이 도시의 마법을 경험해 보십시오! 상징적인 명소부터 숨겨진 보석까지, 빅 Apple 구석구석에는 신나는 무언가가 있다. 다른 사람들이 이미 즐기고 있는 잊을 수 없는 순간들을 놓치지 마세요. 떠들썩하게 굴어라. 오늘도 자리를 지키고 평생 남을 추억을 만들어 보세요. 서둘러, 빈자리가 빨리 채워지고 있어!

## 교육 비디오

### 콘텐츠 생성을 위해 AI Assistant를 사용하여 콘텐츠 생성

>[!VIDEO](https://video.tv.adobe.com/v/3434635/?learn=on">https://video.tv.adobe.com/v/3434635/?learn=on)
