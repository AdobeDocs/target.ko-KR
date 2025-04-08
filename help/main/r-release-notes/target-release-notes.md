---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: eaba6fe562644874fc800612894218094ca37f1b
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 44%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 일자: 2025년 4월 8일 수요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## 타겟 권한 업데이트(2025년 4월 22일)

이 향후 업데이트는 [!DNL Target] 인스턴스 구성에 대한 조직의 제어를 강화하여 다양한 테스트 및 개인화 팀의 활동 전달에 영향을 줄 수 있는 우발적인 업데이트를 방지합니다.

2025년 4월 22일부터 [!DNL Target] 작업 영역의 역할에 관계없이 [!UICONTROL Product] 및 [!UICONTROL Solutions] 관리자만 [!UICONTROL Administration] 섹션의 설정을 업데이트할 수 있습니다. 이 권한이 없는 사용자는 [!UICONTROL Administration] 섹션에 대한 읽기 전용 액세스 권한을 갖게 됩니다.

자세한 내용은 [Target 관리](/help/main/administrating-target/start-target.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 25.4.3(2025년 4월 10일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* [!UICONTROL Form-Based Experience Composer]의 [!UICONTROL Activity QA] 링크가 [!DNL Adobe Experience Cloud] 홈 페이지로 잘못 리디렉션되는 문제가 해결되었습니다. (TGT-52055)
* 활동에서 중복 옵션을 확인하는 방법을 사용자에게 안내하는 오류 메시지를 추가했습니다. (TGT-51927)

## [!DNL Target Standard/Premium] 25.4.2(2025년 4월 8일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 저장하고 다시 연 후 [!UICONTROL A/B Test] 활동에 추가된 추가 페이지가 유지되지 않던 문제를 수정했습니다. (TGT-51994)
* 고객이 인라인 스타일 섹션에서 스타일을 삭제할 수 없는 문제를 해결했습니다. (TGT-52070)
* 기존 UI와 유사한 [!UICONTROL Activity QA] 대화 상자에서 [대상 정의 카드](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780)에 대한 액세스를 복원했습니다. (TGT-52056)
* 업데이트된 UI는 수정 없이 페이지 또는 대상자를 저장하지 않았습니다. 고객이 새 페이지나 대상을 활동에 추가했지만 변경하지 않는 경우 [!DNL Target]이(가) 저장 시 수정되지 않은 대상을 삭제했습니다. 이 동작을 사용자에게 알리기 위해 관련 위치에 알림이 추가되었습니다. (TGT-52104)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
