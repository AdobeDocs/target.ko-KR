---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 065220af5c8e3b6cc25ef7289d006a901d2e932a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 15%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 날짜: 2025년 7월 22일**

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
* 사용자가 보조 데이터베이스에서 이전에 삭제된 활동 옵션을 복원할 수 있는 새 API 엔드포인트가 도입되었습니다. 이 기능은 `RemovedCampaignElements` 및 `RemovedOptionInfo` 클래스에서 제공하는 기존 인프라를 활용하므로 삭제된 옵션을 활성 활동으로 원활하게 재통합할 수 있습니다. (TGT-52903)
* [!DNL Target]&#x200B;(AP) 활동에서 삭제된 오퍼가 원래 이름 대신 [!UICONTROL Automated Personalization]&#x200B;(예: 기존 UI에 표시된 `Deleted option with ID: X`)으로 표시되는 업데이트된 `Offer Name [Deleted]` UI의 문제를 해결했습니다. 이 수정 사항은 삭제된 오퍼에 대해 의미 있는 레이블을 복원하여 명확성을 개선하고 보다 정확하고 사용자 친화적인 보고를 만듭니다. (TGT-52921)
* 삭제된 옵션이 올바르게 저장되었지만 기존 API 끝점을 통해 액세스할 수 없는 백엔드 지속성 레이어의 문제를 해결했습니다. 따라서 프론트엔드 응용 프로그램에서 삭제된 옵션의 의미 있는 이름을 검색할 수 없어 기록 보고 보기에 영향을 줍니다. 이 수정 사항을 통해 보존된 삭제된 옵션 데이터가 이제 UI에 제대로 표시될 수 있습니다. (TGT-52973)
* 이전에 수정된 동기화 버그로 인해 Target 프론트엔드에서 Target Central로 마이그레이션된 일부 활동의 지표 구성이 일치하지 않는 문제가 수정되었습니다. 특히 원래 전환 지표를 사용했으며 나중에 분석 기반 지표로 업데이트된 활동은 `primaryMetricType` 및 `successCriteria` 필드에 오래된 값을 유지합니다. (TGT-52643)

+++

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
* API 제한으로 인해 25자를 초과하는 지표 이름이 포함된 [!DNL Recommendations] 활동을 열거나 편집할 수 없는 문제가 해결되었습니다. 이 수정 사항은 문자 제한을 초과하는 지표 이름과의 호환성을 보장하여 영향을 받는 활동에 대한 전체 액세스를 복원합니다. (TGT-52839)
* 사용자가 [!DNL Recommendation] UI에서 site_cart_z1 [!DNL Target] 활동을 편집할 수 없는 문제가 해결되었습니다. 활동을 열려고 하면 [!UICONTROL Overview] 페이지에서 오류가 발생하여 편집기에 대한 액세스가 차단됩니다. (TGT-53221)

+++

**보고**

+++세부 정보 보기
* 보고 소스를 [!DNL Customer Journey Analytics] 또는 [!DNL Analytics]에서 [!DNL Target]&#x200B;(으)로 전환할 때 활동 데이터베이스의 샌드박스 필드가 지워지지 않는 문제가 해결되었습니다. 이전에는 UI에서 샌드박스: null을 올바르게 보냈지만 백엔드가 이 값을 무시하여 오래된 샌드박스 데이터가 제자리에 남았습니다. 이제 null이 수신되면 백엔드가 샌드박스 필드를 제대로 지웁니다. (TGT-52798)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 정확한 내역 보고를 지원하기 위해 Target 백엔드에서 삭제된 옵션 지속성 계층을 다시 구현했습니다. 이전에는 옵션을 삭제할 때 해당 이름이 손실되어 이전 성능 데이터를 해석하기 어려웠습니다.

  **주요 개선 사항**:

   * 삭제된 옵션은 이제 기존 `RemovedCampaignElements` 및 `RemovedOptionInfo` 인프라를 사용하여 추적됩니다.
   * 옵션이 AP 활동에서 제거되면 해당 메타데이터(예: ID 및 이름)는 유지됩니다.
   * 보고 UI는 이제 기록 지표와 함께 원래 옵션 이름(예: `Option Name [Deleted]`)을 표시할 수 있으므로 명확성과 유용성이 향상되었습니다.

  이 업데이트를 사용하면 활동에서 옵션이 제거된 후에도 일관되고 의미 있는 보고를 수행할 수 있습니다. (TGT-52986)

