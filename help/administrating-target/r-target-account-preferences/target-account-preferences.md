---
description: 계정에서 올바르게 작동하도록 계정 기본 설정을 사용하여 Target Standard 또는 Target Premium을 구성합니다.
keywords: 계정 환경 설정;환경 설정;사이트 세부 사항;사용자 지정 mbox 이름;보고에 사용되는 Experience Cloud 솔루션;매출액에서 예상되는 상승도 표시;css 선택기;요소 클래스 사용;기본 시각적 경험 작성기 URL;고급 경험 작성기 활성화;경험 스냅샷 생성;모바일 뷰포트 구성;수직 시장;필터 비호환 기준
seo-description: 계정 환경 설정을 지정하여 계정과 올바르게 작동하도록 Adobe Target Standard 또는 Target Premium를 구성합니다.
seo-title: 기본 설정
solution: Target
subtopic: 시작하기
title: 기본 설정
topic: Standard
uuid: ed3904c8-533b-4b9c-a3a1-079c61b1bf2a
translation-type: tm+mt
source-git-commit: ecd707927629ff8bc3882a322f0744d93abced2c

---


# 기본 설정{#preferences}

계정에서 올바로 작동하도록 [!DNL Target Standard] 또는 [!DNL Target Premium]을 구성하려면 계정 환경 설정을 설정하십시오.

계정 환경 설정을 지정하려면 **[!UICONTROL 설정]** &gt; **[!UICONTROL 환경 설정]**을 클릭하고 원하는 대로 환경 설정을 구성한 다음, **[!UICONTROL 제출]**을 클릭합니다.

다음 그림은 [!UICONTROL 계정 기본 설정] 페이지에서 사용할 수 있는 설정을 보여 줍니다.

![환경 설정 페이지](/help/administrating-target/r-target-account-preferences/assets/target-account-preferences.png)에 지정된 대로 로그인된 사용자의 시간대가 적용됩니다

