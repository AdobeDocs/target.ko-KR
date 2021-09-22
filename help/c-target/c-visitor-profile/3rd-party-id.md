---
keywords: mbox;mbox 타사 Id;프로필 동기화;프로파일 동기화;PCID
description: 멤버십 ID 또는 조직의 충성도 프로그램과 같이 조직의 방문자 ID인 mbox3rdPartyID를 사용하는 방법을 알아봅니다.
title: mbox3rdPartyId에 대한 실시간 프로필 동기화를 사용하려면 어떻게 해야 합니까?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 20%

---

# mbox3rdPartyId에 대한 실시간 프로필 동기화

[!DNL Adobe Target]의 `mbox3rdPartyId`은 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

[!DNL Target]이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 [!DNL Target] PCID가 지정됩니다. 방문자가 로그인하고 `mbox3rdPartyId`이 [!DNL Target]에 전달되면 [!DNL Target]는 해당 방문자의 `mbox3rdPartyId`을 [!DNL Target] PCID와 연결합니다.

3~5분 간격으로 업데이트가 데이터베이스와 동기화됩니다. 방문자가 로그아웃하면 병합된 데이터가 `mbox3rdPartyId`에 연결된 이전 데이터를 대신하여 해당 방문자 작업에 대한 전체 레코드를 만듭니다. 동일한 속성이 두 ID에 대해 존재하면(예: PCID에는 category=hats가 지정되고 `mbox3rdPartyId`에는 category=skis가 지정되거나, 방문자가 로그인 전에 경험 A를 보았으나 `mbox3rdPartyId`에는 경험 B가 저장되는 경우) `mbox3rdPartyId`에 저장된 속성이 PCID의 속성을 덮어씁니다. 방문자가 로그인하기 전에 한 활동 또는 경험에 있었으나 `mbox3rdPartyId`에 다른 활동 및 경험이 저장되는 경우 로그인한 후에 해당 방문자는 `mbox3rdPartyId` 활동 및 경험에 배치됩니다.

| PCID(로그인되지 않음) | mbox3rdPartyID(로그인됨) | 병합되어 mbox3rdPartyID에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>인증된(로그인된) 사용자와 인증되지 않은 사용자를 구별하려면 mbox3rdPartyID 대신 [!DNL Adobe Experience Cloud Identity Service](ECID)를 사용하십시오. 사용자가 mbox3rdPartyID와 연결되면 로그아웃한 후에도 사용자와 계속 연결됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] 프로필이 mbox3rdPartyID를 기반으로 병합될 수 있고 여전히 활동 정보가 있더라도 EDID( [!DNL Adobe Experience Cloud] ID)가 변경되는 경우(예: 방문자가  [!DNL Target] 장치를 변경) 목표가 추적되지 않습니다. 동일한 EDID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) [!DNL Analytics for Target] (A4T)가 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

* 페이지에 여러 개의 mbox가 있고 일부만 `3rdPartyID`을 사용하는 경우, [!DNL Target]에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. `3rdPartyID` 컨텍스트는 PCID 컨텍스트에 우선합니다. PCID보다 우선하기 위해 한 개의 mbox가 해당 컨텍스트에 `3rdPartyId`을 전달하는 것으로 충분합니다.

   예를 들어, 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 본다고 가정하십시오. 글로벌 mbox는 `3rdPartyID`을 사용하지 않습니다. 로그인 후에 방문자는 세 개의 경험 중 하나를 하위 mbox로 보고, 일부는 `3rdPartyID`를 사용합니다. 방문자는 사이트에서 다양한 페이지를 방문한 다음 뒤로 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서 글로벌 mbox는 `3rdPartyID`를 전달하지 않았지만 하나 이상의 하위 mbox가 수행했습니다. `3rdPartyID` PCID보다 우선합니다.

* 다음 두 가지 방법을 사용하여 방문자의 고객 ID를 [!DNL Target]로 보낼 수 있습니다.

   1. 활동을 만들려면 `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` 는 또는 를 사용할 때 매개 변수  `targetPageParams` 이름입니다  `targetPageParamsAll`
      * `thirdPartyId` 는 배달 API 페이로드에서 직접 설정한 매개 변수 이름입니다.
      * 이 매개 변수에서는 값을 하나만 보낼 수 있습니다.
   1. ECID 서비스의 `setCustomerId`/`customerIds` 함수를 사용합니다.

      * `setCustomerId` 는 페이지에서 VisitorAPI.js를 사용할 수 있을 때 클라이언트측(브라우저) 구현에서 사용할 수 있는 함수입니다.
      * `customerIds` 는 배달 API 페이로드에서 직접 설정할 때 사용되는 매개 변수 이름이며, 일반적으로 서버측 또는 IOT(사물인터넷) 구현에서 수행됩니다.
      * `mbox3rdPartyId`/`thirdPartyId`과 달리 여러 ID를 이 접근 방식의 목록으로 보낼 수 있지만, [!DNL Target]는 TnT ID당 단일 고객 ID만 지원하므로 알려진 별칭(고객 속성 UI에 구성된 별칭)이 있는 목록의 첫 번째 ID를 사용합니다.

   >[!IMPORTANT]
   >
   > 한 방문자에 대해 위에서 언급한 두 접근 방식을 서로 교환하여 사용할 수 있게 되면 인증되지 않은 프로필과 인증되지 않은 [!DNL Target] 프로필이 잘못 병합될 수 있습니다.
   >
   >Adobe은 `mbox3rdPartyId`/`thirdPartyId` 와 `setCustomerID`/`customerIds`를 모두 함께 사용하지 않는 것이 좋습니다.
   >
   >두 접근 방식을 서로 교환하여 사용해야 하는 경우 `setCustomerID`/`customerIds`에서 사용하는 목록의 첫 번째 ID가 `thirdPartyId`/`mbox3rdPartyId`에서 사용하는 ID인지 또는 그 반대의 경우인지 확인하십시오.

