---
keywords: 깜박임, 사전 숨기기, 사전 숨김, 개인화, 구현, 깜박임 방지, VEC, 시각적 경험 작성기
description: 계정 수준 설정, 간단한 페이지 라이브러리 및 활동별 컨트롤을 사용하여 활성 Adobe Target 개인화가 변경되는 영역만 숨김으로써 콘텐츠 사전 숨김이 깜박임을 줄이는 방법에 대해 알아봅니다.
title: 개인화된 경험을 위한 콘텐츠 사전 숨김
feature: Administration & Configuration
role: Admin
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
source-git-commit: 77741253fdfb007d0eda0c57fe293df2f9c638a2
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 3%

---

# 개인화된 경험을 위한 콘텐츠 사전 숨김

>[!AVAILABILITY]
>
>개인화된 콘텐츠에 대한 콘텐츠 사전 숨김은 **베타** 기능으로 사용할 수 있습니다.

방문자가 페이지를 로드할 때 기본 콘텐츠가 잠깐 나타났다가 [!DNL Adobe Target]에서 개인화된 콘텐츠로 바뀔 수 있습니다. 보이는 스위치를 종종 **깜박임**&#x200B;이라고 하며 이는 개인화 프로그램의 일반적인 경험 문제입니다.

콘텐츠 사전 숨김을 사용하면 페이지 로드 중에 활동이 개인화하는 페이지의 일부만 숨겨 깜박임을 관리할 수 있으므로 고객에게 깜박임이 적고 빈 화면 시간이 줄어듭니다.

다음은 계정 기본값에서 페이지 구현 및 활동별 선택 사항에 이르기까지 콘텐츠 사전 숨김이 작동하는 방식입니다.

1. 계정에 대해 콘텐츠 사전 숨김을 활성화하여 전역 기본값을 설정합니다. 기본적으로 꺼져 있습니다. [자세히 알아보기](#content-pre-hiding-enable-account)

1. 개인화 활동을 실행하는 모든 페이지의 `<head>`에 콘텐츠 사전 숨김 라이브러리를 추가합니다.

1. [!DNL Target]이(가) 라이브 [!UICONTROL Visual Experience Composer] 및 [!UICONTROL Enhanced Experience Composer] 활동에서 규칙 집합을 만듭니다. 규칙 집합은 게재가 변경될 수 있는 선택기 및 영역을 나열합니다.

   [!UICONTROL Form-Based Composer] 활동은 지원되지 않습니다.

1. 라이브러리는 Adobe CDN에서 해당 규칙 세트를 가져오고 개인화된 콘텐츠가 로드되는 동안에만 일치하는 요소를 사전에 숨깁니다.

1. **[!UICONTROL Goals & Settings]**&#x200B;에서 개별 활동에 대해 **[!UICONTROL Content pre-hiding]**&#x200B;을(를) 비활성화할 수 있지만 계정 수준에서 활성화된 경우에만 가능합니다. [자세히 알아보기](#content-pre-hiding-activity)

## 인스턴스에 대해 콘텐츠 사전 숨기기 활성화 {#content-pre-hiding-enable-account}

>[!IMPORTANT]
>
>인스턴스에 대해 콘텐츠 사전 숨김을 사용하려면 **관리자**&#x200B;여야 합니다.

콘텐츠 사전 숨김은 활성화할 때까지 인스턴스에 대해 해제됩니다. **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**&#x200B;을(를) 사용하여 기능을 켜고 기본값을 설정한 다음 구현 팀에 대한 다운로드에 액세스하십시오.

1. [!DNL Target]에서 **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Content pre-hiding]** 메뉴에서 콘텐츠 사전 숨김 옵션을 활성화합니다.

   ![](assets/content-pre-hiding-1.png)

1. 필요한 경우 **[!UICONTROL Pre-hiding timeout]**&#x200B;을(를) 초 단위로 업데이트합니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다. 그러면 플리커 관리 설정이 인스턴스에 적용됩니다.

1. 활성화하면 **[!UICONTROL Download]**&#x200B;을(를) 클릭한 다음 [!DNL at.js] 또는 [!DNL Web SDK] 전에 로드되도록 `<head>` 페이지에 파일을 추가하십시오. 전체 구현 지침은 [콘텐츠 사전 숨김 SDK](https://experienceleague.adobe.com/ko/docs/target-dev/developer/client-side/prehide-sdk)을 참조하십시오.

   ![](assets/content-pre-hiding-2.png)

이제 인스턴스는 저장된 콘텐츠 사전 숨김 및 시간 초과 설정을 옵트인하는 활동의 기본값으로 사용합니다.

## 활동에 대해 컨텐츠 사전 숨김 활성화 {#content-pre-hiding-activity}

인스턴스에 대해 사전 숨김을 활성화한 상태에서 각 활동이 **[!UICONTROL Goals & Settings]**&#x200B;에서 이를 사용하는지 여부를 선택합니다. 사전 숨김을 활성화하는 활동은 라이브 상태일 때 타깃팅된 동작에 포함됩니다.

그런 다음 [!DNL Target]은(는) [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 및 [!UICONTROL Form-Based Composer]에서 작성된 라이브 활동에서 게재가 변경될 수 있는 선택기와 영역을 설명하는 간단한 규칙 집합을 만듭니다.

활동을 만들거나 편집할 때:

1. 사전 숨김 옵션을 활성화할 활동에 액세스합니다.

1. **[!UICONTROL Edit activity]** 드롭다운에 액세스하여 **[!UICONTROL Edit Goals & Settings]**&#x200B;을(를) 선택합니다.

   ![](assets/content-pre-hiding-3.png)

1. **[!UICONTROL Content pre-hiding]** 메뉴에서 **[!UICONTROL Enable content pre-hiding]** 옵션을 전환하여 이 활동을 사전 숨김에서 옵트인하거나 옵트아웃합니다.

   ![](assets/content-pre-hiding-4.png)

1. 완료되면 **[!UICONTROL Save & Close]**&#x200B;을(를) 클릭합니다.

활동을 저장하고 실행 또는 비활성화하면 규칙 세트가 업데이트되어 각 론치에 대한 페이지 코드를 편집하지 않고도 사전 숨김 상태가 실제로 전달되는 내용과 일치합니다.

방문자 측에서 라이브러리는 각 페이지 로드 시 Adobe CDN에서 해당 규칙 세트를 검색하고 개인화된 콘텐츠가 준비될 때까지 필요한 경우에만 일치하는 요소를 사전에 숨깁니다.
