---
keywords: ajo;adobe 여정 최적화 도구;adobe 여정 최적화 도구 target 통합;권장 사항;target 권장 사항;통합
description: 통합 [!DNL Adobe Target Recommendations] 포함 [!DNL Adobe Journey Optimizer].
title: 사용 방법 [!DNL Target Recommendations] 를 사용하는 고객 여정에서 [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
source-git-commit: ce74c85380333476b97f47fab4d2659a3c9c86e1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# 통합 [!DNL Adobe Target Recommendations] 및 [!DNL Adobe Journey Optimizer]

이 문서에서는 간의 통합을 설정하는 데 도움이 되는 사용 사례 및 정보에 대해 설명합니다 [!DNL Adobe Target Recommendations] 및 [!DNL Adobe Journey Optimizer] 을 통해 고객에게 연관성 있고 상황에 맞는 개인화된 경험을 제공할 수 있습니다.

이 통합은 더 많은 전환을 유도하고 개인화된 권장 사항이 포함된 이메일 메시지의 영향을 확인하는 데 도움이 됩니다.

## 전제 조건

을(를) 사용하려면 [!DNL Target Recommendations] 및 [!DNL Adobe Journey Optimizer] 통합하려면 다음이 필요합니다.

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) 를 사용하여 구현됨 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  이 기능은 다음에서 사용할 수 없습니다. [!DNL Target Standard] 라이센스 또는 구현 시 [!DNL Target] at.js 또는 기타 [!DNL Target] SDK.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## 샘플 사용 사례

다음은 를 통합하는 데 사용할 수 있는 몇 가지 사용 사례입니다 [!DNL Target Recommendations] 포함 [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]장바구니 포기 후 개인화된 이메일을 보냅니다.**: 이 사용 사례는 고객이 웹 사이트를 방문하여 장바구니에 품목을 넣은 다음 구매 프로세스를 완료하지 않고 사이트를 나가는 경우를 기반으로 합니다.

  예를 들어 방문자가 의류 회사의 웹 사이트를 방문하여 장바구니에 겨울 코트 2개와 스웨트 셔츠를 둔다고 가정해 봅시다. 그런 다음 방문자는 주의가 산만해져 웹 사이트를 떠나거나 구매를 확신하지 못하고 브라우저나 앱을 닫습니다.

  지정된 기간 후(아마도 몇 시간 또는 하루) 의 사용자 지정 작업 [!DNL Adobe Journey Optimizer] 을 호출합니다. [!DNL Target Recommendations] 을(를) 사용하여 포기한 장바구니의 콘텐츠 확인 [장바구니 기반 권장 사항](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) 알고리즘. [!DNL Adobe Journey Optimizer] 그런 다음 이 방문자에게 구매 프로세스가 완료되지 않았다는 알림 메시지와 함께 이미지 및 구매하지 않은 항목에 대한 링크를 개인화된 전자 메일로 보냅니다.

* **[!DNL Adobe Journey Optimizer]은(는) 사이트 방문 후 방문자에게 열람된 항목을 알려 주기 위해 벌크 이메일을 보냅니다.**: 이 사용 사례는 방문자가 웹 사이트를 방문하고 다양한 항목을 본 다음 장바구니에 항목을 배치하지 않고 사이트 또는 앱을 떠나는 경우를 기반으로 합니다.

  지정된 기간 후 의 사용자 지정 작업 [!DNL Adobe Journey Optimizer] 을 호출합니다. [!DNL Target Recommendations] 각 방문자의 항목을 사용하여 각 방문자가 본 항목 확인 [!DNL Adobe Experience Cloud Identifier] (EDID), 방문자의 [!DNL Target] 프로필 및 [사용자 기반](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) 알고리즘. [!DNL Adobe Journey Optimizer] 그런 다음 자격이 있는 대상자의 각 구성원에게 이미지와 각 방문자의 표시된 항목에 대한 링크가 포함된 개인화된 이메일을 보내어 방문자가 재방문하여 구매하도록 합니다.

  이 시나리오에서는 [!UICONTROL Experience Cloud 방문자 ID] (ECID) 및 각 방문자의 콘텐츠 [!DNL Target] 프로필은 최근에 본 알고리즘을 기반으로 추천을 생성하는 데 사용됩니다.

  예를 들어 방문자가 소매 웹 사이트를 방문하여 여러 개의 시계를 본다고 가정해 봅시다. 이 방문자의 [!DNL Target] 프로필이 조회한 시계 목록으로 업데이트됩니다. ECID 및 방문자 사용 [!DNL Target] 프로필, [!DNL Target] 추천 발송 대상 [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] 그런 다음 최근에 본 알고리즘을 사용하여 이 방문자가 본 시계에 대한 이미지와 링크가 포함된 이메일을 보냅니다. 다른 방문자는 이 방문자가 본 항목에 대한 이미지와 링크가 포함된 개인화된 이메일을 수신합니다. 각 이메일 메시지는 각 방문자에 대해 개인화됩니다.

* **[!DNL Adobe Journey Optimizer]인기 있는 항목을 제안하기 위해 사이트 방문 후 자격을 갖춘 방문자에게 벌크 이메일을 보냅니다.**: 이 사용 사례는 웹 사이트를 방문하는 방문자를 기반으로 하지만 특정 항목을 보지 않습니다. 이메일은 특정 대상에 적합한 모든 사용자에게 일괄적으로 전송됩니다. 예를 들면 다음과 같습니다.

  방문자가 특정 시계를 보지 않는다고 가정합시다. 방문자가 단순히 사이트를 클릭해서 카테고리 페이지나 블로그 항목을 본 것 같습니다. 그 결과 [!DNL Target] 프로필에 최근에 본 항목에 대한 특정 정보가 없습니다. 이런 상황에서는 [!DNL Target Recommendations] 를 사용합니다. [백업 권장 사항](/help/main/c-recommendations/c-algorithms/backup-recs.md) 그래서 [!DNL Adobe Journey Optimizer] 은 웹 사이트에서 인기 있는 항목에 대한 이미지와 링크가 포함된 이메일을 보내어 방문자가 돌아와서 구매할 수 있도록 할 수 있습니다.


