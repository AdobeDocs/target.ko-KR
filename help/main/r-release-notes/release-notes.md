---
keywords: 릴리스 노트;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트,현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 729b88c3db9e88a5cd428587e34614c5d56542da
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 45%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 25.3.5(2025년 3월 11일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 사용자가 [!UICONTROL Modifications] 패널에서 오퍼를 변경할 수 없는 문제를 해결했습니다. (TGT-51800)
* [!UICONTROL ClickTrack] 모드를 포함하여 경험 및 대상을 위한 왼쪽 패널에 액션이 잘못 표시되는 문제를 해결했습니다. (TGT-51895)
* [!UICONTROL ClickTrack] 선택기가 올바른 대상 페이지에 적용되지 않던 문제를 해결했습니다. (TGT-51871)

## [!DNL Target Standard/Premium] 25.3.4(2025년 3월 7일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 활동 전용 대상이 [!UICONTROL Audiences] 패널에 표시되지 않아서 편집하거나 재사용할 수 없는 문제가 해결되었습니다. (TGT-51860)
* [!DNL Target Standard] 고객이 [!UICONTROL Analytics for Target]&#x200B;(A4T) 보고를 사용하여 활동을 만들 수 없도록 차단하는 문제를 해결했습니다. (TGT-51854)
* 일괄 작성 및 편집 작업 중에 페이로드에서 로컬 ID 카운터를 제외하는 문제를 해결했습니다. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2(2025년 3월 6일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 활동 전용 대상을 사용하여 활동을 복사하는 경우 원래 활동의 대상을 대신 잘못 사용하여 새 활동을 만들지 못하는 문제가 해결되었습니다. (TGT-51855)
* 활동 전용 대상이 있는 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동을 편집할 수 없는 문제를 해결했습니다. (TGT-51846)
* [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 첫 번째 편집 시 환경에 수정 사항을 올바르게 적용하지 못하는 문제를 해결했습니다. (TGT-51843)
* VEC 내에서 특정 요소를 클릭할 때 &#39;ID&#39; 오류를 트리거하는 문제를 해결했습니다. (TGT-51814)
* 활동을 만드는 동안 VEC에서 오류 처리가 업데이트되었습니다. (TGT-51759)
* 활동을 저장할 때 [!UICONTROL Modifications] 패널에서 보기가 누락되어 &#39;잘못된 사용자 입력&#39; 오류가 발생하는 문제를 해결했습니다. (TGT-51827)
* 권장 사항 기준을 만들 수 없는 문제를 해결했습니다. (TGT-51834)
* 다른 URL로 리디렉션하기 전에 확인 메시지를 추가했습니다. (TGT-51703)
* 오퍼 및 폴더 내의 GraphQL 통합 테스트와 관련된 문제가 해결되었습니다. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1(2025년 3월 3일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 결합된 대상은 하위 그룹을 포함할 수 있으며 각 그룹에는 여러 대상이 포함됩니다. 이 릴리스에서는 하위 그룹 대상이 [!UICONTROL Rules] 대화 상자에 표시되지 않는 문제를 해결했습니다. (TGT-51813)
* 이전 활동을 열 때 일부 경험 대상이 [!UICONTROL All Visitors]&#x200B;(으)로 대체되는 문제가 해결되었습니다. (TGT-51812)
* 활동 전용 대상이 있는 활동을 편집할 수 없는 문제를 해결했습니다. (TGT-51807)
* 업데이트된 [!DNL Target] UI에서 페이지 헤드 수정 사항을 편집할 수 없는 문제를 해결했습니다. (TGT-51797)
* 경험을 복제하고 다른 경험을 삭제한 다음 활동을 저장하려고 할 때 발생하는 null 오류를 해결했습니다. (TGT-51796)
* 활동을 만드는 [!UICONTROL Targeting] 단계 동안 대상 제외 규칙이 대상의 정보 패널에 표시되지 않는 문제를 해결했습니다. (TGT-51579)
* 한국어로 현지화된 오류 메시지가 업데이트되었습니다. (TGT-51701 및 TGT-51699)

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
