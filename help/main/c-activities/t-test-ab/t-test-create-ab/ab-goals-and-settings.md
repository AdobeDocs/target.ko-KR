---
keywords: 활동 설정;A/B 목표 및 설정;보고 설정;목표 지표;성공 지표;종속 성공 지표;고급 설정;기본 목표;추가 지표;목표;우선순위;지속 기간;보고 솔루션;목표;보고 대상;이 지표를 늘리려면 어떤 성공 지표에 도달해야 합니까;사용자가 이 목표 지표를 접하면 어떻게 됩니까;메모
description: 사용 방법 알아보기 [!UICONTROL Goals and Settings] A/B 활동의 목표에 대한 정보를 지정하는 페이지입니다.
title: 에서 목표 및 설정을 지정하는 방법 [!DNL Target] A/B 활동
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: b5f508d283390c859085d4ee52c582312085addc
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 35%

---

# 목표 및 설정

다음 [!UICONTROL Goals & Settings] 페이지 위치 [!DNL Adobe Target] 은 활동의 목표에 대한 정보를 지정하는 곳입니다.

사용 가능한 설정은 Target 사용 여부에 따라 다릅니다. [분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md) 를 보고 소스로 사용합니다.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

다음 [!UICONTROL Activity Settings] 의 섹션 [!UICONTROL Goals & Settings] 페이지에서는 다음 옵션을 구성할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 설명 |
|--- |--- |
| [!UICONTROL Objective] | 추가 목표를 입력합니다. 목표는 사용자와 팀 구성원이 활동을 식별하는 데 도움이 되는 모든 정보일 수 있습니다. |
| [!UICONTROL Priority] | 설정에 따라 [!DNL Target] 의 UI 및 옵션 [!UICONTROL Priority] 다양합니다. 의 이전 설정을 사용할 수 있습니다. [!UICONTROL Low], [!UICONTROL Medium], 또는 [!UICONTROL High]또는 0에서 999까지 세분화된 우선순위를 활성화할 수 있습니다.<P>대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<P>이 옵션이에서 활성화되지 않은 경우 [!UICONTROL Administration] (기본값), 우선 순위를 지정합니다. [!UICONTROL Low], [!UICONTROL Medium], 또는 [!UICONTROL High].<P>활성화하려면 [세분화된 우선 순위](/help/main/administrating-target/reporting.md), 클릭 [!UICONTROL Administration] > [!UICONTROL Reporting]을 클릭한 다음 을 전환합니다 [!UICONTROL Enable Fine-Grained Priorities] 옵션을 &quot;켜짐&quot; 위치에 추가합니다. <P>이 옵션이 활성화되면 0에서 999 사이의 값을 지정하십시오(0 = ). [!UICONTROL Low] 및 999 = [!UICONTROL High]. <P>이전 버전에서 만든 활동의 경우 [!DNL Target], [!UICONTROL Low] 우선 순위가 0으로 전환됩니다. [!UICONTROL Medium] 5로 변환되고, [!UICONTROL High] 는 10으로 변환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.<P>참고: 세분화된 우선순위를 사용한 후에 이 선택 사항을 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다. |
| 지속 시간 | 활동은 승인될 때 시작되거나 특정 날짜 및 시간을 설정하여 시작할 수 있습니다. 이와 마찬가지로, 활동은 비활성화될 때 종료되거나 날짜 및 시간을 설정하여 종료할 수 있습니다. 시간 선택기는 24시간 형식을 사용하며 00:00은 자정을 나타냅니다. 해당 시간대는 브라우저에 구성된 시간대로 설정됩니다. 다른 시간대를 사용하려면 브라우저를 다른 시간대로 설정하고 브라우저를 다시 시작하십시오. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

다음 [!UICONTROL Reporting Settings] 의 섹션 [!UICONTROL Goals & Settings] 페이지에서는 다음 옵션을 구성할 수 있습니다.

