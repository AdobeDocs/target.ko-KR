---
keywords: mbox;mbox 타사 Id;프로필 동기화;프로파일 동기화;PCID
description: 조직의 멤버십 ID 또는 충성도 프로그램과 같은 조직의 방문자 ID인 mbox3rdPartyID를 사용하는 방법에 대해 알아봅니다.
title: mbox3rdPartyId에 대한 실시간 프로필 동기화를 사용하는 방법은 무엇입니까?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 18%

---

# mbox3rdPartyId에 대한 실시간 프로필 동기화

[!DNL Adobe Target]의 `mbox3rdPartyId`은(는) 회사의 충성도 프로그램을 위한 멤버십 ID와 같은 회사의 방문자 ID입니다.

방문자가 회사 사이트에 로그인하면 일반적으로 회사는 방문자 계정, 포인트 카드, 멤버십 번호 또는 해당 회사에 대한 기타 적용 가능한 식별자에 연결되는 ID를 만듭니다.

[!DNL Target]이 활성화된 페이지에 방문자가 액세스하면 해당 방문자에게 [!DNL Target] PCID가 지정됩니다. 방문자가 로그인하고 구현이 `mbox3rdPartyId`을(를) [!DNL Target]에 전달하면 [!DNL Target]이(가) 해당 방문자의 `mbox3rdPartyId`을(를) [!DNL Target] PCID와 연결합니다.

업데이트는 5~10분마다 프로필 스토어와 동기화됩니다. 방문자의 세션이 종료되면 병합된 데이터가 `mbox3rdPartyId`과(와) 연결된 이전 데이터를 대체하여 해당 방문자의 작업에 대한 전체 레코드를 만듭니다. 동일한 속성이 두 ID에 모두 있는 경우(예: PCID에는 category=hats가 있고 `mbox3rdPartyId`에는 category=skis가 있는 경우) 또는 방문자가 로그인 전에 경험 A를 보았으나 경험 B가 `mbox3rdPartyId`에 저장된 경우 `mbox3rdPartyId`에 저장된 속성이 PCID의 속성을 덮어씁니다. 방문자가 로그인하기 전에 한 활동 또는 경험에 있었으나 다른 활동 및 경험이 `mbox3rdPartyId`에 저장된 경우 로그인한 후 해당 방문자는 `mbox3rdPartyId` 활동 및 경험에 배치됩니다.

| PCID(로그인되지 않음) | mbox3rdPartyID(로그인됨) | 병합되어 mbox3rdPartyID에 저장됨 |
|---|---|---|
| category=hats | category=skis | category=skis |
|   | store=94103 | store=94103 |
| 활동 1, 경험 A | 활동 1, 경험 B | 활동 1, 경험 B |
| 활동 1 |  | 활동 1 |

방문자가 로그아웃해도 병합된 프로필은 그대로 유지됩니다.

>[!NOTE]
>
>인증된(로그인한) 사용자와 인증되지 않은 사용자를 구분하려면 mbox3rdPartyID 대신 [!DNL Adobe Experience Cloud Identity Service](ECID)를 사용하십시오. 사용자가 mbox3rdPartyID에 연결되면, 로그아웃 후에도 사용자와 연결된 상태로 유지됩니다.

>[!NOTE]
>
>[!DNL Target] 프로필이 mbox3rdPartyID를 기반으로 병합될 수 있고 여전히 활동 정보가 있더라도 [!DNL Adobe Experience Cloud] ID(ECID)가 변경되는 경우(예: 방문자가 장치 변경) [!DNL Adobe Analytics] 목표가 추적되지 않습니다. 동일한 ECID로 식별된 방문자의 경우(동일한 장치로 페이지에 액세스하는 방문자) A4T([!DNL Analytics for Target])가 예상대로 작동해야 합니다.

## 고려 사항 {#considerations}

