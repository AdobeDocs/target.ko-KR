---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b1bde455f686c34e7a5184868ce63db0b74e2af7
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 29%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 6월 19일**

>[!NOTE]
>
>* 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.6.3 (2025년 6월 20일 토요일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 기존 VEC에서 사용할 수 있는 기능에 맞게 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) UI에 [!UICONTROL Rearrange] 옵션을 추가했습니다. (TGT-46957)
* 한 작업 영역에서 다른 작업 영역으로 활동을 복사하면 &quot;null이 아니어야 합니다&quot; 또는 &quot;문제가 발생했습니다&quot;와 같은 오류가 트리거되는 문제가 해결되었습니다. (TGT-52474)
* 특정 활동에 대해 [!UICONTROL Automated Segments] 및 [!UICONTROL Important Attributes] 보고서가 생성되지 않는 문제가 해결되었습니다. (TNT-52904)
* 업데이트된 VEC에서 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동의 기본 콘텐츠 처리가 이전 UI와 일치하지 않는 문제를 해결했습니다. 이제 명시적으로 추가된 그룹이 없을 때 시스템은 `optionGroupLocalId = 0`을(를) 가진 &quot;기본 콘텐츠&quot;라는 기본 `optionGroup`을(를) 자동으로 추가합니다. 이 그룹에는 기본 옵션(예: `optionLocalId: 0`)이 포함되어 있습니다. 기본 콘텐츠가 제거되면 해당 옵션 그룹도 제거됩니다. (TGT-52651)
* 이전에 제거한 경험에서 `experienceLocalId`을(를) 다시 사용할 수 없도록 잘못 설정된 [!UICONTROL Multivariate Test]&#x200B;(MVT) 활동의 문제를 해결했습니다. (TNT-52672)
* 슬래시(/)와 같은 잘못된 문자로 인해 활동 위치의 URL에 쿼리 매개 변수가 표시되지 않는 문제가 해결되었습니다. (TNT52845)
* 백 엔드 API를 통해 [!DNL A/B Test] 활동 업데이트에 대한 유효성 검사 오류 메시지가 개선되었습니다. 중복된 위치 이름이 있으면 메시지에 `locations.selectors`에 대해 &quot;중복된 이름은 사용할 수 없습니다.&quot;라는 메시지가 표시됩니다. (TGT-52589)
* 요청 페이로드의 인식할 수 없는 속성으로 인해 실시간 [!UICONTROL Recommendations] 활동을 업데이트할 때 발생하는 오류를 수정했습니다. 이제 시스템에서 &quot;잘못된 JSON&quot;을 올바르게 처리합니다. 인식할 수 없는 속성 이름 오류. (TNT52723)
* [!UICONTROL Recommendations] 활동을 저장할 때 &quot;400 잘못된 요청&quot; 오류가 발생하는 백엔드 유효성 검사 오류를 해결했습니다. (TNT-52716)
* [!UICONTROL Location] 드롭다운에서 특수 문자가 있는 mbox를 마우스로 가리키면 편집기가 비어 있고 &quot;Element&quot;에서 &quot;querySelector&quot;를 실행하지 못했습니다.&quot;가 트리거되는 [!UICONTROL Form-Based Experience Composer]의 문제를 해결했습니다. 라는 오류가 표시됩니다. (TGT-52717)
* 새로운 &quot;PARTIALLY_IMPORTED&quot; 표시기로 피드 상태 정확도를 개선했습니다. 이전에는 파일의 모든 행을 가져오지 않았더라도 피드가 &quot;성공&quot;으로 표시되었으므로 이는 잘못된 선택이었습니다.
* AP V2로 마이그레이션한 후 특정 API 호출이 `/admin/rest/ui/v1/campaigns`에 대해 클라이언트측 오류를 반환한 오류를 해결했습니다(HTTP 4xx). (TGT-52721)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
