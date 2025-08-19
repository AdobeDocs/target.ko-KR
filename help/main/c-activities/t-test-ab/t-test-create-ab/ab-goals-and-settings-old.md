---
keywords: 활동 설정;A/B 목표 및 설정;보고 설정;목표 지표;성공 지표;종속 성공 지표;고급 설정;기본 목표;추가 지표;목표;우선순위;지속 기간;보고 솔루션;목표;보고 대상자;이 지표를 늘리려면 어떤 성공 지표에 도달해야 합니까;사용자가 이 목표 지표를 접하면 어떻게 됩니까;메모
description: '[!UICONTROL Goals and Settings] 페이지를 사용하여 A/B 활동의 목표에 대한 정보를 지정하는 방법을 알아봅니다.'
title: ' [!DNL Target] A/B 활동에서 목표와 설정을 지정하는 방법'
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 33%

---

# 목표 및 설정

[!UICONTROL Goals & Settings]의 [!DNL Adobe Target] 페이지에서 활동 목표에 대한 정보를 지정합니다.

사용 가능한 설정은 Target 또는 [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을 보고 소스로 사용하는지에 따라 다릅니다.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

[!UICONTROL Activity Settings] 페이지의 [!UICONTROL Goals & Settings] 섹션에서 다음 옵션을 구성할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 설명 |
|--- |--- |
| [!UICONTROL Objective] | 추가 목표를 입력합니다. 목표는 사용자와 팀 구성원이 활동을 식별하는 데 도움이 되는 모든 정보일 수 있습니다. |
| [!UICONTROL Priority] | 설정에 따라 [!DNL Target]에 대한 [!UICONTROL Priority] UI 및 옵션이 달라집니다. [!UICONTROL Low], [!UICONTROL Medium] 또는 [!UICONTROL High]의 기존 설정을 사용하거나 0에서 999까지 세분화된 우선 순위를 사용할 수 있습니다.<P>대상자가 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<P>이 옵션이 [!UICONTROL Administration]&#x200B;(기본값)에서 활성화되지 않으면 우선 순위 [!UICONTROL Low], [!UICONTROL Medium] 또는 [!UICONTROL High]을(를) 지정하십시오.<P>[세분화된 우선 순위](/help/main/administrating-target/reporting.md)를 사용하려면 [!UICONTROL Administration] > [!UICONTROL Reporting]을(를) 클릭한 다음 [!UICONTROL Enable Fine-Grained Priorities] 옵션을 &quot;켜기&quot; 위치로 전환하십시오. <P>이 옵션이 활성화되면 0에서 999 사이의 값을 지정하십시오(0 = [!UICONTROL Low] 및 999 = [!UICONTROL High]). <P>이전 버전의 [!DNL Target]에서 만든 활동의 경우 [!UICONTROL Low] 우선 순위는 0으로, [!UICONTROL Medium]은(는) 5로, [!UICONTROL High]은(는) 10으로 전환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.<P>참고: 세분화된 우선순위를 사용한 후에 이 선택 사항을 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다. |
| 지속 시간 | 활동은 승인될 때 시작되거나 특정 날짜 및 시간을 설정하여 시작할 수 있습니다. 이와 마찬가지로, 활동은 비활성화될 때 종료되거나 날짜 및 시간을 설정하여 종료할 수 있습니다. 시간 선택기는 24시간 시계를 사용하며 00:00은(는) 자정입니다. 해당 시간대는 브라우저에 구성된 시간대로 설정됩니다. 다른 시간대를 사용하려면 브라우저를 다른 시간대로 설정하고 브라우저를 다시 시작하십시오. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

[!UICONTROL Reporting Settings] 페이지의 [!UICONTROL Goals & Settings] 섹션에서 다음 옵션을 구성할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 설명 |
|--- |--- |
| [!UICONTROL Reporting Source] | 수집할 솔루션 데이터 지정:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>[계정 설정](/help/main/administrating-target/reporting.md)에 보고 소스가 지정되어 있으면 지정된 소스가 사용되며 이 설정은 표시되지 않습니다.<P>보고서 일관성을 유지하기 위해 활동이 활성 상태가 되면 보고 소스를 변경할 수 없습니다.<P>**Adobe Analytics**: 보고 솔루션과 각 솔루션의 이점 간의 차이점에 대해 알아보려면 [Target용 보고 Source으로서의 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을 참조하십시오. [!DNL Analytics]에 대한 보고 소스로 [!DNL Target]을(를) 선택할 때 [!DNL Analytics] 활동 데이터를 받을 [!DNL Target] 보고서 세트를 선택합니다.<P>보고 소스를 지정하려면 먼저 사용자 계정이 연결된 [!DNL Analytics] 회사 중에서 선택한 다음 활동에 대한 보고서 세트를 선택합니다. [!DNL Adobe Target]에 연결하기 위해 제공된 보고서 세트만 선택할 수 있습니다. 예상한 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 [!DNL Adobe Experience Cloud]에 다시 로그인하여 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 고객 지원 센터에 문의하십시오.<P><P>**Adobe Customer Journey Analytics**: [[!DNL Target] 과(와)  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) 간의 통합에 대한 자세한 내용은 [!DNL Adobe Customer Journey Analytics]보고 위치[!DNL Target]를 참조하십시오.<P>[!DNL Target]의 [!DNL Customer Journey Analytics] 보고는 수동 트래픽 분할을 사용하는 A/B 활동에서 지원됩니다. [!UICONTROL Auto-Target] 및 [!UICONTROL Auto-Allocate] A/B 활동에서 [!DNL Target]의 [!DNL Customer Journey Analytics] 보고를 사용할 수 없습니다. |
| [!UICONTROL Goal Metric] | 목표를 달성하려면 방문자가 수행한 동작을 선택합니다. 예를 들어 [!UICONTROL Conversion] 지표를 선택한 다음 성공 시기를 결정하는 매개 변수를 설정합니다. 지표 설정에 대한 자세한 내용은 [지표 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md)을 참조하십시오.<P>참고: 보고 솔루션을 [!DNL Analytics]&#x200B;(으)로 설정한 경우 사용 가능한 목표 지표는 [!UICONTROL Conversion]뿐입니다. [!DNL Analytics] 지표를 목표로 선택할 수 없습니다. 성공 지표를 선택하면 선택기가 표시됩니다. 이 선택기를 사용하여 성공 지표의 자세한 정보를 선택합니다.<P>사용하도록 설정하면 [!UICONTROL Estimated Value of the Conversion] 필드([!UICONTROL Page Score] 지표에 사용할 수 없음)가 목표 값을 제공하지만 다른 지표에 대해서는 값을 제공하지 않습니다. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 모든 매출 지표([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] 및 [!UICONTROL Orders])에 대해 예상 값은 [!UICONTROL Revenue per Visitor]을(를) 사용합니다. 데이터 유형은 통화입니다.<P>활동 목표에 도달한 후에는 우선순위가 높은 활동에 방문자가 적격한 경우를 제외하고 방문자에게 활동 콘텐츠가 계속 표시됩니다. 해당 방문자가 목표에 다시 도달하면 다른 전환으로 카운트됩니다. 이는 방문자가 활동을 다시 볼 경우 새 방문자로 계산되는 [!DNL Target Classic]의 기본 비헤이비어와 다릅니다. |
| [!UICONTROL Additional Metrics] | 추가 성공 지표를 만듭니다. 보고 솔루션을 [!DNL Analytics]&#x200B;(으)로 설정한 경우에는 이 설정을 사용할 수 없습니다. 이 경우 [!DNL Analytics] 보고서 세트에 대해 정의된 지표가 적용됩니다. |
| [!UICONTROL Audiences for Reporting] | 기본적으로 보고서에는 자격을 갖춘 모든 방문자의 결과가 표시됩니다. 보고서 대상을 추가하여 특정 대상에만 대한 정보를 표시할 수 있습니다. [!DNL Analytics]을(를) 보고 솔루션으로 선택하는 경우에는 이 설정을 사용할 수 없습니다. [!DNL Analytics] 보고서 세트에 대해 정의된 대상이 적용됩니다. |

## 고급 설정 {#section_E2FE441AFB324E498793ABB025ED9974}

[!UICONTROL Advanced Settings] 페이지의 [!UICONTROL Goals & Settings] 섹션에서 다음 옵션을 구성할 수 있습니다.

고급 설정을 지정하려면 다음 그림과 같이 **[!UICONTROL More]** 아이콘(세로 줄임표)을 클릭한 다음 **[!UICONTROL Advanced Settings]**&#x200B;을(를) 클릭합니다.

![고급 설정 메뉴](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>[!DNL Adobe Analytics]를 보고 소스로 사용하는 경우 설정은 [!DNL Analytics] 서버에서 관리됩니다. 고급 설정 옵션은 사용할 수 없습니다.

![고급 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| 설정 | 설명 |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | 다른 성공 지표에 도달한 적이 있는 경우에만 이 옵션을 사용하여 성공 지표에 도달한 것으로 카운트하십시오. 예를 들어, 방문자가 전환하기 전에 오퍼를 클릭하거나 특정 페이지에 도달한 경우에만 활동 전환이 유효할 수 있습니다. 여러 지표에 대한 종속성과 유연성을 제공하여 카운트를 늘리기 위해 지표에 도달해야 할지 또는 도달하지 않아야 할지를 선택할 수 있습니다. 두 성공 지표(또는 여러 개의 성공 지표)를 정의한 다음 두 성공 지표를 서로 종속시킵니다. [!UICONTROL Add Dependency] 옵션을 사용하면 다른 성공 지표에 도달했거나 도달하지 않은 경우 성공 지표를 늘릴 수 있습니다. 종속성을 추가하려면 다음을 수행하십시오.<ul><li>추가 지표를 추가한 후 [!UICONTROL Advanced Settings]을(를) 클릭합니다.</li><li>[!UICONTROL Add Dependency] 옵션을 클릭합니다.</li><li>왼쪽 창에서 오른쪽 창으로 원하는 지표를 드래그해 놓은 다음 [!UICONTROL Reached]을(를) 클릭하여 [!UICONTROL Reached]과(와) [!UICONTROL  Not Reached] 사이의 설정을 전환합니다.</li><li>종속성을 추가한 후 편집하거나 제거할 수 있습니다.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | 사용자가 목표 지표에 도달한 다음에 진행되는 상황을 지정할 수 있는 세 가지 옵션이 있습니다.<ul><li>카운트가 증분되는 방식을 지정하려면 [!UICONTROL Increment Count & Keep User in Activity]을(를) 선택하십시오.</li><li>[!UICONTROL Increment Count, Release User & Allow Reentry]을(를) 선택하여 사용자가 활동을 다시 입력할 때 표시되는 경험을 지정합니다.</li><li>[!UICONTROL Increment Count, Release User & Bar from Reentry]을(를) 선택하여 활동 콘텐츠 대신 사용자에게 표시되는 콘텐츠를 지정합니다.</li></ul> |
| [!UICONTROL How will the count be incremented?] | 카운트를 늘리는 방법에는 다음 세 가지가 있습니다.<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

고급 설정에 대한 자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

## 기타 메타데이터 {#section_2E8917BEFB954480A4206B9E9E917F80}

[!UICONTROL Other Metadata] 페이지의 [!UICONTROL Goals & Settings] 섹션에서 자신 또는 다른 팀원을 위해 보관하는 데 유용한 활동에 대한 모든 정보를 지정할 수 있습니다. 노트 창의 크기를 조정할 수 있습니다.|

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 활동 설정(3:02) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 활동 설정에 대한 정보가 포함되어 있습니다.

* 활동의 목표 입력
* 활동의 우선순위 수준 설정
* 활동 시작 및 종료 시간 예약
* 보고서 필터를 작성하기 위해 보고 대상 추가
* 활동에 대한 메모 입력

(https://video.tv.adobe.com/v/17381?captions=kor)

### A/B 테스트 만들기(8:36) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에서는 활동을 만들 때 어떻게 활동 설정이 안내가 있는 3단계 워크플로우에 맞게 지정되는지를 보여 줍니다. 목표 및 설정은 5:30부터 논의됩니다.

* Adobe Target에서 A/B 활동 만들기
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391)
