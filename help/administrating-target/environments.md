---
keywords: environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist;blacklist;blocklist;allowlist
description: 사이트 및 프리 프로덕션 환경을 구성하여 Adobe Target에서 손쉽게 관리하고 리포팅할 수 있습니다.
title: 환경
feature: hosts and environments
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 65%

---


# 환경

쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성하십시오.

관리하기 쉽도록 호스트는 환경으로 번들됩니다. 예를 들어 수십 개의 호스트를 두세 개의 환경으로 그룹화할 수 있습니다. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. 필요한 경우 새 환경을 추가하거나 환경의 이름을 바꿀 수 있습니다.

One environment, the default environment, is pre-named [!UICONTROL Production]. 이 기본 환경은 이름을 변경하는 경우에도 삭제할 수 없습니다. [!DNL Target]은 이 위치에서 승인된 최종 활동 및 테스트를 제공한다고 가정합니다.

When a [!DNL Target] request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. 활동을 활성화하기 전에 호스트 관리를 사용하면 테스트, 스테이징 및 개발 환경에서 새 활동과 컨텐츠의 품질을 쉽게 보장할 수도 있습니다.

환경을 관리하려면 **[!UICONTROL 관리]** > 환경을 **[!UICONTROL 클릭합니다]**.

![환경 목록](/help/administrating-target/assets/environments.png)

## 환경 추가 {#section_32097D0993724DF3A202D164D3F18674}

1. 환경 [!UICONTROL 목록] 에서 환경 **[!UICONTROL 추가를 클릭합니다]**.
1. 환경에 대해 수사적 이름을 지정합니다.
1. 환경에 대해 원하는 활성 모드를 [!UICONTROL 활성 활동]과 [!UICONTROL 활성 및 비활성 활동] 중에서 지정합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Set the default environment for reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

모든 활동 보고서의 기본값으로 사용할 환경을 선택할 수 있습니다.

If you use [!UICONTROL Production] as your default, all unknown hosts automatically are added here and report data from there is included in the default report view. 대신 &quot;깨끗한&quot; 환경을 작성하면 핵심 사이트/도메인만 포함됩니다.

보고할 기본 환경을 설정하려면 다음을 수행하십시오.

1. 환경 [!UICONTROL 목록에서 스타] 아이콘을 클릭합니다

>[!NOTE]
>
>[!DNL Recommendations] 사용자는 호스트가 호스트 그룹을 전환할 경우 자신들의 행동 데이터베이스와 제품 데이터베이스를 다시 구축해야 합니다.

## Change the name of an environment {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. 환경 [!UICONTROL 목록] 에서 **[!UICONTROL 편집]** 아이콘을 클릭합니다.
1. 환경 이름을 변경합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Delete an environment {#section_737F8869612047868D03FC755B1223D3}

더 이상 필요하지 않은 환경을 삭제할 수 있습니다.

1. 환경 [!UICONTROL 목록] 에서 **[!UICONTROL 삭제]** 아이콘을 클릭합니다.
1. **[!UICONTROL 삭제]**&#x200B;를 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>You cannot delete the [!UICONTROL Production] environment, but you can rename it.

## 권장 사항: 환경(호스트 그룹)별로 컬렉션 및 제외 필터링

![Premium 배지](/help/assets/premium.png)

선택한 환경(호스트 그룹)에 대한 권장 사항 컬렉션 및 제외 컨텐츠를 미리 볼 수 있습니다.

>[!NOTE]
>
>Recommendations activities are available as part of the [!DNL Target] Premium solution. 이 기능은 [!DNL Target] Premium 라이센스가 없는 [!DNL Target] Standard에서는 사용할 수 없습니다.

환경은 사용 용도에 따라 카탈로그의 사용 가능한 항목을 구분하는 데 사용할 수 있습니다. For example, you can use host groups for [!UICONTROL Development] and [!UICONTROL Production] environments, different brands, or different geographies. 기본적으로 카탈로그 검색, 컬렉션 및 제외의 미리 보기 결과는 기본 호스트 그룹을 기반으로 합니다. (환경 필터를 사용하여 다른 결과를 미리 볼 호스트 그룹을 선택할 수도 있습니다.) 기본적으로 항목을 만들거나 업데이트할 때 환경 ID를 지정하지 않는 한, 새로 추가된 항목은 모든 호스트 그룹에서 사용할 수 있습니다. 전달되는 권장 사항은 요청에 지정된 호스트 그룹에 따라 다릅니다.

제품이 보이지 않는다면 올바른 호스트 그룹을 사용하고 있는지 확인하십시오. 예를 들어, 스테이징 환경을 사용하도록 권장 사항을 설정하고 호스트 그룹을 스테이징으로 설정하는 경우, 제품을 표시할 스테이징 환경에서 컬렉션을 다시 만들어야 합니다. 각 환경에서 사용 가능한 제품을 확인하려면 각 환경에서 카탈로그 검색을 사용하십시오. 선택한 환경(호스트 그룹)에 대한 권장 사항 컬렉션 및 제외 컨텐츠를 미리 볼 수도 있습니다.

>[!NOTE]
>선택한 환경을 변경한 후 검색을 클릭하여 반환된 결과를 업데이트해야 합니다.

The [!UICONTROL Environment] filter is available from the following places in the Target UI:

* 카탈로그 검색([!UICONTROL 권장 사항 > 카탈로그 검색])
* 컬렉션 만들기 대화 상자([!UICONTROL 권장 사항 > 컬렉션 > 새로 만들기])
* 컬렉션 업데이트 대화 상자([!UICONTROL 권장 사항 > 컬렉션 > 편집])
* 제외 만들기 대화 상자([!UICONTROL 권장 사항 > 제외 > 새로 만들기])
* 제외 업데이트 대화 상자([!UICONTROL 권장 사항 > 제외 > 편집])