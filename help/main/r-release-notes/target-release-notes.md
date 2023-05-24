---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된  [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ecdb94a679e033d3ec030513fd66c9eea039195b
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 72%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target]릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 날짜: 2023년 5월 24일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target] Standard/Premium 23.5.2 (2023년 5월 31일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 프로필 API 인증 토큰을 생성하는 동안 빈 페이지가 표시되는 문제가 해결되었습니다. (TGT-45387)
* 이미지 이름에 GB 18030 문자가 포함된 경우 [!UICONTROL 디자인 만들기] 패널에 이미지를 표시할 수 없는 문제가 해결되었습니다. (TGT-44614)
* 분석 중에 [!UICONTROL 자동 개인화] 활동에 대한 보고서가 정지되는 문제가 해결되었습니다. (TGT-44820)
* 특정 고객에 대한 기본 작업 영역의 Target UI에 활동이 표시되지 않는 문제를 해결했습니다. (TGT-45286)
* &quot;중복 허용 안 함&quot; 플래그의 동작이 업데이트되었습니다. 제외된 반복 오퍼 플래그는 기본 콘텐츠 오퍼인 경우 반복 오퍼를 허용하도록 업데이트되고(API v3, v4의 경우), 옵션이 기본 콘텐츠 오퍼를 참조하고 템플릿이 정의되지 않은 경우 중복 옵션을 허용합니다. (TNT-46617)
* URL에 쿼리 매개 변수가 추가되어 페이지를 VEC(시각적 경험 작성기)에서 로드할 수 없는 문제를 해결했습니다. (TGT-44873)
* 경험의 텍스트/HTML에서 일부 문자가 잘못 이스케이프되는 문제가 수정되었습니다. (TGT-44600)

## [!DNL Target] Standard/Premium 23.5.3 (날짜 미정)

이번 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

| 기능 | 세부 사항 |
|--- |--- |
| [!UICONTROL Automated Personalization] 활동을 위한 [!UICONTROL QA 모드] | 이제 [!UICONTROL Automated Personalization] 활동에서 [!UICONTROL 링크 미리 보기] 기능을 대체하는 [!DNL Adobe Target] [!UICONTROL QA 모드]를 사용할 수 있습니다.<P>자세한 내용은 [활동 QA](/help/main/c-activities/c-activity-qa/activity-qa.md)를 참조하십시오. |
| [!DNL Target]과 공유되는 Real-Time CDP 프로필 속성 | Real-Time CDP 프로필 속성을 [!DNL Target]과 공유하여 HTML 및 JSON 오퍼에 사용할 수 있습니다.<P>자세한 내용은 [ [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes)과 Real-Time CDP 프로필 속성 공유를 참조하십시오. |

* 중복 기능을 허용하지 않도록 성능이 향상되었습니다(로드 시간 감소 포함). [제외 관리](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) 위치: [!UICONTROL Automated Personalization] 활동.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
