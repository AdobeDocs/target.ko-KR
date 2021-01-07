---
keywords: template testing;template;same experience on similar pages;template test
description: Adobe Target의 페이지 템플릿을 사용하여 페이지에 구조를 제공하거나 페이지에 유사한 요소가 포함되어 있는 경우 유사한 구조화된 페이지 요소의 변형을 테스트합니다.
title: Adobe Target을 사용하여 유사한 페이지에 동일한 경험 포함
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 38%

---


# 유사한 페이지에 동일한 경험 포함

[!DNL Adobe Target]의 페이지 템플릿을 사용하여 페이지에 구조를 제공하거나 페이지에 유사한 요소가 포함되어 있는 경우 유사한 구조화된 페이지 요소 또는 전체 도메인의 변형을 테스트합니다.

제대로 작동하려면 구조가 유사하거나 모든 페이지에서 동일한 템플릿 요소를 포함하는 페이지에서 이 기능을 사용해야 합니다.

>[!IMPORTANT]
>
>이 기능을 사용하여 여러 다른 페이지에서 요소를 변경하면 예기치 않은 결과가 발생할 수 있습니다.

예를 들어, 이 기능을 사용하여 다음 중 하나를 수행할 수 있습니다.

* 요소를 재정렬하거나 제거하여 글로벌 탐색 막대 테스트
* 특정 페이지 템플릿을 사용하는 모든 제품 페이지에서 항목 제거
* 모든 제품 페이지에 배너 추가
* 문서 템플릿의 레이아웃 변경

변경 요소를 포함하는 페이지를 지정하거나 사이트 또는 도메인에서 변경 사항을 적용할 수 있습니다.

1. [활동](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)에 설명된 대로 활동을 만들거나 편집합니다.

1. 경험이 나타날 페이지를 지정하려면 [!UICONTROL Visual Experience Composer](VEC)에서 톱니바퀴 아이콘을 클릭한 다음 **[!UICONTROL 페이지 배달]**&#x200B;을 선택합니다.

   ![톱니바퀴 아이콘 > 페이지 배달](/help/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. **[!UICONTROL 템플릿 규칙 추가]**&#x200B;를 클릭한 후 경험을 추가할 페이지에 대한 기준을 지정합니다.

1. 페이지 범위를 지정합니다. 페이지 범위는 다음 중 하나일 수 있습니다.

   * URL Target이 URL을 평가하는 방법에 대한 자세한 내용은 [Target 및 대상 FAQ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)을 참조하십시오.
   * 도메인
   * 경로
   * 해시(#) 조각(# 기호 다음에 오는 URL 부분을 타깃팅합니다.)
   * 쿼리
   * 매개 변수

1. 연산자를 선택합니다.

   연산자는 연산자 뒤에 나오는 항목이 페이지 범위와 어떻게 관련되는지를 지정합니다. 사용 가능한 연산자는 다음과 같습니다.

   * 다음 포함
   * 다음을 포함하지 않음
   * 일치함(대/소문자 구분)
   * 아님
   * 다음으로 시작
   * 다음으로 끝남

1. 페이지 이름에 포함된 도메인 또는 문자열과 같이 경험이 추가되는 위치를 정의하는 문자열을 입력합니다.

   예를 들어, **[!UICONTROL 도메인]**&#x200B;과 **[!UICONTROL 일치함(대/소문자 구분)]**&#x200B;을 선택한 경우에는 경험이 모든 페이지에 추가되는 도메인을 입력합니다.

   여러 항목을 포함할 수 있습니다.

   >[!IMPORTANT]
   >
   >여러 항목은 OR 논리를 사용합니다. 즉, 목록의 단일 항목이 조건을 true로 만듭니다.

1. 원하는 경우 **[!UICONTROL 템플릿 규칙 추가]**&#x200B;를 클릭하고 이전 단계에서 절차를 반복하여 추가 기준을 입력합니다.

   여러 기준이 AND 논리를 사용하여 결합됩니다. [!DNL Target] 지정된 기준과 일치하는 모든 페이지에 경험을 추가합니다.

>[!IMPORTANT]
>
> [!DNL Target] 페이지를 확인할 수 없어 페이지가 예상대로 표시되는지 확인할 수 없으므로 이 기능을 사용하여 영향을 받는 페이지를 공개하기 전에 테스트하는 것이 항상 중요합니다.

## 사용 사례

사이트에서 템플릿 규칙을 사용하는 방법은 다음 사용 사례를 검토하십시오.

### 전체 도메인에 동일한 활동을 렌더링합니다.

다음과 같은 사용 사례를 위해 템플릿 규칙을 사용하여 전체 도메인에 동일한 활동을 렌더링하는 것을 고려할 수 있습니다.

* 전역 머리글 또는 바닥글을 포함하려면
* 글로벌 배너를 포함하려면(예: COVID-19 공지)
* 글로벌 무료 배송 프로모션을 포함하려면

1. [활동](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)에 설명된 대로 활동을 만들거나 편집합니다.

1. 경험이 나타날 도메인을 지정하려면 Visual Experience Composer에서 톱니바퀴 아이콘을 클릭한 다음 **[!UICONTROL 페이지 배달]**&#x200B;을 선택합니다.

1. **[!UICONTROL 템플릿 규칙 추가]** > **[!UICONTROL 도메인]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 평가기 선택]** 드롭다운에서 **[!UICONTROL 포함]**&#x200B;을 선택한 다음 도메인을 지정합니다.

   ![도메인이 다음을 포함](/help/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## 교육 비디오:Visual Experience Composer (2/2) (7:29) ![자습서 배지](/help/assets/tutorial.png)

* 경험 이름 변경 및 경험 복제
* 리디렉션 경험 만들기
* 활동을 단일 URL 또는 URL 그룹에 타깃팅
* 다중 페이지 활동 만들기
* 응답형 웹 사이트용 경험 미리 보기 및 빌드
* 오버레이를 사용하여 요소 유형을 강조 표시

>[!VIDEO](https://video.tv.adobe.com/v/17401)