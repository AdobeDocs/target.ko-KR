---
keywords: 자동화된 개인화;ap;대상;앙상블;랜덤 포레스트;잔차 분산;오차 분산;라이프타임 값
description: 을(를) 만드는 방법 알아보기 [!UICONTROL Automated Personalization] 에서 (AP) 활동 [!DNL Adobe Target] 사용 [!UICONTROL 시각적 경험 작성기].
title: 다음을 만드는 방법 [!UICONTROL Automated Personalization] 활동?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '1853'
ht-degree: 61%

---

# [!UICONTROL Automated Personalization] 활동 만들기

만들기 [!UICONTROL Automated Personalization] 에서 (AP) 활동 [!DNL Adobe Target] 사용 [!UICONTROL 시각적 경험 작성기] (VEC).

다음 [!UICONTROL Automated Personalization] 의 (AP) 활동 워크플로 [!DNL Adobe Target] 다른 활동 유형의 워크플로우와 다릅니다.

1. 다음에서 [!DNL Target] [!UICONTROL 활동] 목록, 클릭 **[!UICONTROL 활동 만들기]** > **[!UICONTROL Automated Personalization]**.

   ![활동 만들기: 자동화된 맞춤설정](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. VEC를 사용하려면 **[!UICONTROL 시각적(기본값)]**.

   ![자동화된 맞춤설정 활동 만들기 대화 상자](/help/main/c-activities/t-automated-personalization/assets/ap_url-new.png){width="300"}

   을(를) 사용하려면 [!UICONTROL 양식 기반 경험 작성기], 선택 [!UICONTROL 양식]. 자세한 내용은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

   >[!NOTE]
   >
   >VEC 및 [!UICONTROL 양식 기반 경험 작성기], [!DNL Target] 오퍼 [!UICONTROL 단일 페이지 애플리케이션 VEC]. 여러 작성기에 대한 자세한 내용은 [경험 및 오퍼](/help/main/c-experiences/experiences.md)를 참조하십시오.
   >
   >VEC에 대한 문제 해결 정보는 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (조건부) [작업 영역 선택](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. 활동 URL을 확인하거나 입력한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `http://www.adobe.com`]과 [!DNL `https://wwww.adobe.com`]은 모두 같습니다.

   지정된 URL의 페이지가 VEC에서 열립니다.

1. 활동의 이름을 지정하려면 **[!UICONTROL 이름]** 필드에 활동 이름을 입력합니다.

   ![이름 필드](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

   활동 이름은 다음 문자로 시작할 수 없습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

   또한 활동 이름에는 &#39;;=&#39;, &#39;;+&#39;, &#39;;-&#39;, &#39;;@&#39;, &#39;,=&#39;, &#39;,+&#39;, &#39;,-&#39;, &#39;,@&#39;, &#39; 문자 시퀀스를 포함할 수 없습니다.[&quot;&#39;, &quot;]&#39;, &#39;[&quot;, &quot;]&#39;.

1. 다음 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)에 설명된 대로 페이지 요소를 수정합니다.

   자산 관리자에서 한꺼번에 여러 이미지를 선택할 수 있습니다. 이렇게 하면 활동에 대해 각 이미지가 구성된 페이지를 빠르게 볼 수 있습니다. 또한 오퍼의 텍스트 요소를 쉽게 편집할 수 있습니다. 요소를 편집하면 해당 요소가 변경되었음을 나타내는 막대가 표시됩니다.

1. **[!UICONTROL 콘텐츠 관리]**&#x200B;를 클릭하여 사용 가능한 조합을 구성합니다.

   ![콘텐츠 관리 옵션](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   화면 맨 위에 세 가지 옵션이 있는 대화 상자가 나타납니다. [!UICONTROL 경험], [!UICONTROL 오퍼], 및 [!UICONTROL 제외 그룹].

   ![콘텐츠 관리 대화 상자](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >AP 활동에서 최대 30,000개의 경험을 작성할 수 있지만, 이 활동은 5,000개 미만의 경험이 사용되는 경우 가장 잘 수행됩니다. 이 제한은 활동이 [!UICONTROL 중복 요소 차단] 옵션을 활성화한 경우에도 적용됩니다.

   다음 [!UICONTROL 경험] 목록에는 활동에 대해 선택된 각 콘텐츠 부분과 지정된 위치가 표시됩니다.

   원하는 경험을 마우스로 가리킨 다음, [!UICONTROL 제외] 아이콘.

   ![제외 아이콘 가리키기](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   관련 경험에 대한 확인란을 선택한 다음, 를 클릭하여 경험을 묶음으로 제외/포함할 수 있습니다. [!UICONTROL 제외] 대화 상자의 오른쪽 상단 모서리에 있는 아이콘

   ![일괄 제외 옵션](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   [!UICONTROL 상태] 드롭다운 목록을 클릭하여 제외되거나 포함된 활동만 표시하도록 이 목록 보기를 필터링할 수 있습니다.

1. (조건부) **[!UICONTROL 오퍼]**&#x200B;를 클릭하여 콘텐츠를 선택하고 이를 보고 그룹에 지정하거나 특정 방문자만 타깃팅으로 한 특정 오퍼를 볼 수 있도록 합니다.

   보고 그룹에 대한 자세한 내용은 [Automated Personalization의 오퍼 보고 그룹](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (조건부) **[!UICONTROL 제외 그룹]**&#x200B;을 클릭하여 활동에서 제외할 요소의 조합을 선택합니다.

   ![콘텐츠 관리 대화 상자의 제외 그룹 탭](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   AP 테스트에서 최대 30,000개의 경험을 만들 수 있지만, 이 알고리즘은 사용되는 고유 경험이 10,000개 보다 작을 때 가장 잘 수행됩니다. 이 제한은 활동이 [!UICONTROL 중복 요소 차단] 옵션을 활성화한 경우에도 적용됩니다.

   현재, 활동에 포함된 제외 그룹이 없는 경우 **제외 그룹 만들기**&#x200B;를 클릭합니다. 제외할 조합만 표시하는 목록을 만들도록 필터링할 수 있습니다. 제외 그룹의 이름을 지정하고 **저장**&#x200B;을 클릭합니다.

   기존 제외 그룹을 편집하려면 편집할 그룹 위로 마우스를 가져간 후 연필 아이콘을 클릭합니다.

1. 활동의 콘텐츠 설정을 완료했으면 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

1. 다음 **타겟팅** 다른 단계를 사용한 적이 있는 경우 단계가 익숙합니다. [!DNL Target] 활동 유형. 여기서 대상을 선택하고, 다음을 클릭하여 제어 경험을 보는 방문자의 비율을 지정할 수 있습니다. **[!UICONTROL 사용자 지정 할당]** 드롭다운 목록을 클릭한 다음 **다음**.

   [!UICONTROL 사용자 지정 할당] 드롭다운 목록에서 다음 선택 사항 중에 선택할 수 있습니다.

   ![트래픽 할당 목표 드롭다운 목록](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL 개인화 알고리즘 평가(50/50)]:** 목표가 알고리즘을 테스트하는 것이면 제어 및 타깃팅된 알고리즘 간에 50/50%로 분할된 방문자를 사용합니다. 이 분할은 가장 정확한 상승도 추정치를 제공합니다. 임의 경험을 제어로 사용하는 것이 좋습니다.
   * **[!UICONTROL 개인화 트래픽 최대화(90/10)]:** 목표가 &quot;상시 설정&quot; 활동을 만드는 것이면 방문자의 10%를 제어권에 넣습니다. 이 옵션은 시간에 따라 알고리즘이 계속 학습할 수 있는 충분한 데이터가 있는지 확인합니다. 여기서 장점은 더 많은 트래픽 비율을 개인화하는 대신 정확한 상승도를 파악하는 데는 정밀도가 떨어진다는 점입니다. 목표에 관계없이, 특정 경험을 제어로 사용할 때 권장되는 트래픽 분할입니다.
   * **[!UICONTROL 사용자 지정 할당]:** 원하는 대로 백분율을 수동으로 분할합니다.

1. (조건부) [!UICONTROL 제어] 드롭다운 목록에서 [제어로 사용할 특정 경험을 선택](/help/main/c-activities/t-automated-personalization/experience-as-control.md)하거나 [!UICONTROL 임의 경험]을 선택합니다.

   제어 경험은 자동 테스트에서 제공하는 상승도 수준을 판별하기 위한 비교를 제공합니다.

   [!UICONTROL 자동화된 개인화는 항상 통제군을 기준으로 성능을 측정합니다. ] 우수 사례는 최소 10%의 참여자를 통제군에 배치하는 것입니다. 목표가 지정된 데이터에 대한 개인화 알고리즘이 개인화가 없는 경우(즉, 무작위로 제공되는 제어)보다 더 나은 결과를 가져올 경우 제어 알고리즘과 개인화 알고리즘 간의 50/50% 트래픽 분할이 이 목표를 달성할 수 있는 가장 빠르고 가장 정확한 방법이 됩니다. 개인화된 트래픽의 양을 최대화하려고 하며, 활동이 생성하는 정확한 상승도를 이해하는 것은 별로 중요하지 않을 경우, 제어 알고리즘과 개인화 알고리즘 간의 10/90% 트래픽 분할이 이 목표를 달성할 수 있는 가장 빠르고 가장 정확한 방법이 됩니다.

   >[!NOTE]
   >
   >위치 [!UICONTROL Automated Personalization] 각 요청에 대해 활동, 항목 기준(URL 타겟팅, 템플릿 규칙 및 대상 타겟)이 평가됩니다. 이전 버전에서는 항목 기준이 세션당 한 번만 평가되었습니다.

1. **[!UICONTROL 다음]**&#x200B;을 클릭하여 **[!UICONTROL 목표 및 설정]** 페이지를 표시합니다.
1. 다음 설정으로 활동을 구성한 다음 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭합니다.

   | 설정 | 설명 |
   |--- |--- |
   | [!UICONTROL 이름] | 활동의 이름을 지정합니다. 활동에서 팀원이 알아볼 수 있을 만큼 충분히 설명적인 이름을 지정합니다. [!UICONTROL 활동] 목록을 표시합니다. 활동 이름에 허용되지 않는 문자를 확인하려면 위의 표를 참조하십시오. |
   | [!UICONTROL 목표] | (선택 사항) 테스트의 목표를 입력합니다. 목표는 활동의 목적을 기억하는 데 도움이 됩니다. |
   | [!UICONTROL 우선순위] | 설정에 따라 [!UICONTROL 우선순위]의 UI 및 옵션이 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다.<br>대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<br>이 옵션이에서 활성화되지 않은 경우 [!UICONTROL 관리] > [!UICONTROL 보고] (기본값), 우선순위를 낮음, 중간 또는 높음으로 지정합니다.<br>세분화된 우선순위를 활성화하려면 [!UICONTROL 관리] > [!UICONTROL 보고]을 클릭한 다음 을 전환합니다 [!UICONTROL 세분화된 우선순위 사용] 옵션을 &quot;켜짐&quot; 위치에 추가합니다.<br>이 옵션이 활성화되면 0에서 999 사이의 값을 지정하십시오.<ul><li>0 = 낮음</li><li>999 = 높음</li></ul>이전 버전의 [!DNL Target Standard/Premium]에서 만든 활동의 경우, 낮음 우선순위는 0으로, 중간은 5로, 높음은 10으로 전환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.<br>**참고:** 세분화된 우선순위를 사용한 후에 이 선택 사항을 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다. |
   | [!UICONTROL 지속 시간] | 활동의 시작 날짜와 종료 날짜를 설정합니다. 다음을 선택할 수 있습니다. [!UICONTROL 활성화 시] 또는 특정 날짜 및 시간을 지정할 수 있습니다. |
   | [!UICONTROL 최적화 목표] | 다음 두 개의 매개 변수로 구성되는 최적화 목표를 지정하십시오.<ul><li>활동으로 측정하려는 작업</li><li>목표가 달성되었음을 보여 주는 작업으로, 활동 참여자가 수행한 것입니다.</li></ul>의 오른쪽에 있는 세 개의 점을 선택하여 최적화 목표의 이름을 지정할 수 있습니다 [!UICONTROL 내 기본 목표]. [!UICONTROL Automated Personalization] 활동이 측정할 수 있음 [!UICONTROL 전환] 또는 [!UICONTROL 매출]. 페이지를 보거나 mbox를 보면 전환이 달성될 수 있습니다. 클릭을 추적할 수도 있습니다.<br>또한 기본 목표는 모델링 시스템에서 경험의 성공을 계산하는 데 사용하는 모델링 지표가 됩니다.<br>모델링 목표에 도달한 후 추적 목적으로 활동에 방문자를 유지할 수 있습니다. 예를 들어 다음과 같은 경우가 있습니다. [!UICONTROL Automated Personalization] 활동은 클릭률을 향상시키는 데 사용되며 모델링 목표로 설정됩니다. 그러나 증가된 클릭률이 최종 전환으로 이어지는 방식을 확인하는 것이 중요하므로 최종 전환까지 추적하는 것이 반드시 필요합니다.<br>여러 지표에 대한 종속성과 유연성을 제공하여 카운트를 늘리기 위해 지표에 도달해야 할지 또는 도달하지 않아야 할지를 선택할 수 있습니다.<br>두 성공 지표(또는 여러 개의 성공 지표)를 정의해야 상호 종속성을 만들 수 있습니다.<br>종속성 추가 옵션을 사용하면 다른 성공 지표에 도달했거나 도달하지 않은 경우 성공 지표를 늘릴 수 있습니다.<br>종속성을 추가하려면 다음을 수행하십시오.<ol><li>추가 지표를 추가한 후에 추가 목표 오른쪽에 있는 3개 점 메뉴 아래에서 **[!UICONTROL 고급 설정]**[!UICONTROL 을 클릭합니다].</li><li>[!UICONTROL 보고 설정] 섹션의 하단에 있는 **[!UICONTROL 종속성 추가]** 선택 사항을 클릭합니다.</li><li>왼쪽 창에서 오른쪽 창으로 원하는 지표를 드래그해 놓은 다음 [!UICONTROL 도달]을 클릭하여 [!UICONTROL 도달] 및 [!UICONTROL 도달 못 함] 간에 설정을 전환합니다</li></ol>종속성을 추가한 후 편집하거나 제거할 수 있습니다. |
   | [!UICONTROL 변환 지표] | 기본적으로 전환 지표는 최적화 목표 지표와 동일합니다. 하지만 [!UICONTROL 최적화 목표와 같음] 옵션을 선택 취소하여 별도의 전환 지표를 정의할 수 있습니다. |
   | [!UICONTROL 추가 지표] | 사용할 추가 보고 지표를 추가합니다. 변환 또는 수입 지표를 추가할 수 있습니다.<br>**참고:** 참여 지표도 추가 지표로 지원되지 않습니다. UI를 통해 다음을 선택할 수 있습니다. [!UICONTROL 참여] 지표를 사용하지만 데이터가 보고서에 정확하게 표시되지 않습니다. |
   | [!UICONTROL 보고 대상] | 보고서의 대상별로 필터링하려면 대상을 추가합니다. 기본적으로 보고서는 자격 있는 모든 방문자의 결과를 표시합니다. 방문자의 보다 구체적인 하위 집합을 위해 결과를 필터링하려면 대상을 추가합니다.<br>**참고**: 다른 활동 유형과 달리, [!UICONTROL Automated Personalization] 을(를) 사용할 수 없음 [!UICONTROL Adobe Analytics] 를 보고 소스 (A4T) 로 사용하십시오. |
   | [!UICONTROL 참고] | 본인 또는 다른 팀 구성원이 쉽게 사용할 수 있도록 본인의 활동에 대한 정보를 입력합니다. 다음 [!UICONTROL 메모] 창의 크기를 조정할 수 있습니다. |

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

을(를) 클릭한 후 **[!UICONTROL 저장 및 닫기]**, 활동의 [!UICONTROL 개요] 페이지가 표시됩니다. 클릭 **경험 미리보기** 을 클릭하여 경험이 전달될 때 어떻게 표시되는지 미리 볼 수 있습니다. 를 사용하여 사이트에서 AP 경험에 대한 링크를 보고 공유하여 의 외부에 있는 경험에 대한 &quot;진정한 미리보기&quot;를 얻을 수 있는 팝업이 나타납니다 [!UICONTROL Target]의 VEC(시각적 경험 작성기)입니다. 미리 보기를 공유하려면 메시지에서 링크를 공유해야 합니다. 링크를 클릭한 다음 브라우저에서 직접 URL을 복사할 수는 없습니다. 링크를 복사하면 메시지의 링크에서 페이지에 액세스할 때만 페이지가 올바르게 표시되는 매개 변수가 URL에 포함됩니다.

보고에 대한 자세한 내용은 [Automated Personalization 보고서](/help/main/c-reports/personalization-reports/reports-ap.md).
