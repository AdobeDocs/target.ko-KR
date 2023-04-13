---
keywords: Real-time Customer Data Platform;rtcdp;개인화;aep 대상;adobe experience platform 대상;프로필 속성
description: ' [!DNL Target]/[!DNL Real-time Customer Data Platform] (RTCDP) 통합을 사용하여 더 풍부한 고객 데이터와 보다 효과적인 개인화를 제공하는 방법에 대해 알아보십시오.'
title: ' [!DNL Target] 을  [!DNL Real-time Customer Data Platform]과 통합하려면 어떻게 합니까?'
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: b31fc335c2066f74ec9aebe835a2c47822a49e5a
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 9%

---

# 통합 대상 [!DNL Real-time Customer Data Platform]

기본 제공 [!DNL Adobe Experience Platform], [!DNL Real-time Customer Data Platform] (RTCDP)는 기업이 여러 엔터프라이즈 소스에서 알려진 데이터와 익명의 데이터를 통합하는 데 도움이 됩니다. RTCDP를 사용하면 모든 채널 및 장치에서 실시간으로 개인화된 고객 경험을 제공하는 데 사용할 수 있는 고객 프로필을 만들 수 있습니다.

RTCDP에 대한 자세한 내용은 [Real-time Customer Data Platform 개요](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}.

## 다음에서 대상 사용 [!DNL Adobe Experience Platform] {#aep}

사용 [대상자](/help/main/c-target/c-audiences/audiences.md) 에서 생성됨 [!DNL Adobe Experience Platform] 는 더 효과적인 개인화를 생성하는 더 풍부한 고객 데이터를 제공합니다. 다음 [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), 구축 [!DNL Adobe Experience Platform]는 회사가 여러 엔터프라이즈 소스에서 알려진 데이터와 익명의 데이터를 통합하는 데 도움이 됩니다. 이 프로세스를 통해 모든 채널 및 장치에서 실시간으로 개인화된 고객 경험을 제공하는 데 사용할 수 있는 고객 프로필을 만들 수 있습니다.

연결 [!DNL Target] 변환 후 [!DNL Real-time Customer Data Platform], 고객은 웹 개인화를 보강할 수 있습니다. 이 통합을 사용하면 이전에 액세스할 수 없었던 새로운 세그먼트의 잠금을 해제할 수 있습니다 [!DNL Target] 고객 웹 방문의 첫 페이지에서 실시간 개인화를 사용하도록 설정하려면 다음을 수행하십시오. 에서 만들어진 대상 및 프로필 속성 사용 [!DNL Adobe Experience Platform] 더 풍부한 개인화를 위해 사용 가능한 데이터 포인트를 확장할 수 있습니다.

이러한 통합은 실시간 CDP를 사용하여 주요 사용 사례를 잠금 해제합니다.

* 동일 페이지/다음 히트 개인화
* 최초/알 수 없는 사용자 개인화

### 주요 기능

주요 기능은 다음과 같습니다.

* 직접 [!DNL Target] 실시간 CDP와 통합/[!DNL Adobe Experience Platform] Edge에 대한 종속성 제거 [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations 카드] 정부 및 정책 집행
* 실시간 CDP 세그먼트 및 공유 프로필 속성

### 개인화 사용 사례

다음 섹션에서는 다른 구현 방법을 사용할 때 사용할 수 있는 개인화 사용 사례(다음 세션 또는 동일한 페이지)를 보여줍니다.

#### at.js 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) 및 [!DNL Target]</li><li>[!DNL RTCDP] (Premium 또는 Ultimate) 및 [!DNL Target]</li><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul> | 다음 세션 개인화 |

#### Adobe Experience Platform Web SDK 또는 Experience Platform 서버측 API 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL RTCDP] (모든 SKU) 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><li>Edge를 통한 동일한 페이지 개인화</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul> |
| <ul><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>[!DNL AAM] 세그먼트</li><li>을 통해 타사 세그먼트 [!DNL AAM]</li></ul><li>Edge를 통한 동일한 페이지 개인화</li><ul><li>[!DNL RTCDP] 세그먼트</li><li>세그먼트 공유 시 적용되는 거버넌스</li></ul> |

#### 혼합 [!UICONTROL at.js] 및 [!DNL Platform Web SDK] 구현

| 솔루션 | 사용 사례 활성화 |
| --- | --- |
| <ul><li>[!DNL RTCDP] (모든 SKU) 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!UICONTROL at.js]</li></ul><li>동일한 페이지 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (모든 SKU), [!DNL AAM], 및 [!DNL Target]</li></ul> | <ul><li>다음 세션 개인화</li><ul><li>을 사용하는 모든 페이지의 경우 [!UICONTROL at.js]</li><li>[!DNL AAM] 세그먼트</li><li>을 통해 타사 세그먼트 [!DNL AAM]</li></ul> |

### 세그먼트 평가 시간

다음 표는 다른 구현 시나리오에서 발생하는 이벤트에 대한 세그먼트 평가 시간을 보여줍니다.

