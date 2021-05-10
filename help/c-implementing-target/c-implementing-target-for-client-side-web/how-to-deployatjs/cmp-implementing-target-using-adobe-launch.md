---
keywords: 구현;구현;adobe 론치;시작;레이스;리디렉션;경험 platform launch;platform launch
description: Adobe [!DNL Target]을 구현하는 데 선호하는 방법인 Adobe Experience Platform Launch을 사용하여 Adobe [!DNL Target] at.js 라이브러리를 구현하는 방법을 알아봅니다.
title: Adobe 시작을 사용하여  [!DNL Target] 을 구현하려면 어떻게 합니까?
feature: 서버측 구현
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
translation-type: tm+mt
source-git-commit: a69737f49a52cde703627f91d4b97609c1796ee6
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 6%

---

# [!DNL Adobe Platform Launch]을(를) 사용하여 [!DNL Target] 구현

[!DNL Adobe Experience Platform Launch] 는 다음세대 태그 관리 플랫폼 [!DNL Adobe] 으로 구현하기 위한 기본 방법입니다 [!DNL Adobe Target]. [!DNL Platform Launch] 고객은 연관성 있는 고객 경험을 향상시키는 데 필요한 분석, 마케팅 및 광고 태그를 간단하게 배포 및 관리할 수 있습니다.

## [!DNL Platform Launch] {#topic_5234DDAEB0834333BD6BA1B05892FC25}를 사용하여 [!DNL Target] 구현

다음 표는 [!DNL Platform Launch]에 대한 자세한 정보를 볼 수 있는 다양한 소스를 보여 줍니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [ [!DNL Target] Adobe Target  [!UICONTROL Extension 자습서를 사용하여 구현]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | 이 자습서에서는 [!DNL Platform Launch]이(가) 있는 웹 사이트에서 [!DNL Target]을(를) 구현하는 단계별 지침을 제공합니다. 다뤄지는 주제에는 at.js JavaScript 라이브러리 추가, 글로벌 mbox 실행, 매개 변수 추가 및 다른 솔루션과의 통합이 있습니다. 이 문서는 [!DNL Platform Launch] 및 기타 [!DNL Adobe Experience Cloud] 솔루션을 구현하는 방법을 보여주는 더 큰 자습서의 일부입니다. |
| [[!DNL Adobe Platform Launch] 설명서](https://experienceleague.adobe.com/docs/launch/using/get-started/quick-start.html#get-started) | 관련 고객 경험을 향상시키는 데 필요한 분석, 마케팅 및 광고 태그 배포 및 관리에 대한 정보입니다. |
| [ [!DNL Target] Adobe Extension 설명서](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | [!DNL Platform Launch]을(를) 사용하여 [!DNL Target] 구현에 대한 정보입니다. |

## [!DNL Target] [!DNL Platform Launch] 확장 {#section_48B3F938B6F8491DAF798E0DB54EF304}을 사용하여 at.js를 구현하는 이점

다음 이점은 at.js를 구현하는 데 [!DNL Platform Launch]을 사용하는 경우에만 적용됩니다. 이러한 이유로 [!DNL Adobe]은 at.js의 수동 구현이 아니라 [!DNL Platform Launch]을 사용하는 것이 좋습니다.

* **문제  [!DNL Adobe Analytics] 해결  [!DNL Target] 및** 경합 조건: [!DNL Analytics] 호출 전에  [!DNL Target] 호출을 실행할 수  [!DNL Target] 있으므로 호출 [!DNL Analytics] 을 호출로 연결할 수없습니다. 이 시퀀스는 잘못된 데이터를 초래할 수 있습니다. 0.6.0부터 시작하여 [!DNL Platform Launch] 확장은 [!DNL Analytics] 비콘 호출이 완료되거나, 성공하거나, 수행하지 않을 때까지 [!DNL Target] 비콘 호출이 대기하도록 합니다. [!DNL Platform Launch]을(를) 사용하면 고객이 수동으로 구현할 때 경험할 수 있는 데이터 불일치 문제를 해결할 수 있습니다.
* **잘못된 리디렉션 오퍼 처리 방지:** 페이지가  [!DNL Target] 있고 [!DNL Analytics] 에 의해 실행되는 리디렉션 오퍼가 있는  [!DNL Target]경우, 추적기가 요청을 실행하지 않을 때(사용자가 다른 URL로 리디렉션되기 때문)  [!DNL Analytics] 요청을 실행하는 상황을 경험할 수 있습니다. [!DNL Platform Launch]을(를) 통해 [!DNL Target] 및 [!DNL Analytics]을(를) 구현하는 경우 이 문제가 발생하지 않습니다. [!DNL Platform Launch]을 사용하여 [!DNL Target]은 [!DNL Analytics]에게 [!DNL Analytics] 비콘 요청을 중단하도록 지시합니다.
