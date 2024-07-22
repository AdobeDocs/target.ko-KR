---
keywords: 권장 사항 디자인;템플릿;디자인 만들기;전달;출력
description: Adobe [!DNL Target] Recommendations에서 디자인을 사용하여 권장 사항이 페이지에 표시되는 방식(1X4, 1X6, 2X2 등)을 정의하는 방법에 대해 알아봅니다.
title: Recommendations에서 디자인을 사용하는 방법
feature: Recommendations
exl-id: 348b1d77-49c9-4a6b-ba85-7ba051713d5b
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 19%

---

# 디자인 개요

[!DNL Adobe Target Recommendations]의 디자인은 페이지에 권장 사항이 표시되는 방식을 정의합니다. 디자인은 권장 사항의 레이아웃과 형식을 정의하여 방문자 참여, 전환 및 매출을 향상시킵니다.

[!DNL Recommendations]에는 몇 가지 기본(빌드 전) 디자인이 포함되어 있거나 직접 만들 수 있습니다.

[!DNL Target]은(는) 다음 그림과 같이 권장 사항의 전체 모양과 느낌을 제공할 수 있습니다. 디자인에는 HTML, JavaScript 및 CSS가 포함될 수 있습니다. 이 디자인을 4 x 1 디자인이라고 합니다. 한 행에 4개의 공백을 포함합니다.

![velocity_example 이미지](assets/velocity_example.png)

또한 Target은 이메일 메시지, IoT(사물인터넷) 장치, 콘솔 또는 음성 사용 사례(Amazon Alexa 또는 Google Home)에서 사용할 수 있는 JSON 개체로서 권장 사항을 전송할 수도 있습니다.

디자인은 다음을 결정하는 데 도움이 됩니다.

* 권장 사항에 표시할 항목 수
* 항목을 표시할 방법(행, 열, 그리드 또는 테이블)
* 방문자에게 지정된 수의 항목만 표시하도록 제한할지 또는 방문자가 여러 항목을 스크롤할 수 있도록 제한할지 여부
