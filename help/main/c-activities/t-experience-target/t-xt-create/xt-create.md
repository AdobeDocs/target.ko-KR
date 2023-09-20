---
keywords: 경험 타깃팅;xt;만들기
description: '사용 방법 알아보기 [!UICONTROL 시각적 경험 작성기] (VEC) 위치 [!DNL Adobe Target] 다음을 만들려면: [!UICONTROL 경험 타기팅] (XT) 활동.'
title: 다음을 만드는 방법 [!UICONTROL 경험 타기팅] 활동?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 4faafcef38d02674072d8b20ae03d3e2ef2115d6
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 48%

---

# 만들기 [!UICONTROL 경험 타기팅] (XT) 활동

사용 [!UICONTROL 시각적 경험 작성기] (VEC): [!UICONTROL 경험 타기팅] (XT) 활동 [!DNL Target]-enabled page 및 내에서 페이지 일부 수정 [!DNL Adobe Target].

[!UICONTROL Experience Targeting] (XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상자에게 전달합니다.

다음 [지리 기반의 타깃팅](/help/main/c-target/c-audiences/c-target-rules/geo.md)을 포함한 경험 타깃팅은 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 콘텐츠 변형을 전달할 수 있습니다.

에 대한 자세한 내용 [!UICONTROL 경험 타기팅], 사용 사례 시나리오 및 교육 비디오, 참조 [경험 타기팅](/help/main/c-activities/t-experience-target/experience-target.md).

**을(를) 만들려면 [!UICONTROL 경험 타기팅] 활동:**

1. 다음에서 [!UICONTROL 활동] 목록, 클릭 **[!UICONTROL 활동 만들기]** > **[!UICONTROL 경험 타기팅]**.

   ![활동 만들기 > 경험 타깃팅](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 [!DNL Target] 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. 예를 들어 [!UICONTROL 자동화된 개인화]는 [Target Premium](/help/main/c-intro/intro.md#premium) 기능입니다.
   >
   >[!DNL Target]에서 사용 가능한 다양한 활동 유형과 그 차이점에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 참조하십시오. 필요한 활동 유형 세트를 결정하는 데 도움이 되는 [타겟 활동 유형](/help/main/c-activities/target-activities-guide.md)을 참조하십시오.

1. 필요한 경우 **[!UICONTROL 시각적(기본값)]**&#x200B;을 선택합니다.

   을(를) 사용하려면 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md), 선택 [!UICONTROL 양식].

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL 양식 기반 경험 작성기], [!DNL Target] 는 단일 페이지 애플리케이션 VEC를 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (조건부) (다음과 같은 경우) [!DNL Target Premium] 고객, [작업 영역 선택](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   다음 [!UICONTROL 작업 공간 선택] 옵션이 [Target Premium](/help/main/c-intro/intro.md) 기능. 조직에 [!DNL Target Standard] 이 옵션이 표시되지 않으면 라이센스를 부여하십시오.

1. [활동 URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)을 지정한 다음, **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

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
