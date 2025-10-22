---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7d73870275c266055825c2fce90489ef82825fca
workflow-type: tm+mt
source-wordcount: '1700'
ht-degree: 17%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 25.10.1(2025년 10월 22일)

이번 릴리스에는 다음과 같은 업데이트 및 수정 사항이 포함되어 있습니다.

**활동**

+++ 세부 정보 보기
* **업데이트된 UI에서 유용성 문제를 해결했습니다**. 이제 [!UICONTROL Observers]은(는) 레거시 UI에서와 마찬가지로 [!UICONTROL View Activity] 옵션을 사용하여 활동을 미리 볼 수 있습니다. (TGT-51741)
* 이제 **[!UICONTROL Observer]명의 사용자가 업데이트된 UI에서 활동 콘텐츠를 볼 수 있습니다.** 업데이트된 활동 UI에서 관찰자 역할 사용자의 가시성을 복원했습니다. 이전에는 관찰자가 수정 사항, 오퍼 및 콘텐츠 변경 사항(기존 UI에서 사용할 수 있었던 기능)을 볼 수 없었습니다. (TGT-53785)
* 이제 **[!UICONTROL Approver]명의 사용자가 편집기 권한 오류 없이 활동 목표를 편집할 수 있습니다.** 승인자 수준 사용자가 고급 목표 설정에 대한 변경 내용을 저장하지 못하도록 차단한 활동 만들기 UI의 권한 문제를 해결했습니다. 영향을 받는 사용자가 액세스 권한이 충분함에도 불구하고 편집기 권한이 필요한 `403 Forbidden.Resource` 오류를 받았습니다. (TGT-53819)

+++

**대상자**

+++세부 정보 보기
* **다중 대상 선택이 &quot;이 활동만&quot; 보고에서 복원되었습니다.** 사용자가 [!UICONTROL This activity only]의 [!UICONTROL Goals & Settings] 섹션 아래에서 여러 대상을 선택할 수 없는 활동 만들기 UI의 문제를 해결했습니다. (TGT-53283)
* **대상 기반 보고 그래프는 이제 전환 데이터를 올바르게 표시합니다.** 기본이 아닌 대상을 선택할 때 그래프가 실패하는 [!UICONTROL Reports] 탭의 문제를 해결했습니다. 데이터와 신뢰도 지표를 사용할 수 있는 반면 시각적 그래프는 실선만 보여 분석이 어려웠다. (TGT-53769)
* **이제 [!UICONTROL Targeting] UI에 제외된 대상 규칙이 명확하게 표시됩니다.** 활동 만들기 UI의 [!UICONTROL Targeting] 섹션에서 [!UICONTROL Exclude]&#x200B;(으)로 설정된 대상 규칙이 명확하게 표시되지 않는 문제를 해결했습니다. 이로 인해 타깃팅 논리, 특히 특정 URL을 제외한 대상에 대해 검토할 때 혼동이 발생했습니다. (TGT-53809)
* **이제 [!UICONTROL Targeting] 탭에서 대상 정의 값을 선택 및 복사할 수 있습니다.** 사용자가 [!UICONTROL Targeting] 탭에서 대상 규칙 값을 선택하고 복사할 수 없는 활동 만들기 인터페이스의 문제를 해결했습니다. 이 기능은 레거시 UI에서 사용할 수 있지만 업데이트된 UI에서는 없습니다. (TGT-53856)

+++

**로컬라이제이션**

+++세부 정보 보기
* **zh_CN 페이지 편집기 컨텍스트에서 &quot;quote&quot;의 오역을 수정했습니다.** &quot;quote&quot;라는 용어가 &quot;报价&quot;로 잘못 번역되어 상업용 가격 견적을 의미하는 zh_CN 로케일에서 상황별 번역 오류를 수정했습니다. 타이포그래피 > 제목 스타일 > 블록 인용 섹션에서 의도된 의미는 가격이 아닌 서식 요소(견적 블록)를 참조합니다. (TGT-53841)
* **zh_CN 페이지 편집기 컨텍스트에서 &quot;따옴표가 제거됨&quot;의 오역을 수정했습니다.** &quot;견적이 제거됨&quot;이 &quot;移除了报价&quot;로 잘못 렌더링되어 상업용 가격 견적을 의미하는 zh_CN 로케일의 번역 오류를 수정했습니다. 타이포그래피 > 제목 스타일 > 블록 견적 섹션에서 이 용어는 가격책정이 아닌 서식 요소(견적 블록)를 참조합니다. (TGT-53843)
* **zh_CN 페이지 편집기 컨텍스트에서 &quot;따옴표가 재배열됨&quot;의 오역이 수정되었습니다.** 상업용 가격 견적을 암시하는 &quot;견적이 재배열됨&quot;이 &quot;重新排列了报价&quot;로 잘못 번역된 zh_CN 로케일의 상황별 번역 오류를 수정했습니다. 타이포그래피 > 제목 스타일 > 블록 견적 섹션에서 이 용어는 가격책정이 아닌 서식 요소(견적 블록)를 참조합니다. (TGT-53844)
* **zh_CN 페이지 편집기 컨텍스트에서 &quot;따옴표 변경됨&quot;의 오역이 수정되었습니다.** &quot;quote changed&quot;가 &quot;更改了报价&quot;로 잘못 렌더링되는 zh_CN 로캘의 번역 오류를 수정하여 상업용 가격 견적을 제안했습니다. 타이포그래피 > 제목 스타일 > 블록 견적 섹션에서 이 용어는 가격책정이 아닌 서식 요소(견적 블록)를 참조합니다. (TGT-53845)

