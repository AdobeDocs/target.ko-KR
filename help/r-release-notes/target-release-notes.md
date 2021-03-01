---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;개선 사항;새 기능;수정 사항;업데이트;출시전 릴리스
description: SDK, API 및 JavaScript 라이브러리를 비롯한 Adobe Target의 향후 릴리스에 포함된 새로운 기능, 향상된 기능 및 수정 사항에 대해 살펴볼 수 있습니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 노트
translation-type: tm+mt
source-git-commit: ddc357197f6a182865c5f06930de747c143c7c38
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 21%

---


# Target 릴리스 노트(사전 릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2021년 1월 3일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시기에 따라 이러한 페이지의 정보가 같을 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>Adobe에서는 모든 고객이 사이트에서 발생할 수 있는 문제를 방지하기 위해 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션할 것을 권장합니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

## Target Standard/Premium 21.2.1(2021년 3월 9일 및 10일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

* 허용되는 오퍼 크기를 늘렸습니다(TGT-38304).

   | 유형 | 이전 제한 | 새 제한 |
   | --- | --- | --- |
   | HTML | 256KB | 1024KB |
   | Target UI에서 제공하는 시각적 오퍼 | 64KB | 각 경험에 대해 1024KB |
   | API를 통해 | 512KB | 1024KB |

* [!UICONTROL 개인화 ] 인사이트 [!UICONTROL  자동 Target] (AT) 및  [!UICONTROL Automated Personalization] (AP) 활동에 대한 보고서가 이제 매일 생성됩니다. 지난 15일, 30일 및 60일 동안 [!UICONTROL 자동화된 세그먼트] 또는 [!UICONTROL 중요 특성]을 제공하는 보고서를 선택할 수 있습니다. 다른 조회 창 설정을 매일 실행할 수 있도록 45일 및 90일 옵션이 제거되었습니다. (TGT-39472)
* 고객이 활동의 [!UICONTROL 목표 및 설정] 페이지에서 [!UICONTROL 종속성 편집]을(를) 클릭할 때 현재 종속성이 표시되지 않는 문제를 해결했습니다. (TGT-39340)
* 작업 영역의 [!UICONTROL 대상 라이브러리]를 새로 고칠 때 발생하는 문제를 수정했습니다. 새로 고침 전에 현재 선택된 작업 영역의 대상이 표시됩니다. 새로 고친 후 [!UICONTROL 기본 작업 영역]과 해당 대상이 표시됩니다. 이제 현재 작업 공간과 해당 대상은 새로 고침 후에도 유지됩니다. (TGT-38871)
* [!UICONTROL Recommendations] 활동을 복사하고 나중에 기준 시퀀스를 변경하여 원래 활동을 편집할 때 발생하는 문제를 수정했습니다. 원래 활동의 기준 순서의 변경 사항도 복사된 활동에 잘못 적용되었습니다. (TGT-39155)
* [!UICONTROL Recommendations] 제외에 대해 잘못된 개수의 제품이 표시되는 문제를 해결했습니다. (TGT-39599)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
