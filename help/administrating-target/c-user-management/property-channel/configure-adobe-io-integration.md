---
description: 원하는 역할을 가진 모든 작업 영역에 대한 Adobe I/O 통합 액세스 권한을 부여하는 정보입니다.
keywords: 통합; 역할; 사용자 권한; Admin Console
seo-description: Adobe Target에서 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여하는 정보
seo-title: Adobe I/O 통합 기능을 통해 작업 영역에 대한 액세스 권한 부여 및 Adobe Target에서 역할 할당
solution: Target
subtopic: 시작하기
title: Adobe I/O 통합 기능을 통해 작업 영역 이용 권한 부여 및 역할 할당
translation-type: tm+mt
source-git-commit: 13ad42da73dd3fcbf4e07be1de646e0eac8c991e

---


# ![PREMIUM](/help/assets/premium.png) Adobe I/O 통합 기능을 통해 작업 영역 이용 및 역할 할당

[!UICONTROL 엔터프라이즈 권한을 통해] [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 여러 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다.

>[!NOTE]
>
>속성 및 권한 기능은 [Target Premium](/help/c-intro/intro.md#premium) 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.

[!UICONTROL 엔터프라이즈 권한] 기능을 사용하면 팀 간의 최적화 프로그램을 효율적으로 확장할 수 있습니다. 이 기능은 [!DNL Target] UI에서 사용할 수 있었지만, 관리 API는 2019 년 이전 까지는 해당 지원을 받지 못했습니다. 2019 [!DNL Target] 년 2 월 릴리스에서 Adobe는 통합 계정을 사용하여 조직에서 만든 모든 작업 영역에 액세스할 수 있도록 관리 API를 업데이트했습니다. 따라서 이전에는 관리 API가 기본 작업 영역으로 제한되어 있었지만 2019 년 2 월 업데이트에는 [!UICONTROL 승인자] 액세스 권한이 있는 모든 작업 영역에 대한 액세스가 허용되었습니다.

2019 년 9 월 [!DNL Target] 릴리스에서 [!DNL Target][!UICONTROL 엔터프라이즈 권한은] 고객에게 다음과 같은 액세스 제어를 제공합니다.

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* Adobe I/O 통합에 역할을 적용할 수 있습니다. [!UICONTROL 승인자], [!UICONTROL 편집자][!UICONTROL 또는 관찰자.]

이 업데이트는 다음 사용 사례를 지원합니다.

* 리소스를 만들거나 편집할 수 있는 권한 없이 보고 목적으로 [!UICONTROL 관찰자] 역할로 모든 작업 영역에 대한 Adobe I/O 통합 액세스 권한을 부여합니다.
* Adobe I/O 통합 권한을 부여하면 Central 팀이 몇 가지 작업 공간에서만 API 중심의 변경을 수행할 수 있도록 적절한 역할의 작업 영역을 선택할 수 있습니다.
* 팀에서 API를 탐색할 준비가 될 때마다 팀이 자신의 작업 공간을 소유하도록 할 수 있고 그에 따라 역할을 선택할 수 있습니다.
* 위의 시나리오 중 하나를 혼합하여 사용할 수 있습니다.

**필요한 조치**: 현재 모든 작업 영역에서 리소스 (활동, 대상, 제안 및 보고) 에 대한 CRUD 작업을 위해 API를 활용하는 고객은 사용 사례에 따라 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. 이렇게 하려면에서 각 [!DNL Target][!UICONTROL 제품 프로필을] [!DNL Adobe Admin Console] 선택하고 [!UICONTROL 통합] 탭에 통합을 추가하면 됩니다. 9 월 릴리스 이전에는 [!UICONTROL 제품 역할 드롭다운 목록에서 선택한 선택 사항과 상관없이, 승인자] 액세스를 사용하여 [!UICONTROL 모든 통합이] 작동되었습니다. 이제 원하는 역할을 선택할 수 있습니다.

>[!NOTE]
>
>이 작업이 수행되지 않으면 2019 [!DNL Target] 년 9 월 릴리스 이후 액세스 제어가 활성화되고 현재 설정된 방식으로 기본 작업 영역에 대한 액세스를 관찰할 수 있습니다. 통합을 미리 설정하는 데 역반응이 없습니다. 이렇게 변경할수록 더 나은 결과를 얻을 수 있습니다. 조직의 작업 영역 수에 따라 이 프로세스는 몇 번의 클릭만으로 원하는 역할을 가진 작업 영역에 기존 통합을 추가할 수 있습니다.

**Adobe I/O 통합 기능을 사용하여 작업 영역에 액세스하고 역할을 할당하려면 다음을 수행하십시오.**

1. Adobe Admin **[Console](https://adminconsole.adobe.com)**&#x200B;를 엽니다.

1. **[!UICONTROL 제품]** 탭을 클릭한 다음 원하는 제품의 이름을 선택합니다.

   ![Adobe Admin Console에서 제품 선택](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. 원하는 작업 영역 (제품 프로필) 를 선택합니다.

   ![제품 프로필 선택](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. **[!UICONTROL 통합]** 탭을 클릭합니다.

   ![통합 탭](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (조건부) 새 통합을 추가하려면 통합 ****&#x200B;추가를 클릭하고 원하는 통합을 선택한 다음 **[!UICONTROL 저장을 클릭합니다]**.

1. **[!UICONTROL 제품 역할]** 드롭다운 목록에서 해당 작업 영역에 대해 원하는 역할을 선택합니다.

   * [!UICONTROL 승인자]
   * [!UICONTROL 편집자]
   * [!UICONTROL 관찰자]
   ![제품 프로필 역할 선택](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
