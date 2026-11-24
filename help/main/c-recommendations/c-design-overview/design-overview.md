---
keywords: 권장 사항 디자인;템플릿;디자인 만들기;전달;출력
description: Adobe [!DNL Target] Recommendations의 디자인을 사용하여 페이지에 권장 사항이 표시되는 방식(1X4, 1X6, 2X2 등)을 정의하는 방법에 대해 알아봅니다.
title: 디자인 시작
feature: Recommendations
exl-id: 348b1d77-49c9-4a6b-ba85-7ba051713d5b
TQID: 'https://experienceleague.adobe.com/08jboJLkp6MhgXiISjkVzh2kVze5DRrxO8BbQBFLeA4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: f9c9c7b2b78ec020fcabae420686b8955e350a0e
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 9%
---
# 디자인 시작 {#design-overview}

>[!BEGINSHADEBOX]

**이 페이지에서:** 디자인이 [!DNL Adobe Target Recommendations]에서 권장 사항의 레이아웃과 형식을 정의하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target Recommendations]의 디자인은 페이지에 권장 사항이 표시되는 방식을 정의합니다. 디자인은 권장 사항의 레이아웃과 형식을 정의합니다.

[!DNL Recommendations]에는 몇 가지 기본(사전 빌드된) 디자인이 함께 제공되며 사용자 지정 디자인도 만들 수 있습니다. 자세한 내용은 [디자인 만들기](/help/main/c-recommendations/c-design-overview/create-design.md)를 참조하십시오.

[!DNL Target]은(는) 다음 그림과 같이 권장 사항의 전체 모양과 느낌을 제공할 수 있습니다. 디자인은 HTML, JavaScript 및 CSS를 포함할 수 있습니다. 이 디자인을 4 x 1 디자인이라고 합니다. 한 행에 4개의 공백을 포함합니다.

![사진, 이름, 가격, 등급 및 거리를 각각 보여 주는 4개의 항목이 있는 &quot;기타 재미있는 활동&quot;이라는 제목의 4 x 1 디자인의 예](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

[!DNL Target]은(는) 이메일 메시지, IoT(사물인터넷) 장치, 콘솔 또는 음성 사용 사례(Amazon Alexa 또는 Google Home)에서 사용할 수 있는 JSON 개체로 권장 사항을 전송할 수도 있습니다.

디자인은 다음을 결정합니다.

* 권장 사항에 표시되는 항목 수
* 항목이 표시되는 방법(행, 열, 그리드 또는 테이블)
* 방문자가 지정된 수의 항목만 볼 수 있는지 또는 여러 항목을 스크롤할 수 있는지 여부
