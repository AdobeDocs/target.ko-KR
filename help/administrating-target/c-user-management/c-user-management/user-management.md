---
keywords: add user;manage user;user permissions
description: Adobe Target에 사용자를 추가하고 Adobe Admin Console에서 해당 권한을 관리할 수 있습니다.
title: 사용자
feature: user management
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 46%

---


# 사용자{#users}

You can add users and manage their permissions in the [!DNL Adobe Admin Console].

>[!NOTE]
>
>[!UICONTROL 속성 및 권한 기능은 ] Premium 솔루션의 일부로 사용할 수 있습니다. [!DNL Target] 이 기능은 [!DNL Target] Premium 라이센스가 없는 [!DNL Target] Standard에서는 사용할 수 없습니다.
>You can tell whether your organization has a Standard or Premium license by clicking the [!UICONTROL Administration] link at the top of the [!DNL Target] UI.
>
>* **[!DNL Target]표준 고객**:[ [!UICONTROL 관리]] 탭([!UICONTROL 속성]탭 **[!UICONTROL 아님)이 표시되는 경우(]** 속성 [!DNL Target] 탭)에는표준 라이선스가 있습니다. [!DNL Target] Standard 고객은 이 문서의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 지정해야 합니다.
   >
   >
* **[!DNL Target]프리미엄 고객**:[ [!UICONTROL 사용자] ] 탭 및 [!UICONTROL 속성] 탭([[!UICONTROL 관리] > [속성]])이 표시되면 [!DNL Target] 조직에프리미엄 라이선스가 있는 것입니다. [!DNL Target] Premium 고객은 [엔터프라이즈 사용자 권한](/help/administrating-target/c-user-management/property-channel/property-channel.md) 및 [엔터프라이즈 권한 구성](/help/administrating-target/c-user-management/property-channel/properties-overview.md)의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 지정해야 합니다.
>
>
사용자 및 권한 관리 방법에 대한 자세한 내용은 [엔터프라이즈 및 팀 사용자 안내서의 제품 및 프로필](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) 관리를 *참조하십시오*.

[!DNL Adobe Target]을 시작하면 [!DNL Adobe Experience Cloud] 계정에 미리 채워져 있는 ID(Adobe.com으로 끝남)를 발견하게 됩니다. These IDs are for members of [!DNL Adobe] teams so that they can assist you with your new account and with your use of [!DNL Adobe Target], should you need help. 지원을 받으려면 일반적인 방법으로 Adobe 팀에 문의하십시오.

You will not see the new user listed on the [!UICONTROL Users] page until the user logs in using his or her [!DNL Adobe Experience Cloud] account and then logs in to [!DNL Target Standard/Premium].

기본적으로 모든 [!DNL Target] 사용자는 관찰자 권한으로 시작합니다.

Admin users are identified in the [!UICONTROL Users] list. 액세스 수준을 변경해야 하는 경우 시스템 관리자 사용자 중 한 명에게 문의하십시오.

## Target 내에서 사용자 정보 보기

Target 환경에서 작업 공간당 역할 및 Target 내에서 직접 이메일 주소를 포함하여 현재 사용자의 목록을 볼 수 있습니다.

사용자 페이지를 보려면 관리 **** > **[!UICONTROL 사용자를]**&#x200B;클릭합니다.

![Target 내의 사용자 목록](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>기존 사용자를 관리하거나 새 사용자를 추가하려면 아래 설명된 대로 [!UICONTROL Adobe Admin Console]를 사용해야 합니다.

## Adobe Admin Console 액세스 {#access}

Adobe Admin Console에서 수행되는 작업의 경우 다음 절차에 따라 콘솔에 액세스하십시오.

1. 내에서 [!DNL Target]관리 **[!UICONTROL > 사용자]** **[!UICONTROL > 사용자]** 관리 **[!UICONTROL 를]**&#x200B;클릭합니다.

   또는

   Go to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/), then sign in using your Adobe ID, if you have not already logged in.

1. (조건부) 두 개 이상의 조직을 위한 [!DNL Admin Console for Enterprise]에 액세스할 수 있는 경우 오른쪽 모서리나 맨 위 탐색 막대의 사용자 아바타를 클릭한 다음, 원하는 조직을 선택하십시오.

