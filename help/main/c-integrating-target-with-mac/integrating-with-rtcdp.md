---
keywords: Real-Time Customer Data Platform;rtcdp;개인화;aep 대상자;adobe experience platform 대상자;프로필 속성
description: ' [!DNL Target]/[!DNL Real-Time Customer Data Platform] (RTCDP) 통합을 사용하여 더 풍부한 고객 데이터와 보다 효과적인 개인화를 제공하는 방법에 대해 알아보십시오.'
title: ' [!DNL Target] 을  [!DNL Real-Time Customer Data Platform]과 통합하려면 어떻게 합니까?'
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: cf7af568f270f97868107032897cd4fdd8e45131
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 90%

---

# [!DNL Real-Time Customer Data Platform]과 통합

[!DNL Adobe Experience Platform] 플랫폼을 기반으로 구축된 [!DNL Real-Time Customer Data Platform](RTCDP)은 기업이 여러 엔터프라이즈 소스의 알려진 데이터와 익명 데이터를 통합할 수 있도록 지원합니다. RTCDP를 통해 모든 채널 및 디바이스에서 실시간으로 개인화된 고객 경험을 제공하는 데 사용할 수 있는 고객 프로필을 만들 수 있습니다.

RTCDP에 대한 자세한 내용은 [Real-Time Customer Data Platform 개요](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}를 참조하십시오.

## 주요 기능

주요 기능은 다음과 같습니다.

* 에지에서 Real-Time CDP/[!DNL Adobe Experience Platform]과 직접 [!DNL Target] 통합 ([!DNL Audience Core services] - AAM에 대한 종속성 제거)
* 거버넌스 및 정책 시행 기능이 포함된 [!UICONTROL Target 에지 대상 카드]
* Real-time CDP 세그먼트 및 공유 프로필 속성

## 구현 시나리오

다음 섹션에서는 다양한 구현 방법을 사용할 때 사용할 수 있는 개인화 사용 사례 유형(다음 세션 또는 동일 페이지)이 표시됩니다.

### at.js 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager](AAM) 및 [!DNL Target]</li><li>[!DNL RTCDP](Premium 또는 Ultimate) 및[!DNL Target]</li><li>[!DNL RTCDP](모든 SKU), [!DNL AAM] 및 [!DNL Target]</li></ul> | 다음 세션 개인화 |

### [!DNL Adobe Experience Platform Web SDK] 또는 [!DNL Experience Platform Server-Side API] 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL RTCDP](모든 SKU) 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><li>에지를 통한 동일 페이지 개인화</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul> |
| <ul><li>[!DNL RTCDP](모든 SKU), [!DNL AAM] 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>[!DNL AAM] 세그먼트</li><li>[!DNL AAM]을 통한 서드파티 세그먼트</li></ul><li>에지를 통한 동일 페이지 개인화</li><ul><li>[!DNL RTCDP] 세그먼트</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul> |

### [!UICONTROL at.js]와 [!DNL Platform Web SDK]의 혼합 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL RTCDP](모든 SKU) 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>[!UICONTROL at.js]가 포함된 모든 페이지의 경우</li></ul><li>동일 페이지 개인화</li><ul><li>[!DNL Platform Web SDK]가 포함된 모든 페이지의 경우</li></ul> |
| <ul><li>[!DNL RTCDP](모든 SKU), [!DNL AAM] 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>[!UICONTROL at.js]가 포함된 모든 페이지의 경우</li><li>[!DNL AAM] 세그먼트</li><li>[!DNL AAM]을 통한 서드파티 세그먼트</li></ul> |

## 세그먼트 평가 시간

다음 표에서는 다양한 구현 시나리오에서 발생하는 이벤트에 대한 세그먼트 평가 시간이 표시됩니다.

| 시나리오 | 에지 세그먼트 (밀리초 평가) | 스트리밍 세그먼트 (분 평가) | 배치 세그먼트 평가 |
| --- | --- | --- | --- |
| DNL [!DNL Adobe Experience Platform] SDK의 이벤트/데이터 | 예 | 예 | 해당 사항 없음 |
| [!UICONTROL at.js] 이벤트 | 아니요 | 예 | 해당 사항 없음 |
| [!DNL Target Mobile] SDK 이벤트 | 아니요 | 예 | 해당 사항 없음 |
| 배치 업로드 이벤트 | 아니요 | 아니요 | 예 |
| 오프라인 데이터 이벤트 (스트림) | 아니요 | 예 | 예 |

