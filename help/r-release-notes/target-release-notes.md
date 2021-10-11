---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f6efc1e921535abdd11501979d6f44e84e443a1f
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 55%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2021년 10월 11일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.10.2(2021년 10월 13일)

[!DNL Target] [!UICONTROL Audiences]를 [!DNL Adobe Experience Platform Web SDK]와 함께 사용할 때 다음과 같은 개선 사항이 추가되었습니다.

* [!DNL Target] UI의 다양한 위치에 경고 아이콘, 팝오버 및 메시지를 추가하여 대상자가 소스에서 삭제되었으며 더 이상 [!DNL Target] 활동에서 사용할 수 없음을 나타냅니다.

   다음 그림은 아이콘, 팝오버 및 메시지가 표시되는 몇 가지 위치를 보여줍니다.

   *  Activitylist 페이지

      ![활동 목록 페이지의 소스 메시지에서 삭제된 대상](assets/deleted-at-source-audiences-list.png)

   * 활동 [!UICONTROL 개요] 페이지:

      ![개요 페이지의 소스 메시지에서 삭제된 대상](assets/deleted-at-source-overview.png)

   *  활동 만들기 워크플로우의 경험 단계:

      ![경험 페이지의 소스 메시지에서 삭제된   대상](assets/deleted-at-source-experiences.png)

   *  활동 생성 워크플로우의 타깃팅 단계:

      ![타겟 페이지의 소스 메시지에서 삭제된   대상](assets/deleted-at-source-targeting.png)

   * [!UICONTROL 활동 ] 생성 워크플로우의 목표 및 설정 단계:

      ![목표 및 설정 페이지에서 소스 메시지 [!UICONTROL 에서 삭제된 ] 대상](assets/deleted-at-source-goals-settings.png)

   * 대상 개선([!UICONTROL 활동 생성 워크플로우의 [!UICONTROL 타깃팅] 단계에서 대상 바꾸기):]

* 대상 결합 기능을 사용하려고 하며 소스에서 대상 중 하나가 삭제된 경우 [!UICONTROL 저장]이 비활성화됩니다.

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
