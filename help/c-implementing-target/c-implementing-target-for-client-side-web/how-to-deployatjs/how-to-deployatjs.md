---
keywords: 구현;at.js;Javascript 라이브러리
description: Adobe Experience Platform Launch을 사용하거나 태그 관리자 없이 Adobe [!DNL Target] at.js JavaScript 라이브러리를 배포하는 방법을 알아봅니다.
title: at.js를 배포하려면 어떻게 합니까?
feature: 서버측 구현
role: Developer
exl-id: a11b916a-923e-43d2-af0f-8efde7cd547e
source-git-commit: 82629fb4c543220796fc99d9c034ebb725e1a645
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 6%

---

# at.js를 배포하는 방법

[!DNL Adobe Experience Platform]에서 태그를 사용하거나 태그 관리자를 사용하지 않고 [!DNL Adobe Target] JavaScript 라이브러리를 배포하는 방법에 대한 정보입니다.

다음 방법을 사용하여 at.js를 배포할 수 있습니다.

* **[ [!DNL Target]  [!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**&#x200B;에서 태그를 사용하여 구현: 의 태그 [!DNL Adobe Experience Platform] 는 의 차세대 태그 관리 기능입니다 [!DNL Adobe]. 태그는 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

   >[!NOTE]
   >
   >[!DNL Adobe Experience Platform Launch] 는에서 데이터 수집 기술 세트로 브랜드 재지정되었습니다 [!DNL Adobe Experience Platform]. 그 결과 제품 설명서에서 몇 가지 용어 변경 사항이 롤아웃되었습니다. 용어 변경 내용을 통합 참조하려면 다음 [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en)을 참조하십시오.

* **[태그 관리자 없이 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: 태그 관리자(예: 의 태그)를 사용하지 않고 Target을 구현할 수  [!DNL Adobe Experience Platform]있습니다.
* **타사 태그 관리자를 사용하여 Target 구현**:  [Target [!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) 를 구현하는 기본 방법은 태그입니다. 그러나 Tealium, Ensiten 및 Google Tag를 포함한 타사 태그 관리자를 사용하여 Target을 구현할 수도 있습니다. Launch 사용의 이점 목록은 [확장 [!DNL Adobe Target] 을 사용하여 at.js를 구현할 때의 이점 목록을 참조하십시오.](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304)

   그러나 태그 관리자 없이 [!DNL Target]을 구현하는 방법을 알고 있는 경우 사이트 코드에서 at.js를 하드 코딩하는 대신 타사 태그 관리자로 쉽게 구현할 수 있습니다.

   다음은 타사 태그 관리자를 사용하여 [!DNL Target]을 구현하는 데 도움이 되는 두 가지 관련 주제입니다.

   * [구현하기 전에](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [태그 관리자 없이  [!DNL Target] 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   자세한 내용은 타사 태그 관리자에 대한 설명서를 확인하십시오.

단일 페이지 앱(SPA)을 사용할 때 [!DNL Target]을 구현하려면 [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)을 참조하십시오.
