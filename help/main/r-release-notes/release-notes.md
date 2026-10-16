---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: '[!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: '[!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: 'https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: c5abb976-5170-45d6-bcac-66d15d10a4d4
    internal-label: Release notes
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 06cdc2613d49e3c71c2d29c6ee1307d39215ac84
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 42%
---
# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 26.10.2(2026년 10월 15일)

**[!UICONTROL 활동]**

+++세부 정보 보기

* **활동 개요에 잘못된 목표 설정이 표시됨**. 활동의 **[!UICONTROL 개요]** 페이지에 표시된 목표 설정이 올바르지 않은 문제가 해결되었습니다. 예를 들어 실제 목표 구성이 올바르지만 `https://`이(가) 페이지 URL에 추가되고 **[!UICONTROL URL 포함]** 조건이 표시되지 않습니다. (TGT-56326)

+++

**[!UICONTROL 추천]**

+++세부 정보 보기

* **실시간 활동에서 프로모션이 업데이트된 후 표시되는 백업 권장 사항**. [!DNL Recommendations] 라이브 활동에서 프로모션을 편집하면 [!DNL Target]이(가) 해당 정의에서 변경된 사항이 없음에도 새 프로모션 및 권장 사항 단위를 만드는 문제가 해결되었습니다. (TGT-56369)

+++

**[!UICONTROL 보고서]**

+++세부 정보 보기

* **보고 사전 설정이 2주 후에 삭제됨**. 사용자가 활동에 대해 저장한 보고 사전 설정이 약 2주 후에 자동으로 삭제되는 문제를 해결했습니다. (TGT-56374)

+++

**[!UICONTROL 시각적 경험 작성기](VEC)**

+++세부 정보 보기

* **Safari 지원이[!DNL Adobe Target]**&#x200B;에 추가되었습니다. [!DNL Target]은(는) 이제 [!DNL Safari] 브라우저에서 지원됩니다. 시각적 경험 작성기 및 [!DNL Enhanced Experience Composer]은(는) [!DNL Safari]에서 지원되지 않습니다. 따라서 이제 [!DNL VEC]에 오버레이가 표시되어 사용자에게 편집기를 사용하려면 [!DNL Chrome]&#x200B;(으)로 전환해야 함을 알립니다. (TGT-55853)

+++


## [!DNL Target Standard/Premium] 26.10.1(2026년 10월 13일)

**[!UICONTROL Analytics for Target]**

+++세부 정보 보기

* **A4T 보고에 실패하고 &quot;문제가 발생했습니다&quot; 오류가 발생했습니다**. 새로 추가된 보고서 세트를 사용하는 [!DNL A4T] 활동에서 [!DNL Target] 보고서에 결과가 아닌 &quot;문제가 발생했습니다&quot; 오류가 표시되던 문제를 해결했습니다. **[!UICONTROL 분석에서 보기]**&#x200B;를 클릭하면 [!DNL Analytics for Target] 분류 정보가 누락된 &quot;호환되지 않는 보고서 세트&quot; 메시지도 표시됩니다. (TGT-56389)

+++

**[!UICONTROL 시각적 경험 작성기](VEC)**

+++세부 정보 보기

* **mbox를 통해 전달된 [!DNL Experience Fragments]의 오퍼 이름 대신 원시 HTML이 표시됨**. [!DNL Experience Fragment]이(가) mbox를 통해 배달될 때 **[!UICONTROL 수정 사항]** 패널에 오퍼 이름 대신 원시 HTML/코드가 표시되는 문제가 해결되었습니다. (TGT-56241)

+++

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 노트](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
