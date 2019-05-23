---
description: Target에서 요소에 대한 클릭 수를 성공 지표로 추적할 수 있습니다.
keywords: 클릭 추적;클릭 수 추적;클릭 수;AppMeasurement
seo-description: Target에서 요소에 대한 클릭 수를 성공 지표로 추적할 수 있습니다.
seo-title: 클릭 추적
solution: Target
subtopic: 시작하기
title: 클릭 추적
topic: Standard
uuid: 4a8fbb23-93d8-49f3-aca3-dbbdd6da0178
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 클릭 추적{#click-tracking}

Target에서 요소에 대한 클릭 수를 성공 지표로 추적할 수 있습니다.

>[!NOTE]
>
>클릭 추적이 양식 기반 활동에서 위치로 사용하는 경우 Target 글로벌 mbox에서 지원되지 않습니다.

## 클릭 추적 설정 {#section_5540C5A533114E57BAE022A600B02E72}

1. 활동에 대한 [!UICONTROL 목표 및 설정] 페이지에서 목표를 설정할 때 **[!UICONTROL 변환]성공 지표를 선택합니다.**
1. 작업에 대해 **[!UICONTROL 요소를 클릭함]**을 선택한 후 **[!UICONTROL 요소 선택]**을 클릭합니다.

   페이지가 VEC([!UICONTROL 시각적 경험 작성기])에서 열립니다.

1. 추적할 요소를 선택합니다.

   요소 선택에 대한 팁은 아래의 고려 사항 섹션을 참조하십시오.

1. 화면 맨 위에 있는 확인 표시를 클릭하여 선택 사항을 저장합니다.

활동 참여자가 선택된 요소를 클릭하면 해당 클릭이 전환으로 카운트됩니다.

## 고려 사항 {#considerations}

요소를 선택할 때 다음과 같은 몇 가지 사항을 고려해야 합니다.

* DOM 경로 기능은 클릭 추적을 설정할 때 사용할 수 있습니다. 페이지에서 요소를 클릭하면 VEC 옵션 메뉴가 표시됩니다. 또한 해당 DOM 경로가 페이지 하단에 표시됩니다. DOM 경로를 사용하여 선택한 요소 (유형, ID 및 클래스) 에 대한 정보를 빠르게 보고 DOM 경로로 위 또는 아래로 이동하여 원하는 요소를 선택할 수 있습니다.

   ![DOM 패스 일러스트레이션](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   활동 작성 워크플로우에서 1 단계에서 경험을 만들 때와 마찬가지로 페이지 하단의 DOM 경로 선택기를 사용하면 요소를 선택할 수 있습니다. DOM 경로에서 요소를 선택하면 VEC의 해당 요소가 &quot;selected&quot; 로 표시됩니다. 선택한 요소를 선택 취소하려면 DOM 경로 선택기에서 요소를 다시 클릭하거나 VEC 내의 &quot;선택&quot; 상자를 클릭합니다.

   자세한 내용은 Visual [Experience Composer 옵션에서 DOM 경로를](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) *사용하여 요소 탐색을 참조하십시오*.

* 페이지에서 컨텐츠를 변경하지 않을 수 있는 클릭 수를 추적하기 위해 다른 페이지로 이동할 수 있습니다. 이 다른 페이지는 [다중 페이지 기능](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48)을 사용하는 활동에 포함되어야 하며, [!DNL at.js] 또는 [!DNL mbox.js]가 구현되어야 합니다.
* 둘 이상의 요소를 선택하는 경우 참여자가 선택된 요소 중 하나를 클릭하면 해당 클릭은 카운트됩니다. 각 항목을 별도로 카운트하려면 각 요소에 대해 개별 성공 지표를 설정하십시오.
* 추적할 요소의 수준을 선택해야 합니다. 예를 들어, 단추를 지정할 때 단추 텍스트가 아닌 링크를 선택해야 합니다.
* 클릭 이벤트는 클릭이 진행된 동일한 페이지에 있는 [!DNL Target]으로 전송됩니다.
* 클릭 추적 지표가 A4T 활동의 목표 지표인 경우, 지표를 추적하기 위해 방문자는 페이지가 로드되고 60초 이내에 이 요소를 클릭해야 합니다.
* 클릭 추적은 다음을 포함하여 선택기에 이스케이프된 문자를 포함하는 요소에는 작동하지 않습니다.

   | 문자 | 설명 |
   |---|---|
   | # | 숫자 기호 또는 해시 |
   | : | 콜론 |
   | 에서 보냅니다. | 기간 |
   | $ | 달러 기호 |
   | [ ] | 대괄호 |

* [!DNL at.js] 클릭 추적을 사용하며, Analytics AppMeasurement도 사용하는 경우 [!DNL at.js] 클릭 추적이 다른 모든 클릭 이벤트 처리기를 취소합니다. 따라서 AppMeasurement 클릭 처리기는 실행되지 않습니다.

   [!DNL at.js]에는 기본 요소가 `A`(링크) 태그 또는 `FORM` 태그인 경우 클릭 추적에 대한 특수 처리가 포함되어 있습니다.

   클릭 추적 이벤트가 [!DNL at.js] (링크) 태그 또는 `A` 태그에 첨부된 경우 `FORM`에서 다음 단계가 실행됩니다.

   1. `event.preventDefault()`를 호출합니다.

   1. Target 요청을 실행합니다.

   1. Target 요청 성공 또는 오류 콜백에서 다음과 같은 기본 동작을 실행합니다.

      * `A`(링크) 태그: 기본 동작은 HREF 속성으로 정의된 URL로 이동하는 것입니다.
      * `FORM` 태그: 기본 동작은 양식을 제출하는 것입니다.
   이 기본 동작은 Analytics 클릭 추적을 방해할 수 있습니다. Analytics를 사용하는 경우에는 클릭 추적 시 Target 대상이 아닌 Analytics를 사용해야 합니다.

* 페이지 및 활동 URL 이 다른 속성에 속하는 페이지에 대해서는 클릭 추적이 기록되지 않습니다. Enterprise 사용자 권한은 Target Premium 기능입니다. 자세한 내용은 [엔터프라이즈 사용자 권한을](/help/administrating-target/c-user-management/property-channel/property-channel.md)참조하십시오.

## 교육 비디오 {#section_36607204DAE146E3B8E2C609D244EDB1}

이 비디오에는 클릭 추적 성공 지표 생성에 대한 정보가 포함되어 있습니다.

* &quot;목표&quot; 지표 이해
* 변환, 수입 및 참여 지표 이해 및 빌드
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)
