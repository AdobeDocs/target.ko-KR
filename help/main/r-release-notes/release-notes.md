---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 29ddf23b41531e5fab80fe7d0f6bc913e778d839
workflow-type: tm+mt
source-wordcount: '1670'
ht-degree: 15%

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

## [!DNL Target Standard/Premium] 25.9.1(2025년 9월 5일)

이번 릴리스에는 다음과 같은 업데이트 및 수정 사항이 포함되어 있습니다.

**[!UICONTROL Experience Fragments]**

+++세부 정보 보기
* **오퍼에 대한 [!UICONTROL AEM Experience Fragment]사용자 속성이 개선되었습니다.** [!UICONTROL Last updated]&#x200B;(XF)에 대한 &quot;[!UICONTROL AEM Experience Fragment]&quot; 필드에 사용자 이름 대신 코드 ID가 잘못 표시되는 VEC의 문제를 해결했습니다. 이 불일치는 업데이트된 UI에서 오퍼를 선택하는 동안 발생했으며, 이전 UI 및 HTML 오퍼와 일치하지 않습니다. 이 오퍼에는 마지막 편집기의 이름이 올바르게 표시됩니다. 이 수정 사항은 오퍼 유형 간에 일관된 사용자 속성을 보장하여 투명도를 높이고 예상 동작에 맞게 정렬합니다. (TGT-52880 및 TGT-52898)

+++

**Offer Decisioning**

+++세부 정보 보기
* ODE 오퍼에 대해 **오퍼 결정 오류가 해결되었습니다.**&#x200B;에서 [!DNL Target]을(를) 통해 삽입된 ODE(오퍼 결정 엔진) 오퍼가 형식 메타데이터 누락으로 인해 400 오류를 반환하는 문제를 해결했습니다. MIME 유형이 null임을 나타내는 오류 메시지가 표시되어 오퍼 결정을 성공적으로 처리할 수 없습니다. 이 수정 사항을 통해 오퍼 메타데이터를 적절하게 처리하고, 개인화된 콘텐츠 전달을 위한 기능을 복원하며, 마케팅 캠페인을 중단 없이 실행할 수 있습니다. (TGT-53635)
* **ODS 오퍼 렌더링 문제가 해결되었습니다.** 활동이 업데이트된 UI에서 VEC를 사용하여 만들어졌을 때 [!DNL Offer Decision Service]&#x200B;(AJO)을 통해 만들어진 [!DNL Adobe Journey Optimizer]&#x200B;(ODS) 오퍼가 렌더링되지 않는 문제를 해결했습니다. 동일한 구성이 레거시 UI에서 올바르게 작동하여 혼동이 발생하고 캠페인 실행이 차단되었습니다. 이 수정 사항은 두 UI 버전 모두에서 일관된 오퍼 전달을 보장하여 AJO 기반 개인화에 대한 예상 동작을 복원합니다.

+++

**보고서**

+++세부 정보 보기
* **업데이트된 보고서 개요 UI의 보고서 섹션에서 다운로드 옵션이 복원되었습니다.** 사용자가 특성 중요도 점수를 내보낼 수 없도록 보고서 섹션에 [!UICONTROL Download] 단추가 없는 새 개요 UI의 문제를 해결했습니다. 이 업데이트는 전체 내보내기 기능을 복원하여 분석 및 보고를 위한 다운로드 가능한 데이터에 대한 능률적인 액세스를 가능하게 합니다. (TGT-53222)
* **[!UICONTROL Download full CSV report]보기에서 [!UICONTROL Important attributes] 단추가 복원되었습니다.** 업데이트된 활동 만들기 UI에서 보고서 보기의 [!UICONTROL Download full CSV report] 섹션에 [!UICONTROL Important Attributes] 단추가 없는 문제를 해결했습니다. 이 수정 사항은 다운로드 가능한 통찰력에 대한 액세스를 복원하여 업데이트된 UI 및 이전 UI 모두에서 일관된 기능을 보장합니다. (TGT-53238)
* **업데이트된 개요 UI에서 [!UICONTROL Auto Target] 보고에 영향을 주는 UI 문제가 해결되었습니다.** [!UICONTROL Auto Target] 활동 보고에 영향을 주는 업데이트된 개요 인터페이스에서 여러 UI 문제를 해결했습니다. 이러한 수정 사항에는 다음이 포함됩니다.

   * 요약 보고서에 상승도 및 신뢰도 지표 누락
   * &quot;모델 작성&quot; 확인란의 잘못된 색상 표시기
   * [!DNL Analytics]의 데이터 분산에도 불구하고 작동하지 않는 그래프 보고서
   * [!UICONTROL Automated Segments] 및 [!UICONTROL Important Attributes] 보고서에 대한 다운로드 링크가 없습니다.
   * [!UICONTROL Automated Segments] 보고서 표시 중단

  이러한 수정 사항은 예상 보고 동작을 복원하고 업데이트된 UI에서 [!UICONTROL Auto Target] 성능에 대한 가시성을 향상시킵니다. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++세부 정보 보기