## [!DNL Adobe Experience Platform]의 대상자 사용 {#aep}

[!DNL Adobe Experience Platform]에서 생성된 [대상자](/help/main/c-target/c-audiences/audiences.md)를 사용하면 더 풍부한 고객 데이터를 제공하여 보다 효과적인 개인화를 실현할 수 있습니다. [!DNL Adobe Experience Platform]을 기반으로 구축된 [Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}(RTCDP)은 기업이 여러 엔터프라이즈 소스의 알려진 데이터와 익명 데이터를 통합할 수 있도록 지원합니다. 이 프로세스를 통해 모든 채널 및 디바이스에서 실시간으로 개인화된 고객 경험을 제공하는 데 사용할 수 있는 고객 프로필을 만들 수 있습니다.

[!DNL Target]을 [!DNL Real-Time Customer Data Platform]에 연결하면 고객은 웹 개인화를 강화할 수 있습니다. 이 통합을 통해 이전에는 [!DNL Target]에서 액세스할 수 없었던 새로운 세그먼트의 잠금을 해제하여 고객의 웹 방문 첫 페이지에서 실시간 밀리초 개인화를 활성화할 수 있습니다. [!DNL Adobe Experience Platform]에서 생성된 대상자 및 프로필 속성을 사용하면 사용 가능한 데이터 포인트를 확장하여 보다 풍부한 개인화를 수행할 수 있습니다.

이 통합을 통해 Real-Time CDP의 주요 사용 사례를 활용할 수 있습니다.

* 동일 페이지 / 다음 히트 개인화
* 최초 / 알 수 없는 사용자 개인화

## [!DNL Target]과 Real-Time CDP 프로필 속성 공유 {#rtcdp-profile-attributes}

Real-Time CDP 프로필 속성을 [!DNL Target]과 공유하여 HTML 오퍼 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md)에 사용할 수 있습니다.

### Real-Time CDP 프로필 속성 기능의 제한 사항 및 고려 사항

>[!NOTE]
>
>Real-Time CDP 프로필 속성 기능은 현재 HTML 오퍼 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md)에 대해 Beta 버전으로 제공됩니다.

다음 사항을 고려하십시오.

* 지정된 오퍼 내의 속성은 동일한 [!UICONTROL Experience Platform] 샌드박스의 속성이어야 합니다. (즉, 오퍼에는 서로 다른 [!UICONTROL Experience Platform] 샌드박스의 속성을 포함할 수 없습니다.)
* 지정된 오퍼 내의 속성은 서로 다른 소스, 즉 [!DNL Target] 프로필과 [!UICONTROL Experience Platform] 프로필에서 가져올 수 있습니다. (즉, [!DNL Target]에서 가져온 속성이든 [!UICONTROL Experience Platform] 프로필에서 가져온 속성이든 모두 결합할 수 있습니다.)
* 오퍼를 정의할 때 속성에 명시적인 값이 없는 경우 [!UICONTROL Real-Time CDP 프로필 속성]에 대한 기본값을 지정할 수 있습니다. 예를 들어 개인화 서비스에서 사용 중인 속성을 동의 또는 거버넌스 정책이 차단하는 경우 기본값을 대신 사용할 수 있습니다.

### JSON 샘플 사용 사례

온라인 마케터라면 AEP/통합 프로필이 [!DNL Target]과 속성 값을 공유하여 실시간 개인화를 제공하기를 원할 수 있습니다. [!UICONTROL Real-Time CDP 프로필 속성]을 사용하면 토큰 대체를 사용하여 [!DNL Target] 오퍼에 [!UICONTROL Experience Platform] 속성 값을 표시할 수 있습니다. 예를 들어 `${aep.profile.favoriteColor}`을(를) 사용하여 고객이 선호하는 색상에 따라 개인화하거나 `${aep.loyalty.tier}` 및 `${aep.loyalty.points}` 토큰을 사용하여 고객의 로열티 등급 및 로열티 포인트 값에 따라 개인화할 수 있습니다.

