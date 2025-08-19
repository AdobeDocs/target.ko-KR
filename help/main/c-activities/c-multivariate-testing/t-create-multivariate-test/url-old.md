---
keywords: 다변량 테스트;활동 url
description: '[!UICONTROL Multivariate Test] 활동이  [!DNL Adobe Target]을(를) 사용하여 디자인될 때 열리는 테스트에 사용되는 페이지를 결정하는 활동 URL을 지정하는 방법을 알아봅니다.'
title: '[!UICONTROL Multivariate Test]​(MVT) 활동의 활동 URL은 무엇입니까?'
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 34%

---

# 활동 URL

활동 URL은 [!UICONTROL Multivariate Test]&#x200B;(MVT)에 사용되는 페이지를 결정하며 테스트가 [!DNL Adobe Target]에 디자인될 때 열립니다.

다음 [활동을 만들](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) 때 메시지가 표시되면 활동 URL을 지정하십시오. 전체 URL(`https://` 포함)을 입력한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `https://www.adobe.com`] 및 [!DNL `http://www.adobe.com`]이(가) 모두 일치합니다.

기본적으로 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)은 [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

VEC가 열린 후에 다른 페이지를 표시하려면 **[!UICONTROL Configure]** 아이콘을 클릭한 다음 **[!UICONTROL Page Delivery]**&#x200B;을(를) 선택하고 URL을 지정하십시오.

![페이지 전달 대화 상자](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL Add Template Rule]**&#x200B;을(를) 클릭하십시오.

추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

* URL
* 도메인
* 경로
* 해시(#) 조각
* 쿼리
* 매개 변수

추가 규칙은 AND 또는 OR로 활동 URL에 조인할 수 있습니다. 추가하는 모든 규칙은 AND로 서로 평가됩니다.

완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>[!DNL Target] JavaScript 코드가 포함되지 않은 사이트 URL을 입력하면 페이지 요소를 선택할 수 없습니다.

기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. **[!UICONTROL Render using JavaScript]**&#x200B;을(를) 사용하여 해당 요소를 변경하려면 [!UICONTROL Visual Experience Composer]을(를) 끌 수 있습니다.

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.
