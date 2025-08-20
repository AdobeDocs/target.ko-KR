---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 14bd000afe6983c2cdab185e4f54cc6b2f14627b
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 12%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 8월 20일**

>[!NOTE]
>
>* 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 이 문서의 정보는 특히 릴리스 전에 자주 업데이트됩니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.8.3(2025년 8월 21일)

이번 릴리스에는 다음과 같은 업데이트 및 수정 사항이 포함되어 있습니다.

**오퍼 결정**

+++세부 정보 보기
* **고객이 업데이트된 UI에서 의사 결정 오퍼를 편집하고 특정 페이지 요소를 선택할 수 없는 문제가 해결되었습니다.**: 업데이트된 활동 만들기 프로세스에서 고객은 시각적 경험 작성기(VEC)에서 기존 의사 결정 오퍼를 편집하거나 특정 페이지 요소를 선택할 수 없었습니다. 의사 결정 오퍼가 HTML 오퍼로 잘못 표시되었으며 편집 중에 변경된 사항이 저장되지 않았습니다. 또한 일본 사이트와 같은 특정 지역 URL이 VEC에서 제대로 로드되지 않아 활동 만들기 및 업데이트가 차단됩니다. 이제 의사 결정 오퍼가 올바르게 표시되고, 페이지 요소는 예상대로 선택할 수 있으며, 지역 URL이 VEC에 제대로 로드되어 전체 편집 기능이 복원됩니다. (TGT-53425)
* **저장한 후 [!UICONTROL Offer Decision] 선택기를 예기치 않게 수정하고 변경할 수 없는 문제가 해결되었습니다.**: 업데이트된 활동 만들기 프로세스에서 고객이 의도한 대로 [!UICONTROL Offer Decision] 선택기를 수정할 수 없습니다. 선택기를 변경하려는 시도가 실패하여 저장한 후 선택기가 잘못된 값으로 되돌아갔습니다. 이 동작으로 인해 의사 결정 오퍼가 시각적 경험 작성기 (VEC)에서 사라져 추가 편집이 차단되었습니다. 이제 선택기 변경 사항이 올바르게 보존되고, 저장 후 의사 결정 오퍼가 VEC에 표시되고 편집 가능한 상태로 유지됩니다.(TGT-53433)
* **저장 후 [!UICONTROL Offer Decisions]이(가) 활동에서 사라지는 문제를 해결했습니다**: 활동 만들기 프로세스 중에 추가된 [!UICONTROL Offer Decisions]이(가) 활동을 저장하고 다시 연 후 유지되지 않았습니다. 동적 콘텐츠를 편집하고 특정 선택기 및 속성을 사용하여 [!UICONTROL Offer Decisions]을(를) 삽입하는 동안 이 문제가 발생했습니다. 저장 후 [!UICONTROL Offer Decisions]이(가) 올바르게 유지되고 선택기가 그대로 유지되므로 일관된 타기팅 및 편집 동작이 보장됩니다. (TGT-53434)

+++

**추천**

