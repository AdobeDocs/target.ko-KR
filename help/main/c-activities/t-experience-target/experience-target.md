---
keywords: 타깃팅;경험 타깃팅;xt;랜딩 페이지;랜딩 페이지 캠페인
description: '[!DNL Adobe Target]의 [!UICONTROL 경험 타깃팅](XT) 활동을 사용하여 마케터가 정의한 규칙 및 기준에 따라 특정 대상에게 콘텐츠를 전달하는 방법을 알아봅니다.'
title: '[!UICONTROL 경험 타깃팅](XT) 활동이란 무엇입니까?'
feature: Experience Targeting
exl-id: 416d8941-d4de-487f-8fd2-27806b73a63c
TQID: 'https://experienceleague.adobe.com/PCTBCP2tGaNZSIAScWLR84B6an42E-2PJ1Ijm0tHrn4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
    internal-label: Experience design
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: aaa094f4f36b6088ca180637d8054b6d5ff59d60
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%
---
# [!UICONTROL 경험 타깃팅] 시작 {#get-started-xt}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 경험 타깃팅]**&#x200B;이 무엇인지, 개인화에 어떻게 적합한지, 시나리오가 다른 경험을 가진 다양한 대상을 타깃팅하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!UICONTROL 경험 타깃팅]&#x200B;(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다. 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 [지역 타깃팅](/help/main/c-target/c-audiences/c-target-rules/geo.md)을 포함한 규칙을 정의하는 데 유용합니다. 단일 활동에서 여러 규칙을 정의하여 다른 대상자에게 다양한 콘텐츠 변형을 전달할 수 있습니다.

방문자가 사이트를 볼 때 [!UICONTROL 경험 타기팅]은(는) 이러한 방문자를 평가하여 설정된 기준을 충족하는지 여부를 판단합니다. 기준을 충족하면 활동을 시작하고 자격을 갖춘 대상자를 위해 디자인된 경험이 표시됩니다.

[!UICONTROL 경험 타깃팅]은(는) 개인화 환경의 첫 번째 단계이며 종종 A/B 테스트부터 시작됩니다. 마케터는 A/B 테스트를 실행하고, 보고 대상을 사용하여 서로 다른 경험이 서로 다른 대상과 공감한다는 것을 발견합니다. [!UICONTROL 경험 타깃팅]을 통해 마케터는 해당 검색을 쉽게 사용하고 컨텐츠의 장기적인 타깃팅을 다른 대상 세그먼트로 전환할 수 있습니다.

## 시나리오: A/B 테스트부터 경험 타깃팅까지 {#xt-scenario}

웹 사이트에 야외 장비가 있다고 가정합니다. A/B 테스트에 대한 보고서는 서로 다른 대상과 공감하는 세 가지 경험이 있음을 나타냅니다. 이 검색을 적용하려면 홈 페이지에 방문자의 위치나 취미에 따라 각 대상에게 흥미를 일으키는 다른 영웅 이미지를 표시해야 합니다. 뉴저지주 방문자에게 하이킹 이미지를, 하와이 방문자에게 서핑 이미지를, 자전거 타기를 좋아하는 대상자에게 세 번째 이미지를 표시하려고 합니다.

[!UICONTROL 경험 타깃팅] 활동을 사용하면 각각에 대해 다른 영웅 이미지로 이 세 대상을 타깃팅할 수 있습니다. 다음 비디오에서는 [!UICONTROL 경험 타기팅]을 통해 A/B 테스트를 한 단계 업그레이드하는 방법에 대해 설명합니다. 다음 방법을 보여 줍니다.

* 안내가 있는 3단계 워크플로우를 사용하여 [!UICONTROL 경험 타깃팅] 활동을 구성합니다.
* 두 가지 상태 모두를 대상으로 하는 경험과 사이클링 애호가를 대상으로 하는 세 번째 경험을 만들어 서로 다른 지리적 영역의 대상자에게 위치 특정 콘텐츠를 제공합니다.
* 세 가지 경험을 재정렬하여 올바른 콘텐츠가 올바른 대상에게 전달되도록 하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

비디오를 시청한 후 [경험 타깃팅 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)를 계속 진행합니다.
