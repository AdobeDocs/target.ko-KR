---
keywords: Analytics as reporting source;a4t;A4T;requirements
description: Adobe Target(A4T)에서 Adobe Analytics 기반 활동을 만들기 위한 사용자 계정 요구 사항입니다.
title: 사용자 권한 요구 사항
feature: a4t implementation
solution: Target,Analytics
topic: Reports and analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
translation-type: tm+mt
source-git-commit: 95e620e78fa6bcb2cded1c6efc79d365c5b70b30
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 48%

---


# 사용자 권한 요구 사항

[!DNL Adobe Target] (A4T)에서 [!DNL Adobe Analytics] 기반 활동을 만들기 위한 사용자 계정 요구 사항에 대한 정보입니다.

[!DNL Analytics] 활동을 정의할 때 보고서 세트를 선택하려면 [!DNL Analytics] 사용자 계정과 [!DNL Target] 사용자 계정이 둘 다 필요합니다.

다음 섹션에 설명된 대로 사용자 계정을 구성해야 합니다.

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

[!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com)에서 다음 작업을 완료하십시오.

### 솔루션 계정을 Adobe ID에 연결합니다

[!DNL Analytics] 및 [!DNL Target] 사용자 계정이 Adobe ID에 연결되어 있어야 합니다.

For more information, see [Organizations and account linking](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Experience Cloud 그룹 멤버십 구성

하나 이상의 [!DNL Experience Cloud] 그룹의 구성원으로서 [!DNL Analytics] 및 [!DNL Target]에 액세스할 수 있어야 합니다.

자세한 내용은 Experience Cloud 사용자 및 제품 [관리를 참조하십시오](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Configure access to the [!DNL Analytics] report suite:

지정된 보고서 세트에서 A4T를 사용하려면 해당 보고서 세트에 액세스할 수 있어야 합니다.

1. Admin Console **[!UICONTROL 에서]**[!DNL Analytics] 제품 프로필을 클릭한 다음 권한 **[!UICONTROL 탭을]** 클릭합니다.

   그러면 프로필에서 액세스할 수 있는 보고서 세트를 볼 수 있습니다.

1. 액세스할 보고서 세트가 사용자가 속한 제품 프로필에 나열된 보고서 중 [!DNL Target] 하나인지 확인합니다.

   다음 그림은 모든 보고서 세트에 액세스할 수 있는 제품 프로필의 예입니다.

   ![Admin Console 권한 탭](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

추가적인 권한이 필요하지 않습니다.
