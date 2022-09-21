---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 3d8da94a52046e70a89dc24d7923f743bee5c458
workflow-type: ht
source-wordcount: '632'
ht-degree: 100%

---

# Target 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 22.9.1 (순차적 공개, 2022년 9월 13~15일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **9월 13일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **9월 14일**: 아메리카 지역
* **9월 15일**: 아시아 태평양(APAC) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* at.js 2.10.0 이상 버전을 다운로드할 때 서드파티 쿠키의 설정을 허용하거나 비활성화하는 [!UICONTROL 크로스 도메인] 옵션을 추가했습니다. (TGT-43674)
* [!DNL Recommendations] 피드 가져오기가 실패할 경우 고객에게 알리도록 [!DNL Target] UI의 알림을 업데이트했습니다. (TGT-35811)
* [!UICONTROL 시각적 경험 작성기] (VEC)에서 [!UICONTROL 의사 결정 제안]이 정상적으로 작동하지 않는 문제를 해결했습니다. (TGT-43866)
* [!UICONTROL Multivariate Testing] (MVT) 활동을 생성하는 동안 [!UICONTROL 요소 클릭] 전환 목표를 선택할 때 오류 메시지가 표시되는 문제를 해결했습니다. (TGT-43842)
* [!UICONTROL 자동화된 개인화] (AP) 활동에 대해 다운로드한 CSV 보고서 파일에 [!UICONTROL 노출 횟수] 열이 표시되지 않는 문제를 해결했습니다. (TGT-43780)
* [!UICONTROL 양식 기반 경험 작성기]를 사용할 때 경험을 복제한 후 고객이 HTML/JSON 오퍼를 편집할 수 없는 문제를 해결했습니다. (TGT-43633)
* 고객이 [!UICONTROL A/B 테스트] 활동을 기본이 아닌 작업 영역에서 다른 기본이 아닌 작업 영역으로 복사할 수 없는 문제를 해결했습니다. (TGT-41910)
* 권장 사항이 포함된 [!UICONTROL A/B 테스트] 및 [!UICONTROL Experience Targeting] (XT) 활동에서 고객이 [!DNL Recommendations] 오브젝트 사용(디자인, 기준, 컬렉션 등)을 올바르게 표시하고 더 이상 사용하지 않는 기준 오브젝트를 [!DNL Target] UI 및 [!DNL Recommendations] 백엔드에서 삭제할 수 있도록 문제를 해결했습니다. (TGT-42331)
* 매개변수를 가져올 때 [!DNL Target] UI에 네트워크 시간 초과 경고가 표시되는 문제를 해결했습니다. (TGT-43737)
* 키보드를 통해 특정 드래그 앤 드롭 액션에 액세스할 수 있도록 UI를 업데이트했습니다. (TGT-42969)
* 텍스트 문자열이 올바르게 현지화되도록 UI를 업데이트했습니다.

## at.js 버전 2.10.0(2022년 9월 13일)

* at.js 2.10.0 이상 버전을 다운로드할 때 서드파티 쿠키의 설정을 허용하거나 비활성화하는 [!UICONTROL 크로스 도메인] 옵션을 추가했습니다. (TGT-43674)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target="_blank"} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
