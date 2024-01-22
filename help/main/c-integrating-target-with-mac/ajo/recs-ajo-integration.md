---
keywords: ajo;adobe 여정 최적화 도구;adobe 여정 최적화 도구 target 통합;권장 사항;target 권장 사항;통합
description: 통합 [!DNL Adobe Target Recommendations] 포함 [!DNL Adobe Journey Optimizer].
title: 사용 방법 [!DNL Target Recommendations] 를 사용하는 고객 여정에서 [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
source-git-commit: 1faedc44c4f8f95000b666af8eecaf1eca5bf48d
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 3%

---

# 통합 [!DNL Adobe Target Recommendations] 및 [!DNL Adobe Journey Optimizer]

이 문서에서는 간의 통합을 설정하는 데 도움이 되는 사용 사례 및 정보에 대해 설명합니다 [!DNL Adobe Target Recommendation] 및 [!DNL Adobe Journey Optimizer] 을 통해 고객에게 연관성 있고 상황에 맞는 개인화된 경험을 제공할 수 있습니다.

## 전제 조건

을(를) 사용하려면 [!DNL Target Recommendations] 및 [!DNL Adobe Journey Optimizer] 통합하려면 다음이 필요합니다.

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) 를 사용하여 구현됨 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  기능은에서 사용할 수 없습니다. [!DNL Target Standard] 라이센스 또는 구현 시 [!DNL Target] at.js 또는 기타 [!DNL Target] SDK.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## 샘플 사용 사례

다음은 를 통합할 때 가능한 두 가지 사용 사례입니다 [!DNL Target Recommendations] 포함 [!DNL Adobe Journey Optimizer]:

* **[!DNL Customer Journey Optimizer]장바구니 포기 후 개인화된 이메일을 보냅니다.**: 이 사용 사례는 고객이 웹 사이트를 방문하여 장바구니에 품목을 넣은 다음 구매 프로세스를 완료하지 않고 사이트를 나가는 경우를 기반으로 합니다.

  예를 들어 방문자가 의류 회사의 웹 사이트를 방문하여 장바구니에 겨울 코트 2개와 스웨트 셔츠를 둔다고 가정해 봅시다. 그런 다음 방문자는 주의가 산만해져 웹 사이트를 떠나거나 구매를 확신하지 못하고 브라우저나 앱을 닫습니다.

  지정된 기간 후(아마도 몇 시간 또는 하루) 의 사용자 지정 작업 [!DNL Adobe Journey Optimizer] 을 호출합니다. [!DNL Target Recommendations] 포기한 장바구니의 컨텐츠를 확인합니다. [!DNL Adobe Journey Optimizer] 그런 다음 이 방문자에게 구매 프로세스가 완료되지 않았다는 알림 메시지와 함께 이미지 및 구매하지 않은 항목에 대한 링크를 개인화된 전자 메일로 보냅니다.

* **[!DNL Customer Journey Optimizer]사용자 프로필을 사용하여 사이트 방문 후 이메일을 보냅니다.**: 이 사용 사례는 고객이 웹 사이트를 방문하여 다양한 항목을 본 다음 장바구니에 항목을 배치하지 않고 사이트를 나가는 경우를 기반으로 합니다.

  지정된 기간 후 의 사용자 지정 작업 [!DNL Adobe Journey Optimizer] 을 호출합니다. [!DNL Target Recommendations] 이 방문자가 방문자의 [!DNL Adobe Experience Cloud Identifier] (EDID). [!DNL Adobe Journey Optimizer] 그런 다음 이 방문자에게 구매 프로세스가 완료되지 않았다는 알림 메시지와 함께 이미지 및 구매하지 않은 항목에 대한 링크를 개인화된 전자 메일로 보냅니다.

