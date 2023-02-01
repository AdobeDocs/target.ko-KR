---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: da159c10bd5100519b58cf2cb9c3d4ce15c4b2d0
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 100%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2023년 1월 26일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.13.3 (2023년 1월 25~26일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **1월 25일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **1월 25일**: 아시아 태평양(APAC) 지역
* **1월 26일**: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
| --- | --- |
| Automated Personalization(AP)에서의 [JSON 오퍼](/help/main/c-experiences/c-manage-content/create-json-offer.md) 지원 | 양식 기반 경험 작성기를 사용하여 [!UICONTROL Automated Personalization] (AP) 활동에서 JSON 오퍼에 대한 지원이 추가되었습니다. (TGT-41460) |
| [AEM 경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | [!DNL Target]으로 내보낸 [!DNL Adobe Experience Manager] 조각(AEM XF) 유형을 구별하는 기능이 추가되었습니다. 이제 “경험 조각” 옵션 대신 [!DNL Target]에서 “HTML XF” 및 “JSON XF”로 필터링하고 검색할 수 있습니다. (TGT-44132) |

* 권장 사항이 포함된 [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타겟팅] (XT) 활동에서 “500 오류”가 발생하는 문제를 해결했습니다. 이 문제는 [!DNL Target]이 더 이상 사용되지 않는 [!DNL Target] UI 및 [!DNL Recommendations] 백엔드에서 기준 오브젝트를 제대로 삭제하지 못했을 때 발생했습니다. (TGT-44383)
* [!UICONTROL Automated Personalization] 활동에 대한 [!UICONTROL 오퍼 수준] 보고서에 표시된 오퍼 이름에서 위치를 제거했습니다. 이렇게 변경하면 보고서를 보다 쉽게 읽을 수 있습니다. (TGT-44294)
* [!DNL Target] UI의 AP 및 [!UICONTROL 자동 타겟팅] [!UICONTROL 개인화 인사이트] 보고서 및 [!UICONTROL 중요 속성] 보고서에서 45일 및 90일 달력 옵션이 제거되었습니다. 사용 패턴과 성능 향상을 위해 이들 날짜 범위는 더 이상 사용되지 않습니다. 현재 허용되는 범위인 15일, 30일 및 60일을 반영하도록 UI가 업데이트되었습니다. (TGT-39357)
* 활동 활성화 이후 [!UICONTROL 목표 및 설정] 페이지에서 [!UICONTROL 최적화 목표와 같음] 설정을 변경할 수 없습니다. (TGT-43923)
* [!DNL Target Standard]에서 [!DNL Target Premium]으로 업그레이드할 때 [!DNL Target] 백엔드의 기본 작업 공간에 문제가 발생하는 문제를 해결했습니다. (TGT-44081 및 TGT-44306)
* 이름에 점 문자 “.”를 포함하는 [!DNL Analytics] 보고서 세트를 허용하도록 변경했습니다. 이에 따라 보고서 세트가 [!DNL Target] UI에서 사용되어 [!DNL Analytics] 분류 피드를 생성할 수 있습니다.
* 지원되는 모든 SDK(Node.js, Java, .NET 및 Python)에 대해 온디바이스 결정을 사용하는 방법을 설명하는 페이지를 가리키도록 “온디바이스 의사 결정을 사용하는 구현 방법”에 대한 [!UICONTROL 구현] 페이지([!UICONTROL 관리] > [!UICONTROL 구현])의 링크를 변경했습니다. 자세한 내용은 [Target SDK 시작하기](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}를 참조하십시오.
* [!DNL Scene7] 및 [!DNL Target]을 사용할 때 파일 업로드 문제를 발생시키는 문제를 해결했습니다.
* 내부 사용성 감사 결과를 사용하여 장애가 있는 사용자를 위한 [!DNL Target] UI 접근성을 개선했습니다. 이러한 접근성 향상에는 이전에 키보드에서 사용할 수 없었던 기능에 대한 액세스, 대체 텍스트 향상, UI의 일부를 보다 유용하게 확대/축소하는 기능, 개선된 키보드 포커스 등이 포함됩니다. (TGT-42759)
* [!DNL Target] UI 전반에 걸쳐 다양한 현지화 수정을 수행했습니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