| 시나리오 | 에지 세그먼트(밀리초 평가) | 스트리밍 세그먼트(분 평가) | 배치 세그먼트 평가 |
| --- | --- | --- | --- |
| 이벤트/데이터 원본 [!DNL Adobe Experience Platform] SDK | 예 | 예 | 해당 사항 없음 |
| 이벤트 출처 [!UICONTROL at.js] | 아니요 | 예 | 해당 사항 없음 |
| 이벤트 출처 [!DNL Target Mobile] SDK | 아니요 | 예 | 해당 사항 없음 |
| 일괄 업로드에서 이벤트 | 아니오 | 아니요 | 예 |
| 오프라인 데이터(스트림)의 이벤트 | 아니요 | 예 | 예 |

### 추가 정보 링크

자세한 내용은 다음 주제를 참조하십시오.

* [대상 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} 에서 *Adobe Experience Platform 릴리스 노트*
* [동일 페이지 및 다음 페이지 개인화를 위한 개인화 대상 구성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} 에서 *대상 개요* 안내서.
* [사용자 지정 개인화 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} 에서 *대상 개요* 안내서
* [Adobe Target 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} 에서 *대상 개요* 안내서
* [동일한 페이지 및 다음 페이지 개인화 사용 사례에 대한 개인화 대상 구성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} 에서 *대상 개요* 안내서

## 와 실시간 CDP 프로필 속성 공유 [!DNL Target] {#rtcdp-profile-attributes}

실시간 CDP 프로필 속성을 [!DNL Target] HTML 오퍼 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### 실시간 CDP 프로필 속성 기능 제한 및 고려 사항

>[!NOTE]
>
>실시간 CDP 프로필 속성 기능은 HTML 오퍼 및 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md).

다음 사항을 고려하십시오.

* 주어진 오퍼 내의 속성은 동일한 Experience Platform 샌드박스에서 가져와야 합니다. (즉, 오퍼는 다른 Experience Platform 샌드박스의 속성을 포함할 수 없습니다.)
* 주어진 오퍼 내의 속성은 다른 소스에서 올 수 있습니다. 즉, [!DNL Target] 프로필 및 Experience Platform 프로필을 참조하십시오. (다시 말해, 속성이 파생되는지 여부를 결합할 수 있습니다 [!DNL Target] 또는 Experience Platform 프로필에서 가져올 수 있습니다.
* 오퍼를 정의할 때 속성에 명시적 값이 없는 경우 실시간 CDP 프로필 속성에 대한 기본값을 할당할 수 있습니다. 예를 들어, 동의 또는 거버넌스 정책이 개인화 서비스에서 사용되는 속성을 차단하는 경우 기본값을 대신 사용할 수 있습니다.
* 공유하면 실시간 CDP 프로필 속성이 의 인공 지능/시스템 학습 개인화 모델에서 사용됩니다 [!UICONTROL 자동 Target] 및 [!UICONTROL Automated Personalization] 활동.

### 샘플 사용 사례

온라인 마케터는 AEP/통합 프로필이 속성 값을 와 공유할 수 있도록 합니다 [!DNL Target] 을 입력하여 실시간 개인화를 제공할 수 있습니다. 실시간 CDP 프로필 속성을 사용하면 [!DNL Target] 토큰 대체를 사용하여 오퍼. 예를 들어 `${aep.profile.favoriteColor}`또는 토큰을 사용하여 충성도 계층 및 충성도 포인트 값을 생성합니다 `${aep.loyalty.tier}` 및 `${aep.loyalty.points}`.

AEP/Unified Profile 속성을 와 공유할 JSON 오퍼를 작성하려면 다음을 수행하십시오 [!DNL Target]:

1. While [json 오퍼 만들기](/help/main/c-experiences/c-manage-content/create-json-offer.md): **[!UICONTROL 소스 선택]** 목록, 선택 **[!UICONTROL Adobe Experience Platform]**.
1. 에서 **[!UICONTROL 프로필 샌드박스 이름 선택]** 목록에서 원하는 샌드박스를 선택합니다.
1. 에서 **[!UICONTROL 프로필 속성 선택]** 목록에서 원하는 속성을 선택합니다.
1. (선택 사항) **[!UICONTROL 기본값 삽입]** 목록에서 원하는 값을 선택합니다.
1. **[!UICONTROL 추가를 클릭합니다]**.

   다음 그림은 두 개의 프로필 속성을 보여줍니다. `loyalty.tier` 및 `loyalty.points` 을 JSON 오퍼에 추가했습니다.

   ![offer-json-aep-shared-attribute 이미지](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## 비디오 및 블로그 게시물

다음 비디오 및 블로그 게시물은 Target 및 RTCDP를 사용한 향상된 개인화에 대한 자세한 정보를 제공합니다.

### 비디오: 실시간 CDP와 [!DNL Adobe Target]{#RTCDP}

을 사용하여 다음 히트에 대해 개인화하는 방법을 알아봅니다. [!DNL Real-time Customer Data Platform] 및 [!DNL Adobe Target]. 다음 [!DNL Adobe Target] 대상 [!DNL Real-time CDP] 를 사용하면 [!DNL Experience Platform] 세그먼트 [!DNL Adobe Target] 거버넌스 및 개인 정보 지원을 통해 동일한 페이지 개인화 및 다음 페이지 개인화를 위해.

자세한 내용은 [실시간 CDP 및 Adobe Target을 사용한 다음 히트 개인화](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} 에서 *플랫폼 Tutorials* 안내서.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Adobe Target 블로그 및 비디오: 동일한 페이지 향상된 개인화

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] 및 [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
