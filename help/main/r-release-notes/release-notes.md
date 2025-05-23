---
keywords: 릴리스 노트;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트,현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0d7ae6e269211b1c0beea346f527d28c8765f8c3
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 21%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## Target UI 버전 전환 중단(2025년 5월 23일) {#toggle}

새 [!DNL Target] 사용자 인터페이스의 롤아웃이 **2025년 5월 27일**&#x200B;까지 완료됩니다. 이 시점에서 모든 고객은 최신 UI 버전에 액세스할 수 있습니다.

**2025년 6월 22일**&#x200B;부터 UI 버전 토글이 제거됩니다. 모든 사용자는 이전 버전으로 되돌릴 옵션 없이 새 인터페이스로 영구적으로 전환됩니다.

**UI 버전 전환에 대한 중요 정보**

토글 단추를 사용하여 업데이트된 [!DNL Target] UI와 레거시 버전 간을 전환할 수 있는 임시 기능을 제공하고 있습니다. 이 옵션은 UI 롤아웃의 마지막 단계 동안에만 사용할 수 있습니다.

![Target UI 버전 전환](/help/main/r-release-notes/assets/toggle.png)

롤아웃이 완료되면 토글이 제거되고 모든 사용자가 **2025년 6월 22일**&#x200B;에 업데이트된 UI로 영구적으로 전환됩니다. Adobe에서는 이 기능이 곧 단계적으로 중단되므로 미리 계획을 수립하는 것이 좋습니다.

**UI 전환 동작 제한**

* **새 활동의 가시성**: 기존 UI로 다시 전환하면 업데이트된 UI에서 만들어진 활동이 표시되지 않습니다.
* **기존 활동 편집**: 업데이트된 UI를 사용하는 동안 기존 활동(원래 기존 UI에서 만들어짐)에 대한 변경 사항이 웹 사이트에 게시됩니다. 그러나 다시 전환하는 경우 이러한 업데이트가 이전 UI에 표시되지 않습니다. 이전 UI에서 마지막으로 수행한 업데이트만 표시됩니다.
* **활동 세부 정보의 일관성**: 사용하는 UI에 관계없이 가장 최근의 변경 내용이 라이브 웹 사이트에 반영됩니다. 하지만 기존 UI에는 해당 버전 내에서 변경된 최신 변경 사항만 표시됩니다. 업데이트된 UI에서 편집된 활동이 기존 UI에 표시되는 것과 다른 경우 혼동을 일으킬 수 있습니다.

업데이트된 UI에 대한 자세한 내용은 다음 리소스를 참조하십시오.

* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2)
* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1)
* [[!UICONTROL Visual Experience Composer]개 변경](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
* [[!UICONTROL Visual Experience Composer] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

## [!DNL Target Standard/Premium] 25.5.3(2025년 5월 22일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* [!UICONTROL Activities] 목록의 이름별 검색 기능이 다중 단어 쿼리에서 올바르게 작동하지 않는 문제를 해결했습니다. (TGT-52529)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 경험을 제외하지 못하는 문제를 해결했습니다. (TGT-52383)
* AP 활동에서 콘텐츠를 관리할 때 [!UICONTROL Filter Rules]에서 &quot;[!UICONTROL Contains]&quot; 옵션이 누락되는 문제를 해결했습니다. (TGT-52384)
* [!DNL Target]의 내부 시스템에서 `optionLocalId` 값을 사용하여 기본 오퍼를 추적하고 보고하는 방법과 관련된 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동의 보고 불일치를 수정했습니다.
* QA 링크가 의도한 활동 경험을 전달하지 못하는 문제를 해결했습니다. (TGT-52163)
* [!UICONTROL Approver] 권한이 있는 사용자가 라이브 활동을 편집할 수 없도록 잘못 차단되어 &quot;액세스 거부됨&quot; 오류 메시지가 표시되는 문제를 해결했습니다. (TGT-52416)
* 업데이트된 [!DNL Target] UI의 특정 활동에 대해 대상 세분화가 표시되지 않는 문제가 해결되었습니다. (TGT-52057)
* 업데이트된 UI에서 대상 세분화 및 활동 대상이 반전되는 문제가 해결되었습니다. (TGT-52158)
* 임시 오퍼를 생성하여 오퍼가 중복되던 문제를 수정했습니다. (TGT-51938)
* 오퍼 업데이트를 차단하고 &quot;잘못된 사용자&quot; 오류를 잘못 표시하는 문제를 해결했습니다. (TGT-52361)
* 기존 활동을 저장할 수 없어 &quot;잘못된 사용자 입력&quot; 오류가 발생하는 문제를 해결했습니다. (TGT-52422)
* 코드를 변경하지 않은 경우에도 기존 HTML 오퍼 편집을 차단하여 저장 시 &quot;잘못된 사용자 입력&quot; 오류를 트리거하는 문제를 해결했습니다. (TGT-52351)
* [!DNL Target]이(가) 웹 사이트 URL에서 &quot;#&quot; 문자를 인식하지 못하게 하는 문제를 해결했습니다. (TGT-52093)
* [!DNL Recommendations] 활동을 편집하여 프로모션을 추가하거나 업데이트하지 못했으며, 이로 인해 저장 실패 및 프로모션 중복이 발생하는 문제를 해결했습니다. (TGT-52343)
* [!DNL Recommendations] 활동에서 기준이나 디자인을 변경할 수 없어 &quot;잘못된 JSON: 인식할 수 없는 속성 이름&quot; 오류가 발생하는 문제를 해결했습니다. (TGT-52375)
* [!DNL Recommendations] 활동에 대한 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 시퀀스 기준이 올바르게 표시되지 않는 문제가 수정되었습니다. (TGT-52435)
* [!DNL Adobe Experience Platform Web SDK]을(를) 사용할 때 SPA 페이지에서 보기가 올바르게 식별되지 않는 문제를 해결했습니다. (TGT-52106)
* 일괄 처리 작업 페이로드에 포함되더라도 ODS(온디바이스 의사 결정) 세부 사항이 올바르게 저장되지 않는 문제가 해결되었습니다. (TGT-52406)
* 편집 중에 읽고 업데이트할 수 있는 `audienceMetadata` 필드를 활동에 추가했습니다. (TGT-51004)
* 대상 기간이 잘못된 경우 사용자에게 경고하는 오류 메시지가 추가되었습니다. (TGT52522)
* 유형이 다른 중복 대상을 지원하도록 활동 구조가 업데이트되었습니다. (TGT-51200)

## [!DNL Adobe Target] [!DNL AI Assistant] 릴리스(2025년 5월 16일)

[!DNL Adobe Target]에 [!DNL AI Assistant]의 시작을 알려드리겠습니다! 이 강력한 사용자 인터페이스 기능은 [!DNL Target] 개념을 쉽게 탐색하고 이해할 수 있도록 설계되었습니다. [!DNL Target]을(를) 포함하여 [!DNL Adobe Experience Cloud]의 여러 제품에서 사용할 수 있습니다. [!DNL AI Assistant]이(가) 사용자의 경험을 혁신하기 위해 여기에 있습니다.

[!UICONTROL Target]의 [!DNL AI Assistant]은(는) [!DNL Experience Platform]개의 응용 프로그램 및 서비스를 통해 워크플로를 가속화하는 데 사용할 수 있는 대화 도구입니다. [!DNL AI Assistant]을(를) 사용하여 전반적인 생산성을 높이고 제품 지식을 이해합니다.

[!DNL Target]에서 [!DNL AI Assistant]의 첫 번째 단계는 [!DNL Experience League] 설명서에 기반을 둔 중요한 제품 지식을 제공합니다. 프로필 스크립트를 설정하든, 오류를 해결하든 아니면 AEP Web SDK으로 업그레이드하든 관계없이 [!DNL AI Assistant]에서 다루었습니다.

자세한 내용은 [Adobe Experience Platform AI Assistant 개요](/help/main/c-intro/ai-assistant.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 25.5.2(2025년 5월 8일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* [!UICONTROL Product Administrator] 및 [!UICONTROL System Administrator] 권한이 있는 [!DNL Target] 사용자는 이제 [!DNL Target]의 역할에 관계없이 [!UICONTROL Administration] 페이지의 모든 설정을 편집할 수 있습니다. 이러한 권한이 없는 사용자는 이러한 설정에 대해 읽기 전용 액세스 권한을 갖습니다. 이 업데이트는 [관리 설정](/help/main/administrating-target/administrating-target.md)에 대한 액세스 제어를 강화합니다. (TGT-48179)
* [사이트 환경 설정](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) 활동을 저장할 수 없는 캐싱 문제를 해결했습니다. (TGT-52213)
* 고객이 VEC에서 사이트를 로드한 후 [!UICONTROL Site Preferences] 섹션에서 ID 및 클래스별로 선택을 활성화할 수 없는 문제를 해결했습니다. [!UICONTROL Site Preferences] 설정을 사용하도록 설정한 후에도 사용하지 않도록 자동으로 되돌렸습니다. (TGT-52207)
* [페이지 배달](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) URL이 슬래시(/)로 끝났을 때 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)이 올바른 페이지를 표시하지 못하는 문제를 해결했습니다. (TGT-52237)
* 경험을 변경할 때 사용자 지정 코드 수정 사항을 제거할 수 없는 문제를 해결했습니다. (TGT-52240)
* VEC의 HTML 수정 사항이 기존 페이지 요소를 오버레이하는 문제를 해결했습니다. (TGT-52265)
* 기존 사용자 지정 코드가 편집기에 표시되지 않아서 업데이트된 VEC에서 사용자 지정 코드를 편집할 수 없는 문제가 해결되었습니다. (TGT-52272)
* Recommendations 활동을 저장할 때 &quot;중복 이름이 허용되지 않습니다&quot; 오류 메시지가 표시되는 문제를 해결했습니다. (TGT-52318)
* 업데이트된 VEC에서 고객이 텍스트 요소를 편집하거나 컨테이너 개체를 제거하지 못하는 문제를 해결했습니다. (TGT-52348)
* [!UICONTROL Overview] 활동 페이지에서 [!DNL Customer Journey Analytics]이(가) 올바르게 표시되지 않도록 차단하는 문제를 해결했습니다. (TGT-52359)
* 보고 그룹이 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 지속되지 않는 문제를 해결했습니다. (TGT-52368)
* Offer Decisioning이 포함된 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-52390)
* 기본 오퍼를 선택했지만 다른 오퍼 콘텐츠가 [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Multivariate Test]&#x200B;(MVT) 활동에 표시되는 문제를 해결했습니다. (TGT-52372)
* 전체 조직 액세스와 특정 조직 + 사용자 액세스 사이에서 OR로 확인하는 GET 권한 논리를 수정했습니다. (TGT-52374)
* [!UICONTROL Show Only Selected]이(가) 활성화되었음에도 불구하고 [!UICONTROL Managed Content] 및 [!UICONTROL Reporting Audiences]에 대한 대상을 선택한 후 대상 이름이 표시되지 않는 문제를 해결했습니다. (TGT-52393)

## [!DNL Target Standard/Premium] 25.5.1(2025년 5월 5일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 업데이트된 UI의 특정 활동에 대해 대상 세분화가 표시되지 않는 문제를 해결했습니다. (TGT-52057)
* 활동에서 결합된 대상을 사용할 수 없는 문제를 해결했습니다. (TGT-52346)
* 동일한 작업 영역의 활동 전용 대상을 사용하여 기본값이 아닌 작업 영역에서 새 활동을 만들 수 없는 문제를 해결했습니다. (TGE-52349)
* 새 대상을 만들고 선택한 후 활동 전용 대상이 업데이트된 UI에서 사라지는 문제를 해결했습니다. (TGT=52091)
* 활동에서 중복 대상을 사용할 수 없는 문제를 해결했습니다. (TGT-51200 및 TGT-52057)
* 업데이트된 UI에서 대상 세분화 및 활동 대상이 반전되는 문제가 해결되었습니다. (TGT-52158)
* 사용자 입력 오류: &quot;이 사용자에게 기본이 아닌 작업 영역이 허용되지 않습니다.&quot;로 인해 새 활동을 만들 수 없는 문제가 해결되었습니다. (TGT-52267)
* 기본 및 비기본 작업 영역 모두에 대해 업데이트된 UI에 오퍼가 표시되지 않는 문제를 해결했습니다. 이제 [!DNL Target]에 두 작업 영역의 오퍼가 표시됩니다. (TGT-52339)
* [!DNL Target]이(가) 활동을 편집하고 수정된 웹 사이트 요소를 변경할 때 고객에게 경고하지 않는 문제를 해결했습니다. (TGT-52100)
* 임시 오퍼를 사용하여 오퍼를 편집하면 기존 오퍼를 업데이트하는 대신 새 오퍼가 만들어지는 문제를 해결했습니다. (TGT-52135)
* 오퍼를 폴더로 이동할 때 잘못된 페이로드 오류가 발생하는 문제를 해결했습니다. (TGT-52325)
* 오퍼를 폴더로 이동할 때 사용자 입력 오류가 발생하는 문제를 해결했습니다. (TGT-52296)
* 각 활동에 대해 `audienceMetadata` 필드를 추가했으며 활동을 편집할 때 읽고 업데이트했는지 확인했습니다. (TGT-51004)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
