---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;개선 사항;새 기능;수정 사항;업데이트;출시전 릴리스
description: SDK, API 및 JavaScript 라이브러리를 비롯한 Adobe Target의 향후 릴리스에 포함된 새로운 기능, 향상된 기능 및 수정 사항에 대해 살펴볼 수 있습니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: 2e678fa8a4826f6bfdaef1a04b89b8da7de48d12
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 22%

---

# Target 릴리스 노트(사전 릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2021년 4월 16일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시기에 따라 이러한 페이지의 정보가 같을 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리를 더 이상  [!DNL Adobe Target] 지원하지 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트의 잠재적 문제를 방지하려면 최신 버전의 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리로 마이그레이션하십시오. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

## Target Standard/Premium 21.4.1(2021년 4월 19일)

이 릴리스에는 다음과 같은 새로운 기능이 포함됩니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

| 기능 | 세부 사항 |
| --- | --- |
| at.js에 대한 장치 내 의사 결정 지원 | 디바이스 내 의사 결정을 통해 마케터와 개발자는 0분 지연 시간에 사용자의 브라우저에서 실험과 개인화를 전달할 수 있습니다. |

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 대상자를 [!UICONTROL 모든 방문자]로 변경한 후 활동이 동기화되지 않는 문제를 수정했습니다. (TGT-40259)
* [!UICONTROL 중복 허용 안 함] 옵션이 활성화되어 있음에도 불구하고 [!UICONTROL Automated Personalization] 활동의 다른 위치에 오퍼가 사용될 때 중복되지 않는 문제를 해결했습니다. (TGT-39567)
* [!UICONTROL 관리] > [!UICONTROL Scene7 구성] 페이지가 제대로 로드되지 않는 문제를 해결했습니다. (TGT-39918)
* 속성이 잘못된 작업 영역에 매핑되는 문제를 수정했습니다. (TGT-39869)
* [!DNL Target Recommendations] 엔티티 필터링 규칙에 대한 새 목록 기반 연산자를 지원합니다. (TGT-39234)

   새롭게 추가된 연산자는 다음과 같습니다.

   * 목록에 포함
   * 목록에 포함되지 않음
   * 목록에
   * 목록에
   * 목록에
   * 목록에

* 권장 사항 제외를 만드는 동안 환경을 변경한 후 요청이 실패하는 경우 로드가 제한적으로 로드되는 문제를 해결했습니다. (TGT-39948)

## at.js 버전 2.5.0(2021년 4월 19일)

at.js의 이번 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* at.js에 대한 장치 내 의사 결정 지원
* Automated Personalization 활동에 대한 링크 지원 미리 보기

또한 이 릴리스에서는 Microsoft Internet Explorer 10 이상 버전에 대한 지원도 제거되었습니다.

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
