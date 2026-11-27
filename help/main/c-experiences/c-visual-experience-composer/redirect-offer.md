---
keywords: 리디렉션;리디렉션 url;다른 페이지로 보내기
description: 방문자를 동일한 페이지에 콘텐츠를 표시하지 않고 다른 페이지로 보내려는 경우 Adobe [!DNL Target]에서 URL로 리디렉션 옵션을 사용하는 방법에 대해 알아봅니다.
title: 페이지를 다른 URL로 리디렉션할 수 있습니까?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
TQID: 'https://experienceleague.adobe.com/8Bh5z7SRWw3QqKQMHZck01GKVBtMufwLbw9JxLsSACU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 2%
---
# URL로 리디렉션 {#redirect-to-url}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL URL로 리디렉션]** 옵션을 사용하여 방문자를 같은 페이지에 콘텐츠를 표시하지 않고 다른 페이지로 보내는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL URL로 리디렉션]** 옵션이 방문자를 동일한 페이지에 콘텐츠를 표시하지 않고 다른 페이지로 보냅니다. 한 페이지 내의 콘텐츠 조각에 대한 변경 사항과 대조적으로 완전히 다른 두 페이지의 비교에 적합합니다. 그런 다음 A/B 테스트는 페이지 A와 페이지 B를 비교합니다. 한 경험은 기본 페이지 A를 가리키고 다른 경험은 페이지 B로 리디렉션됩니다.

리디렉션 오퍼는 브라우저를 리디렉션하는 JavaScript 코드를 실행합니다. 이 코드는 `window.location.replace();` 메서드를 사용하므로 방문자를 리디렉션하는 페이지는 브라우저 기록에 저장되지 않습니다. 따라서 방문자는 여전히 브라우저의 뒤로 버튼을 사용할 수 있습니다.

## 리디렉션 오퍼 만들기 {#create-redirect-offer}

리디렉션하는 경험은 방문자가 전송되는 페이지와 리디렉션 조건(선택 사항)을 정의합니다.

1. 경험을 만듭니다.

1. **[!UICONTROL 경험]** 프레임에서 리디렉션하는 경험에 대한 **[!UICONTROL 추가 작업]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg))을 클릭합니다.

1. **[!UICONTROL URL로 리디렉션]**&#x200B;을 클릭합니다.

   ![추가 작업 아이콘](assets/redirect_1.png)

1. **[!UICONTROL URL로 리디렉션]** 대화 상자에서 페이지 B의 URL을 입력합니다.

   ![추가 작업 아이콘](assets/redirect_2.png)

1. (선택 사항) 현재 쿼리 매개 변수를 포함하는 옵션을 선택합니다.

   이 옵션을 선택하면 방문자의 URL에서 `?` 뒤의 모든 내용이 리디렉션 시 리디렉션 URL에 추가됩니다.

## 제한

리디렉션 오퍼에는 다음 제한 사항이 있습니다.

* **A4T:** A4T를 사용하는 활동에서 리디렉션 오퍼를 사용하려면 특정 최소 요구 사항을 충족하는 구현이 필요하며 다른 중요한 정보가 적용됩니다. [리디렉션 오퍼 - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오.
* **양식 기반 경험 작성기:** 페이지의 일부인 mbox에서는 리디렉션 오퍼를 사용하지 않습니다. HTML `<head>`의 일부인 스크립트 태그에서만 리디렉션 오퍼를 사용하며, 항상 글로벌 mbox에 대해 자동 만들기를 사용하고 리디렉션 오퍼를 설정합니다.

>[!NOTE]
>
>랜딩 페이지의 레퍼러 값을 전달하려면 리디렉션 오퍼 대신 HTML 오퍼를 사용하십시오.

## 알려진 문제

at.js 구현의 리디렉션 활동으로 인해 오퍼가 반복적으로 전달되는 경우 미리보기 URL이 루프로 들어갈 수 있습니다. 대신 [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)를 사용하여 활동을 미리 보고 테스트하십시오. 이 문제는 오퍼의 실제 게재에는 영향을 주지 않습니다. (TGT-23019)
