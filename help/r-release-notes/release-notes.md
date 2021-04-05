---
keywords: 릴리스 정보;새 기능;릴리스;업데이트;업데이트;릴리스;개선 사항;개선 사항;수정 사항;버그 수정;업데이트
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 최신 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 현재 릴리스에 포함된 새로운 기능은 무엇입니까?
feature: 릴리스 정보
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 36%

---

# Target 릴리스 노트(현재)

이 릴리스 노트에서는 각 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리를 더 이상  [!DNL Adobe Target] 지원하지 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하기 위해 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## at.js 2.4.1(2021년 3월 23일)

at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

* `targetPageParams`이(가) mbox 요청에 포함되는 문제를 해결했습니다. `targetPageParams` 는  `pageLoad` 요청에만 포함되어야 합니다. (TNT-40247)
* platform launch 전역 개체 종속성을 해당 개체에 대한 직접 참조로 대체하여 A[!DNL dobe Experience Platform Launch] 확장의 문서 및 창 글로벌 개체 관련 문제를 수정했습니다. (TNT-37124)

## Recommendations 피드 처리 서버의 IP 주소 변경 사항(2021년 3월 16일)

[!DNL Target Recommendations] 피드 처리 서버 IP 주소가 2021년 3월 16일에 업데이트되었습니다. 자세한 내용은 Recommendations 피드 처리 서버에서 사용하는 [IP 주소](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md)를 참조하십시오.

## Target Standard/Premium 21.2.1(2021년 3월 9일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

* 허용되는 오퍼 크기를 늘렸습니다(TGT-38304).

   | 유형 | 이전 제한 | 새 제한 |
   | --- | --- | --- |
   | HTML | 256KB | 1024KB |
   | Target UI에서 제공하는 시각적 오퍼 | 64KB | 각 경험에 대해 1024KB |
   | API를 통해 | 512KB | 1024KB |

* [!UICONTROL 개인화 ] 통찰력 [!UICONTROL 의 자동 Target] (AT) 및  [!UICONTROL Automated Personalization] (AP) 활동에 대한 보고서가 이제 매일 생성됩니다. 지난 15일, 30일 및 60일 동안 [!UICONTROL 자동화된 세그먼트] 또는 [!UICONTROL 중요 특성]을 제공하는 보고서를 선택할 수 있습니다. 다른 전환 확인 창 설정을 매일 실행할 수 있도록 45일 및 90일 옵션이 제거되었습니다. (TGT-39472)
* 고객이 활동의 [!UICONTROL 목표 및 설정] 페이지에서 [!UICONTROL 종속성 편집]을(를) 클릭할 때 현재 종속성이 표시되지 않는 문제를 해결했습니다. (TGT-39340)
* 작업 영역의 [!UICONTROL 대상 라이브러리]를 새로 고칠 때 발생하는 문제를 수정했습니다. 새로 고침 전에 현재 선택된 작업 영역의 대상이 표시됩니다. 새로 고친 후 [!UICONTROL 기본 작업 영역]과 해당 대상이 표시됩니다. 이제 현재 작업 공간과 해당 대상은 새로 고침 후에도 유지됩니다. (TGT-38871)
* [!UICONTROL Recommendations] 활동을 복사하고 나중에 기준 시퀀스를 변경하여 원래 활동을 편집할 때 발생하는 문제를 수정했습니다. 원래 활동의 기준 순서의 변경 사항도 복사된 활동에 잘못 적용되었습니다. (TGT-39155)
* [!UICONTROL Recommendations] 제외에 대해 잘못된 개수의 제품이 표시되는 문제를 해결했습니다. (TGT-39599)

## 추가 릴리스 노트 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 봅니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은  [Experience Cloud 릴리스 노트를 참조하십시오](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선 순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
