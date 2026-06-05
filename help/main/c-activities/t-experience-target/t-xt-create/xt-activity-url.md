---
keywords: 경험 타깃팅;xt;활동 url;url
description: '[!UICONTROL 경험 타깃팅] 활동이  [!DNL Adobe Target]을(를) 사용하여 디자인될 때 열리는 테스트에 사용되는 페이지를 결정하는 [!UICONTROL 활동 URL]을(를) 지정하는 방법을 알아봅니다.'
title: '[!UICONTROL 경험 타깃팅]​(XT) 활동에서 [!UICONTROL 활동 URL]은(는) 무엇입니까?'
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
TQID: https://experienceleague.adobe.com/igvyk-2atEe7JdYuFj3IXlXyE1CzVkLuwv50DSmSxuY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 35%

---

# [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동의 활동 URL

[!UICONTROL 활동 URL]은(는) [!DNL Adobe Target] [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동에서 사용되는 페이지를 결정합니다. 활동을 디자인할 때 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC) 또는 [!UICONTROL 양식 기반 경험 작성기]에서 열리는 페이지입니다.

1. [XT 활동을 만드는](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) 동안 메시지가 표시되면 활동 URL을 지정합니다. 전체 URL(`https://` 포함)을 입력한 다음 **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `https://www.adobe.com`] 및 [!DNL `http://www.adobe.com`]이(가) 모두 일치합니다.
   >
   >기본적으로 VEC 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)는 [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.
   >
   >[[!DNL Target] at.js JavaScript 라이브러리 또는 [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=ko){target=_blank}이(가) 포함되지 않은 사이트 URL을 지정하면 페이지 요소를 선택할 수 없습니다.

1. (조건부) VEC가 열린 후에 다른 페이지를 표시하려면 **[!UICONTROL 구성]**&#x200B;을 클릭하고 **[!UICONTROL 페이지 배달]**&#x200B;을 선택한 다음 [!UICONTROL URL] 필드에 URL을 지정하십시오.

   >[!NOTE]
   >
   >페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.

1. (조건부) 활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다.

   추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

   * URL
   * 도메인
   * 경로
   * 해시(#) 조각
   * 쿼리
   * mbox 매개 변수

   추가 규칙은 AND 또는 OR을 사용하여 활동 URL에 결합할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
