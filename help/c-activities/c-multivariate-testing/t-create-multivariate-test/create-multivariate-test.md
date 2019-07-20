---
description: Target의 Visual Experience Composer를 사용하면 Target 지원 페이지에 MVT (다변수 테스트) 를 쉽게 만들고 Target 내에서 페이지의 일부를 수정할 수 있습니다.
keywords: mvt;다변량 테스트;다변량 테스트 만들기;다변량 테스트 생성;mvt 만들기;mvt 생성;mvt 방법;다변량 테스트 방법
seo-description: Adobe Target의 Visual Experience Composer (VEC) 를 사용하면 Target 지원 페이지에 MVT (다변수 테스트) 를 쉽게 만들고 Target 내에서 페이지의 일부를 수정할 수 있습니다.
seo-title: 다변량 테스트 만들기
solution: Target
title: 다변량 테스트 만들기
uuid: 876441bd-d841-4974-b1ec-3ad7cb6ef3ee
translation-type: tm+mt
source-git-commit: 5dd87afce38e7ff9c763aa65031ec837689d4ae8

---


# 다변량 테스트 만들기{#create-a-multivariate-test}

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] makes it easy to create your test right on a Target-enabled page and to modify portions of the page within [!DNL Target].

Target 가리키고 클릭 편집기를 사용하여 모든 위치를 선택하고 여러 오퍼를 추가할 수 있습니다.

[!UICONTROL 다변량 테스트] (MVT) 는 페이지 첫 번째 보고서를 사용합니다. 즉, 테스트가 해당 페이지에 대해 디자인한 경험을 사용하여 특정 URL에서 실행됩니다.

1. **[!UICONTROL 활동 만들기]** &gt; **[!UICONTROL 다변량 테스트]**&#x200B;를 클릭합니다.

   ![다변수 테스트 만들기](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >사용 가능한 활동 유형은 Target 계정에 따라 다릅니다. 일부 활동 유형은 목록에 표시되지 않을 수 있습니다. For example, [!UICONTROL Automated Personalization] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![다변량 테스트 활동 만들기 대화 상자](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-mvt-dialog.png)

   >[!NOTE]
   >
   >문제가 있는 경우 VEC에 대한 문제 해결 정보가 필요하면 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.
   >
   >The [!UICONTROL Choose Workplace] option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. 이 옵션이 표시되지 않는 경우 조직에 Target Standard 라이선스가 있습니다.]

1. (Conditional) If you are a Target Premium customer, [choose a workspace](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. [테스트할 페이지의 URL](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) 를 지정하고 **[!UICONTROL 다음을 클릭합니다]**.

   >[!NOTE]
   >
   >시작 부분에 HTTP 또는 HTTPS를 포함하는 전체 URL을 사용합니다.

   브라우저에서 혼합 컨텐츠를 사용하도록 허용할지 묻는 메시지가 표시되면 메시지의 지침을 따르십시오. 브라우저를 혼합 컨텐츠에 대해 활성화한 후 1단계부터 다시 시작하십시오.

   시각적 경험 작성기가 열립니다.

1. 활동의 이름을 입력합니다.

   ![활동 이름 필드](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   다음 문자는 활동 이름에서 허용되지 않습니다.

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

1. [각 위치에 오퍼를 만듭니다](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![텍스트/HTML 편집 대화 상자](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   다음과 같은 종류의 오퍼를 추가할 수 있습니다.

   * HTML
   * 이미지
   * 텍스트

1. **[!UICONTROL 미리 보기를]** 클릭하여 경험을 [미리 봅니다](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![경험 미리 보기](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   각 경험을 보고, 테스트에 포함하지 않으려는 경험을 제외할 수 있습니다. To exclude one or more experiences, select the desired checkboxes, then click **[!UICONTROL Exclude]** .

   ![경험 제외](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [트래픽 견적 도구를 사용하여](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) 테스트 계획의 가능성을 테스트합니다.

   ![트래픽 표시기](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   다음 그림은 활동에 트래픽이 충분하지 않음을 나타냅니다.

   ![](assets/estimator.png)

   다음 그림은 활동에 트래픽이 충분하지 않음을 나타냅니다.

   ![](assets/estimator2.png)

1. Click **[!UICONTROL Next]** to advance to the [!UICONTROL Targeting] page.]

1. 활동을 시작할 자격 있는 방문자의 대상 및 비율을 선택합니다.

   ![MVT 활동의 타깃팅 페이지](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 "캘리포니아" 대상의 45%로 제한할 수 있습니다.

   >[!NOTE]
   >
   >기존 대상을 선택할 수 있을 뿐만 아니라, 새 대상을 만들지 않고 여러 대상을 결합하여 임시로 결합한 대상을 만들 수도 있습니다. 자세한 내용은 [여러 대상 결합](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

1. [테스트 요약을](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) 검토하고 원하는 변경을 수행한 후 다음을 클릭합니다 ****.

1. [테스트에 대한 목표 및 설정을 지정](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)합니다.

1. **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭하여 활동을 만듭니다.

## 교육 비디오: 다변량 테스트 만들기(9:25)

다음 비디오에서는 Target 3단계 안내가 있는 워크플로우를 사용하여 다변량 테스트를 계획하고 작성하는 방법을 보여줍니다.

* 다변량 테스트 정의 및 디자인
* 다변량 테스트 만들기

>[!VIDEO](https://video.tv.adobe.com/v/17395?captions=kor)
