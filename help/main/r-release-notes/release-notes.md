---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6b92e823c854996e074716a7b8c4856176710c24
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 15%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## [!DNL Target Standard/Premium] 26.1.1 (2026년 1월 18일 월요일)

**활동**

+++세부 정보 보기

* **활동을 복사할 수 없습니다. 잘못된 사용자 입력입니다.** 활동을 복사할 때 사용자에게 유용하지 않은 &quot;잘못된 사용자 입력&quot; 오류가 표시되는 문제가 해결되었습니다. 이전에는 활동이 중복되면 해당 작업 영역별 속성 할당이 유지되지 않으므로 ABAactivity에 기본이 아닌 작업 영역에 속하는 속성이 하나 이상 필요하므로 백엔드가 저장 요청을 거부했습니다. 이 불일치로 UI에 일반 오류가 발생하여 사용자에게 지침이 없습니다. 이 수정 사항을 사용하면 복사 작업 중에 작업 공간 할당이 올바르게 유지되므로 사용자가 복사한 활동을 수정 없이 저장할 수 있고 잘못된 유효성 검사 오류를 방지할 수 있습니다. (TGT-54282)
* **웹 편집기 오퍼의 작업 영역 열을 사용하도록 설정합니다.** 이 업데이트는 [!UICONTROL Default Workspace]의 오퍼가 웹 편집기의 다른 작업 영역에 표시되기 때문에 발생하는 고객 혼동을 해결합니다. 이 동작은 설계된 대로 작동하지만 [!UICONTROL Default Workspace]개의 오퍼가 모든 작업 영역에서 의도적으로 표시되지만, 특히 &quot;승인자&quot;와 같이 기본이 아닌 작업 영역에서 활동을 만들 때 UI가 작업 영역 원본을 명확하게 하지 않았다고 고객이 보고했습니다. 명확성을 개선하기 위해 웹 편집기의 오퍼 목록에서 [!UICONTROL Workspace] 열을 활성화하여 사용자가 각 오퍼가 속한 작업 영역을 쉽게 구별하고 표시되는 추가 오퍼를 잘못 해석할 수 있습니다. (TGT-54138)
* **target=&quot;_blank&quot;인 링크가 새 탭에서 열립니다.** 이 수정 사항은 ~ 모드에서 클릭할 때 ~target=&quot;_blank&quot;[!UICONTROL Browse]인 링크가 포함된 작성된 웹 사이트가 새 브라우저 탭에서 열려 편집기의 미리 보기 환경을 중단하는 문제를 해결합니다. 이 동작은 앵커 요소가 변형되고 편집기 내에서 탐색을 유지하기 위해 대상이 재정의되는 기존 UI에서와 달리, 작성된 페이지의 기본 링크 속성이 확장의 주입된 JavaScript에 의해 가로채지지 않았기 때문에 발생했습니다. 업데이트를 통해 ~target=&quot;_blank&quot;~을(를) 사용하는 링크가 이제 웹 편집기에서 제대로 처리되므로 작성하는 동안 외부 탭이 더 이상 열리지 않습니다. (TGT-54134)
* **속성 경고를 선택 취소합니다.** 이 업데이트에서는 활동 편집기에서 자동 검색 속성을 선택 해제할 때 사용자에게 명확하게 알리는 시각적 경고를 도입합니다. 이전에는 자동 감지된 속성을 제거해도 속성이 영구적으로 삭제된다는 표시가 없으므로 타깃팅 구성이 실수로 손실됩니다. 이 수정 사항은 기존 UI의 비헤이비어와 일치하는 경고 아이콘을 추가하여 속성을 선택 해제하면 활동에서 제거됨을 사용자에게 알립니다. (TGT-54121)
* **[!UICONTROL Workspaces]드롭다운은 [!UICONTROL Users] 섹션에서 20개로 제한됩니다.** 이 수정 사항은 사용자가 더 많은 항목에 액세스할 수 있는 경우에도 [!UICONTROL Workspaces] > [!UICONTROL Administration] 섹션의 [!UICONTROL Users] 드롭다운에 20개의 작업 영역만 표시되는 문제를 해결합니다. `licenseGroups`에 대한 기본 GraphQL 호출도 20개의 결과로 제한되어 사용자가 조직의 더 많은 작업 영역에 액세스할 수 있더라도 UI에 불완전한 목록이 표시됩니다. 업데이트에서는 이 엄격한 제한이 제거되므로 이제 사용 가능한 작업 영역의 전체 세트가 반환되고 올바르게 표시됩니다. (TGT-53820)
* **오퍼 모달에 작업 영역 열이 표시되지 않는 문제가 해결되었습니다.** 오퍼 모달이 업데이트된 UI에서 작업 영역 열을 표시하지 않는 문제를 해결했습니다. 이로 인해 [!UICONTROL Default Workspace]의 오퍼가 출처를 표시하지 않고 선택한 작업 영역의 오퍼와 함께 표시되므로 고객에게 혼동이 발생했습니다. 이제 작업 영역 열이 활성화되어 고객이 각 오퍼가 속한 작업 영역을 명확하게 식별할 수 있습니다. (TGT-52320)

