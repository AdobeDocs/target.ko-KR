---
keywords: 구현;javascript 라이브러리;js;at-device decisioning;Device Decisioning;at.js;온장치;온장치;문제 해결;문제 해결
description: at.js 라이브러리를 사용하여 장치 내 의사 결정 문제를 해결하는 방법을 알아봅니다.
title: at.js JavaScript 라이브러리를 사용하여 On-Device Decisioning 문제를 어떻게 해결합니까?
feature: at.js
role: Developer
exl-id: 76bb9393-1560-455b-9d95-91576faee1f2
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# at.js에 대한 온디바이스 의사 결정 문제 해결

다음 단계를 완료하여 의 On-Device Decisioning 문제를 해결하십시오. [!DNL Adobe Target] at.js JavaScript 라이브러리 사용:

## 1단계: at.js에 대한 콘솔 로그 활성화

URL 매개 변수 추가 `mboxDebug=1` at.js에서 브라우저 콘솔에서 메시지를 인쇄할 수 있도록 합니다.

모든 메시지에는 편리한 개요를 위해 접두사 &quot;AT:&quot;가 포함되어 있습니다. 아티팩트가 성공적으로 로드되었는지 확인하려면 콘솔 로그에 다음과 유사한 메시지가 포함되어야 합니다.

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

다음 그림은 콘솔 로그에 이러한 메시지를 보여 줍니다.

![객체 메시지가 있는 콘솔 로그](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## 2단계: 브라우저의 네트워크 탭에서 규칙 객체 다운로드를 확인합니다

브라우저의 네트워크 탭을 엽니다.

예를 들어 Google Chrome에서 DevTools를 열려면 다음을 수행하십시오.

1. Ctrl+Shift+J(Windows) 또는 Command+Option+J(Mac)을 누릅니다.
1. 네트워크 탭으로 이동합니다.
1. 호출을 키워드 &quot;rules.json&quot;으로 필터링하여 객체 규칙 파일만 표시합니다.

   또한 &quot;/delivery|rules.json/&quot;로 필터링하여 모두 표시할 수 있습니다 [!DNL Target] 호출 및 artifact rules.json을 참조하십시오.

   ![Google Chrome의 네트워크 탭](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## 3단계: at.js 사용자 지정 이벤트를 사용하여 규칙 객체 다운로드 확인

at.js 라이브러리는 온장치 의사 결정을 지원하기 위해 두 개의 새로운 사용자 지정 이벤트를 전달합니다.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

구독하면 응용 프로그램에서 이러한 사용자 지정 이벤트를 수신하여 객체 규칙 파일 다운로드의 성공 또는 실패 시 작업을 수행할 수 있습니다.

다음 예는 객체 다운로드 성공 및 실패 이벤트를 수신하는 코드 샘플을 보여줍니다.

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
