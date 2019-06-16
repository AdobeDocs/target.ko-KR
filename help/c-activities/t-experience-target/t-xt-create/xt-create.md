---
description: Target을 사용할 수 있는 페이지에서 경험 타깃팅 활동을 만들고 Target 내에서 해당 페이지의 부분을 수정하려면 시각적 경험 작성기를 사용하십시오.
seo-description: Visual Experience Composer를 사용하여 Target 이 활성화된 페이지에서 XT (Experience Targeting) 활동을 만들고 Adobe Target 내에서 페이지의 일부를 수정할 수 있습니다.
seo-title: 경험 타깃팅 활동 만들기
solution: Target
subtopic: 다변량 테스트
title: 경험 타깃팅 활동 만들기
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: c6085fae6428cb837eed6eadd778140687348817

---


# 경험 타깃팅 활동 만들기{#create-an-experience-targeting-activity}

[!UICONTROL Visual Experience Composer] (VEC) 를 사용하여 Target 이 활성화된 페이지에서 [!UICONTROL 경험 타깃팅] (XT) 활동을 만들고 페이지의 [!DNL Adobe Target]일부를 수정합니다.

경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 컨텐츠를 특정 대상에 전달합니다.

[지역 타깃팅을](/help/c-target/c-audiences/c-target-rules/geo.md)포함한 경험 타깃팅은 특정 경험이나 컨텐츠를 특정 대상에 타깃팅하는 규칙을 정의하는 데 중요합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 컨텐츠 변형을 전달할 수 있습니다.

경험 타깃팅, 사용 사례 시나리오 및 교육 비디오에 대한 자세한 내용은 [경험 타깃팅을 참조하십시오](/help/c-activities/t-experience-target/experience-target.md).

**XT 활동을 만들려면:**

1. [!UICONTROL 활동] 목록에서 **[!UICONTROL 활동 만들기]** &gt; **[!UICONTROL 경험 타깃팅]** 을 클릭합니다.

   ![활동 만들기 &gt; 경험 타깃팅](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 Target 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL 자동화된 개인화는] [Target Premium 기능입니다](/help/c-intro/intro.md#premium).
   >
   >사용 가능한 다양한 활동 유형과 그 차이점에 대한 [!DNL Target] 자세한 내용은 [활동을 참조하십시오](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). 필요한 활동 유형을 결정하는 데 도움이 되는 [타겟 활동 유형을](/help/c-activities/target-activities-guide.md) 참조하십시오.

1. 필요한 경우 **[!UICONTROL 시각적 (기본값)]** 를 선택합니다.

   ![경험 타깃팅 활동 만들기 대화 상자](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   양식 기반 경험 작성기를 사용하려면 [!UICONTROL 양식을 선택합니다]. 자세한 내용은 [양식 기반 Experience Composer](/help/c-experiences/form-experience-composer.md) 를 참조하십시오.

   >[!NOTE]
   >
   >Target는 VEC 및 양식 기반 Experience Composer 외에도 단일 페이지 애플리케이션 VEC와 모바일 앱용 VEC를 제공합니다. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >이전 그림에서 작업 영역 [!UICONTROL 선택] 옵션은 [Target Premium](/help/c-intro/intro.md) 기능입니다. 이 옵션이 표시되지 않는 경우 조직에 Target Standard 라이선스가 있습니다.]

1. (조건부) Target Premium 고객인 경우 작업 영역을 [선택합니다](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. [활동 URL](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)를 지정하고 다음을 클릭합니다 **[!UICONTROL ]**.

   계정이 기본 URL로 [구성된 경우 기본적으로 해당 URL 이 나타납니다](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

   vec가 열리고 URL에 지정된 페이지가 표시됩니다.

   ![VEC 내에서 경험 타깃팅 활동](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

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

1. 고객을 차별화하는 새로운 경험 제작

   단계별 지침은 경험 [추가를](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md)참조하십시오.

1. 활동에 대한 [목표 및 설정](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)을 지정합니다.