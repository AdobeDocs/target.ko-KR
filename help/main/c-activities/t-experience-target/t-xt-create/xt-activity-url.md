---
keywords: 경험 타깃팅;xt;활동 url;url
description: 테스트에 사용되는 페이지를 결정하고 Adobe Target을 사용하여 경험 타깃팅 활동을 디자인할 때 열리는 활동 URL을 지정하는 방법을 알아봅니다.
title: Xt(경험 타깃팅) 활동에서 활동 URL은 무엇입니까?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 63%

---

# XT(경험 타깃팅) 활동의 활동 URL

다음 [!UICONTROL 활동 URL] 는 다음에서 사용되는 페이지를 결정합니다 [!DNL Adobe Target] [!UICONTROL 경험 타깃팅] (XT) 활동 및에서 열립니다. [!UICONTROL 시각적 경험 작성기] (VEC) 또는 [!UICONTROL 양식 기반 경험 작성기] 활동을 디자인할 때.

1. [XT 활동을 만드는](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) 동안 메시지가 표시되면 활동 URL을 지정합니다. 전체 URL(`https://` 포함)을 입력하고 **[!UICONTROL 활동 만들기]**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `https://www.adobe.com`]과 [!DNL `http://www.adobe.com`]은 모두 같습니다.
   >
   >기본적으로 VEC 또는 양식 기반 경험 작성기는 [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md). 활동을 만들 때 다른 페이지를 지정할 수 있습니다.
   >
   >Target Standard JavaScript 코드가 포함되지 않은 사이트 URL을 지정하면 페이지 요소를 선택할 수 없습니다.

1. (조건부) VEC가 열린 후에 다른 페이지를 표시하려면 **[!UICONTROL 구성]**&#x200B;을 클릭하고 **[!UICONTROL 페이지 전달]**&#x200B;을 선택한 다음 [!UICONTROL URL] 필드에 URL을 지정합니다.

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
