---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c6799d43ee2f5ebe568f7199ae4ec1deaa164c06
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 43%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 일자: 2025년 4월 3일 금요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target Standard/Premium] 25.4.1(2025년 4월 2일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 경험 대상이 활동에서 사라지는 문제를 해결했습니다. (TGT-52003)
* 게재 중 예기치 않은 요소가 발생하는 문제를 해결했습니다. (TGT-52011)
* 고객이 활동 편집 중에 [!UICONTROL r]보기 페이지의 타깃팅 그래프에서 대상을 볼 수 없도록 하는 문제를 해결했습니다. (TGT-52050)
* 고객이 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에서 우선순위 순서대로 경험을 재정렬할 수 없는 문제를 해결했습니다. (TGT-52054)
* 텍스트 스타일 변경을 실행 취소할 때 잘못된 렌더링이 발생하는 문제를 해결했습니다. (TGT-51876)
* 리디렉션 오퍼를 수정할 때 [!DNL Target]이(가) 해당 오퍼와 연결된 [!UICONTROL ClickTrack] 선택기도 제거하는 문제를 해결했습니다. (TGT-51936)
* [!UICONTROL ClickTrack]을(를) 취소할 때 [!DNL Target]이(가) 선택기를 잘못 저장하는 문제를 해결했습니다. (TGT-51937)
* [!UICONTROL Goals & Settings] 페이지에서 mbox 선택기를 열고 닫은 후 변경하지 않고 잘못된 이름 오류를 트리거하는 문제를 해결했습니다. (TGT-51983)
* 기존 [!DNL Target] UI에서 만든 임시 오퍼 편집을 차단하는 문제를 해결했습니다. (TGT-51984)
* 사용자 지정 코드가 포함된 임시 오퍼가 있는 편집 활동을 차단하는 문제를 해결했습니다. (TGT-51995)
* 결합된 대상 정의를 편집할 때 제외 규칙이 포함 규칙으로 표시되던 문제를 수정했습니다. (TGT-51999)
* 경험 편집 중에 사용자 지정 코드가 올바르게 표시되지 않는 문제를 해결했습니다. (TGT-52005)
* 탐색 모음 앞에 콘텐츠를 삽입할 때 [!UICONTROL Insert Before] 옵션을 사용할 수 없는 문제를 해결했습니다. (TGT-52031)
* 보고에서 기본 경험이 올바르게 강조 표시되지 않는 문제를 해결했습니다. (TGT-51716)
* 활동을 만들 때 `default message [Invalid optionLocalIds: xx]]` 메시지를 트리거하는 문제를 해결했습니다. (TGT-52038)

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