| 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 | 설명 |
|--- |--- |
| [!UICONTROL Reporting Source] | 수집할 솔루션 데이터 지정:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>에 보고 소스가 지정된 경우 [계정 설정](/help/main/administrating-target/reporting.md)지정된 소스가 사용되며 이 설정은 표시되지 않습니다.<P>보고서 일관성을 유지하기 위해 활동이 활성 상태가 되면 보고 소스를 변경할 수 없습니다.<P>**Adobe Analytics**: 를 참조하십시오 [Target용 보고 소스로서의 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) 보고 솔루션의 차이점과 각각의 장점에 대해 알아봅니다. 선택 시 [!DNL Analytics] 을(를) 위한 보고 소스로 사용 [!DNL Target], 다음을 선택합니다. [!DNL Analytics] 받을 보고서 세트 [!DNL Target] 활동 데이터.<P>보고 소스를 지정하려면 먼저 다음 중 하나를 선택합니다 [!DNL Analytics] 계정이 연결된 회사 를 선택한 다음 활동에 대한 보고서 세트를 선택합니다. 연결할 수 있도록 프로비저닝된 보고서 세트만 [!DNL Adobe Target] 선택할 수 있습니다. 예상하는 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 다음에 다시 로그인하십시오 [!DNL Adobe Experience Cloud] 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 고객 지원 센터에 문의하십시오.<P><P>**Adobe Customer Journey Analytics**: 를 참조하십시오 [[!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) 를 참조하십시오. [!DNL Adobe Customer Journey Analytics] 및 [!DNL Target].<P>[!DNL Target] 보고 위치 [!DNL Customer Journey Analytics] 는 수동 트래픽 분할을 사용하는 A/B 활동에서 지원됩니다. [!UICONTROL Auto-Target] 및 [!UICONTROL Auto-Allocate] A/B 활동은 다음을 사용할 수 없습니다. [!DNL Target] 보고 위치 [!DNL Customer Journey Analytics]. |
| [!UICONTROL Goal Metric] | 목표를 달성하려면 방문자가 수행한 동작을 선택합니다. 예를 들어 [!UICONTROL Conversion] 지표를 만든 다음 성공 시기를 결정하는 매개 변수를 설정합니다. 지표 설정에 대한 자세한 내용은 [지표 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md)을 참조하십시오.<P>참고: 보고 솔루션을 로 설정한 경우 [!DNL Analytics], 사용 가능한 유일한 목표 지표는 다음과 같습니다 [!UICONTROL Conversion]. [!DNL Analytics] 지표를 목표로 선택할 수 없습니다. 성공 지표를 선택하면 선택기가 표시됩니다. 이 선택기를 사용하여 성공 지표의 자세한 정보를 선택합니다.<P>활성화된 경우 [!UICONTROL Estimated Value of the Conversion] 필드(다음에 사용할 수 없음) [!UICONTROL Page Score] 지표)는 목표에 대한 값을 제공하지만 다른 지표에 대해서는 제공하지 않습니다. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 모든 매출 지표([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], 및 [!UICONTROL Orders]), 예상 사용 [!UICONTROL Revenue per Visitor]. 데이터 유형은 통화입니다.<P>활동 목표에 도달한 후에는 우선순위가 높은 활동에 방문자가 적격한 경우를 제외하고 방문자에게 활동 콘텐츠가 계속 표시됩니다. 해당 방문자가 목표에 다시 도달하면 다른 전환으로 카운트됩니다. 이는 의 기본 비헤이비어와 다릅니다. [!DNL Target Classic]: 방문자가 활동을 다시 보는 경우 새 방문으로 카운트합니다. |
| [!UICONTROL Additional Metrics] | 추가 성공 지표를 만듭니다. 보고 솔루션을 로 설정한 경우에는 이 설정을 사용할 수 없습니다. [!DNL Analytics]. 이 경우 다음에 대해 정의된 지표 [!DNL Analytics] 보고서 세트가 적용됩니다. |
| [!UICONTROL Audiences for Reporting] | 기본적으로 보고서에는 자격을 갖춘 모든 방문자의 결과가 표시됩니다. 보고서 대상을 추가하여 특정 대상에만 대한 정보를 표시할 수 있습니다. 이 설정은 다음을 선택하는 경우 사용할 수 없습니다. [!DNL Analytics] 를 보고 솔루션으로 사용하십시오. 다음에 대해 정의된 대상자 [!DNL Analytics] 보고서 세트가 적용됩니다. |

