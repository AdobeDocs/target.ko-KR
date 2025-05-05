---
keywords: 타깃팅;경험;경험 추가;경험 추가
description: ' [!DNL Adobe Target]에서 [!UICONTROL Visual Experience Composer] (VEC)을(를) 사용하는 방법을 알아봅니다.'
title: A [!DNL Target] A/B 활동에서 경험을 추가하려면 어떻게 합니까?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 43%

---

# 경험 추가

[!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)은 페이지에서 경험을 추가하고 편집하기 위한 시각적 인터페이스를 제공합니다.

경험에 대한 자세한 내용은 [경험](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)을 참조하십시오.

1. VEC의 **[!UICONTROL Experiences]** 페이지에서 **[!UICONTROL Add Experience]**&#x200B;을(를) 클릭합니다.

   ![경험 추가 선택 사항](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/add-experience.png)

   >[!NOTE]
   >
   >경험을 대상자로 타기팅하는 경우 경험을 추가하기 전에 먼저 대상자를 선택해야 합니다. 사용자에게 대상자를 선택하라는 메시지가 표시됩니다.

1. 변경할 요소를 선택하고 원하는 대로 변경합니다.

   페이지의 요소 위로 마우스를 가져가면 요소가 강조 표시됩니다. 강조 표시된 요소는 VEC를 사용하여 변경할 수 있습니다.

   [!DNL Target Classic] (이전의 [!DNL Test&Target])을(를) 사용하여 페이지에서 [!DNL Target] 요청을 만든 경우 해당 [!DNL Target] 요청은 요청 이름을 나타내는 요소로 표시되며 다른 요소와 같이 수정할 수 있습니다.

   표시된 페이지의 요소에서 수행하여 경험을 변경할 수 있는 작업 목록은 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을 참조하십시오.

   >[!NOTE]
   >
   >기본 페이지 이외의 소스에서 가져온 이미지(예: `akamai.net`에 호스팅되고 `example.com`에 전달된 이미지)를 전달하는 경우 해당 이미지가 흐름 다이어그램에 표시된 페이지의 썸네일에 표시되지 않습니다.

1. 경험 디자인을 마치면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 경험 이름 변경

1. [!UICONTROL A/B Test] 또는 [!UICONTROL Experience Targeting] (XT) 활동에서 경험에 대한 **[!UICONTROL Rename Experience]** 아이콘을 클릭하여 경험에 새 이름을 지정합니다.

   ![경험 이름 변경](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/rename-experience.png)

2. 새 이름을 지정합니다.

   경험에 이름을 지정하거나 경험의 이름을 바꾸는 경우 다음 문자가 허용되지 않습니다.

   | 문자 | 설명 |
   |--- |--- |
   | / | 슬래시 |
   | ? | 물음표 |
   | # | 숫자 기호 |
   | : | 콜론 |
   | = | 다음과 같음 |
   | + | 플러스 |
   | - | 빼기 |
   | @ | 로그인 |

## URL로 리디렉션

1. [!UICONTROL A/B Test] 또는 [!UICONTROL Experience Targeting] (XT) 활동에서 경험에 대한 **[!UICONTROL More]** 아이콘(세로 줄임표) 아이콘을 클릭한 다음 **[!UICONTROL Redirect to URL]**&#x200B;을(를) 클릭합니다.

   자세한 내용은 [URL로 리디렉션](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md)을 참조하십시오.

   **참고**: 경험에 이름을 지정하거나 경험의 이름을 바꾸는 경우 다음 문자가 허용되지 않습니다.

   | 문자 | 설명 |
   |--- |--- |
   | / | 슬래시 |
   | ? | 물음표 |
   | # | 숫자 기호 |
   | : | 콜론 |
   | = | 다음과 같음 |
   | + | 플러스 |
   | - | 빼기 |
   | @ | 로그인 |

1. 경험을 리디렉션할 URL을 지정합니다.

1. (조건부) **[!UICONTROL Include Current Query Parameters]** 확인란을 선택합니다.

## 경험 복제

[!UICONTROL A/B Test]에서 환경을 복사할 수 있으므로 처음부터 환경을 다시 작성하지 않고도 간단한 콘텐츠를 변경할 수 있습니다.

1. **[!UICONTROL Experiences]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 수직 줄임표 아이콘 > **[!UICONTROL Duplicate]**&#x200B;을(를) 클릭합니다.

   ![중복된 선택 사항](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/duplicate-experience.png)

## 경험 삭제

1. **[!UICONTROL Experiences]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 수직 줄임표 아이콘 > **[!UICONTROL Duplicate]**&#x200B;을(를) 클릭합니다.

   ![경험 삭제 선택 사항](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/delete-experience.png)

## 교육 비디오: [!UICONTROL Visual Experience Composer] 사용

아래 비디오에서는 [!UICONTROL Visual Experience Composer] 옵션 사용에 대한 정보를 제공합니다. (7:17)

* 페이지 콘텐츠 변경
* 페이지 레이아웃 변경

>[!VIDEO](https://video.tv.adobe.com/v/17399)
