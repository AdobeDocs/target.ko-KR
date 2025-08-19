---
keywords: 클릭 추적;클릭 수 추적;클릭 수;AppMeasurement
description: ' [!DNL Adobe Target] 요소에 대한 클릭 수를 성공 지표로 추적하는 방법에 대해 알아봅니다.'
title: 클릭 추적이란?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: 43d2484e57b1e2d292cf65c041fb9f5f49b2084c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 56%

---

# 클릭 추적

[!DNL Adobe Target]을(를) 사용하면 요소에 대한 클릭 수를 성공 지표로 추적할 수 있습니다. 클릭 추적은 웹 페이지 또는 경험 내의 요소에 대한 사용자 상호 작용(특히, 클릭)을 모니터링하고 기록하는 프로세스를 말합니다. 이는 A/B 테스트, 다변량 테스트 및 개인화 활동에서 참여 및 성과를 측정하는 데 있어 핵심 부분입니다.

>[!NOTE]
>
>클릭 추적이 양식 기반 활동에서 위치로 사용되는 경우 전역 [!DNL Target] 요청에서 지원되지 않습니다.

## 클릭 추적 설정 {#section_5540C5A533114E57BAE022A600B02E72}

1. 활동에 대한 [!UICONTROL Goals & Settings] 페이지에서 목표를 설정할 때 **[!UICONTROL Conversion]** 성공 지표를 선택하십시오.
1. 작업에 대해 **[!UICONTROL Clicked an element]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Select elements]**&#x200B;을(를) 클릭합니다.

   페이지가 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 열립니다.

1. 추적할 요소를 선택합니다.

   요소 선택에 대한 팁은 아래의 *고려 사항* 섹션을 참조하십시오.

1. 화면 상단의 **[!UICONTROL Done]**&#x200B;을(를) 클릭하여 선택 항목을 저장합니다.

활동 참여자가 선택된 요소를 클릭하면 해당 클릭이 전환으로 카운트됩니다.

## 선택한 요소 패널 {#selected-elements}

[!UICONTROL A/B Test], [!UICONTROL Experience Targeting]&#x200B;(XT), [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Multivariate Test]&#x200B;(MVT) 활동의 경우 [!UICONTROL Selected Elements] 패널에 왼쪽의 클릭 추적에 대해 선택한 요소가 나열됩니다.

![선택한 요소 패널](/help/main/c-activities/r-success-metrics/assets/selected-elements.png)

[!UICONTROL Tracked Components] 패널에서 요소를 클릭할 때 적용할 수 있는 몇 가지 작업이 있습니다. 다음 테이블에서는 요소에 대해 수행할 수 있는 각 작업을 설명합니다.

| 액션 | 설명 |
| --- | --- |
| [!UICONTROL Tracked actions] | 요소 작업을 표시합니다. |
| [!UICONTROL CSS selector] | CSS 선택기를 편집할 수 있습니다. |
| [!DNL Delete] | 요소를 삭제합니다. |

### 요소 추가

선택기의 DOM 경로를 이미 알고 있는 경우 패널 위쪽에 있는 [!UICONTROL Add Component] 아이콘을 클릭하여 수동으로 추가할 수 있습니다.

## 고려 사항 {#considerations}

요소를 선택할 때 다음과 같은 몇 가지 사항을 고려해야 합니다.

* DOM 경로 기능은 클릭 추적을 설정할 때 사용할 수 있습니다. 페이지에서 요소를 클릭하면 VEC 옵션 메뉴가 표시됩니다. 또한 해당 DOM 경로가 페이지 하단에 표시됩니다. DOM 경로를 사용하여 선택한 요소(유형, ID 및 클래스)에 대한 정보를 빠르게 확인하고, DOM 경로로 위 또는 아래로 이동하여 원하는 요소를 선택할 수 있습니다.

  활동 만들기 워크플로의 1단계에서 경험을 만들 때와 마찬가지로 페이지 하단에 있는 DOM 경로 선택기를 사용하여 요소를 선택할 수 있습니다. DOM 경로에서 요소를 선택할 때 VEC에서 해당 요소가 &quot;선택됨&quot;으로 표시됩니다. 선택한 요소를 선택 취소하려면 DOM 경로 선택기에서 요소를 다시 클릭하거나 VEC 내에서 &quot;선택됨&quot; 상자를 클릭할 수 있습니다.

  자세한 내용은 *시각적 경험 작성기 선택 사항*&#x200B;에서 [DOM 경로를 사용하여 요소 탐색](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path)을 참조하십시오.

