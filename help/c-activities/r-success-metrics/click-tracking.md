---
keywords: 클릭 추적;클릭 수 추적;클릭 수;AppMeasurement
description: Adobe [!DNL Target] 을 통해 요소에 대한 클릭 수를 성공 지표로 추적하는 방법을 알아봅니다.
title: 클릭 추적이란?
feature: 성공 지표
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 93%

---

# 클릭 추적

[!DNL Adobe Target] 요소에 대한 클릭 수를 성공 지표로 추적할 수 있습니다.

>[!NOTE]
>
>클릭 추적이 양식 기반 활동에서 위치로 사용하는 경우 글로벌 Target 요청에서 지원되지 않습니다.

## 클릭 추적 설정 {#section_5540C5A533114E57BAE022A600B02E72}

1. 활동에 대한 [!UICONTROL 목표 및 설정] 페이지에서 목표를 설정할 때 **[!UICONTROL 변환]** 성공 지표를 선택합니다.
1. 작업에 대해 **[!UICONTROL 요소를 클릭함]**&#x200B;을 선택한 후 **[!UICONTROL 요소 선택]**&#x200B;을 클릭합니다.

   페이지가 VEC([!UICONTROL 시각적 경험 작성기])에서 열립니다.

1. 추적할 요소를 선택합니다.

   요소 선택에 대한 팁은 아래의 고려 사항 섹션을 참조하십시오.

1. 화면 맨 위에 있는 확인 표시를 클릭하여 선택 사항을 저장합니다.

활동 참여자가 선택된 요소를 클릭하면 해당 클릭이 전환으로 카운트됩니다.

## 선택한 요소 패널 {#selected-elements}

A/B 테스트, XT(경험 타깃팅), AP(자동화된 개인화) 및 MVT(다변량 테스트) 활동의 경우 [!UICONTROL 선택한 요소] 패널에 오른쪽의 클릭 추적에 대해 선택한 모든 요소가 나열됩니다.

![선택한 요소 패널](/help/c-activities/r-success-metrics/assets/selected-elements.png)

다음 [!UICONTROL 선택한 요소] 패널의 요소를 마우스로 가리키면 적용할 수 있는 몇 가지 작업이 표시됩니다. 다음 표에서는 요소에 대해 수행할 수 있는 각 작업을 설명합니다.

| 작업 | 설명 |
| --- | --- |
| 정보 | 선택기에 요소 유형 및 전체 DOM 경로를 표시합니다. |
| 편집 | CSS 선택기를 편집할 수 있습니다. |
| 삭제 | 요소를 삭제합니다. |

### 요소 추가

선택기의 DOM 경로를 이미 알고 있는 경우에는 패널 위쪽에 있는 더하기 아이콘을 클릭하여 수동으로 추가할 수 있습니다.

![요소 추가 아이콘](/help/c-activities/r-success-metrics/assets/add-element.png)

### 선택한 요소 가리키기 팝업

클릭 추적을 위해 여러 요소를 선택한 후 활동의 [!UICONTROL 목표 및 설정] 단계에서 [!UICONTROL 선택한 요소] 링크를 클릭하여 클릭 추적을 위해 선택한 전체 요소 목록을 표시할 수 있습니다. 목록에는 선택한 요소가 클릭 추적에 사용되는지 확인하는 데 도움이 되는 요소에 대한 전체 DOM 경로가 포함되어 있습니다.

![선택한 요소 링크](/help/c-activities/r-success-metrics/assets/elements-selected-link.png)

## 고려 사항 {#considerations}

요소를 선택할 때 다음과 같은 몇 가지 사항을 고려해야 합니다.

