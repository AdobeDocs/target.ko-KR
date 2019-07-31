---
description: 원하는 역할을 가진 모든 작업 영역에 대한 Adobe I/O 통합 액세스 권한을 부여하는 정보입니다.
keywords: 통합; 역할; 사용자 권한; Admin Console
seo-description: Adobe Target에서 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여하는 정보
seo-title: Adobe I/O 통합 기능을 통해 작업 영역에 대한 액세스 권한 부여 및 Adobe Target에서 역할 할당
solution: Target
subtopic: 시작하기
title: Adobe I/O 통합 기능을 통해 작업 영역 이용 권한 부여 및 역할 할당
translation-type: tm+mt
source-git-commit: a6aae8602b8f3c3f879bd6e3e37591f330197cf8

---


# ![PREMIUM](/help/assets/premium.png) Adobe I/O 통합 기능을 통해 작업 영역 이용 및 역할 할당

[!UICONTROL 엔터프라이즈 권한을 통해] [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 여러 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다.

>[!NOTE]
>
>속성 및 권한 기능은 [Target Premium](/help/c-intro/intro.md#premium) 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.

[!UICONTROL 엔터프라이즈 권한] 기능을 사용하면 팀 간의 최적화 프로그램을 효율적으로 확장할 수 있습니다. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier in 2019. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!DNL Target] [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

이 업데이트는 다음 사용 사례를 지원합니다.

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Adobe I/O 통합 권한을 부여하면 Central 팀이 몇 가지 작업 공간에서만 API 중심의 변경을 수행할 수 있도록 적절한 역할의 작업 영역을 선택할 수 있습니다.
* 팀에서 API를 탐색할 준비가 될 때마다 팀이 자신의 작업 공간을 소유하도록 할 수 있고 그에 따라 역할을 선택할 수 있습니다.
* 위의 시나리오 중 하나를 혼합하여 사용할 수 있습니다.

**필요한 조치**: 현재 모든 작업 영역에서 리소스 (활동, 대상, 제안 및 보고) 에 대한 CRUD 작업을 위해 API를 활용하는 고객은 사용 사례에 따라 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of choice made from the [!UICONTROL Product Role] drop-down list. 이제 원하는 역할을 선택할 수 있습니다.

This action should be performed before **September 4, 2019** to not face any disruption on your end. If this action is not performed, after the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. 위의 가이드라인에 따라 통합을 설정한다는 역반응이 없습니다. 이렇게 변경할수록 더 나은 결과를 얻을 수 있습니다. 조직의 작업 영역 수에 따라 작업 시간을 단축할 수 있습니다. 이 프로세스는 몇 번의 클릭만으로 원하는 역할을 가진 작업 영역에 기존 통합을 추가할 수 있습니다.

**Adobe I/O 통합 기능을 사용하여 작업 영역에 액세스하고 역할을 할당하려면 다음을 수행하십시오.**

1. Open the **[!DNL[Adobe Admin Console](https://adminconsole.adobe.com)]**.

1. **[!UICONTROL 제품]** 탭을 클릭한 다음 원하는 제품의 이름을 선택합니다.

   ![Adobe Admin Console에서 제품 선택](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. 원하는 작업 영역 (제품 프로필) 를 선택합니다.

   ![제품 프로필 선택](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. **[!UICONTROL 통합]** 탭을 클릭합니다.

   ![통합 탭](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Conditional) To add a new integration, click **[!UICONTROL Add Integration]**, select the desired integration, then click **[!UICONTROL Save]**.

1. **[!UICONTROL 제품 역할]** 드롭다운 목록에서 해당 작업 영역에 대해 원하는 역할을 선택합니다.

   * [!UICONTROL 승인자]
   * [!UICONTROL 편집자]
   * [!UICONTROL 관찰자]
   ![제품 프로필 역할 선택](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
