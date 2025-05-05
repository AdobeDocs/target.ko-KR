---
keywords: 양식 기반 경험 작성기;양식 기반 작성기;세분화
description: 비시각적 경험 작성에 Adobe [!DNL Target] 양식 기반 경험 작성기를 사용하는 방법을 알아봅니다. VEC를 사용할 수 없거나 실용적이지 않은 경우 이 작성기를 사용하십시오.
title: 양식 기반 경험 작성기를 사용하려면 어떻게 해야 합니까?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: 2f86c9ee89b4e1698180f6b3dc9df393733eb780
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 33%

---

# 양식 기반 경험 작성기

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer]은(는) VEC([!UICONTROL Visual Experience Composer])를 사용할 수 없거나 실용적이지 않을 때 [!UICONTROL A/B Test], [!UICONTROL Experience Targeting], [!UICONTROL Automated Personalization] 및 [!UICONTROL Recommendations] 활동에 사용할 경험을 만드는 데 유용한 시각적이지 않은 경험 및 오퍼 만들기 인터페이스입니다. 예를 들어 양식 기반 경험 작성기를 사용하여 이메일, 키오스크 및 음성 도우미에 게재할 경험과 오퍼를 만들 수 있습니다.

[!UICONTROL Recommendations] 활동을 만드는 경우 경험이 없습니다. 기준 및 디자인을 선택합니다. 여러 기준이나 디자인을 선택하면 [!UICONTROL Target]에서 자동으로 경험을 생성합니다.

1. **[!UICONTROL Create Activity]**&#x200B;을(를) 클릭한 다음 만들려는 활동 유형을 선택합니다.

   [!UICONTROL Form-Based Experience Composer]은(는) [!UICONTROL A/B Test], [!UICONTROL Experience Targeting], [!UICONTROL Automated Personalization] 및 [!UICONTROL Recommendations] 활동에 사용할 수 있습니다.

1. [!UICONTROL Create Activity] 대화 상자에서 **[!UICONTROL Form]** 선택

