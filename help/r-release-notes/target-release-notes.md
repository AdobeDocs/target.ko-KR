---
description: 최신 또는 예정된 [! DNL Adobe Target] 릴리스.
keywords: 릴리스 노트
seo-description: 최신 또는 예정된 [! DNL Adobe Target] 릴리스.
seo-title: Adobe Target 릴리스 노트 (베타 버전)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: e1174aacc5610878c8671e88fbd20d51fedffe6c

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트 날짜: 2019년 7월 31일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## 공지

**2019 년 7 월 31 일**

[!UICONTROL 엔터프라이즈 권한을 통해] [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 여러 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다. [!UICONTROL 엔터프라이즈 권한] 기능을 사용하면 팀 간의 최적화 프로그램을 효율적으로 확장할 수 있습니다. Although this feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until the [!DNL Target] February 2019 release. Adobe는 통합 계정을 사용하여 조직에서 만든 모든 작업 영역에 액세스할 수 있도록 관리 API를 업데이트했습니다. So, while earlier, Admin APIs were restricted to the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**조치 필요**: 현재 모든 작업 영역에서 리소스 (활동, 대상, 제안 및 보고) 에 대한 CRUD 작업을 위해 API를 활용하는 고객은 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. 향후 릴리스에서는 원하는 역할을 선택할 수 있습니다.

This action should be performed during the month of **August 2019**. After the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. 통합 역할을 미리 설정하는 데에는 불리한 결과가 없습니다.

For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.8.1(2019년 8월 20일) {#tgt-19-8-1}

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* Visual Experience Composer (VEC) 의 RTE (Rich Text Editor) 에 대한 보안 업데이트를 포함한 여러 보안 수정 사항이 있습니다. (TGT-35383)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
