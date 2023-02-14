---
keywords: 릴리스 노트;새 기능;릴리스;업데이트;릴리스;개선 사항;개선 사항;수정 사항;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: abf4c005a3c0e3b2e0e9f1402bb2af3444634942
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 91%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 22.14.5(2023년 2월 13~15일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **2월 13일**: 아메리카 지역
* **2월 15일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **2월 15일**: 아시아 태평양(APAC) 지역

이번 릴리스에는 다음과 같은 수정 사항이 포함됩니다:

* 속성이 Automated Personalization (AP) 활동에 지정되었더라도 다음 오류 메시지가 표시되는 문제를 해결했습니다. &quot;오류: 하나 이상의 속성이 기본값이 아닌 작업 공간에 속해야 함&quot;(TGT-44607)
* 서버 측 Recommendations 피드에 영향을 줄 수 있는 보안 문제를 해결했습니다. (TGT-43769)

## at.js 버전 2.10.1 (2023년 2월 2일)

* 이름에 점이 있는 매개변수를 포함하는 대상자 규칙과 관련된 활동이 온디바이스 결정을 위해 예상되는 경험을 반환하지 않는 버그가 수정되었습니다.
* at.js 2.6.0에서 새로 발생한, `mboxDisable`이 활성화된 경우에도 at.js가 게재 호출을 시작하는 버그가 수정되었습니다.

모든 at.js 릴리스에 대한 정보는 [at.js 버전 세부 정보](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}를 참조하십시오.

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

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 정보 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 정보 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR)을 참조하십시오. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 프리릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 프리릴리스](/help/main/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
