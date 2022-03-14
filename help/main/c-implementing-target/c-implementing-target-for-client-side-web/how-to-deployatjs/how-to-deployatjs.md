---
keywords: 구현;at.js;Javascript 라이브러리
description: Adobe 배포 방법 알아보기 [!DNL Target] Adobe Experience Platform에서 태그를 사용하거나 태그 관리자 없이 at.js JavaScript 라이브러리입니다.
title: at.js를 배포하려면 어떻게 합니까?
feature: Implement Server-side
role: Developer
exl-id: a11b916a-923e-43d2-af0f-8efde7cd547e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 17%

---

# at.js를 배포하는 방법

배포 방법에 대한 정보 [!DNL Adobe Target] JavaScript 라이브러리, at.js,에서 태그 사용 [!DNL Adobe Experience Platform] 태그 관리자 없이 또는

다음 방법을 사용하여 at.js를 배포할 수 있습니다.

* **[구현 [!DNL Target] 태그 사용 [!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: 의 태그 [!DNL Adobe Experience Platform] 는에서 차세대 태그 관리 기능입니다 [!DNL Adobe]. 태그는 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

   >[!NOTE]
   >
   >[!DNL Adobe Experience Platform Launch] 가 [!DNL Adobe Experience Platform]의 데이터 수집 기술군으로 새롭게 브랜딩되었습니다. 그 결과로 제품 설명서 전반에서 몇 가지 용어 변경이 있었습니다. 다음을 참조하십시오 [문서](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) 용어 변경 내용을 통합 참조하기 위해.

* **[태그 관리자 없이 Target 구현](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: 태그 관리자(예: 의 태그)를 사용하지 않고 Target을 구현할 수 있습니다 [!DNL Adobe Experience Platform]).
* **타사 태그 관리자를 사용하여 Target 구현**: [의 태그 [!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) is the preferred method to implement Target; however, you can also implement Target using a third-party tag manager, including Tealium, Ensighten, and Google Tag. For a list of benefits of using Launch, see [Advantages of implementing at.js using the [!DNL Adobe Target] 확장](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304).

   그러나 구현 방법을 알고 있는 경우 [!DNL Target] 태그 관리자를 사용하지 않으면 사이트 코드에서 at.js를 하드 코딩하는 대신 타사 태그 관리자를 사용하여 쉽게 구현할 수 있습니다.

   다음은 구현에 도움이 되는 두 가지 관련 주제입니다 [!DNL Target] 타사 태그 관리자 사용:

   * [구현하기 전에](/help/main/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [구현 [!DNL Target] 태그 관리자 없이](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   자세한 내용은 타사 태그 관리자에 대한 설명서를 확인하십시오.

구현하려면 [!DNL Target] 단일 페이지 앱(SPA)을 사용할 때 [단일 페이지 애플리케이션 구현](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).
