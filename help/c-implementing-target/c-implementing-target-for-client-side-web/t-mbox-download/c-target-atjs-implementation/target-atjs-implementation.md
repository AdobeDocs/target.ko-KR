---
description: at.js 라이브러리는 일반적인 웹 구현과 단일 페이지 애플리케이션 둘 다에 맞게 디자인된 새로운 Adobe Target용 구현 라이브러리입니다.
keywords: Target Standard;at.js;구현
seo-description: at.js 라이브러리는 일반적인 웹 구현과 단일 페이지 애플리케이션 둘 다에 맞게 디자인된 새로운 Adobe Target용 구현 라이브러리입니다.
seo-title: mbox.js에서 at.js로 마이그레이션
solution: Target
title: mbox.js에서 at.js로 마이그레이션
topic: Standard
uuid: 10da01d7-d308-44e3-9c6e-ff4f713bd312
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mbox.js에서 at.js로 마이그레이션{#migrate-from-mbox-js-to-at-js}

at.js 라이브러리는 일반적인 웹 구현과 단일 페이지 애플리케이션 둘 다에 맞게 디자인된 새로운 [!DNL Adobe Target]용 구현 라이브러리입니다.

여러 가지 이점 중에서 [!DNL at.js]는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다.

[!DNL at.js]는 [!DNL Target]을 구현할 수 있도록 [!DNL mbox.js]를 대체합니다. [!DNL at.js] 라이브러리에는 [!DNL target.js]에 포함된 조각도 포함되어 있으므로 더 이상 [!DNL target.js] 호출이 없습니다.

>[!NOTE]
>
>FP-11577을 사용하는 Adobe Experience Manager(AEM) 6.2(또는 이상)에서는 Adobe Target 클라우드 서비스 통합을 통해 at.js 구현을 지원합니다. 자세한 내용은 *Adobe Experience Manager 6.2* 설명서에서 [기능 팩](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) 및 [Adobe Target과 통합](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html)을 참조하십시오.

[!DNL at.js]를 사용하려면 구현하려는 페이지에서 [!DNL mbox.js] 참조를 바꾸십시오. 하나의 페이지에서 [!DNL mbox.js]와 [!DNL at.js]를 함께 사용할 수 없습니다. 그러나 사이트의 각 페이지에서 어느 하나를 사용할 수는 있습니다.

[!DNL at.js] 라이브러리는 `mboxCreate()`, `mboxDefine()` 및 `mboxUpdate()` 함수를 사용하여 기존 구현에 대해 작동하며, 단일 페이지 앱 기반 구현에 초점을 맞춘 새로운 기능을 지원합니다.

현재 [!DNL mbox.js]를 사용하는 곳이라면 어디든 [!DNL at.js]를 사용할 수 있습니다.

[!DNL at.js] 라이브러리는 [!DNL mbox.js] 라이브러리와 비교하여 다음을 포함한 몇 가지 개선 사항을 제공합니다.

* 교차 도메인 AJAX를 통해 완전히 비동기적인 통신

   >[!IMPORTANT]
   >
   >[!DNL at.js]가 [!DNL Target] 서버와 비동기적으로 통신하긴 하지만 [!DNL at.js] 파일 자체는 페이지의 `<head>` 섹션에서 동기적으로 로드되어야 합니다. 이상적으로는 로드된 첫 번째 스크립트 중 하나여야 합니다. [!DNL at.js]는 로드된 후에는`XMLHttpRequest`를 통해 mbox 호출을 비동기적으로 실행하고 페이지 렌더링을 차단하지 않습니다.

* 더 이상 차단 호출이 없음
* `document.write()`이 사용되지 않음
* [!DNL Target] 응답에서 즉각적인 JavaScript 실행이 없음
* 더 나은 시간 제한 및 오류 처리

   * 사용자 지정 가능한 호출당 [시간 제한](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)
   * 시간 초과 시 다시 로드되지 않음

* 단일 페이지 앱/MVC 프레임워크용으로 특별히 디자인된 함수

## 교육 비디오: at.js - 이점 및 구현 우수 사례

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](../../../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* at.js 라이브러리 작동 방식
* mbox.js에 비해 at.js의 장점
* at.js에서 플리커를 관리하는 방법
* at.js의 오류 처리
* 디버깅 방법론
* 알려진 문제 및 향후 로드맵

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
