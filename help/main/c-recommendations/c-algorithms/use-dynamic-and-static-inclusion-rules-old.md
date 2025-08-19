---
keywords: 포함 규칙;포함 기준;권장 사항;새 기준 만들기;프로모션;판촉;동적 필터링;동적;비어 있는 값;필터링 규칙 무시;정적 필터;값으로 필터링;엔티티 속성 일치;프로필 속성 일치;매개 변수 일치;값으로 필터링 정적 필터
description: Adobe [!DNL Target] 기준 및 프로모션에 대한 권장 사항에서 포함 규칙을 만드는 방법을 알아봅니다. 더 나은 결과를 얻으려면 동적 또는 정적 필터링 규칙을 더 추가합니다.
title: Recommendations에서 동적 및 정적 포함 규칙을 사용하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '2013'
ht-degree: 16%

---

# 동적 및 정적 포함 규칙 사용

[!DNL Adobe Target]에서 기준 및 프로모션에 대한 포함 규칙을 만들고 동적 또는 정적 필터링 규칙을 추가하여 권장 사항에 대한 더 나은 결과를 얻는 방법에 대한 정보입니다.

기준 및 프로모션에 대한 포함 규칙을 만들고 사용하는 프로세스는 사용 사례 및 예와 비슷합니다. 기준 및 프로모션과 포함 규칙 사용 모두 이 섹션에서 다룹니다.

## 기준에 필터링 규칙 추가 {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

[기준을 만드는 중](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)에 **[!UICONTROL Add Filtering Rule]** 아래의 **[!UICONTROL Inclusion Rules]**&#x200B;을(를) 클릭합니다.

![inclusion_options_new image](assets/inclusion_options_new.png)

사용 가능한 선택 사항은 선택한 업계 카테고리와 권장 사항 키에 따라 다릅니다.

## 프로모션에 필터링 규칙 추가 {#section_D59AFB62E2EE423086281CF5D18B1076}

[프로모션을 만드는 중](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14)에 **[!UICONTROL Promote by Attribute]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Add Filtering Rule]**&#x200B;을(를) 클릭합니다.

![inclusion_options 이미지](assets/inclusion_options.png)

## 필터 유형 {#section_0125F1ED10A84C0EB45325122460EBCD}

다음 섹션에는 기준 및 프로모션에 대한 [!UICONTROL Dynamic Filtering] 및 [!UICONTROL Filter by Value]의 필터링 옵션 유형이 나와 있습니다.

### 동적 필터링

동적 포함 규칙은 정적 포함 규칙보다 강력하며 더 나은 결과와 참여를 제공합니다. 다음 사항을 고려하십시오.

* 동적 포함 규칙은 사용자의 프로필 매개 변수 또는 mbox 호출에서 속성을 일치시켜 권장 사항을 제공합니다.

  예를 들어 &quot;가장 빈도가 높은 기준&quot; 권장 사항을 만들 수 있습니다. 반환된 권장 사항 세트에서 사용자가 권장 사항이 표시된 페이지에 액세스할 때 전달된 속성에 대해 모든 권장 사항을 실시간으로 필터링할 수 있습니다.

* 정적 규칙을 사용하여 컬렉션 대신 권장 사항에 포함되는 항목을 제한합니다.

* 동적 포함 규칙을 필요한 만큼 만들 수 있습니다. 포함 규칙들은 AND 연산자로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

동적 필터링에 사용할 수 있는 옵션은 다음과 같습니다.