+++

**추천**

+++세부 정보 보기
* 권장 사항에 대한 **CSS 선택기 변경 사항이 올바르게 저장됩니다.** 사용자가 권장 사항 배치에 대한 CSS 선택기를 업데이트할 수 없는 활동 만들기 UI의 문제를 해결했습니다. 저장 후 변경 사항이 반환되어 타기팅 컨테이너에 대한 업데이트가 차단됩니다. (TGT-53835)
* **페이지 로드 이벤트 선택이 권장 사항 수정 시 유지됩니다.** 사용자가 권장 사항의 이벤트 유형을 [!UICONTROL View]에서 [!UICONTROL Page Load]&#x200B;(으)로 전환할 때 변경 사항을 저장하지 못하는 활동 만들기 UI의 문제를 해결했습니다. 선택이 성공한 것처럼 보였지만 다른 곳으로 이동한 후 되돌아가 활동 게시를 차단했습니다. (TGT-53957)

+++

**보고서**

+++세부 정보 보기
* **&quot;[!UICONTROL Export order details to CSV]&quot;이(가) 이제 전체 데이터를 다운로드합니다.** 올바른 보고서 데이터가 있어도 &quot;[!UICONTROL Overview]&quot; 옵션이 빈 파일을 다운로드하는 업데이트된 [!UICONTROL Export Order details to CSV] UI의 문제를 해결했습니다. (TGT-53787)

+++

**보안**

+++세부 정보 보기
* 조직 간 데이터 노출로부터 GQL 끝점을 보호하기 위해 **IMS 사전 필터가 추가되었습니다.** licenseGroups 및 targetProperties GraphQL 끝점에 영향을 주는 관리 탭의 보안 취약점이 해결되었습니다. 문제는 교차 조직 제품 데이터에 액세스하는 데 악용될 수 있는 관리 클라이언트 토큰과 함께 JIL API를 사용하는 것에서 비롯되었습니다. (TGT-53837)

+++

**VEC(시각적 경험 작성기)**

