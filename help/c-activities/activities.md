---
keywords: 활동 목록;활동;활동;활동 유형;편집 활동;활동 작업;활동 특성;활동 목록 필터;활동 제한;개인화;activities list;activities;activity limitations;personalization;personalization
description: Adobe [!DNL Target] 에서 특정 대상에 맞게 컨텐츠를 개인화하고 페이지 디자인을 테스트하는 방법을 알아봅니다.
title: Target을 사용하여 컨텐츠를 개인화하고 페이지 디자인을 테스트하려면 어떻게 해야 합니까?
feature: 활동
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '2099'
ht-degree: 91%

---

# 활동

[!DNL Adobe Target]의 활동을 사용하면 특정 대상에 맞게 컨텐츠를 개인화하고 페이지 디자인을 테스트할 수 있습니다.

예를 들어 여성의 여름 신발에 대한 정보를 강조 표시하는 페이지와 보다 일반적인 여름 의류를 강조 표시하는 랜딩 페이지 등 두 개의 다른 랜딩 페이지를 테스트하는 활동을 디자인할 수 있습니다. 활동은 이러한 각 랜딩 페이지가 표시되는 시기를 제어하는 조건과 보다 성공적인 페이지를 확인하는 지표를 결정합니다. 특정 날짜 사이 등의 특정 조건이 충족될 때 시작되고 종료되거나 활동이 승인될 때 시작되고 비활성화될 때 종료되도록 활동이 구성됩니다.

활동을 디자인할 때는 신중하게 계획해야 합니다. 활동이 시작되는 시기와 지속되는 기간을 결정하십시오. 그런 후에 오퍼를 표시하고 각 오퍼에 대상을 할당합니다.

## 활동 유형

Target에는 여러 가지 활동 유형이 포함됩니다. 다음 표는 자세한 내용을 알 수 있는 링크와 함께 각 활동 유형에 대한 개요를 제공합니다. 목적에 가장 적합한 활동 유형을 선택하는 데 도움이 되도록 [Adobe Target 활동 안내서](/help/c-activities/target-activities-guide.md)를 만들었습니다.