1. (조건부) [Target Premium 고객](/help/main/c-intro/intro.md#premium)인 경우 **[!UICONTROL Choose Workspace]** 드롭다운 목록에서 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을(를) 선택하십시오.

   [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 옵션은 [Target Premium](/help/main/c-intro/intro.md) 기능이며 조직에 [!UICONTROL Target Standard] 라이선스가 있는 경우 표시되지 않을 수 있습니다.

1. 속성을 선택합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

   [!UICONTROL Form-Based Experience Composer]이(가) 열립니다.

   [!UICONTROL Recommendations] 활동을 만드는 경우 이 화면은 다릅니다. [!UICONTROL Recommendations] 활동에 경험이 포함되어 있지 않습니다.

1. &#x200B;
   1. **[!UICONTROL Rename]** 아이콘(![이름 바꾸기 아이콘](/help/main/assets/icons/MoreSmallListVert.svg))을 클릭하고 **[!UICONTROL Rename]**&#x200B;을 클릭한 다음 활동의 이름을 지정하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   활동 이름은 다음 문자로 시작할 수 없습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

   활동 이름에는 다음 문자 시퀀스를 사용할 수 없습니다.

   | 문자 시퀀스 | 설명 |
   |--- |--- |
   | ;= | 세미콜론, 다음과 같음 |
   | ;+ | 세미콜론, 플러스 |
   | ;- | 세미콜론, 빼기 |
   | ;@ | 세미콜론, @ 기호 |
   | ,= | 쉼표, 같음 |
   | ,+ | 쉼표, 더하기 |
   | ,- | 쉼표, 빼기 |
   | ,@ | 쉼표, @ 기호 |
   | `[`&quot; | 대괄호 열기, 큰따옴표 |
   | &quot;`]` | 큰따옴표, 대괄호 닫기 |

1. 위치를 선택합니다.

   [!UICONTROL Select Location] 상자를 클릭하면 사용 가능한 위치 목록이 나타납니다. 해당 위치 중 하나를 선택합니다.

   여기에 나열되지 않은 위치를 입력할 수도 있습니다. 이 방식은 mbox가 페이지에서 아직 만들어졌거나 열람되지 않은 경우에 유용할 수 있습니다. 위치의 이름을 입력합니다. 아직 없는 위치를 입력할 때는 주의하십시오. 철자 또는 대소문자가 mbox 호출이 수행될 때의 철자 및 대소문자와 일치하지 않으면 활동이 전달되지 않습니다. 수동으로 입력한 위치는 사용 가능한 위치 목록에 저장됩니다. 다음에 수동으로 입력한 위치를 선택하려고 하면 해당 활동에 대한 [!UICONTROL Select Location] 드롭다운 목록에서 사용할 수 있습니다.

   >[!NOTE]
   >
   >활동을 만드는 동안 수동으로 입력한 위치를 만들어도 새 위치가 자동으로 만들어지지 않습니다. 위치 이름은 활동의 컨텍스트에서만 저장됩니다. 위치는 콘텐츠 게재 호출이 있을 때 만들어집니다. 위치가 생성되면 다른 활동에서 사용하거나 대상 만들기 등에 사용할 수 있습니다. 사용 가능한 위치 드롭다운 목록에서 선택합니다.

1. **[!UICONTROL Add Audience Refinements]**&#x200B;을(를) 클릭하고 이 활동에 대해 하나 이상의 [대상](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522)을(를) 선택한 다음 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Form-based Experience Composer]에서 세분화는 전체 대상 기능으로 대체되었습니다. 기존 활동에 대한 세분화가 [활동 전용 대상](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)(으)로 마이그레이션되었습니다.

1. 해당 위치에 표시할 콘텐츠 유형을 선택합니다.

1. 선택한 콘텐츠 유형에 대해 콘텐츠를 지정합니다.

   **HTML 오퍼 변경:** HTML 오퍼를 선택합니다.

   **이미지 오퍼 변경:** Target의 콘텐츠 라이브러리에 저장된 이미지를 선택합니다.

   이미지에 대한 링크(클릭스루, 대상, 랜딩 등)를 추가할 수도 있습니다.

   1. [!UICONTROL Change Image Offer] 아이콘을 클릭합니다.
   1. 원하는 이미지를 선택한 다음 [!UICONTROL Edit Links]을(를) 클릭합니다.
   1. 사이트에서 원하는 URL 또는 페이지를 지정한 다음 [!UICONTROL Update]을(를) 클릭합니다.

   **JSON 오퍼 변경:** JSON 오퍼를 선택합니다.

   **경험 조각 변경:** 경험 조각을 선택합니다. 자세한 내용은 [경험 조각](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)을 참조하세요.

   **리디렉션 오퍼 변경:** 리디렉션 오퍼를 선택합니다. 자세한 내용은 [리디렉션 오퍼 만들기](/help/main/c-experiences/c-manage-content/offer-redirect.md)를 참조하십시오.

   **원격 오퍼 변경:** 원격 오퍼를 선택합니다. 자세한 내용은 [원격 오퍼 만들기](/help/main/c-experiences/c-manage-content/about-remote-offers.md)를 참조하세요.

   **HTML 오퍼 만들기:**

   1. [!UICONTROL Offers]을(를) 클릭한 다음 [!UICONTROL Code Offers] 탭을 선택합니다.
   1. [!UICONTROL Create] > [!UICONTROL HTML Offer]을(를) 클릭합니다.
   1. 오퍼 이름을 입력합니다.
   1. 코드 상자에 HTML 코드를 입력하거나 붙여넣습니다.
   1. [!UICONTROL Save] 아이콘을 클릭합니다.

   **JSON 오퍼 만들기:**

   1. [!UICONTROL Offers]을(를) 클릭한 다음 [!UICONTROL Code Offers] 탭을 선택합니다.
   1. [!UICONTROL Create] > [!UICONTROL JSON Offer]을(를) 클릭합니다.
   1. 오퍼 이름을 입력합니다.
   1. 코드 상자에 JSON 코드를 입력하거나 붙여 넣습니다.
   1. [!UICONTROL Save] 아이콘을 클릭합니다.

   **추천 추가:**

   Recommendations 활동의 경우 콘텐츠 드롭다운에 [!UICONTROL Add Recommendation] 옵션이 제공됩니다. **[!UICONTROL Add Recommendation]**&#x200B;을(를) 클릭한 다음 페이지 유형을 선택합니다. 그런 다음, 인터페이스에 정의된 일반적인 단계를 수행하여 [권장 사항 활동을 만듭니다](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   양식 기반 경험 작성기에서 권장 사항 기준을 선택하는 동안 선택한 기준 카드에 직접 연결되는 링크가 있으므로 기준을 빠르고 쉽게 편집할 수 있습니다.

   [!DNL Target]의 [!UICONTROL Targeting] 페이지에서 안내가 있는 3단계 워크플로:

   **오퍼 결정 추가:**

   [!DNL Adobe Journey Optimizer] (AJO)에서 만든 오퍼를 [!DNL Adobe Target] 활동에 추가하여 offer decisioning을 사용하여 웹 사이트 또는 모바일 사이트의 방문자에게 최고의 동적 오퍼 및 경험을 제공합니다. 이 옵션은 수동 [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting] (XT) 활동에만 사용할 수 있습니다.

   자세한 내용은 [오퍼 결정 사용](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md)을 참조하세요.

1. (선택 사항, [!UICONTROL A/B Test], [!UICONTROL Automated Personalization] 및 [!UICONTROL Experience Targeting] 활동의 경우) 추가 위치에 대해 이 프로세스를 반복하려면 **[!UICONTROL Add Location]**&#x200B;을(를) 클릭하고 위치 및 콘텐츠를 구성하십시오.
1. **[!UICONTROL Next]**&#x200B;을(를) 클릭한 다음 활동 유형에 대한 활동 만들기 단계를 평소처럼 완료합니다.

* [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [경험 타깃팅 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [권장 사항 활동 만들기](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## 교육 비디오: 양식 기반 작성기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

다음 비디오에서는 양식 기반 작성기 데모를 제공합니다.

* 양식 기반 경험 작성기를 사용하여 활동 만들기
* 언제 양식 기반 경험 작성기를 사용하고 언제 시각적 경험 작성기를 사용할지 이해
* 개선을 통해 위치 타깃팅

>[!VIDEO](https://video.tv.adobe.com/v/17390)
