---
keywords: 자동화된 개인화;ap
description: '[!UICONTROL Visual Experience Composer]을(를) 사용하여 [!UICONTROL Automated Personalization]​(AP) 활동을 만드는 방법을 알아봅니다.'
title: '[!UICONTROL Automated Personalization] 활동을 만드는 방법'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: 9cc1eb4c5c95ea51bc0a1fc9e89b245a18c9914b
workflow-type: tm+mt
source-wordcount: '1851'
ht-degree: 23%

---

# [!UICONTROL Automated Personalization] 활동 만들기

[!UICONTROL Visual Experience Composer]&#x200B;(VEC)를 사용하여 [!DNL Adobe Target]에서 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동을 만듭니다.

[!DNL Target]의 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동 워크플로는 다른 활동 유형의 워크플로와 다릅니다.

1. [!DNL Target] [!UICONTROL Activities] 목록에서 **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**&#x200B;을(를) 클릭합니다.

1. VEC([!UICONTROL Visual Experience Composer])를 사용하려면 **[!UICONTROL Visual]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Form-Based Experience Composer]을(를) 사용하려면 [!UICONTROL Form]을(를) 선택하십시오. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL Form-Based Experience Composer] 외에 [!DNL Target]에서 [!UICONTROL Single Page Application VEC]을(를) 제공합니다. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

1. (조건부) [작업 영역을 선택하십시오](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. **[!UICONTROL Enter Activity URL]** 상자에서 [활동 URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)을 지정하십시오.

   계정이 [기본 URL로 구성](/help/main/administrating-target/visual-experience-composer-set-up.md)된 경우 기본적으로 해당 URL이 표시됩니다. 필요한 경우 기본값에서 다른 URL로 변경할 수 있습니다.

   [!DNL Target]은(는) URL 프로토콜([!DNL https] 및 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `http://www.adobe.com`] 및 [!DNL `https://wwww.adobe.com`]이(가) 모두 일치합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

   지정된 URL의 페이지가 VEC에서 열립니다.

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

1. 다음 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)에 설명된 대로 페이지 요소를 수정합니다.

   자산 관리자에서 한꺼번에 여러 이미지를 선택할 수 있습니다. 이렇게 하면 활동에 대해 구성된 각 이미지가 있는 페이지를 빠르게 볼 수 있습니다. 또한 오퍼의 텍스트 요소를 쉽게 편집할 수 있습니다. 요소를 편집하면 해당 요소가 변경되었음을 나타내는 막대가 표시됩니다.

1. **[!UICONTROL Manage Content]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭하여 사용 가능한 조합을 구성합니다.

   대화 상자가 화면 맨 위에 두 개의 옵션([!UICONTROL Experiences] 및 [!UICONTROL Offers])과 함께 표시됩니다.

   >[!NOTE]
   >
   >AP 활동에서 최대 30,000개의 경험을 작성할 수 있지만, 이 활동은 5,000개 미만의 경험이 사용될 때 가장 잘 수행됩니다. 이 제한은 활동이 [!UICONTROL Disalow Duplicates] 옵션을 활성화한 경우에도 적용됩니다.

   [!UICONTROL Experiences] 목록에는 활동에 대해 선택된 각 콘텐츠 부분과 지정된 위치가 표시됩니다.

   원하는 경험 옆에 있는 확인란을 선택한 다음 [!UICONTROL Exclude] 아이콘을 클릭하여 특정 경험을 제외할 수 있습니다.

   관련 경험에 대한 확인란을 선택한 다음 [!UICONTROL Exclude] 아이콘을 클릭하여 경험을 묶음으로 제외하거나 포함할 수 있습니다.

1. (조건부) **[!UICONTROL Offers]**&#x200B;을(를) 클릭하여 콘텐츠를 선택하고 이를 보고 그룹에 지정하거나 특정 방문자만 타깃팅으로 한 특정 오퍼를 볼 수 있도록 합니다.

   보고 그룹에 대한 자세한 내용은 [Automated Personalization의 오퍼 보고 그룹](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md)을 참조하세요.

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.-->

