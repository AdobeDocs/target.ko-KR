---
keywords: 구현;javascript 라이브러리;js;atjs;on-device decisioning;device decisioning;지원되는 기능
description: On-Device Decisioning에 대해 지원되는 기능을 알아봅니다.
title: On-Device Decisioning에서 지원되는 기능
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 13%

---

# 온디바이스 의사 결정에 대한 지원 기능

다음 [!DNL Adobe Target] JS SDK는 고객이 결정을 내릴 때 데이터의 성능과 새로 고침 중 선택할 수 있는 유연성을 제공합니다. 즉, 기계 학습을 통해 가장 연관성이 높고 매력적인 개인화된 컨텐츠를 전달하는 것이 가장 중요한 경우 라이브 서버 호출을 수행해야 합니다. 그러나 성능이 더 중요한 경우, 온디바이스 및 인메모리 결정을 내려야 합니다. 장치 내 의사 결정이 작동하려면 지원되는 기능을 나열하는 다음 섹션을 참조하십시오.

## 지원되는 활동 유형

다음 표는 [활동 유형](/help/main/c-activities/target-activities-guide.md) 만든 사람 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 또는 [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC)가 지원 또는 On-Device Decisioning에서 지원되지 않습니다.

| 활동 유형 | 지원됨? |
| --- | --- |
| [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) | 예 |
| [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니오 |
| [자동 타깃팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md) ![프리미엄](/help/main/assets/premium.png) | 아니요 |
| [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | 아니요 |
| [경험 타기팅](/help/main/c-activities/t-experience-target/experience-target.md) (XT) | 예 |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) ![Premium](/help/main/assets/premium.png) | 아니오 |
| [권장 사항](/help/main/c-recommendations/recommendations.md) ![프리미엄](/help/main/assets/premium.png) | 아니요 |
| [Target에 Analytics를 사용하는 활동](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | 예 |

## 대상 타겟팅

다음 표는 On-Device Decisioning에서 지원되거나 지원되지 않는 대상 규칙을 나타냅니다.

| 대상 규칙 | 지원됨? |
| --- | --- |
| [지역](/help/main/c-target/c-audiences/c-target-rules/geo.md) | 예 |
| [네트워크](/help/main/c-target/c-audiences/c-target-rules/network.md) | 아니요 |
| [모바일](/help/main/c-target/c-audiences/c-target-rules/mobile.md) | 아니요 |
| [사용자 지정 매개 변수](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md) | 예 |
| [운영 체제](/help/main/c-target/c-audiences/c-target-rules/operating-system.md) | 예 |
| [사이트 페이지](/help/main/c-target/c-audiences/c-target-rules/site-pages.md) | 예 |
| [브라우저](/help/main/c-target/c-audiences/c-target-rules/browser.md) | 예 |
| [방문자 프로필](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) | 아니요 |
| [트래픽 소스](/help/main/c-target/c-audiences/c-target-rules/traffic-sources.md) | 아니요 |
| [시간대](/help/main/c-target/c-audiences/c-target-rules/time-frame.md) | 예 |
| Adobe Experience Cloud 대상<br>(대상: [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], 및 [!DNL Adobe Experience Manager] | 아니요 |

### 장치 내 의사 결정을 위한 지역 타깃팅

지역 기반 대상과 함께 장치 내 의사 결정 활동에 대한 최소 지연을 유지하려면 호출에 직접 지역 값을 제공하는 것이 좋습니다 [getOffers](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/). 요청 컨텍스트에서 지역 개체를 설정합니다. 이것은 브라우저에서 각 방문자의 위치를 확인하는 방법을 의미합니다. 예를 들어 사용자가 구성하는 서비스를 사용하여 IP-to-Geo 조회를 수행할 수 있습니다. Google Cloud와 같은 일부 호스팅 제공업체는 각 웹 사이트에서 사용자 지정 헤더를 통해 이 기능을 제공합니다 `HttpServletRequest`.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				city: "SAN FRANCISCO", 
				countryCode: "US", 
				stateCode: "CA", 
				latitude: 37.75, 
				longitude: -122.4 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

그러나 서버에서 IP-to-Geo 조회를 수행할 수 없지만, [getOffers](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/) 지역 기반 대상을 포함하는 요청이며, 이 요청도 지원됩니다. 이 방법은 원격 IP-to-Geo 조회를 사용하여 각 사이트에 지연을 추가하는 단점이 있습니다 `getOffers` 호출. 지연 시간은 `getOffers` 서버 측 의사 결정을 사용하여 호출합니다. 서버 근처에 있는 CDN에 도달하기 때문입니다. SDK에 대한 요청 컨텍스트의 지역 개체에 있는 &quot;ipAddress&quot; 필드만 방문자 IP 주소의 지역 위치를 검색합니다. ipAddress 외에 다른 필드가 제공되면 [!DNL Target] SDK는 해결을 위해 지리적 위치 메타데이터를 가져오지 않습니다.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				ipAddress: "127.0.0.1" 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

### 할당 방법

다음 표는 On-Device Decisioning에서 지원되거나 지원되지 않는 할당 방법을 나타냅니다.

| 할당 방법 | 지원됨? |
| --- | --- |
| 수동 | 예 |
| [최고 경험에 자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니요 |
| [개인화된 경험에 대한 자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 아니요 |