| 동적 필터링 옵션 | 세부 사항 |
| --- | --- |
| [엔티티 속성 일치](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | 잠재적 권장 사항 항목의 풀을 사용자가 상호 작용한 특정 항목과 비교하여 동적으로 필터링합니다.<br>방문자가 가장 좋아하는 브랜드와 같이 방문자에게 가장 인기 있는 권장 사항을 표시하려는 경우 [!UICONTROL Entity Attribute Matching]을(를) 사용합니다. |
| [프로필 속성 일치](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | 항목(엔티티)을 사용자 프로필에 있는 값과 비교하여 동적으로 필터링합니다.<br>크기 또는 즐겨찾기 브랜드와 같이 방문자의 프로필에 저장된 값과 일치하는 권장 사항을 표시하려면 [!UICONTROL Profile Attribute Matching]을(를) 사용합니다. |
| [매개 변수 일치](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | 항목(엔티티)을 요청(API 또는 mbox)에 있는 값과 비교하여 동적으로 필터링합니다.<br>페이지 매개 변수 또는 방문자의 매개 변수(예: 장치 차원 또는 지리적 위치)와 일치하는 콘텐츠를 추천하려면 [!UICONTROL Parameter Matching]을(를) 사용합니다. |

### 값으로 필터링

다음 옵션은 값으로 필터링할 수 있습니다.

| 값으로 필터링 옵션 | 세부 사항 |
| --- | --- |
| [정적 필터](/help/main/c-recommendations/c-algorithms/static-value.md) | 필터링할 하나 이상의 정적 값을 수동으로 입력합니다. |

## 사용 가능한 연산자 {#operators}

동적 기준 및 프로모션은 정적 기준 및 프로모션보다 훨씬 강력하며 더 나은 결과와 참여를 제공합니다.

다음 예는 마케팅 활동에서 동적 프로모션 및 제외를 사용하는 방법에 대한 일반적인 아이디어를 제공합니다.

| 연산자 | 예 |
| --- | --- |
| Equals<br>(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능) | 동적 프로모션에서 &quot;equals&quot;(다음과 같음) 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음 방법으로 다른 항목을 프로모션할 수 있습니다.<ul><li>동일 브랜드</li><li>동일한 범주</li><li>하우스 브랜드의 동일한 카테고리 및 AND</li><li>동일한 스토어</li></ul> |
| 같지 않음<br>(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능) | 동적 프로모션에서 &quot;does not equal&quot;(다음과 같지 않음) 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음 방법으로 다른 항목을 프로모션할 수 있습니다.<ul><li>다른 TV 시리즈</li><li>다른 장르</li><li>다른 제품 시리즈</li><li>다른 스타일 ID</li></ul> |
| 하위 문자열 <br>이(가) 없습니다. 엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용할 수 있습니다. | &quot;하위 문자열을 포함하지 않음&quot; 연산자를 사용하여 방문자가 웹 사이트에서 항목을 보고 있으면(제품 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>제목에 욕설이 포함되어 있지 않음</li></ul> |
| 다음으로 시작 <br>(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능) | 다음으로 시작 연산자를 사용하면 방문자가 웹 사이트에서 항목을 보고 있을 때(제품 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>iPhone으로 시작하는 제품 이름</li></ul> |
| 다음으로 끝남<br>(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능) | &quot;다음으로 끝남&quot; 연산자를 사용하면 방문자가 웹 사이트에서 항목을 보고 있을 때(제품 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>콘텐츠는 영어를 나타내는 EN으로 끝납니다.</li></ul> |
| 이(가) <br>보다 크거나 같습니다(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능). | &quot;다음보다 크거나 같음&quot; 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>가격은 같거나 더 비쌉니다</li></ul> |
| <br>보다 작거나 같음(엔터티 특성 일치, 프로필 특성 일치, 매개 변수 일치 및 정적 필터에서 사용 가능) | &quot;다음보다 작거나 같음&quot; 연산자를 사용하는 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>비용은 동일하거나 더 저렴함</li><li>비용이 덜 드는 항목 제외</li></ul> |
| <br> 사이입니다(엔터티 특성 일치, 프로필 특성 일치 및 매개 변수 일치에서 사용 가능). | 동적 프로모션에서 &quot;is between&quot;(다음 사이) 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>더 비싼 가격</li><li>저렴한 가격</li><li>비용 더하기 또는 빼기 30%</li><li>같은 계절의 나중 에피소드</li><li>연속되는 선행 저서</li></ul> |
| <br> 목록에 포함되어 있습니다(프로필 특성 일치 및 매개 변수 일치에서 사용 가능). | 프로필 속성 일치에서 &quot;목록에 포함됨&quot; 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>방문자의 지리적 위치에 사용 가능</li></ul>**예**: 방문자의 지리적 영역에서 사용할 수 있는 항목만 추천합니다.<br>필터 규칙이 다음과 같이 표시될 수 있습니다.<br>`availableGeographies list contains an item in user.currentGeography`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [오른쪽](#caveats)에 목록이 필요합니다. |
| <br> 목록에 포함되어 있지 않습니다(프로필 특성 일치 및 매개 변수 일치에서 사용 가능). | 프로필 속성 일치에서 &quot;목록에 없음&quot; 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음과 같은 다른 항목을 제외할 수 있습니다.<ul><li>방문자가 본 마지막 10개 항목 목록</li></ul></ul>**예**: 방문자가 최근에 보고 관심이 없는 항목을 프로모션하지 않습니다.<br>필터링 규칙이 다음과 같이 표시될 수 있습니다.<br>`id is not contained in list user.lastViewedItems`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [오른쪽](#caveats)에 목록이 필요합니다. |
| 목록에 <br>의 항목이 포함되어 있습니다(엔터티 특성 일치, 프로필 특성 일치 및 매개 변수 일치에서 사용 가능). | 프로필 속성 일치에서 &quot;list contains a item in&quot; 연산자를 사용하면 방문자가 웹 사이트에서 항목을 보고 있을 때(예: 스포츠 이벤트 또는 콘서트) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>방문자가 좋아하는 팀 중 하나와 연결됨</li></ul>**예**: 방문자가 좋아하는 팀 중 하나와 연결된 게임을 추천하려고 합니다.<br>필터링 규칙이 다음과 같이 표시될 수 있습니다.<br>` teamsPlaying list contains an item in user.favoriteTeams`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [양면](#caveats)에 목록이 필요합니다. |
| 목록에 <br>의 항목이 없습니다(엔터티 특성 일치, 프로필 특성 일치 및 매개 변수 일치에 사용 가능). | 매개 변수 속성 일치에서 &quot;list does not contain a item in&quot; 연산자를 사용할 경우, 방문자가 웹 사이트에서 항목을 보고 있으면(제품, 문서 또는 동영상 등) 다음과 같은 다른 항목을 제외할 수 있습니다.<ul><li>금지된 유형 목록에 포함됨</li></ul>**예**: 담배, 술과 같이 성인 방문자가 사용할 수 있는 항목을 제외하려는 경우<br>필터링 규칙이 다음과 같이 표시될 수 있습니다.<br>`itemType is not contained in list mbox.prohibitedTypes`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [양면](#caveats)에 목록이 필요합니다. |
| 목록에 <br>의 모든 항목이 포함되어 있습니다. 엔터티 특성 일치, 프로필 특성 일치 및 매개 변수 일치와 함께 사용할 수 있습니다. | 프로필 속성 일치에서 &quot;list contains all items in&quot; 연산자를 사용하면 방문자가 웹 사이트에서 항목을 보고 있을 때(예: Job 게시 또는 레서피) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>스킬 세트 포함</li><li>필수 구성 요소 세트 포함</li></ul>**예 1**: 방문자에게 스킬 집합(Java, C++ 및 HTML)이 있다고 가정합니다. 카탈로그의 항목은 필요한 기술(Java 및 HTML)이 있는 작업입니다. 방문자에게 작업을 추천하기 전에 방문자의 프로필에 필요한 모든 기술이 포함되어 있는지 확인해야 합니다.<br>필터링 규칙이 다음과 같을 수 있습니다.<br>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<br>**예 2**: 사용자에게 식료품 재료 목록이 있다고 가정합니다. 그 요리법에는 필요한 재료들의 목록이 있다. 방문자에게 레시피를 추천하기 전에 방문자 프로필에 필요한 모든 재료가 포함되어 있는지 확인해야 합니다.<br>필터링 규칙이 다음과 같이 표시될 수 있습니다.<br>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [양면](#caveats)에 목록이 필요합니다. |
| 목록에 <br>의 모든 항목이 포함되어 있지 않습니다(엔터티 특성 일치, 프로필 특성 일치 및 매개 변수 일치에서 사용 가능). | 엔티티 속성 일치에서 &quot;list does not contain all items in&quot; 연산자를 사용하면 방문자가 웹 사이트에서 항목을 보고 있을 때(예: 스포츠 이벤트 또는 콘서트) 다음과 같은 다른 항목을 프로모션할 수 있습니다.<ul><li>팀 집합을 포함하지 않음</li></ul>**예**: 스포츠 이벤트에 두 팀이 포함되어 있다고 가정합니다. 방문자의 프로필은 이 방문자가 이러한 팀에 대한 게임을 보고 싶어하지 않음을 나타냅니다. 이러한 팀이 플레이하는 경우 게임을 추천하지 않도록 해야 합니다.<br>필터링 규칙이 다음과 같이 표시될 수 있습니다.<br>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<br>**참고**: 이 연산자를 사용할 때는 규칙의 [양면](#caveats)에 목록이 필요합니다. |

## 엔티티 속성 일치, 프로필 속성 일치 및 매개 변수 일치로 필터링할 때 빈 값 처리 {#section_7D30E04116DB47BEA6FF840A3424A4C8}

종료 기준 및 프로모션을 위해 [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching] 기준으로 필터링할 때 빈 값을 처리하는 여러 옵션을 선택할 수 있습니다.

이전에는 값이 비어 있으면 결과가 반환되지 않았습니다. &quot;*x*&#x200B;이(가) 비어 있는 경우&quot; 드롭다운 목록에서는 다음 그림과 같이 기준에 빈 값이 있을 경우 수행할 적절한 작업을 선택할 수 있습니다.

![empty_value 이미지](assets/empty_value.png)

원하는 작업을 선택하려면 톱니바퀴 아이콘(![icon_gear 이미지](assets/icon_gear.png))을 마우스로 가리킨 다음, 원하는 작업을 선택하십시오.

| 액션 | 사용 가능한 경우 | 세부 사항 |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching] | 이 작업은 [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching]의 기본값입니다.<br>이 선택 사항은 규칙이 무시되도록 지정합니다. 예를 들어 세 개의 필터링 규칙이 있고 세 번째 규칙이 어떤 값도 전달하지 않는 경우, 결과를 반환하는 대신 빈 값으로 세 번째 규칙을 무시할 수 있습니다. |
| [!UICONTROL Do not show any results for this criteria]<br>(기준만) | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching] | 이 작업은 [!UICONTROL Entity Attribute Matching]의 기본값입니다.<br>이 작업은 이 옵션을 추가하기 전에 [!DNL Target]이 빈 값을 처리한 방식입니다. 이 기준에 대한 결과는 표시되지 않습니다. |
| [!UICONTROL Do not promote any items<br>(프로모션만 해당)] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching] | 이 작업은 [!UICONTROL Entity Attribute Matching]의 기본값입니다.<br>이 작업은 이 옵션을 추가하기 전에 [!DNL Target]이 빈 값을 처리한 방식입니다. 이 기준에 대한 결과는 표시되지 않습니다. |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] 및 [!UICONTROL Parameter Matching] | 값이 비어 있으면 정적 값을 사용하도록 선택할 수 있습니다. |

## 주의 사항 {#caveats}

>[!IMPORTANT]
>
>&quot;equals&quot;(다음과 같음)와 &quot;does not equal&quot;(다음과 같지 않음) 연산자를 사용하는 런타임 동안 서로 다른 데이터 유형 속성이 동적 기준이나 프로모션에서 호환되지 않을 수 있습니다. 왼쪽에 사전 정의된 특성 또는 사용자 지정 특성이 있는 경우 오른쪽에서 [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] 및 [!UICONTROL Environment] 값을 현명하게 사용하십시오.

![left_right 이미지](assets/left_right.png)

다음 표는 유효 규칙과 런타임 중에 호환되지 않을 수 있는 규칙을 보여줍니다.

| 호환 규칙 | 잠재적으로 호환되지 않는 규칙 |
|--- |--- |
| 값 - 다음 사이 - 현재 항목의 90%와 110% - salesValue | salesValue - 다음 사이 - 현재 항목의 90%와 110% - 값 |
| 값 - 다음 사이 - 현재 항목의 90%와 110% - 값 | clearancePrice - 다음 사이 - 현재 항목의 90%와 110% - 순익 |
| 순익 - 다음 사이 - 현재 항목의 90%와 110% - 순익 | storeInventory - 다음과 같음 - 현재 항목 - 재고 |
| 재고 - 다음과 같음 - 현재 항목 - 재고 |  |
