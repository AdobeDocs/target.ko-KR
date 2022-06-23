---
keywords: 구현;api;프로필;프로필 api 설정;인증 토큰
description: Adobe을 통해 배치 업데이트에 대한 인증을 구성하는 방법을 알아봅니다 [!DNL Target] API 및 프로필 인증 토큰을 생성합니다.
title: 프로필 API 설정을 사용하여 배치 업데이트를 활성화 또는 비활성화하려면 어떻게 합니까?
feature: APIs/SDKs
role: Developer
exl-id: 6346e11b-0853-47f1-9706-69e8635a6f25
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 59%

---

# 프로필 API 설정

를 통해 배치 업데이트에 대한 인증을 활성화 또는 비활성화합니다 [!DNL Adobe Target] API 및 프로필 인증 토큰을 생성합니다.

[!DNL Adobe Target] 모든 개별 사용자에 대해 프로필을 만들고 유지 관리합니다. 이 프로필은 [!DNL Target] edge cluster 및 를 방문할 때마다 실시간으로 업데이트됩니다. 그러나 API를 통해 개별적으로 또는 대량으로 프로필을 업데이트할 수 있습니다.

추가 보안을 위해 벌크 업데이트 API 호출 시 요청의 헤더에서 전달할 올바른 액세스 토큰을 요구할 수 있습니다.

**Target UI를 사용하여 인증을 요구하고 액세스 토큰을 생성하려면 다음을 수행하십시오.**

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭합니다.
1. 아래 **[!UICONTROL 프로필 API]** 슬라이드 **[!UICONTROL 인증 필요]** 활성화 또는 비활성화 위치로 전환합니다.

   ![](assets/profile_api_settings.png)

1. (조건부) 인증 요구 사항을 활성화한 경우 **[!UICONTROL 새 프로필 인증 토큰 생성]**.

   ![](assets/profile_api_settings_2.png)

   토큰은 [!UICONTROL 다음 기간 후에 만료] 상자에 나열된 시간에 따라 만료됩니다.

   인증 토큰을 생성하려면 다음 사용자 권한 중 하나가 있어야 합니다.

   * 최소 [!UICONTROL 편집자] 권한(또는 [!UICONTROL 승인자])

      . [!DNL Target Standard] 고객에 대한 자세한 내용은 사용자에서 [역할 및 권한 지정](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions)을 *참조하십시오*. [!DNL Target Premium] 고객에 대한 자세한 내용은 [기업 권한 구성](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md)을 참조하십시오.

   * 작업 영역/제품 프로필 수준에서 관리자 역할

      작업 영역은 [!DNL Target Premium] 고객만 사용할 수 있습니다. 자세한 내용은 [기업 권한 구성](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md)을 참조하십시오.

   * [!DNL Adobe Target] 제품 수준의 관리자 권한(Sysadmin 권한)
   >[!NOTE]
   >
   >API를 통해 프로필 인증 토큰을 생성할 수도 있습니다. 자세한 내용은 [Adobe Target 개발자 웹 사이트](https://developers.adobetarget.com/)에서 [프로필](https://developers.adobetarget.com/api/#profiles)을 참조하십시오.

1. 토큰을 복사하고 &quot;Authorization&quot; : &quot;Bearer &quot; 형식으로 요청 헤더에 포함합니다.

클릭 [!UICONTROL 새 프로필 인증 토큰 생성] 필요한 경우 토큰을 재생성합니다.

>[!IMPORTANT]
>
>이 토큰을 재설정하면 현재 토큰을 사용하는 API 호출이 실패하게 됩니다. 따라서 이 토큰을 재설정한 경우 이 토큰을 사용하는 모든 스크립트나 앱을 업데이트해야 합니다.
