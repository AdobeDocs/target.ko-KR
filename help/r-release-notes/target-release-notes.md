---
description: 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
keywords: 릴리스 노트
seo-description: 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
seo-title: Adobe Target 릴리스 노트(사전 릴리스)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: d675c6875c8474ba490956ea395076eef5b9e58f

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

[!UICONTROL 기업 권한을] 통해 [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다. 엔터프라이즈 [!UICONTROL 권한] 기능을 사용하면 팀 전체의 최적화 프로그램을 효과적으로 확장할 수 있습니다. 이 기능은 UI에서 사용할 수 [!DNL Target] 있었지만 관리 API는 2019년 2월 릴리스까지 해당 지원이 [!DNL Target] 없었습니다. Adobe는 통합 계정을 사용하여 조직에서 만든 모든 작업 영역에 액세스할 수 있도록 관리 API를 업데이트했습니다. 이전 버전에서 관리 API는 기본 작업 영역으로 제한되었지만 2019년 2월 업데이트에서는 승인자 액세스 권한이 있는 모든 작업 영역에 대한 액세스 권한을 [!UICONTROL 부여했습니다] .

2019년 [!DNL Target] 9월 릴리스를 통해 [!UICONTROL 엔터프라이즈] 권한은 고객에게 다음과 같은 액세스 제어를 제공합니다.

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다
* Adobe I/O 통합에 역할을 적용할 수 있습니다.승인자 [!UICONTROL ,]편집자 [!UICONTROL 또는]관찰자 .

**필요한 작업**:모든 작업 영역에서 리소스(활동, 대상, 제안 및 보고)에 대한 CRUD 작업을 위해 현재 API를 활용하는 고객은 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. 9월 릴리스 이전에는 제품 역할 [!UICONTROL 드롭다운 목록에서 선택한 역할에] 관계없이 승인자 [!UICONTROL 액세스를 사용하여 모든 통합을] 실행했습니다. 이제 예정된 릴리스에서 원하는 역할을 선택할 수 있습니다.

이 작업은 2019년 8월에 **수행해야 합니다**. 2019 [!DNL Target] 년 9월 릴리스 이후 액세스 제어가 활성화되고 현재 설정된 경우 기본 작업 공간에 대한 액세스 권한을 확인합니다. 미리 통합 역할을 설정하는 데 문제가 없습니다.

단계별 지침과 자세한 내용은 작업 영역에 [대한 Adobe I/O 통합 액세스 권한 부여 및 역할](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)할당을 참조하십시오.

## Target Standard/Premium 19.9.2(2019년 9월 30일)

This maintenance release includes the following enhancement:

* VEC(Visual Experience Composer)의 RTE(Rich Text Editor)에 대한 보안 업데이트를 비롯한 몇 가지 보안 수정 사항이 있습니다. (TGT-35383)

## Target Standard/Premium 19.9.1(2019년 9월 10일)

| 기능 / 개선 사항 | 설명 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 엔터프라이즈 권한 | Target 2019년 9월 릴리스에서 엔터프라이즈 권한은 고객에게 다음과 같은 액세스 제어를 제공합니다.<UL><li>통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.</li><li>Adobe I/O 통합에 역할을 적용할 수 있습니다.승인자, 편집자 또는 관찰자를 참조하십시오.</li></ul>단계별 지침과 자세한 내용은 작업 영역에 [대한 Adobe I/O 통합 액세스 권한 부여 및 역할](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)할당을 참조하십시오. |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
