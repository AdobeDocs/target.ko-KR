---
keywords: ajo;adobe 여정 최적화 도구;adobe 여정 최적화 도구 target 통합;권장 사항;target 권장 사항;통합
description: ' [!DNL Adobe Target Recommendations] 을(를)  [!DNL Adobe Journey Optimizer]과(와) 통합합니다.'
title: ' [!DNL Adobe Journey Optimizer]을(를) 사용하는 고객 여정에서  [!DNL Target Recommendations] 을(를) 사용하려면 어떻게 합니까?'
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
exl-id: 81bbbd51-47fc-4e23-a1cb-7c18fea1c159
source-git-commit: b4f9e14f9dfa94f8648686e43e66eee7e0f7daa1
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 1%

---

# [!DNL Adobe Target Recommendations]과(와) [!DNL Adobe Journey Optimizer] 통합

이 문서에서는 [!DNL Adobe Target Recommendations]을(를) [!DNL Adobe Journey Optimizer]과(와) 통합하기 위한 사용 사례 및 지침을 제공하여 연관성 있고 상황에 맞는 개인화된 고객 경험을 제공할 수 있도록 합니다.

이 통합은 더 많은 전환을 유도하고 개인화된 권장 사항이 포함된 이메일 메시지의 영향을 확인하는 데 도움이 됩니다.

## 전제 조건

[!DNL Target Recommendations] 및 [!DNL Adobe Journey Optimizer] 통합을 사용하려면 다음이 필요합니다.

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium)이(가) [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}을(를) 사용하여 구현되었습니다.

  이 기능은 [!DNL Target Standard] 라이선스나 at.js 또는 다른 [!DNL Target] SDK를 사용하여 [!DNL Target]을(를) 구현하는 경우에는 사용할 수 없습니다.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home){target=_blank}.

## 샘플 사용 사례

이러한 사용 사례는 [!DNL Target Recommendations]을(를) [!DNL Adobe Journey Optimizer]과(와) 통합하는 데 사용할 수 있는 몇 가지 사용 사례입니다.

* **[!DNL Adobe Journey Optimizer]에서 장바구니 포기 후 개인화된 전자 메일을 보냅니다**: 이 사용 사례는 고객이 웹 사이트를 방문하여 장바구니에 항목을 넣은 다음 구매 프로세스를 완료하지 않고 사이트를 나가는 것을 기반으로 합니다.

  예를 들어 방문자가 의류 회사의 웹 사이트를 방문하여 장바구니에 겨울 코트 2개와 스웨트 셔츠를 둔다고 가정해 봅시다. 그런 다음 방문자는 주의가 산만해져 웹 사이트를 떠나거나 구매를 확신하지 못하고 브라우저나 앱을 닫습니다.

  지정된 기간 후, 아마도 몇 시간 또는 하루 후에 [!DNL Journey Optimizer]의 사용자 지정 작업에서 [장바구니 기반 권장 사항](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) 알고리즘을 사용하여 포기한 장바구니의 콘텐츠를 결정하기 위해 [!DNL Target Recommendations]을(를) 호출합니다. 그런 다음 [!DNL Journey Optimizer]이(가) 구매가 완료되지 않았다는 알림 메시지와 함께 이미지 및 구매하지 않은 항목에 대한 링크를 이 방문자에게 보냅니다.

* **[!DNL Adobe Journey Optimizer]이(가) 사이트 방문 후 대량 전자 메일을 보내 방문자에게 어떤 항목을 보았는지 알려줍니다**: 이 사용 사례는 방문자가 웹 사이트를 방문하고 다양한 항목을 본 다음 장바구니에 항목을 배치하지 않고 사이트 또는 앱을 종료하는 것을 기반으로 합니다.

  지정된 기간 후에 [!DNL Journey Optimizer]의 사용자 지정 작업에서 [!DNL Target Recommendations]을(를) 호출하여 각 방문자의 EDID([!DNL Adobe Experience Cloud Identifier]), 방문자의 [!DNL Target] 프로필 및 [사용자 기반](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) 알고리즘을 사용하여 각 방문자가 본 항목을 결정합니다. 그런 다음 [!DNL Adobe Journey Optimizer]은(는) 자격 있는 대상의 각 구성원에게 이미지와 각 방문자의 표시된 항목에 대한 링크가 포함된 개인화된 전자 메일을 보내어 방문자가 돌아와서 구매하도록 합니다.

  이 시나리오에서는 [!UICONTROL Experience Cloud Visitor ID] (ECID) 및 각 방문자의 [!DNL Target] 프로필에 있는 콘텐츠를 사용하여 최근에 본 알고리즘을 기반으로 권장 사항을 생성합니다.

  예를 들어 방문자가 소매 웹 사이트를 방문하여 여러 개의 시계를 본다고 가정해 봅시다. 이 방문자의 [!DNL Target] 프로필이 표시된 시계 목록으로 업데이트되었습니다. [!DNL Target]이(가) ECID와 방문자의 [!DNL Target] 프로필을 사용하여 [!DNL Journey Optimizer]에게 권장 사항을 보냅니다. 그런 다음 [!DNL Journey Optimizer]은(는) 최근에 본 알고리즘을 사용하여 이 방문자가 본 시계에 대한 이미지와 링크가 포함된 전자 메일을 보냅니다. 다른 방문자는 이 방문자가 본 항목에 대한 이미지와 링크가 포함된 개인화된 이메일을 수신합니다. 각 이메일 메시지는 각 방문자에 대해 개인화됩니다.

* **[!DNL Adobe Journey Optimizer]이(가) 사이트 방문 후 자격 있는 방문자에게 대량 전자 메일을 보내 인기 항목을 제안합니다**: 이 사용 사례는 방문자가 웹 사이트를 방문하지만 특정 항목을 보지 않은 경우를 기반으로 합니다. 이메일은 특정 대상의 자격을 규정하는 모든 방문자에게 일괄적으로 전송됩니다. 예를 들면 다음과 같습니다.

  방문자가 특정 시계를 보지 않는다고 가정합시다. 방문자가 단순히 사이트를 클릭해서 카테고리 페이지나 블로그 항목을 본 것 같습니다. 따라서 [!DNL Target] 프로필에는 최근에 본 항목에 대한 특정 정보가 없습니다. 이 경우 [!DNL Target Recommendations]은(는) [백업 권장 사항](/help/main/c-recommendations/c-algorithms/backup-recs.md)을 사용하므로 [!DNL Journey Optimizer]은(는) 이미지와 웹 사이트의 인기 항목에 대한 링크가 포함된 전자 메일을 보내 방문자가 돌아와서 구매할 수 있습니다.
