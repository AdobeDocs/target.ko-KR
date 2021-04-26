---
keywords: 구현;javascript 라이브러리;js;장치 내 결정;장치 결정;at.js;온-장치;온-장치;문제 해결;문제 해결
description: at.js 라이브러리를 사용하여 장치 내 의사 결정 문제를 해결하는 방법을 알아봅니다.
title: at.js JavaScript 라이브러리에서 장치 내 의사 결정 문제를 해결하려면 어떻게 합니까?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: 85a17944c7d5924edb1bbabb7531274249ceaaa8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# at.js에 대한 장치 내 의사 결정 문제 해결

at.js JavaScript 라이브러리를 사용하여 [!DNL Adobe Target]의 장치 내 의사 결정 문제를 해결하려면 다음 단계를 완료하십시오.

## 1단계:at.js에 대한 콘솔 로그 활성화

URL 매개 변수 `mboxDebug=1`을 추가하면 at.js가 브라우저의 콘솔에서 메시지를 인쇄할 수 있습니다.

모든 메시지에는 편리한 개요를 위해 접두사 &quot;AT:&quot;가 포함되어 있습니다. 가공물이 성공적으로 로드되었는지 확인하려면 콘솔 로그에 다음과 유사한 메시지가 포함되어야 합니다.

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

다음 그림은 콘솔 로그에 이러한 메시지를 보여 줍니다.

![가공물 메시지가 있는 콘솔 로그](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## 2단계:브라우저의 [네트워크] 탭에서 규칙 아티팩트 다운로드 확인

브라우저의 네트워크 탭을 엽니다.

예를 들어 Google Chrome에서 개발 도구를 열려면 다음을 수행하십시오.

1. Ctrl+Shift+J(Windows) 또는 Command+Option+J(Mac)를 누릅니다.
1. 네트워크 탭으로 이동합니다.
1. &quot;rules.json&quot; 키워드로 호출을 필터링하여 아티팩트 규칙 파일만 표시되도록 합니다.

   또한 &quot;/delivery|rules.json/&quot;로 필터링하여 모든 [!DNL Target] 호출 및 artifact rules.json을 표시할 수 있습니다.

   ![Google Chrome의 네트워크 탭](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## 3단계:at.js 사용자 지정 이벤트를 사용하여 규칙 아티팩트 다운로드 확인

at.js 라이브러리는 2개의 새로운 사용자 지정 이벤트를 전달하여 장치 내 의사 결정을 지원합니다.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

구독하면 응용 프로그램에서 이러한 사용자 정의 이벤트를 수신하여 객체 규칙 파일 다운로드에 성공하거나 실패할 때 작업을 수행할 수 있습니다.

다음 예는 객체 다운로드 성공 및 실패 이벤트를 수신하는 코드 샘플을 보여 줍니다.

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
