---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 6957eb88e2ee7d54fdad5afeaedf75b091b601e7
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 36%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**최근 업데이트: 2021년 9월 14일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.9.1(2021년 9월 14일)

이 유지 보수 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

* 일부 웹 브라우저에서 타사 쿠키에 대한 새 보안 정책으로 인해 고객이 [!UICONTROL 시각적 경험 작성기] (VEC)에 로그인하지 못하는 문제를 해결했습니다. 이 문제는 [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)에서 Google Chrome 버전 80+를 사용할 때 &quot;VEC(시각적 경험 작성기) 또는 EEC(고급 경험 작성기)에서 페이지가 로드되지 않음&quot;에 설명되어 있습니다.
* VEC에 있는 오퍼 이름에 오퍼의 친숙한 이름 대신 오퍼의 경로가 표시되던 문제를 수정했습니다. (TGT-41300)
* 중복 활동의 프로모션에서 엔티티 ID 변경 사항을 원래 활동에 잘못 적용하는 [!DNL Recommendations]의 문제를 수정했습니다. (TGT-41482)
* VEC의 [!DNL Recommendations] 활동에 대한 [!UICONTROL 경험] 페이지에 &quot;기준 편집&quot; 단추가 제대로 표시되지 않는 문제를 수정했습니다. (TGT-39512)
* 복제 및 테스트 작업 공간에 복사할 때 활동 동기화를 방지할 수 있는 문제를 수정했습니다. (TGT-40686)
* VEC에서 &quot;[!UICONTROL 다음 항목 뒤에 삽입]&quot;을 사용할 때 [경험 구성요소](/help/c-experiences/c-manage-content/aem-experience-fragments.md)가 있는 선택기를 수정할 수 없는 문제를 해결했습니다. (TGT-41802)
* 오퍼의 빈 JSON 콘텐츠가 백엔드로 전송되지 않는 문제를 해결했습니다. [!DNL Target] 는 비어 있더라도 JSON 개체를 전송합니다. (TGT-41555)
* 고객이 보고서를 보는 동안 Analytics]에서 &quot;[!UICONTROL 보기&quot;를 클릭할 때 [!DNL Analysis Workspace] 대신 이전 [!DNL Analytics] 보고가 열리던 문제를 수정했습니다. (TGT-41867)
* 고객이 [!UICONTROL Automated Personalization] 활동에 대한 보고 소스(A4T)로 [!DNL Analytics]을 선택하려고 할 때 표시되는 UI 메시지에 추가 설명이 추가되었습니다. 메시지에 &quot;[!DNL Target]이 [!UICONTROL Automated Personalization] 활동에 대해 지원되는 유일한 소스라고 표시됩니다.&quot; (TGT-41954)
* 고객이 쉼표 대신 &quot;줄바꿈&quot;으로 호스트를 구분하려고 할 때 오류 메시지에 추가 설명이 추가되었습니다. (TGT-40671)
* [!DNL Platform] 및 [!DNL AAM]([!DNL Adobe Audience Manager])를 정확하게 포함하도록 세그먼트의 [!UICONTROL 유형] 필드를 업데이트했습니다. (TGT-41328)
* [!UICONTROL 저장]을 클릭한 후 트래픽 소스 피연산자가 변경되는 문제를 해결했습니다. (TGT-41408)
* 활동 전용 대상을 저장(규칙 기반 또는 결합)한 후, 이제 UI가 활동 전용 필터가 적용된 [!UICONTROL Audience] 선택기를 로드합니다. (TGT-41747).
* 소스([!DNL Adobe Experience Platform], [!UICONTROL AAM] 등)에서 삭제된 대상이 [!DNL Target] UI에 계속 표시되던 문제를 해결했습니다.
* [!DNL Adobe Experience Platform]대상] 페이지에 [!UICONTROL 에서 가져온 대상만 표시하는 필터 옵션을 추가했습니다. (TGT-41298)
* [!UICONTROL 대상] UI에 향상된 키보드 액세스 가능성 옵션이 추가되었습니다. (TGT-39927)
* 일부 활동의 &quot;[!UICONTROL 최근 업데이트]&quot; 날짜가 스페인어 및 일본어 고객을 위한 영어 UI와 달라지는 문제를 해결했습니다(스페인어 및 일본어로 UI를 볼 때). (TGT-38980)

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
