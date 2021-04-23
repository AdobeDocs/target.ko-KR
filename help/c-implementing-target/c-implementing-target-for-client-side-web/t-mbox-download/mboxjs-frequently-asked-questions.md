---
keywords: mbox.js faq;mbox.js 자주 묻는 질문;document.write;tt.omtrdc.net;파서 차단
description: Adobe Target의 기존 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 버전의 at.js로 마이그레이션합니다.
title: ' [!DNL Target] mbox.js에 대한 일부 FAQ는 무엇입니까?'
feature: at.js
role: Developer
exl-id: 0e207896-d45b-45f9-8556-6532fda72a45
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 71%

---

# mbox.js FAQ

mbox.js에 대해 자주 묻는 질문과 대답(FAQ)입니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리를 더 이상  [!DNL Adobe Target] 지원하지 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

## 페이지 로드 시 mbox.js의 영향은 어떤 것입니까? {#section_90B3B94FE0BF4B369577FCB97B67F089}

자세한 내용은 [at.js의 이점](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits)을 참조하십시오.

## mbox.js 및 document.write를 사용할 때 Google Chrome에서 &quot;Parser-blocking&quot;(파서 차단)이라는 경고 메시지가 표시되는 이유는 무엇입니까? {#section_355A3A5BF02F42EEB8271C96EF41590A}

이 콘솔 메시지는 `document.write` 함수가 mbox.js 파일 내에서 사용되는 많은 상황에서 Chrome을 사용할 때 표시되는 이 경고 메시지는 활동 설정 프로세스에 영향을 주지 않습니다.

이 상황을 방지하는 가장 좋은 방법은 [Target 구현을 at.js JavaScript 라이브러리로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)하는 것으로서, 이 라이브러리에서는 `document.write` 함수를 사용하지 않습니다. at.js를 사용하면 mbox.js을 사용하는 것에 비해 많은 이점이 있습니다. 자세한 내용은 [at.js FAQ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769)를 참조하십시오.

## 웹 페이지에서 mbox가 실행되지 않는 이유는 무엇입니까? {#section_4BA5DA424B734324AAB51E4588FA50F5}

 고객들이 테스트나 간단한 개념 입증 용도로 [!DNL Target]Target에 클라우드 기반 인스턴스를 사용하는 경우가 있습니다. 이러한 도메인 및 기타 많은 다른 도메인이 [공용 접미사 목록](https://publicsuffix.org/list/public_suffix_list.dat)에 나와 있습니다.

최신 브라우저에서는 targetGlobalSettings()를 사용하여 `cookieDomain` 설정을 사용자 지정하지 않는 한, 이러한 도메인을 사용하는 경우 쿠키를 저장하지 않습니다. 자세한 내용은 [Target에 클라우드 기반 인스턴스 사용](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566)을 참조하십시오.

## [!DNL Target] 서버 호출이 이동하는 tt.omtrdc.net 도메인은 무엇입니까?{#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net]은 Target에 대한 모든 서버 호출을 받는 데 사용되는 Adobe 에지 네트워크의 도메인 이름입니다.

## at.js와 mbox.js가 HttpOnly 및 Secure 쿠키 플래그를 사용하지 않는 이유는 무엇입니까? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly는 서버 측 코드를 통해서만 설정할 수 있습니다. mbox와 같은 Target 쿠키가 생성되고 JavaScript 코드를 통해 저장되므로 Target에서 HttpOnly 쿠키 플래그를 사용할 수 없습니다.

HTTPS를 통해 페이지를 로드한 경우에만 JavaScript를 통해 보안을 설정할 수 있습니다. 페이지가 처음에 HTTP를 통해 로드된 경우에는 JavaScript에서 이 플래그를 설정할 수 없습니다. 또한 보안 플래그를 사용하는 경우 HTTPS 페이지에서만 쿠키를 사용할 수 있습니다.

Target이 제대로 사용자를 추적할 수 있는지 보장하기 위해 그리고 쿠키가 클라이언트 측에서 생성되므로 Target에서 이러한 플래그 중 하나를 사용하지 않습니다.
