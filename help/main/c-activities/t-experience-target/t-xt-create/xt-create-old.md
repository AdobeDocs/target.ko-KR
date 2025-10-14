---
keywords: 경험 타깃팅;xt;만들기
description: '[!UICONTROL Visual Experience Composer]의  [!DNL Adobe Target] (VEC)를 사용하여 [!UICONTROL Experience Targeting]​(XT) 활동을 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Experience Targeting] 활동을 만드는 방법'
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 38%

---

# [!UICONTROL Experience Targeting]&#x200B;(XT) 활동 만들기

[!UICONTROL Visual Experience Composer]이(가) 활성화된 페이지에서 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동을 만들고 [!DNL Target] 내에서 해당 페이지의 부분을 수정하려면 [!DNL Adobe Target]&#x200B;(VEC)를 사용하십시오.

[!UICONTROL Experience Targeting]&#x200B;(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.

[!UICONTROL Experience Targeting]지리 기반의 타깃팅[을(를) 포함한 &#x200B;](/help/main/c-target/c-audiences/c-target-rules/geo.md)은(는) 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상자에 다양한 콘텐츠 변형을 전달할 수 있습니다.

[!UICONTROL Experience Targeting], 사용 사례 시나리오 및 교육 비디오에 대한 자세한 내용은 [경험 타기팅](/help/main/c-activities/t-experience-target/experience-target.md)을 참조하세요.

**[!UICONTROL Experience Targeting] 활동을 만들려면:**

1. [!UICONTROL Activities] 목록에서 **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**&#x200B;을(를) 클릭합니다.

   ![활동 만들기 > 경험 타깃팅](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL Automated Personalization]은(는) [Target Premium 기능](/help/main/c-intro/intro.md#premium)입니다.
   >
   >[!DNL Target]에서 사용 가능한 다양한 활동 유형과 그 차이점에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 참조하십시오. 필요한 활동 유형 세트를 결정하는 데 도움이 되는 [타겟 활동 유형](/help/main/c-activities/target-activities-guide.md)을 참조하십시오.

1. 필요한 경우 **[!UICONTROL Visual (Default)]**&#x200B;을(를) 선택합니다.

   [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하려면 [!UICONTROL Form]을(를) 선택하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL Form-Based Experience Composer] 외에 [!DNL Target]에서 단일 페이지 응용 프로그램 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [!DNL Target Premium] 고객인 경우 [작업 영역을 선택](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)합니다.

   [!UICONTROL Choose Workplace] 옵션은 [Target Premium](/help/main/c-intro/intro.md) 기능입니다. 이 옵션이 표시되지 않는 경우 조직에 [!DNL Target Standard] 라이선스가 있는 경우.

1. [활동 URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)을(를) 지정한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   계정이 [기본 URL로 구성](/help/main/administrating-target/visual-experience-composer-set-up.md)된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

   VEC가 열리고 URL에 지정된 페이지가 표시됩니다.

   ![VEC 내의 경험 타깃팅 활동](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. 제공된 공간에 활동의 이름을 입력합니다.

   ![이름 필드](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

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

1. 다른 대상을 타깃팅한 새로운 경험을 만듭니다.

   단계별 지침은 [경험 추가](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md)를 참조하십시오.

1. 활동에 대한 [목표 및 설정](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)을 지정합니다.
