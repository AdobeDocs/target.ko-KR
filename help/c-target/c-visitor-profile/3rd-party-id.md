---
description: mbox3rdPartyID는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.
keywords: mbox;mbox3rdPartyID;프로필 동기화;프로필 동기화
seo-description: mbox3rdPartyID는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.
seo-title: mbox3rdPartyID에 대한 실시간 프로필 동기화
solution: Target
title: mbox3rdPartyID에 대한 실시간 프로필 동기화
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mbox3rdPartyID에 대한 실시간 프로필 동기화{#real-time-profile-syncing-for-mbox-rdpartyid}를 참조하십시오

mbox3rdPartyID는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

Target이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 Target PCID가 지정됩니다. 방문자가 로그인하고 mbox3rdPartyID가 Target에 전달되도록 구현되면 Target은 해당 방문자의 mbox3rdPartyID를 Target PCID에 연결합니다.

3~5분 간격으로 업데이트가 데이터베이스와 동기화됩니다. 방문자가 로그아웃하면 병합된 데이터가 mbox3rdPartyID에 연결된 이전 데이터를 대신하여 해당 방문자 작업에 대해 보다 완벽한 기록을 만듭니다. 동일한 속성이 두 ID에 대해 존재하면(예: PCID에는 category=hats가 지정되고 mbox3rdPartyID에는 category=skis가 지정되거나, 방문자가 로그인 전에 경험 A를 보았으나 mbox3rdPartyID에는 경험 B가 저장되는 경우) mbox3rdPartyID에 저장된 속성이 PCID의 속성을 덮어씁니다. 방문자가 로그인하기 전에 어떤 활동 또는 경험에 있었으나 mbox3rdPartyID에는 다른 활동 및 경험이 저장되는 경우 로그인한 후에 해당 방문자는 mbox3rdPartyID 활동 및 경험을 사용하게 됩니다.

| PCID(로그인되지 않음) | mbox3rdPartyID(로그인됨) | 병합되어 mbox3rdPartyID에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>[!DNL Target] 프로필이 mbox3rdPartyID를 기반으로 병합될 수 있고 여전히 활동 정보가 있더라도 MID([!DNL Adobe Experience Cloud] ID)가 변경되는 경우(예: 방문자가 장치 변경) [!DNL Adobe Analytics] 목표가 추적되지 않습니다. 동일한 MID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) A4T([!DNL Analytics for Target])가 예상대로 작동해야 합니다.
