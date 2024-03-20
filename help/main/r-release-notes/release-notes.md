---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6e15b9b10e6a40c8efec06c45442b0f9894e648e
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 55%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 다음에 대한 업데이트 `Browser:iPad` 및 `Browser:iPhone` 위치: [!UICONTROL Browser] 대상 속성(2024년 4월 30일)

| 업데이트 | 세부 사항 |
|--- |--- |
| [!UICONTROL Browser:iPad] 및 [!UICONTROL Browser:iPhone] 다음에서 업데이트됨: [브라우저 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md) 대상자를 만들 때 사용됩니다. | [!DNL Adobe Target] 다음 작업을 수행할 수 있습니다. [여러 범주 속성 중 하나를 타깃팅합니다.](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md) 방문자가 페이지를 방문할 때입니다.<P>다음으로 시작 [!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일), Target UI를 사용하여 생성된 내장 대상, 예: `Browser:iPad` 및 `Browser:iPhone` 다음에 대한 적절한 타깃팅을 수행하도록 업데이트됩니다. [!DNL iPad] 및 [!DNL iPhone] 사용 `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` 및 `profile.mobile.isTablet`.<P>이 업데이트에는 고객 측에서 작업을 수행할 필요가 없습니다.<p><B>중요 사항</b>: 고객이 다음에 대한 적절한 타겟팅을 수행할 수 있도록 지원 [!DNL iPad] 및 [!DNL iPhone] 프로필 스크립트(및 JavaScript 세그먼트)에서 수동 변경은 다음 작업을 수행하여 고객이 수행해야 합니다 **2024년 4월 30일**. 수동으로 변경해야 하는 대체 설정의 예는 [다음에 대한 업데이트 [!DNL iPad] 및 [!DNL iPhone] 위치: [!UICONTROL Browser] 대상 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

## [!UICONTROL Visual Editing Helper] 내선 번호(2024년 3월 14일)

이 릴리스에는 다음과 같은 개선 사항 및 수정 사항이 포함되어 있습니다. [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) 확장 [!DNL Google Chrome]:

* 고객 웹 사이트에서 작성을 수행할 때 iFrame 로드 메커니즘을 개선했습니다.
* 에서 작성을 수행하는 동안 확장에서 쿠키를 복제하는 문제가 해결되었습니다. [!UICONTROL Visual Experience Composer] (VEC).

## [!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일)

이번 릴리스는 다음 날짜로 예정되어 있습니다.

* **3월 4일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 5일**: 아시아 태평양(APAC) 지역
* **3월 6일**: 아메리카 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 활동에서 고유 선택기의 수를 계산하는 논리를 수정했습니다. (TGT-47878)
* 의 원인이 되는 문제가 해결되었습니다. [!UICONTROL Multivariate] (MVT) 활동 구성 [!UICONTROL Analytics for Target] (A4T) 보고가 제대로 표시되지 않습니다. (TGT-47490)
* 트래픽이 없는 경험을 제어 경험으로 사용할 때 보고에 표시되는 경고 메시지가 개선되었습니다. (TGT-47537)
* 많은 백엔드 및 현지화 수정 사항이 추가되었습니다.

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
