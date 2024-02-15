---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 4395caa7e40717c59067eaedff5e53776768eda9
workflow-type: ht
source-wordcount: '573'
ht-degree: 100%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 브라우저 대상자 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)

| 사용 중단 | 세부 사항 |
|--- |--- |
| 대상자를 만들 때 사용되는 [브라우저 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md)에서 [!DNL iPad] 및 [!DNL iPhone]이 사용 중단됩니다.<p>사용 중단 일자:<P>2024년 4월 30일 | [!DNL Adobe Target]에서는 페이지를 방문할 때 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md)을 사용하는 사용자 등 [여러 카테고리 속성을 타겟팅](/help/main/c-target/c-audiences/c-target-rules/target-rules.md)할 수 있습니다.<P><B>2024년 4월 30일부터 대상자 카테고리를 만들 때 사용 가능한 [!UICONTROL 브라우저] 유형 드롭다운 목록에서 iPad 및 iPhone이 제거됩니다.</b><P>“브라우저: iPad” 및 “브라우저: iPhone”과 같이 [!DNL Target] UI를 사용하여 생성된 기본 대상자는 자동으로 새 대상자 정의로 이동됩니다.<p>수동으로 변경해야 하는 대체 설정의 예는 [브라우저 대상자 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation)을 참조하십시오. |

## [!DNL Target] Standard/Premium 24.1.1 (2024년 1월 22일, 23일 및 25일)

이번 릴리스는 다음 날짜로 예정되어 있습니다.

* **1월 22일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **1월 23일**: 아시아 태평양(APAC) 지역
* **1월 25일**: 아메리카 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 수익 목표 지표가 포함된 [!UICONTROL Analytics for Target] (A4T) 활동에 “매출”이 열 이름으로 표시되지 않았고 매출 지표가 보고에서 ($) 형식으로 표시되지 않았습니다. 이는 이미 해결된 표시용 문제였습니다. (TGT-46995)
* 보고 일자 간격이 올바르게 작동하지 않는 문제를 수정했습니다. (TGT-47396)
* 고객이 [!UICONTROL 추가 작업] 아이콘을 사용하여 활동을 활성화하거나 비활성화한 후 [!UICONTROL 모든 활동] 페이지에 잘못된 상태가 표시되는 문제를 수정했습니다. (TGT-47367)
* [!UICONTROL 중요 속성] 보고서가 단일 고객에 대해 표시되지 않는 문제를 수정했습니다. (TGT-47272)
* 단일 고객이 “인증 요구”를 활성화하려고 하면 “잘못된 페이로드” 메시지가 표시되는 문제를 수정했습니다. (TGT-47195)
* [!DNL Target] UI에서 여러 현지화된 문자열을 업데이트했습니다.

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
