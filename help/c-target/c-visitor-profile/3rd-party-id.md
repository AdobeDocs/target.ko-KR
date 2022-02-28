---
keywords: mbox;mbox 타사 Id;프로필 동기화;프로파일 동기화;PCID
description: 멤버십 ID 또는 조직의 충성도 프로그램과 같이 조직의 방문자 ID인 mbox3rdPartyID를 사용하는 방법을 알아봅니다.
title: mbox3rdPartyId에 대한 실시간 프로필 동기화를 사용하려면 어떻게 해야 합니까?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 8969b3b04b8f02a4ae9860bafe4b0a1c80a6f35e
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 20%

---

# mbox3rdPartyId에 대한 실시간 프로필 동기화

다음 `mbox3rdPartyId` in [!DNL Adobe Target] 는 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

[!DNL Target]이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 [!DNL Target] PCID가 지정됩니다. 방문자가 로그인하고 구현이 를 전달하는 경우 `mbox3rdPartyId` to [!DNL Target], [!DNL Target] 해당 방문자의 `mbox3rdPartyId` 사용 [!DNL Target] PCID입니다.

3~5분 간격으로 업데이트가 데이터베이스와 동기화됩니다. 방문자가 로그아웃하면 병합된 데이터가 `mbox3rdPartyId`를 눌러 해당 방문자의 작업에 대한 전체 레코드를 만듭니다. 동일한 속성이 두 ID에 있는 경우(예: PCID에는 category=hats가 지정되고 `mbox3rdPartyId` 에는 category=skis가 있고, 방문자가 로그인 전에 경험 A를 보았으나 경험 B는 `mbox3rdPartyId`- `mbox3rdPartyId` 는 PCID의 속성을 덮어씁니다. 방문자가 로그인하기 전에 한 활동 또는 경험에 있었으나 경험에 다른 활동 및 경험이 저장되는 경우입니다 `mbox3rdPartyId`로 로그인하면 해당 방문자가 `mbox3rdPartyId` 활동 및 경험.

| PCID(로그인되지 않음) | mbox3rdPartyID(로그인됨) | 병합되어 mbox3rdPartyID에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>인증된(로그인된) 사용자와 인증되지 않은 사용자를 구별하려면 [!DNL Adobe Experience Cloud Identity Service] (ECID) 대신 사용할 수 있습니다. 사용자가 mbox3rdPartyID와 연결되면 로그아웃한 후에도 사용자와 계속 연결됩니다.

>[!NOTE]
>
>[!DNL Adobe Analytics] 목표가 추적되지 않는 경우 [!DNL Adobe Experience Cloud] ID(ECID)가 변경되더라도(예: 방문자가 장치를 변경함) [!DNL Target] 프로필은 mbox3rdPartyID를 기반으로 병합될 수 있지만 여전히 활동 정보가 있습니다. 동일한 ECID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자), [!DNL Analytics for Target] (A4T)가 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

* 페이지에 여러 개의 mbox가 있고 일부만 사용되는 경우 `3rdPartyID`, [!DNL Target] 에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. 다음 `3rdPartyID` 컨텍스트보다 컨텍스트가 우선합니다. 하나의 mbox가 전달하기에 충분합니다 `3rdPartyId` PCID보다 우선하기 위한 컨텍스트

   예를 들어, 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 본다고 가정하십시오. 글로벌 mbox는 `3rdPartyID`. 로그인 후에 방문자는 세 개의 경험 중 하나를 하위 mbox로 보고, 일부는 를 사용합니다 `3rdPartyID`. 방문자는 사이트에서 다양한 페이지를 방문한 다음 뒤로 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서는 글로벌 mbox가 전달되지 않았습니다 `3rdPartyID`하지만 하나 이상의 하위 mbox가 수행했습니다. `3rdPartyID` PCID보다 우선합니다.

* 방문자의 고객 ID를에 보낼 수 있습니다 [!DNL Target] 두 가지 방법 사용

   1. 활동을 만들려면 `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` 는 `targetPageParams` 또는 `targetPageParamsAll`
      * `thirdPartyId` 는 배달 API 페이로드에서 직접 설정한 매개 변수 이름입니다.
      * 이 매개 변수에서는 값을 하나만 보낼 수 있습니다.
   1. 를 사용하십시오 `setCustomerId`/`customerIds` ECID 서비스의 함수입니다.

      * `setCustomerId` 는 페이지에서 VisitorAPI.js를 사용할 수 있을 때 클라이언트측(브라우저) 구현에서 사용할 수 있는 함수입니다.
      * `customerIds` 는 배달 API 페이로드에서 직접 설정할 때 사용되는 매개 변수 이름이며, 일반적으로 서버측 또는 IOT(사물인터넷) 구현에서 수행됩니다.
      * 다른 `mbox3rdPartyId`/`thirdPartyId`여러 ID를 이 접근 방식의 목록으로 보낼 수 있지만 [!DNL Target] 은 TnT ID당 단일 고객 ID만 지원하며 알려진 별칭(고객 속성 UI에 구성된 별칭)이 있는 목록의 첫 번째 ID를 사용합니다.

   다음을 사용할 수 있습니다 `mbox3rdPartyId`/`thirdPartyId` if [!DNL Target] 유일한 사용자 [!DNL Adobe Experience Cloud] 솔루션 을 사용할 수 없습니다. 기타 모든 경우에 `setCustomerId`/`customerIds` 추가 정보.

   >[!IMPORTANT]
   >
   > 한 방문자에 대해 위에서 언급한 두 접근 방식을 서로 교환하여 사용할 수 있게 되면 인증되지 않은 방문자와 인증된 방문자의 프로필 병합이 잘못될 수 있습니다 [!DNL Target] 프로필 .
   >
   >Adobe은 두 가지를 모두 사용하지 않는 것이 좋습니다 `mbox3rdPartyId`/`thirdPartyId` 및 `setCustomerID`/`customerIds` 함께
   >
   >두 접근 방식을 서로 교환하여 사용해야 하는 경우, `setCustomerID`/`customerIds` 에서 사용하는 것은 입니다. `thirdPartyId`/`mbox3rdPartyId` 반대로

