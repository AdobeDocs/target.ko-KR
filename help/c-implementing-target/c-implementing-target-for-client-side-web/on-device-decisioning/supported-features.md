---
keywords: 구현;javascript 라이브러리;js;atjs;장치 의사 결정;장치 의사 결정;지원되는 기능
description: 장치 내 의사 결정을 위해 지원되는 기능에 대해 알아봅니다.
title: 장치 내 의사 결정에서 지원되는 기능
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
translation-type: tm+mt
source-git-commit: 62a3b387445977a1bdcd2cf45306c8ff032fca50
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 11%

---

# 장치 내 의사 결정을 위한 지원 기능

[!DNL Adobe Target] JS SDK는 고객이 결정을 위한 데이터의 최신 성능과 성능 중에서 선택할 수 있는 유연성을 제공합니다. 즉, 머신 러닝을 통해 관련성이 높고 매력적인 개인화된 콘텐츠를 전달하는 것이 가장 중요한 경우 라이브 서버를 호출해야 합니다. 그러나 성능이 더 중요한 경우 디바이스와 메모리 내 의사 결정을 내려야 합니다. 장치 내 의사 결정 기능이 작동하려면 지원되는 기능을 나열하는 다음 섹션을 참조하십시오.

## 지원되는 활동 유형

다음 표는 [양식 기반 Experience Composer](/help/c-experiences/form-experience-composer.md) 또는 [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC)가 장치 내 의사 결정에 대해 지원되거나 지원되지 않는 활동 유형을 나타냅니다.](/help/c-activities/target-activities-guide.md)[

| 활동 유형 | 지원됨? |
| --- | --- |
| [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) | 예 |
| [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니오 |
| [자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/assets/premium.png) | 아니오 |
| [](/help/c-activities/c-multivariate-testing/multivariate-testing.md)다변량 테스트(MVT) | 아니오 |
| [](/help/c-activities/t-experience-target/experience-target.md)경험 타깃팅(XT) | 예 |
| [자동화된 ](/help/c-activities/t-automated-personalization/automated-personalization.md) ![PersonalizationPremium](/help/assets/premium.png) | 아니오 |
| [RecommendationsPremium ](/help/c-recommendations/recommendations.md) ![](/help/assets/premium.png) | 아니오 |
| [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T)을 사용한 활동 | 예 |

## 고객 타깃팅

다음 표는 장치에서 의사 결정을 위해 지원되거나 지원되지 않는 대상 규칙을 나타냅니다.

| 대상 규칙 | 지원됨? |
| --- | --- |
| [지역](/help/c-target/c-audiences/c-target-rules/geo.md) | 예 |
| [네트워크](/help/c-target/c-audiences/c-target-rules/network.md) | 아니오 |
| [모바일](/help/c-target/c-audiences/c-target-rules/mobile.md) | 아니오 |
| [사용자 지정 매개 변수](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) | 예 |
| [운영 체제](/help/c-target/c-audiences/c-target-rules/operating-system.md) | 예 |
| [사이트 페이지](/help/c-target/c-audiences/c-target-rules/site-pages.md) | 예 |
| [브라우저](/help/c-target/c-audiences/c-target-rules/browser.md) | 예 |
| [방문자 프로필](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) | 아니오 |
| [트래픽 소스](/help/c-target/c-audiences/c-target-rules/traffic-sources.md) | 아니오 |
| [시간대](/help/c-target/c-audiences/c-target-rules/time-frame.md) | 예 |
| Adobe Experience Cloud 대상<br>([!DNL Adobe Analytics], [!DNL Adobe Audience Manager] 및 [!DNL Adobe Experience Manager]의 대상) | 아니오 |

### 장치 내 의사 결정을 위한 지역 타깃팅

지역 기반 대상의 장치 내 의사 결정 활동에 대한 최소 지연을 유지하려면 [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) 호출에 지리적 값을 직접 제공할 것을 Adobe이 권장합니다. 요청의 컨텍스트에서 지역 개체를 설정합니다. 이것은 브라우저에서 각 방문자의 위치를 확인하는 방법을 의미합니다. 예를 들어 구성한 서비스를 사용하여 IP-지역 조회를 수행할 수 있습니다. Google Cloud와 같은 일부 호스팅 제공업체는 각 `HttpServletRequest`에 있는 사용자 정의 헤더를 통해 이 기능을 제공합니다.

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

그러나 서버에서 IP-to-Geo 조회를 수행할 수 없지만 여전히 지리 기반 대상이 포함된 [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) 요청에 대해 장치 내 의사 결정을 수행하려는 경우 이 또한 지원됩니다. 이 접근 방식의 단점은 각 `getOffers` 호출에 지연을 추가하는 원격 IP-지역 조회를 사용한다는 것입니다. 이 지연은 서버 쪽 의사 결정이 있는 `getOffers` 호출보다 작아야 합니다. 이 지연은 서버 가까이에 있는 CDN을 히트하기 때문입니다. 방문자의 IP 주소의 지역 위치를 검색하기 위해 SDK에 대한 요청 컨텍스트의 지역 개체에 &quot;ipAddress&quot; 필드만 제공합니다. &quot;ipAddress&quot; 외에 다른 필드가 제공되는 경우, [!DNL Target] SDK는 해결을 위해 지리적 위치 메타데이터를 가져오지 않습니다.

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

다음 표는 장치 내 의사 결정에 대해 지원되거나 지원되지 않는 할당 방법을 나타냅니다.

| 할당 방법 | 지원됨? |
| --- | --- |
| 수동 | 예 |
| [최적의 경험에 자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 아니오 |
| [개인화된 경험을 위한 자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md) | 아니오 |
