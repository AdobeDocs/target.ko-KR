---
keywords: 권장 사항;설정;이름;목표;우선순위;지속 기간;보고 설정;기타 메타데이터
description: Adobe Target에서 Recommendations 활동을 설명하고 제어하는 데 사용되는 설정을 구성하는 방법에 대해 알아봅니다.
title: Recommendations 활동 설정을 구성하는 방법
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 48%

---

# 권장 사항 활동 설정

를 설명하고 제어하는 데 사용할 수 있는 설정에 대한 정보 [!UICONTROL Recommendations] 의 활동 [!DNL Adobe Target].

![권장 사항 목표 및 설정 페이지](/help/main/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

다음 섹션에서는 다음에 사용 가능한 설정을 설명합니다. [!UICONTROL Recommendations] 활동.

## 이름

사용자 및 팀이 활동을 식별하는 데 도움이 되는 수사적 이름을 제공하십시오.

다음 문자는 활동 이름에서 허용되지 않습니다.

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

다음을 지정하는 경우 [!UICONTROL Recommendations] 의 다른 활동에 대해 이미 존재하는 활동 이름 [!UICONTROL Recommendations Classic], 새 활동이 새 이름으로 다시 동기화됩니다. 새 이름을 고유하게 만들기 위해 원래 이름에 타임스탬프가 추가됩니다. 이 새 이름은 [!DNL Target Standard/Premium]과 [!UICONTROL Recommendations Classic] 모두에 표시됩니다.

## 목표

(선택 사항) 활동의 목표를 설명합니다.

## 우선순위

슬라이더를 조정하여 우선순위의 수준을 파악합니다.

대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.

## 지속 시간

활동의 지속 기간을 설정하십시오.

활동은 활성화될 때 시작되거나 특정 날짜 및 시간을 설정하여 시작할 수 있습니다. 이와 마찬가지로, 활동은 비활성화될 때 종료되거나 날짜 및 시간을 설정하여 종료할 수 있습니다. 시간 선택기는 24시간 형식을 사용하며 00:00은 자정을 나타냅니다. 해당 시간대는 브라우저에 구성된 시간대로 설정됩니다. 다른 시간대를 사용하려면 브라우저를 다른 시간대로 설정하고 브라우저를 다시 시작하십시오.

## 보고 설정

* **보고 소스:** 수집할 솔루션 데이터 지정:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  에 보고 솔루션이 지정된 경우 [계정 설정](/help/main/administrating-target/reporting.md)을 지정하면 지정된 솔루션이 사용되고 이 설정이 표시되지 않습니다.

  보고서 일관성을 유지하기 위해 활동이 활성 상태가 되면 보고 소스를 변경할 수 없습니다.

  **[!DNL Adobe Analytics]**: 를 참조하십시오 [[!DNL Adobe Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) 보고 솔루션의 차이점과 각각의 장점에 대해 알아봅니다.

  선택 시 [!DNL Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Target] (A4T), 다음을 선택합니다. [!DNL Analytics] 받을 보고서 세트 [!DNL Target] 활동 데이터. 이렇게 하려면 먼저 다음 중 하나를 선택합니다 [!DNL Analytics] 계정이 연결된 회사 를 선택한 다음 활동에 대한 보고서 세트를 선택합니다. 연결할 수 있도록 프로비저닝된 보고서 세트만 [!DNL Target] 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 다음에 다시 로그인하십시오 [!DNL Adobe Experience Cloud] 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T)에서 결과를 올바로 보고하려면 추적 서버가 필요합니다. 기본 추적 서버가에 표시됩니다 [!UICONTROL Tracking Server] 필드. 추적 서버를 두 개 이상 사용하는 경우 이 필드에 올바른 추적 서버를 포함해야 합니다. 다음을 참조하십시오 [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) 추가 정보.

  **[!DNL Adobe Customer Journey Analytics]**: 를 참조하십시오 [[!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) 를 참조하십시오. [!DNL Adobe Customer Journey Analytics] 및 [!DNL Target].

* **목표 지표:** 활동이 성공적인지를 결정하는 성공 지표를 선택합니다.
* **추가 지표:**&#x200B;보고서에서 사용할 추가 성공 지표를 구성하십시오.
* **보고 대상:**&#x200B;보고서를 필터링할 때 사용할 수 있는 대상을 정의합니다.

## 기타 메타데이터

활동에 대한 메모를 입력합니다.

## 교육 비디오: 활동 설정(3:02) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 활동 설정에 대한 정보가 포함되어 있습니다.

* 활동의 목표 입력
* 활동의 우선순위 수준 설정
* 활동 시작 및 종료 시간 예약
* 보고서 필터를 작성하기 위해 보고 대상 추가
* 활동에 대한 메모 입력

>[!VIDEO](https://video.tv.adobe.com/v/17381)
