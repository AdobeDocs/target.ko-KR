---
description: 활동 URL는 경험 타깃팅 활동에 사용되는 페이지를 결정하며, 활동이 디자인할 때 Visual Experience Composer (VEC) 또는 양식 기반 경험 작성기에서 열립니다.
keywords: 타겟 지정
seo-description: 활동 URL는 경험 타깃팅 활동에 사용되는 페이지를 결정하며, 활동이 디자인할 때 Adobe Target Visual Experience Composer (VEC) 또는 양식 기반 경험 작성기에서 열립니다.
seo-title: 활동 URL
solution: Target
title: 활동 URL
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 활동 URL{#activity-url}

활동 URL는 경험 타깃팅 (XT) 활동에서 사용되는 페이지를 결정하며, 활동이 디자인할 때 Visual Experience Composer (VEC) 또는 양식 기반 경험 작성기에서 열립니다.

1. When prompted while [creating an XT activity](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specify the activity URL. 전체 URL(`https://` 포함)을 입력하고 **[!UICONTROL 활동 만들기]** 를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `https://www.adobe.com`]과 [!DNL `http://www.adobe.com`]은 모두 같습니다.
   >
   >By default, the VEC or Form-Based Experience Composer opens the page that is specified in your [Account Preferences](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). 활동을 만들 때 다른 페이지를 지정할 수 있습니다.
   >
   >Target Standard JavaScript 코드를 포함하지 않는 사이트의 URL를 지정하는 경우 페이지 요소를 선택할 수 없습니다.

1. (Conditional) To display a different page after the VEC opens, click **[!UICONTROL Configure]**, select **[!UICONTROL Page Delivery]**, and specify the URL in the [!UICONTROL URL] field.

   ![페이지 배달 대화 상자](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.

1. (Conditional) Click **[!UICONTROL Add Template Rule]** to add more pages or sections to the activity.

   추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

   * URL
   * 도메인
   * 경로
   * 해시(#) 조각
   * 쿼리
   * mbox 매개 변수
   추가 규칙은 AND 또는 OR을 사용하여 활동 URL에 결합할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

1. 완료되면 **[!UICONTROL 저장]을 클릭합니다.**