---
description: 원하는 역할을 가진 모든 작업 영역에 Adobe I/O 통합 액세스 권한을 부여하는 방법에 대한 정보입니다.
keywords: 통합;역할;사용자 권한;관리 콘솔
seo-description: Adobe Target에서 원하는 역할을 가진 모든 작업 영역에 기존 Adobe I/O 통합 액세스 권한을 부여하는 방법에 대한 정보
seo-title: 작업 영역에 Adobe I/O 통합 액세스 권한을 부여하고 Adobe Target에서 역할 할당
solution: Target
subtopic: 시작하기
title: 작업 영역에 Adobe I/O 통합 액세스 권한 부여 및 역할 할당
translation-type: tm+mt
source-git-commit: 13ad42da73dd3fcbf4e07be1de646e0eac8c991e

---


# ![프리미엄](/help/assets/premium.png) 작업 영역에 Adobe I/O 통합 액세스 권한을 부여하고 역할 할당

[!UICONTROL 기업 권한을] 통해 [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다.

>[!NOTE]
>
>속성 및 권한 기능은 [Target Premium](/help/c-intro/intro.md#premium) 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.

엔터프라이즈 [!UICONTROL 권한] 기능을 사용하면 팀 전체의 최적화 프로그램을 효과적으로 확장할 수 있습니다. 이 기능은 UI에서 사용할 수 [!DNL Target] 있었지만 관리 API는 2019년 이전까지는 해당 지원이 없었습니다. 2019 [!DNL Target] 년 2월 릴리스에서는 통합 계정을 사용하여 조직에서 만든 모든 작업 영역에 액세스할 수 있도록 관리 API가 업데이트되었습니다. 이전에는 관리 API가 기본 작업 영역으로 제한되었지만 2019년 2월 업데이트에서는 승인자 액세스 권한이 있는 모든 작업 영역에 대한 액세스 권한을 [!UICONTROL 부여했습니다] .

2019년 [!DNL Target] 9월 릴리스에서 [!DNL Target] 엔터프라이즈 [!UICONTROL 권한은 고객에게 다음 액세스 제어를 제공합니다] .

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다
* Adobe I/O 통합에 역할을 적용할 수 있습니다.승인자 [!UICONTROL ,]편집자 [!UICONTROL 또는]관찰자 .

이 업데이트는 다음과 같은 사용 사례를 지원합니다.

* Adobe I/O 통합 액세스 권한을 모든 작업 영역에 [!UICONTROL Observer] 역할을 부여하여 리소스를 만들거나 편집할 권한이 없는 보고 목적으로 사용할 수 있습니다.
* Adobe I/O 통합을 통해 적합한 역할이 있는 일부 작업 영역을 선택하여 중앙 팀이 몇 개의 작업 영역에서만 API 중심의 변경 작업을 수행할 수 있도록 합니다.
* 팀이 API를 탐색하고 그에 따라 역할을 선택할 준비가 되면 작업 영역을 소유한 각 팀이 고유한 통합을 가질 수 있습니다.
* 위의 시나리오 중 하나를 혼합 및 일치시킬 수 있습니다.

**필요한 작업**:모든 작업 영역에서 리소스(활동, 대상, 제안 및 보고)에 대한 CRUD 작업을 위해 현재 API를 이용하고 있는 고객은 사용 사례에 따라 원하는 역할을 가진 모든 작업 영역에 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. 이렇게 하려면 에서 각 제품 프로필을 [!DNL Target] 선택하고 [!UICONTROL 통합] 탭에서 통합을 [!DNL Adobe Admin Console] 추가하면 [!UICONTROL 됩니다] . 9월 릴리스 이전에는 제품 역할 [!UICONTROL 드롭다운 목록에서 선택한] 옵션에 관계없이 승인자 [!UICONTROL 액세스를 사용하여 모든] 통합을실행했습니다. 이제 원하는 역할을 선택할 수 있습니다.

>[!NOTE]
>
>이 작업이 수행되지 않는 경우 2019년 [!DNL Target] 9월 릴리스 이후 액세스 제어가 활성화되며 현재 설정된 경우 기본 작업 공간에 대한 액세스 권한만 확인할 수 있습니다. 미리 통합을 설정하는 데 부정적인 반응이 없습니다. 빨리 바꾸면 더 좋다. 조직의 작업 영역 수에 따라 이 프로세스는 몇 번의 클릭만으로 원하는 역할이 있는 작업 영역에 기존 통합을 추가할 수 있습니다.

**Adobe I/O 통합 액세스 권한을 작업 영역에 부여하고 역할을 할당하려면 다음을 수행하십시오.**

1. Adobe Admin **[Console을 엽니다](https://adminconsole.adobe.com)**.

1. 제품 **[!UICONTROL 탭을]** 클릭한 다음 원하는 제품의 이름을 선택합니다.

   ![Adobe Admin Console에서 제품 선택](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. 원하는 작업 영역(제품 프로필)을 선택합니다.

   ![제품 프로필 선택](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![통합 탭](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (조건부) 새 통합을 추가하려면 통합 **[!UICONTROL 추가를]**&#x200B;클릭하고 원하는 통합을 선택한 다음 저장을 **[!UICONTROL 클릭합니다]**.

1. 제품 **[!UICONTROL 역할]** 드롭다운 목록에서 해당 작업 공간에 대해 원하는 역할을 선택합니다.

   * [!UICONTROL 승인자]
   * [!UICONTROL 편집자]
   * [!UICONTROL 관찰자]
   ![제품 프로필 역할 선택](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
