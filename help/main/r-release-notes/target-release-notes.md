---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 07d71ccf934a1c638c37285372c3ec3199ec2000
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 32%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2022년 7월 9일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.10.1(시차를 두고 릴리스 2022년 10월 4-6일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **10월 4일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **10월 5일**: 아시아 태평양(APAC) 지역
* **10월 6일**: 아메리카 지역

이 릴리스에는 다음과 같은 새로운 기능, 개선 사항 및 수정 사항이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
| 새로 만들기 [!UICONTROL 시각적 경험 작성기] Google Chrome용 확장 프로그램 | 새로운 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] Chrome용 (VEC) 확장은 Chrome 웹 스토어에서 사용할 수 있습니다.<br>2023년 1월부터 현재 [!DNL Target] Google에서 Manifest V2를 사용하여 확장을 허용하지 않으므로 VEC Helper 확장은 Google Chrome에서 작동하지 않습니다. 에서 웹 사이트를 시각적으로 작성하려면 새 확장을 다운로드하십시오 [!DNL Target] 새해부터 |
| 에 최적화된 A4T 지표 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target]<br>(정확한 릴리스 날짜를 결정합니다.) | 다음 변경 사항에 유의하십시오.<ul><li>에 이진 및 최대화 지표에 대한 지원을 추가했습니다. [!UICONTROL Target 분석] 용 A4T 보고 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동</li><li>에 대한 이진 지표 경고 메시지가 제거되었습니다. [!UICONTROL 자동 Target] 활동</li><li>2023년 2월 20일까지 기존 활동에 대한 동작을 보존합니다. 이 날짜 이후에는 기존 활동 마이그레이션을 새 동작으로 강제 적용하기 위해 활동이 중단됩니다</li><li>2023년 2월 20일부터 지원 `averagetimespentonsite`, `bouncerate`, 및 `entries` 지표 [!DNL Target] 활동은 더 이상 사용되지 않습니다.</li></ul> |

* 대상 규칙 정보가 [!UICONTROL 대상 개선] 정보 창. (TGT-43917)
* 성능 향상 [!DNL Target] UI를 사용하여 [권장 타깃팅 규칙 제한](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* 일부 구성 요소가 [!UICONTROL 수정 사항] 패널의 [!UICONTROL 경험] 페이지에서 전환한 후 VEC에서 활동을 만들거나 편집할 때 [!UICONTROL 작성] to [!UICONTROL 찾아보기] 모드. (TGT-43300)
* 일부 고객이 보관하지 못하는 문제를 해결했습니다 [!UICONTROL A/B 테스트] 를 사용하는 활동 [!UICONTROL 자동 Target]. (TGT-40978)
* 단일 보고 그룹 내의 여러 위치에서 단일 오퍼를 자동으로 사용하는 기능이 추가되었습니다. (TGT-43974)
* 에서 유형(HTML 또는 JSON)별로 경험 조각을 필터링하는 기능을 추가했습니다. [!UICONTROL 오퍼] 목록. (TGT-43121)
* 고객이 JSON을 삽입할 수 있는 문제가 해결되었습니다 [!UICONTROL 경험 조각] VEC를 사용할 때 오퍼를 사용할 수 있습니다. JSON 오퍼는 [!UICONTROL 양식 기반 경험] 작성기. (TGT-43846)

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
