---
keywords: 중복 제거;중복 허용;중복 오퍼 제외;자동화된 개인화;중복 오퍼 허용 안 함;제외;기본 컨텐츠;
description: '[!UICONTROL Automated Personalization](AP) 활동에서 제외를 관리합니다.'
title: '[!UICONTROL Automated Personalization] 활동에서 제외를 관리하려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
TQID: 'https://experienceleague.adobe.com/ERpNwQPsIRBmU0vTZbGa-lYg30BYl-uJxA8UT0f6060'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 4%
---
# 제외 관리 {#manage-exclusions}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL Automated Personalization]** 활동에서 중복 오퍼를 방지하고, 특정 경험을 제외하며, 기본 콘텐츠를 제외하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

제외는 **[!UICONTROL Automated Personalization]**(AP) 활동에서 제공하는 오퍼 및 경험을 제어합니다. 동일한 오퍼가 두 번 표시되지 않도록 하고, 함께 작동하지 않는 오퍼 조합을 제거하고, 기본 콘텐츠를 제거하여 활동이 목표 및 대상자와 일치하는 더 깨끗하고 더 적절한 경험을 제공하도록 합니다.

## 중복 오퍼 허용 또는 허용 안 함 {#allow-duplicate-offers}

<a id="concept_4EF78013F80E48EFA024AE0274C9F037"></a>

AP 활동의 여러 위치에서 사용하는 경우 오퍼 라이브러리의 오퍼가 복제되지 않도록 합니다.

예를 들어 활동에는 12개의 오퍼가 있는 페이지에서 6개의 위치가 있을 수 있으므로 동일한 오퍼를 두 개 이상의 위치에 배치할 수 있습니다. 중복 오퍼를 허용하지 않으면 동일한 오퍼가 동일한 활동 내의 다른 위치에 동시에 표시되지 않습니다.

1. [AP 활동을 만들거나 편집](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity)하는 동안 **[!UICONTROL 구성]** 아이콘(![구성 아이콘](/help/main/assets/icons/Setting.svg))을 클릭하십시오.

1. 필요에 따라 이 기능을 켜거나 끄려면 **[!UICONTROL 중복 오퍼 허용]**&#x200B;을 클릭하세요.

   ![구성 아이콘](../assets/exclusion-1.png)

## 특정 경험 제외 {#exclude-experiences}

<a id="task_C17D36EF58AF4908B17A3D84CA6DE85A"></a>

특정 경험을 제외하여 AP 활동에서 특정 오퍼 조합을 제거합니다. 일부 조합이 함께 작동하지 않거나 테스트된 경험 수를 제한하여 활동의 트래픽 요구 사항을 줄일 수 있습니다.

1. [AP 활동을 만들거나 편집하는 동안](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) **[!UICONTROL 콘텐츠 관리]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭합니다.

   **[!UICONTROL 경험]** 목록에는 모든 컨텐츠 및 위치 선택 사항들의 순열에서 생성된 각 경험이 표시됩니다.

1. 테스트하지 않을 경험을 제외합니다.

   * 단일 경험을 제외하려면 **[!UICONTROL 추가 작업]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 **[!UICONTROL 제외]**&#x200B;를 클릭합니다.
   * 여러 경험을 한 번에 제외하려면 각 경험에 대한 확인란을 선택한 다음 **[!UICONTROL 제외]**&#x200B;를 클릭합니다. 하나 이상의 경험을 선택하면 **[!UICONTROL 제외]** 아이콘이 표시됩니다.

   ![경험을 일괄 제외](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   이제 경험이 활동에서 제외되며 **[!UICONTROL 상태]**&#x200B;가 **[!UICONTROL 제외됨]**(으)로 표시됩니다.

## 기본 콘텐츠 제외 {#exclude-default-content}

<a id="task_DCB4528989DF4C05A3A4729E5891D18F"></a>

위치에 기본 컨텐츠와 다른 하나의 오퍼만 포함되도록 AP 활동에 포함되지 않게 하려면 기본 컨텐츠를 제외하십시오. 또한 이 접근 방식을 사용하면 테스트하는 오퍼에 맞게 나머지 페이지의 모양과 느낌을 변경할 수 있습니다. 예를 들어 오퍼의 색상 팔레트와 일치시키기 위해 페이지의 배경색을 변경하고 기본 배경색을 제외할 수 있습니다.

1. [AP 활동을 만들거나 편집하는 동안](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) 바꿀 콘텐츠를 선택한 다음 **[!UICONTROL 텍스트/HTML 변경]**, **[!UICONTROL 이미지 오퍼 변경]** 또는 **[!UICONTROL 배경색 변경]**&#x200B;을 클릭합니다. 사용 가능한 옵션은 콘텐츠 유형에 따라 다릅니다.

   ![옵션 변경](../assets/exclusion-1.png)

1. 새 콘텐츠를 만듭니다.

1. **[!UICONTROL 추가 작업]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/Setting.svg))을 클릭한 다음 **기본 오퍼 제외/기본 오퍼 포함** 전환을 클릭하여 기본 오퍼를 제외하거나 포함합니다.

   <!--
   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)
   -->

<!--
1. Click **[!UICONTROL Save]**.

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_vec_4 image](assets/exclude_content_vec_4.png)

**To exclude default content using the [!UICONTROL Form-Based Experience Composer]:** 

1. While creating or editing an AP activity, click **[!UICONTROL Change Text/HTML]** or **[!UICONTROL Change Image Offer]** under **[!UICONTROL Content]**. 
1. In the dialog box, create your new content and uncheck **[!UICONTROL Include]** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen). 

   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![exclude_content_form_1 image](assets/exclude_content_form_1.png)

   For Image/Video content: 

   ![exclude_content_form_2 image](assets/exclude_content_form_2.png)

1. Click **[!UICONTROL Save]**. 

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)
-->
