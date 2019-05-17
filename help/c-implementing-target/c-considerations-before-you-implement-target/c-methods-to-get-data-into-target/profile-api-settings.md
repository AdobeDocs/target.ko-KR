---
description: API를 통해 묶음 업데이트에 대한 인증을 활성화 또는 비활성화하고 프로필 인증 토큰을 생성합니다.
keywords: 구현;api;프로필;프로필 api 설정
seo-description: API를 통해 묶음 업데이트에 대한 인증을 활성화 또는 비활성화하고 프로필 인증 토큰을 생성합니다.
seo-title: 프로필 API 설정
solution: Target
subtopic: 시작하기
title: 프로필 API 설정
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 프로필 API 설정{#profile-api-settings}

API를 통해 묶음 업데이트에 대한 인증을 활성화 또는 비활성화하고 프로필 인증 토큰을 생성합니다.

Adobe Target은 모든 개별 사용자에 대한 프로필을 작성하고 유지 관리합니다. 이 프로필은 Target 에지 클러스터에 저장되며 모든 방문 후 실시간으로 업데이트되지만, API를 통해 프로필을 개별적으로 또는 벌크로 업데이트할 수 있습니다.

추가 보안을 위해 벌크 업데이트 API 호출 시 요청의 헤더에서 전달할 올바른 액세스 토큰을 요구할 수 있습니다. 승인자 권한이 있는 사용자는 프로필 API 인증 토큰을 생성하고 활성화할 수 있습니다.

**Target UI를 사용하여 인증을 요구하고 액세스 토큰을 생성하려면 다음을 수행하십시오.**

1. **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]**을 클릭합니다.
1. **[!UICONTROL 프로필 API 설정]**에서 **인증 필요[!UICONTROL 드롭다운 목록을 사용하여 인증 요구 사항을 활성화 또는 비활성화합니다.]**

   ![](assets/profile_api_settings.png)

1. (조건부) 인증 요구 사항을 활성화했다면 **[!UICONTROL 프로필 인증 토큰 생성을 클릭하십시오]**.

   ![](assets/profile_api_settings_2.png)

   토큰은 [!UICONTROL 다음 기간 후에 만료] 상자에 나열된 시간에 따라 만료됩니다.

   >[!NOTE]
   >
   >API를 통해 프로필 인증 토큰을 생성할 수도 있습니다. 자세한 내용은 [Adobe Target 개발자 웹 사이트](https://developers.adobetarget.com/)에서 [프로필](https://developers.adobetarget.com/api/#profiles)을 참조하십시오.

1. 토큰을 복사하고 &quot;Authorization&quot; : &quot;Bearer &quot; 형식으로 요청 헤더에 포함합니다.

필요에 따라 토큰을 재생성하려면 [!UICONTROL 프로필 인증 토큰 재생]을 클릭하십시오.

>[!IMPORTANT]
>
>이 토큰을 재설정하면 현재 토큰을 사용하는 API 호출이 실패하게 됩니다. 따라서 이 토큰을 재설정한 경우 이 토큰을 사용하는 모든 스크립트나 앱을 업데이트해야 합니다.

