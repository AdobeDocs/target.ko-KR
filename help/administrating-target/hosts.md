---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Adobe Target에서 손쉽게 관리하고 분리된 보고를 위해 사이트와 프리 프로덕션 환경을 구성할 수 있습니다.
title: 호스트
feature: hosts and environments
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 26%

---


# 호스트{#hosts}

쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성하십시오.

호스트 관리의 기본 목적은 비활성화 상태 컨텐츠가 실수로 웹 사이트에 나타나지 않도록 하는 것입니다. 호스트 관리를 사용하면 보고서 데이터를 [environment](/help/administrating-target/environments.md)로 분리할 수도 있습니다.

호스트는 [!DNL Target] 요청이 수행된 모든 도메인입니다. 웹 사이트에서는 일반적으로 [!DNL Target] 요청을 만드는 URL의 `location.hostname` 속성입니다.

기본적으로 [!DNL Target]은(는) [!DNL Target] 요청을 수행하고 [!DNL Target] 응답을 받을 수 있는 호스트를 제한하지 않습니다. 새 주최자가 요청을 하면 자동으로 작동합니다. 모르거나 예상할 수 없는 다른 도메인에서 테스트할 수도 있습니다. 이 기본 비헤이비어를 무시하려면 [!DNL Target]에서 사용할 호스트를 제한하도록 허용 목록에 추가하다 또는 차단 목록에 추가하다를 설정할 수 있습니다.

호스트를 관리하려면 **[!UICONTROL 관리]** > **[!UICONTROL 호스트]**&#x200B;를 클릭합니다.

![](assets/hosts_list.png)

## 호스트 {#concept_0D4B43E23AA9408F8B28A57ED754BF65} 인식

호스트를 인식하고 [!UICONTROL 호스트] 목록에 추가하려면 다음 조건을 충족해야 합니다.

* 호스트에 적어도 하나의 [!DNL Target] 요청이 있어야 합니다.
* 호스트의 페이지에 다음 항목이 있어야 합니다.

   * at.js 또는 mbox.js 참조의 정확성
   * [!DNL Target] 요청 또는 자동 생성된 글로벌 [!DNL Target] 요청

* [!DNL Target] 요청이 있는 페이지는 브라우저에서 봐야 합니다.

페이지를 보면 호스트가 [!UICONTROL 호스트] 목록에 표시되므로 환경에서 관리하고 활동 및 테스트를 미리 보고 실행할 수 있습니다.

>[!NOTE]
>
>여기에는 개인 개발 서버가 모두 포함됩니다.

호스트가 [!UICONTROL 호스트] 목록에 추가되면 호스트가 인식되는지 확인하십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 호스트]**&#x200B;를 클릭합니다.
1. 해당 호스트가 나열되지 않으면 브라우저를 새로 고치십시오.

   기본적으로 새로 인식된 호스트는 [!UICONTROL 프로덕션] 환경에 배치됩니다. 이러한 호스트에서는 비활성 상태 활동을 보는 것이 허용되지 않으므로 이 환경은 가장 안전한 환경입니다.

1. (조건부) **[!UICONTROL 이동]** 아이콘( ![이동 아이콘](/help/administrating-target/assets/icon-move.png))을 클릭하여 호스트를 [!UICONTROL 개발], [!UICONTROL 스테이징] 또는 기타 환경으로 이동합니다.

>[!NOTE]
>
>이름을 바꾸더라도 [!UICONTROL 프로덕션] 환경을 삭제할 수 없습니다. 이 위치에서 활성 상태 최종 활동 및 테스트를 제공한다고 가정합니다. 기본 환경은 비활성 상태 캠페인을 보도록 허용하지 않습니다.

## 호스트 목록 {#section_068B23C9D8224EB78BC3B7C8580251B0} 정렬 또는 검색

[!UICONTROL 호스트] 목록을 정렬하려면 열 헤더([!UICONTROL 이름], [!UICONTROL 환경] 또는 [!UICONTROL 마지막으로 요청한 항목])를 클릭하여 오름차순 또는 내림차순으로 목록을 정렬합니다.

[!UICONTROL 호스트] 목록을 검색하려면 [!UICONTROL 호스트 검색] 상자에 검색어를 입력합니다.

## Target 요청을 Target으로 보낼 수 있는 호스트를 지정하는 허용 목록을 만듭니다.{#allowlist}

[!DNL Target] 요청을 [!DNL Target]에 보낼 수 있는 호스트(도메인)를 지정하는를 만들 허용 목록에 추가하다 수 있습니다. 요청을 생성하는 다른 모든 호스트는 주석 처리된 인증 오류 응답을 가져옵니다. 기본적으로 [!DNL Target] 요청을 포함하는 모든 호스트는 [!UICONTROL 프로덕션] 환경에서 [!DNL Target]에 등록되며 모든 활성 및 승인된 활동에 액세스할 수 있습니다. 이 방식을 원하지 않는 경우 대신를 사용하여 허용 목록에 추가하다 [!DNL Target] 요청을 수행할 수 있는 특정 호스트를 기록하고 [!DNL Target] 컨텐츠를 수신할 수 있습니다. 모든 호스트는 [!UICONTROL 호스트] 목록에 계속 표시되며, 환경에서는 이러한 호스트를 그룹화하고 각 호스트에 다른 수준을 할당하는 데 사용할 수 있습니다(예: 호스트가 활성 및/또는 비활성 활동을 볼 수 있는지 여부).

