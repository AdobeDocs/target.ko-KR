---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 80481a149d436f13bd510c4c4287d447799afbb4
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 54%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2022년 10월 19일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.10.3 (순차적 공개, 2022년 25월 10~27일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **10월 25일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **26월 10일**: 아시아 태평양(APAC) 지역
* **10월 27일**: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
| --- | --- |
| 연속 지표 | 에서 매출과 같은 연속 지표를 사용하는 기능이 추가되었습니다 [!UICONTROL 자동 Target] 및 [!UICONTROL 할당-할당] 활동.<br>이전에는 [!UICONTROL 자동 Target] 및 [!UICONTROL 자동 할당] 모델은 이진(전환 기반) 지표에서만 작동하도록 최적화되었습니다. (TGT-43649 및 TGT-43649)<BR>이 기능은 일부 고객에게만 제공됩니다. 이 기능은 향후 릴리스에서 모든 고객이 사용할 수 있습니다. |
| [!DNL Recommendations] 친숙한 이름 | 에 친숙한 이름이 추가되었습니다. [!UICONTROL Target 분석] A4T 보고. 이전에는 [!DNL Target] 나열된 경험 ID만 해당. 이 개선 사항은 [!DNL Adobe Analytics] 및 [!DNL Target] 및 은 고객이 A4T에서 보고서 작성을 간소화하는 데 도움이 됩니다. (TGT-41853 |

* 에 도구 설명이 추가되었습니다 [!DNL Target] 고객이 Audience Builder를 보다 효율적으로 탐색하고 익숙하지 않을 수 있는 기능을 사용하는 방법을 학습할 수 있도록 지원하는 UI입니다. (TGT-44139)
* 고객이 비활성화된 활동을 편집하지 못하도록 하는 기능이 추가되었습니다. [!DNL Target] 지원되지 않는 지표를 사용하기 때문입니다. UI의 메시지는 고객이 활동을 복제한 다음 전환 지표를 업데이트하도록 안내합니다.

   이 릴리스 사용 `averagetimespentonsite`, `bouncerate`, 및 `entries` 지표 [!DNL Target] 활동은 새 활동에서 더 이상 사용되지 않습니다. 기존 활동은 2023년 2월 6일까지 이러한 지표를 계속 사용할 수 있습니다. (TGT-43860, TGT-43861, TGT-43650)

* 에 도구 설명이 추가되었습니다 [!DNL Target] 고객이 을(를) 만들거나 편집하는 동안 최적화 기준을 선택하는 데 도움이 되는 UI [!UICONTROL 자동 Target] A4T를 사용하는 활동. (TGT-43713)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
