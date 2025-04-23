---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ad82d108adc6f5c76b2104f40fb0bb2c66e98a2b
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 33%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 일자: 2025년 4월 23일 목요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target Standard/Premium] 25.4.5(2025년 4월 24일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* [!DNL Recommendations] 활동을 활성화한 후 권장 사항이 고객의 웹 사이트에 표시되지 않는 문제를 해결했습니다. (TGT-52164)
* 옵션이 변경되지 않은 경우 `OptionLocalIDs`이(가) 더 이상 잘못 증가하지 않습니다. (TGT-52187)
* 이제 다운로드된 보고 파일에 보고 UI에 있는 데이터가 올바르게 표시됩니다. (TGT-52068)
* 페이지 전달 규칙을 추가한 후 배치 작업이 더 이상 실패하지 않습니다. (TGT-52097)
* [!DNL Target]이(가) 웹 사이트의 URL에서 모든 쿼리 매개 변수를 트리밍하는 문제를 해결했습니다. (TGT-52100)
* 고객이 기존 및 업데이트된 Target UI에서 활동을 만들 수 없는 콘솔 오류를 해결했습니다. (TGT-52181)
* 고객이 새 페이지를 추가할 수 없도록 차단하여 잘못된 사용자 입력 오류가 발생하는 문제를 해결했습니다. (TGT-52258)
* 페이지를 추가한 후 [!UICONTROL Experiences] 탭으로 다시 이동한 후 수정 사항이 사라지는 문제를 해결했습니다. (TGT-52264)
* [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에서 고객이 대상을 변경할 수 없도록 차단하는 문제를 해결했습니다. (TGT-52191)
* 지원되지 않는 UI 규칙으로 인해 XT 활동을 편집할 수 없는 오류가 수정되었습니다. (TGT-52273)
* 웹 페이지에 성공적으로 전달되었지만 활동 수정 사항이 [!DNL Target] UI에 표시되지 않는 문제를 해결했습니다. (TGT-52192)
* 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 이동 경로가 편집기 하단에 항상 표시되지 않아 요소를 정확하게 선택할 수 없는 문제가 해결되었습니다. (TGT-51169)
* 페이지 매김 때문에 [!UICONTROL Audience] 드롭다운 목록에 모든 대상이 표시되지 않던 문제를 해결했습니다. (TGT-52204)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에 새 오퍼를 추가할 때 잘못된 사용자 입력 메시지가 발생하는 문제를 해결했습니다. (TGT-52210)
* 고객이 A4T에 액세스할 수 없어도 [!UICONTROL Analytics for Target]&#x200B;(A4T)이 보고 소스로 잘못 선택되던 문제를 해결했습니다. (TGT-52226)
* [!UICONTROL View a Page] URL 지표로 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-52260)
* 고객이 활동 내에 오퍼를 만드는 동안 작업 영역을 선택할 수 없도록 차단하는 문제를 해결했습니다. (TGT-52289)
* 다른 경험으로 전환할 때 한 경험의 수정 사항이 잘못 표시되던 문제를 수정했습니다. (TGT-52184)
* 활동을 연 후 [!DNL Target] UI에 기본 오퍼가 잘못 표시되는 문제가 해결되었습니다. (TGT-52198)

## 타겟 권한 업데이트(2025년 4월 22일)

이 향후 업데이트는 [!DNL Target] 인스턴스 구성에 대한 조직의 제어를 강화하여 다양한 테스트 및 개인화 팀의 활동 전달에 영향을 줄 수 있는 우발적인 업데이트를 방지합니다.

2025년 4월 22일부터 [!DNL Target] 작업 영역의 역할에 관계없이 [!UICONTROL Product] 및 [!UICONTROL Solutions] 관리자만 [!UICONTROL Administration] 섹션의 설정을 업데이트할 수 있습니다. 이 권한이 없는 사용자는 [!UICONTROL Administration] 섹션에 대한 읽기 전용 액세스 권한을 갖게 됩니다.

자세한 내용은 [Target 관리](/help/main/administrating-target/start-target.md)를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
