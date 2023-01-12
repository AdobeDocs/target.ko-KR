---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 02105c00a856e755ef2fd0bb41620fd35ed609d2
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 52%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2023년 1월 4일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.13.3(2023년 1월 25~26일)

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

* 양식 기반 경험 작성기를 사용하여 [!UICONTROL Automated Personalization](AP) 활동에서 JSON 오퍼에 대한 지원이 추가되었습니다. (TGT-41460)
* 구현됨 [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md) AP 활동용.
* 의 경험 이름 [!DNL Recommendations] 이제 활동이 친숙한 이름으로 표시되므로 고객이 의 데이터를 보다 효과적으로 상호 연관시킬 수 있습니다 [!DNL Adobe Analytics] 그리고 [!DNL Target] UI. (TGT-41853)
* 에서 &quot;500 오류&quot;가 발생하는 문제를 수정했습니다. [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅] (XT) 추천이 포함된 활동. 이 문제는 [!DNL Target] 에서 기준 개체를 제대로 삭제하지 못했습니다. [!DNL Target] UI 및 [!DNL Recommendations] 더 이상 사용되지 않는 백엔드를 반환합니다. (TGT-44383)
* 에서 표시된 오퍼 이름에서 위치가 제거되었습니다. [!UICONTROL 오퍼 수준] 보고서 [!UICONTROL Automated Personalization] 활동. 이 변경 사항으로 보고서를 더 읽기 쉽게 만듭니다. (TGT-44294)
* 이름이 &quot;[!UICONTROL 경험 조각]&quot; 옵션을 선택합니다 [!UICONTROL 시각적 경험 작성기] (VEC) 워크플로우입니다. 이 옵션은 이제 “[!UICONTROL HTML XF]”입니다. (TGT-44132)
* 오퍼 정보 도구 설명에서 경험 조각 오퍼 메타데이터를 볼 수 있는 기능이 추가되었습니다. (TGT-43838)
* [!DNL Target] UI의 AP 및 [!UICONTROL 자동 타겟팅] [!UICONTROL 개인화 인사이트] 보고서 및 [!UICONTROL 중요 속성] 보고서에서 45일 및 90일 달력 옵션이 제거되었습니다. 사용 패턴과 성능 향상을 위해 이들 날짜 범위는 더 이상 사용되지 않습니다. 현재 허용되는 범위인 15일, 30일 및 60일을 반영하도록 UI가 업데이트되었습니다. (TGT-39357)
* 변경할 수 없습니다. [!UICONTROL 최적화 목표와 동일] 설정 [!UICONTROL 목표 및 설정] 활동이 라이브 상태가 된 후의 페이지입니다. (TGT-43923)
* 의 기본 작업 공간에 문제를 일으킨 문제를 수정했습니다 [!DNL Target] 에서 업그레이드할 때 백엔드 [!DNL Target Standard] to [!DNL Target Premium]. (TGT-44081 및 TGT-44306)
* 에서 링크가 변경되었습니다. [!UICONTROL 구현] 페이지 ([!UICONTROL 관리] > [!UICONTROL 구현]) &quot;On-Device Decisioning을 사용하는 구현 메서드&quot;에서 지원되는 모든 SDK에 대해 Device Decisioning을 사용하는 방법을 설명하는 페이지를 가리키도록 합니다. Node.js, Java, .NET 및 Python. 자세한 내용은 [Target SDK 시작하기](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* 을 사용할 때 파일 업로드 문제가 발생하는 문제를 해결했습니다. [!DNL Scene7] 및 [!DNL Target].
* 의 액세스 가능성 향상 [!DNL Target] 내부 유용성 감사 결과를 사용하여 장애인용 UI. 이러한 액세스 가능성 개선 사항에는 키보드를 통해 이전에 액세스할 수 없었던 기능에 대한 액세스, 대체 텍스트 개선 사항, UI의 일부를 보다 유용하게 확대/축소하는 기능, 키보드 포커스 개선 등이 있습니다.   (TGT-42759)
* 전체 사이트에서 다양한 현지화 수정 작업을 수행했습니다. [!DNL Target] UI.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
