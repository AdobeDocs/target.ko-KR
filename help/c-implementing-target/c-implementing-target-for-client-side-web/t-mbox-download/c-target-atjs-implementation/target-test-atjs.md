---
description: at.js를 비프로덕션 환경에 안전하게 배포하는 방법에 대한 정보입니다.
title: 비프로덕션 환경에 at.js 배포
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 92%

---


# Deploy at.js to a non-production environment{#deploy-at-js-to-a-non-production-environment}

at.js를 비프로덕션 환경에 안전하게 배포하는 기법에 대한 정보.

## DTM 스테이징에 배포

DTM을 사용하는 경우 Adobe Target 도구 구성에 at.js를 쉽게 저장할 수 있습니다.

라이브러리를 저장한 후 DTM 전환 도구를 사용하여 프로덕션 코드에 대해 테스트하십시오. 이를 통해 Adobe 컨설턴트는 사용자를 쉽게 지원할 수 있습니다.

자세한 정보는 *다이내믹 태그 관리를 사용하여 Adobe Target을 구현하기 위한 우수 사례* 가이드에서 [옵션 3: DTM을 통해 호스팅된 Target 자바스크립트 라이브러리를 사용하여 수동으로 Target 구현](https://experienceleague.adobe.com/docs/dtm/implementing/target/add-target/t-implementing-target-manually-js-hosted-dtm.html)을 참조하십시오.

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