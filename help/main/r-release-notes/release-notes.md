---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 44ac64d0b97db4995193dea11c0c65934f386926
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 84%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!UICONTROL 활동] 페이지 사용자 인터페이스 새로 고침 (2023년 10월 25일)

[!DNL Target] 사용자용 사용자 경험을 개선하기 위한 [!DNL Adobe Target] 팀의 지속적인 노력의 일환으로 이번 릴리스에서는 [!DNL Target] UI의 [!UICONTROL 활동] 페이지가 새롭게 업데이트되었습니다. 이번 업데이트를 통해 새로운 개선 사항이 추가되었으며 이전에 일관되지 않았던 디자인 패턴이 통합되고 표준화되었습니다.

10월 25일 수요일부터 일부 고객이 새로운 UI에 액세스할 수 있으며, 향후 수일 이내에 더 많은 고객이 액세스할 수 있게 될 예정입니다.

자세한 내용은 [활동](/help/main/c-activities/activities.md)을 참조하십시오.

## [!DNL Target] Standard/Premium 23.11.1 (2023년 11월 13일, 14일)

이 릴리스는 다음 요일에 예정되어 있습니다.

* **11월 13일**: 아시아 태평양(APAC) 지역
* **11월 14일**: 아메리카 지역
* **11월 14일**: 유럽, 중동 및 아프리카(EMEA) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 이(가) 을(를) 개선했습니다. [활동 QA](/help/main/c-activities/c-activity-qa/activity-qa.md) 지원 기능 [중복 오퍼 허용 안 함](/help/main/c-activities/t-automated-personalization/managing-exclusions.md) 의 경험 [!UICONTROL Automated Personalization] 활동. (TGT-46627)
* 제어 경험에 트래픽이 할당되지 않을 경우 활동 보고서에 사용 가능한 데이터가 없을 수 있는 이유를 고객이 이해할 수 있도록 [!DNL Target] UI에 툴팁이 추가되었습니다. 자세한 정보에 대한 링크는 다음 툴팁에 포함되어 있습니다. [내 활동 보고서에 대해 사용 가능한 데이터가 없는 이유는 무엇입니까?](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B). (TGT-46610)
* 일부 고객의 [!UICONTROL 활동] 페이지에 활동이 제대로 표시되지 않는 문제가 해결되었습니다. (TGT-46830)
* 를 사용하는 활동에 영향을 주는 다음 문제를 해결했습니다. [[!UICONTROL Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) 보고 소스로서의 (A4T):
   * 일부 고객이 보고 데이터를 볼 수 없는 문제를 해결했습니다. (TGT-46557)
   * 다음과 같은 문제가 발생하던 문제를 수정했습니다. [!UICONTROL Analytics에서 보기] 활동 보고 페이지에 대한 링크가 제대로 작동하지 않습니다. (TGT-46731)
   * 에 대한 데이터를 사용할 수 없는 문제가 해결되었습니다. [!UICONTROL 상승도] 및 [!UICONTROL 신뢰도] 에 올바르게 표시 [!DNL Target] UI. (TGT-46592, TGT-46554 및 TGT-46586)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