+++세부 정보 보기
* **Recommendations UI에서 사용자 지정 기준 CSV 다운로드가 404 오류를 반환한 문제가 해결되었습니다: 고객이 활동 만들기 프로세스에서 사용자 지정 기준 CSV를 다운로드할 수 없는 문제가 해결되었습니다.** 이제 다운로드 링크가 제대로 작동하여 고객이 예상대로 사용자 지정 기준을 내보낼 수 있습니다. (TGT-51966)
* **[!UICONTROL Catalog Search]**&#x200B;에서 일관되지 않은 이미지 로드 문제 해결: [!UICONTROL &#x200B; Catalog Search]의 썸네일 및 이미지가 활동 만들기 프로세스에서 일관되게 로드되지 않는 문제가 해결되었습니다. 이미지가 나타나지 않는 한 &quot;썸네일 URL&quot; 열이 표시되고 일부 제품 이미지가 탐색 또는 검색 작업 후 부분적으로 로드되거나 전혀 로드되지 않습니다. 이미지 로드 동작이 안정되었으며 이제 열 가시성 또는 탐색 동작에 관계없이 썸네일이 안정적으로 표시됩니다. (TGT-52778)
* **중복된 경험에서 권장 사항을 편집하면 원본 경험에 영향을 주는 문제가 해결되었습니다.**: 중복된 경험에서 권장 사항을 수정하면 의도하지 않게 원본 경험이 변경되었다고 고객이 보고했습니다. 특히 활동 만들기 프로세스에서 경험 B를 복제하고 해당 디자인 또는 기준을 편집한 후에는 별도의 엔티티임에도 불구하고 원래 경험 B에 동일한 변경 사항이 반영되었습니다. 이제 중복된 경험은 별도의 구성을 유지하므로, 한 경험에 대한 편집 내용이 원본에 영향을 주지 않습니다. (TGT-53369)
* **중복된 경험에 대한 변경 내용이 활동의 원래 경험에 의도하지 않게 영향을 주는 문제를 해결했습니다.**: 고객이 활동 내에서 경험을 복제하고 새 대상을 할당할 때 중복된 경험의 디자인 또는 기준에 대한 변경 내용이 원래 경험에도 반영되었다고 보고했습니다. 이 문제는 원래 버전을 직접 편집하지 않았더라도 발생하며, 동일한 활동 내에서 독립적인 변형을 만드는 기능에 영향을 줍니다. 활동 만들기 프로세스는 이제 복제된 경험을 올바르게 격리하여 한 경험에 대한 편집 내용이 원본에 영향을 주지 않도록 합니다. (TGT-53361)
* **전체 제품 특성 데이터를 [!UICONTROL Recommendation Catalog]에서 간헐적으로 표시하지 못하는 문제가 해결되었습니다.**: 데이터가 피드에 있더라도 업데이트된 [!DNL Recommendations] UI에서 고객은 메시지와 같은 특정 제품 특성이 C[!UICONTROL atalog Search] 결과에 일관되게 표시되지 않는 문제를 경험했습니다. 이 문제는 고객이 누락된 값을 검색하기 위해 열 가시성을 수동으로 다시 구성해야 했습니다. [!UICONTROL Catalog Search]은(는) 이제 구성된 모든 특성을 안정적으로 표시하므로 수동으로 열을 재설정할 필요가 없습니다. (TGT-52769)
* **라이브 활동에서 [!UICONTROL Front Promotion]을(를) 비활성화할 수 없는 문제가 해결되었습니다.**: 라이브 활동에서 [!UICONTROL Front Promotion]을(를) 비활성화하려는 시도가 저장되지 않았습니다. [!UICONTROL Change Promotion]을(를) 선택하고 비활성화한 후에도 활동을 다시 편집할 때 프로모션이 활성 상태로 유지되어 추천 구성에 대한 업데이트가 수행되지 않았습니다. 이제 프로모션 설정이 올바르게 저장되므로 고객이 예상대로 라이브 활동에서 프로모션을 비활성화하거나 수정할 수 있습니다. (TGT-53231)
* **데이터 없이 [!DNL Recommendations] [!UICONTROL Promotion]을(를) 사용하면 명확하지 않은 오류 메시지가 트리거되는 문제가 해결되었습니다.**: 필수 값을 지정하지 않고 [!UICONTROL Front] 활동에서 [!UICONTROL Back Promotion] 또는 [!DNL Recommendations]을(를) 사용하면 일반적인 &quot;잘못된 입력 오류&quot; 메시지가 표시됩니다. 기본 문제는 구성 필드가 누락되었지만 오류 메시지에 원인이 명확하게 표시되지 않아 문제 해결이 어려웠습니다. 이제 활동 만들기 프로세스에서 `collectionId` 또는 규칙과 같은 필수 필드가 누락된 경우 명확하고 실행 가능한 오류 메시지를 제공하므로 고객이 구성 문제를 신속하게 식별하고 해결할 수 있습니다. (TGT-52616)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++세부 정보 보기
* **AP 활동의 [!UICONTROL Targeting] 단계로의 진행을 차단하는 활동 만들기 프로세스의 문제 해결**: 고객이 두 위치를 추가하지 않으면 [!UICONTROL Targeting]&#x200B;(AP) 활동의 [!UICONTROL Automated Personalization] 단계로 진행할 수 없는 활동 만들기 프로세스의 문제를 해결했습니다. 이 동작은 오퍼가 여러 개인 단일 위치만으로도 충분했던 이전 경험과 다릅니다. 요구 사항이 수정되어 고객이 단일 위치 설정을 AP 워크플로우의 일부로 계속 사용할 수 있습니다. (TGT-53426)
* **새 활동 만들기 프로세스에서 투명 이미지에 대해 fmt=png-alpha 매개 변수를 설정하지 않은 문제가 해결되었습니다**: 업데이트된 UI에서 활동 만들기 프로세스 중에 삽입된 이미지는 기본적으로 `fmt=png-alpha` 매개 변수를 더 이상 포함하지 않으므로 투명도가 손실됩니다. 이 동작은 투명 배경을 유지하면서 자동으로 매개 변수를 이미지 URL에 추가한 이전 UI와 다릅니다. 이제 활동 만들기 프로세스에서 투명도가 필요한 경우 `fmt=png-alpha` 매개 변수를 이미지 URL에 올바르게 적용하여 투명한 에셋의 일관된 렌더링을 보장합니다. (TGT-52615)

+++

**[!UICONTROL Workspaces]**

+++세부 정보 보기
* **단일 작업 영역으로 제한된 고객이 다른 작업 영역의 활동을 볼 수 있는 문제를 해결했습니다**: 활동 만들기 프로세스에서 [!UICONTROL All Workspaces]을(를) 선택할 때 한 작업 영역으로 제한된 액세스 권한을 가진 고객이 예기치 않게 모든 작업 영역의 활동을 볼 수 있었습니다. 이러한 가시성은 다른 작업 공간의 라이브 활동에 의도하지 않은 변경을 초래할 수 있으며, 웹 사이트 성능에 영향을 줄 수 있습니다. 고객이 할당된 작업 영역 내의 활동만 보고 상호 작용할 수 있도록 Workspace 액세스 제어를 강화했습니다. (TGT-53101)
* **고객이 액세스 권한 없이 [!UICONTROL Default Workspace]의 활동을 볼 수 있는 문제를 해결했습니다.** 스테이징 작업 영역에만 액세스할 수 있는 고객이 활동 만들기 프로세스를 통해 [!UICONTROL Default Workspace]의 활동을 볼 수 있습니다. 이 동작은 올바른 백엔드 구성 및 액세스 권한에도 불구하고 발생했습니다. 고객이 할당된 작업 영역 내에서만 활동을 볼 수 있도록 Workspace 액세스 제어가 강화되었습니다.(TGT-53297)

+++

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
