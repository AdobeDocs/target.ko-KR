---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: dea956fe5d28200515a9638306a7d879585cb794
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 75%

---

# Target 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 22.10.1 (순차적 공개, 2022년 10월 5~7일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **10월 5일**: 아시아 태평양(APAC) 지역
* **10월 6일**: 아메리카 지역
* **10월 7일**: 유럽, 중동 및 아프리카(EMEA) 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) 경험 구성요소 | AEM 경험 구성요소 기능에 대한 업데이트에는 다음이 포함됩니다.<ul><li>에서 유형(HTML 또는 JSON)별로 AEM 경험 조각을 필터링하는 기능을 추가했습니다. [!UICONTROL 오퍼] 목록. (TGT-43121)</li><li>고객이 JSON을 삽입할 수 있는 문제가 해결되었습니다 [!UICONTROL 경험 조각] 오퍼는 VEC를 사용할 때 지원되지 않습니다. JSON 오퍼는 [!UICONTROL 양식 기반 경험] 작성기. (TGT-43846)</li></ul>자세한 내용은 AEM 를 참조하십시오. [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Google Chrome용 새로운 [!UICONTROL 시각적 경험 작성기] 확장 기능 | Chrome용 새로운 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기](VEC) 확장 기능은 Chrome 웹 스토어에서 사용할 수 있습니다.<br>2023년 1월부터는 Google이 Manifest V2를 사용하는 확장 기능을 허용하지 않으므로 현재 [!DNL Target] VEC Helper 확장 기능은 Google Chrome에서 작동을 중지합니다. 새해부터는 [!DNL Target]에서 웹 사이트를 계속 시각화하려면 새 확장 버전을 다운로드하십시오.<br>다음 링크는 Chrome 웹 스토어의 두 확장을 보여줍니다.<ul><li>[새 확장](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[이전 확장](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>자세한 내용은 [시각적 편집 도우미 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟]<br>에 최적화된 A4T 지표(정확한 릴리스 일자는 미정) | 다음 변경 사항에 유의하십시오.<ul><li>[!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 활동에 대한 A4T([!UICONTROL Analytics for Target]) 보고에서 바이너리 및 최대화 지표 지원 추가</li><li>기존 활동에 대한 비헤이비어는 2023년 2월 20일까지 유지됩니다. 이 날짜 이후에는 기존 활동을 새 비헤이비어로 강제 마이그레이션하기 위해 활동이 중단됩니다.</li><li>2023년 2월 20일부터 [!DNL Target] 활동의 `averagetimespentonsite`, `bouncerate`, `entries` 및 지표에 대한 지원이 중단됩니다.</li></ul> |
| 설명서 업데이트 | 주요 설명서 업데이트에는 다음 사항이 포함됩니다.<ul><li>신규 및 업데이트 [Adobe Target 관리 및 보고 API 설명서](https://developer.adobe.com/target/administer/admin-api/){target=_blank}에는 속성, 오퍼, 호스트, 환경, 클라이언트, 대상, 활동 등을 포함하는 관리 및 보고 API 엔드포인트에 대한 포괄적인 범위가 포함되어 있습니다.<br>에서 이 콘텐츠와 추가 개발자 콘텐츠를 참조하십시오. [[!DNL Adobe Target] [!UICONTROL 개발자 안내서]](https://developer.adobe.com/target/){target=_blank}.</li><li>[A/B 테스트의 통계적 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>이 문서에서는 의 수동 A/Bn 테스트에 사용되는 자세한 통계적 계산 [!DNL Adobe Target].<br>이 문서의 정보는 *A/B 테스트를 위한 Adobe Target 계산* 이전에 이 사이트에서 다운로드할 수 있었던 pdf 파일입니다.</li></ul> |

* [!UICONTROL 대상자 세분화] 정보 창에서 대상자 규칙 정보가 제대로 표시되지 않는 문제를 해결했습니다. (TGT-43917)
* [타겟팅 규칙의 권장 제한](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules)에 근접한 대상자를 로드할 때 [!DNL Target] UI의 성능이 향상되었습니다. (TGT-43675)
* [!UICONTROL 구성]에서 [!UICONTROL 찾아보기] 모드로 전환한 후 VEC에서 활동을 생성하거나 편집할 때 일부 구성 요소가 [!UICONTROL 경험] 페이지의 [!UICONTROL 수정] 패널에 제대로 표시되지 않는 문제를 해결했습니다. (TGT-43300)
* 일부 고객이 [!UICONTROL 자동 타겟]을 사용하는 [!UICONTROL A/B 테스트 활동]을 보관할 수 없는 문제를 해결했습니다. (TGT-40978)
* 단일 보고 그룹 내 여러 위치에서 단일 오퍼를 자동으로 사용할 수 있는 기능이 추가되었습니다. (TGT-40689)

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
