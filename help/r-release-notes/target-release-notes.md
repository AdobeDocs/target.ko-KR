---
description: 최신 또는 예정된 Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
seo-description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
seo-title: Adobe Target 릴리스 노트(사전 릴리스)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d91c46c78c0bcb58607def4cacaff0b761162fa

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**최근 업데이트: 2019년 9월 24일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## 공지

**2019년 7월 31일**

[!UICONTROL Enterprise Permissions allows  customers to use a single organization, but divide it into workspaces for different teams or workflows. ][!DNL Target] The Enterprise Permissions feature facilitates effective scaling of optimization programs across teams.  Although this feature was available in the  UI, the Admin APIs lacked the corresponding support until the  February 2019 release. [!DNL Target][!DNL Target] Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to the default workspace, the February 2019 update granted access to all workspaces with Approver access.

With the upcoming  September 2019 release, Enterprise Permissions will provide customers with the following access controls:[!DNL Target]

* You can choose the workspaces to which the integration can be applied
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**Action Required: Customers who are currently leveraging APIs for CRUD operations on resources (activities, audiences, offers, and reporting) across all workspaces need to grant their existing Adobe I/O integration access to all workspaces with the desired role.** Prior to the September release, all integrations operated using Approver access, regardless of the role selected from the Product Role drop-down list.  이제 예정된 릴리스에서 원하는 역할을 선택할 수 있습니다.

This action should be performed during the month of **August 2019**. After the  September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. [!DNL Target] 미리 통합 역할을 설정하는 데 문제가 없습니다.

For step-by-step instructions and more information, see Grant Adobe I/O integrations access to workspaces and assign roles.[](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)

## Target Standard/Premium 19.9.2(2019년 9월 30일)

이 유지 관리 릴리스에는 다음과 같은 향상된 기능이 포함되어 있습니다.

* VEC(Visual Experience Composer)의 RTE(Rich Text Editor)에 대한 보안 업데이트를 비롯한 몇 가지 보안 수정 사항이 있습니다. (TGT-35383)

## Target Standard/Premium 19.9.1(2019년 9월 10일)

| 기능/향상 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 엔터프라이즈 권한 | Target 2019년 9월 릴리스에서 엔터프라이즈 권한은 고객에게 다음과 같은 액세스 제어를 제공합니다.<UL><li>통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.</li><li>Adobe I/O 통합에 역할을 적용할 수 있습니다.승인자, 편집자 또는 관찰자를 참조하십시오.</li></ul>단계별 지침과 자세한 내용은 작업 영역에 [대한 Adobe I/O 통합 액세스 권한 부여 및 역할](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)할당을 참조하십시오. |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
