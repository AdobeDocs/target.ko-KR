---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 265108dbb0a459e1b111fda01a35042170f05562
workflow-type: tm+mt
source-wordcount: '4383'
ht-degree: 11%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]은(는) [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

+++세부 정보 보기
[!DNL Target] 팀은 토글 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능을 제공하고 있습니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다.

![Target UI 버전 전환](/help/main/r-release-notes/assets/toggle.png)

롤아웃이 완료되면 토글이 제거되고 모든 사용자가 업데이트된 UI로 영구적으로 전환됩니다. [!DNL Adobe]은(는) 이 기능이 곧 단계적으로 중단될 예정이므로 미리 계획하는 것이 좋습니다.

#### 사용 중단 타임라인

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 [!DNL Target] 팀이 사용 중단 타임라인을 조정했습니다.

* **2025년 6월 17일**: 모든 IMS 조직이 특정 사용자 또는 조직 전체에 대해 업데이트된 [!DNL Target] UI에 대해 활성화되어 새 경험 테스트를 시작합니다.

* **2025년 6월 30일**: [업데이트됨 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md)는 UI 버전 전환을 사용하도록 설정한 모든 IMS 조직의 기본 환경이 되었습니다.

   * 현재 기존 UI가 표시되는 고객은 기본적으로 이제 로그인 시 업데이트된 UI가 표시됩니다.
   * UI 버전 토글 기능은 7월 말까지 계속 사용할 수 있으며, 필요한 경우 다시 전환할 수 있습니다.

  >[!IMPORTANT]
  >
  > [!DNL Adobe]은(는) 업데이트된 [!DNL Target] UI를 사용할 것을 강력히 권장합니다. [전환 스위치 동작의 제한](#limitations) 때문에 차단기 문제가 발생하는 경우에만 레거시 UI로 다시 전환하십시오.

* **7월 15일부터 2025년 7월 30일까지**: UI 버전 토글이 단계적으로 영구적으로 비활성화됩니다. 영향을 받는 IMS 조직은 더 이상 기존 UI로 되돌릴 수 없습니다.

   * 예외는 사안별로 검토됩니다.
   * 전환 중단 지연은 차단 문제가 해결되는 동안 잠시(며칠) 동안만 부여됩니다.

문제가 있거나 이 전환 중에 문제가 예상되면 [Adobe 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)에 문의하십시오.

#### UI 전환 동작 제한 사항 {#limitations}

다음 정보는 버전 토글을 사용할 때 알아 두어야 할 제한 사항에 대해 설명합니다.

* **새 활동의 가시성**: 기존 UI로 다시 전환하면 업데이트된 UI에서 만들어진 활동이 표시되지 않습니다.
* **기존 활동 편집**: 업데이트된 UI를 사용하는 동안 기존 활동(원래 기존 UI에서 만들어짐)에 대한 변경 사항이 웹 사이트에 게시됩니다. 그러나 다시 전환하는 경우 이러한 업데이트가 이전 UI에 표시되지 않습니다. 이전 UI에서 수행한 마지막 업데이트만 표시됩니다.
* **활동 세부 정보의 일관성**: 사용하는 UI에 관계없이 가장 최근의 변경 내용이 라이브 웹 사이트에 반영됩니다. 하지만 기존 UI에는 해당 버전 내에서 변경된 최신 변경 사항만 표시됩니다. 업데이트된 UI에서 편집된 활동이 기존 UI에 표시되는 것과 다른 경우 이 상황이 혼동을 일으킬 수 있습니다.

#### 업데이트된 UI에 대해 알아볼 수 있는 추가 리소스

* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.
* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!DNL Target], [!UICONTROL Activities] 및 [!UICONTROL Recommendations]&#x200B;(VEC)에 대한 [!UICONTROL Visual Experience Composer]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!DNL Target]에 대한 [!UICONTROL Offers Library]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.
* [[!UICONTROL Visual Experience Composer] 변경 내용](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 도입되었습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.
* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.

+++

## [!DNL Target Standard/Premium] 25.7.3(2025년 7월 24일)

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 이 릴리스에는 다음 수정 사항 및 업데이트가 포함되어 있습니다.

**활동**

+++세부 정보 보기
* 빌더 클래스의 `buildViews` 메서드가 `viewMaxLocalId`을(를) 할당된 가장 높은 `viewLocalId`이(가) 아닌 총 보기 수로 잘못 설정하는 문제를 해결했습니다. (TGT-53207)
* [!DNL Target]&#x200B;(AP) 활동에서 삭제된 오퍼가 원래 이름 대신 [!UICONTROL Automated Personalization]&#x200B;(예: 기존 UI에 표시된 `Deleted option with ID: X`)으로 표시되는 업데이트된 `Offer Name [Deleted]` UI의 문제를 해결했습니다. 이 수정 사항은 삭제된 오퍼에 대해 의미 있는 레이블을 복원하여 명확성을 개선하고 보다 정확하고 사용자 친화적인 보고를 만듭니다. (TGT-52921)
* [!DNL Target] 프론트엔드에서 [!DNL Target] Central로 마이그레이션된 일부 활동이 이전에 수정된 동기화 버그로 인해 일치하지 않는 지표 구성을 가졌던 문제를 해결했습니다. 특히 원래 전환 지표를 사용했으며 나중에 분석 기반 지표로 업데이트된 활동은 `primaryMetricType` 및 `successCriteria` 필드에 오래된 값을 유지합니다. (TGT-52643)
* HTML 수정 사항에 의도하지 않은 `contentEditable` 속성 포함으로 인해 QA 미리 보기 페이지의 전체 콘텐츠를 편집할 수 있게 되는 문제를 해결했습니다. 이렇게 하면 사용자가 페이지의 모든 텍스트를 클릭하고 편집할 수 있으므로 레이아웃 문제와 QA 중에 혼동이 발생할 수 있습니다. (TGT-53247)
* 수정 내용을 [!DNL Page Load]에서 [!UICONTROL View]&#x200B;(으)로 이동하면 [!UICONTROL Page Load]에도 표시되면서 수정 내용이 복제되어 [!UICONTROL View]에 남아 있는 문제가 해결되었습니다. 또한 [!UICONTROL View]에서 수정 사항을 제거하면 [!UICONTROL Page Load]에서도 수정 사항이 잘못 제거됩니다. (TGT-53270)

+++

**API**

+++세부 정보 보기
* 삭제된 옵션이 올바르게 저장되었지만 기존 API 끝점을 통해 액세스할 수 없는 백엔드 지속성 레이어의 문제를 해결했습니다. 따라서 프론트엔드 응용 프로그램에서 삭제된 옵션의 의미 있는 이름을 검색할 수 없어 기록 보고 보기에 영향을 줍니다. 이 수정 사항을 통해 보존된 삭제된 옵션 데이터가 이제 UI에 제대로 표시될 수 있습니다. (TGT-52973)
* 삭제된 활동 옵션을 JCR 기반 활동에서 [!DNL Target] Central로 전송하는 것을 지원하기 위해 새 마이그레이션 끝점을 구현했습니다. 이 기능을 사용하면 시스템 간에 일관된 추적 및 보고를 수행할 수 있습니다. 이 기능을 사용하면 삭제된 옵션이 [!DNL Target] 프론트엔드 및 백엔드에서 유지되고 동기화되어 기록 보고 및 데이터 무결성을 향상시킬 수 있습니다. (TGT-53217)
* 사용자가 보조 데이터베이스에서 이전에 삭제된 활동 옵션을 복원할 수 있는 새 API 엔드포인트가 도입되었습니다. 이 기능은 `RemovedCampaignElements` 및 `RemovedOptionInfo` 클래스에서 제공하는 기존 인프라를 활용하므로 삭제된 옵션을 활성 활동으로 원활하게 재통합할 수 있습니다. (TGT-52903)
* API 제한으로 인해 25자를 초과하는 지표 이름이 포함된 [!DNL Recommendations] 활동을 열거나 편집할 수 없는 문제가 해결되었습니다. 이 수정 사항은 문자 제한을 초과하는 지표 이름과의 호환성을 보장하여 영향을 받는 활동에 대한 전체 액세스를 복원합니다. (TGT-52839)

+++

**양식 기반 경험 작성기**

+++세부 정보 보기
* [!UICONTROL Form-Based Experience Composer]&#x200B;(AP) 활동을 만들거나 편집할 때 **[!UICONTROL Manage Content]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭한 후 편집기가 충돌하는 [!UICONTROL Automated Personalization]의 문제를 해결했습니다. (TGT-53047)

+++

**추천**

+++세부 정보 보기
* 목록의 맨 아래로 스크롤할 때 [!UICONTROL Catalog Search]이(가) 추가 결과를 로드하지 못하고 레거시 UI와 일치하는 동작을 복원하는 문제를 해결했습니다. (TGT-53088)
* [!UICONTROL Criteria Details] 대화 상자에서 항목 삭제를 차단하는 문제를 해결했습니다. (TGT-53245)
* 이름이 없는 제품을 열거나 상호 작용할 수 없는 문제를 해결했습니다. 이 문제는 명명되지 않은 결과를 반환하는 환경을 선택할 때 발생하여 제품 세부 정보에 대한 액세스를 방해했습니다. (TGT-53007)
* 특정 제품을 선택할 때 [!UICONTROL Catalog Search] 페이지가 충돌하고 빈 화면이 표시되는 문제를 해결했습니다. (TGT-53087)
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

## [!DNL Target Standard/Premium] 25.7.2(2025년 7월 18일)

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 이 릴리스에는 다음 수정 사항 및 업데이트가 포함되어 있습니다.

**활동**

+++세부 정보 보기
* 저장하지 않은 변경 내용으로 활동 편집을 취소할 때 확인 경고가 추가되었습니다. &quot;이 활동을 저장하시겠습니까? 저장하지 않으면 변경 내용이 모두 손실됩니다.&quot; 이 메시지는 우발적인 데이터 손실을 방지하는 데 도움이 됩니다. (TGT-52865)
* [!UICONTROL Priority]의 [!UICONTROL Goals & Settings] 슬라이더에 레거시 기능을 복원하여 고객이 레거시 UI에서 지원되는 대로 숫자 값을 직접 입력할 수 있도록 했습니다. (TGT-53185 및 TGT-53219)

+++

**대상자**

+++세부 정보 보기
* 사용자 지정 대상이 포함된 활동을 저장하거나 편집할 수 없는 문제가 해결되었습니다. 고객에게 오류 메시지 &quot;요청을 완료할 수 없습니다. 문제가 지속되면 [!DNL Adobe Client Care]에 문의하십시오.&quot; 특정 활동에 변경 사항을 저장하거나 변경 없이 저장하려고 할 때. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++세부 정보 보기
* 고객이 [!UICONTROL Goals & Settings] 페이지에서 특정 활동에 대한 보고서를 볼 때 [!UICONTROL View in Analytics] 링크가 프로덕션 환경 대신 QA 환경을 잘못 가리키는 문제가 해결되었습니다. (TGT-53163)

+++

**[!UICONTROL Experiences]및[!UICONTROL Offers]**

+++세부 정보 보기
* 사용자 지정 코드를 통해 `triggerView`을(를) 호출하면 무한 루프가 발생하는 문제가 해결되었습니다. (TGT-52885)
* 활동에 대해 정의된 `LocalIds`과(와) 경험 정의에 사용된 `LocalIds` 간에 불일치가 발생하는 문제가 해결되었습니다. (TGT-52669)
* [!UICONTROL Overview] 활동 페이지에서 지표 이름이 누락되고 올바른 지표 이름 대신 &#39;오퍼&#39;만 표시되는 문제가 해결되었습니다. (TGT-53054)

+++

**양식 기반 경험 작성기**

+++세부 정보 보기
* 활동이 저장되지 않고 오류 메시지를 트리거하는 [!UICONTROL Form-Based Experience Composer]의 문제를 해결했습니다. &quot;정의되지 않은 속성을 읽을 수 없습니다(&#39;맵&#39; 읽기)&quot;. (TGT-53145)

+++

**추천**

+++세부 정보 보기
* [!UICONTROL Catalog Search]에서 제품을 클릭하면 &#39;제품 세부 정보를 검색하지 못했습니다&#39;라는 오류가 표시되고 닫기 옵션 없이 모달이 열리는 문제가 해결되었습니다. (TGT-53082)
* 컬렉션이나 프로모션을 변경할 때 [ 활동의 ](/help/main/c-recommendations/recommendations-as-an-offer.md)오퍼로서의 권장 사항[!UICONTROL A/B Test]이 올바르게 업데이트되지 않는 문제를 해결했습니다. (TGT-52884)
* 업데이트된 UI에서 엔티티를 클릭하면 다음과 같은 오류가 표시되는 프로덕션 환경의 문제가 해결되었습니다. &quot;제품 세부 정보를 검색하지 못했습니다. 이 문제가 지속되면 [!DNL Adobe Client Care]에 문의하십시오.&quot; (TGT-53071)

+++

**보고서**

+++세부 정보 보기
* 주문 세부 사항을 CSV 파일로 저장하면 빈 파일이 발생하는 문제가 해결되었습니다. (TGT-52225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++세부 정보 보기
* 여러 경험에 사용된 선택기가 선택된 상태로 일관되게 강조 표시되지 않던 [!UICONTROL Goals & Settings] 페이지의 문제를 해결했습니다. (TGT-53062)
* 활동 편집을 할 수 없고 다음과 같은 오류 메시지가 트리거되는 문제를 해결했습니다. &quot;정의되지 않은 속성을 읽을 수 없습니다(&#39;맵&#39; 읽기).&quot; (TGT-53161)

+++

**작업 공간**

+++세부 정보 보기
* 작업 영역을 전환할 때 임시 오퍼를 보다 효율적으로 처리할 수 있습니다.
   * 기본 작업 영역에서 기본값이 아닌 작업 영역으로(또는 기본값이 아닌 작업 영역 사이에서) 전환할 때 이제 임시 오퍼가 올바르게 복사됩니다. 초기화 중에 작업 공간 컨텍스트가 업데이트되고 고유성을 보장하기 위해 새 ID가 오퍼에 할당됩니다.
   * 동일한 작업 영역 내에 있을 때는 변경 사항이 발생하지 않습니다. (TGT-53079)
* 고객이 [다른 작업 영역 간에 활동을 복사할 수 없도록](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6)하는 문제가 해결되었습니다. (TGT-52753 및 TGT-47094)
* 작업 영역 간 속성을 변경할 때 발생하는 문제를 해결했습니다.
   * 기본 작업 영역을 기본이 아닌 작업 영역으로 전환할 때 현재 속성이 대상 작업 영역에 있으면 속성이 유지됩니다.
   * [!UICONTROL Properties] 목록에 경고가 표시되고(일부 속성이 호환되지 않을 수 있음을 나타낼 수 있음) 고객이 [!UICONTROL Add] 또는 [!UICONTROL Remove]을(를) 클릭한 다음 [!UICONTROL Save]을(를) 클릭하면 대상 작업 영역에 없는 모든 속성이 제거됩니다. 고객이 [!UICONTROL Cancel]을(를) 클릭하면 대상 작업 영역에 없는 경우에도 모든 속성이 유지됩니다. (TGT-47094)
   * 동일한 작업공간에 있거나 기본이 아닌 작업공간에서 기본 또는 다른 작업공간으로 전환하는 경우 모든 것이 그대로 유지됩니다. (TGT-53078)
* 활동의 원래 작업 영역 컨텍스트를 준수하도록 엔티티 유효성 검사 논리를 업데이트했습니다. [!UICONTROL Experience Fragments]&#x200B;(XF)과 같은 엔터티는 이제 활동이 원래 만들어진 작업 영역을 기반으로 유효성이 검사됩니다. 예를 들어, 기본 작업공간에 XF가 존재하고 활동이 작업공간 X에서 작업공간 Y로 복사되는 경우 원본(기본) 작업공간에서 XF가 유효한 한 유효성 검사가 계속 진행됩니다. (TGT-53196)
* 활동을 복제하는 동안 임시 대상 복사에 대한 지원이 개선되었습니다.
   * 지표, 보고, 페이지 및 활동 전용 유형을 포함한 임시 대상은 이제 다음 시나리오에서 자동으로 복사됩니다.
      * 기본 작업 영역에서 기본이 아닌 작업 영역으로 활동을 복사할 경우.
      * 동일한 작업 영역 내에서 활동을 복사할 때. (TGT-53197)

+++

## [!DNL Target Standard/Premium] 25.7.1(2025년 7월 11일)

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 이 릴리스에는 다음 수정 사항 및 업데이트가 포함되어 있습니다.

**활동**

+++세부 정보 보기
* [!UICONTROL Activity QA] URL에 불필요한 쿼리 매개 변수가 포함된 문제가 해결되었습니다. `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* 미리보기 URL이 사용자가 명시적으로 입력한 대상 이외의 추가 대상을 잘못 포함하던 문제를 수정했습니다. QA 또는 미리 보기 링크를 생성할 때 지정된 대상만 적용되도록 이 동작이 수정되었습니다. (TGT-52912)
* 트래픽 할당을 설정하는 동안 [!UICONTROL Auto-Target]&#x200B;(AA)를 먼저 선택한 경우 사용자가 [!UICONTROL Auto-Allocate]&#x200B;(AT) 활동을 만들 수 없는 문제를 해결했습니다. 이 문제로 인해 백엔드 유효성 검사 오류가 발생하고 활동이 저장되지 않습니다. (TGT-53096)

+++

**대상자**

+++세부 정보 보기
* [!UICONTROL Approver] 역할을 가진 사용자가 활동 전용 대상 세분화를 추가하거나 저장할 수 없는 문제를 해결했습니다. 사용자에게 활동을 승인하고 관리할 권한이 충분함에도 불구하고 &quot;[editor]&quot; 권한이 필요함을 알리는 403 금지된 오류가 발생했습니다. (TGT-52984)
* [!UICONTROL Remove Audience Refinement] 옵션을 사용하여 활동별 대상을 제거하면 동일한 활동 내에서 다시 선택할 수 있도록 대상이 대상 목록에 더 이상 표시되지 않는 문제가 해결되었습니다. 이 비헤이비어는 사용자가 동일한 대상자를 처음부터 다시 만들지 않는 한 다시 추가하지 못하도록 했습니다. (TGT-52979)
* 활동이 저장되기 전이라도 위치에서 제거된 후 바로 UI에서 활동 전용 대상 세분화가 사라지는 문제를 해결했습니다. 이 동작은 예상 기능 및 도구 설명 지침과 모순됩니다. 이 지침에는 &quot;활동이 저장되면 이 라이브러리에서 사용되지 않은 모든 대상이 삭제됩니다.&quot;가 표시됩니다. (TGT-52982)
* [!UICONTROL All Visitors] 이외의 대상을 활동에 할당하려고 할 때 발생하는 문제를 해결했습니다. 저장하면 다음과 같은 오류 메시지가 표시됩니다. &quot;요청을 완료할 수 없습니다. 문제가 지속되면 [!UICONTROL Adobe Client Care]에 문의하십시오.&quot; (TGT-53008)
* 활동 편집기 내에서 새 대상을 만들고 할당한 후 활동 저장을 차단하는 문제를 해결했습니다. 표시되는 오류 메시지: &quot;요청을 완료할 수 없습니다. 문제가 지속되면 [!UICONTROL Adobe Client Care]에 문의하십시오.&quot; (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++세부 정보 보기
* 기존 활동을 복사하고 보고 소스를 [!DNL Adobe Analytics]&#x200B;(A4T)으로 변경하면 &quot;잘못된 사용자 입력&quot; 오류가 발생하는 문제를 해결했습니다. [!DNL Analytics], `restart_same_experience` 및 `restart_random_experience`과(와) 같이 `restart_new_experience` 보고와 호환되지 않는 특정 지표 작업이 원래 활동에서 유지된 경우 오류가 트리거되었습니다. (TGT-52900)
* [!DNL Adobe Analytics] 단계에서 [!UICONTROL Goals & Settings]&#x200B;(A4T)을(를) 보고 소스로 선택할 때 고객이 활동을 만들거나 저장할 수 없도록 하는 문제를 해결했습니다. 특히 [!UICONTROL Custom Event] 지표(예: &quot;사용자 지정 이벤트 16&quot;)를 선택할 때 문제가 발생하여 다음 오류가 발생했습니다. &quot;잘못된 사용자 입력&quot; (TGT-52910)
* &quot;[!UICONTROL View in Analytics]&quot; 링크를 클릭하면 의도한 [!DNL Analytics] 대시보드가 아닌 홈 페이지로 리디렉션되는 문제가 해결되었습니다. (TGT-53092 및 TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* [!DNL Recommendations]&#x200B;(A4T)을(를) 보고 소스로 선택하면 업데이트된 [!UICONTROL Overview] UI에서 [!UICONTROL Goals & Settings] 활동을 볼 때 [!DNL Adobe Analytics] 섹션이 로드되지 않는 문제를 해결했습니다. 다음 오류 메시지가 표시되었습니다. &quot;문제가 발생했습니다. 요청을 완료할 수 없습니다. 문제가 지속되면 Adobe 클라이언트 지원 센터에 문의하십시오.”라는 오류 메시지가 표시됩니다. (TGT-52999)

+++

**[!UICONTROL Experiences]및[!UICONTROL Offers]**

+++세부 정보 보기
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* 모든 콘텐츠 옵션이 제거된 후 [!UICONTROL Manage Content] 기능이 위치 상태를 제대로 확인하지 못하는 문제를 해결했습니다. 이 문제로 인해 활동 구성을 저장하거나 진행하려고 할 때 일관되지 않은 동작이나 오류가 발생할 수 있습니다. (TGT-52801)
* 새 페이지를 추가하고 다른 경험 내에서 특정 요소를 삭제할 때 사용자에게 &quot;잘못된 입력&quot; 오류가 발생하는 문제를 해결했습니다. 이 오류는 요소 조작 중, 특히 경험 간에 전환하고 공유 페이지 구조를 수정할 때 중복 `LocalIds`이(가) 발생하여 트리거됩니다. (TGT-52720)
* [!UICONTROL Generate Adhoc Offer] 기능을 사용하면 정의되지 않은 위치가 [!UICONTROL Manage Content] 패널에 표시되는 문제가 해결되었습니다. (TGT-53076 및 TGT-53070)
* [!UICONTROL Targeting]에서 [!UICONTROL Experiences]&#x200B;(으)로 다시 이동할 때 HTML 오퍼를 사용하여 수정한 내용이 누락된 것으로 표시되는 고객의 동작을 명확히 했습니다. 이 고객의 경우 영향을 받는 웹 사이트에서 각 페이지 로드와 함께 변경된 여러 DOM 선택기를 동적으로 생성했습니다. 따라서 편집기를 다시 열 때 원래 수정에 사용된 선택기를 찾을 수 없으므로 수정 사항이 누락되거나 유효하지 않은 것으로 표시됩니다. 이 시나리오는 설계된 대로 작동합니다. 수정 사항이 편집기에서 시각적으로 지속되도록 하려면 클라이언트가 페이지 다시 로드 간에 변경되지 않는 안정적이고 일관된 선택기를 사용하는 것이 좋습니다. (TGT-52874)
* 제외된 경험의 일부인 오퍼를 삭제하거나 비활성화하려고 할 때 &quot;잘못된 사용자 입력&quot; 오류가 트리거되는 문제를 해결했습니다. 이 문제는 오퍼가 포함된 경험에서 활발하게 사용되지 않았음에도 불구하고 발생했습니다. (TGT-52917)

+++

**양식 기반 경험 작성기**

+++세부 정보 보기
* 경험을 복제하고 복제된 경험 중 하나에서 사용자 지정 코드를 편집하면 의도하지 않게 이러한 변경 사항이 모든 복제된 경험에 적용되는 양식 기반 활동의 문제를 해결했습니다. 이제 각 경험은 복제 후 독립적으로 자체 사용자 지정 코드를 유지합니다. (TGT-51600)

+++

**로컬라이제이션**

+++세부 정보 보기
* 프랑스어(fr_FR), 독일어(de_DE), 이탈리아어(it_IT), 한국어(ko_KO) 및 중국어 간체(zh_CN)에 대한 새 UI의 현지화 문자열이 업데이트되었습니다.

+++

**[!DNL Recommendations]**

+++세부 정보 보기
* 새 [!DNL Recommendations] 피드를 추가했습니다. [상태](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* [!DNL Recommendations]과(와) 함께 [!UICONTROL promotions]을(를) 추가할 때 활동 만들기 워크플로에 영향을 주는 문제를 해결했습니다. 사용자가 &quot;[!UICONTROL Promote by Attribute]&quot;을(를) 선택하고 필터링 규칙을 추가한 경우(예: [!UICONTROL Parameter Matching]) 활동을 저장하고 다시 편집한 후 선택한 규칙 유형 및 피연산자 값이 유지되지 않았습니다. 다시 열면 필터링 규칙 유형이 예기치 않게 변경되고 피연산자 값이 누락됩니다. (TGT-53059)
* 단일 규칙으로 만든 프로모션이 규칙의 논리에 관계없이 &quot;항목 목록&quot; 프로모션 유형으로 잘못 해석되어 표시되는 [!DNL Recommendations] UI의 문제가 해결되었습니다. (TGT-53063)
* 업데이트된 [!UICONTROL Overview]UI를 사용할 때 [!UICONTROL Download Recommendations Data]을(를) 포함하는 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에 대해 &quot;[!DNL Recommendations]&quot; 단추가 누락되는 문제를 해결했습니다. (TGT-52730 및 TGT-52756)
* 이전에는 피드에서 성공적으로 가져온 엔티티 수만 권장 사항 UI에 표시되었습니다. 그러나 백 엔드 메시지 형식에는 가져온 엔터티 수와 `# of entities imported / # of total entities` 형식의 총 엔터티 수가 모두 포함됩니다. 이러한 불일치로 인해 사용자는 UI에서 첫 번째 값(가져온 개수)만 볼 수 있었고, 이로 인해 혼동이 발생했습니다. 이제 UI에 두 숫자가 모두 표시됩니다. (TGT-53073)
* 추천이 있는 양식 기반 A/B 활동에서 &quot;[!UICONTROL Promote by attribute]&quot; 프로모션을 구성할 때 고객이 필터링 규칙을 저장할 수 없는 문제를 해결했습니다. 활동을 저장하고 다시 연 후 필터링 규칙이 누락되어 활동을 저장할 수 없습니다. (TGT-53057)

+++

**보고서**

+++세부 정보 보기
* [!UICONTROL Export order details to CSV] 페이지에서 &quot;[!UICONTROL Reports]&quot;을(를) 선택하면 다운로드되는 빈 파일이 발생하는 문제가 해결되었습니다. 이 문제는 활동에 유효한 주문 데이터가 있는 경우에도 발생했습니다. (TGT-52225)
* 새 보고 대상을 만들고 할당한 후 활동을 저장하려고 할 때 발생하는 문제를 해결했습니다. 반환된 오류 메시지: &quot;액세스 거부됨. 이 작업을 수행하려면 [editor] 권한이 모두 필요합니다.&quot; 이 문제는 사용자가 승인자 수준 액세스 권한을 가지고 있음에도 불구하고 발생했습니다. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++세부 정보 보기
* 보기에 수정 사항을 적용하면 보기가 복제되고 활동이 &quot;잘못된 사용자 입력&quot; 오류를 반환하는 문제를 해결했습니다. 이 수정 사항은 중복 또는 유효성 검사 오류를 트리거하지 않고 보기 수정 사항이 올바르게 적용되도록 합니다. (TGT-52886)
* 사용자 지정 코드 수정 사항이 잘못된 경험에 대해 잘못 표시되던 문제를 수정했습니다. 구체적으로, 한 경험을 위해 의도된 변경 사항이 다른 경험에서 나타나, 라이브 활동의 혼란과 잠재적인 오구성을 초래했다. (TGT-52776)
* 새 VEC UI에서 사용자 지정 코드 수정 사항을 편집하거나 저장할 수 없는 문제를 해결했습니다. 특히:

   * 사용자 지정 코드 블록을 편집하고 저장한 후 변경 사항이 UI나 QA 미리 보기에 반영되지 않았습니다.
   * 경우에 따라 활동을 닫고 다시 열지 않으면 수정 사항을 삭제할 수 없습니다.
   * 해결 방법으로, 사용자는 코드를 복사하고 수정 사항을 삭제한 다음 업데이트된 콘텐츠로 수동으로 다시 만들어야 했습니다. (TGT-53072)

* 사용자 지정 코드를 편집하고 저장하면 [!UICONTROL Modifications] 패널이 응답하지 않는 문제를 해결했습니다. (TGT-53075)
* 변형 경험에서 사용자 지정 코드에 대한 수정 사항이 의도하지 않게 [!UICONTROL Control] 경험에 반영되던 문제를 수정했습니다. 이로 인해 게재 동작이 의도하지 않게 변경되었습니다. 이제 [!UICONTROL Control] 경험은 다른 경험에 대한 사용자 지정 코드 편집에서 격리된 상태로 유지됩니다. (TGT-52413)
* 편집기가 완전히 로드되기 전에 사용자가 두 번째 경험을 클릭한 경우 한 경험(예: 경험 B)에 대한 수정 사항이 의도하지 않게 다른 경험(경험 A)에 복제되는 문제가 해결되었습니다. 처음 선택한 경험에 변경 사항이 없는 경우 이 동작으로 인해 수정 사항이 손실될 수도 있습니다. (TGT-52597)
* 활동 만들기 [!UICONTROL Modifications] 단계의 변경 내용이 일관되게 저장되지 않던 문제를 수정했습니다. 경우에 따라 모든 단계를 완료하고 [!UICONTROL Save]을(를) 클릭하면 저장 프로세스 중에 표시되는 오류가 없더라도 [!UICONTROL Modifications] 섹션에 추가된 사용자 지정 스크립트가 라이브 사이트에서 반영되지 않습니다. (TGT-52661)
* 사용자 지정 코드 변경 사항이 올바르게 저장되지 않고 동일한 활동 내의 여러 경험에 의도하지 않게 미러링되는 문제가 수정되었습니다. 또한 특정 활동을 열거나 새로 고칠 때 액세스 문제가 발생하여 화면이 비어 있습니다. 이제 안정적인 활동 편집과 정확한 경험 격리를 위해 이러한 문제가 해결되었습니다. (TGT-52594)
* 사용자가 [!UICONTROL Browse Mode]에서 다른 URL을 탐색할 수 없는 문제를 해결했습니다. 이렇게 하면 테스터와 편집자가 동일한 활동 세션 내에서 대체 페이지를 확인하거나 미리 볼 수 없습니다. (TGT-53052)
* 활동을 만드는 동안 여러 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 인스턴스가 동시에 열리는 문제를 해결했습니다. 이 문제는 사용자가 [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC)을(를) 사용하지 않도록 설정하고 [!UICONTROL Page Delivery] 단계에서 웹 사이트 URL에서 슬래시를 제거할 때 발생했습니다. (TGT-52782)
* 사용자가 다른 지표를 선택한 후에도 [!UICONTROL Revenue] 단계의 [!UICONTROL Goals & Settings] 지표 드롭다운이 [!UICONTROL Revenue per Visit]&#x200B;(RPVISIT)으로 잘못 설정되던 문제를 수정했습니다.  지표 구성 패널을 축소하고 다시 확장할 때 문제가 발생하여 이전에 선택한 값이 재설정되었습니다. (TGT-52811 및 TGT-52878)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Multivariate Testing]&#x200B;(MVT) 활동의 오퍼 이름 지정 및 콘텐츠 변환과 관련된 활동 만들기 워크플로의 몇 가지 문제를 해결했습니다.

  해결된 주요 문제:

   * 이름이 같은 여러 HTML 오퍼를 만들면(예: &quot;경험&quot;) &quot;중복된 오퍼 이름은 허용되지 않습니다&quot; 오류가 발생했지만 UI에서 충돌을 일으키는 오퍼를 명확하게 표시하지 않았습니다.
   * 오른쪽 패널을 통해 오퍼의 이름을 바꾸면 UI에서 이름이 업데이트되었지만 변경 내용이 [!UICONTROL Manage Content] 탭 또는 [!UICONTROL Offers] 탭에 반영되지 않아 지속적인 유효성 검사 오류가 발생했습니다.
   * MVT 활동에서는 이름을 바꾼 후에도 중복 이름 오류가 지속되지 않지만 UI는 탭 간에 업데이트된 오퍼 이름을 일관되게 반영하지 못했습니다. (TGT-52933)

+++

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 노트](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