1. 활동의 콘텐츠 설정을 완료했으면 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. 안내가 있는 3단계 워크플로우에서 다음 단계로 이동하려면 [!UICONTROL Visual Experience Composer]의 맨 위에서 **[!UICONTROL Targeting]**&#x200B;을(를) 클릭합니다.

   **타깃팅** 단계는 다른 [!DNL Target] 활동 유형을 사용해본 적이 있는 경우 친숙하게 보입니다. 여기에서 대상을 선택하고 각 경험을 보는 방문자의 비율을 지정할 수 있습니다.

   흐름 다이어그램이 열립니다.

   ![AP 테스트 타깃팅 단계](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

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

1. **[!UICONTROL Traffic Allocation]** 컨트롤을 클릭하여 다음 옵션 중에서 선택합니다.

   ![트래픽 할당 목표 옵션](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** 목표가 알고리즘을 테스트하는 것이면 제어 및 타깃팅된 알고리즘 간에 50/50%로 분할된 방문자를 사용합니다. 이 분할은 가장 정확한 상승도 추정치를 제공합니다. 임의 경험을 제어로 사용하는 것이 좋습니다.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** 목표가 &quot;상시 설정&quot; 활동을 만드는 것이면 방문자의 10%를 제어로 넣으십시오. 이 옵션은 시간에 따라 알고리즘이 계속 학습할 수 있는 충분한 데이터가 있는지 확인합니다. 여기서 장점은 더 많은 트래픽 비율을 개인화하는 대신 정확한 상승도를 파악하는 데는 정밀도가 떨어진다는 점입니다. 목표에 관계없이 이 옵션은 특정 경험을 제어로 사용할 때 권장되는 트래픽 분할입니다.
   * **[!UICONTROL Custom Allocation]:** 원하는 대로 백분율을 수동으로 분할합니다.

1. (조건부) [!UICONTROL Control] 드롭다운 목록에서 [제어로 사용할 특정 환경을 선택](/help/main/c-activities/t-automated-personalization/experience-as-control.md)하거나 [!UICONTROL Random Experience.]을(를) 선택합니다

   제어 경험은 자동 테스트에서 제공하는 상승도 수준을 판별하기 위한 비교를 제공합니다.

   [!UICONTROL Automated Personalization]은(는) 항상 컨트롤 그룹에 대한 성능을 측정합니다. 우수 사례는 최소 10%의 참여자를 통제군에 배치하는 것입니다. 데이터 소스에 지정된 개인화 알고리즘이 어떤 개인화도 수행하지 않는 것(예: 임의로 제공되는 컨트롤)보다 더 잘 수행되는지 테스트하는 것이 목표라면 제어와 개인화 알고리즘 간에 50/50%로 분할된 트래픽이 이 목표를 달성하는 가장 빠르고 정확한 방법입니다. 개인화된 트래픽의 양을 극대화하려는 경우 활동이 생성하는 정확한 상승도를 이해하는 데 관심이 적다면 제어와 개인화 알고리즘 간에 10/90%의 트래픽 분할이 이 이 목표를 달성할 수 있는 가장 빠르고 정확한 방법입니다.

   >[!NOTE]
   >
   >[!UICONTROL Automated Personalization] 활동에서 각 요청에 대해 항목 기준(URL 타겟팅, 템플릿 규칙 및 대상 타겟)이 평가됩니다. 이전 버전에서는 항목 기준이 세션당 한 번만 평가되었습니다.

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 **[!UICONTROL Goals & Settings]** 페이지를 표시합니다.
1. 다음 설정으로 활동을 구성한 다음 **[!UICONTROL Save & Close]**&#x200B;을(를) 클릭합니다.

   | 설정 | 설명 |
   |--- |--- |
   | [!UICONTROL Name] | 활동의 이름을 지정합니다. 팀 구성원이 [!UICONTROL Activities] 목록에서 활동을 인식할 수 있을 만큼 충분히 설명적인 이름을 지정합니다. 활동 이름에 허용되지 않는 문자를 확인하려면 위의 테이블을 참조하십시오. |
   | [!UICONTROL Objective] | (선택 사항) 테스트의 목표를 입력합니다. 목표는 활동의 목적을 기억하는 데 도움이 됩니다. |
   | [!UICONTROL Priority] | 설정에 따라 [!UICONTROL Priority]에 대한 [!DNL Target] UI 및 옵션이 달라집니다. [!UICONTROL Low], [!UICONTROL Medium] 또는 [!UICONTROL High]의 기존 설정을 사용하거나 0에서 999까지 세분화된 우선 순위를 사용할 수 있습니다.<P>대상자가 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<P>이 옵션이 [!UICONTROL Administration] > [!UICONTROL Reporting]&#x200B;(기본값)에서 활성화되지 않으면 우선 순위([!UICONTROL Low], [!UICONTROL Medium] 또는 [!UICONTROL High])를 지정하십시오.<P>세분화된 우선 순위를 사용하려면 [!UICONTROL Administration] > [!UICONTROL Reporting]을(를) 클릭한 다음 [!UICONTROL Enable Fine-Grained Priorities] 옵션을 &quot;켜기&quot; 위치로 전환하십시오.<P>이 옵션이 활성화되면 0에서 999 사이의 값을 지정하십시오.<ul><li>0 = 낮음</li><li>999 = 높음</li></ul>이전 버전의 [!DNL Target Standard/Premium]에서 만든 활동의 경우 [!UICONTROL Low] 우선 순위는 0으로, [!UICONTROL Medium] 우선 순위는 5로, [!UICONTROL High] 우선 순위는 10으로 전환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.<P>**참고**: 세분화된 우선순위를 사용한 후에 이 옵션을 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다. |
   | [!UICONTROL Duration] | 활동의 시작 및 종료 날짜를 설정합니다. [!UICONTROL When Activated]을(를) 선택하거나 특정 날짜 및 시간을 지정할 수 있습니다. |
   | [!UICONTROL Optimization Goal] | 다음 두 개의 매개 변수로 구성되는 최적화 목표를 지정하십시오.<ul><li>활동으로 측정하려는 작업</li><li>목표가 달성되었음을 보여 주는 작업으로, 활동 참여자가 수행한 것입니다.</li></ul>[!UICONTROL My Primary Goal]의 오른쪽에 있는 세 점을 선택하여 최적화 목표의 이름을 지정할 수 있습니다. [!UICONTROL Automated Personalization] 활동은 [!UICONTROL Conversion] 또는 [!UICONTROL Revenue]을(를) 측정할 수 있습니다. 페이지 보기 또는 mbox 보기를 통해 전환할 수 있습니다. 클릭을 추적할 수도 있습니다.<P>또한 기본 목표는 경험의 성공을 계산하기 위해 모델링 시스템에서 사용하는 모델링 지표가 됩니다.<P>모델링 목표에 도달한 후 추적 목적으로 활동에 방문자를 유지할 수 있습니다. 예를 들어 [!UICONTROL Automated Personalization] 활동은 종종 클릭률을 향상시키는 데 사용되며 모델링 목표로 설정됩니다. 그러나 증가된 클릭률이 최종 전환으로 이어지는 방식을 확인하는 것이 중요하므로 최종 전환까지 추적하는 것이 반드시 필요합니다.<P>여러 지표에 대한 종속성과 유연성을 제공하여 카운트를 늘리기 위해 지표에 도달해야 할지 또는 도달하지 않아야 할지를 선택할 수 있습니다.<P>두 성공 지표(또는 여러 개의 성공 지표)를 정의해야 상호 종속성을 만들 수 있습니다.<P>[!UICONTROL Add Dependency] 옵션을 사용하면 다른 성공 지표에 도달했거나 도달하지 않은 경우 성공 지표를 늘릴 수 있습니다.<P>종속성을 추가하려면 다음을 수행하십시오.<ol><li>추가 지표를 추가한 후 [!UICONTROL Additional Goal]의 오른쪽에 있는 세 점 메뉴 아래에서 **[!UICONTROL Advanced Settings]**&#x200B;을(를) 클릭합니다.</li><li>[!UICONTROL Reporting Settings] 섹션 아래쪽의 **[!UICONTROL Add Dependency]** 옵션을 클릭합니다.</li><li>왼쪽 창에서 오른쪽 창으로 원하는 지표를 드래그해 놓은 다음 [!UICONTROL Reached]을(를) 클릭하여 [!UICONTROL Reached]과(와) [!UICONTROL Not Reached] 사이의 설정을 전환합니다.</li></ol>종속성을 추가한 후 편집하거나 제거할 수 있습니다. |
   | [!UICONTROL Conversion Metric] | 기본적으로 전환 지표는 최적화 목표 지표와 동일합니다. 그러나 [!UICONTROL Same as Optimization Goal] 옵션을 선택 취소하여 별도의 전환 지표를 정의할 수 있습니다. |
   | [!UICONTROL Additional Metrics] | 사용할 추가 보고 지표를 추가합니다. 변환 또는 수입 지표를 추가할 수 있습니다.<P>**참고**: [!UICONTROL Engagement] 지표는 추가 지표로 지원되지 않습니다. [!DNL Target] UI를 통해 [!UICONTROL Engagement] 지표를 선택할 수 있지만 데이터가 보고서에 정확하게 표시되지 않습니다. |
   | [!UICONTROL Audiences for Reporting] | 보고서의 대상별로 필터링하려면 대상을 추가합니다. 기본적으로 보고서는 자격 있는 모든 방문자의 결과를 표시합니다. 방문자의 보다 구체적인 하위 집합을 위해 결과를 필터링하려면 대상을 추가합니다.<P>**참고**: 다른 활동 형식과 달리 [!UICONTROL Automated Personalization]에서는 [!UICONTROL Adobe Analytics]을(를) 보고 소스로 사용(A4T)할 수 없습니다. |
   | [!UICONTROL Notes] | 귀하 또는 다른 팀 구성원에게 유용한 활동에 대한 정보를 입력합니다. [!UICONTROL Notes] 창의 크기를 조정할 수 있습니다. |

   지표의 이름을 지정하거나 지표의 이름을 바꾸는 경우 다음 문자가 허용되지 않습니다.

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

**[!UICONTROL Save & Close]**&#x200B;을(를) 클릭하면 활동의 [!UICONTROL Overview] 페이지가 표시됩니다. **경험 미리 보기**&#x200B;를 클릭하여 경험이 전달될 때 어떻게 표시되는지 미리 봅니다. 사이트에서 AP 경험에 대한 링크를 보고 공유하여 [!UICONTROL Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 외부의 경험에 대한 &quot;실제 미리 보기&quot;를 얻을 수 있는 팝업이 나타납니다. 미리 보기를 공유하려면 메시지에서 링크를 공유해야 합니다. 링크를 클릭한 다음 브라우저에서 직접 URL을 복사할 수 없습니다. 링크를 복사하면 메시지의 링크에서 페이지에 액세스할 때만 페이지가 올바르게 표시되는 매개 변수가 URL에 포함됩니다.

보고에 대한 자세한 내용은 [Automated Personalization 보고서](/help/main/c-reports/personalization-reports/reports-ap.md)를 참조하십시오.
