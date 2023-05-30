---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2e6efe777925eb14e280ea38110dc1cb12264d17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 82%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 23.5.2 (2023년 5월 31일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 프로필 API 인증 토큰을 생성하는 동안 빈 페이지가 표시되는 문제가 해결되었습니다. (TGT-45387 및 TGT-45423)
* 이미지 이름에 GB 18030 문자가 포함된 경우 [!UICONTROL 디자인 만들기] 패널에 이미지를 표시할 수 없는 문제가 해결되었습니다. (TGT-44614)
* 경험의 텍스트/HTML에서 일부 GB 18030 기호 문자가 잘못 이스케이프되는 문제가 수정되었습니다. (TGT-44600)
* 분석 중에 [!UICONTROL 자동 개인화] 활동에 대한 보고서가 정지되는 문제가 해결되었습니다. (TGT-44820)
* 에서 활동을 검색할 수 없는 문제를 해결했습니다. [!UICONTROL 활동] 활동 이름에 대괄호( )가 포함된 경우 페이지 [ 또는 ] ). (TGT-44777)
* 활동 목표에 특수 문자가 포함된 경우 활동이 동기화되지 않는 문제를 해결했습니다. (TGT-44982)
* 에 활동이 표시되지 않던 문제를 수정했습니다. [!DNL Target] 특정 고객을 위한 기본 작업 영역의 UI. (TGT-45286)
* “중복 허용 안 함” 플래그의 비헤이비어가 업데이트되었습니다. 제외된 반복 오퍼 플래그가 기본 콘텐츠 오퍼(API v3, v4의 경우)인 경우 반복 오퍼를 허용하고, 옵션이 기본 콘텐츠 오퍼를 참조하고 정의된 템플릿이 없는 경우에는 중복 옵션을 허용하도록 업데이트되었습니다. (TNT-46617)
* URL에 쿼리 매개 변수가 추가되어 페이지에서 페이지를 로드할 수 없는 문제가 해결되었습니다. [!UICONTROL 시각적 경험 작성기] (VEC). (TGT-44873)
* [!DNL Target] UI 전반에 걸쳐 다양한 현지화 수정을 수행했습니다.

## [!DNL Target] Standard/Premium 23.5.1 (2023년 5월 23~25일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

5월 23일: 유럽, 중동 및 아프리카(EMEA) 지역
5월 24일: 아시아 태평양(APAC) 지역
5월 25일: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 개선 사항 및 수정 사항이 포함되어 있습니다.

* 특정 고객이 “다음보다 큼” 또는 “다음보다 작음” 연산자를 사용하여 방문자 프로필로 대상자를 만들 수 없는 문제가 해결되었습니다. (TGT-45271)
* [!DNL Target] UI 전반에 걸쳐 다양한 현지화 수정을 수행했습니다.
* 향후 예정된 UI 개선을 위해 다양한 위치에서 Target UI가 업데이트되었습니다(업데이트가 출시될 때까지 변경 사항은 기능 플래그 뒤에 있음).

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