+++세부 정보 보기
* **Activity Create UI에서 작성 안정성이 복원되었습니다.** 작성에 실패하고 링크를 예기치 않게 클릭할 수 있게 되어 사용자를 페이지에서 멀리 리디렉션하는 VEC UI의 간헐적인 문제를 해결했습니다. (TGT-53153)
* **활동 만들기 UI에서 저장된 활동에 대한 편집이 복원되었습니다.** 수정 내용을 저장한 후 사용자가 활동을 편집할 수 없도록 하는 문제를 해결했습니다. 영향을 받는 활동이 &quot;[!UICONTROL Applying initial modifications]&quot;에서 중단된 상태로 유지되어 추가 업데이트가 차단되고 [!UICONTROL Cancel] 단추가 숨겨졌습니다. (TGT-53631)
* **VEC가 더 이상 &quot;[!UICONTROL Applying initial modifications]&quot;에서 중지되지 않습니다.** 수정 횟수가 많은 경험을 로드할 때 오래 지연되는 VEC의 성능 문제를 해결했습니다. 영향을 받는 사용자는 특히 경험 B 시나리오에서 몇 분 동안 &quot;[!UICONTROL Applying initial modifications]&quot;에서 UI가 중단된 것을 확인했습니다. (TGT-53727)
* **이제 VEC가 루트 요소 없이 수정 내용을 로드합니다.**
명확한 루트 요소가 부족한 수정 사항을 로드할 때 경험이 중단되는 VEC의 문제를 해결했습니다. 이러한 수정 사항으로 인해 이전에 &quot;A[!UICONTROL pplying initial modifications]&quot;에서 UI가 무기한 중단되었습니다. (TGT-53799)
* **이제 활동의 변경 내용을 저장하는 것이 예상대로 작동합니다.** 사용자가 활동의 목표 및 고급 설정을 편집할 때 변경 사항을 저장하지 못하게 하는 새 만들기 UI의 권한 관련 문제를 해결했습니다. 해당하는 사용자는 적절한 액세스 권한이 있음에도 불구하고 빨간색 오류 리본과 &quot;Forbidden.Resource&quot; 메시지를 표시했습니다. (TGT-53816)
* **VEC UI는 이제 보기 간에 수정된 환경을 유지합니다.** 업데이트된 VEC에서 경험 개발에 영향을 주는 여러 문제를 해결했습니다. 특히 HTML 오퍼를 사용하거나 보기 간에 전환할 때 수정 사항이 올바르게 지속되지 않았습니다. (TGT-53825)
* **수정 사항이 여러 경험에 걸쳐 적용되면 이제 모든 보기가 올바르게 표시됩니다.** 수정 사항이 여러 보기에 걸쳐 적용되었을 때 하나의 보기만 표시되는 활동 만들기 UI의 문제를 해결했습니다. 수정이 올바르게 적용되었는데도 마우스로 가리키면 연결된 보기가 모두 나열되지 않습니다. (TGT-53827)
* **VEC가 더 이상 &quot;[!UICONTROL Applying initial modifications]&quot;에서 간헐적으로 중지되지 않습니다.** 경험을 로드하지 못하고 &quot;[!UICONTROL Applying initial modifications]&quot;에서 중단된 VEC의 간헐적인 문제를 해결했습니다. 이 동작은 일관되지 않았으며 경우에 따라 리디렉션 루프 또는 필요한 수동 캐시 지우기가 트리거되기도 했습니다. (TGT-53916)
* **VEC 로드 문제를 재현할 수 없습니다.** 기존 활동을 편집할 때 VEC가 &quot;[!UICONTROL Applying initial modifications]&quot;에 남아 있는 보고된 문제를 조사했습니다. 이 동작은 상위 요소가 없는 HTML 컨텐츠와 관련이 있는 것으로 의심되었습니다. 재발을 계속 모니터링하고 안정성을 보장하기 위해 HTML 오퍼에 대해 구조화된 컨테이너를 사용하는 것이 좋습니다. (TGT-53972)
* VEC의 **[!UICONTROL Design]모드가 더 이상 [!UICONTROL Browse] 모드처럼 간헐적으로 작동하지 않습니다.** UI에서 [!UICONTROL Design] 모드가 간헐적으로 [!UICONTROL Browse] 모드처럼 동작하여 클릭 가능한 `<a>` 링크를 허용하고 요소 선택을 방지하는 문제를 해결했습니다. 이로 인해 마우스로 가리키면 상자가 사라지고 수정 워크플로가 차단되었습니다. (TGT-53136)
* **모드에서 [!UICONTROL Composer]단추 클릭이 더 이상 페이지 리디렉션을 트리거하지 않습니다.** 업데이트된 VEC UI에서 [!UICONTROL Composer] 모드에서 단추를 클릭하면 단추의 대상 URL로 예기치 않은 리디렉션이 발생하는 문제를 해결했습니다. 이로 인해 사용자가 call-to-action(CTA) 요소를 편집할 수 없고 작성 워크플로우가 중단되었습니다. (TGT-53137)
* **이제 자동화된 개인화 활동의 오퍼 코드 업데이트가 오류 없이 저장됩니다.** [!UICONTROL Invalid user input] 활동에서 오퍼 코드를 업데이트할 때 &quot;[!UICONTROL Automated Personalization]&quot; 오류가 발생하는 새 만들기 UI의 문제를 해결했습니다. 이 오류로 인해 입력이 유효한 경우에도 사용자가 변경 사항을 저장할 수 없습니다. (TGT-53586)
* 이제 VEC의 **[!UICONTROL Design]모드에서 편집 가능한 구성 요소에 대한 링크 탐색을 차단합니다.** [!UICONTROL Design] 모드에 있는 동안에도 클릭 가능한 요소(예: 단추 및 링크)가 페이지 리디렉션을 트리거한 업데이트된 VEC의 문제를 해결했습니다. 이 동작은 [!UICONTROL Browse] 모드를 모방했으며 사용자가 주요 구성 요소를 수정할 수 없습니다. (TGT-53696)
* 이제 **&quot;[!UICONTROL Clicked an element]&quot; 지표가 리디렉션 또는 오류 없이 작동합니다.** &quot;[!UICONTROL Clicked an element]&quot; 전환 지표를 선택할 때 예기치 않은 리디렉션 및 빈 화면이 발생하는 새 만들기 UI의 문제를 해결했습니다. 설치 중에 단추를 클릭하면 요소를 등록하는 대신 탐색이 트리거되어 &quot;[!UICONTROL element not found]&quot; 오류가 발생합니다. (TGT-53817)
* **편집하는 동안 기존 활동이 무한한 로드 루프에 더 이상 걸리지 않습니다.** VEC에서 기존 활동을 편집하면 페이지가 무한 로드 루프에 남아 있는 새 만들기 UI의 문제를 해결했습니다. 이 문제는 새로 만든 활동에는 영향을 주지 않았으며 페이지의 기존 수정 사항에 의해 트리거되었습니다. (TGT-53913)
* **수정 사항이 있는 기존 활동 페이지가 VEC에 올바르게 로드됩니다.** 저장된 수정 사항으로 기존 활동을 편집할 때 페이지가 로드 단계에서 계속 남아 있는 업데이트된 VEC의 문제를 해결했습니다. 새 활동이 문제 없이 로드되었지만 이전에 구성된 활동이 렌더링되지 않았습니다. (TGT-53967)

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