* DOM 경로 기능은 클릭 추적을 설정할 때 사용할 수 있습니다. 페이지에서 요소를 클릭하면 VEC 옵션 메뉴가 표시됩니다. 또한 해당 DOM 경로가 페이지 하단에 표시됩니다. DOM 경로를 사용하여 선택한 요소(유형, ID 및 클래스)에 대한 정보를 빠르게 확인하고, DOM 경로로 위 또는 아래로 이동하여 원하는 요소를 선택할 수 있습니다.

   ![DOM 경로 일러스트레이션](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   활동 생성 워크플로우의 1단계에서 경험을 만들 때와 마찬가지로 페이지 하단에 있는 DOM 경로 선택기를 사용하여 요소를 선택할 수 있습니다. DOM 경로에서 요소를 선택할 때 VEC에서 해당 요소가 &quot;선택됨&quot;으로 표시됩니다. 선택한 요소를 선택 취소하려면 DOM 경로 선택기에서 요소를 다시 클릭하거나 VEC 내에서 &quot;선택됨&quot; 상자를 클릭할 수 있습니다.

   자세한 내용은 *시각적 경험 작성기 선택 사항*&#x200B;에서 [DOM 경로를 사용하여 요소 탐색](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path)을 참조하십시오.

* 페이지에서 컨텐츠를 변경하지 않을 수 있는 클릭 수를 추적하기 위해 다른 페이지로 이동할 수 있습니다. 이 다른 페이지는  [다중 페이지 ](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) 기능 을 구현해야  [!DNL at.js] 합니다.
* 둘 이상의 요소를 선택하는 경우 참여자가 선택된 요소 중 하나를 클릭하면 해당 클릭은 카운트됩니다. 각 항목을 별도로 카운트하려면 각 요소에 대해 개별 성공 지표를 설정하십시오. 페이지에서 여러 요소를 클릭하여 한 항목을 계산하려면 CSS 요소 선택기를 여러 요소와 일치하도록 편집하십시오.
* 추적할 요소의 수준을 선택해야 합니다. 예를 들어, 단추를 지정할 때 단추 텍스트가 아닌 링크를 선택해야 합니다.
* 클릭 이벤트는 클릭이 진행된 동일한 페이지에 있는 [!DNL Target]으로 전송됩니다.
* 클릭 추적 지표가 A4T 활동의 목표 지표인 경우, 지표를 추적하기 위해 방문자는 페이지가 로드되고 60초 이내에 이 요소를 클릭해야 합니다.
* 클릭 추적은 다음을 포함하여 선택기에 이스케이프된 문자를 포함하는 요소에는 작동하지 않습니다.

   | 문자 | 설명 |
   |---|---|
   | # | 숫자 기호 또는 해시 |
   | : | 콜론 |
   | . | 기간 |
   | $ | 달러 기호 |
   | `[ ]` | 대괄호 |

* [!DNL at.js] 클릭 추적을 사용하며, Analytics AppMeasurement도 사용하는 경우 [!DNL at.js] 클릭 추적이 다른 모든 클릭 이벤트 처리기를 취소합니다. 따라서 AppMeasurement 클릭 처리기는 실행되지 않습니다.

   [!DNL at.js]에는 기본 요소가 `A` (링크) 태그 또는 `FORM` 태그인 경우 클릭 추적에 대한 특수 처리가 포함되어 있습니다.

   클릭 추적 이벤트가 [!DNL at.js] (링크) 태그 또는 `A` 태그에 첨부된 경우 `FORM`에서 다음 단계가 실행됩니다.

   1. `event.preventDefault()`를 호출합니다.

   1. Target 요청을 실행합니다.

   1. Target 요청 성공 또는 오류 콜백에서 다음과 같은 기본 동작을 실행합니다.

      * `A` (링크) 태그: 기본 동작은 HREF 속성으로 정의된 URL로 이동하는 것입니다.
      * `FORM` 태그: 기본 동작은 양식을 제출하는 것입니다.

   이 기본 동작은 Analytics 클릭 추적을 방해할 수 있습니다. Analytics를 사용하는 경우에는 클릭 추적 시 Target 대상이 아닌 Analytics를 사용해야 합니다.

* 클릭 추적은 페이지 및 활동 URL이 다른 속성에 속하는 페이지에 기록되지 않습니다. 엔터프라이즈 사용자 권한은 Target Premium 기능입니다. 자세한 내용은 [엔터프라이즈 사용자 권한](/help/administrating-target/c-user-management/property-channel/property-channel.md)을 참조하십시오.

## 교육 비디오 {#section_36607204DAE146E3B8E2C609D244EDB1}

이 비디오에는 클릭 추적 성공 지표 생성에 대한 정보가 포함되어 있습니다.

* &quot;목표&quot; 지표 이해
* 변환, 수입 및 참여 지표 이해 및 빌드
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)