+++

**속성**

+++세부 정보 보기
* **이미 제거된 경우 활동 편집에서 자동 검색 속성을 추가해서는 안 됩니다.** 이 수정 사항은 활동을 편집하면 사용자가 이전에 제거한 자동 검색 속성이 자동으로 다시 시작되는 문제를 해결합니다. 편집을 위해 활동을 다시 열 때 시스템에서 제거된 속성을 잘못 복원하여 [!UICONTROL Properties List]에서 일관되지 않은 동작과 혼동을 초래했습니다. 업데이트는 자동 검색 속성이 제거되면 이후에 편집하는 동안 제거된 상태로 유지되며 사용자가 명시적으로 다시 추가하지 않으면 다시 나타나지 않습니다. (TGT-54182)
* **자동으로 검색된 속성을 이미 제거한 경우에는 추가하지 마십시오.** 이 수정 사항을 사용하면 사용자가 활동에서 자동 검색 속성을 수동으로 제거한 후 활동 편집기 내에서 이후에 탐색하는 동안 시스템이 더 이상 속성을 다시 도입하지 않습니다. 이전에는 사용자가 자동 검색 속성을 선택 취소하고 [!UICONTROL Targeting] 단계로 이동한 다음 [!UICONTROL Experiences]&#x200B;(으)로 돌아오면 편집기에서 활동 편집기 상태 슬라이스에 저장된 자동 검색 목록을 기반으로 제거된 속성을 다시 채웁니다. 업데이트된 논리는 이제 자동 감지된 속성을 ~ActivityState~ 슬라이스의 현재 속성과 비교하고, 사용자가 이미 제거한 자동 감지된 속성을 다시 추가하는 것을 방지합니다. 이렇게 하면 여러 단계에서 일관된 동작이 발생하고 사용자 의도를 따릅니다. (TGT-54181)
* **자동으로 검색된 텍스트를 속성 목록에 추가합니다.** 이 향상된 기능은 [!UICONTROL Properties List]을(를) 업데이트하여 시스템에서 자동으로 감지한 모든 속성에 레이블을 지정합니다. 자동 검색 속성도 사용자가 볼 수 있는 [!UICONTROL Properties List]에 있으면 이제 ~ActivityEditorSlice~ 상태에 저장된 값을 사용하여 이름 옆에 &quot;(자동 검색)&quot; 텍스트가 표시됩니다. 이렇게 하면 기존 UI의 동작이 미러링되며 사용자가 수동으로 선택한 속성과 자동으로 식별된 속성을 쉽게 구분할 수 있습니다. (TGT-54120)
* **자동 검색된 [!UICONTROL Properties]을(를) 상태에 추가합니다.** 이 업데이트는 ~ActivityEditorSlice.ExperienceEditor~ 상태가 웹 편집기에서 Activity [!UICONTROL Experiences] 탭으로 전달된 모든 자동 검색 속성 ID의 최신 목록을 일관되게 유지하도록 합니다. 사용자가 [!UICONTROL Experiences] 탭으로 이동할 때마다 중복을 방지하면서 새로 감지된 속성으로 상태가 새로 고쳐져 정확한 추적이 보장되고 안정적인 다운스트림 동작이 보장됩니다. (TGT-54119)

+++

**추천**

+++세부 정보 보기
* **[!UICONTROL Environment]드롭다운에는 100개의 결과만 표시됩니다.** 이 수정 사항은 환경이 100개를 초과하는 고객이 [!UICONTROL Environment] 내의 [!UICONTROL Recommendations] 드롭다운에서 처음 100개의 항목만 볼 수 있는 제한을 해결합니다. 기본 GraphQL 쿼리(~getEnvironmentsV2~)는 100의 하드 코딩된 페이지 크기로 페이지 매김되어 추가 페이지를 사용할 수 있는 경우에도 UI에 부분 목록만 표시됩니다. 환경이 100개를 초과하는 고객의 경우 이 문제로 인해 옵션이 누락되고 선택 경험이 불완전합니다. 업데이트는 제한이 증가하여 모든 환경이 반환되고 표시되므로 환경 수에 관계없이 전체 가시성이 보장됩니다. (TGT-53903)

