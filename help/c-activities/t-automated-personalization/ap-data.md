---
description: Adobe Target는 자동으로 다양한 데이터를 수집 및 사용하여 자동화된 개인화 (AP) 및 자동 타겟 (AT) 활동에 개인화 알고리즘을 구축합니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
keywords: 환경 데이터; 세션 데이터; 지역 데이터; 지리적 데이터; 장치 데이터; 모바일 데이터; 속성; 프로필 속성
seo-description: Adobe Target는 자동으로 다양한 데이터를 수집 및 사용하여 자동화된 개인화 (AP) 및 자동 타겟 (AT) 활동에 개인화 알고리즘을 구축합니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
seo-title: Adobe Target의 개인화 알고리즘에 대한 데이터 수집
solution: Target
title: Target의 개인화 알고리즘에 대한 데이터 수집
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 156587a0375fe2dbf8c461e310b2eae04b491b57

---


# ![PREMIUM](/help/assets/premium.png) Target의 개인화 알고리즘을 위한 데이터 수집{#data-collection-for-the-target-personalization-algorithms}

Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.

Target 개인화 알고리즘에 대한 자세한 내용은 [Random Forest 알고리즘](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA)을 참조하십시오.

The following table shows the data collected by Automated Personalization and Auto-Target by default, without the marketer having to do anything, as well as the naming convention used to indicate these attributes in [Personalization Insights Reports](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). 언제든지 입력 데이터 세트를 늘릴 수 있습니다. 추가 데이터를 업로드하는 방법에 대한 자세한 내용은 [Target의 개인화 알고리즘을 위한 데이터 업로드](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)를 참조하십시오.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 | 예제 속성 |
| --- | --- | --- | --- |
| [장치 및 모바일 데이터](#device-mobile) | 장치 및 모바일 전용 정보입니다.<br>아래의 "장치 및 모바일 데이터" 를 참조하십시오. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Mobile Device OS<br>Mobile Screen Size |
| [환경 데이터](#env) | 방문자의 운영 체제와 방문자가 활동에 액세스하는 방법과 시기에 대한 정보입니다. | `Browser - / Operating System] - [Attribute Name]` | 브라우저 - 유형 |
| Experience Cloud 세그먼트 | Audience Manager 또는 Analytics에서 제작하여 Experience Cloud에서 공유한 고객 | `Custom - Experience Cloud Audience - [Audience Name]` | 사용자 지정 데이터 |
| [지리적 데이터](#geo) | 방문자가 있는 위치에 대한 정보입니다.<br>아래의 "지리 데이터" 를 참조하십시오. | `Geo - [geo attribute]` | City<br>Country<br>Region/State<br>Zip Code<br>Latitude<br>Longitude<br>ISP or Mobile Carrier |
| 프로필 속성 | 업데이트 API를 통해 Target 프로필에 직접 업로드된 프로필 스크립트 또는 속성 | `Custom - Visitor Profile - [attribute name]` | 사용자 지정 데이터 |
| 참조 URL 매개 변수 | 일반적으로 참조 URL은 mbox 호출을 시작한 특정 페이지를 참조하는 URL입니다.<br>이 변수는 사이트의 사용자 활동뿐만 아니라 사이트의 기술 구현에 의해서도 영향을 받을 수 있습니다. | `Custom - [Referring URL Parameter] - [Parameter value]` | 사용자 지정 데이터 |
| 보고 세그먼트 | 활동 설정에서 설정된 모든 세그먼트. | `Reporting Segment -[Segment Name]` | 사용자 지정 데이터 |
| [세션 데이터](#session) | 활동에 액세스할 때 세션에서 방문자의 행동에 대한 정보입니다. | `Visitor Profile - [Attribute Name]` | 방문자 프로필 - 최근 방문 시작일 |
| URL 매개 변수 | Target에서는 URL 매개 변수를 추출할 URL을 검사합니다. | `Custom - URL Parameter - [URL Parameter]` | 사용자 지정 데이터 |

다음 섹션에는 속성 이름, 설명 및 샘플 값을 비롯한 다양한 데이터 유형에 대한 자세한 정보가 들어 있습니다.

## Device and Mobile data {#device-mobile}

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 모바일 - 장치 - 브랜드 | 활동에 액세스하기 위해 사용한 모바일 장치의 브랜드. | Apple |
| 모바일 - 장치 - Ereader | 장치가 Ereader 인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 장치 - 게임 콘솔 | 장치가 게임 콘솔인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 장치 - 미디어 플레이어 | 장치가 미디어 플레이어인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 장치 - 휴대폰 | 장치가 휴대폰인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 장치 - 모델 이름 | 활동에 액세스하기 위해 사용한 방문자의 모델 이름입니다. | iPhone XS |
| 장치 - 셋톱 박스 | 장치가 셋톱 박스인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 장치 - 태블릿 | 장치가 태블릿인지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 픽셀 밀도 (ppi) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 픽셀 밀도입니다. | 1, 2, 3 등 |
| 모바일 - OS - OSX (Android, Windows 등) | 사용자가 OSX (또는 Android, Windows 등) 를 장치에 액세스하여 활동에 액세스합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 화면 높이 (px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 모바일 - 화면 너비 (px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 너비 (픽셀 단위) 입니다. | 1, 2, 3 등 |

## Environmental data {#env}

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 브라우저 - 요일 | 방문자가 활동에 액세스한 요일. | 0 - 6.<br>(0는 일요일임) |
| 브라우저 - 하루 중 시간 | 방문자가 활동에 액세스한 시간입니다. | 0 to 23<br>(0 is midnight) |
| 브라우저 - 주 중 시간 | 방문자가 활동에 액세스한 시간입니다. | 0 to 168<br>(Sunday midnight is 0) |
| 브라우저 - 언어 설정 | 활동에 액세스하는 데 사용된 방문자의 브라우저에 지정된 언어입니다. | English<br>German |
| 브라우저 - 화면 높이 (px) | 활동에 액세스하기 위해 사용된 방문자의 브라우저 화면 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 브라우저 - 하루 중 시간 | 방문자가 활동에 액세스한 브라우저의 시간입니다. | 0, 6, 12, 18<br>(0 is night, 6 is morning,<br>12 is afternoon, 18 is evening) |
| 브라우저 - 표준 시간대 | 활동에 액세스하는 동안 방문자의 시간대가 표시됩니다. | Pacific Time<br>Eastern Time<br>GMT |
| 브라우저 - 유형 | 방문자가 활동에 액세스하는 동안 사용한 브라우저의 유형입니다. | Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other |
| 브라우저 - 평일/주말 | 방문자가 활동에 액세스할 때의 작업 상태 (주말, 근무 시간 또는 평일 자유-시간). | Saturday and Sunday is weekend<br>Monday-Friday 0900 to 1800 is work time<br>Monday-Friday after 1800 until 0900 is weekday free time |
| 브라우저 - 창 높이 (px) | 활동에 액세스하기 위해 사용된 방문자의 창 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 브라우저 - 창 너비 (px) | 활동에 액세스하기 위해 사용된 방문자의 창 너비 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 장치 - 화면 높이 | 방문자가 활동에 액세스하는 데 사용한 장치의 화면 높이입니다. | 1, 2, 3 등 |
| 장치 - 화면 너비 | 활동에 액세스하기 위해 사용된 방문자의 화면 너비입니다. | 1, 2, 3 등 |
| 운영 체제 | 활동에 액세스하는 데 사용되는 방문자의 장치에 있는 운영 체제입니다. | Mac OS<br>Windows<br>Linux<br>Search Bot<br>Unknown OS |
| 운영 체제 - 버전 | 방문자가 활동에 액세스하는 데 사용한 운영 체제의 버전입니다. | Windows 10<br>Mac OS 10 |
| 트래픽 소스 - 참조 랜딩 페이지 URL | 사이트에 액세스할 때 방문자가 본 첫 번째 페이지입니다. | `https://www.adobe.com/ecloud.html` |

## Geographical data {#geo}

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 지역 - 구/군/시 | 방문자가 활동에 액세스한 도시. | San Francisco |
| 지역 - 국가 | 방문자가 활동에 액세스한 국가. | 독일 |
| 지역 - DMA | 방문자가 활동에 액세스한 DMA (Designated Marketing Area). | Charlottesville |
| 지역 - 위도 | 방문자가 활동에 액세스한 위도입니다. | 47.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| 지역 - 경도 | 방문자가 활동에 액세스한 경도입니다. | -122.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| 지역 - 주/지역 | 방문자가 활동에 액세스한 상태 또는 지역. | Utah<br>New South Wales |
| 지역 - 우편번호 | 방문자가 활동에 액세스한 우편 번호. | 84004 |
| 모바일 - 통신사 | 활동에 액세스할 때 방문자가 사용한 이동통신사. | Vodafone<br>T-Mobile |
| 네트워크 - 연결 속도 | 방문자가 활동에 액세스할 때의 장치 연결 속도입니다. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite |
| 네트워크 - 도메인 이름 | 방문자가 활동에 액세스한 네트워크 도메인의 이름. | `nnt.net` |
| 네트워크 - ISP | 방문자가 활동에 액세스한 네트워크입니다. | NNT Communications Corporation |

## Session data {#session}

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 방문자 프로필 - 활동 라이프타임 순서 값 | 모든 방문/세션에 걸친 모든 주문 값의 합을 특정 활동에 지정합니다. | 이중 |
| 방문자 프로필 - 사이트에서 활동 라이프타임 시간 | 방문자의 현재 세션을 제외하고 사이트에서 보낸 총 시간을 지정하고 세션이 만료되면 업데이트됩니다. | double, milliseconds |
| 방문자 프로필 - 활동 중 방문당 평균 페이지 보기 횟수 | 현재 세션을 제외하고 세션당 평균 페이지 보기 수를 지정합니다. | 이중 |
| 방문자 프로필 - 방문당 평균 시간 | 방문당 평균 체류 시간을 지정합니다. 현재 세션은 포함되지 않습니다. | double, milliseconds |
| 방문자 프로필 - 첫 번째 방문 | 사용자가 Target와 상호 작용한 첫 번째 방문의 시간을 지정합니다. | double, milliseconds |
| 방문자 프로필 - 마지막 방문 이후 시간 | 이 특정 활동에 대한 마지막 방문 이후 시간을 지정합니다. | 이중 (정수 양수만) 1, 2, 3 등 |
| 방문자 프로필 - 위치/컨텐츠의 노출 횟수 | 특정 활동에서 특정 위치/컨텐츠 조합에 대한 노출 횟수를 지정합니다. | 이중 (정수 양수만) 1, 2, 3 등 |
| 방문자 프로필 - 마지막 타겟 상호 작용 | Target와 마지막 상호 작용 시간을 지정합니다. 상호 작용은 Target의 현재 구현에서 각 요청 시 프로필을 업데이트하기 때문에 모든 mbox 요청에서 발생합니다. | double, milliseconds |
| 방문자 프로필 - 활동 전에 본 페이지 | 방문자가 활동에 들어올 때까지 현재 방문/세션을 포함한 총 페이지 보기 횟수 (노출 횟수) 를 지정합니다. | 이중 (정수 양수만) 1, 2, 3 등 |
| 방문자 프로필 - 현재 방문의 페이지 보기 | 방문자가 활동에 들어올 때까지 현재 방문/세션에 있는 페이지 보기 수를 지정합니다. 더 정확하게 노출 횟수 이러한 노출 횟수는 실제 페이지 뷰가 아니라 요청이 Target에 도달한 횟수입니다. Target는 시간 초과를 구별하거나 사용자가 컨텐츠를 받지 못하거나 보지 않은 다른 이유를 구별하지 못합니다. | double (정수 정수만) |
| 방문자 프로필 - 현재 방문 시작 | Target 이 시작된 현재 방문/세션이 시작된 시간을 지정합니다. Target의 방문은 활동을 입력하지 않고 시작할 수 있습니다. 모든 mbox에 대한 호출만 필요합니다. 방문자는 활동을 입력하고 스냅샷을 가져올 때까지 잠시 걸릴 수 있습니다. | double, milliseconds |
| 방문자 프로필 - 최근 방문 시작일 | Target 이 시작된 마지막 방문/세션이 시작된 시간을 지정합니다. 이 속성은 세션이 만료되면 업데이트됩니다.<br>방문자의 첫 번째 세션인 경우 `LAST_SESSION_START = 0.` | double, milliseconds |
| 방문자 프로필 - 처음 활동을 시작할 때 가장 최근 방문 이후 시간 | 이전 세션과 사용자가 활동에 참여하고 스냅숏이 수행되는 시간 사이의 지속 기간을 지정합니다. | double, milliseconds |
| 방문자 프로필 - 활동 입력 전 방문 시간 | Target와 마지막 상호 작용과 현재 방문이 시작된 시점 간의 차이를 지정합니다. 이 속성은 사용자가 활동에 진입하고 스냅숏이 수행될 때까지 방문/세션 지속 기간으로 간주될 수 있습니다.<br>세션 시작과 마지막 업데이트 시간이 동일한 mbox 호출에 의해 트리거되면 음수 값이 발생합니다. 음수 값은 0로 간주해야 합니다. | double, milliseconds |
| 방문자 프로필 - 총 방문 횟수 | 총 방문 수/세션 수를 지정합니다. 현재 방문/세션을 포함하지 않습니다. | 이중 (정수 양수만) 1, 2, 3 등 |
| 방문자 프로필 - 총 활동 방문 | 특정 활동에 대한 방문 횟수를 지정합니다. 이전 방문이 없는 경우 0를 반환합니다. | 이중 (정수 양수만) 1, 2, 3 등 |
| 방문자 프로필 - 전환을 사용한 활동에 대한 총 방문 수 | 방문 중에 전환이 하나 이상 있었던 경우 특정 활동에 대한 방문 횟수/세션을 지정합니다. | 이중 |
| 방문자 프로필 - 전환이 없는 활동에 대한 방문 | 특정 활동으로 전환이 없는 방문 횟수/세션 수. 이 값은 전환 후 0로 재설정되거나 전환이 발생하지 않는 경우 -1로 재설정됩니다. | 이중 (정수 양수만) 1, 2, 3 등 |
