---
keywords: 템플릿 테스트;템플릿;유사한 페이지의 동일한 경험;템플릿 테스트
description: Adobe [!DNL Target] 시각적 경험 작성기(VEC)를 사용하여 구조가 유사하거나 동일한 템플릿 요소를 포함하는 여러 페이지에 동일한 경험을 포함하는 방법에 대해 알아봅니다.
title: 유사한 페이지에 동일한 경험을 포함할 수 있습니까?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 33%

---

# 유사한 페이지에 동일한 경험 포함

[!DNL Adobe Target]의 페이지 템플릿을 사용하여 페이지에 구조를 제공하거나 페이지에 유사한 요소가 포함되어 있는 경우 유사한 구조의 페이지 요소에서 또는 전체 도메인에서 변형을 테스트합니다.

이 기능이 제대로 작동하려면 구조가 유사하거나 모든 페이지에서 동일하게 구성된 템플릿 요소를 포함하는 페이지에서 이 기능을 사용해야 합니다.

>[!IMPORTANT]
>
>이 기능을 사용하여 여러 다른 페이지에서 요소를 변경하면 예기치 않은 결과가 발생할 수 있습니다.

예를 들어, 이 기능을 사용하여 다음 중 하나를 수행할 수 있습니다.

* 요소를 재정렬하거나 제거하여 글로벌 탐색 막대 테스트
* 특정 페이지 템플릿을 사용하는 모든 제품 페이지에서 항목 제거
* 모든 제품 페이지에 배너 추가
* 문서 템플릿의 레이아웃 변경

변경 요소를 포함하는 페이지를 지정하거나 사이트 또는 도메인에서 변경 사항을 적용할 수 있습니다.

1. [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)에 설명된 대로 활동을 만들거나 편집합니다.

1. 경험이 나타날 페이지를 지정하려면 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에서 톱니바퀴 아이콘을 클릭한 다음 **[!UICONTROL Page Delivery]**&#x200B;을(를) 선택합니다.

   ![톱니바퀴 아이콘 > 페이지 전달](/help/main/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. **[!UICONTROL Add Template Rule]**&#x200B;을(를) 클릭한 다음 경험을 추가할 페이지에 대한 기준을 지정합니다.

1. 페이지 범위를 지정합니다. 페이지 범위는 다음 중 하나일 수 있습니다.

   * URL(Target에서 URL을 평가하는 방법에 대한 자세한 내용은 [대상 및 대상 FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)를 참조하십시오.)
   * 도메인
   * 경로
   * 해시(#) 조각(# 기호 뒤에 오는 URL 부분을 대상으로 함)
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

   예를 들어 **[!UICONTROL Domain]** 및 **[!UICONTROL Is (case sensitive)]**&#x200B;을(를) 선택한 경우 경험이 모든 페이지에 추가되는 도메인을 입력합니다.

   여러 항목을 포함할 수 있습니다.

   >[!IMPORTANT]
   >
   >여러 항목은 OR 논리를 사용합니다. 즉, 목록의 항목 하나만 있으면 조건이 true가 됩니다.

1. 원할 경우 **[!UICONTROL Add Template Rule]**&#x200B;을(를) 클릭하고 이전 단계의 절차를 반복하여 추가 기준을 입력합니다.

   여러 기준이 AND 논리를 사용하여 결합됩니다. [!DNL Target]이(가) 지정한 조건과 일치하는 모든 페이지에 환경을 추가합니다.

>[!IMPORTANT]
>
> [!DNL Target]은(는) 페이지가 예상대로 표시되는지 확인할 수 없으므로 이 기능을 사용하여 영향을 받는 페이지를 공개하기 전에 테스트하는 것은 항상 중요한 방법입니다.

## 사용 사례

사이트에서 템플릿 규칙을 사용하는 방법에 대해서는 다음 사용 사례를 검토하십시오.

### 전체 도메인에서 동일한 활동 렌더링

다음의 사용 사례에 대해 템플릿 규칙을 사용하여 전체 도메인에서 동일한 활동을 렌더링할 수 있습니다.

* 글로벌 머리글 또는 바닥글을 포함하려면
* 글로벌 배너를 포함하려면(예: COVID-19 공지)
* 글로벌 무료 배송 프로모션을 포함하려면

1. [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)에 설명된 대로 활동을 만들거나 편집합니다.

1. 경험이 표시될 도메인을 지정하려면 시각적 경험 작성기에서 톱니바퀴 아이콘을 클릭하고 **[!UICONTROL Page Delivery]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Add Template Rule]** > **[!UICONTROL Domain]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Choose evaluator]** 드롭다운에서 **[!UICONTROL Contains]**&#x200B;을(를) 선택한 다음 도메인을 지정합니다.

   ![도메인 포함](/help/main/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## 교육 비디오: 시각적 경험 작성기(2/2) (7:29) ![튜토리얼 배지](/help/main/assets/tutorial.png)

* 경험 이름 변경 및 경험 복제
* 리디렉션 경험 만들기
* 활동을 단일 URL 또는 URL 그룹에 타기팅
* 다중 페이지 활동 만들기
* 반응형 웹 사이트용 경험 미리보기 및 빌드
* 오버레이를 사용하여 요소 유형을 강조 표시

>[!VIDEO](https://video.tv.adobe.com/v/30526?captions=kor)