* 삭제된 활동 옵션을 JCR 기반 활동에서 [!DNL Target] Central로 전송하는 것을 지원하기 위해 새 마이그레이션 끝점을 구현했습니다. 이 기능을 사용하면 시스템 간에 일관된 추적 및 보고를 수행할 수 있습니다. 이 기능을 사용하면 삭제된 옵션이 [!DNL Target] 프론트엔드 및 백엔드에서 유지되고 동기화되어 기록 보고 및 데이터 무결성을 향상시킬 수 있습니다. (TGT-53217)

+++

**VEC(시각적 경험 작성기)**

+++세부 정보 보기

* 보기에 수정 사항을 적용하면 중복이 발생하고 &#39;잘못된 사용자 입력&#39; 오류가 트리거되는 VEC의 문제가 해결되었습니다. (TGT-52886)
* VEC에서 이미지 오퍼를 구성할 때 [!UICONTROL Undo] 및 [!UICONTROL Insert Before] 옵션에 대한 [!UICONTROL Insert After] 기능 문제를 해결했습니다.

  이전에는 이미지 오퍼에서 [!UICONTROL Insert Before] 또는 [!UICONTROL Insert After] 작업을 실행 취소하면 일관되지 않은 동작이 발생하거나, 특히 레거시 [!DNL Target] UI에서 만든 활동에서 수정을 제대로 되돌리지 못했습니다. 이 문제는 실행 취소 작업이 이러한 수정 사항에 대해 안정적으로 작동하도록 하기 위해 해결되었습니다. (TGT-52809)

* `contentEditable` 특성이 실수로 true로 설정되어 저장된 HTML 콘텐츠에서 지속되는 문제가 해결되었습니다. 이 업데이트를 통해 의도하지 않은 편집 동작 없이 깔끔하고 예상되는 HTML 출력이 보장됩니다. (TGT-52319)
* 삭제된 옵션의 영구 손실을 방지하고 서비스 간 일관된 동작을 보장하기 위해 UI 및 관련 마이크로 서비스의 옵션에 대해 소프트 삭제 기능을 구현했습니다.

  **주요 변경 사항**:

   * 옵션이 더 이상 영구적으로 삭제되지 않습니다. 대신 매개 변수 XML 개체에 새로운 deleted: true 플래그로 표시됩니다.
   * 이 플래그는 삭제된 옵션을 렌더링에서 제외하고 Edge Services로 전송되지 않도록 업데이트된 [!DNL Target] UI에서만 사용됩니다.
   * 삭제된 옵션은 편집하는 동안 활동 페이로드의 일부로 유지되므로 추적성이 보장되며 존재하지 않는 옵션은 고객에게 전달되지 않습니다.

  이 업데이트는 데이터 무결성을 향상시키고 분산 시스템에서 삭제 작업을 관리하는 우수 사례에 부합합니다. (TGT-52726)

+++

**작업 공간**

+++세부 정보 보기
* 기본이 아닌 작업 영역에서 기본 작업 영역으로 또는 기본이 아닌 작업 영역 간에 활동을 복사할 때 발생하는 문제를 해결했습니다. 이제 충돌을 방지하기 위해 향상된 추적 및 이름 지정으로 오퍼가 복제됩니다.

  **주요 개선 사항**:
   * 오퍼는 업데이트된 ID 및 메타데이터로 대상 작업 영역에 다시 생성됩니다.
   * 복사된 오퍼의 이름은 고유성을 위해 &quot;오퍼 이름 사본&quot; 형식과 난수 또는 타임스탬프를 사용하여 변경됩니다.
   * 시스템은 새 ID를 반영하도록 오퍼 및 활동 상태를 업데이트합니다.
   * 이 기능은 반복된 복사 작업 동안 여러 개의 동일한 &quot;오퍼 복사&quot; 이름으로 인해 발생하는 오류를 방지합니다.
   * 오퍼가 대상 작업 영역의 오퍼 목록에 바로 표시되지 않을 수 있지만 적절하게 처리되고 표시됩니다.

  이 업데이트는 여러 작업 공간에서 오퍼를 관리할 때 안정성과 추적 가능성을 향상시킵니다. (TGT-53080)

+++

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