* 업데이트된 UI에서 **매개 변수 존재 조건에 대한 양식 유효성 검사가 수정되었습니다.** 업데이트된 UI에서 &quot;[!UICONTROL Custom mbox parameter value is present]&quot; 또는 &quot;[!UICONTROL Parameter is present]&quot;을(를) 선택하면 고객이 값을 입력해야 하는 문제가 해결되었습니다. 이 동작은 해당 값에 관계없이 매개 변수가 있는지 확인하는 의도한 논리와 충돌합니다. 이 수정 사항은 양식 유효성 검사를 예상 동작에 맞게 조정하므로 활동을 더욱 원활하게 설정하고 업데이트된 UI를 완전히 적용할 수 있도록 지원합니다. (TGT-53638)
* **페이지 게재에서 매개 변수 존재 규칙에 대한 양식 논리가 수정되었습니다.&quot;** 업데이트된 UI에서 &quot;[!UICONTROL Parameter is present]&quot;, &quot;[!UICONTROL Parameter is not present]&quot;,&quot;[!UICONTROL Parameter value is present]&quot; 또는 &quot;[!UICONTROL Parameter value is not present]&quot;과(와) 같은 페이지 전달 규칙을 선택하면 사용자가 추가 매개 변수 값을 입력해야 하는 문제가 해결되었습니다. 이 동작은 기존 UI와 일관되지 않으며 값을 지정하지 않고 매개 변수 존재를 감지하는 의도한 논리와 모순됩니다. 이 수정 사항은 예상되는 규칙 구성 동작을 복원하여 활동 설정을 간소화하고 유용성을 개선합니다. (TGT-53640)
* **업데이트된 UI에서 다중 페이지 규칙 빌더에 대한 유효성 검사 논리가 개선되었습니다.** 업데이트된 UI 내의 다중 페이지 규칙 빌더에서 여러 유효성 검사 문제가 해결되었습니다. 이러한 수정 사항에는 다음이 포함됩니다.

   * mbox 매개 변수가 비어 있을 때 규칙 만들기 방지
   * 잘못된 규칙 상태에 대한 적절한 오류 메시지 표시
   * 피연산자 값이 필요 없는 단항 및 매개 변수 기반 연산자에 대한 유효성 검사 논리 수정
   * 저장 기능을 복원하여 단항 연산자로 해시 조각 규칙 활성화

  이러한 업데이트는 정확한 규칙 구성을 보장하고 복잡한 페이지 전달 시나리오에서 유용성을 향상시킵니다. (TGT-53722)
* **A/B 및 MVT 활동에서 위치 이름 변경 문제가 해결되었습니다.** 위치 목록, 타깃팅 및 뒤로 탐색한 후 [!UICONTROL A/B Test] 또는 [!UICONTROL Multivariate Test]&#x200B;(MVT) 활동에서 위치 이름 변경이 지속되지 않는 업데이트된 UI의 버그를 수정했습니다. 이 업데이트를 통해 위치 이름 변경 사항이 저장되고 활동 워크플로우 전반에 지속적으로 반영됩니다. (TGT-52367)
* **업데이트된 UI에서 MVT 및 AP 활동에 대한 위치 이름 지속성이 수정되었습니다.** 업데이트된 UI에서 [!UICONTROL Multivariate Test]&#x200B;(MVT) 및 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 편집된 위치 이름이 올바르게 저장되지 않는 문제를 해결했습니다. 위치 이름을 바꾼 후 [!UICONTROL Targeting]과(와) [!UICONTROL Experiences] 등의 탭 사이를 탐색하면 이름이 이전 상태로 되돌아갑니다. 이 수정 사항으로 탭 간 일관된 위치 이름이 지정되며 활동 설정 중에 안정성이 향상됩니다. (TGT-52927)
* **MVT 활동에 대한 경험 관리 패널에서 위치 레이블이 수정되었습니다.** [!UICONTROL Manage Experiences]&#x200B;(MVT) 활동의 [!UICONTROL Multivariate Test] 패널에 일관되지 않은 위치 번호가 표시되는 업데이트된 UI의 문제를 해결했습니다. 이 수정 사항을 통해 위치 레이블이 사용자 정의 수정 사항과 올바르게 정렬되어 경험 설정 중 명확성과 유용성이 향상됩니다. (TGT-52929)

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