AEP/통합 프로필 속성을 [!DNL Target]과 공유하기 위한 JSON 오퍼를 만들려면 다음 작업을 수행하십시오.

1. [JSON 오퍼를 만드는](/help/main/c-experiences/c-manage-content/create-json-offer.md) 동안 **[!UICONTROL 소스 선택]** 목록에서 **[!UICONTROL Adobe Experience Platform]**&#x200B;을 선택합니다.
1. **[!UICONTROL 프로필 샌드박스 이름 선택]** 목록에서 원하는 샌드박스를 선택합니다.
1. **[!UICONTROL 프로필 속성 선택]** 목록에서 원하는 속성을 선택합니다.
1. (선택 사항) **[!UICONTROL 기본값 삽입]** 목록에서 원하는 값을 선택합니다.
1. **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

다음 그림은 두 개의 프로필 속성(`loyalty.tier` 및 `loyalty.points`)이 JSON 오퍼에 추가되었음을 보여 줍니다.

![offer-json-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## 추가 정보 링크

자세한 내용은 다음 주제를 참조하십시오.

* *Adobe Experience Platform 릴리스 정보*&#x200B;의 [대상 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko#destinations){target=_blank}
* *대상 개요* 안내서에서 [동일 페이지 및 다음 페이지 개인화에 대한 개인화 대상을 구성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank}합니다.
* *대상 개요* 안내서의 [Adobe Target 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank}
* *대상 개요* 안내서의 [맵 속성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=en#map-attributes){target=_blank}.

## 비디오 및 블로그 게시물 {#videos-blogs}

Target 및 RTCDP를 통한 향상된 개인화에 대한 자세한 내용은 다음 비디오 및 블로그 게시물을 참조하십시오.

### 비디오: Real-Time CDP 및 [!DNL Adobe Target]을 사용하여 다음 히트 개인화{#RTCDP}

[!DNL Real-Time Customer Data Platform] 및 [!DNL Adobe Target]을 사용하여 다음 히트를 개인화하는 방법을 알아보십시오. [!DNL Real-Time CDP]의 [!DNL Adobe Target] 대상을 통해 [!DNL Adobe Target]의 [!DNL Experience Platform] 세그먼트를 사용하여 거버넌스 및 개인정보 보호 지원 기능을 제공받으며 동일 페이지 개인화 및 다음 페이지 개인화를 수행할 수 있습니다.

자세한 내용은 *Platform 튜토리얼* 안내서에서 [Real-Time CDP 및 Adobe Target을 사용하여 다음 히트 개인화](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank}를 참조하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### 비디오: 구성 [!DNL Adobe Target] 대상 위치: [!DNL Real-Time Customer Data Platform]

구성 방법 알아보기 [!DNL Adobe Target] 대상 위치: [!DNL Real-Time Customer Data Platform] 에서 세그먼트 및 프로필 속성 전송을 시작하려면 [!DNL Real-Time CDP] 끝 [!DNL Target].

>[!VIDEO](https://video.tv.adobe.com/v/3418799/?learn=on)

### 비디오: 세그먼트 및 프로필 속성 활성화

에서 세그먼트 및 프로필 속성을 활성화하는 방법을 알아봅니다 [!DNL Adobe Real-Time Customer Data Platform] 끝 [!DNL Adobe Target] 을 사용하여 웹 사이트, 모바일 앱 및 기타 디지털 속성에 개인화된 실시간 컨텐츠를 표시할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3419036/?learn=on)

### 비디오: 사용 [!DNL Real-Time CDP] 의 세그먼트 [!DNL Target]

사용 방법 알아보기 [!DNL Real-Time Customer Data Platform] 의 세그먼트 [!DNL Adobe Target] 웹 사이트 및 모바일 앱에서 개인화된 경험을 제공할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3419149/?learn=on)

### 비디오: 사용 [!DNL Real-Time CDP] 의 프로필 속성 [!DNL Adobe Target]

사용 방법 알아보기 [!DNL Adobe Real-Time Customer Data Platform] 의 프로필 속성 [!DNL Adobe Target] 웹 사이트 및 모바일 앱에서 개인화된 경험을 제공할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3419318/?learn=on)

### [!DNL Adobe Target] 블로그 및 비디오: 동일 페이지의 향상된 개인화

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] 및 [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
