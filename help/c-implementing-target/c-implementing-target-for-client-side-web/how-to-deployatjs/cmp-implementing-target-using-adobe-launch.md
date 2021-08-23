---
keywords: 구현;구현하기;adobe launch;launch;경합;리디렉션;경험 platform launch;platform launch
description: Adobe [!DNL Target]을 구현하는 기본 방법인 Adobe Experience Platform Launch을 사용하여 Adobe [!DNL Target] at.js 라이브러리를 구현하는 방법을 알아봅니다.
title: Adobe Launch를 사용하여 [!DNL Target] 을 구현하려면 어떻게 합니까?
feature: 서버측 구현
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: fd7d3900f9e5d1a6c3d13fd2452de8528f8fd248
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# [!DNL Adobe Platform Launch]을 사용하여 [!DNL Target] 구현

[!DNL Adobe Experience Platform Launch] 는 의 차세대 태그 관리 플랫폼 [!DNL Adobe] 이며, 가 구현에 선호되는 방법입니다  [!DNL Adobe Target]. [!DNL Platform Launch] 는 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

## [!DNL Platform Launch]을 사용하여 [!DNL Target] 구현 {#topic_5234DDAEB0834333BD6BA1B05892FC25}

다음 표에는 [!DNL Platform Launch]에 대한 자세한 정보를 얻을 수 있는 다양한 소스가 나와 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [ [!DNL Target]  [!UICONTROL Adobe Target Extension 자습서를 사용하여 구현]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | 이 자습서에서는 [!DNL Platform Launch]을(를) 사용하여 웹 사이트에서 [!DNL Target]을 구현하는 단계별 지침을 제공합니다. 다뤄지는 주제에는 at.js JavaScript 라이브러리 추가, 글로벌 mbox 실행, 매개 변수 추가 및 다른 솔루션과의 통합이 있습니다. 이 문서는 [!DNL Platform Launch] 및 기타 [!DNL Adobe Experience Cloud] 솔루션을 구현하는 방법을 보여주는 더 큰 자습서의 일부입니다. |
| [Adobe Experience Platform의 태그에 대한 빠른 시작 안내서](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배치하고 관리하는 방법에 대한 정보입니다. |
| [ [!DNL Target] Adobe Extension 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | [!DNL Platform Launch]을 사용하여 [!DNL Target]을 구현하는 방법에 대한 정보입니다. |

## [!DNL Target] [!DNL Platform Launch] 확장을 사용하여 at.js를 구현할 때의 이점 {#section_48B3F938B6F8491DAF798E0DB54EF304}

다음 장점은 [!DNL Platform Launch]을 사용하여 at.js를 구현하는 경우에만 적용됩니다. 이러한 이유로 [!DNL Adobe]은 at.js의 수동 구현이 아니라 [!DNL Platform Launch]을 사용하는 것이 좋습니다.

* **[!DNL Adobe Analytics] 및  [!DNL Target] 경합 조건:**   [!DNL Analytics] 호출이 호출 전에 실행될 수  [!DNL Target] 있으므로,  [!DNL Target] 호출은 호출에  [!DNL Analytics] 결합되지 않습니다. 이 시퀀싱은 잘못된 데이터를 초래할 수 있습니다. 0.6.0부터 [!DNL Platform Launch] 확장 기능을 사용하면 [!DNL Analytics] 비콘 호출이 성공했는지에 관계없이 완료될 때까지 대기합니다. [!DNL Target] [!DNL Platform Launch]을 사용하면 데이터 불일치가 해결되므로 고객이 수동으로 구현할 때 발생할 수 있습니다.
* **잘못된 리디렉션 오퍼 처리 방지:**  가  [!DNL Target] 있고 페이지 [!DNL Analytics] 에 가 있는 경우, 그리고  [!DNL Target]에 의해 리디렉션 오퍼가 실행된 경우, 사용자가 다른 URL로 리디렉션되기 때문에 추적기가 요청을  [!DNL Analytics] 실행하지 말아야 할 때 요청을 실행하는 상황이 발생할 수 있습니다. [!DNL Target] 및 [!DNL Analytics] 를 [!DNL Platform Launch]에서 구현하는 경우 이 문제가 발생하지 않습니다. [!DNL Platform Launch] 을 사용하면 [!DNL Target]이 [!DNL Analytics]에 [!DNL Analytics] 비콘 요청을 중단하도록 지시합니다.
