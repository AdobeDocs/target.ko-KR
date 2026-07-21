---
title: 시작 안내서
description: 액세스 요청에서 첫 번째 기능 플래그 만들기에 이르기까지, 응용 프로그램을 플래그와 통합하려면 다음 단계를 따르십시오.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 9a4e16418c93fa163d821409a0eecb251f2a9929
workflow-type: tm+mt
source-wordcount: '352'
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

## 3단계: 환경 파일 ID 가져오기 {#step-3-credentials}

필요한 환경 파일 ID는 통합 경로에 따라 다릅니다.

* **웹 및 모바일(태그 기반):** 게시된 태그 속성에서 **환경 파일 ID**&#x200B;를 사용합니다. 이 작업을 수행하는 방법은 4a단계 를 참조하십시오.

## 4단계: SDK을 사용하여 통합 {#step-4-integrate}

애플리케이션 유형에 대한 통합 안내서를 따르십시오. 스택에 맞는 경로를 선택합니다.

* **웹 및 모바일 앱** — 통합 안내서 섹션의 [Android](../sdk-releases/android/android-extension-integration-guide.md), [iOS](../sdk-releases/ios/ios-extension-integration-guide.md) 및 [웹](../sdk-releases/web/web-extension-integration-guide.md) 안내서를 참조하십시오.

## 4a단계: 데이터 수집 설정 및 구성 게시 {#step-4a-data-collection}

태그 기반 접근 방식(웹 또는 모바일)을 통해 통합하는 경우 SDK을 초기화하기 전에 태그 속성을 구성하십시오.

1. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/data-collection)에서 모바일 또는 웹 속성을 엽니다.
1. **Edge Network** 확장을 설치한 다음 **플래그** 확장을 순서대로 설치합니다.
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
* [SDK](sdks.md)

<!-- -->
