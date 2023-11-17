---
keywords: 사용자 추가;사용자 관리;사용자 권한
description: 사용 방법 알아보기 [!DNL Adobe Admin Console] 에서 사용자 및 해당 권한 및 권한을 관리하려면 [!DNL Adobe Target Standard].
title: 다음에 대한 사용자 추가 및 권한 관리 방법 [!DNL Target Standard] 계정?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: d40c25f75103327e749ad864b17df926cb323be0
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 73%

---

# 사용자

에서 사용자 추가 및 권한 관리 [!DNL Adobe Admin Console] 용 [!DNL Target Standard] 계정입니다.

>[!NOTE]
>
>[!UICONTROL 속성] 및 [!UICONTROL 권한] 기능은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target] Premium 라이선스가 없는 [!DNL Target] Standard에서는 사용할 수 없습니다.
>
>조직에 다음이 있는지 여부를 알 수 있습니다. [!UICONTROL 표준] 또는 [!UICONTROL Premium] 라이센스 부여 [!UICONTROL 관리] 링크(맨 위) [!DNL Target] UI.
>
>* **[!DNL Target] Standard 고객**: [!UICONTROL 속성] 탭이 아닌 [!UICONTROL 사용자] 탭(**[!UICONTROL 관리 > 사용자]**)이 표시된다면 귀사는 [!DNL Target] Standard 라이선스를 보유하고 있습니다.  [!DNL Target] Standard 고객은 이 문서의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 할당해야 합니다.
>
>* **[!DNL Target]Premium 고객**: [!UICONTROL 사용자] 탭과 [!UICONTROL 속성] 탭([!UICONTROL 관리 > 속성])이 표시된다면 귀사는 [!DNL Target] Premium 라이선스를 보유하고 있습니다. [!DNL Target] Premium 고객은 [기업 사용자 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 및 [기업 권한 구성](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md)의 지침에 따라 [!DNL Adobe Admin Console]에서 사용자를 추가하고 권한을 할당해야 합니다.
>
>사용자 및 권한 관리 방법에 대한 자세한 내용은 *Enterprise 및 Teams 사용 안내서*&#x200B;의 [제품 및 프로필 관리](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)를 참조하십시오.

[!DNL Adobe Target]을 시작하면 [!DNL Adobe Experience Cloud] 계정에 미리 채워져 있는 ID(Adobe.com으로 끝남)를 발견하게 됩니다. 이들 ID는 [!DNL Adobe] 팀원을 위한 것으로, 이를 통해 도움이 필요한 경우 새 계정 및 [!DNL Adobe Target] 사용에 대한 지원을 받을 수 있습니다. 지원을 받으려면 일반적인 방법으로 Adobe 팀에 문의하십시오.

새 사용자는에 나열되지 않습니다. [!UICONTROL 사용자] 을 사용하여 로그인할 때까지 페이지 [!DNL Adobe Experience Cloud] 계정 그런 다음 로그인합니다. [!DNL Target].

기본적으로 모두 [!DNL Target] 다음으로 시작하는 사용자 [!UICONTROL 관찰자] 사용 권한.

관리자 사용자는 [!UICONTROL 사용자] 목록에 명시되어 있습니다. 액세스 수준을 변경해야 하는 경우 시스템 관리자 사용자 중 한 명에게 문의하십시오.

##  내에서 사용자 정보 보기[!DNL Target]

에서 현재 사용자 목록을 볼 수 있습니다. [!DNL Target] 작업 영역별 역할 및 이메일 주소를 포함한 UI.

을(를) 보려면 [!UICONTROL 사용자] 페이지, 클릭 **[!UICONTROL 관리]** > **[!UICONTROL 사용자]**.

![Target 내 사용자 목록](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>기존 사용자를 관리하거나 신규 사용자를 추가하려면 아래에 설명된 바와 같이 [!UICONTROL Adobe Admin Console]를 사용해야 합니다.

## 액세스 [!DNL Adobe Admin Console] {#access}

에서 수행된 작업의 경우 [!DNL Adobe Admin Console], 다음 단계에 따라 콘솔에 액세스합니다.

1. [!DNL Target] 내부에서 **[!UICONTROL 관리]** > **[!UICONTROL 사용자]** > **[!UICONTROL 사용자 관리]**&#x200B;를 클릭합니다.

   또는

   [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)로 이동한 다음 이미 로그인하지 않았다면 Adobe ID를 사용하여 로그인합니다.

1. (조건부) 하나 이상의 조직에 대한 [!DNL Admin Console for Enterprise] 액세스 권한을 보유하고 있는 경우 내비게이션 바의 오른쪽 또는 상단에 있는 사용자 아바타를 클릭한 다음 원하는 조직을 선택하십시오.

## 사용자 추가 {#add-users}

모든 사용자 관리는 [!DNL Adobe Admin Console for Enterprise]에서 수행해야 합니다. 그러나 [!DNL Target]의 모든 기존 사용자는 [!DNL Target]에서 [!DNL Admin Console for Enterprise]로 마이그레이션됩니다.

1. [Admin Console에서](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) **[!UICONTROL 사용자]** > **[!UICONTROL 사용자]**&#x200B;를 클릭하여 신규 사용자를 만들거나 기존 사용자를 편집합니다.
1. *Enterprise 사용 안내서*&#x200B;의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## 사용자 그룹 만들기 {#user-groups}

개발자, 분석가, 마케터, 경영진 등과 같은 사용자 그룹을 만든 다음 여러 사용자에게 권한을 할당할 수 있습니다 [!DNL Adobe] 제품 및 작업 공간 다른 팀 구성원 간에 적절한 모든 권한 할당 [!DNL Adobe] 제품은 특정 사용자 그룹에 추가하는 것만큼 간단할 수 있습니다.

1. [Admin Console에서](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) **[!UICONTROL 사용자]** > **[!UICONTROL 사용자 그룹]**&#x200B;을 클릭하여 신규 사용자 그룹을 만들거나 기존 사용자 그룹을 편집합니다.
1. *Enterprise 사용 안내서*&#x200B;의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## 역할 및 권한 지정 {#roles-permissions}

시스템 관리자만 [!DNL Target]에서 사용자 역할을 설정할 수 있습니다. 예: [!UICONTROL 표준] 승인자 사용자는 관찰자를 승인자로 변경할 수 없습니다. [!DNL Experience Cloud] 관리자 권한.

시스템 관리자 사용자는 시스템에 사용자를 추가해야 합니다. 사용자는 자동으로 추가되지 않습니다. [!DNL Experience Cloud]에서 이메일을 통해 초대되며 계정 등록 전 이메일 주소를 확인해야 합니다.

1. [Admin Console에서](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) **[!UICONTROL 제품]**&#x200B;을 클릭한 다음 원하는 제품의 이름을 선택합니다.

   ![제품 탭](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. 원하는 작업 영역(예: 기본 작업 영역)을 클릭합니다.

   ![기본 작업 영역](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   [!UICONTROL 사용자] 탭에는 해당 작업 공간의 모든 사용자가 표시됩니다.

   ![구성 사용자](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. 원하는 권한 역할 선택([!UICONTROL 승인자], [!UICONTROL 편집자], [!UICONTROL 관찰자] 또는 [!UICONTROL 게시자])의 각 사용자에 대한 드롭다운 목록을 사용하여 다음을 수행합니다. [!UICONTROL 제품 역할] 열.

   ![제품 역할 드롭다운 목록](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | 역할 | 설명 |
   |--- |--- |
   | [!UICONTROL 승인자] | 활동을 만들고, 편집하고 활성화하거나 중지할 수 있습니다. |
   | [!UICONTROL 편집자] | 활동이 라이브 상태가 되기 전에 활동을 만들고 편집할 수 있지만 활동 시작을 승인할 수는 없습니다. |
   | [!UICONTROL 관찰자] | 활동을 볼 수 있지만 만들거나 편집할 수는 없습니다. |
   | [!UICONTROL 게시자] | 와 유사 [!UICONTROL 관찰자] 역할(활동을 볼 수 있지만 만들거나 편집할 수는 없음) 그러나 [!UICONTROL 게시자] 역할에는 활동을 활성화할 수 있는 추가 권한이 있습니다. |

자세한 내용은 *Enterprise 사용 안내서*&#x200B;의 [Admin Console에서 제품 권한 및 역할 관리](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html)를 참조하십시오.

## 교육 비디오: Adobe Target 작업 영역을 구성하는 방법 ![튜토리얼 배지](/help/main/assets/tutorial.png)

학습 목표:

* Adobe Target 인터페이스에서 Adobe Admin Console에 액세스(3가지 방법)
* Adobe Admin Console에서 작업 공간 구성
   * 작업 공간에 사용자 추가
   * 작업 공간에 속성 추가
* 기본 작업 공간 이해

>[!NOTE]
>
>[!DNL Target] [!UICONTROL 관리] 메뉴 UI(이전명: [!UICONTROL 설정])는 향상된 성능을 제공하고, 새로운 기능을 출시할 때 필요한 유지 관리 시간을 줄이고, 제품 전반에 걸쳐 사용자 경험을 개선할 수 있도록 새롭게 디자인되었습니다. 다음 비디오에서 설명하는 정보는 일반적으로 정확하지만 옵션이 약간 다른 위치에 있을 수 있습니다. 업데이트된 비디오는 곧 게시될 예정입니다.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
