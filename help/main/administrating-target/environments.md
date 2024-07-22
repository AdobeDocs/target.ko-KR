---
keywords: 환경;문제 해결;ubox;리디렉션;리디렉션;허용 목록;차단 목록;리디렉션;차단 목록 허용 목록에 추가하다
description: Adobe [!DNL Target] 에서 환경을 사용하여 간편하게 관리하고 개별적으로 보고하기 위해 사이트와 사전 프로덕션 환경을 구성하는 방법에 대해 알아봅니다.
title: 환경은 무엇이며 어떻게 사용할 수 있습니까?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 516d3969c8a6ed073b9f8d53c842e4d759cee8a2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 49%

---

# 환경

쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성하십시오.

관리하기 쉽도록 호스트는 환경으로 번들됩니다. 예를 들어 수십 개의 호스트를 두세 개의 환경으로 그룹화할 수 있습니다. 사전 설정 환경에는 [!UICONTROL Production], [!UICONTROL Staging] 및 [!UICONTROL Development]이(가) 포함됩니다. 필요한 경우 새 환경을 추가하거나 환경의 이름을 바꿀 수 있습니다.

기본 환경인 하나의 환경은 [!UICONTROL Production](으)로 이름이 지정됩니다. 이 기본 환경은 이름을 변경하는 경우에도 삭제할 수 없습니다. [!DNL Target]은 이 위치에서 승인된 최종 활동 및 테스트를 제공한다고 가정합니다.

새 웹 사이트 또는 도메인에서 [!DNL Target] 요청을 받으면 이러한 새 도메인이 항상 [!UICONTROL Production] 환경에 표시됩니다. [!UICONTROL Production] 환경에서는 설정을 변경할 수 없으므로 알 수 없거나 새 사이트에는 활성 상태이고 준비된 콘텐츠만 표시됩니다. 활동을 활성화하기 전에 호스트 관리를 사용하면 테스트, 스테이징 및 개발 환경에서 새 활동과 컨텐츠의 품질을 쉽게 보장할 수도 있습니다.

환경을 관리하려면 **[!UICONTROL Administration]** > **[!UICONTROL Environments]**&#x200B;을(를) 클릭합니다.

![환경 목록](/help/main/administrating-target/assets/environments.png)

## 환경 추가 {#section_32097D0993724DF3A202D164D3F18674}

1. [!UICONTROL Environments] 목록에서 **[!UICONTROL Add Environment]**&#x200B;을(를) 클릭합니다.
1. 환경에 대해 수사적 이름을 지정합니다.
1. 환경에 대해 원하는 활성 모드를 지정하십시오. [!UICONTROL Active Activities] 또는 [!UICONTROL Active and Inactive Activities].

   [!UICONTROL Active and Inactive Activities]을(를) 지정하면 이 환경의 호스트도 비활성 활동을 표시합니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 보고를 위한 기본 환경 설정 {#section_4F8539B07C0C45E886E8525C344D5FB0}

모든 활동 보고서의 기본값으로 사용할 환경을 선택할 수 있습니다.

[!UICONTROL Production]을(를) 기본값으로 사용하는 경우 알 수 없는 모든 호스트가 여기에 자동으로 추가되고 여기에서 나온 보고서 데이터가 기본 보고서 보기에 포함됩니다. 대신 &quot;깨끗한&quot; 환경을 작성하면 핵심 사이트/도메인만 포함됩니다.

보고할 기본 환경을 설정하려면 다음을 수행하십시오.

1. [!UICONTROL Environments] 목록에서 별 아이콘을 클릭합니다.

>[!NOTE]
>
>[!DNL Recommendations] 사용자는 호스트가 호스트 그룹을 전환할 경우 자신들의 행동 데이터베이스와 제품 데이터베이스를 다시 구축해야 합니다.
>
> [!DNL Adobe Experience Platform] 데이터 스트림](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=en#target){target=_blank}에서 [기본 환경을 지정하는 경우 이 설정은 [!DNL Target]의 설정을 무시합니다.

## 환경 이름 변경 {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. [!UICONTROL Environment] 목록에서 **[!UICONTROL Edit]** 아이콘을 클릭합니다.
1. 환경 이름을 변경합니다.
1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 환경 삭제 {#section_737F8869612047868D03FC755B1223D3}

더 이상 필요하지 않은 환경을 삭제할 수 있습니다.

1. [!UICONTROL Environment] 목록에서 **[!UICONTROL Delete]** 아이콘을 클릭합니다.
1. **[!UICONTROL Delete]**&#x200B;을(를) 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>[!UICONTROL Production] 환경은 삭제할 수 없지만 이름을 바꿀 수는 있습니다.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."}

선택한 환경(호스트 그룹)에 대한 권장 사항 컬렉션 및 제외 컨텐츠를 미리 볼 수 있습니다.

{{premium-note}}

환경을 사용하여 카탈로그에 있는 사용 가능한 항목을 다양한 용도로 구분할 수 있습니다. 예를 들어 [!UICONTROL Development] 및 [!UICONTROL Production] 환경, 다른 브랜드 또는 다른 지역에 대해 호스트 그룹을 사용할 수 있습니다. 기본적으로 카탈로그 검색, 컬렉션 및 제외의 미리 보기 결과는 기본 호스트 그룹을 기반으로 합니다. (환경 필터를 사용하여 다른 결과를 미리 볼 호스트 그룹을 선택할 수도 있습니다.) 기본적으로 항목을 만들거나 업데이트할 때 환경 ID를 지정하지 않는 한 새로 추가된 항목은 모든 호스트 그룹에서 사용할 수 있습니다.

>[!NOTE]
>
>전달되는 권장 사항은 요청에 지정된 호스트 그룹 또는 환경 ID에 따라 다릅니다.


제품이 보이지 않는다면 올바른 호스트 그룹을 사용하고 있는지 확인하십시오. 예를 들어, 스테이징 환경을 사용하도록 권장 사항을 설정하고 호스트 그룹을 스테이징으로 설정하는 경우, 제품을 표시할 스테이징 환경에서 컬렉션을 다시 만들어야 합니다. 각 환경에서 사용 가능한 제품을 확인하려면 각 환경에서 카탈로그 검색을 사용하십시오. 선택한 환경(호스트 그룹)에 대한 권장 사항 컬렉션 및 제외 컨텐츠를 미리 볼 수도 있습니다.

>[!NOTE]
>선택한 환경을 변경한 후 검색을 클릭하여 반환된 결과를 업데이트해야 합니다.

[!UICONTROL Environment] 필터는 Target UI의 다음 위치에서 사용할 수 있습니다.

* 카탈로그 검색([!UICONTROL Recommendations > Catalog Search])
* 컬렉션 만들기 대화 상자([!UICONTROL Recommendations > Collections > Create New])
* 컬렉션 업데이트 대화 상자([!UICONTROL Recommendations > Collections > Edit])
* 제외 만들기 대화 상자([!UICONTROL Recommendations > Exclusions > Create New])
* 제외 업데이트 대화 상자([!UICONTROL Recommendations > Exclusions > Edit])
