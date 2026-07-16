---
title: 시작 안내서
description: 액세스 요청에서 첫 번째 기능 플래그 만들기에 이르기까지, 응용 프로그램을 플래그와 통합하려면 다음 단계를 따르십시오.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# 시작 안내서 {#startup-guide}

플래그를 애플리케이션에 통합하려면 다음 단계를 따르십시오.

## 1단계: 액세스 요청 {#step-1-access}

플래그 콘솔에 대한 액세스를 요청하고 팀에 참여합니다. 단계별 지침은 [액세스 요청](../console/request-access.md)을 참조하십시오.

## 2단계: 애플리케이션 온보드 {#step-2-onboard}

액세스 권한을 얻은 후 Flags 콘솔에 로그인하고 팀이 사용자의 응용 프로그램 목록에 있는지 확인합니다. 그렇지 않은 경우 팀 관리자에게 추가하도록 요청하십시오. [응용 프로그램 온보딩](../applications/onboard-your-application.md)을 참조하세요.

온보딩 전에 다음 사항을 준비하십시오.

| 요구 사항 | 세부 사항 |
|---|---|
| **응용 프로그램 ID** | Flags API를 호출할 때 사용되는 고유 클라이언트 식별자입니다. 사용 가능한 경우 애플리케이션의 기존 클라이언트 ID를 사용합니다. |
| **서버측 클라이언트** | 서버측 SDK과 통합하는 경우 적절한 권한이 있는 관리 클라이언트 ID가 필요합니다. |
| **데스크톱 클라이언트** | 클라이언트 ID 대신 제품 코드와 제품 버전을 사용할 수 있습니다. |

## 3단계: 자격 증명 가져오기 {#step-3-credentials}

필요한 자격 증명은 통합 경로에 따라 다릅니다.

* **웹 및 모바일(태그 기반):** 게시된 태그 속성에서 **환경 파일 ID**&#x200B;를 사용합니다. 이 작업을 수행하는 방법은 4a단계 를 참조하십시오.
* **서버 측 SDK:** SDK에서 API를 호출하기 전에 **서비스 토큰 ID를 요청**&#x200B;하고 Flags를 지원하도록 합니다.
* **데스크톱:** 클라이언트 ID 대신 제품 코드와 제품 버전을 사용할 수 있습니다.

## 4단계: SDK을 사용하여 통합 {#step-4-integrate}

응용 프로그램 유형에 대해 [통합 단계](integration-steps.md)를 따르십시오. 스택에 맞는 경로를 선택합니다.

* **웹 서비스** → Java SDK 또는 Node.js SDK
* AEP Mobile SDK→ **웹 및 모바일 앱** — [Android](../sdk-releases/android/android-extension-integration-guide.md) 및 [iOS](../sdk-releases/ios/ios-extension-integration-guide.md) 안내서 참조
* **데스크톱 앱** → SDK(준비 중)

## 4a단계: 데이터 수집 설정 및 구성 게시 {#step-4a-data-collection}

태그 기반 접근 방식(웹 또는 모바일)을 통해 통합하는 경우 SDK을 초기화하기 전에 태그 속성을 구성하십시오.

1. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에서 모바일 또는 웹 속성을 엽니다.
1. **Edge Network** 확장을 설치한 다음 **경험 롤아웃** 확장을 순서대로 설치합니다.
1. **데이터 스트림**(Customer Journey Analytics 데이터 세트를 포함해야 함)과 Edge 도메인을 선택하십시오.
1. **프로덕션의 개발 → 스테이징**→ 통해 구성을 게시합니다.
1. **환경** 탭에서 **환경 파일 ID**&#x200B;을(를) 복사합니다. 이 ID를 사용하여 SDK을 초기화합니다.

>[!IMPORTANT]
>
>**스테이징** 환경에서 환경 파일 ID를 `staging/`(으)로 접두사로 사용합니다. 즉, `staging/<environmentId>`을(를) 사용합니다. **프로덕션**&#x200B;에서 환경 파일 ID를 직접 사용하십시오.

## 5단계: 첫 번째 기능 플래그 만들기 및 테스트 {#step-5-feature-flag}

통합이 완료되면 콘솔에서 첫 번째 기능 플래그를 만들고 테스트합니다.

* [첫 번째 기능 플래그 만들기](../feature-flags/create-your-first-feature-flag.md)

## 참조: {#see-also}

* [앱에 플래그 통합](integrating-in-your-app.md)
* [통합 단계](integration-steps.md)
* [SDK](sdks.md)

<!-- -->
