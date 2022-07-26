---
keywords: 대상;대상 규칙;대상 결합;제외;제외 추가;제외하기;대상 결합하기;임시 대상;애드혹 대상
description: 여러 대상(Adobe Experience Cloud 대상 및 [!DNL Target] 대상)을 사용하여 임시 대상을 만들 수 있습니다.
title: 여러 대상을 결합 하여 새 대상을 만들 수 있습니까?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 64%

---

# 여러 대상 결합

여러 대상 결합(포함) [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform], 및 [!DNL Target] 대상)을 사용하여 임시 대상을 만들 수 있습니다. 제외 규칙을 만들고 규칙에서 대상을 제외할 수도 있습니다.

>[!NOTE]
>
>다음 [!DNL Adobe Experience Platform] 모든 사용자가 소스를 사용할 수 있습니다. [!DNL Target] 고객이 [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}. 에서 사용할 수 있는 대상 [!DNL Adobe Experience Platform] 이 주제에서 설명한 대로 그대로 사용하거나 기존 대상과 결합할 수 있습니다.
>
>자세한 내용은 [Adobe Experience Platform의 대상 사용](/help/main/c-target/c-audiences/audiences.md#aep).

&quot;새로운 방문자&quot; 대상과 &quot;Chrome 사용자&quot; 대상이 있다고 가정합니다. 특정 활동에 대해 이 기존 대상들을 결합하여 Chrome 브라우저를 사용하는 새 방문자를 타깃팅할 수 있습니다. 세 번째 대상을 만들어 [!UICONTROL 대상] 라이브러리에 저장하는 대신, 활동을 만들 때 또는 기존 활동을 편집할 때 이 두 대상을 결합할 수 있습니다.

다른 예로, 모든 충성도 고객을 타깃팅할 수 있습니다. 예를 들어 특정 [!DNL Audience Manager] 충성도 상태를 위한 대상 및 결합 [!DNL Target] 현재 세션 동안 충성도 프로그램에 등록한 사람들로 구성된 대상입니다. 이러한 두 대상을 결합하는 것은 세 번째 영구 대상을 만드는 것보다 쉽습니다.

AND 및 OR 연산자를 사용하여 최대 20개의 대상을 결합할 수 있습니다.

[!DNL Target] UI의 다양한 위치에서 결합된 대상을 만들어 사용할 수 있습니다. 

## 활동을 만들 때 결합된 대상 만들기 {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

3단계 안내가 있는 워크플로우 동안 활동의 [!UICONTROL Target] 페이지에서 결합된 임시 대상을 만들 수 있습니다.

1. 를 만드는 동안 [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), **[!UICONTROL 타깃팅]** 페이지에서 3개의 수직 줄임표를 클릭한 다음 **[!UICONTROL 대상 바꾸기]**.

   ![단계 결과](assets/edit_audience.png)

1. **[!UICONTROL 대상 선택]** 페이지에서, 결합된 대상을 위한 빌딩 블록으로 사용할 대상의 옆에 있는 확인란을 선택합니다.

   를 사용하십시오 [!UICONTROL 대상 검색] 원하는 대상에 대한 검색 범위를 좁히려면 상자를 선택합니다.

   ![단계 결과](assets/combine_multiple_audiences1.png)

1. 클릭 **[!UICONTROL 여러 대상 결합]** 오른쪽 상단 모서리에서

   ![단계 결과](assets/combine_multiple_audiences2.png)

1. (조건부) 결합된 새 대상을 원하는 대로 편집합니다.

   다음 [!UICONTROL 대상자 편집] 대화 상자에서는 왼쪽의 추가 대상 빌딩 블록을 새로운 결합된 대상으로 끌어다 놓을 수 있습니다. 제외 규칙을 추가하고 대상을 제외할 수도 있습니다.

   1. 드래그 앤 드롭 기능을 사용하여 기존 섹션 내의 대상을 레벨 2 빌딩 블록으로 추가할 수 있습니다.

      예를 들어 앞의 예를 가정할 때 이제 결합된 대상에서 Safari 사용자도 포함시키려고 합니다. 다음 예와 같이, &quot;Safari 브라우저&quot; 대상을 검색하여 오른쪽의 &quot;Firefox 브라우저&quot; 상자로 드래그합니다.

      ![combined_multiple_audiences3 이미지](assets/combine_multiple_audiences3.png)

      두 브라우저 유형 대상 사이의 연산자는 &quot;AND&quot;입니다. 을(를) 선택합니다 [!UICONTROL 및] 드롭다운 목록을 &quot;OR&quot;로 변경하여 Firefox나 Safari 중 하나를 사용하여 새로운 방문자를 위한 새로운 결합된 대상을 만듭니다. 모든 잠재적 대상 구성원을 제외하는 규칙을 작성하지 않도록 주의하십시오. 예를 들어 고객이 Firefox와 Safari를 동시에 사용하여 페이지를 방문할 수는 없습니다.

      >[!NOTE]
      >
      >연산자(AND 또는 OR)는 대상을 결합할 때처럼 동일하게 유지되어야 합니다. 연산자들을 혼합하여 짜 맞출 수는 없습니다.

   1. 규칙에 제외를 추가하려면 **[!UICONTROL 제외]**.

      ![combined_multiple_audiences3a 이미지](assets/combine_multiple_audiences3a.png)

      대상자를 드래그하여 놓습니다.

      예를 들어 새 방문자에서 미국 방문자를 제외하려면 시장을 드래그할 수 있습니다. 미국 관객들이 이 상자 안에 들어 있습니다.

      이 결합된 대상은 Safari 또는 Firefox를 사용하여 사이트를 방문하는 모든 새로운 방문자(San Francisco의 방문자 제외)를 포함합니다.

   1. 규칙에서 대상을 제외하려면 **[!UICONTROL 제외]** > **[!UICONTROL 이 대상 제외]**&#x200B;를 클릭하십시오.

      예를 들어, Firefox를 사용하는 대상을 제외하고 사이트를 방문하는 모든 새 방문자를 포함하는 결합된 대상을 만들 수 있습니다. Firefox를 사용하는 방문자를 제외하는 것이 여러 브라우저(Safari, Chrome 및 Internet Explorer)를 명시적으로 포함하고 Firefox는 포함하지 않는 결합된 대상을 만드는 것보다 더 쉽고 빠릅니다.

1. 결합된 대상에 대해 수사적 이름을 지정한 다음 **[!UICONTROL 완료]**.

## 지표 타깃팅에서 사용할 결합된 대상 만들기 {#section_A42E795AFCBD4575809C5942039910F0}

지표 타깃팅에서 사용할 결합된 임시 대상을 활동의 [!UICONTROL 목표 및 설정] 페이지에서 만들어 수 있습니다. 예를 들어, 결합된 대상을 사용하여 전환을 기반으로 타깃팅을 만들려면 다음을 수행하십시오.

1.   [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 편집하거나 만들 때 **[!UICONTROL 목표 및 설정]** 페이지에서 성공 지표에 대한 **[!UICONTROL 전환]**&#x200B;을 선택한 다음, mbox 확인함&#x200B;**[!UICONTROL 을 작업으로 선택합니다.]**
1. **[!UICONTROL mbox 검색]** 필드에서 원하는 mbox를 선택합니다.

   ![combined_multiple_audiences4 이미지](assets/combine_multiple_audiences4.png)

1. 톱니바퀴 아이콘을 클릭한 다음, **[!UICONTROL 대상 타깃팅 추가를 클릭합니다]**.
1. **[!UICONTROL 대상/타깃팅 조건 추가]** 링크를 클릭하여 [!UICONTROL 대상 선택] 대화 상자를 표시합니다.

   ![combined_multiple_audiences5 이미지](assets/combine_multiple_audiences5.png)

1. &quot;활동을 만들 때 결합된 대상 만들기&quot;의 [2단계](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77)로 진행하여 결합된 대상을 만듭니다.

## 보고에 사용할 결합된 대상 만들기 {#section_4682D342EFBB43C38E54B99B3A1E14CD}

보고에서 사용할 결합된 임시 대상을 활동의 [!UICONTROL 목표 및 설정] 페이지에서 만들어 수 있습니다.

1. [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 편집하거나 만들 때, **[!UICONTROL 목표 및 설정]** 페이지에서 **[!UICONTROL 보고 대상]** 아래의 [!UICONTROL 대상 추가] 아이콘을 클릭하여 [!UICONTROL 대상 선택] 페이지를 표시합니다.

   ![combined_multiple_audiences6 이미지](assets/combine_multiple_audiences6.png)

1. &quot;활동을 만들 때 결합된 대상 만들기&quot;의 [2단계](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77)로 진행하여 결합된 대상을 만듭니다.

## 활동을 편집할 때 결합된 대상 만들기 {#section_364A12CE96E04B61B7C18113AA586C2C}

기존 활동을 편집할 때 결합된 임시 대상을 만들 수 있습니다.

1. [!UICONTROL 활동] 페이지에서 원하는 활동을 마우스로 가리킨 다음 **[!UICONTROL 편집]** 아이콘을 클릭합니다.

   또는

   원하는 활동을 클릭하여 연 다음, **[!UICONTROL 활동 편집을 클릭합니다]**.

1. 을(를) 클릭합니다. **[!UICONTROL 구성]** > **[!UICONTROL 대상]** > **[!UICONTROL 여러 대상]**.

   ![구성 > 대상 > 여러 대상](assets/combine_multiple_audiences7.png)

1. 활동의 현재 대상 옆에 있는 더 보기 선택 사항 아이콘(3개의 수직 줄임표)을 클릭한 다음, **[!UICONTROL 대상 변경을 클릭합니다]**.

   ![대상 변경](assets/combine_multiple_audiences8.png)

1. &quot;활동을 만들 때 결합된 대상 만들기&quot;의 [2단계](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77)로 진행하여 결합된 대상을 만듭니다.
