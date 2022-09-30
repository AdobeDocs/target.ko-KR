---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 0c6d2df47a9115bcbd3c0d8a5ea7d401df29d6c8
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 79%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2022년 9월 29일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.10.1 (순차적 공개, 2022년 10월 4~6일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **10월 4일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **10월 5일**: 아시아 태평양(APAC) 지역
* **10월 6일**: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) 경험 구성요소 | AEM 경험 구성요소 기능에 대한 업데이트에는 다음이 포함됩니다.<ul><li>에서 유형(HTML 또는 JSON)별로 AEM 경험 조각을 필터링하는 기능을 추가했습니다. [!UICONTROL 오퍼] 목록. (TGT-43121)</li><li>고객이 JSON을 삽입할 수 있는 문제가 해결되었습니다 [!UICONTROL 경험 조각] 오퍼는 VEC를 사용할 때 지원되지 않습니다. JSON 오퍼는 [!UICONTROL 양식 기반 경험] 작성기. (TGT-43846)</li></ul>자세한 내용은 AEM 를 참조하십시오. [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Google Chrome용 새로운 [!UICONTROL 시각적 경험 작성기] 확장 기능 | Chrome용 새로운 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기](VEC) 확장 기능은 Chrome 웹 스토어에서 사용할 수 있습니다.<br>2023년 1월부터는 Google이 Manifest V2를 사용하는 확장 기능을 허용하지 않으므로 현재 [!DNL Target] VEC Helper 확장 기능은 Google Chrome에서 작동을 중지합니다. 새해부터는 [!DNL Target]에서 웹 사이트를 계속 시각화하려면 새 확장 버전을 다운로드하십시오.<br>다음 링크는 Chrome 웹 스토어의 두 확장을 보여줍니다.<ul><li>[새 확장](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[이전 확장](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>자세한 내용은 [시각적 편집 도우미 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟]<br>에 최적화된 A4T 지표(정확한 릴리스 일자는 미정) | 다음 변경 사항에 유의하십시오.<ul><li>[!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 활동에 대한 A4T([!UICONTROL Analytics for Target]) 보고에서 바이너리 및 최대화 지표 지원 추가</li><li>기존 활동에 대한 비헤이비어는 2023년 2월 20일까지 유지됩니다. 이 날짜 이후에는 기존 활동을 새 비헤이비어로 강제 마이그레이션하기 위해 활동이 중단됩니다.</li><li>2023년 2월 20일부터 [!DNL Target] 활동의 `averagetimespentonsite`, `bouncerate`, `entries` 및 지표에 대한 지원이 중단됩니다.</li></ul> |

* [!UICONTROL 대상자 세분화] 정보 창에서 대상자 규칙 정보가 제대로 표시되지 않는 문제를 해결했습니다. (TGT-43917)
* [타겟팅 규칙의 권장 제한](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules)에 근접한 대상자를 로드할 때 [!DNL Target] UI의 성능이 향상되었습니다. (TGT-43675)
* [!UICONTROL 구성]에서 [!UICONTROL 찾아보기] 모드로 전환한 후 VEC에서 활동을 생성하거나 편집할 때 일부 구성 요소가 [!UICONTROL 경험] 페이지의 [!UICONTROL 수정] 패널에 제대로 표시되지 않는 문제를 해결했습니다. (TGT-43300)
* 일부 고객이 [!UICONTROL 자동 타겟]을 사용하는 [!UICONTROL A/B 테스트 활동]을 보관할 수 없는 문제를 해결했습니다. (TGT-40978)
* 단일 보고 그룹 내 여러 위치에서 단일 오퍼를 자동으로 사용할 수 있는 기능이 추가되었습니다. (TGT-40689)

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