* 페이지에서 콘텐츠를 변경하지 않을 수 있는 클릭 수를 추적하기 위해 다른 페이지로 이동할 수 있습니다. 이 다른 페이지는 [다중 페이지 기능](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48)을 사용하여 활동에 포함되어야 하며 [!DNL at.js]을(를) 구현해야 합니다.
* 둘 이상의 요소를 선택하는 경우 참여자가 선택된 요소 중 하나를 클릭하면 해당 클릭은 카운트됩니다. 각 항목을 별도로 카운트하려면 각 요소에 대해 개별 성공 지표를 설정하십시오. 페이지에서 여러 요소를 클릭하여 한 항목을 계산하려면 CSS 요소 선택기를 여러 요소와 일치하도록 편집합니다.
* 추적할 요소의 수준을 선택해야 합니다. 예를 들어, 단추를 지정할 때 단추 텍스트가 아닌 링크를 선택해야 합니다.
* 클릭 이벤트는 클릭이 진행된 동일한 페이지에 있는 [!DNL Target]으로 전송됩니다.
* 클릭 추적 지표가 [!UICONTROL Analytics for Target]&#x200B;(A4T) 활동의 목표 지표인 경우 방문자는 지표가 추적할 수 있도록 페이지 로드 후 60초 이내에 이 요소를 클릭해야 합니다.
* 클릭 추적은 다음을 포함하여 선택기에 이스케이프된 문자를 포함하는 요소에는 작동하지 않습니다.

  | 문자 | 설명 |
  |---|---|
  | # | 숫자 기호 또는 해시 |
  | : | 콜론 |
  | . | 기간 |
  | $ | 달러 기호 |
  | `[ ]` | 대괄호 |

* [!DNL at.js] 클릭 추적을 사용하며 [!DNL Analytics] AppMeasurement도 사용하는 경우 [!DNL at.js] 클릭 추적이 다른 모든 클릭 이벤트 처리기를 취소합니다. 따라서 AppMeasurement 클릭 처리기는 실행되지 않습니다.

  [!DNL at.js]에는 기본 요소가 `A` (링크) 태그 또는 `FORM` 태그인 경우 클릭 추적에 대한 특수 처리가 포함되어 있습니다.

  클릭 추적 이벤트가 [!DNL at.js] (링크) 태그 또는 `A` 태그에 첨부된 경우 `FORM`에서 다음 단계가 실행됩니다.

   1. `event.preventDefault()`를 호출합니다.

   1. [!DNL Target] 요청을 실행합니다.

   1. [!DNL Target] 요청 성공 또는 오류 콜백에서 기본 동작을 실행하십시오.

      * `A` (링크) 태그: 기본 동작은 HREF 속성으로 정의된 URL로 이동하는 것입니다.
      * `FORM` 태그: 기본 동작은 양식을 제출하는 것입니다.

  이 기본 동작은 [!DNL Analytics] 클릭 추적을 방해할 수 있습니다. [!DNL Analytics]을(를) 사용하는 경우 [!DNL Analytics]이(가) 아닌 클릭 추적을 위해 [!DNL Target]을(를) 사용해야 합니다.

* 클릭 추적은 페이지 및 활동 URL이 다른 속성에 속하는 페이지에 기록되지 않습니다. Enterprise 사용자 권한은 [!DNL Target Premium] 기능입니다. 자세한 내용은 [엔터프라이즈 사용자 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 참조하십시오.

* 클릭 추적 지표는 활동의 특정 경험에 연결되지 않습니다.

* 클릭 추적 지표 범위를 제한할 필요가 있는 경우 대상자를 사용합니다.

* 여러 활동을 통해 동일한 선택기에 대한 클릭 추적 지표를 정의할 수 있습니다. 그렇다면 해당 활동 중 하나를 수행할 자격이 있는 방문자가 해당 선택기를 클릭하는 경우 자격이 부여된 모든 관련 활동에 대해 클릭 추적 지표가 증가합니다.

## 교육 비디오 {#section_36607204DAE146E3B8E2C609D244EDB1}

이 비디오에는 클릭 추적 성공 지표 생성에 대한 정보가 포함되어 있습니다.

* &quot;목표&quot; 지표 이해
* [!UICONTROL Conversion], [!UICONTROL Revenue] 및 [!UICONTROL Engagement] 지표 이해 및 작성
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)