* 페이지에 여러 개의 mbox가 있고 일부만 `3rdPartyID`을(를) 사용하는 경우 [!DNL Target]에는 각 방문자 요청에 대해 별도의 방문자 프로필/컨텍스트가 없습니다. `3rdPartyID` 컨텍스트는 PCID 컨텍스트보다 우선합니다. 한 mbox가 해당 컨텍스트에 대해 `3rdPartyId`을(를) PCID보다 우선하도록 전달하는 것으로 충분합니다.

  예를 들어 방문자가 로그인하기 전에 페이지에 액세스하여 경험을 본다고 가정해 보겠습니다. 글로벌 mbox에서 `3rdPartyID`을(를) 사용하지 않습니다. 로그인 후 방문자는 세 개의 경험 중 하나를 하위 mbox로 보고, 일부는 `3rdPartyID`을(를) 사용합니다. 방문자는 사이트에서 다양한 페이지를 방문한 다음 뒤로 단추를 사용하여 로그인하기 전에 액세스한 기본 페이지로 돌아가서 다른 경험을 봅니다. 이 시나리오에서는 글로벌 mbox가 `3rdPartyID`을(를) 전달하지 않았지만 하나 이상의 하위 mbox가 전달했습니다. `3rdPartyID`이(가) PCID보다 우선했습니다.

* 다음 두 가지 방법을 사용하여 방문자의 고객 ID를 [!DNL Target](으)로 보낼 수 있습니다.

   1. `mbox3rdPartyId`/`thirdPartyId` 사용

      * `mbox3rdPartyId`은(는) `targetPageParams` 또는 `targetPageParamsAll`을(를) 사용할 때의 매개 변수 이름입니다.
      * `thirdPartyId`은(는) 배달 API 페이로드에서 직접 설정한 매개 변수 이름입니다.
      * 이 매개 변수에는 값을 하나만 보낼 수 있습니다.

   1. ECID 서비스의 `setCustomerId`/`customerIds` 함수를 사용합니다.

      * `setCustomerId`은(는) 페이지에서 VisitorAPI.js를 사용할 수 있을 때 클라이언트측(브라우저) 구현에서 사용할 수 있는 함수입니다.
      * `customerIds`은(는) 배달 API 페이로드에서 직접 설정할 때 사용되는 매개 변수 이름으로, 일반적으로 서버측 또는 IOT(사물인터넷) 구현에서 수행됩니다.
      * `mbox3rdPartyId`/`thirdPartyId`과(와) 달리 이 방법에서는 여러 ID를 목록으로 보낼 수 있지만, [!DNL Target]은(는) TnT ID당 하나의 고객 ID만 지원하므로 알려진 별칭(고객 특성 UI에 구성된 별칭)이 있는 목록의 첫 번째 ID를 사용합니다.

  [!DNL Target]이(가) 유일한 [!DNL Adobe Experience Cloud] 솔루션이고 고객 특성을 사용하지 않으려는 경우 `mbox3rdPartyId`/`thirdPartyId`을(를) 사용할 수 있습니다. 다른 모든 경우에는 고객 ID를 보낼 때 `setCustomerId`/`customerIds`을(를) 사용하는 것이 좋습니다.

  >[!IMPORTANT]
  >
  > 한 방문자에 대해 위에서 언급한 두 접근 방식을 혼용하여 사용하면 인증되지 않고 인증된 [!DNL Target] 프로필에 대해 잘못된 프로필 병합이 발생할 수 있습니다.
  >
  >Adobe은 `mbox3rdPartyId`/`thirdPartyId`과(와) `setCustomerID`/`customerIds`을(를) 함께 사용하지 않는 것이 좋습니다.
  >
  >두 접근 방식을 서로 바꿔서 사용해야 하는 경우 `setCustomerID`/`customerIds`에서 사용하는 목록의 첫 번째 ID가 `thirdPartyId`/`mbox3rdPartyId`에서 사용하는 ID인지 또는 그 반대의 ID인지 확인하십시오.

