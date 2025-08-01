---
keywords: 관리;승인자 역할;승인자
description: ' [!DNL Adobe Target] 관리자가  [!DNL Adobe Experience Cloud]에 대한 전자 메일 초대를 받은 후 수행해야 하는 첫 번째 작업을 수행합니다.'
title: ' [!DNL Target] 관리를 시작하려면 어디서 시작해야 합니까?'
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
source-git-commit: 614fd89c9746ce55f502debd5b689c34de400ae5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 32%

---

# 관리자의 첫 단계

이 문서에는 [!DNL Adobe Target] 관리자가 [!DNL Adobe Experience Cloud]에 대한 이메일 초대를 받은 후 수행해야 하는 첫 번째 단계가 포함되어 있습니다.

## [!DNL Target]&#x200B;(으)로 초대 받기 {#task_3E0817630774431983FAA3D2CB2E75BD}

[!DNL Adobe Admin Console]의 시스템 관리자가 귀하를 가입하도록 초대하여 [!DNL Target]에서 사용자로 추가해야 합니다. 그런 다음 시스템 관리자가 귀하를 하나 이상의 역할별 제품 프로필(사용자 그룹)에 추가해야 합니다. 이러한 작업은 모두 [Adobe Admin Console](https://adminconsole.adobe.com)에서 수행됩니다.

자세한 내용은 [사용자 그룹 관리](https://helpx.adobe.com/kr/enterprise/using/users.html)를 참조하십시오.

시스템 관리자가 이러한 단계를 수행하면 초대 이메일을 받게 됩니다.

## 초대 수락 {#task_24FE66659E634B24AB61DB8497772E17}

[!DNL Adobe Experience Cloud]에 가입하라는 초대를 받으면 초대를 수락하고 로그인한 다음 [!UICONTROL End User License Agreement]&#x200B;(EULA)에 동의하십시오.

1. [!DNL Adobe Experience Cloud] 에 대한 초대를 수락합니다.
1. Adobe ID가 없는 경우 ID를 만들라는 메시지가 표시됩니다.

   Adobe ID이 있는 경우 Adobe ID이 인식되면 로그인하라는 메시지가 표시됩니다.
1. [!UICONTROL Terms of Use]을(를) 수락합니다.
1. 지금까지 수행한 작업에 대한 요약을 검토하고 **[!UICONTROL Continue to Experience Cloud]**&#x200B;을(를) 클릭합니다.
1. [!DNL Adobe Experience Cloud]에 로그인하고 **[!UICONTROL Link Account]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >계정을 연결하지 않으면 [!DNL Target]에 액세스할 수 없습니다.

   모든 [!UICONTROL Experience Cloud] 제품이 연결 페이지에 표시됩니다. `Link Target`을(를) 클릭하고 [!DNL Target] 사용자 이름과 암호를 입력하여 [!DNL Target]에 액세스합니다.
1. **[!UICONTROL Continue to Experience Cloud]** 아이콘을 클릭합니다.

   이 시점에서는 연결할 자격이 있는 그룹이 아직 설정되어 있지 않습니다.
1. 원할 경우 [!DNL Adobe Experience Cloud]를 소개하는 비디오를 시청하십시오.
1. 본인의 새 권한을 확인하고 제품에 액세스하려면 [!DNL Adobe Experience Cloud]에서 로그아웃했다가 다시 로그인하십시오.
1. 다음 단계로 계속하여 [자신에게 승인자 역할을 지정](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7)합니다.

## 자기 자신에게 승인자 역할 지정 {#task_15CAA437A71444E2932B333D5E66A3C7}

[!DNL Adobe Experience Cloud] 가입 초대를 수락하고 로그인한 후 [!DNL Target]이(가) [!DNL Experience Cloud] 계정에 추가되었는지 확인한 다음, [!UICONTROL Approver]에 대한 [!DNL Target] 역할을 자신에게 할당하십시오.

조직에 [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) 라이센스가 있는 경우 *사용자*&#x200B;의 [역할 및 권한 지정](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions)을 참조하십시오.

조직에 [Target Premium](/help/main/c-intro/intro.md#premium) 라이센스가 있는 경우 *Enterprise 권한 구성*&#x200B;에서 [6단계: 역할 및 권한 지정](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80)을 참조하십시오.

다음 단계는 [!DNL Target Standard] 및 [!DNL Target Premium]에서 사용자를 설정하는 것입니다. 자세한 내용은 [사용자 관리](/help/main/administrating-target/c-user-management/user-management.md)를 참조하십시오.

## [!UICONTROL Administration] 설정을 편집하는 데 필요한 권한 {#admin-permissions}

**2025년 4월 22일 이전**: [!UICONTROL Approvers]에 [!DNL Adobe Admin Console] 권한이 있는 사용자는 [[!UICONTROL Administration] 역할에 관계없이 ](/help/main/administrating-target/administrating-target.md)의 [!DNL Target] 페이지[!DNL Target] 페이지에서 모든 설정을 편집하거나 변경할 수 있습니다.

**2025년 4월 22일**: [!UICONTROL Product] 및 [!UICONTROL Solutions] 관리자만 [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) 작업 영역의 역할에 관계없이 [!DNL Target] 섹션의 설정을 업데이트할 수 있습니다. 이 권한이 없는 사용자는 [!UICONTROL Administration] 섹션에 대한 읽기 전용 액세스 권한을 갖게 됩니다.

이 업데이트는 [!DNL Target] 인스턴스 구성에 대한 조직의 제어를 강화하여 다양한 테스트 및 개인화 팀의 활동 전달에 영향을 줄 수 있는 우발적인 업데이트를 방지합니다.
