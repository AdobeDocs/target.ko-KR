---
keywords: Multivariate Tests;activity url
description: 활동 URL은 Adobe Target MVT(Multivariate Test)에 사용되는 페이지를 결정하며 테스트가 Adobe Target에서 디자인될 때 열립니다.
title: 활동 URL
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 84%

---


# 활동 URL{#activity-url}

활동 URL은 MVT([!UICONTROL 다변량 테스트])에 사용되는 페이지를 결정하며 테스트가 [!DNL Adobe Target]에 디자인될 때 열립니다.

다음 [활동을 만들](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) 때 메시지가 표시되면 활동 URL을 지정하십시오. 전체 URL(`https://` 포함)을 입력하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `https://www.adobe.com`]과 [!DNL `http://www.adobe.com`]은 모두 같습니다.

기본적으로 [!UICONTROL VEC(Visual Experience Composer])는 [Visual Experience Composer 설정](/help/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

VEC가 열린 후 다른 페이지를 표시하려면 **[!UICONTROL 구성]** 아이콘을 클릭하고 **[!UICONTROL 페이지 배달]**&#x200B;을 선택한 다음 URL를 지정합니다.

![페이지 전달 대화 상자](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 템플릿 규칙 추가]**&#x200B;를 클릭합니다.

추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

* URL
* 도메인
* 경로
* 해시(#) 조각
* 쿼리
* 매개 변수

추가 규칙은 AND 또는 OR을 사용하여 활동 URL에 결합할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>Target Standard JavaScript 코드가 포함되지 않은 사이트 URL을 입력하면 페이지 요소를 선택할 수 없습니다.

기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 이러한 요소를 변경하려면 [!UICONTROL JavaScript를 사용하여 렌더링]을 끄면 됩니다.

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.