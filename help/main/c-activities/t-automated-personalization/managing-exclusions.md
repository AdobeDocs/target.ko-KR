---
keywords: 중복 제거;중복 허용;중복 오퍼 제외;자동화된 개인화;중복 오퍼 허용 안 함;제외;기본 컨텐츠;
description: '[!UICONTROL Automated Personalization]​(AP) 활동에서 제외를 관리합니다.'
title: '[!UICONTROL Automated Personalization] 활동에서 제외를 관리하려면 어떻게 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: a68e7501fbb157a1ac5b0c0cbb3d574abdb747dd
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 21%

---

# 제외 관리

제외를 마스터하여 [!UICONTROL Automated Personalization]&#x200B;(AP) 전략을 제어하십시오. 중복 오퍼를 방지하거나, 경험 조합을 개선하거나, 기본 콘텐츠를 제거하든 관계없이 제외를 사용하면 목표 및 대상의 기대에 부합하는 보다 청결하고 관련성이 높은 경험을 제공할 수 있습니다.

## 중복 오퍼 허용 또는 허용 안 함 {#concept_4EF78013F80E48EFA024AE0274C9F037}

AP 활동의 여러 위치에서 사용하는 경우 오퍼 라이브러리의 오퍼가 복제되지 않도록 합니다.

예를 들어, 12개의 오퍼가 있는 페이지에 6개의 위치가 있는 활동이 있을 수 있습니다. 활동에서 하나 이상의 위치에 동일한 오퍼를 배치할 수 있습니다. 이 기능을 사용하면 동일한 활동 내의 다른 위치에 중복 오퍼가 동시에 표시되지 않도록 할 수 있습니다.

1. [AP 활동을 만들거나 편집](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)하는 동안 **[!UICONTROL Configure]** 아이콘(![구성 아이콘](/help/main/assets/icons/Setting.svg) )을 클릭하고 **[!UICONTROL Allow Duplicate Offers]**&#x200B;을 클릭하여 필요에 따라 이 기능을 켜거나 끕니다.

## 특정 경험 제외 {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

AP 활동에서 특정 오퍼 조합을 제외하려면 특정 경험을 제외하십시오.

함께 작동하지 않는 특정 조합이 있을 수 있으며, 또는 활동에 대한 트래픽 요구 사항을 줄이기 위해 테스트한 경험 수를 제한할 수 있습니다.

1. [AP 활동을 만들거나 편집하는 동안](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) **콘텐츠 관리** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭합니다.

   [!UICONTROL Experiences] 목록에는 모든 콘텐츠 및 위치 옵션의 순열에서 생성된 각 경험이 표시됩니다.

1. 원하는 대로 환경을 제외합니다.

   [!UICONTROL **추가 작업**] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 [!UICONTROL **제외**]&#x200B;를 클릭하여 특정 경험을 제외할 수 있습니다.

   또는 관련 경험에 대한 확인란을 선택한 다음 **[!UICONTROL Exclude]**&#x200B;을(를) 클릭하여 경험을 묶음으로 제외할 수 있습니다. 하나 이상의 경험을 선택하면 [!UICONTROL Exclude] 아이콘이 표시됩니다.

   ![경험을 일괄 제외](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   이제 경험이 활동에서 제외되고 해당 [!UICONTROL Status]이(가) [!UICONTROL Excluded]&#x200B;(으)로 표시됩니다.

## 기본 콘텐츠 제외 {#task_DCB4528989DF4C05A3A4729E5891D18F}

경우에 따라 기본 콘텐츠를 AP 활동의 일부로 포함하지 않을 수 있습니다. 이 메서드를 사용하면 활동의 일부로 위치에 하나의 오퍼(기본 컨텐츠와 다름)만 있을 수 있습니다.

기본 콘텐츠를 제외하는 것은 사용자가 AP 활동으로 테스트하는 오퍼에 맞게 나머지 페이지의 모양과 느낌을 변경할 수 있는 좋은 방법입니다. 예를 들어, 테스트 중인 오퍼의 색상 팔레트를 일치시키려는 경우 페이지의 배경색을 변경하고 기본 배경색을 제외할 수 있습니다.

**VEC([!UICONTROL Visual Experience Composer])를 사용하여 기본 콘텐츠를 제외하려면:**

1. [AP 활동을 만들거나 편집](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)하는 동안 바꿀 콘텐츠를 선택하고 클릭하여 **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image Offer]** 또는 **[!UICONTROL Change Background Color]**&#x200B;에 액세스하십시오. 사용 가능한 옵션은 콘텐츠 유형에 따라 다릅니다.

   ![옵션 변경](/help/main/c-activities/t-automated-personalization/assets/options.png)
1. 새 콘텐츠를 만듭니다.

1. **[!UICONTROL More Actions]**(![추가 작업 아이콘](/help/main/assets/icons/Setting.svg)) 아이콘을 클릭한 다음 **기본 오퍼 제외/기본값 포함**/ 전환을 클릭하여 기본 오퍼를 제외하거나 포함하십시오.

   <!-- Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)-->

<!-- 1. Click **[!UICONTROL Save]**.

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

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)-->
