---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 911950b341d8221145eeacfa288926b0a1be434e
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 33%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 3월 7일 토요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target Standard/Premium] 25.3.5(2025년 3월 11일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 이동 경로가 편집기 하단에 항상 표시되지 않아 요소를 정확하게 선택할 수 없는 문제가 해결되었습니다. (TGT-51844)
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

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
