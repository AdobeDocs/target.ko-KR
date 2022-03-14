---
keywords: 구현;구현;adobe launch;launch;경합;리디렉션;경험 platform launch;platform launch;태그;adobe platform
description: 구현 방법 알아보기 [!DNL Adobe Target] at.js 라이브러리 사용 [!DNL Adobe Experience Platform]를 구현하기 위해 선호되는 방법입니다 [!DNL Target].
title: 구현 방법 [!DNL Target] 사용 [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 10%

---

# [!DNL Target]을 사용하여[!DNL Adobe Experience Platform]구현 

의 태그 [!DNL Adobe Experience Platform] 는에서 차세대 태그 관리 기능입니다 [!DNL Adobe]. 태그는 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] 가 [!DNL Adobe Experience Platform]의 데이터 수집 기술군으로 새롭게 브랜딩되었습니다. 그 결과로 제품 설명서 전반에서 몇 가지 용어 변경이 있었습니다. 다음을 참조하십시오 [문서](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) 용어 변경 내용을 통합 참조하기 위해.

다음 표에는 추가 정보를 얻을 수 있는 다양한 소스가 나와 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [추가 [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | 이 자습서에서는 구현을 위한 단계별 지침을 제공합니다 [!DNL Target] 웹 사이트에 태그 [!DNL Adobe Experience Platform]. 다뤄지는 주제에는 at.js JavaScript 라이브러리 추가, 글로벌 mbox 실행, 매개 변수 추가 및 다른 솔루션과의 통합이 있습니다. 이 문서는 구현 방법을 보여주는 더 큰 자습서의 일부입니다 [!DNL Adobe Experience Platform], 및 기타 [!DNL Adobe Experience Cloud] 솔루션. |
| [빠른 시작 안내서](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | 관련 고객 환경을 향상하는 데 필요한 분석, 마케팅 및 광고 태그를 배치하고 관리하는 방법에 대한 정보입니다. |
| [Adobe [!DNL Target] 확장 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | 구현에 대한 정보입니다 [!DNL Target] 사용 [!DNL Adobe Experience Platform]. |

## 를 사용하여 at.js를 구현할 때의 이점 [!DNL Target] 확장 {#section_48B3F938B6F8491DAF798E0DB54EF304}

다음은에서 태그를 사용하는 경우에만 적용됩니다 [!DNL Adobe Experience Platform] at.js를 구현하려면 다음을 수행하십시오. 이런 이유로 [!DNL Adobe] 는에서 태그를 사용하는 것이 좋습니다 [!DNL Adobe Experience Platform] at.js를 수동으로 구현하지 마십시오.

* **해결 방법 [!DNL Adobe Analytics] 및 [!DNL Target] 경합 조건:** 왜냐하면 [!DNL Analytics] 호출이 수행되기 전에 [!DNL Target] 호출, [!DNL Target] 호출은 와 연결되지 않습니다 [!DNL Analytics] 호출. 이 시퀀싱은 잘못된 데이터를 초래할 수 있습니다. 다음 [!DNL Target] 확장은 다음을 보장합니다 [!DNL Analytics] 비콘 호출은 [!DNL Target] 호출이 완료되었는지, 성공적으로 완료되었는지 여부. 에서 태그 사용 [!DNL Adobe Experience Platform] 수동으로 구현할 때 데이터 불일치를 해결할 수 있습니다.

   >[!NOTE]
   >
   >를 사용하십시오 [!UICONTROL 비콘 보내기] 의 작업 [!DNL Adobe Analytics] 확장 [!DNL Analytics] 호출 대기 시간 [!DNL Target] 호출. 직접 전화하는 경우 `s.t()` 또는 `s.tl()` 사용자 지정 코드 사용 [!DNL Analytics] 호출은 [!DNL Target] 호출이 완료되었습니다.

* **잘못된 리디렉션 오퍼 처리를 방지합니다.** 만약 [!DNL Target] 및 [!DNL Analytics] 및 가 실행하는 리디렉션 오퍼가 있습니다. [!DNL Target]를 설정하는 경우 [!DNL Analytics] 추적기는 사용자가 다른 URL로 리디렉션되기 때문에 하지 않아야 할 때 요청을 실행합니다. 를 구현하는 경우 [!DNL Target] 및 [!DNL Analytics] 의 태그를 통해 [!DNL Adobe Experience Platform], 이 문제가 발생하지 않습니다. 에서 태그 사용 [!DNL Adobe Experience Platform], [!DNL Target] 지시 [!DNL Analytics] 를 중단하려면 [!DNL Analytics] 비콘 요청.
