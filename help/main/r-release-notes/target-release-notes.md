---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: df7e28060a6add53e1aaed928351b4f399b19c17
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 34%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 7월 10일**

>[!NOTE]
>
>* 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.7.3(2025년 7월 24일)

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 이 릴리스에는 다음 수정 사항 및 업데이트가 포함되어 있습니다.

**활동**

+++세부 정보 보기
* 빌더 클래스의 `buildViews` 메서드가 `viewMaxLocalId`을(를) 할당된 가장 높은 `viewLocalId`이(가) 아닌 총 보기 수로 잘못 설정하는 문제를 해결했습니다. (TGT-53207)

**양식 기반 경험 작성기**

+++세부 정보 보기
* [!UICONTROL Form-Based Experience Composer]&#x200B;(AP) 활동을 만들거나 편집할 때 **[!UICONTROL Manage Content]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭한 후 편집기가 충돌하는 [!UICONTROL Automated Personalization]의 문제를 해결했습니다. (TGT-53047)

+++

**추천**

+++세부 정보 보기
* 목록의 맨 아래로 스크롤할 때 [!UICONTROL Catalog Search]이(가) 추가 결과를 로드하지 못하고 레거시 UI와 일치하는 동작을 복원하는 문제를 해결했습니다. (TGT-53088)
* 업데이트된 [!UICONTROL Number of Products] UI의 [!UICONTROL Collections] 페이지에서 [!DNL Target] 열이 누락되는 문제를 해결했습니다. 이제 열이 올바르게 표시되어 예상 기능을 복원합니다. (TGT-53168)
* [!UICONTROL Collection] 규칙이 규칙에 따라 제대로 필터링되지 않는 문제가 해결되었습니다. (TGT-53254)
* [!UICONTROL Criteria Details] 대화 상자에서 항목 삭제를 차단하는 문제를 해결했습니다. (TGT-53245)
* 이름이 없는 제품을 열거나 상호 작용할 수 없는 문제를 해결했습니다. 이 문제는 명명되지 않은 결과를 반환하는 환경을 선택할 때 발생하여 제품 세부 정보에 대한 액세스를 방해했습니다. (TGT-53007)
* 특정 제품을 선택할 때 [!UICONTROL Catalog Search] 페이지가 충돌하고 빈 화면이 표시되는 문제를 해결했습니다. (TGT-53087)

+++

**VEC(시각적 경험 작성기)**

+++세부 정보 보기

* 보기에 수정 사항을 적용하면 중복이 발생하고 &#39;잘못된 사용자 입력&#39; 오류가 트리거되는 VEC의 문제가 해결되었습니다. (TGT-52886)
* VEC에서 이미지 오퍼를 구성할 때 [!UICONTROL Undo] 및 [!UICONTROL Insert Before] 옵션에 대한 [!UICONTROL Insert After] 기능 문제를 해결했습니다.

  이전에는 이미지 오퍼에서 [!UICONTROL Insert Before] 또는 [!UICONTROL Insert After] 작업을 실행 취소하면 일관되지 않은 동작이 발생하거나, 특히 레거시 [!DNL Target] UI에서 만든 활동에서 수정을 제대로 되돌리지 못했습니다. 이 문제는 실행 취소 작업이 이러한 수정 사항에 대해 안정적으로 작동하도록 하기 위해 해결되었습니다. (TGT-52809)

+++

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
