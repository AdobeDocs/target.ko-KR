---
keywords: mbox;mbox 타사 Id;프로필 동기화;프로파일 동기화;PCID
description: 조직의 멤버십 ID 또는 충성도 프로그램과 같은 조직의 방문자 ID인 mbox3rdPartyID를 사용하는 방법에 대해 알아봅니다.
title: mbox3rdPartyId에 대한 실시간 프로필 동기화를 사용하는 방법은 무엇입니까?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 18%

---

# mbox3rdPartyId에 대한 실시간 프로필 동기화

다음 `mbox3rdPartyId` 위치: [!DNL Adobe Target] 는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

[!DNL Target]이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 [!DNL Target] PCID가 지정됩니다. 방문자가 로그인하고 구현이 다음을 전달하는 경우 `mbox3rdPartyId` 끝 [!DNL Target], [!DNL Target] 해당 방문자의 `mbox3rdPartyId` (으)로 [!DNL Target] PCID.

업데이트는 5~10분마다 프로필 스토어와 동기화됩니다. 방문자의 세션이 종료되면 병합된 데이터가 와 연결된 이전 데이터를 대체합니다. `mbox3rdPartyId`, 해당 방문자 작업에 대한 전체 레코드 만들기. 동일한 속성이 두 ID에 있는 경우(예: PCID에는 category=hats 및 `mbox3rdPartyId` 에는 category=skis가 있거나, 방문자가 로그인 전에 경험 A를 보았으나 경험 B는에 저장되는 경우 `mbox3rdPartyId`- 다음에 저장된 속성 `mbox3rdPartyId` pcid의 속성을 덮어씁니다. 방문자가 로그인하기 전에 한 활동 또는 경험에 있었으나 다른 활동 및 경험은에 저장됩니다. `mbox3rdPartyId`에 로그인하면 해당 방문자가 `mbox3rdPartyId` 활동 및 경험.

| PCID(로그인되지 않음) | mbox3rdPartyID(로그인됨) | 병합되어 mbox3rdPartyID에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>인증된(로그인한) 사용자와 인증되지 않은 사용자를 구분하려면 [!DNL Adobe Experience Cloud Identity Service] mbox3rdPartyID 대신 (ECID). 사용자가 mbox3rdPartyID에 연결되면, 로그아웃 후에도 사용자와 연결된 상태로 유지됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] 다음과 같은 경우에는 목표가 추적되지 않습니다. [!DNL Adobe Experience Cloud] 다음과 같은 경우에도 ID(ECID)가 변경됩니다(예: 방문자가 장치 변경). [!DNL Target] 프로필이 mbox3rdPartyID를 기반으로 병합될 수 있으며 여전히 활동 정보가 있습니다. 동일한 ECID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) [!DNL Analytics for Target] (A4T)는 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

* 페이지에 여러 개의 mbox가 있고 일부만 사용하는 경우 `3rdPartyID`, [!DNL Target] 에는 각 방문자 요청에 대한 별도의 방문자 프로필/컨텍스트가 없습니다. 다음 `3rdPartyID` 컨텍스트는 PCID 컨텍스트보다 우선합니다. 1개의 mbox가 통과하기에 충분합니다 `3rdPartyId` PCID보다 우선시되는 컨텍스트에 대해.

   예를 들어 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 본다고 가정해 보겠습니다. 글로벌 mbox는 를 사용하지 않습니다. `3rdPartyID`. 로그인 후 방문자는 세 경험 중 하나를 하위 mbox로 보고, 일부는 을 사용합니다 `3rdPartyID`. 방문자는 사이트에서 다양한 페이지를 방문한 다음 뒤로 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서는 글로벌 mbox가 전달되지 않았습니다 `3rdPartyID`그러나 하나 이상의 하위 mbox가 수행했습니다. `3rdPartyID` PCID보다 우선했습니다.

* 방문자의 고객 ID를에 보낼 수 있습니다. [!DNL Target] 두 가지 접근 방식 사용:

   1. 활동을 만들려면 `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` 는 를 사용할 때의 매개 변수 이름입니다. `targetPageParams` 또는 `targetPageParamsAll`
      * `thirdPartyId` 는 게재 API 페이로드에서 직접 설정하는 매개 변수 이름입니다.
      * 이 매개 변수에는 값을 하나만 보낼 수 있습니다.
   1. 사용 `setCustomerId`/`customerIds` ECID 서비스 기능.

      * `setCustomerId` 는 페이지에서 VisitorAPI.js를 사용할 수 있을 때 클라이언트측(브라우저) 구현에 사용할 수 있는 함수입니다.
      * `customerIds` 는 게재 API 페이로드에서 직접 설정할 때 사용되는 매개 변수 이름으로, 일반적으로 서버측 또는 IOT(사물인터넷) 구현에서 수행됩니다.
      * 좋아하지 않음 `mbox3rdPartyId`/`thirdPartyId`, 이 접근 방법에서는 여러 ID를 목록으로 보낼 수 있지만 [!DNL Target] 는 TnT ID당 하나의 고객 ID만 지원하며 알려진 별칭(고객 속성 UI에 구성된 별칭)이 있는 목록의 첫 번째 ID를 사용합니다.

   다음을 사용할 수 있습니다. `mbox3rdPartyId`/`thirdPartyId` if [!DNL Target] 유일한 항목임 [!DNL Adobe Experience Cloud] 와 같은 질문에 답변할 수 있습니다. 다른 모든 경우에는 다음을 사용하는 것이 좋습니다. `setCustomerId`/`customerIds` 고객 ID를 보냅니다.

   >[!IMPORTANT]
   >
   > 단일 방문자에 대해 위에 언급된 두 접근 방식을 혼용하여 사용하면 인증되지 않은 프로필과 인증된 프로필이 잘못 병합될 수 있습니다 [!DNL Target] 프로필.
   >
   >Adobe은 두 가지를 모두 사용하지 않는 것이 좋습니다. `mbox3rdPartyId`/`thirdPartyId` 및 `setCustomerID`/`customerIds` 함께.
   >
   >두 접근 방식을 혼용하여 사용해야 하는 경우 목록에서 첫 번째 ID가에 사용되는지 확인하십시오. `setCustomerID`/`customerIds` 은(는) 다음의 경우 사용됩니다. `thirdPartyId`/`mbox3rdPartyId` 그리고 그 반대도 마찬가지입니다.

