---
keywords: 서버 측;서버 측;sdk;sdk;on-device;의사 결정;장치;온장치;온장치;0개 지연;지연 시간;near-zero;node.js
description: On-Device Decisioning을 사용하여 [!DNL Target] A/B 및 MVT 활동을 서버에 캐시하여 0에 가까운 지연에서 메모리 내 의사 결정을 수행하는 방법을 알아봅니다.
title: On-Device Decisioning 소개
feature: 서버측 구현
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: fe70f357e2298f1656d713aae5fae800e6775d64
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 9%

---

# 온디바이스 의사 결정

On-Device Decisioning에서는 [!DNL Adobe Target] [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting] (XT) 활동을 서버에 캐시하고 [!DNL Adobe Target] Edge 네트워크에 대한 네트워크 요청을 차단하지 않고 거의 0에 가까운 지연에서 메모리 내 의사 결정을 수행하는 기능을 제공합니다.

자세한 내용은 *[Adobe Target SDK 설명서](https://adobetarget-sdks.gitbook.io/docs/)*&#x200B;에서 [Introduction to on-device decisioning](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) 을 참조하십시오.

## 웨비나: 지연 없이 [!DNL Adobe Target]의 장치 내 결정을 사용하여 개인화 및 테스트

그 어느 때보다 마케터, 제품 소유자 및 개발자들은 사이트, 앱, 그리고 고객과 연결되는 모든 곳에서 전체적인 고객 경험을 최적화해야 하는 과제를 안고 있습니다. 데이터 사일로와 복잡한 구현이 포함된 여러 도구가 불충분합니다.

이 녹음된 웨비나에서는 [!DNL Adobe Target] 제품 전문가가 0에 가까운 지연 시간을 사용하여 로컬로 실행되도록 장치에서 중요한 경험 최적화 결정을 이동하는 것이 고객의 사이트 성능을 향상시키면서 새로운 사용 사례를 여는 방법에 대해 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## 우수 사례

Adobe은 On-Device Decisioning을 사용할 때 다음과 같은 우수 사례를 권장합니다.

### 의사 결정 방법이 &quot;온장치&quot;일 때 모범 사례 {#best-practices-on-device}

&quot;온장치&quot;를 의사 결정 방법으로 사용하는 경우 방문자가 처음으로 웹 페이지를 로드할 때 아티팩트가 다운로드됩니다. 첫 번째 페이지 로드(캐시 없음)에서 수행해야 하는 모든 활동 조건은 아티팩트가 완전히 다운로드된 후에만 발생합니다. 익명의 새 방문자에 대해 활동 자격이 신속히 수행되도록 하기 위해 따라야 할 특정 모범 사례가 있습니다.

* 아티팩트에 포함되지 않도록 &quot;On-Device&quot; 지원 활동을 비활성화합니다.
* [!DNL Target Premium]이 있는 경우 [속성/작업 공간](/help/administrating-target/c-user-management/property-channel/property-channel.md)을 사용하여 다른 작업 공간에 대해 다른 객체 파일을 생성할 수 있습니다.
* 적합한 이유로 아티팩트 파일이 매우 큰 경우 &quot;hybrid&quot; 의사 결정 방법을 사용할 수 있습니다. 이 방법을 사용하면 아티팩트를 동시에 다운로드할 수 있으며 아티팩트가 다운로드될 때까지 모든 [!DNL Target] API 호출은 와이어에서 실행됩니다. 이 방법에 대한 자세한 내용은 아래의 &quot;Hybrid&quot; 의사 결정 모드](#best-practices-hybrid)에 대한 우수 사례 섹션을 참조하십시오.[
* SPA(단일 페이지 애플리케이션)이 있는 경우 첫 번째 페이지 로드 중에 애플리케이션의 기본 JavaScript 파일을 로드하기 전에 at.js를 로드하고 초기화하는 것이 좋습니다. [!DNL Adobe] 이러한 접근 방식은 훨씬 일찍 객체 다운로드를 시작하므로 더욱 빠른 경험 렌더링 을 제공합니다.

### 의사 결정 방법이 &quot;hybrid&quot;일 때 모범 사례 {#best-practices-hybrid}

의사 결정 방법으로 &quot;hybrid&quot;를 사용하는 경우 아티팩트가 동시에 다운로드됩니다. 아티팩트가 다운로드될 때까지 &quot;위치&quot;가 온장치에서만 사용 가능한 경우에도 모든 [!DNL Target] API 호출이 와이어로 전달됩니다. 이 동작은 모든 `getOffers()` 호출에 대한 기본값이며 대부분의 상황에서 최상의 성능을 제공합니다. `decisioningMethod` 을 `on-device`(으)로 설정하여 `getOffers()`의 기본 동작을 변경하는 경우, 이 우수 사례를 사용하여 오류를 방지하고 최상의 성능을 확보하십시오.

* 페이지가 처음 로드될 때 `decisioningMethod` 를 `on-device`로 사용하여 `getOffers()`을 호출하기로 결정한 경우, 오류를 방지하려면 &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot; at.js 이벤트 처리기 내에서 호출해야 합니다. 아티팩트가 매우 큰 경우 이 방법을 사용하는 모든 &quot;위치&quot;는 아티팩트가 완전히 다운로드된 후에만 렌더링되므로 경험 렌더링이 지연될 수 있습니다. [!DNL Adobe] 에서는 이 접근 방식을 거의 사용하지 않는 것이 좋습니다. 이 방법을 사용할 때 위의 [&quot;On Device&quot; 우수 사례 섹션](#best-practices-on-device)에서 아티팩트 크기를 줄이는 우수 사례를 따릅니다.

## 자습서: On-Device Decisioning

[!DNL Adobe Target] On-Device Decisioning을 사용하면 지연 시간이 거의 없습니다.

이 7분 비디오:

* [!DNL Target] 구현의 다른 메서드와 비교하는 방법을 포함하여 장치 내 의사 결정에 대해 설명합니다
* [!DNL Target]에서 장치 내 의사 결정을 활성화하는 방법을 보여 줍니다.
* JSON 콘텐츠로 구성된 샘플 양식 기반 작성기 활동을 검사합니다
* On-Device Decisioning에 필요한 키 구성이 포함된 샘플 Node.JS SDK 코드를 표시합니다
* 브라우저에서 결과 표시

>[!VIDEO](https://video.tv.adobe.com/v/329032)

추가 비디오 및 자습서는 [Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=ko-KR) 안내서를 참조하십시오.

## Adobe 기술 블로그 - 1부: 에지 플랫폼에서 실험 및 개인화를 위해 [!DNL Adobe Target] NodeJS SDK를 실행합니다(Akamai Edge Workers)

[블로그 게시물에 액세스하려면 여기를 클릭하십시오](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9).

## Adobe 기술 블로그 - 파트2: Edge 플랫폼(AWS Lambda@Edge)에서 실험과 개인화에 대해 [!DNL Adobe Target] NodeJS SDK 실행하기

[블로그 게시물에 액세스하려면 여기를 클릭하십시오](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563).