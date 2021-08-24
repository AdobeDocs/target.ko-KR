---
keywords: Adobe Experience Platform Web SDK;aep 웹 SDK;웹 SDK;sdk;adobe experience cloud;platform edge 네트워크;adobe experience platform edge 네트워크;edge 네트워크;aep edge 네트워크
description: Adobe Experience Platform Web SDK를 사용하여 AEP Edge 네트워크를 통해 Adobe Experience Cloud의 다양한 서비스와 상호 작용하는 방법을 알아봅니다.
title: Experience Platform 웹 SDK를 사용하여 어떻게 구현합니까?
feature: AEP 웹 SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 6%

---

# Adobe Experience Platform 웹 SDK

[!DNL Adobe Experience Platform Web SDK] (AEP 웹 SDK)는 고객이  [!DNL Adobe Experience Cloud] Adobe Experience Platform Edge Network [!DNL Target]를 통해 Experience Cloud( [!UICONTROL  포함)에서 다양한 서비스와 상호 작용할 수 ]있는 클라이언트측 JavaScript 라이브러리입니다. JavaScript 라이브러리 외에 웹 SDK 구성에 도움이 되는 [!DNL Adobe Experience Platform] 확장이 있습니다.

자세한 내용은 *Adobe Experience Platform Web SDK* 도움말에서 다음 링크를 참조하십시오.

* 포괄적인 정보는 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)
* [!DNL Target]에 관한 정보는 [Target 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html)

## 권장 설명서

위에 언급된 [!DNL Platform Web SDK] 설명서 외에, 이 안내서의 항목에는 [!DNL Target] 기능 및 기능과 관련된 [!DNL Platform Web SDK] 관련 정보도 있습니다.

| 기능 | 설명/링크 |
| --- | --- |
| [활동 QA](/help/c-activities/c-activity-qa/activity-qa.md) | [!DNL Adobe Target]의 QA URL을 사용하여, 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행할 수 있습니다. [!UICONTROL 활동 ] QA를 사용하면 활동을  [!DNL Target] 실시간으로 실행하기 전에 활동을 완전히 테스트할 수 있습니다.<br>JavaScript  [라이브러리 QA 모드 호환성 ](/help/c-activities/c-activity-qa/activity-qa.md#compatibility) 및 미리  [보기 URL Target](/help/c-activities/c-activity-qa/activity-qa.md#preview)를 참조하십시오. |
| [[!UICONTROL Analytics for Target] (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T)는  [!DNL Analytics] 전환 지표 및 대상 세그먼트를 기반으로 활동을 만들 수 있는 교차 솔루션 통합입니다. A4T 통합을 사용하면 [!DNL Analytics] 보고서를 사용하여 결과를 검사할 수 있습니다.<br>Adobe Experience Platform  [Web ](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) SDK  [구현에 대해 지원되는 활동 유형 및 구현 단계 를 참조하십시오](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [대상자](/help/c-target/target.md) | [!DNL Adobe Target]의 대상은 타깃팅된 활동에서 컨텐츠 및 경험을 보는 사용자를 결정합니다.<br>대상  [라이브러리 ](/help/c-target/c-audiences/audiences.md#use-list) 사용  [여러 대상 결합](/help/c-target/combining-multiple-audiences.md)을 참조하십시오. |
| [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오 | 리디렉션 오퍼로 인해 방문자의 브라우저가 새 페이지로 리디렉션됩니다.<br>A4T [에  [!DNL Adobe Experience Platform Web SDK] 대해 리디렉션 오퍼가 지원됩니까? 를 참조하십시오.](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [응답 토큰](/help/administrating-target/response-tokens.md) | 응답 토큰을 사용하면 Target 데이터를 Google Analytics 및 기타 타사 통합에 보낼 수 있습니다.<br>이  [작업을 수행하는 방법에 대한 코드 샘플을 보려면 Platform Web ](/help/administrating-target/response-tokens.md#platform-web-sdk) SDK를 통해 Google Analytics에 데이터 보내기 를 참조하십시오. |
| [Platform Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) 개요 안내서의  *단일 페이지 애플리케이션* 구현. | [!UICONTROL Adobe Experience Platform 웹 ] SDK는 SPA(단일 페이지 애플리케이션)과 같은 차세대 클라이언트측 기술에 대한 개인화를 실행하도록 기업을 지원하는 다양한 기능을 제공합니다. |
| [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | TLS(Transport Layer Security)는 가장 높은 보안 표준을 유지 관리하고 고객 데이터의 안전을 높이는 데 도움이 됩니다. |
