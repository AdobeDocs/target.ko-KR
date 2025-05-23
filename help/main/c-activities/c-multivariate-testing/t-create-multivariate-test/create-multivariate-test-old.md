---
keywords: mvt;다변량 테스트;다변량 테스트 만들기;다변량 테스트 생성;mvt 만들기;mvt 생성;mvt 방법;다변량 테스트 방법
description: ' [!DNL Adobe Target] 의 [!UICONTROL Visual Experience Composer] (VEC)을(를) 사용하여 [!UICONTROL Multivariate Test] (MVT)을(를) 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Multivariate Test]을(를) 만드는 방법'
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 56%

---

# 다변량 테스트 만들기

[!DNL Adobe Target]의 [!UICONTROL Visual Experience Composer] (VEC)을(를) 사용하면 [!UICONTROL Multivariate Test]을(를) 쉽게 만들고 [!DNL Target] 내에서 페이지의 일부를 수정할 수 있습니다.

[!DNL Target] 가리키고 클릭 편집기를 사용하여 원하는 위치를 선택하고 여러 오퍼를 추가할 수 있습니다.

[!UICONTROL Multivariate Test] (MVT)은 페이지 우선 보고서를 사용합니다. 즉, 테스트가 해당 페이지에 대해 디자인한 경험을 사용하여 특정 URL에서 실행됩니다.

1. **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**&#x200B;을(를) 클릭합니다.

   ![다변량 테스트 만들기](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >[!DNL Target]에서 사용 가능한 다양한 활동 유형과 그 차이점에 대한 자세한 내용은 [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 참조하십시오. 필요한 활동 유형 세트를 결정하는 데 도움이 되는 [타겟 활동 유형](/help/main/c-activities/target-activities-guide.md)을 참조하십시오.

1. (조건부) 배달 유형: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email] 또는 [!UICONTROL Other/API]을(를) 선택합니다.

1. (조건부) [Target Premium](/help/main/c-intro/intro.md#premium) 고객인 경우 [작업 영역을 선택](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)합니다.

1. 테스트할 페이지의 [URL을 지정](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0)한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >시작 부분에 HTTP 또는 HTTPS를 포함하는 전체 URL을 사용합니다.

   브라우저에서 혼합 콘텐츠를 사용하도록 허용할지 묻는 메시지가 표시되면 메시지의 지침을 따르십시오. 브라우저를 혼합 콘텐츠에 대해 활성화한 후 1단계부터 다시 시작하십시오.

   [!UICONTROL Visual Experience Composer]이(가) 열립니다.

1. 활동의 이름을 입력합니다.

   ![활동 이름 필드](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

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

   ![텍스트/HTML 편집 대화 상자](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   다음과 같은 종류의 오퍼를 추가할 수 있습니다.

   * HTML
   * 이미지
   * 텍스트

1. **[!UICONTROL Preview]**&#x200B;을(를) 클릭하여 [환경을 미리 봅니다](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![미리 보기 환경](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   각 경험을 보고, 테스트에 포함하지 않으려는 경험을 제외할 수 있습니다. 경험을 한 개 이상의 제외하려면 원하는 확인란을 선택한 다음 **[!UICONTROL Exclude]** 을(를) 클릭합니다.

   ![경험 제외](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [트래픽 견적 도구를 사용하여](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) 테스트 계획의 가능성을 테스트합니다.

   ![트래픽 표시기](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   다음 그림은 활동에 트래픽이 충분하지 않음을 나타냅니다.

   ![견적 도구 이미지](assets/estimator.png)

   다음 그림은 활동에 트래픽이 충분하지 않음을 나타냅니다.

   ![estimator2 이미지](assets/estimator2.png)

1. [!UICONTROL Targeting] 페이지로 이동하려면 **[!UICONTROL Next]**&#x200B;을(를) 클릭하십시오.

1. 활동을 시작할 자격 있는 방문자의 대상자 및 비율을 선택합니다.

   ![MVT 활동의 타깃팅 페이지](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   예를 들어 항목 수를 모든 방문자의 50% 또는 &quot;캘리포니아인&quot; 대상자의 45%로 제한할 수 있습니다.

   >[!NOTE]
   >
   >기존 대상자를 선택할 수 있을 뿐만 아니라, 새 대상자를 만들지 않고 여러 대상자를 결합하여 임시로 결합한 대상자를 만들 수도 있습니다. 자세한 내용은 [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

1. [테스트 요약을 검토하고](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7)원하는 대로 변경한 다음 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. [테스트에 대한 목표 및 설정을 지정](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)합니다.

1. **[!UICONTROL Save and Close]**&#x200B;을(를) 클릭하여 활동을 만듭니다.

## 교육 비디오: 다변량 테스트 만들기(9:25) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에서는 안내가 있는 [!DNL Target] 3단계 워크플로우를 사용하여 다변량 테스트를 계획하고 만드는 방법을 보여 줍니다.

* 다변량 테스트 정의 및 디자인
* 다변량 테스트 만들기

>[!VIDEO](https://video.tv.adobe.com/v/30528?captions=kor)
