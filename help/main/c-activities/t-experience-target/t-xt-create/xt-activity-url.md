---
keywords: 경험 타깃팅;xt;활동 url;url
description: 을(를) 지정하는 방법 알아보기 [!UICONTROL 활동 URL] 테스트에 사용되는 페이지를 결정하며 [!UICONTROL 경험 타기팅] 활동은 다음을 사용하여 디자인되었습니다. [!DNL Adobe Target].
title: 이란? [!UICONTROL 활동 URL] 다음에서 [!UICONTROL 경험 타기팅] (XT) 활동
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 24513d8cb39d38dcfbc74bf40961d5517cc90a4b
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 48%

---

# 의 활동 URL [!UICONTROL 경험 타기팅] (XT) 활동

다음 [!UICONTROL 활동 URL] 에서 사용되는 페이지를 결정합니다. [!DNL Adobe Target] [!UICONTROL 경험 타기팅] (XT) 활동. 에 열리는 페이지입니다. [!UICONTROL 시각적 경험 작성기] (VEC) 또는 [!UICONTROL 양식 기반 경험 작성기] 활동을 디자인할 때입니다.

1. [XT 활동을 만드는](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) 동안 메시지가 표시되면 활동 URL을 지정합니다. 전체 URL(`https://` 포함)을 입력하고 **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `https://www.adobe.com`]과 [!DNL `http://www.adobe.com`]은 모두 같습니다.
   >
   >기본적으로 VEC 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 에 지정된 페이지를 엽니다. [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md). 활동을 만들 때 다른 페이지를 지정할 수 있습니다.
   >
   >를 포함하지 않는 사이트의 URL을 지정하는 경우 [[!DNL Target] at.js JavaScript 라이브러리 또는 [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank}, 페이지 요소는 선택할 수 없습니다.

1. (조건부) VEC가 열린 후 다른 페이지를 표시하려면 을 클릭합니다 **[!UICONTROL 구성]**, 선택 **[!UICONTROL 페이지 전달]**&#x200B;을(를) 만든 다음 [!UICONTROL URL] 필드.

   ![페이지 전달 대화 상자](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.

1. (조건부) 활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 템플릿 규칙 추가]**&#x200B;를 클릭합니다.

   추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

   * URL
   * 도메인
   * 경로
   * 해시(#) 조각
   * 쿼리
   * mbox 매개 변수

   추가 규칙은 AND 또는 OR을 사용하여 활동 URL에 결합할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
