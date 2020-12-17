---
keywords: integration;roles;user permissions;admin console
description: Adobe Target에서 원하는 역할을 가진 모든 작업 공간에 기존 Adobe I/O 통합 액세스 권한을 부여하는 것과 관련된 정보입니다.
title: Adobe Target에서 작업 공간에 Adobe I/O 통합 액세스 권한을 부여하고 역할 할당
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 88%

---


# ![PREMIUM](/help/assets/premium.png) 작업 공간에 Adobe I/O 통합 액세스 권한을 부여하고 역할 할당

[!UICONTROL 엔터프라이즈 권한]을 통해 [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 여러 팀 또는 워크플로우를 위한 작업 공간으로 나눌 수 있습니다.

>[!NOTE]
>
>속성 및 권한 기능은 [Target Premium](/help/c-intro/intro.md#premium) 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.

[!UICONTROL 엔터프라이즈 권한] 기능을 사용하면 팀 간의 최적화 프로그램을 효율적으로 확장할 수 있습니다. 이 기능은 [!DNL Target] UI에서 사용할 수 있었지만, 관리 API는 2019년 초까지 해당 지원을 받지 못했습니다. [!DNL Target] 2019년 2월 릴리스에서 Adobe는 통합 계정을 사용하여 조직에서 생성한 모든 작업 영역에 액세스할 수 있도록 관리 API를 업데이트했습니다. 따라서 이전에는 관리 API가 기본 작업 영역으로 제한되어 있었지만 2019년 2월 업데이트를 통해 [!UICONTROL 승인자] 액세스 권한이 있는 모든 작업 영역에 대한 액세스가 허용되었습니다.

[!DNL Target] 2019년 9월 릴리스에서 [!DNL Target] [!UICONTROL 기업 권한]은 다음과 같은 액세스 제어를 고객에게 제공합니다.

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* Adobe I/O 통합에 [!UICONTROL 승인자], [!UICONTROL 편집자] 또는 [!UICONTROL 관찰자] 역할을 적용할 수 있습니다.

이 업데이트는 다음과 같은 사용 사례를 지원합니다.

* 리소스를 만들거나 편집할 수 있는 권한이 없으며 보고 목적으로 [!UICONTROL 관찰자] 역할을 가진 모든 작업 영역에 대해 Adobe I/O 통합 액세스 권한을 부여합니다.
* Adobe I/O 통합에 적절한 역할이 있는 작업 영역을 선택할 수 있는 액세스 권한을 부여하면 중앙 팀이 소수의 작업 영역에서만 API 기반 변경을 수행할 수 있습니다.
* 팀이 API를 탐색하고 그에 따라 역할을 선택할 준비가 될 때마다 작업 영역을 보유한 각 팀이 자체 통합을 할 수 있도록 허용합니다.
* 위의 시나리오 중 몇 가지를 혼합하여 사용할 수 있습니다.

**필요한 조치**: 현재 모든 작업 영역의 리소스(활동, 대상, 제안 및 보고)에서 CRUD 운영을 위해 API를 활용하는 고객은 사용 사례에 따라 원하는 역할을 가진 모든 작업 영역에 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. 이렇게 하려면 [!DNL Adobe Admin Console]에서 각 [!DNL Target] [!UICONTROL 제품 프로필]을 선택하고 [!UICONTROL 통합] 탭에 통합을 추가하면 됩니다. 9월 릴리스 이전에는 [!UICONTROL 제품 역할] 드롭다운 목록에서 선택한 사항과 관계없이, [!UICONTROL 승인자] 액세스 권한을 사용하여 모든 통합이 작동했습니다. 이제 원하는 역할을 선택할 수 있습니다.

>[!NOTE]
>
>이 작업이 수행되지 않으면 [!DNL Target] 2019년 9월 릴리스 이후 액세스 제어가 활성화되고 현재 설정된 방식으로 기본 작업 영역에 대한 액세스를 관찰할 수 있습니다. 통합을 미리 설정해도 부작용이 없습니다. 더 빨리 변경할수록 더 나은 결과를 얻을 수 있습니다. 조직에서 작업 영역 수에 따라 이 프로세스를 몇 번의 클릭만으로 원하는 역할이 있는 작업 영역에 기존 통합을 추가할 수 있습니다.

**작업 공간에 Adobe I/O 통합 액세스 권한을 부여하고 역할을 할당하는 방법:**

1. **[Adobe Admin Console](https://adminconsole.adobe.com)**&#x200B;을(를) 엽니다.

1. **[!UICONTROL 제품]** 탭을 클릭한 다음 원하는 제품의 이름을 선택합니다.

   ![Adobe Admin Console에서 제품 선택](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. 원하는 작업 영역(제품 프로필)을 선택합니다.

   ![제품 프로필 선택](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. **[!UICONTROL 확장]** 탭을 클릭합니다.

   ![통합 탭](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (조건부) 새 통합을 추가하려면 **[!UICONTROL 통합 추가]**&#x200B;를 클릭하고 원하는 통합을 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 제품 역할]** 드롭다운 목록에서 해당 작업 영역에 대해 원하는 역할을 선택합니다.

   | 역할 | 설명 |
   |--- |--- |
   | 승인자 | 활동을 만들고, 편집하고 활성화하거나 중지할 수 있습니다. |
   | 편집자 | 활동이 라이브 상태가 되기 전에 활동을 만들고 편집할 수 있지만 활동 시작을 승인할 수는 없습니다. |
   | 관찰자 | 활동을 볼 수 있지만 만들거나 편집할 수는 없습니다. |
   | 게시자 | 관찰자 역할과 유사합니다(활동을 볼 수는 있지만 만들거나 편집할 수는 없습니다). 그러나 게시자 역할에는 활동을 활성화할 수 있는 추가 권한이 있습니다. |
