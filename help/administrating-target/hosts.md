---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: 쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성하십시오.
title: 호스트
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: cf69c1d8472088d5f6a6b7250bedd1048cac5c10
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 57%

---


# 호스트{#hosts}

쉽게 관리하고 개별적으로 보고하려면 사이트와 사전 프로덕션 환경을 구성하십시오.

호스트 관리의 기본 목적은 비활성화 상태 컨텐츠가 실수로 웹 사이트에 나타나지 않도록 하는 것입니다. Host management also lets you separate report data by [environment](/help/administrating-target/environments.md).

호스트는 프로젝트의 모든 단계에서 컨텐츠를 제공하는 웹 서버(또는 웹 도메인)입니다. mbox를 제공하는 모든 호스트가 인식됩니다.

관리하기 쉽도록 호스트는 환경으로 번들됩니다. 예를 들어 수십 개의 호스트를 두세 개의 환경으로 그룹화할 수 있습니다. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. 필요한 경우 새 환경을 추가하거나 환경의 이름을 바꿀 수 있습니다.

One environment, the default environment, is pre-named [!UICONTROL Production]. 이 기본 환경은 이름을 변경하는 경우에도 삭제할 수 없습니다. [!DNL Target]은 이 위치에서 승인된 최종 활동 및 테스트를 제공한다고 가정합니다.

When an mbox request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. 활동을 활성화하기 전에 호스트 관리를 사용하면 테스트, 스테이징 및 개발 환경에서 새 활동과 컨텐츠의 품질을 쉽게 보장할 수도 있습니다.

[!DNL Target] 은 mbox를 보내고 받을 수 있는 호스트를 제한하지 않으므로 새 서버나 도메인이 들어오면 자동으로 작동합니다(허용 목록 또는 차단 목록을 설정하지 않은 경우). 또한 모르거나 예상할 수 없는 여러 도메인에서 광고 테스트가 활성화됩니다.

호스트를 관리하려면 **[!UICONTROL 관리]** > **[!UICONTROL 호스트를 클릭합니다]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

호스트를 인식하고 [!UICONTROL 호스트] 목록에 추가하려면 다음 조건을 충족해야 합니다.

* 호스트에 적어도 하나의 mbox가 있어야 합니다.
* 호스트의 페이지에 다음 항목이 있어야 합니다.

   * 정확한 at.js 또는 mbox.js 참조
   * mbox 또는 자동 생성된 글로벌 mbox 호출

* mbox가 있는 페이지는 브라우저에서 봐야 합니다.

페이지를 보면 호스트가 [!UICONTROL 호스트] 목록에 나열되어 있으므로 환경에서 관리하고 할 수 있으며, 활동 및 테스트를 미리 보거나 시작할 수도 있습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>여기에는 개인 개발 서버가 모두 포함됩니다.

호스트가 [!UICONTROL 호스트] 목록에 추가되면 호스트가 인식되는지 확인하십시오.

1. 관리 **** > **[!UICONTROL 호스트를 클릭합니다]**.
1. 해당 호스트가 나열되지 않으면 브라우저를 새로 고치십시오.

   By default, a newly recognized host is placed in the [!UICONTROL Production] environment. 이러한 호스트에서는 비활성 상태 활동을 보는 것이 허용되지 않으므로 이 환경은 가장 안전한 환경입니다.

1. (조건부) 이동 아이콘( ![이동 아이콘](/help/administrating-target/assets/icon-move.png) )을 클릭하여 호스트를 [!UICONTROL 개발], 스테이징 [!UICONTROL 또는]기타 환경으로이동합니다.

>[!NOTE]
>
>The [!UICONTROL Production] environment cannot be deleted, even if you rename it. 이 위치에서 활성 상태 최종 활동 및 테스트를 제공한다고 가정합니다. 기본 환경은 비활성 상태 캠페인을 보도록 허용하지 않습니다.

## Sort or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To sort the [!UICONTROL Hosts] list, click any column header ([!UICONTROL Name], [!UICONTROL Environment], or [!UICONTROL Last Requested]) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the [!UICONTROL Search Hosts] box.

## Create allowlists that specify hosts that are authorized to send mbox calls to Target. {#whitelist}

You can create an allowlist that specifies hosts (domains) that are authorized to send mbox calls to [!DNL Target]. 호출을 생성하는 다른 모든 호스트는 주석 처리된 인증 오류 응답을 받게 됩니다. 기본적으로 mbox 호출이 포함된 모든 호스트는 프로덕션 환경에서 [!DNL Target]에 등록되며 모든 활성 상태의 승인된 활동에 액세스할 수 있습니다. If this is not the desired approach, you can instead use the allowlist to record specific hosts that are eligible to make mbox calls and receive [!DNL Target] content. 모든 호스트는 [!UICONTROL 호스트] 목록에 계속 표시되며 환경은 이러한 호스트를 그룹화하고 각각에 다른 수준(예: 호스트가 활성 상태 캠페인을 볼 수 있는지 및/또는 비활성 상태 캠페인을 볼 수 있는지)을 지정하는 데 사용될 수 있습니다.

