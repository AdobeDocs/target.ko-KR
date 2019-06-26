---
description: Adobe Target 애플리케이션 및 컨텐츠 전달은 다양한 브라우저 및 장치에서 테스트되었습니다.
keywords: 브라우저;사전 요구 사항;요구 사항;internet explorer;chrome;firefox;safari;android;surface
seo-description: Adobe Target 애플리케이션 및 컨텐츠 전달은 다양한 브라우저 및 장치에서 테스트되었습니다.
seo-title: 지원되는 브라우저
solution: Target
subtopic: 시작하기
title: 지원되는 브라우저
topic: Standard
uuid: 614088da-412c-45e3-9f2d-6985391973be
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 지원되는 브라우저{#supported-browsers}

[!DNL Adobe Target] 애플리케이션 및 컨텐츠 전달은 광범위한 브라우저 및 장치에서 테스트되었습니다.

TLS에 대한 추가적으로 중요한 정보는 [TLS(전송 계층 보안) 암호화 변경](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)을 참조하십시오.

## [!DNL Target] Standard/Premium 인터페이스 {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

[!DNL [!DNL Target]] Standard/Premium] 인터페이스는 다음 브라우저 및 장치를 지원합니다.

| 장치 유형 | 브라우저 버전 |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome(최신, 최신 버전-1)</li><li>Mozilla Firefox(최신, 최신 버전-1)</li></ul> |
| Mac | <ul><li>Firefox(최신, 최신 버전-1)</li><li>Chrome(최신, 최신 버전-1)</li></ul> |

## Content delivery {#section_1045A946056441268D40025529918D3D}

컨텐츠 전달은 다음 브라우저 및 장치에서 테스트되었습니다.

| 장치 유형 | 브라우저 버전 |
|--- |--- |
| Windows | <ul><li>Internet Explorer 9 및 10. 에뮬레이션 모드에서 테스트되었습니다.<br>**참고**: at.js 1.3.0 이상 버전은 더 이상 Microsoft Internet Explorer 9에서 컨텐츠 전달을 지원하지 않습니다.</li><li>Internet Explorer 11</li><li>Microsoft Edge</li><li>Chrome(최신, 최신 버전-1)</li><li>Firefox(최신, 최신 버전-1)</li></ul> |
| Mac | <ul><li>Apple Safari(최신)<br>**참고**: Safari가 퍼스트 파티 및 타사 쿠키를 처리하는 방법에 대한 자세한 내용은 [Target 쿠키](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md)를 참조하십시오.</li><li>Firefox(최신, 최신 버전-1)</li><li>Chrome(최신, 최신 버전-1)</li></ul> |
| 모바일/태블릿 | <ul><li>Apple iOS(최신)</li><li>Android 장치 및 태블릿(Android 4 이상)</li><li>Microsoft Surface(Windows 8.1)</li></ul> |

[!DNL at.js] 구현의 경우, [!DNL Target]은 Internet Explorer 이전 버전 및 위에 나열된 브라우저의 이전 버전에서 기본 컨텐츠를 표시합니다. [!DNL mbox.js] 구현의 경우 [!DNL Target]은 컨텐츠를 렌더링하려고 시도하지만 성공하지 못할 수 있습니다.

[!DNL Target] [퀴즈] 모드를 사용하는 [브라우저나 위에 나열되지 않은 브라우저의 기본 컨텐트를 표시합니다](https://en.wikipedia.org/wiki/Quirks_mode). at.js에는 표준 모드에서 렌더링되는 문서 형식(예: `<!DOCTYPE html>`)이 필요합니다.

>[!NOTE]
>
>Adobe Delivery 인프라는 2018년 9월 12일 이후에 TLS 1.0 장치 및 브라우저를 지원하지 않도록 보호됩니다. 이러한 변경의 전반적 영향에 대해 이해하려면 [TLS(전송 계층 보안) 암호화 변경 사항](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)을 참조하십시오.