| 활동 유형 | 설명 |
|--- |--- |
| [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) | A/B 테스트에서는 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사전 지정된 테스트 기간에 전환율이 가장 많이 향상된 버전을 확인합니다.<br>**참고:** 이제 [A/B 테스트 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 자동 할당은 둘 이상의 경험에서 승자를 식별하고, 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다.<br>**참고:** 이제 [자동 지정 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | 자동 타겟은 콘텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 식별하고, 개별 고객 프로필과, 이 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 잘 맞춤 설정된 경험을 제공합니다.<br>**참고:** 이제 [자동 타겟 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [Analytics 데이터 사용](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md)(A4T) | [!DNL Adobe Analytics]를 보고 소스로 사용하도록 활동을 구성할 수 있습니다. 이 활동 유형을 사용하려면 [!DNL Adobe Experience Cloud] 계정을 [!DNL Analytics]와 [!DNL Target] 모두에 연결해야 합니다. |
| [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | 다변량 테스트(MVT)는 페이지의 요소에 있는 오퍼 조합을 비교하여 특정 대상에 대해 성과가 가장 좋은 조합을 판별하고 활동의 성공에 영향을 가장 많이 주는 요소를 식별합니다. |
| [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md) | 경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.<br>**참고:** 이제 [경험 타깃팅 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/assets/premium.png) | 자동화된 개인화(AP)는 콘텐츠를 개인화하고 전환을 유도하기 위해, 오퍼나 메시지를 결합하고 고급 기계 학습을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 변형을 각 방문자와 연결합니다. |
| [Recommendations](/help/c-recommendations/recommendations.md)<br>![Target Premium](/help/assets/premium.png) | 권장 사항은 사이트에서의 사용자 활동에 따라 웹 사이트 사용자에게 제품을 제안하는 방법을 결정합니다.<br>예를 들어, 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 하려는 경우, &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여주는 권장 사항을 생성할 수 있습니다. 또는 &quot;이 항목을 보고 다른 항목도 본 사람&quot; 알고리즘을 사용하여 방문자에게 보고 있는 것과 유사한 비디오를 추천하여 미디어 사이트에서 더 많은 시간을 소비하도록 할 수도 있습니다.<br>**참고:** 이제 A/B 테스트(자동 할당 및 자동 타겟 포함)와 경험 타깃팅(XT) 활동 내에 권장 사항을 포함할 수 있습니다. [오퍼로서의 Recommendations](/help/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오. |

## 활동 목록 {#section_DE8E2DB30D534962A931EF8BB48240F5}

[!UICONTROL 활동] 목록은 [!DNL Target]을 열 때의 기본 보기입니다. 이 페이지에서 새 활동을 만들고 기존 활동을 관리할 수 있습니다.

[!DNL Target] UI 상단에 있는 [!UICONTROL 활동] 탭을 클릭하여 [!UICONTROL 활동] 목록을 표시할 수도 있습니다.

![활동 목록](/help/c-activities/assets/activities-list.png)

활동 목록에서는 모든 활동을 개괄적으로 볼 수 있습니다:

| 요소 | 설명 |
|--- |--- |
| 유형 | A/B나 MVT와 같은 활동 유형. |
| 이름 | 활동의 이름. |
| URL | URL은 이름 아래에 더 밝은 텍스트로 표시됩니다.<br>활동용 URL은 활동이 표시되는 위치를 나타냅니다. 이 URL을 사용하면 활동을 빠르게 식별하고 특정 페이지에서 이미 테스트가 실행 중인지 여부를 판별하는 데 도움이 됩니다.<br>테스트가 여러 URL에서 실행되는 경우에는 링크에 추가로 사용된 URL의 수가 표시됩니다. 해당 활동에 대한 전체 URL 목록을 보려면 링크를 클릭하십시오.<br>URL을 기준으로 검색할 수 있습니다. 검색 상자 옆에 있는 드롭다운 목록을 사용하고 [!UICONTROL 검색 URL]을 선택하십시오. |
| 상태 | 활동의 상태는 다음 중 하나일 수 있습니다.<ul><li>**라이브**: 활동이 현재 실행 중입니다.</li><li>**초안**: 활동 설정이 시작되었지만 아직 활동을 실행할 준비가 되지 않았습니다.</li><li>**예약됨**: 지정된 시작 날짜 및 시간에 도달하면 활동이 활성화되도록 준비되었습니다.</li><li>**비활성**: 활동이 일시 정지되었거나 비활성화되었습니다.</li><li>**동기화 중**: 활동이 저장되었으며 Target 배달 네트워크에 동기화되고 있습니다.</li><li>**종료**: 활동의 지정한 종료 날짜 및 시간이 완료되어 활동이 더 이상 지원되지 않습니다.</li><li>**보관됨**: 활동이 보관되었습니다. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.</li></ul>**참고**: API 방법을 사용하여 UI 외부에서의 활동 활성화와 같은 특정 작업을 수행하면 업데이트가 UI로 전파되는 데 최대 10분이 걸릴 수 있습니다. |
| 소스 | 활동이 만들어진 위치를 보여줍니다.<ul><li>Adobe Target</li><li>Adobe Target Classic</li><li>AEM(Adobe Experience Manager)</li><li>AMS(Adobe Mobile Services)</li></ul> |
| 장치 내 의사 결정 자격 조건 | 장치 내 의사 결정 자격 조건을 갖춘 활동을 만든 후, 활동의 개요 페이지에 장치 내 의사 결정 자격 조건을 나타내는 레이블이 표시됩니다.<br>이 레이블은 활동이 항상 장치 내 결정을 통해 전달된다는 것을 의미하지 않습니다. at.js 2.5.0+이 장치 내 의사 결정을 사용하도록 구성된 경우에만 이 활동이 장치에서 실행됩니다. at.js 2.5.0+이 온디바이스를 사용하도록 구성되어 있지 않은 경우, 이 활동은 at.js에서 만들어진 서버 호출을 통해 여전히 전달됩니다.<br>장치  [내 의사 결정을 참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md). |
| 속성 | 활동에 대한 [속성](/help/administrating-target/c-user-management/property-channel/property-channel.md)을 표시합니다. |
| 수입의 예상 상승도 | 대상의 100%에게 가장 성과가 좋은 경험이 표시되는 경우 수입의 예상되는 증가를 보여줍니다.<br>다음 공식을 사용하여 계산됩니다.<br>`(<winning experience> - <control experience>)*<total number of visitors>`<br>이 숫자는 압축 양식에서 소수 앞에 한 자릿수만 있으면 최대 소수 첫째 자리로 반올림됩니다. 예를 들어 $1.6M, $60K, $900, $8.5K, $205K와 같습니다.<br>승자를 확정하기에 충분한 데이터가 없거나 예상 비용이 없는 활동의 경우 이 열에 &quot;---&quot;이 표시됩니다.<br>자세한 내용은 [매출 상승도 평가](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오. |
| 마지막 업데이트 날짜 | 활동이 마지막으로 업데이트된 날짜와 업데이트한 사람. |

사용 가능한 작업을 보려면 마우스를 활동 위에 놓으십시오.

![활동 목록 가리키기 작업](/help/c-activities/assets/activities_list_hover.png)

권한에 따라 다음 작업을 사용할 수 있습니다.

| 작업 | 설명 |
| --- | --- |
| 편집 | 활동을 변경합니다. 모든 활동은 편집할 수 있습니다.<br>활동을 편집할 수 있는 다양한 방법에 대해서는 [활동 편집 또는 초안으로 저장](/help/c-activities/edit-activity.md)을 참조하십시오. |
| 비활성화 | 라이브 또는 예약된 활동을 중지합니다. 비활성화된 캠페인은 다시 활성화하거나 보관할 수 있습니다.<br>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| 활성화 | 비활성 상태 또는 준비된 활동을 시작합니다. |
| 보관 | 활동을 보관 파일에 보냅니다. 기본적으로 보관된 활동은 더 이상 활동 목록에 표시되지 않습니다. 보관된 활동을 보려면 이러한 활동을 포함하도록 활동 목록에 대한 필터를 변경하십시오. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.<br>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| 복사 | 활동을 복사합니다. 모든 활동은 복사할 수 있습니다. 활동을 복사하면 동일한 이름에 &quot;사본&quot;이 추가된 채 새 활동이 만들어집니다. 예를 들어, &quot;브라우저 오퍼&quot;라는 테스트는 &quot;브라우저 오퍼 사본&quot;으로 복사됩니다.<br>시각적 오퍼는 활동과 함께 복사됩니다. 원래 활동에 영향을 주지 않고 사본에서 오퍼를 안전하게 편집할 수 있습니다. 유일한 예외는 콘텐츠/자산 폴더에 있는 저장된 오퍼와 이미지입니다. |
| 삭제 | 초안이나 활동을 삭제합니다.<BR>**참고**:삭제된 활동은 복구할 수 없습니다. 이 활동이 다시 필요하지 않은지 확신할 수 없는 경우 [!UICONTROL 보관] 작업을 사용하십시오. 필요한 경우 활동을 다시 활성화할 수 있습니다. |

활동 목록에 대한 다음 세부 사항을 참고하십시오.

* 보관된 활동과 종료된 활동은 [!UICONTROL 활동] 목록에 표시되지 않습니다. 이러한 활동을 보려면 왼쪽 레일의 고급 필터 설정을 사용하여 필터링하십시오.
* 원래 [!DNL Target Classic]에서 만들어진 활동은 비활성화되거나 삭제되는 즉시 [!DNL Target Standard/Premium]에서 삭제됩니다. 원래 [!DNL Target Classic]에서 만들어진 삭제된 작업은 [!DNL Target Standard/Premium]의 [!UICONTROL 보관] 폴더로 보내지지 않습니다. 보관된 폴더 기능은 [!DNL Target Standard/Premium]에서 만들어진 활동에만 적용됩니다.
* [!UICONTROL 자동화된 개인화] (AP), [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 이외의 모든 활동 유형에서는 [!DNL Target] 또는 [!DNL Adobe Analytics]를 데이터 소스로 사용하도록 선택할 수 있습니다. [!UICONTROL AP], [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟]은 *항상* [!DNL Target] 데이터를 사용합니다.
* 활동은 몇 가지 채널에서 사용할 수 있습니다.

   * 웹 및 모바일 사이트
   * 키오스크 및 ATM을 포함하는 인터넷이 연결된 스크린 및 장치
   * 이메일 및 기타 획득 채널 또는 파트너 사이트
   * 모바일 앱
   * 태그된 콘텐츠를 제공할 수 있는 그 밖의 모든 곳

## 활동 목록 정렬 및 필터링 {#section_41DAD479FFF740E2BB67BF4825955670}

기본적으로 목록은 활동을 마지막 수정 날짜별로 정렬되며, 최근에 수정한 항목이 맨 위에 표시됩니다. 그러나 보고 싶은 활동을 표시하도록 목록을 사용자 지정하는 데 도움이 되는 몇 가지 필터링 선택 사항이 있습니다.

### 검색 {#search-heading}

검색 기준과 일치하는 활동을 검색하려면 검색 필드를 사용하십시오.

![활동 검색](/help/c-activities/assets/activities_search_new.png)

검색 필드에는 [!UICONTROL 활동 이름] 및 [!UICONTROL URL] 검색 필터 중 하나를 지정하여 검색 범위를 좁히는 데 도움이 되는 드롭다운 메뉴가 포함되어 있습니다.

### 활동 목록 필터

목록 필터를 선택하여 활동 목록에 나타나는 활동을 결정할 수 있습니다.

![유형별 활동 필터링](/help/c-activities/assets/activities_filters_new.png)

다음 선택 사항에 따라 필터링할 수 있습니다. 각 카테고리에서 아무것도 선택하지 않을 경우 기본값은 모두입니다.

| 필터 카테고리 | 필터 |
|--- |--- |
| 유형 | A/B 테스트: [수동](/help/c-activities/t-test-ab/test-ab.md), [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 및 [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md).<br>[자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>[경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md)<br>[다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md)<br>[Recommendations](/help/c-recommendations/recommendations.md) |
| 상태 | 라이브<br>초안<br>예약됨<br>비활성<br>동기화 중<br>종료<br>보관됨 |
| 장치 내 의사 결정 자격 조건 | 예<br>아니요 |
| 보고 소스 | Target<br>Analytics |
| 경험 작성기 | 시각적<br>양식 기반 |
| 지표 유형 | 변환<br>수입<br>참여 |
| 활동 소스 | Adobe Target<br>Adobe Target Classic<br>Adobe Experience Manager<br>Adobe Mobile Services |

### 활동 속성별 정렬

선택한 열 제목에 따라 활동을 오름차순으로 나열하는 방식과 내림차순으로 나열하는 방식 간을 전환하려면 다음 열 제목 중 하나를 클릭하십시오.

* 유형
* 이름

![활동 목록 오름차순](/help/c-activities/assets/activities_list_ascending.png)

![오늘의 팁 비활성화](/help/c-activities/assets/tip-disable-new.png)

## 제한 {#section_049D4684403A4E07B998067EB8E9BE56}

각 Target 활동에는 다음의 콘텐츠 제한 사항이 있습니다.

| 항목 |  제한 |
|--- |--- |
| 고유 선택기 | 300  선택기가 다른 경험에서 반복되는 경우 한 번만 카운트됩니다. 그러나 동일한 경험에서 반복되는 경우에는 다시 카운트됩니다. |
| 각 경험의 오퍼 | 350 |
| 지표에 있는 클릭 추적 선택기 | 50 |
| 지표의 mbox | 50 |
| 대상 및 위치 | 50 대상 및 위치(mbox) 조합은 50 이하라야 합니다. |

이러한 제한을 초과하는 경우 활동을 저장할 수 없습니다.

활동에서 이러한 항목들의 수를 늘리면 Target에서 활동을 동기화하는 하는 데 걸리는 시간이 길어집니다.

시각적 경험 작성기의 추가적인 제한에 대해서는 [시각적 경험 작성기 제한 사항](/help/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721)을 참조하십시오.

## [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44} 외부에서 업데이트된 활동에 대해 [!DNL Target]으로 가져온 특성

[!DNL Target]에서 만든 활동이 [!DNL Target]의 외부에서(예를 들어, Adobe I/O를 통해) 업데이트된 경우 다음 활동 속성을 다시 [!DNL Target]으로 가져오게 됩니다.

`thirdpartyId`

`startDate`

`endDate`

`status`

`priority`

`marketingCloudMetadata(remoteModifiedBy)`

이 가져오기 작업은 활동 페이지가 열리면 실행되고, 최대 지연 시간은 10분입니다. (KB-1526)

## 교육 비디오 {#section_BE80D13A2E81460C885F902010E1AD87}

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 활동 유형(9:03)  ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### 활동 관리(5:55) ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 활동 목록을 사용하여 활동을 관리하는 방법에 대해 설명합니다.

* *활동*&#x200B;이라는 용어 정의
* 활동 목록에서 활동 찾기
* 활동 편집, 비활성화, 복사 및 삭제

>[!VIDEO](https://video.tv.adobe.com/v/18550)
