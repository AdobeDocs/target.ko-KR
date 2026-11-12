---
keywords: 활동 url;url;다른 url
description: A/B, 경험 타기팅 또는 다변량 테스트 활동에서 [!UICONTROL 활동 URL]을 설정하여 테스트 페이지를 정의하고 정확한 테스트 디자인을 보장하는 방법을 알아봅니다.
title: A/B, 경험 타기팅 또는 다변량 테스트 활동의 활동 URL이란 무엇입니까?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
reason: republish
TQID: 'https://experienceleague.adobe.com/arQWsSfBKYtrayq9AI8ejU1T-Uor-oL5j2Sp2JKKXZE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aad553690f1f399177214c94a2276d038f46d9cb
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 25%
---
# 활동 URL {#ab-activity-url}

>[!BEGINSHADEBOX]

**이 페이지에서:** A/B, XT(경험 타기팅) 또는 MVT(다변량 테스트) 활동의 활동 URL을 지정하는 방법, 다른 페이지를 표시하는 방법 및 더 많은 페이지 또는 섹션에 대한 규칙을 추가하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!UICONTROL 활동 URL]은(는) 활동에 사용되는 페이지를 결정합니다. 활동이 [!DNL Adobe Target]에서 디자인될 때 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC) 또는 [!UICONTROL 양식 기반 경험 작성기]에서 열리는 페이지입니다.

## 활동 URL 지정 {#specify-url}

활동을 만들 때 메시지가 표시되면 활동 URL을 지정하십시오. 전체 URL(`https://` 포함)을 입력한 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

>[!NOTE]
>
>[!DNL Target]은(는) URL 프로토콜([!DNL https] 및 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `http://www.adobe.com/kr`] 및 [!DNL `https://www.adobe.com/kr`]이(가) 모두 일치합니다.

[!DNL Target] [at.js JavaScript 라이브러리 또는 [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=ko){target=_blank}이(가) 포함되지 않은 사이트 URL을 지정하면 페이지 요소를 선택할 수 없습니다.

## 다른 페이지 표시 {#different-page}

기본적으로 VEC 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)는 [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

VEC가 열린 후 다른 페이지를 표시하려면 다음을 수행하십시오.

1. **[!UICONTROL 경험]** 페이지에서 페이지 상단의 **[!UICONTROL 구성]**&#x200B;을 클릭한 다음 **[!UICONTROL 페이지 배달]**&#x200B;을 선택합니다.

1. **[!UICONTROL URL]** 필드에 URL을 지정하십시오.

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. VEC를 사용하여 이러한 요소를 변경하려면 **[!UICONTROL JavaScript을 사용하여 렌더링]**&#x200B;을 끄면 됩니다.

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.

## 더 많은 페이지 또는 섹션에 대한 규칙 추가 {#add-rules}

활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 페이지 배달]** 설정에서 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭한 다음, 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

* URL
* 도메인
* 경로
* 해시(#) 조각
* 쿼리
* mbox 매개 변수
* 사용자 정의

추가 규칙은 AND 또는 OR로 활동 URL에 조인할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.
