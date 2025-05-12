---
keywords: mvt;다변량 테스트;다변량 테스트 만들기;다변량 테스트 생성;mvt 만들기;mvt 생성;mvt 방법;다변량 테스트 방법
description: ' [!DNL Adobe Target] 의 [!UICONTROL Visual Experience Composer]​(VEC)을(를) 사용하여 [!UICONTROL Multivariate Test]​(MVT)을(를) 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Multivariate Test]을(를) 만드는 방법'
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 9cc1eb4c5c95ea51bc0a1fc9e89b245a18c9914b
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 26%

---

# 다변량 테스트 만들기

[!DNL Adobe Target]의 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)을(를) 사용하면 [!UICONTROL Multivariate Test]을(를) 쉽게 만들고 [!DNL Target] 내에서 페이지의 일부를 수정할 수 있습니다.

[!DNL Target] 가리키고 클릭 편집기를 사용하여 원하는 위치를 선택하고 여러 오퍼를 추가할 수 있습니다.

[!UICONTROL Multivariate Test]&#x200B;(MVT)은 페이지 우선 보고서를 사용합니다. 즉, 테스트가 해당 페이지에 대해 디자인한 경험을 사용하여 특정 URL에서 실행됩니다.

1. **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]에서 사용 가능한 다양한 활동 유형과 그 차이점에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 참조하십시오. 필요한 활동 유형 세트를 결정하는 데 도움이 되는 [타겟 활동 유형](/help/main/c-activities/target-activities-guide.md)을 참조하십시오.

1. (조건부) 배달 유형: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email] 또는 [!UICONTROL Other/API]을(를) 선택합니다.

1. (조건부) [Target Premium](/help/main/c-intro/intro.md#premium) 고객인 경우 [작업 영역을 선택](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)합니다.

1. 테스트할 페이지의 [URL을 지정](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0)한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >시작 부분에 HTTP 또는 HTTPS를 포함하는 전체 URL을 사용합니다.

   브라우저에서 혼합 콘텐츠를 사용하도록 허용할지 묻는 메시지가 표시되면 메시지의 지침을 따르십시오. 브라우저를 혼합 콘텐츠에 대해 활성화한 후 1단계부터 다시 시작하십시오.

   [!UICONTROL Visual Experience Composer]이(가) 열립니다.

1. 활동의 이름을 지정하려면 &quot;[!UICONTROL Untitled Activity]&quot; 옆에 있는 **[!UICONTROL Edit]** 아이콘(![편집 아이콘](/help/main/assets/icons/Edit.svg))을 클릭하고 활동에 대한 수사적 이름을 지정한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

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

1. [각 위치에 오퍼를 만듭니다](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   다음과 같은 종류의 오퍼를 추가할 수 있습니다.

   * HTML
   * 이미지
   * 텍스트

1. **[!UICONTROL Preview]**&#x200B;을(를) 클릭하여 [환경을 미리 봅니다](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. **[!UICONTROL Show Experiences]** 아이콘(![경험 표시 아이콘](/help/main/assets/icons/WebPages.svg))을 클릭하여 왼쪽 프레임에 모든 경험 목록을 표시합니다.

1. 목록에서 특정 경험을 클릭하여 해당 경험을 봅니다.

1. (조건부) 활동에서 경험을 한 개 이상 제외하려면 **[!UICONTROL Manage Content]** 아이콘(![경험 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭하여 [!UICONTROL Manage Experiences] 대화 상자를 표시합니다.

1. (조건부) [!UICONTROL Manage Experiences] 대화 상자에서 제외하려는 경험 옆에 있는 **[!UICONTROL More Actions]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg))을 클릭한 다음 **[!UICONTROL Exclude]**&#x200B;을(를) 클릭합니다.

   충돌하는 변형을 표시하는 경험이나 미적으로 균형 잡히지 않은 경험을 제외하도록 선택할 수 있습니다.

1. (조건부) 여러 경험을 제외하려면 원하는 경험에 대한 확인란을 선택한 다음 **[!UICONTROL Exclude]**&#x200B;을(를) 클릭합니다.

1. [트래픽 견적 도구를 사용하여](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) 테스트 계획의 가능성을 테스트합니다.

1. [!UICONTROL Targeting] 페이지로 이동하려면 **[!UICONTROL Next]**&#x200B;을(를) 클릭하십시오.

   **타깃팅** 단계는 다른 [!DNL Target] 활동 유형을 사용해본 적이 있는 경우 친숙하게 보입니다. 여기에서 대상을 선택하고 각 경험을 보는 방문자의 비율을 지정할 수 있습니다.

   흐름 다이어그램은 대상과 해당 트래픽 비율을 할당하고, 트래픽 할당 방법을 선택하고, 활동의 각 경험에 대한 트래픽 할당을 지정하는 단계를 안내합니다.

1. (조건부) **[!UICONTROL All Visitors]** 컨트롤을 클릭하여 활동에 대한 다른 대상을 선택합니다.

   [!UICONTROL All Visitors] 대상이 기본값으로 설정됩니다. 다른 대상을 선택하면 해당 이름이 가장 왼쪽 컨트롤에 표시됩니다.

   오른쪽 프레임이 표시되어 대상을 추가 또는 삭제하고 활동에 대한 방문자 비율을 할당할 수 있습니다.

   1. 대상을 변경하려면 오른쪽 프레임에서 **[!UICONTROL Replace]아이콘**(![바꾸기 아이콘](/help/main/assets/icons/Retweet.svg))을 클릭합니다.
   1. [!UICONTROL Add Audience] 대화 상자에서 [원하는 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)한 다음 **[!UICONTROL Assign Audience]**&#x200B;을(를) 클릭합니다.

      **대상 결합**&#x200B;을 클릭하여 [여러 대상을 결합하는 대상을 만들 수 있습니다](/help/main/c-target/combining-multiple-audiences.md).

      [!UICONTROL Audience Library]에 없는 새 대상을 만들어야 하는 경우 **대상 만들기**&#x200B;를 클릭합니다. [대상자 만들기 워크플로](/help/main/c-target/c-audiences/audiences.md) 동안 다음 옵션 중에서 선택할 수 있습니다.

      * **[!UICONTROL Audience Library]**: [!UICONTROL Audience Library]에 저장된 온디맨드 대상을 만들어 다른 활동에서 다시 사용할 수 있습니다.
      * **[!UICONTROL This activity only]**: [!UICONTROL Audience Library]에 저장되지 않고 현재 활동에서만 사용할 수 있는 [활동별 대상](/help/main/c-target/creating-activity-only-audience.md)을 만듭니다.

   1. 오른쪽 프레임에서 **[!UICONTROL Visitor Percentage]**&#x200B;을(를) 클릭한 다음 활동을 시작할 자격 있는 방문자의 비율을 선택합니다.

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아인&quot; 대상자의 45%로 제한할 수 있습니다.

1. [테스트 요약을 검토하고](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7)원하는 대로 변경한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. [테스트에 대한 목표 및 설정을 지정](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)합니다.

1. **[!UICONTROL Save and Close]**&#x200B;을(를) 클릭하여 활동을 만듭니다.

## 교육 비디오: 다변량 테스트 만들기(9:25) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에서는 안내가 있는 [!DNL Target] 3단계 워크플로우를 사용하여 다변량 테스트를 계획하고 만드는 방법을 보여 줍니다.

* 다변량 테스트 정의 및 디자인
* 다변량 테스트 만들기

>[!VIDEO](https://video.tv.adobe.com/v/17395)