+++

**보고서**

+++세부 정보 보기

* **[!UICONTROL Reports] 화살표가 확장 가능한 열을 명확하게 나타내지 않는 문제를 해결했습니다.** 보고 테이블에서 업데이트된 UI에서 추가 열을 확장할 수 있음을 명확하게 표시하지 않는 문제를 해결했습니다. 열 헤더 근처의 [!UICONTROL Reports] 화살표에 사라진 도구 설명이 추가되어 고객이 더 많은 열을 사용할 수 있음을 이해할 수 있습니다.

+++

**보기 횟수**

+++세부 정보 보기

* **보기에 적용된 수정 사항을 삭제할 수 없습니다.** 이 수정 사항은 수정 사항이 추가 보기에 다시 적용되지 않는 한 사용자가 활동 내에서 수정 사항을 삭제할 수 없는 문제를 해결합니다. 활동(예: 활동 ID 302467) 편집 시 수정 사항 삭제 시도는 영향을 미치지 않았으므로 사용자가 원치 않는 변경 사항을 제거할 수 없습니다. 그러나 &quot;더 많은 보기에 적용&quot;을 사용하여 수정 사항을 다시 적용하고 `Page Load` 이벤트에 할당하면 예상대로 삭제가 갑자기 작동합니다. (TGT-54088)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++세부 정보 보기
* **[!UICONTROL Experience Fragment]이름이 새 VEC UI**&#x200B;에서 잘렸습니다(TGT-54312).
* **[!UICONTROL Advanced Settings] 지표에 [!UICONTROL Revenue]을(를) 사용할 수 없습니다.** 이 수정 사항은 사용자가 [!UICONTROL Advanced Settings]의 [!UICONTROL Revenue] 지표에 대해 [!UICONTROL Goals & Settings]을(를) 구성할 때 403 &quot;액세스 거부&quot; 오류가 발생하는 문제를 해결합니다. 기본 목표에 연결된 종속성 조건을 추가할 때 문제가 발생했습니다. 활동을 만들고 편집할 수 있는 권한이 이미 있는 사용자에게도 백엔드에 편집기 권한이 잘못 필요했습니다. 그 결과, 올바른 구성에도 불구하고 활동을 저장하지 못했습니다. 업데이트는 적절한 액세스 권한이 있는 사용자가 금지된 리소스 오류를 트리거하지 않고 매출 지표 종속성을 성공적으로 추가할 수 있도록 권한 검사를 수정합니다. (TGT-54092)
* **추가 단추가 선택한 이미지에 적용되지 않는 문제를 해결했습니다.** 고객이 활동 만들기 프로세스에서 이미지를 선택하거나 업데이트할 때 특정 이미지를 추가하지 못하는 문제를 해결했습니다. 고객이 특정 자산(예: &quot;ipp&quot;를 검색할 때 반환된 이미지)을 검색할 때 [!UICONTROL Add] 단추를 클릭해도 선택한 이미지가 적용되지 않고 수정되지 않았습니다. `Homepage-banner-1-moz.jpg`과(와) 같은 다른 이미지를 선택하면 예상대로 계속 작동합니다. 이 업데이트를 통해 모든 유효한 이미지를 업데이트된 UI에서 일관되게 적용할 수 있습니다. (TGT-53610)
* **URL 조건을 삭제하면 목표 지표 구성이 재설정되는 문제가 해결되었습니다.** [!UICONTROL Goal] 지표에서 단일 URL 조건을 제거하면 전체 구성이 업데이트된 UI에서 재설정되는 문제가 해결되었습니다. 고객이 [!UICONTROL Conversion] > [!UICONTROL Viewed a Page]에서 저장된 URL 조건을 삭제하려고 할 때 목표 유형이 예기치 않게 [!UICONTROL Viewed an Mbox]&#x200B;(으)로 전환되었으며 이전에 구성된 모든 설정이 제거되었습니다. 이 업데이트에서는 선택한 URL 조건만 삭제되고 나머지 목표 설정은 모두 그대로 유지됩니다. (TGT-53271)
* **하위 폴더를 검색하지 못하는 문제가 해결되었습니다.** 오퍼를 검색해도 업데이트된 UI의 하위 폴더에서 결과가 반환되지 않는 문제를 해결했습니다. 고객이 오퍼가 저장된 폴더로 수동으로 이동하여 검색 동작이 API 기능과 일치하지 않는 경우에만 오퍼를 찾을 수 있습니다. 이제 검색은 폴더를 재귀적으로 검색할 수 있도록 지원하므로 고객은 각 폴더를 개별적으로 열 필요 없이 오퍼를 찾을 수 있습니다. (TGT-51954)

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