>[!NOTE]
>
>이러한 환경 설정 중 일부는 Target Premium 이 있는 [경우에만 사용할 수](/help/c-intro/intro.md#premium)있습니다.

## 사이트 세부 사항 {#section_04A3340FC29B46978DB77058259F4EE0}

사이트가 구성되는 방식을 지정합니다.

### 사용자 지정 글로벌 mbox

[!DNL Target] 활동을 전달하는 데 사용할 선택적인 사용자 지정 mbox 이름을 선택합니다. 이 글로벌 mbox는 기본 컨텐츠가 없음을 나타내도록 비어 있어야 합니다. 사이트에 업데이트되거나 [!DNL at.js][!DNL mbox.js] 파일이 설치된 후에만 이 설정을 저장합니다.

>[!CAUTION]
>
>이 설정을 잘못 구성하면 기존 활동이 중단될 수 있습니다.

## 결과 및 보고 {#section_47C887AABD704A96BCD1C00BEABF4BCE}

결과 및 보고서에 사용되는 데이터를 결정하는 옵션을 설정합니다.

| 옵션 | 설명 |
|--- |--- |
| 보고에 사용되는 Experience Cloud 솔루션 | 활동의 보고 소스로 [!DNL Target] 또는 Adobe Analytics 중 하나를 선택합니다. 또한 활동별로 보고 소스를 선택하도록 지정할 수 있습니다. 보고 소스를 선택하는 경우 다음 정보를 고려하십시오.<ul><li>[!UICONTROL 자동 할당], [!UICONTROL 자동 타겟] 및 [!UICONTROL 자동화된 개인화](AP) 활동 작성, 활성화 및 비활성화는 선택된 보고 소스와 관계없이 허용됩니다. 이러한 활동 유형은 [Adobe Analytics를 Adobe Target(A4T)의 보고 소스](/help/c-integrating-target-with-mac/a4t/a4t.md)로 선택할 때 지원되지 않습니다. Analytics를 보고 소스로 지정하더라도 [!DNL Target]은 이러한 활동 유형의 보고 소스로 사용됩니다.</li><li>보고 소스가 여기에서 Analytics로 설정된 경우 [!DNL Target]을 보고 소스(보고 소스가 활동별 Target으로 지정됨)로 사용하는 활동을 활성화할 수 없습니다. 활동의 보고 소스를 Analytics로 변경하거나 설정 &gt; 환경 설정에서 활동당 선택으로 보고 엔진을 변경해야 합니다.</li><li>보고 소스가 여기에서 [!DNL Target]으로 설정된 경우 Analytics를 보고 소스로 사용하는 활동을 활성화할 수 없습니다. 활동의 보고 소스를 [!DNL Target]으로 변경하거나 설정 &gt; 환경 설정에서 활동당 선택으로 보고 소스를 변경해야 합니다.</li><li>보고 소스가 여기에서 활동당 선택으로 설정된 경우, 선택한 보고 소스에서 지원하는 활동을 작성, 활성화 및 비활성화할 수 있습니다. 지원되는 활동의 매트릭스는 [](/help/c-integrating-target-with-mac/a4t/a4t.md)Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)를 참조하십시오.</li><li>A/B Manual에서 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 타겟]으로 전환하면 A/B Manual 활동의 보고 소스가 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 타겟] 활동에서 지원되지 않는 경우 모든 지표 및 보고 대상이 손실됩니다.</li></ul> |
| 매출액에서 예상되는 상승도 표시 | 목표에 대한 통화 값을 입력하는 경우 매출액에서 예상되는 상승도를 표시하도록 선택할 수도 있습니다. [!DNL Target]은 모든 사용자가 우승을 경험하는 경우 이루게 되는 매출 상승도를 예측할 수 있습니다. 예상되는 상승도 기능은 기본적으로 비활성화됩니다.<br>Experience Cloud 관리자 사용자만 이 기능을 활성화하거나 비활성화할 수 있습니다. 예상되는 상승도가 비활성화되면 해당 필드가 인터페이스에 표시되지 않습니다. 이 기능을 비활성화해도 예상치에 사용되는 데이터를 비롯한 어떤 데이터도 손실되지 않습니다. 예상치는 기능의 활성화 여부와 관계없이 수집되는 데이터를 기준으로 합니다.<br>자세한 내용은 [매출 상승도 평가](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오. |
| 세밀한 우선 순위 설정 | 0-999 범위의 우선 순위를 입력할 수 있습니다.<br>설정에 따라 우선순위의 UI 및 옵션이 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다.<br>대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다. |

## CSS 선택기 {#section_8155EDBF449E4198863235F94D1EA872}

[!DNL Target]이 CSS 선택기를 생성하는 방법을 지정하십시오.

이러한 선택 사항은 [!DNL Target]에서 사이트 구조를 이해하여 컨텐츠 전달을 위한 더 나은 CSS 선택기를 생성하는 데 도움이 됩니다. 기본적으로 [!DNL Target]은 페이지의 요소 ID를 기준으로 선택기를 생성합니다. 사이트에서 소수의 ID를 사용하거나 같은 페이지에서 ID를 복제하는 경우 클래스를 사용하는 것이 더 나은 옵션이 될 수 있습니다.

다음 옵션 중 하나 또는 둘 다를 선택할 수 있습니다.

| 옵션 | 설명 |
|--- |--- |
| 요소 ID 사용 | 동일한 ID를 여러 요소에 사용하거나 요소 ID가 페이지 로드 시 변경될 경우 이 옵션을 선택 취소하십시오. |
| 요소 클래스 사용 | 기본적으로 [!DNL Target]은 요소 ID만 사용합니다. 그러나 페이지가 [!DNL Adobe Experience Manager]로 작성한 페이지처럼 클래스를 사용하여 요소를 식별하도록 디자인된 경우 [!UICONTROL 요소 클래스 사용]도 선택해야 합니다.<br>**참고**: 정확도를 위한 모든 작업이 수행되었더라도 클래스를 사용하면 오류가 발생할 수 있습니다. 어떤 옵션도 선택하지 않으면 정확도도 영향을 받습니다. 정확도 순서는 ID &gt; 클래스 &gt; 두 옵션을 모두 선택하지 않은 경우입니다. 항상 페이지를 테스트하여 선택기가 올바른지 확인해야 합니다.<br>[!UICONTROL ]활동별로 이 설정을 재정의할 수 있습니다. 설정 톱니바퀴 아이콘을 클릭한 다음, [!UICONTROL CSS 선택기]를 선택합니다. 이 기능은 여러 사이트가 서로 다르게 구성된 경우에 특히 유용합니다.<br>**참고**: 활동별로 이 설정을 재정의하는 기능을 [!UICONTROL 자동화된 개인화] 및 [!UICONROL 다변량 테스트] 활동에서는 사용할 수 없습니다.  선택기에 대한 추가 정보는 ](/help/c-experiences/c-visual-experience-composer/vec-selectors.md)시각적 경험 작성기에서 사용되는 요소 선택기[를 참조하십시오. |

## 시각적 경험 작성기 {#section_CD9BDD372CF54E678F88E8BA95757A5A}

| 옵션 | 설명 |
|--- |--- |
| 기본 시각적 경험 작성기 URL | [!UICONTROL 시각적 경험 작성기]에서 사용되는 기본 URL을 설정합니다. 이것은 홈 페이지와 같이 각 새 활동에 대한 경험을 설정할 때마다 사용되는 기본 페이지입니다. 기본 URL을 설정하지 않은 경우, 활동을 만들 때 각 활동의 URL을 입력해야 합니다. |
| 고급 경험 작성기 활성화 | iFrame 버스팅 사이트 및 혼합 컨텐츠가 있는 사이트에서 편집할 수 있도록 허용합니다. 일부 사이트는 향상된 버전과 호환되지 않을 수 있습니다. 이 경우 이 옵션을 선택 취소하여 원래 경험 작성기로 복구하십시오. 사이트의 활동 전달은 이 선택 옵션의 영향을 받지 않습니다.<br>자세한 내용은 [시각적 경험 작성기 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.<br>**참고**: 활동 수준에서 고급 경험 작성기를 활성화할 수도 있습니다. |
| 혼합 컨텐츠 로드 | 향상된 Experience Composer를 사용하여 웹 사이트를 여는 동안 혼합 콘텐츠를 사용할 수 있습니다. 이 옵션을 활성화하면 Target 프록시 서버를 통해 정적 리소스를 로드하는 오버헤드가 줄어듭니다. |
| 경험 스냅샷 생성 | 경험 스냅샷을 활성화하면 활동 워크플로우 다이어그램에서 경험에 대한 썸네일이 생성됩니다. 스냅샷을 비활성화하면 일부 사용자의 경우 성능이 더 빨라질 수 있습니다. |

## 모바일 뷰포트 구성{#section_42176D062BCE4A28ADBB784CC4BEF84D}을 참조하십시오 

경험을 미리 볼 때 사용할 장치를 추가할 수 있습니다. 각 장치에는 연결된 대상이 있습니다.

| 옵션 | 설명 |
|--- |--- |
| ![Premium 배지](/help/assets/premium.png) 새로 추가 | [!UICONTROL 새로 추가][!UICONTROL 를 클릭하고, 모바일 뷰포트에 대한 수사적 이름을 지정하고, 너비와 높이를 지정한 후 원하는 운영 체제를 선택하고 저장을 클릭하십시오].  모바일 뷰포트를 추가하는 방법에 대한 내용은 [모바일 뷰포트 구성](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md)을 참조하십시오. |

## 교육 비디오: 계정 환경 설정(7:33)

이 비디오에는 계정 기본 설정에 대한 정보가 포함되어 있습니다.

* [!DNL Target Standard]에서 사용할 수 있는 계정 설정을 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17379)