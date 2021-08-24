---
keywords: 모바일 앱;자주 묻는 질문;faq;target 모바일 앱
description: 모바일 앱용 Adobe [!DNL Target] 에 대한 FAQ와 답변을 봅니다.
title: 모바일 앱용 [!DNL Target] 에 대한 Faq는 무엇입니까?
feature: 모바일 구현
role: Developer
exl-id: 1ddd8345-e753-4608-9293-939e092cb16d
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# 모바일 앱을 위한 Target FAQ

모바일 앱용 [!DNL Target]에 대한 FAQ 목록입니다.

## [!DNL Adobe Experience Platform]에서 태그를 사용하여 SDK를 배포해야 합니까? 아니면 [!DNL Launch]를 사용하지 않고 SDK를 배포할 수 있습니까?

SDK는 [Adobe Marketing Cloud git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)에서 사용할 수 있습니다. Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)에서 [태그를 사용하지 않는 경우, 자체 설정 파일을 관리하고 앱에서 관리해야 합니다.

## 현재 사용 가능한 SDK는 무엇입니까?

Adobe Experience Platform Mobile SDK는 현재 iOS, Android 및 React를 지원합니다. 자세한 내용은 [Adobe Experience Cloud Platform Mobile SDK 안내서](https://aep-sdks.gitbook.io/docs/)를 참조하십시오.

## 위도와 경도에 대한 확인 측면에서 위치 기반 기능의 빈도는 얼마입니까?

자세한 내용은 [위치 Adobe 설명서](https://placesdocs.com/places-services-by-adobe-documentation/)를 참조하십시오.

## Adobe Experience Platform Mobile SDK가 작동하려면 at.js가 필요합니까?

아니요. Mobile SDK를 사용하기 위해 at.js가 필요하지 않습니다. at.js는 웹 사이트용 [!DNL Target] JavaScript 라이브러리입니다. Adobe Experience Platform Mobile SDK는 모바일 앱용입니다.

## [!DNL Target] Mobile이 Adobe [!DNL Target] Premium 제품 SKU의 기능만 됩니까?

아니오. [!DNL Adobe Target Standard] 고객의 경우 A/B 테스트 및 경험 타깃팅(XT) 활동에만 Mobile SDK를 사용할 수 있으며, [!DNL Target Standard] 모바일 앱 추가 기능이 있습니다. 모바일 앱에서 Recommendations 또는 AI 기반 기능을 사용하려면 [Adobe Target Premium](/help/c-intro/intro.md#premium) 라이센스가 있어야 합니다.

## Adobe Experience Manager(AEM)과 [!DNL Target] 모바일 활동 간에 모바일 앱 통합이 있습니까?

로드맵에 있지만 아직 일정이 없습니다. 현재, AEM에서 Target으로 JSON [경험 조각](/help/c-experiences/c-manage-content/aem-experience-fragments.md)을 공유할 수 있으며 모바일 앱 활동에서 이러한 조각을 사용할 수 있습니다.
