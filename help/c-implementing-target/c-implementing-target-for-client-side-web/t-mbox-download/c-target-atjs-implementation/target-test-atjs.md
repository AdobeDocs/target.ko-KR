---
keywords: at.js;비-프로덕션;비-프로덕션;배포
description: Adobe Target의 기존 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 버전의 at.js로 마이그레이션합니다.
title: at.js를 비프로덕션 환경에 배포하려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 607b2b5b-bb2a-4443-abc0-452b421fc009
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 80%

---

# at.js를 비프로덕션 환경에 배포

at.js를 비프로덕션 환경에 안전하게 배포하는 기법에 대한 정보.

## &quot;Requestly&quot; Chrome 확장을 사용하여 다른 파일에 매핑

>[!NOTE]
>
>다음 정보 외에 Google Chrome용 [Adobe Target VEC Helper 브라우저 확장 프로그램](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 사용할 수 있습니다.

[Requestly](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en)는 대체 URL로 요청을 리디렉션할 수 있는 무료 Chrome 확장입니다.

at.js를 URL에 배포한 다음, Requestly를 사용하여 현재 mbox.js 파일 URL을 새 at.js URL에 매핑합니다. 그런 다음 웹 사이트에서 mbox.js를 로드하려고 하면 at.js를 대신 로드합니다. 이 방법을 사용하면 Adobe에서 지원을 보다 쉽게 제공할 수 있습니다.

## 개발, 스테이징 또는 QA 환경에 배포

코드 베이스에 mbox.js를 호스팅하고 코드 환경을 쉽게 업데이트할 수 있는 경우, at.js를 하위 환경 중 하나에 배포하십시오.

Adobe에서 더 나은 지원을 받으려면 Adobe가 액세스할 수 있는 환경에 파일을 배포하십시오.

## Charles 또는 Fiddler를 사용하여 로컬 파일 매핑

[Charles Web Debugging Proxy](https://www.charlesproxy.com/)는 프로덕션 mbox.js 파일을 at.js의 로컬 사본에 매핑하기 위해 해당 로컬 매핑 기능을 사용할 수 있는 Mac 및 Windows용 애플리케이션입니다. Mac 및 Windows용 무료 평가판 버전을 다운로드할 수 있습니다.

[Fiddler](https://www.telerik.com/fiddler)는 무료로 다운로드할 수 있는 유사한 Windows용 도구입니다.

## 다른 태그 관리자 환경에 배포

다른 태그 관리자를 사용하는 경우, 프로덕션 트래픽에 영향을 주지 않고 at.js를 안전하게 배포할 수 있습니다.
