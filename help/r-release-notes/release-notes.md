---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
feature: Release Notes
translation-type: tm+mt
source-git-commit: ae44c57c7b8767915fbbce4271a4b1858dd07efd
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 44%

---


# Target 릴리스 노트(현재)

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

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

## at.js 2.4.0(2021년 1월 14일)

at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항을 포함합니다.

* 통합 프로필/플랫폼 ID에 대한 지원을 배달 API customerId에 추가합니다.
* 잘못된 스타일 태그 삽입이 수정되었습니다.

## 추가 릴리스 노트 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은  [Experience Cloud 릴리스 노트를 참조하십시오](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