허용 목록을 만들려면:

1. 호스트 [!UICONTROL 목록에서 호스트] 권한 **[!UICONTROL 을 클릭합니다]**.
1. 컨텐츠 **[!UICONTROL 전달에 대해 인증된 호스트 활성화 전환을]** 활성화합니다.
1. Add the desired hosts in the **[!UICONTROL Host contains]** box, as desired.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. Add the desired hosts in the **[!UICONTROL Host does not contains]** box, as desired.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

허가되지 않은 호스트에서 mbox 호출이 수행되면 해당 호출은 `/* no display - unauthorized mbox host */`로 응답합니다.

>[!IMPORTANT]
>
>**보안 모범 사례**: 의 ubox 기능을 사용하는 [!DNL Target]경우 이 허용 목록은 리디렉터가 탐색할 수 있는 도메인 목록도 [제어합니다](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) . 구현의 일부로 ubox를 사용할 때 리디렉션할 도메인을 추가하는지 확인하십시오. allowlist를 지정하지 않은 경우 Adobe는 리디렉션 URL을 확인하고 잠재적인 악성 리디렉션에서 보호할 수 없습니다.
>
>allowlist가 환경보다 우선합니다. allowlist 기능을 사용하기 전에 모든 호스트를 지워야 합니다. 그러면 허용 목록에서 허용되는 호스트만 호스트 목록에 표시됩니다. 그런 후 호스트를 원하는 환경으로 이동할 수 있습니다.

다른 사이트의 도메인이 환경에 표시되는 경우가 있습니다. 도메인이 at.js 또는 mbox.js를 호출하는 경우 목록에 나타납니다. 예를 들어 웹 페이지 중 하나를 서버로 복사하면 해당 도메인이 환경에 표시됩니다. 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수도 있습니다.

`mboxHost`가 API 호출에서 전달되는 경우 전달된 환경에 대해 전환이 기록됩니다. If no environment is passed, the host in the call defaults to [!UICONTROL Production].

[!DNL Target]호스트에 다음이 제외됨[!UICONTROL  상자에서 원하는 호스트를 추가하여 mbox 호출을 ]에 전송할 수 없는 호스트(도메인)를 지정하는 블랙리스트를 만들 수도 있습니다.

>[!NOTE]
>
>승인된 호스트 목록은 mbox 호스트 및 기본 리디렉션 호스트 모두에 사용되므로 Adobe Target Javascript SDK(at.js) *AND* ubox 기본 리디렉션 url에 사용된 모든 도메인을 사용하도록 승인된 기존 도메인을 모두 추가해야 합니다. 향후 허용 목록에 유사한 새 도메인을 추가해야 합니다.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

더 이상 필요하지 않은 호스트를 삭제할 수 있습니다.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Delete]** icon.
1. **[!UICONTROL 삭제]**&#x200B;를 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>호스트에서 mbox가 있는 페이지로 이동하면 호스트가 다시 나열됩니다.

## 호스트 문제 해결 {#concept_B3D7583FA4BB480382CC7453529FE1B7}

[!DNL Adobe Target]에서 호스트를 관리하고 호스트 문제를 해결하기 위한 우수 사례

호스트에 문제가 발생하는 경우 다음의 문제 해결 팁을 사용해 보십시오.

**호스트가 계정의 mbox 목록에 표시되지 않습니다.**

* 브라우저에서 [!UICONTROL 호스트] 페이지를 새로 고치십시오.
* at.js 또는 mbox.js 참조를 포함하여 mbox 코드가 올바른지 확인합니다.
* 호스트의 mbox 중 하나를 탐색하십시오. 호스트의 mbox가 브라우저에서 하나도 렌더링된 적이 없을 수 있습니다.

**[!UICONTROL 호스트]목록에 임의 도메인이나 알 수 없는 도메인이 표시됩니다.**

도메인에서 [!DNL Target]이 호출된 경우 해당 도메인이 이 목록에 표시됩니다. 대체로 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수 있습니다. 나열된 도메인이 팀에서 사용하는 도메인이 아닌 경우 [!UICONTROL 삭제]를 클릭하여 제거할 수 있습니다.

**내 mbox 호출이 /* no display - unauthorized mbox host */를 반환합니다.**

허가되지 않은 호스트에서 mbox 호출이 수행되면 해당 호출은 /* no display - unauthorized mbox host */로 응답합니다.
