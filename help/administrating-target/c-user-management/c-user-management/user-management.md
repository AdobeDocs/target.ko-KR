---
description: 사용자를 추가하고 Adobe Admin Console에서 사용자 권한을 관리할 수 있습니다.
keywords: 사용자 추가;사용자 관리;사용자 권한
seo-description: 사용자를 추가하고 Adobe Admin Console에서 사용자 권한을 관리할 수 있습니다.
seo-title: 사용자
solution: Target
subtopic: 시작하기
title: 사용자
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 사용자{#users}

사용자를 추가하고 Adobe Admin Console에서 사용자 권한을 관리할 수 있습니다.

>[!NOTE]
>
>[!UICONTROL ][!UICONTROL 속성 및 권한 기능은 ] Premium 솔루션의 일부로 사용할 수 있습니다. [!DNL Target] 이 기능은 [!DNL Target] Premium 라이센스가 없는 [!DNL Target] Standard에서는 사용할 수 없습니다.
> UI의 맨 위에서 [!UICONTROL 설정] 링크를 클릭하여 조직에 Standard 라이센스나 Premium 라이센스가 있는지 여부를 알 수 있습니다.[!DNL Target]
>
>**[!DNL Target]Standard 고객**: [!UICONTROL 사용자] 탭([!UICONTROL 설정 &gt; 사용자])이 표시된다면, 조직에 [!DNL Target] Standard 라이센스가 있는 것입니다. [!DNL Target Standard 고객은 이 문서의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 지정해야 합니다.
>
>**[!DNL Target]Premium 고객**: [!UICONTROL 속성] 탭([!UICONTROL 설정 &gt; 속성])이 표시되면 조직에 [!DNL Target] Premium 라이센스가 있는 것입니다. [!DNL Target] Premium 고객은 [엔터프라이즈 사용자 권한](/help/administrating-target/c-user-management/property-channel/property-channel.md) 및 [엔터프라이즈 권한 구성](/help/administrating-target/c-user-management/property-channel/properties-overview.md)의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 지정해야 합니다.

시스템 관리자만 사용자를 추가하고 사용자의 권한을 관리할 수 있습니다. 시스템 관리자 역할은 [!DNL Experience Cloud] 수준에서 지정됩니다. [!DNL Experience Cloud] 역할은 각 솔루션에서 관리되는 역할과 별도입니다.

[!DNL Adobe Target]을 시작하면 [!DNL Adobe Experience Cloud] 계정에 미리 채워져 있는 ID(Adobe.com으로 끝남)를 발견하게 됩니다. 이 ID는 Adobe 팀의 구성원용으로서, 도움이 필요할 경우 새 계정과 [!DNL Adobe Target] 사용과 관련하여 여러분을 지원할 수 있습니다. 지원을 받으려면 일반적인 방법으로 Adobe 팀에 문의하십시오.

사용자가 Adobe Experience Cloud 계정을 사용하여 로그인한 다음, [!UICONTROL  카드를 클릭하여 ]에 로그인하기 전까지는 [!DNL Target Standard/Premium]사용자[!DNL Target] 페이지에 새 사용자가 표시되지 않습니다.

기본적으로 모든 [!DNL Target] 사용자는 관찰자 권한으로 시작합니다.

시스템 관리자는 사용자 목록에서 식별됩니다. 액세스 수준을 변경해야 할 경우 해당 시스템 관리자 사용자 중 한 명에게 문의하십시오.

## Adobe Admin Console 액세스 {#access}

Adobe Admin Console에서 수행되는 작업의 경우 다음 절차에 따라 콘솔에 액세스하십시오.

1. 아직 로그인하지 않은 경우 [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)로 이동하고 Adobe ID를 사용하여 로그인합니다.

   또는

   If you are already logged in to the Experience Cloud, go to [https://www.experiencecloud.adobe.com](https://experiencecloud.adobe.com), then click the [!UICONTROL App] icon in the top navigation bar &gt; click **[!UICONTROL Admin]** on the right side.

1. (조건부) 두 개 이상의 조직을 위한 [!DNL Admin Console for Enterprise]에 액세스할 수 있는 경우 오른쪽 모서리나 맨 위 탐색 막대의 사용자 아바타를 클릭한 다음, 원하는 조직을 선택하십시오.

## 사용자 추가 {#add-users}

모든 사용자 관리는 [!DNL Adobe Admin Console for Enterprise]에서 수행해야 합니다. 그러나 [!DNL Target]의 모든 기존 사용자는 [!DNL Target]에서 [!DNL Admin Console for Enterprise]로 마이그레이션됩니다.

1. [관리 콘솔에서](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)**[!UICONTROL 사용자]** &gt; **[!UICONTROL 사용자를]** 클릭하여 새 사용자를 만들거나 기존 사용자를 편집합니다.
1. *Enterprise 사용 안내서*의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## 사용자 그룹 만들기 {#user-groups}

개발자, 분석가, 마케터, 경영진 등과 같은 사용자 그룹을 만든 다음 여러 Adobe 제품 및 작업 공간에서 권한을 지정할 수 있습니다. 새 팀 구성원에게 다른 Adobe 제품에 대한 모든 적절한 권한을 지정하면 특정 사용자 그룹에 팀 구성원을 쉽게 추가할 수 있습니다.

1. [관리 콘솔에서](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)**[!UICONTROL 사용자]** &gt; **[!UICONTROL 사용자 그룹을]** 클릭하여 새 사용자 그룹을 만들거나 기존 그룹을 편집합니다.
1. *Enterprise 사용 안내서*의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## 역할 및 권한 지정 {#roles-permissions}

시스템 관리자만 [!DNL Target]에서 사용자 역할을 설정할 수 있습니다. 예를 들어, Standard 승인자 사용자는 Experience Cloud 관리 권한도 가지고 있지 않으면 관찰자를 승인자로 변경할 수 없습니다.

시스템 관리자 사용자는 시스템에 사용자를 추가해야 합니다. 사용자는 자동으로 추가되지 않습니다. 사용자는 Experience Cloud에서 이메일로 초대를 받으며 계정 등록 전에 자신의 이메일 주소를 확인해야 합니다.

1. [Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)에서 **[!UICONTROL 제품]** 을 클릭한 다음, 원하는 제품의 이름을 선택합니다.

   ![제품 탭](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. 원하는 구성의 이름을 클릭합니다.
1. **[!UICONTROL 사용자를 클릭합니다]**.

   The [!UICONTROL Users] tab displays all of the users in that workspace.

   ![구성 사용자](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new.png)

1. [!UICONTROL 제품 역할] 열의 각 사용자에 대한 드롭다운 목록을 사용하여 원하는 권한 역할(관찰자, 편집자 또는 승인자)을 선택합니다.

   | 역할 | 설명 |
   |--- |--- |
   | 관찰자 | 활동을 볼 수 있지만 만들거나 편집할 수는 없습니다. |
   | 편집자 | 활동이 라이브 상태가 되기 전에 활동을 만들고 편집할 수 있지만 활동 시작을 승인할 수는 없습니다. |
   | 승인자 | 활동을 만들고, 편집하고 활성화하거나 중지할 수 있습니다. |

자세한 내용은 *Enterprise 사용 안내서*의 [Admin Console에서 제공 권한 및 역할 관리](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html)를 참조하십시오.

## 교육 비디오: Target 작업 영역을 구성하는 방법

학습 목표:

* Adobe Target 인터페이스에서 Adobe Admin Console에 액세스 (세 가지 방법)
* Adobe Admin Console에서 작업 영역 구성
   * 작업 공간에 사용자 추가
   * 작업 공간에 속성 추가
* 기본 작업 공간 이해

>[!VIDEO](https://video.tv.adobe.com/v/19463/?captions=kor)