## 고급 설정 {#section_E2FE441AFB324E498793ABB025ED9974}

다음 [!UICONTROL Advanced Settings] 의 섹션 [!UICONTROL Goals & Settings] 페이지에서는 다음 옵션을 구성할 수 있습니다.

고급 설정을 지정하려면 **[!UICONTROL More]** 아이콘(세로 줄임표)을 클릭한 다음 **[!UICONTROL Advanced Settings]**&#x200B;다음 그림과 같이 을 참조하십시오.

![고급 설정 메뉴](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>[!DNL Adobe Analytics]를 보고 소스로 사용하는 경우 설정은 [!DNL Analytics] 서버에서 관리됩니다. 고급 설정 옵션은 사용할 수 없습니다.

![고급 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| 설정 | 설명 |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | 다른 성공 지표에 도달한 적이 있는 경우에만 이 옵션을 사용하여 성공 지표에 도달한 것으로 카운트하십시오. 예를 들어, 방문자가 전환하기 전에 오퍼를 클릭하거나 특정 페이지에 도달한 경우에만 활동 전환이 유효할 수 있습니다. 여러 지표에 대한 종속성과 유연성을 제공하여 카운트를 늘리기 위해 지표에 도달해야 할지 또는 도달하지 않아야 할지를 선택할 수 있습니다. 두 성공 지표(또는 여러 개의 성공 지표)를 정의한 다음 두 성공 지표를 서로 종속시킵니다. 다음 [!UICONTROL Add Dependency] 옵션을 사용하면 다른 성공 지표에 도달했거나 도달하지 않은 경우 성공 지표를 늘릴 수 있습니다. 종속성을 추가하려면 다음을 수행하십시오.<ul><li>추가 지표를 추가한 후 [!UICONTROL Advanced Settings].</li><li>다음을 클릭합니다. [!UICONTROL Add Dependency] 옵션:</li><li>왼쪽 창에서 오른쪽 창으로 원하는 지표를 드래그해 놓은 다음 를 클릭합니다 [!UICONTROL Reached] 설정 전환 [!UICONTROL Reached] 및[!UICONTROL  Not Reached].</li><li>종속성을 추가한 후 편집하거나 제거할 수 있습니다.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | 사용자가 목표 지표에 도달한 다음에 진행되는 상황을 지정할 수 있는 세 가지 옵션이 있습니다.<ul><li>선택 [!UICONTROL Increment Count & Keep User in Activity] 카운트가 증분되는 방식을 지정합니다.</li><li>선택 [!UICONTROL Increment Count, Release User & Allow Reentry] 활동을 다시 입력할 때 사용자에게 표시되는 경험을 지정합니다.</li><li>선택 [!UICONTROL Increment Count, Release User & Bar from Reentry] 활동 콘텐츠 대신 사용자에게 표시되는 콘텐츠를 지정합니다.</li></ul> |
| [!UICONTROL How will the count be incremented?] | 카운트를 늘리는 방법에는 다음 세 가지가 있습니다.<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

고급 설정에 대한 자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

## 기타 메타데이터 {#section_2E8917BEFB954480A4206B9E9E917F80}

다음 [!UICONTROL Other Metadata] 의 섹션 [!UICONTROL Goals & Settings] 페이지를 사용하여 자신 또는 다른 팀원이 계속 사용할 수 있는 활동에 대한 모든 정보를 지정할 수 있습니다. 노트 창의 크기를 조정할 수 있습니다.|

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

이 비디오에서는 활동을 만들 때 어떻게 활동 설정이 안내가 있는 3단계 워크플로우에 맞게 지정되는지를 보여 줍니다. 목표 및 설정은 5시 30분부터 논의됩니다.

* Adobe Target에서 A/B 활동 만들기
* 수동 분할 또는 자동 트래픽 할당을 사용한 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17391)
