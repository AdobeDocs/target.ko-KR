---
keywords: 다변량 테스트;활동 url
description: '[!UICONTROL 다변량 테스트] 활동이  [!DNL Adobe Target]을(를) 사용하여 디자인될 때 열리는 테스트에 사용되는 페이지를 결정하는 활동 URL을 지정하는 방법을 알아봅니다.'
title: '[!UICONTROL 다변량 테스트]​(MVT) 활동의 활동 URL은 무엇입니까?'
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
TQID: https://experienceleague.adobe.com/oQKwrlZ95XKEKSJIUiWqXXo9AJJzCb20gfS1rtwGImM
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 38%

---

# 활동 URL

활동 URL은 MVT([!UICONTROL Multivariate Test])에 사용되는 페이지를 결정하며 테스트가 [!DNL Adobe Target]에 디자인될 때 열립니다.

1. 다음 [활동을 만들](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) 때 메시지가 표시되면 활동 URL을 지정하십시오. 전체 URL(`https://` 포함)을 입력한 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `https://www.adobe.com`] 및 [!DNL `http://www.adobe.com`]이(가) 모두 일치합니다.

   기본적으로 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)는 [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

1. (조건부) VEC가 열린 후에 다른 페이지를 표시하려면 **[!UICONTROL 구성]** 아이콘을 클릭한 다음 **[!UICONTROL 페이지 배달]**&#x200B;을 선택하고 URL을 지정하십시오.

1. (조건부) 활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다.

   추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

   * [!UICONTROL &#x200B; URL]
   * [!UICONTROL 도메인]
   * [!UICONTROL 경로]
   * [!UICONTROL 해시(#) 조각]
   * [!UICONTROL 쿼리]
   * [!UICONTROL 사용자 지정]

   추가 규칙은 AND 또는 OR로 활동 URL에 조인할 수 있습니다. 추가하는 모든 규칙은 AND로 서로 평가됩니다.

   완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>[!DNL Target] JavaScript 코드가 포함되지 않은 사이트 URL을 입력하면 페이지 요소를 선택할 수 없습니다.
>
>기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. [!UICONTROL 시각적 경험 작성기]에서 이러한 요소를 변경하려면 **[!UICONTROL JavaScript를 사용하여 렌더링]**&#x200B;을 끄면 됩니다.

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.
