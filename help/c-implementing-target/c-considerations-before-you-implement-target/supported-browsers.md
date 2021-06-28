---
keywords: 브라우저;사전 요구 사항;요구 사항;internet explorer;chrome;firefox;safari;android;surface
description: 인터페이스 및 콘텐츠 전달을 위해 지원하는 인터넷 브라우저 Adobe [!DNL Target] 을 알아봅니다.
title: ' [!DNL Target] 어떤 브라우저를 지원합니까?'
feature: 구현
role: Developer
exl-id: 8a366c79-d944-4d44-be5a-7c4f65385beb
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 43%

---

# 지원되는 브라우저

[!DNL Adobe Target] 애플리케이션 및 콘텐츠 전달은 광범위한 브라우저 및 장치에서 테스트되었습니다.

TLS에 대한 자세한 내용은 [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)을 참조하십시오.

## [!DNL Target] Standard/Premium 인터페이스 {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

[!DNL Target] 인터페이스는 다음 브라우저 및 장치를 지원합니다.

| 장치 유형 | 브라우저 버전 |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome(최신, 빼기 1)</li><li>Mozilla Firefox(최신, 마이너스 1)</li></ul> |
| Mac | <ul><li>Firefox(최신, 최신 - 1)</li><li>Chrome(최신, 빼기 1)</li></ul> |

## 콘텐츠 전달 {#section_1045A946056441268D40025529918D3D}

콘텐츠 전달은 다음 브라우저 및 장치에서 테스트되었습니다.

| 장치 유형 | 브라우저 버전 |
|--- |--- |
| Windows | <ul><li>Microsoft Internet Explorer 9 및 10. 에뮬레이션 모드에서 테스트되었습니다.<br>**참고**:IE 9의 콘텐츠 전달은 더 이상 at.js 1.3.0(이상)에서 지원되지 않습니다. IE 10, 11 및 모든 이전 버전의 컨텐츠 전달은 더 이상 at.js 2.5.0 이상 버전에서 지원되지 않습니다.</li><li>Internet Explorer 11 <br>**참고**:IE 10, 11 및 모든 이전 버전의 컨텐츠 전달은 더 이상 at.js 2.5.0 이상 버전에서 지원되지 않습니다.</li><li>Microsoft Edge</li><li>Chrome(최신, 빼기 1)</li><li>Firefox(최신, 최신 - 1)</li></ul> |
| Mac | <ul><li>Apple Safari(최신)<br>**참고**:Safari가 퍼스트 파티 및 타사 쿠키를 처리하는 방법에 대한 자세한 내용은 [쿠키 Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md)를 참조하십시오.</li><li>Firefox(최신, 최신 - 1)</li><li>Chrome(최신, 빼기 1)</li></ul> |
| 모바일/태블릿 | <ul><li>Apple iOS(최신)</li><li>Android 장치 및 태블릿(Android 4 이상)</li><li>Microsoft Surface(Windows 8.1)</li></ul> |

다음을 참조하십시오.

* [!DNL at.js] 구현의 경우, [!DNL Target]은 Internet Explorer 이전 버전 및 위에 나열된 브라우저의 이전 버전에서 기본 콘텐츠를 표시합니다. 
* Internet Explorer는 알 수 없는 모든 요소(예: 사용자 지정 요소)를 동일한 요소 유형으로 처리합니다. 따라서 게재는 사용자 지정 요소에서 작동하지 않습니다.
* [!DNL Target] 위 목록에 없는 브라우저와 quirks 모드를 사용하는 브라우저에는 기본  [콘텐츠가 표시됩니다](https://en.wikipedia.org/wiki/Quirks_mode). at.js에는 표준 모드에서 렌더링되는 문서 형식(예: `<!DOCTYPE html>`)이 필요합니다.
* Adobe Delivery 인프라는 2018년 9월 12일 이후에 TLS 1.0 장치 및 브라우저를 지원하지 않도록 보호됩니다. 이러한 변경의 전반적 영향에 대해 이해하려면 [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)을 참조하십시오.
