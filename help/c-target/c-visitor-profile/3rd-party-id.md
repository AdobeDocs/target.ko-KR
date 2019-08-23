---
description: mbox 3 rdpartyid는 회사의 충성도 프로그램에 대한 회원 ID와 같은 회사의 방문자 ID 입니다.
keywords: mbox; mbox 3 rdpartyid; 프로필 동기화; 프로필 동기화; PCID
seo-description: '실시간 프로필에 대한 정보 '
seo-title: Adobe Target에서 mbox 3 rdpartyid에 대한 실시간 프로필 동기화
solution: Target
title: mbox 3 rdpartyid에 대한 실시간 프로필 동기화
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: f54dba622e449fb8dac44cb37ff711419f8eda4b

---


# Real-time profile syncing for mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

mbox 3 rdpartyid는 회사의 충성도 프로그램에 대한 회원 ID와 같은 회사의 방문자 ID 입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyId to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyId with the [!DNL Target] PCID.

3~5분 간격으로 업데이트가 데이터베이스와 동기화됩니다. 방문자가 로그아웃하면 병합된 데이터가 mbox 3 rdpartyid와 연관된 이전 데이터를 대체하여 해당 방문자의 작업에 대한 보다 전체적인 기록을 만듭니다. 두 ID 모두에 동일한 속성이 있는 경우—예를 들어 PCID 에는 category = hat 이 있고 mbox 3 rdpartyid 에는 category = skis가 있거나 방문자가 경험 A를 본 적이 있는 경우 경험 B가 mbox 3 rdpartyid에 저장됩니다. —mbox 3 rdpartyid에 저장된 속성은 PCID에서 속성을 덮어씁니다. 방문자가 로그인하기 전에 하나의 활동 또는 경험에 있었던 경우, 해당 방문자에 로그인한 후에 mbox 3 rdpartyid 활동 및 경험에 다른 활동과 경험이 저장됩니다.

| PCID(로그인되지 않음) | mbox 3 rdpartyid (로그인됨) | 병합되어 mbox 3 rdpartyid에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] 프로필이 mbox 3 rdpartyid를 기반으로 [!DNL Adobe Experience Cloud] 병합될 수 [!DNL Target] 있고 여전히 활동 정보가 있는 경우에도 방문자가 장치 변경을 변경하는 경우 (예: 방문자가 장치 변경) 목표가 추적되지 않습니다. 동일한 MID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) A4T([!DNL Analytics for Target])가 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

페이지에 몇 개의 mbox가 있고 일부 mbox만 사용하는 경우, Target 에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. 3 Rdpartyid 컨텍스트는 PCID 컨텍스트에 우선합니다. 한 mbox가 해당 컨텍스트에 대해 3 rdpartyid를 전달하기에 충분하며 PCID 보다 우선 순위가 높습니다.

예를 들어 방문자가 로그인하기 전에 페이지에 액세스하고 경험을 보는 경우 글로벌 mbox는 3 rdpartyid를 사용하지 않습니다. 로그인 후에 방문자는 세 개의 경험 중 하나를 하위 mbox로 보고, 일부는 3 rdpartyid를 사용합니다. 방문자는 사이트에서 다양한 페이지를 방문한 다음 [뒤로] 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 표시합니다. 이 시나리오에서 글로벌 mbox는 3 rdpartyid를 전달하지 않았지만 하나 이상의 하위 mbox가 수행되었습니다. 3 Rdpartyid가 PCID 보다 우선시되었습니다.
