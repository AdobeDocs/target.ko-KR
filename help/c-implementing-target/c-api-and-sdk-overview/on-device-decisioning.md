---
keywords: 서버 측;서버 측;sdk;sdk;on-device;의사 결정;장치;온장치;온장치;0개 지연;지연 시간;near-zero;node.js
description: On-Device Decisioning을 사용하여 [!DNL Target] A/B 및 MVT 활동을 서버에 캐시하여 0에 가까운 지연에서 메모리 내 의사 결정을 수행하는 방법을 알아봅니다.
title: On-Device Decisioning 소개
feature: 서버측 구현
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: ed4e6715c120fe692c7f3f84f6b869b5ad9bd1b7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 20%

---

# 온디바이스 의사 결정

On-Device Decisioning에서는 [!DNL Adobe Target] [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting] (XT) 활동을 서버에 캐시하고 [!DNL Adobe Target] Edge 네트워크에 대한 네트워크 요청을 차단하지 않고 거의 0에 가까운 지연에서 메모리 내 의사 결정을 수행하는 기능을 제공합니다.

자세한 내용은 *[Adobe Target SDK 설명서](https://adobetarget-sdks.gitbook.io/docs/)*&#x200B;에서 [Introduction to on-device decisioning](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) 을 참조하십시오.

## 웨비나: Adobe Target의 디바이스에서 의사 결정을 통해 대기 시간 없이 개인화 및 테스트

그 어느 때보다 마케터, 제품 소유자 및 개발자들은 사이트, 앱, 그리고 고객과 연결되는 모든 곳에서 전체적인 고객 경험을 최적화해야 하는 과제를 안고 있습니다. 데이터 사일로와 복잡한 구현이 포함된 여러 툴을 사용해도 이런 과제가 줄어들지 않습니다.

이 녹음된 웨비나에서는 [!DNL Adobe Target] 제품 전문가가 0에 가까운 지연 시간을 사용하여 로컬로 실행되도록 장치에서 중요한 경험 최적화 결정을 이동하는 것이 고객의 사이트 성능을 향상시키면서 새로운 사용 사례를 여는 방법에 대해 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## 자습서:On-Device Decisioning

[!DNL Adobe Target] On-Device Decisioning을 사용하면 지연 시간이 거의 없습니다.

이 7분 비디오:

* [!DNL Target] 구현의 다른 메서드와 비교하는 방법을 포함하여 장치 내 의사 결정에 대해 설명합니다
* [!DNL Target]에서 장치 내 의사 결정을 활성화하는 방법을 보여 줍니다.
* JSON 콘텐츠로 구성된 샘플 양식 기반 작성기 활동을 검사합니다
* On-Device Decisioning에 필요한 키 구성이 포함된 샘플 Node.JS SDK 코드를 표시합니다
* 브라우저에서 결과 표시

>[!VIDEO](https://video.tv.adobe.com/v/329032)

추가 비디오 및 자습서는 [Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=ko-KR) 안내서를 참조하십시오.

## Adobe 기술 블로그 - 1부:에지 플랫폼에서 실험 및 개인화를 위해 [!DNL Adobe Target] NodeJS SDK를 실행합니다(Akamai Edge Workers)

[블로그 게시물에 액세스하려면 여기를 클릭하십시오](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9).

## Adobe 기술 블로그 - 2부:에지 플랫폼에서 실험 및 개인화를 위해 [!DNL Adobe Target] NodeJS SDK를 실행합니다(AWS Lambda@Edge)

[블로그 게시물에 액세스하려면 여기를 클릭하십시오](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563).