## Add users {#add-users}

모든 사용자 관리는 [!DNL Adobe Admin Console for Enterprise]에서 수행해야 합니다. 그러나 [!DNL Target]의 모든 기존 사용자는 [!DNL Target]에서 [!DNL Admin Console for Enterprise]로 마이그레이션됩니다.

1. [Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)에서 **[!UICONTROL 사용자]** > 사용자 **[!UICONTROL 를 클릭하여]** 새 사용자를 만들거나 기존 사용자를 편집합니다.
1. *Enterprise 사용 안내서*&#x200B;의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## Create user groups {#user-groups}

개발자, 분석가, 마케터, 경영진 등과 같은 사용자 그룹을 만든 다음 여러 Adobe 제품 및 작업 공간에서 권한을 지정할 수 있습니다. 새 팀 구성원에게 다른 Adobe 제품에 대한 모든 적절한 권한을 지정하면 특정 사용자 그룹에 팀 구성원을 쉽게 추가할 수 있습니다.

1. [Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)에서 **[!UICONTROL 사용자]** > **[!UICONTROL 사용자 그룹]** 을 클릭하여새 사용자 그룹을 만들거나 기존 그룹을 편집합니다.
1. *Enterprise 사용 안내서*&#x200B;의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## Specify roles and permissions {#roles-permissions}

시스템 관리자만 [!DNL Target]에서 사용자 역할을 설정할 수 있습니다. For example, a Standard approver user cannot change an observer to an approver, without also having [!DNL Experience Cloud] Admin rights.

시스템 관리자 사용자는 시스템에 사용자를 추가해야 합니다. 사용자는 자동으로 추가되지 않습니다. They are invited by email from the [!DNL Experience Cloud] and must confirm their email addresses before their accounts are registered.

1. [Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)에서 **[!UICONTROL 제품]**&#x200B;을 클릭한 다음, 원하는 제품의 이름을 선택합니다.

   ![제품 탭](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. 원하는 작업 공간(예: 기본 작업 공간)을 클릭합니다.

   ![기본 작업 공간](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   [!UICONTROL 사용자] 탭에는 해당 작업 공간의 모든 사용자가 표시됩니다.

   ![구성 사용자](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. [!UICONTROL 제품 역할] 열의 각 사용자에 대한 드롭다운 목록을 사용하여 원하는 권한 역할(승인자, 편집자 또는 관찰자)을 선택합니다.

   ![제품 역할 드롭다운 목록](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | 역할 | 설명 |
   |--- |--- |
   | 승인자 | 활동을 만들고, 편집하고 활성화하거나 중지할 수 있습니다. |
   | 편집자 | 활동이 라이브 상태가 되기 전에 활동을 만들고 편집할 수 있지만 활동 시작을 승인할 수는 없습니다. |
   | 관찰자 | 활동을 볼 수 있지만 만들거나 편집할 수는 없습니다. |
   | 게시자 | 옵저버 역할과 유사(활동을 볼 수 있지만 만들거나 편집할 수는 없음) 그러나 게시자 역할에는 활동을 활성화할 수 있는 추가 권한이 있습니다. |

자세한 내용은 *Enterprise 사용 안내서*&#x200B;의 [Admin Console에서 제공 권한 및 역할 관리](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html)를 참조하십시오.

## Training video: How to Configure Target Workspaces ![Tutorial badge](/help/assets/tutorial.png)

학습 목표:

* Adobe Target 인터페이스에서 Adobe Admin Console에 액세스(3가지 방법)
* Adobe Admin Console에서 작업 공간 구성
   * 작업 공간에 사용자 추가
   * 작업 공간에 속성 추가
* 기본 작업 공간 이해

>[!NOTE]
>
>관리 [!DNL Target]  메뉴 UI(이전 [!UICONTROL 설정])는 향상된 성능을 제공하고, 새로운 기능을 출시할 때 필요한 유지 관리 시간을 단축하고, 제품 전반의 사용자 경험을 개선하기 위해 다시 설계되었습니다. 다음 비디오의 정보는 일반적으로 정확하다.그러나 옵션이 약간 다를 수 있습니다. 업데이트된 비디오가 곧 게시될 예정입니다.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
