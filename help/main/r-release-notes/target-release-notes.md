---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 04d4cf13e0054a767e9bf08770cdace1e130067f
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 49%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2023년 3월 20일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 23.3.1(2023년 3월 28~30일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **3월 28일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 29일**: 아시아 태평양(APAC) 지역
* **3월 30일**: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
|--- |--- |
| 헤드리스 개인화 및 실험을 위한 AEM 컨텐츠 조각 | 사용 [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 컨텐츠 조각] in [!DNL Target] 활동. AEM의 편의성과 기능을 강력한 AI(인공 지능) 및 ML(기계 학습) 기능과 결합할 수 있습니다. [!DNL Target] 경험을 규모에 맞게 테스트 및 개인화합니다. |
| 최적화된 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅]에 대한 A4T 지표 | [!DNL Target]을 사용하면 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅] 활동에 대한 [!UICONTROL A4T]를 사용할 때 이항 이벤트 또는 연속 이벤트를 기반으로 지표를 선택할 수 있습니다.<P>다음은 유의해야 할 지원되는 지표에서의 변경 내용입니다.<ul><li>[!DNL Target]은 2023년 9월 9일까지의 기존 활동에 대한 이전 동작을 유지했습니다. 이 날짜 이후에는 기존 활동을 새 동작으로 강제 마이그레이션하기 위해 지원되지 않는 지표를 사용하는 활동이 중단됩니다.</li></ul> |
| [!UICONTROL Analytics for Target](A4T)을 사용하는 [!UICONTROL 자동 할당] | 업데이트된 자습서:<ul><li>[[!UICONTROL 자동 할당] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Analytics for Target](A4T)을 사용하는 [!UICONTROL 자동 타겟팅] | 업데이트된 자습서:<ul><li>[[!UICONTROL 자동 타겟팅] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

* 에서 항목을 만들 수 있도록 대상 및 활동 동기화가 개선되었습니다. [!DNL Adobe Experience Platform] 및 [!DNL Adobe Audience Manager] 다음에서 사용 가능합니다. [!DNL Target] UI 를 더 빨리 (TGT-44568)
* 사용자가 [!UICONTROL 기본 URL] 아래에 [!UICONTROL 관리] > [!UICONTROL 시각적 경험 작성기] > [!UICONTROL 기본 URL]. 이 변경 사항을 통해 고객은 기본 URL을 다시 빈 문자열로 변경할 수 있습니다. 이 문자열은 이전에 초기 구성 이후에 사용할 수 없었습니다. (TGT-44577)
* 고객이 기본 제공 대상(예약된 이름이 있는 대상)을 편집하거나 삭제할 수 없는 제한을 제거했습니다. (TGT-44655)
* &quot;[!UICONTROL 완료]회전자를 로드하는 동안 &quot; 옵션이 [!DNL Target] 작성 시 UI [결합된 대상](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* 수정 사항 [!UICONTROL 언어] 의 맨 아래에 있는 링크 [!UICONTROL 대상] 페이지를 사용하여 &quot;[!UICONTROL 계정 통신 환경 설정]&quot; 페이지에서 참조할 수 있습니다. (TGT-43562)
* 가끔 고객이 [!UICONTROL A/B 테스트] 활동 을 선택한 후 [!UICONTROL Adobe Analytics] 옵션 아래의 [!UICONTROL 관리] > [!UICONTROL 보고] > [!UICONTROL 보고 Experience Cloud 솔루션]. (TGT-44844)
* 고객이 [!UICONTROL 다변량 테스트] 내에서 많은 경험을 가진 활동 [!UICONTROL 시각적 경험 작성기] (VEC). 다음 [DOM 경로](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) VEC 하단에서 고객이 마지막 경험을 보지 못하는 경우가 있습니다. (TGT-44578)
* 페이지에 인증이 필요하거나 리디렉션을 호출하는 경우 VEC의 찾아보기 URL이 일반 브라우저 세션에 표시되는 현재 페이지를 반영하지 않는 문제를 해결했습니다. (TGT-44350)
* 고객이 [!UICONTROL 호환되지 않는 기준 필터링] 설정 [!UICONTROL Recommendations] > [!UICONTROL 설정]. (TGT-44398)
* POST 요청이 새 [!DNL Recommendations] 을 사용할 때 피드가 실패합니다 [!UICONTROL Analytics 분류] 이름에 점이 있는 보고서 세트 포함. (TGT-44598)
* 에서 링크가 업데이트되었습니다. [!DNL Target] 새 페이지를 가리키는 UI [시각적 편집 도우미 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* SSRF(Server-Side Request Forgery)가 [!DNL Recommendations] 피드 를 참조하십시오. (TGT-43769)
* 고객이 의 미리 보기 이미지를 볼 수 없는 문제를 해결했습니다 [!DNL Recommendations] 이미지 이름에 가 포함된 경우 디자인 [GB18030 문자](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* 일부 항목이 [GB18030 문자](https://en.wikipedia.org/wiki/GB_18030){target=_blank} 탈출하다 [!UICONTROL 수정 사항] 편집하는 동안 패널 [!UICONTROL 텍스트/HTML] 활동 [!UICONTROL 경험] 페이지.
* [!DNL Target] UI 전반에 걸쳐 다양한 현지화 수정을 수행했습니다.


## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