을 허용 목록에 추가하다 만들려면:

1. [!UICONTROL 호스트] 목록에서 **[!UICONTROL 호스트 승인]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 컨텐츠 전달에 대해 인증된 호스트 활성화]** 전환을 활성화합니다.
1. 원하는 대로 **[!UICONTROL 주최자 포함]** 상자에 원하는 호스트를 추가합니다.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. 원하는 대로 **[!UICONTROL 호스트에]** 상자가 포함되지 않은 호스트를 추가합니다.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

권한이 없는 호스트에서 [!DNL Target] 요청이 수행된 경우 호출은 `/* no display - unauthorized mbox host */`로 응답합니다.

>[!IMPORTANT]
>
>**보안 모범 사례**:의 ubox 기능을 사용하는  [!DNL Target]경우 이허용 목록에 추가하다는 리디렉터가 탐색하는 도메인 목록도  [](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) 제어합니다. 구현의 일부로 ubox를 사용할 때 리디렉션할 도메인을 추가하는지 확인하십시오. 허용 목록에 추가하다를 지정하지 않은 경우 [!DNL Adobe]은 리디렉션 URL을 확인할 수 없으며 잠재적인 악성 리디렉션에서 보호할 수 없습니다.
>
>허용 목록에 추가하다는 환경보다 우선합니다. 기능을 사용하기 전에 모든 호스트허용 목록에 추가하다를 지워야 합니다. 그러면에서 허용하는 호스트만 호스트 목록에 허용 목록에 추가하다 표시됩니다. 그런 후 호스트를 원하는 환경으로 이동할 수 있습니다.

다른 사이트의 도메인이 환경에 표시되는 경우가 있습니다. 도메인이 at.js 또는 mbox.js를 호출하면 목록에 도메인이 표시됩니다. 예를 들어 웹 페이지 중 하나를 서버로 복사하면 해당 도메인이 환경에 표시됩니다. 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수도 있습니다.

`mboxHost`가 API 호출에서 전달되는 경우 전달된 환경에 대해 전환이 기록됩니다. 전달된 환경이 없으면 호출의 호스트는 기본적으로 [!UICONTROL Production]입니다.

[!UICONTROL 호스트가 포함하지 않음] 상자에 원하는 호스트를 추가하여 [!DNL Target] 요청을 [!DNL Target]에 보낼 수 없는 호스트(도메인)를 지정하는를 만들 수도 있습니다차단 목록.

>[!NOTE]
>
>인증된 호스트 목록은 [!DNL Target] 호스트 및 기본 리디렉션 호스트 모두에 사용되므로 [!DNL Adobe Target] Javascript SDK(at.js) *AND* ubox 기본 리디렉션 URL에 사용된 모든 도메인을 사용하도록 승인된 기존 도메인을 모두 추가해야 합니다. 나중에에 유사한 새 도메인을 허용 목록에 추가하다 추가해야 합니다.

## 호스트 {#section_F56355BA4BC54B078A1A8179BC954632} 삭제

더 이상 필요하지 않은 호스트를 삭제할 수 있습니다.

1. [!UICONTROL 호스트] 목록에서 **[!UICONTROL 삭제]** 아이콘을 클릭합니다.
1. **[!UICONTROL 삭제]**&#x200B;를 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>호스트에서 [!DNL Target] 요청이 들어 있는 페이지로 이동하면 호스트가 다시 나열됩니다.

## 호스트 문제 해결 {#concept_B3D7583FA4BB480382CC7453529FE1B7}

호스트에 문제가 발생하는 경우 다음의 문제 해결 팁을 사용해 보십시오.

**호스트가 계정의 목록에 표시되지 않습니다.**

* 브라우저에서 [!UICONTROL 호스트] 페이지를 새로 고치십시오.
* at.js 또는 mbox.js 참조를 포함하여 [!DNL Target] 요청이 올바른지 확인합니다.
* 호스트의 [!DNL Target] 요청 중 하나를 찾아보십시오. 호스트의 [!DNL Target] 요청이 브라우저에서 렌더링되지 않았을 수 있습니다.

**[!UICONTROL 호스트] 목록에 임의 도메인이나 알 수 없는 도메인이 표시됩니다.**

도메인에서 [!DNL Target]에 대한 요청이 수행된 경우 도메인이 이 목록에 표시됩니다. 대체로 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수 있습니다. 나열된 도메인이 팀에서 사용하는 도메인이 아닌 경우 [!UICONTROL 삭제]를 클릭하여 제거할 수 있습니다.

**내  [!DNL Target] 요청이 /* no display - unauthorized mbox host */를 반환합니다.**

권한이 없는 호스트에서 [!DNL Target] 요청이 수행된 경우, 요청은 /* no display - unauthorized mbox host */로 응답합니다.
