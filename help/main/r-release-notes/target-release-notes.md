---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c882a5eb6530f3b3fe44484ee580beadeddaae23
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 29%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 6월 25일**

>[!NOTE]
>
>* 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.6.4 (2025년 6월 26일 금요일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 기존 VEC에서 사용할 수 있는 기능에 맞게 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) UI에 [!UICONTROL Rearrange] 옵션을 추가했습니다. (TGT-46957 및 TGT-52876)
* [!UICONTROL A/B Test] 활동에서 변형 경험(예: 경험 B)에 대한 수정 사항이 유지되지 않는 문제를 해결했습니다. 경험 간에 전환하면 변형에 대한 변경 사항이 사라집니다. 이 문제는 제어 경험에 영향을 주지 않았습니다. (TGT-52664)
* 특정 고객은 활동을 만들거나 저장할 수 없지만 다른 고객은 문제 없이 동일한 작업을 수행할 수 있는 문제를 해결했습니다. 그 문제는 여러 면에서 일관성이 없었다.(TGT-52842)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에 대한 보고 데이터를 가져올 때 발생하는 null 포인터 예외를 해결했습니다. (TGT-52362)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에 대한 .CSV 파일에 오퍼 수준 세부 정보가 표시되지 않는 문제를 해결했습니다. (TGT-52675)
* 업데이트된 VEC에서 수정 사항을 적용할 때 필요한 [!UICONTROL Experience Fragment]을(를) 포함하여 변경 사항이 처음에 올바르게 표시됩니다. 그러나 경험을 전환하거나 추가로 편집할 때 선택기 문제로 인해 일부 수정 사항이 적용되지 않습니다. (TGT-52679)
* 기존 활동을 복제하여 새 활동을 만들 때 복제된 활동의 QA 링크가 원래 활동의 페이지 URL을 잘못 유지하는 문제를 해결했습니다. (TGT-52775)
* 업데이트된 VEC에서 실수로 [!UICONTROL On-device Decisioning]을(를) 사용할 수 없는 문제를 해결했습니다. (TGT-52371)
* 제품 [!DNL Recommendations] 활동을 편집할 수 없는 문제를 해결했습니다. Target UI를 통해 VEC에 액세스하려고 할 때 [!UICONTROL Overview] 페이지에 오류가 발생하여 편집할 수 없습니다. (TGT-52823)
* 경험 이름이 50자를 초과할 때 [!DNL Recommendations] 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-52619)
* 고객이 새 UI에서 기준을 수정한 후 권장 사항 활동을 저장할 수 없는 문제를 해결했습니다. 이 문제는 권한과 관련된 것으로 표시되며 유사한 역할을 가진 모든 사용자에게 영향을 주지 않습니다. (TGT-52816)
* [!UICONTROL Editor] 역할을 가진 사용자가 [!DNL Recommendations] 활동을 편집할 수 없는 문제가 해결되었습니다. 사용자가 관련 작업 영역에서 이미 해당 역할을 가지고 있더라도 디자인을 변경하고 활동을 저장하려고 하면 &quot;[editor]&quot; 권한이 필요함을 알리는 403 금지된 오류가 발생했습니다. (TGT-52836)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
