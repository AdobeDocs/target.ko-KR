---
keywords: implement;implementing;implementation;adobe launch;launch;race;redirect;experience platform launch
description: Adobe Experience Platform Launch은 Adobe의 차세대 태그 관리 플랫폼으로 Adobe Target을 구현하는 데 선호되는 방법입니다. Launch는 관련 고객 환경을 향상하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.
title: Adobe Launch를 사용하여 Target 구현을 참조하십시오
feature: implementation with launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: 3ddaf11d272fc68e98d6063591cdcf956a5e7faa
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 80%

---


# Adobe Launch를 사용하여 Target 구현을 참조하십시오{#implement-target-using-adobe-launch}

Adobe Experience Platform Launch은 Adobe의 차세대 태그 관리 플랫폼으로 Adobe Target을 구현하는 데 선호되는 방법입니다. Launch는 관련 고객 환경을 향상하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

## Adobe Launch를 사용하여 Target 구현{#topic_5234DDAEB0834333BD6BA1B05892FC25}을 참조하십시오 

Launch는 Adobe의 차세대 태그 관리 플랫폼이며 Adobe Target을 구현하는 데 권장되는 방법입니다. Launch는 관련 고객 환경을 향상하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

다음 표에는 Launch에 대한 자세한 정보를 얻을 수 있는 여러 소스가 나열되어 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe Target 확장 자습서를 사용하여 Target 구현](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | 이 자습서에서는 Launch를 사용하여 웹 사이트에서 Adobe Target을 구현하는 단계별 지침을 제공합니다. 다뤄지는 주제에는 at.js JavaScript 라이브러리 추가, 글로벌 mbox 실행, 매개 변수 추가 및 다른 솔루션과의 통합이 있습니다. 이 문서는 다른 Adobe Experience Cloud 솔루션뿐만 아니라 Adobe Launch를 구현하는 방법도 보여주는 더 광범위한 자습서의 일부입니다. |
| [Adobe Launch 설명서](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html) | 관련 고객 경험을 수행하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배치하고 관리하는 방법에 대한 정보입니다. |
| [Adobe Target 익스텐션 설명서](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Launch를 사용하여 Target을 구현하는 방법에 대한 정보입니다. |

## Advantages of implementing at.js using the Target Launch extension {#section_48B3F938B6F8491DAF798E0DB54EF304}

Adobe Launch를 사용하여 at.js를 구현하는 경우에만 다음과 같은 이점이 있습니다. 따라서 DTM이 아닌 Adobe Launch를 사용하거나 at.js를 수동으로 구현하는 것이 좋습니다.

* **Analytics 및 Target 경쟁 조건 해결:** Analytics 호출이 Target 호출 전에 실행될 수 있으므로, Target 호출은 Analytics 호출에 연결되지 않습니다. 이로 인해 잘못된 데이터가 발생할 수 있습니다. 0.6.0부터 Target Launch Extension에서 Analytics 신호 호출은 Target 호출이 성공했는지에 관계없이 완료될 때까지 대기합니다. 이로 인해 데이터 불일치가 발생했을 수 있습니다.
* **잘못된 리디렉션 오퍼 처리 방지:** 페이지에 Target과 Analytics가 있고 Target에 의해 리디렉션 오퍼가 실행된 경우, 사용자가 다른 URL로 리디렉션되기 때문에 Analytics 추적기가 요청을 실행하지 말아야 할 때 요청을 실행하는 상황이 발생할 수 있습니다. Launch를 통해 Target 및 Analytics를 구현하는 경우 이 문제가 발생하지 않습니다. Launch를 사용하면 Target은 Analytics에 Analytics 비콘 요청을 중단하도록 지시합니다.
