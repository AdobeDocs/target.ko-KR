---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 44445f269a69a3ac3e3bc88bab8abf9fc4d51663
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 58%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics] (2024년 5월 8일)

통합 대상 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} 및 [!DNL Target] 은 최적화 프로그램에 강력한 분석 및 시간 절약 도구를 제공합니다.

[!DNL Customer Journey Analytics]를 [!DNL Target]에 대한 보고 소스로 사용하는 경우의 주요 이점은 다음과 같습니다.

* 마케터가 언제든지 [!DNL Customer Journey Analytics] 성공 지표 또는 보고 세그먼트를 [!DNL Target] 활동 보고서에 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 마케터는 를 활용할 수 있습니다. [!DNL Customer Journey Analytics] 다음과 같은 기능 [실험 패널](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}을 추가하여 웹 사이트 개인화를 추가로 분석하십시오.
* 마케터는에 대한 단일 보고 소스를 가질 수 있습니다. [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/reporting/cja-ajo){target=_blank} 및 [!DNL Target]. 두 개인화 제품 모두 [!DNL Customer Journey Analytics]에 연결하여 웹 개인화를 보다 전체적으로 살펴볼 수 있습니다.

자세한 내용은 [Adobe Customer Journey Analytics의 Target 보고](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

## [!UICONTROL Visual Experience Composer] 도우미 확장 프로그램(2024년 4월 23일)

레거시 [!DNL Target] 시각적 경험 작성기 Helper 확장이 매니페스트 V2를 사용하여 만들어졌습니다. [!DNL Google] 2024년 6월부터 Manifest V2를 사용하여 만든 확장을 더 이상 허용하지 않는다고 발표했습니다. 자세한 내용은 [[!UICONTROL Visual Experience Composer] 도우미 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] 는 고객이 최신 (으)로 이동하기를 권장합니다. [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) 가능한 한 빨리

## 다음에 대한 업데이트 `Browser:iPad` 및 `Browser:iPhone` 위치: [!UICONTROL Browser] 대상 속성(2024년 4월 30일)

| 업데이트 | 세부 사항 |
|--- |--- |
| [!UICONTROL Browser:iPad] 및 [!UICONTROL Browser:iPhone] 다음에서 업데이트됨: [브라우저 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md) 대상자를 만들 때 사용됩니다. | [!DNL Adobe Target] 다음 작업을 수행할 수 있습니다. [여러 범주 속성 중 하나를 타깃팅합니다.](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md) 방문자가 페이지를 방문할 때입니다.<P>다음으로 시작 [!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일), Target UI를 사용하여 생성된 내장 대상, 예: `Browser:iPad` 및 `Browser:iPhone` 다음에 대한 적절한 타깃팅을 수행하도록 업데이트됩니다. [!DNL iPad] 및 [!DNL iPhone] 사용 `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` 및 `profile.mobile.isTablet`.<P>이 업데이트에는 고객 측에서 작업을 수행할 필요가 없습니다.<p><B>중요 사항</b>: 고객이 다음에 대한 적절한 타겟팅을 수행할 수 있도록 지원 [!DNL iPad] 및 [!DNL iPhone] 프로필 스크립트(및 JavaScript 세그먼트)에서 수동 변경은 다음 작업을 수행하여 고객이 수행해야 합니다 **2024년 4월 30일**. 수동으로 변경해야 하는 대체 설정의 예는 [다음에 대한 업데이트 [!DNL iPad] 및 [!DNL iPhone] 위치: [!UICONTROL Browser] 대상 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
