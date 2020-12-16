---
keywords: mbox;mbox3rdPartyId;profile syncing;profile synch;PCID
description: '실시간 프로필에 대한 정보 '
title: Adobe Target의 mbox3rdPartyId에 대한 실시간 프로필 동기화
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 81%

---


# mbox3rdPartyId에 대한 실시간 프로필 동기화{#real-time-profile-syncing-for-mbox-rdpartyid}

mbox3rdPartyID는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

[!DNL Target]이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 [!DNL Target] PCID가 지정됩니다. 방문자가 로그인하고 mbox3rdPartyID가 [!DNL Target]에 전달되도록 구현되면 [!DNL Target]은 해당 방문자의 mbox3rdPartyID를 [!DNL Target] PCID에 연결합니다.

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
>인증된(로그인) 사용자와 인증되지 않은 사용자를 구별하려면 mbox3rdPartyID 대신 Adobe Experience Cloud ID(ECID)를 사용하십시오. 사용자가 mbox3rdPartyID에 연결되면 로그아웃한 후에도 사용자와 연결된 상태로 유지됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] mbox3rdPartyId를 기반으로  [!DNL Adobe Experience Cloud] 프로필을 병합하고 여전히 활동 정보를 가지고 있더라도  [!DNL Target] ID(EDID)가 변경되는 경우(예: 방문자가 장치를 변경하는 경우) 목표는 추적되지 않습니다. 동일한 EDID(동일한 디바이스를 사용하여 페이지에 액세스하는 방문자)로 식별되는 방문자의 경우 [!DNL Analytics for Target](A4T)는 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

페이지에 여러 개의 mbox가 있고 일부만 3rdPartyID를 사용하는 경우, Target에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. 3rdPartyID 컨텍스트는 PCID 컨텍스트에 우선합니다. PCID보다 우선하기 위해 한 개의 mbox가 해당 컨텍스트에 3rdPartyId를 전달하는 것으로 충분합니다.

예를 들어, 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 본다고 가정하십시오. 전역 mbox는 3rdPartyID를 사용하지 않습니다. 로그인 후에 방문자는 세 개의 경험 중 하나를 하위 mbox로 보고, 일부는 3rdPartyID를 사용합니다. 방문자는 사이트에서 다양한 페이지를 방문한 다음 뒤로 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서 전역 mbox는 3rdPartyID를 전달하지 않았지만 하나 이상의 하위 mbox가 수행했습니다. 3rdPartyID가 PCID보다 우선했습니다.
