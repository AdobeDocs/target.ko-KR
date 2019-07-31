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
source-git-commit: 48cb808283c9b2858e1bd041feb3fe8228253d6a

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

Enterprise Permissions allows [!DNL Target] customers to use a single organization, but divide it into workspaces for their different teams or workflows. 따라서 팀 간의 최적화 프로그램을 효과적으로 확장할 수 있습니다. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier this year. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, Target Enterprise Permissions will provide customers with the following access controls:

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

이 업데이트는 다음 사용 사례를 지원합니다.

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Adobe I/O 통합 권한을 부여하면 Central 팀이 몇 가지 작업 공간에서만 API 중심의 변경을 수행할 수 있도록 적절한 역할의 작업 영역을 선택할 수 있습니다.
* 작업 영역을 소유한 각 팀은 팀에서 API를 탐색할 준비가 될 때마다 자체 통합을 가지고 그에 따라 역할을 선택할 수 있습니다.
* 위의 시나리오 중 하나를 혼합하여 사용할 수 있습니다.

**필요한 조치**: 현재 모든 작업 영역에서 리소스 (활동, 대상, 제안 및 보고) 에 대한 CRUD 작업을 위해 API를 활용하는 고객은 사용 사례에 따라 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, irrespective of choice made in the [!UICONTROL Product Role] drop-down list. 이제 원하는 역할을 선택할 수 있습니다.

This action *must* be performed before September 4, 2019 to not face any disruption on your end. 이 작업이 수행되지 않으면 [! DNL Target 9 월 릴리스, 액세스 제어가 활성화되고 현재 설정된 방식으로 기본 작업 영역에 대한 액세스를 관찰할 수 있습니다. 위의 가이드라인에 따라 통합을 설정한다는 역반응이 없습니다. 이렇게 변경할수록 더 나은 결과를 얻을 수 있습니다. 조직의 작업 영역 수에 따라 작업 시간을 단축할 수 있습니다. 이 프로세스는 몇 번의 클릭만으로 원하는 역할을 가진 작업 영역에 기존 통합을 추가할 수 있습니다.

## Target Standard/Premium 19.8.1(2019년 8월 20일) {#tgt-19-8-1}

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* Visual Experience Composer (VEC) 의 RTE (Rich Text Editor) 에 대한 보안 업데이트를 포함한 여러 보안 수정 사항이 있습니다. (TGT-35383)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
