---
keywords: 경험 타깃팅;xt;create
description: Adobe Target에서 VEC(Visual Experience Composer)를 사용하여 Target이 활성화된 페이지에서 XT(경험 타깃팅) 활동을 만드는 방법에 대해 알아보십시오.
title: 경험 타깃팅 활동을 만들려면 어떻게 합니까?
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 89%

---


# 경험 타깃팅 활동 만들기{#create-an-experience-targeting-activity}

Target을 사용할 수 있는 페이지에서 XT([!UICONTROL 경험 타깃팅]) 활동을 만들고 [!DNL Adobe Target] 내에서 해당 페이지의 부분을 수정하려면 VEC([!UICONTROL 시각적 경험 작성기])를 사용하십시오.

경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.

다음 [지리 기반의 타깃팅](/help/c-target/c-audiences/c-target-rules/geo.md)을 포함한 경험 타깃팅은 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 콘텐츠 변형을 전달할 수 있습니다.

경험 타깃팅, 사용 사례 시나리오 및 교육 비디오에 대한 자세한 내용은 [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md)을 참조하십시오.

**XT 활동을 만들려면 다음을 수행하십시오.**

1. [!UICONTROL 활동] 목록에서 **[!UICONTROL 활동 만들기]** > **[!UICONTROL 경험 타깃팅]**&#x200B;을 클릭합니다.

   ![활동 만들기 > 경험 타깃팅](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 Target 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL 자동화된 개인화]는 [Target Premium](/help/c-intro/intro.md#premium) 기능입니다.
   >
   >[!DNL Target]에서 사용 가능한 다양한 활동 유형과 그 차이점에 대한 자세한 내용은 [활동](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 참조하십시오. 필요한 활동 유형 세트를 결정하는 데 도움이 되는 [타겟 활동 유형](/help/c-activities/target-activities-guide.md)을 참조하십시오.

1. 필요한 경우 **[!UICONTROL 시각적(기본값)]**&#x200B;을 선택합니다.

   ![경험 타깃팅 활동 만들기 대화 상자](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   양식 기반 경험 작성기를 사용하려면 [!UICONTROL 양식을 선택합니다]. 자세한 내용은 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >Target은 VEC 및 양식 기반 경험 작성기 외에도 단일 페이지 애플리케이션 VEC와 모바일 앱용 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/c-experiences/experiences.md)를 참조하십시오.
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >이전 그림에서 [!UICONTROL 작업 공간 선택] 선택 사항은 [Target Premium](/help/c-intro/intro.md) 기능입니다. 이 선택 사항이 표시되지 않는 경우 조직에 Target Standard 라이센스가 있는 것입니다.

1. (조건부) Target Premium 고객인 경우 [작업 공간을 선택](/help/administrating-target/c-user-management/property-channel/property-channel.md)합니다.

1. [활동 URL](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)을 지정한 후, **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   계정이 [기본 URL로 구성](/help/administrating-target/visual-experience-composer-set-up.md)된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

   VEC가 열리고 URL에 지정된 페이지가 표시됩니다.

   ![VEC 내의 경험 타깃팅 활동](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. 제공된 공간에 활동의 이름을 입력합니다.

   ![이름 필드](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   다음 문자는 활동 이름에서 허용되지 않습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `/` | 슬래시 |
   | `?` | 물음표 |
   | `#` | 숫자 기호 |
   | `:` | 콜론 |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

1. 다른 대상을 타깃팅한 새로운 경험을 만듭니다.

   단계별 지침은 [경험 추가](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md)를 참조하십시오.

1. 활동에 대한 [목표 및 설정](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)을 지정합니다.