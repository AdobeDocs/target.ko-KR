---
description: mbox3rdPartyId는 회사의 로열티 프로그램에 대한 멤버십 ID와 같은 회사의 방문자 ID입니다.
keywords: mbox;mbox3rdPartyId;프로필 동기화;프로필 동기화;PCID
seo-description: '실시간 프로필에 대한 정보 '
seo-title: Adobe Target에서 mbox3rdPartyId에 대한 실시간 프로필 동기화
solution: Target
title: mbox3rdPartyId에 대한 실시간 프로필 동기화
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: f54dba622e449fb8dac44cb37ff711419f8eda4b

---


# Real-time profile syncing for mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

mbox3rdPartyId는 회사의 로열티 프로그램에 대한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyId to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyId with the [!DNL Target] PCID.

3~5분 간격으로 업데이트가 데이터베이스와 동기화됩니다. 방문자가 로그아웃하면 병합된 데이터가 mbox3rdPartyId와 연결된 이전 데이터를 대체하여 해당 방문자의 작업에 대한 보다 완전한 레코드를 만듭니다. 두 ID 모두에 동일한 속성이 있는 경우(예: PCID에는 category=hats가 있고 mbox3rdPartyId에는 category=skis가 있거나 방문자가 로그인 전에 경험 A를 보았지만 경험 B는 mbox3rdPartyId에 저장되어 있는 경우) PCID의 속성을 덮어씁니다. 방문자가 로그인하기 전에 한 활동 또는 경험에 있었지만 다른 활동 및 경험이 mbox3rdPartyId에 저장되어 있는 경우, 로그인한 후에는 해당 방문자가 mbox3rdPartyId 활동 및 경험에 배치됩니다.

| PCID(로그인되지 않음) | mbox3rdPartyId(로그인됨) | 병합되어 mbox3rdPartyId에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] mbox3rdPartyId를 기반으로 프로필을 병합할 수 있고 여전히 활동 정보를 가지고 있더라도 ID [!DNL Adobe Experience Cloud] (MID)가 변경되는 경우(예: 방문자가 장치를 변경하는 경우) [!DNL Target] 목표가 추적되지 않습니다. 동일한 MID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) A4T([!DNL Analytics for Target])가 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

페이지에 여러 개의 mbox가 있고 일부 mbox만 3rdPartyID를 사용하는 경우 Target에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. 타사 ID 컨텍스트가 PCID 컨텍스트에 우선합니다. 컨텍스트가 PCID보다 우선하도록 하려면 하나의 mbox가 3rdPartyId를 전달하기에 충분합니다.

예를 들어 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 보게 된다고 가정합니다. 전역 mbox는 3rdPartyID를 사용하지 않습니다. 로그인하면 방문자에게 세 개의 자식 mbox 중 하나가 표시됩니다. 이 중 일부는 3rdPartyID를 사용합니다. 방문자는 사이트에서 다양한 페이지를 방문한 다음 [뒤로] 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서는 글로벌 mbox가 3rdPartyID를 전달하지 않았지만 하나 이상의 하위 mbox가 전달되었습니다. 타사 ID가 PCID보다 우선합니다.
