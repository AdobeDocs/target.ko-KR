---
keywords: Adobe Experience Platform Web SDK;aep 웹 SDK;웹 SDK;sdk;adobe experience cloud;platform edge 네트워크;adobe experience platform edge 네트워크;edge 네트워크;aep edge 네트워크
description: Adobe Experience Platform Web SDK를 사용하여 AEP Edge 네트워크를 통해 Adobe Experience Cloud의 다양한 서비스와 상호 작용하는 방법을 알아봅니다.
title: Experience Platform 웹 SDK를 사용하여 어떻게 구현합니까?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: 636016be6e8a6adc8c4b7fb09af93bb89e28373a
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 5%

---

# Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP 웹 SDK)는 [!DNL Adobe Experience Cloud] Experience Cloud(다음을 포함)의 다양한 서비스와 상호 작용합니다 [!DNL Target]) [!UICONTROL Adobe Experience Platform Edge Network]. JavaScript 라이브러리 외에 [!DNL Adobe Experience Platform] 확장을 사용하여 웹 SDK 구성에 도움을 줄 수 있습니다.

자세한 내용은 *Adobe Experience Platform Web SDK* 도움말:

* 포괄적인 정보는 [Adobe Experience Platform Web SDK란?](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)
* 에 해당하는 정보 [!DNL Target]: [Target 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html)

## 자습서: Platform Web SDK를 사용하여 Adobe Experience Cloud 구현

방법 알아보기 [Adobe Experience Platform Web SDK를 사용하여 Experience Cloud 애플리케이션 구현](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=_blank}. Target 관련 정보는 [Platform Web SDK를 사용하여 Target 설정](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-target.html)자습서 내에서 {target=_blank}.

## 권장 설명서

추가 [!DNL Platform Web SDK] 위에 언급된 설명서, 이 안내서의 항목에는 다음과 같은 정보가 있습니다 [!DNL Platform Web SDK] 관련 [!DNL Target] 기능 및 특징을 참조하십시오.

| 기능 | 설명/링크 |
| --- | --- |
| [활동 QA](/help/c-activities/c-activity-qa/activity-qa.md) | 에서 QA URL 사용 [!DNL Adobe Target] 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행할 수 있습니다. [!UICONTROL 활동 QA] 을(를) 완전히 테스트할 수 있도록 해줍니다. [!DNL Target] 활동을 라이브로 시작하기 전에 활동.<br>자세한 내용은 [Target JavaScript 라이브러리 QA 모드 호환성](/help/c-activities/c-activity-qa/activity-qa.md#compatibility) 및 [미리 보기 URL](/help/c-activities/c-activity-qa/activity-qa.md#preview). |
| [[!UICONTROL Analytics for Target] (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T)는 을 기반으로 활동을 만들 수 있는 교차 솔루션 통합입니다 [!DNL Analytics] 전환 지표 및 대상 세그먼트 . A4T 통합을 사용하여 다음을 사용할 수 있습니다 [!DNL Analytics] 보고서를 사용하여 결과를 검사합니다.<br>자세한 내용은 [지원되는 활동 유형](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) 및 [Adobe Experience Platform Web SDK 구현을 위한 구현 단계](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [대상자](/help/c-target/target.md) | 의 대상 [!DNL Adobe Target] 타깃팅된 활동에서 콘텐츠 및 경험을 보는 사용자를 결정합니다.<br>자세한 내용은 [대상 목록 사용](/help/c-target/c-audiences/audiences.md#use-list) 및 [여러 대상 결합](/help/c-target/combining-multiple-audiences.md). |
| [오퍼 결정](/help/c-integrating-target-with-mac/ajo/offer-decision.md) | Adobe Journey Optimizer에서 만든 오퍼 결정을 Target 활동(수동 A/B 테스트 또는 경험 타깃팅)에 추가하여 웹 및 모바일에서 방문자를 위한 다음 최상의 오퍼를 결정하고 전달합니다. |
| [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오 | 리디렉션 오퍼로 인해 방문자의 브라우저가 새 페이지로 리디렉션됩니다.<br>자세한 내용은 [다음을 수행합니다. [!DNL Adobe Experience Platform Web SDK] a4T에 대한 리디렉션 오퍼를 지원합니까?](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [응답 토큰](/help/administrating-target/response-tokens.md) | 응답 토큰을 사용하면 Target 데이터를 Google Analytics 및 기타 타사 통합에 보낼 수 있습니다.<br>자세한 내용은 [Platform Web SDK를 통해 Google Analytics에게 데이터 보내기](/help/administrating-target/response-tokens.md#platform-web-sdk) 를 입력하여 이 작업을 수행하는 방법에 대한 코드 샘플을 볼 수 있습니다. |
| [단일 페이지 애플리케이션 구현](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) 에서 *Platform Web SDK 개요* 안내서. | [!UICONTROL Adobe Experience Platform Web SDK] 에서는 단일 페이지 애플리케이션(SPA)과 같은 차세대 클라이언트측 기술에 대한 개인화를 실행하도록 기업을 지원하는 다양한 기능을 제공합니다. |
| [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | TLS(Transport Layer Security)는 가장 높은 보안 표준을 유지 관리하고 고객 데이터의 안전을 높이는 데 도움이 됩니다. |
