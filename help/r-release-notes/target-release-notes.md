---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
feature: Release Notes
translation-type: tm+mt
source-git-commit: bffda8c3461998767a002d66fd9340252237ae5d
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 20%

---


# Target 릴리스 노트(사전 릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜:2021년 1월 14일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시기에 따라 이러한 페이지의 정보가 같을 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다. 사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다.
>
>* **Adobe Experience Platform 웹 SDK**:Adobe Experience Platform  [!UICONTROL 웹 ] SDK를 사용하면 Adobe Experience Edge Network를  [!DNL Experience Cloud] (포함)에서 다양한 서비스와 상호 작용할  [!DNL Target]수 있습니다. [!DNL Adobe Experience Platform Web SDK]으로 마이그레이션하도록 선택하는 경우 *웹 SDK 안내서*&#x200B;에서 [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)란?을 참조하십시오.
   >
   >
* **at.js**:at.js JavaScript 라이브러리는 mbox.js보다 많은 이점을 제공합니다. 다른 이점 중에서도 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다. at.js로 마이그레이션하도록 선택하는 경우 [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target Skill Builder:개발자 채팅, Adobe Target의 mbox.js를 at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)로 마이그레이션합니다.
>
>
mbox.js는 현재 지원되지만(2021년 3월 31일까지) 2017년 7월 이후로 이 라이브러리에 기능 업데이트를 제공하지 않았습니다. 모든 고객을 [!UICONTROL Adobe Experience Platform Web SDK] 또는 at.js로 이동하면 엔지니어 및 지원 직원이 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있게 됩니다.

## Target Standard/Premium 21.1.1(2021년 1월 19일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

* [!UICONTROL 자동 Target] 활동에서 [!UICONTROL Analytics를 보고 소스](A4T)로 사용할 때 [!DNL Adobe Analytics] 지표를 선택할 때 경고를 추가했습니다. [!UICONTROL 자동 ] 타게팅 모델은 이진(전환 기반) 지표와 작동하도록 최적화되었습니다. 매출과 같은 연속 지표를 선택하면 차선의 결과가 있을 수 있으며 [!UICONTROL 개인화 인사이트] 보고서가 정확하지 않을 수 있습니다. (TGT-38926)
* A4T를 사용하는 [!UICONTROL 자동 Target] 활동에 대한 [!UICONTROL 자동 Target 요약] 보고서에 상태 아이콘을 추가했습니다. 보고서에서 각 경험 옆에 있는 녹색 확인 아이콘은 해당 경험에 대해 개인화된 기계 학습 모델이 생성되었음을 나타냅니다. 시계 아이콘은 모델을 만들 수 있는 충분한 트래픽이 제공되지 않았음을 나타냅니다. (TGT-38925)
* A4T 및 [!DNL Analytics] 전환 지표를 사용하는 [!UICONTROL 자동 Target] 활동에 대한 [!UICONTROL 자동화된 세그먼트] 및 [!UICONTROL 중요 속성] 보고서가 생성되고 [!DNL Target]을 보고 소스로 사용할 때와 동일하게 보입니다. (TGT-38931)
* [!UICONTROL Recommendations] [!UICONTROL 컬렉션] 목록에 환경 필터링 옵션을 추가했습니다. (TGT-38353)
* 잘못된 제품 수가 [!UICONTROL Recommendations] 컬렉션에 표시되는 문제를 해결했습니다. (TGT-39162)
* [!UICONTROL 마지막으로 업데이트된] 필터를 [!UICONTROL Recommendations] [!UICONTROL 카탈로그 검색]에 추가했습니다. (TGT-38340)
* 업계 수직 변경 후 [!UICONTROL 시퀀스 만들기] 페이지가 중단되는 [!UICONTROL Recommendations]의 문제를 수정했습니다. (TGT-38160)
* Device Co-op이 활성화되어 있고 사용자가 [!DNL Target]에서 보고 소스로 [!DNL Analytics](A4T)로 변경된 경우 활동이 저장되지 않는 문제를 해결했습니다. (TGT-38163)
* 사용자가 [!UICONTROL Automated Personalization](AP) 활동의 오퍼에서 대상을 제거하지 못했던 문제를 수정했습니다. (TGT-39058)
* 일부 고객의 [!UICONTROL 대상 정보] 카드에 잘못된 시간 프레임(시작 및 종료 날짜)이 표시되는 문제를 수정했습니다. (TGT-39150)
* 일부 고객이 [!UICONTROL 기본 작업 공간]의 활동 목록을 볼 수 없는 문제를 수정했습니다. (TGT-38526)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
