---
description: Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
seo-description: Adobe Target는 자동으로 다양한 데이터를 수집 및 사용하여 자동화된 개인화 (AP) 및 자동 타겟 (AT) 활동에 개인화 알고리즘을 구축합니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
seo-title: Adobe Target의 개인화 알고리즘에 대한 데이터 수집
solution: Target
title: Target의 개인화 알고리즘에 대한 데이터 수집
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 59a838b5cca86c7f67fa62494dc30eb64a3e70c2

---


# ![PREMIUM](/help/assets/premium.png) Target의 개인화 알고리즘을 위한 데이터 수집{#data-collection-for-the-target-personalization-algorithms}

Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 &quot;교육 레코드&quot;(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.

Target 개인화 알고리즘에 대한 자세한 내용은 [Random Forest 알고리즘](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA)을 참조하십시오.

다음 표는 마케터가 작업을 수행하지 않고도 기본적으로 자동화된 개인화를 통해 수집된 데이터와, [개인화 통찰력 보고서](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)에서 이러한 속성을 표시하는 데 사용된 이름 지정 규칙을 보여 줍니다. 언제든지 입력 데이터 세트를 늘릴 수 있습니다. 추가 데이터를 업로드하는 방법에 대한 자세한 내용은 [Target의 개인화 알고리즘을 위한 데이터 업로드](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)를 참조하십시오.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 | 예제 속성 |
| --- | --- | --- | --- |
| URL 매개 변수 | Target에서는 URL 매개 변수를 추출할 URL을 검사합니다. | `Custom - URL Parameter - [URL Parameter]` | 사용자 지정 데이터 |
| URL 매개 변수 참조 | 일반적으로 참조 URL은 mbox 호출을 시작한 특정 페이지를 참조하는 URL입니다.<br>이 변수는 사이트의 사용자 활동뿐만 아니라 사이트의 기술 구현에 의해서도 영향을 받을 수 있습니다. | `Custom - [Referring URL Parameter] - [Parameter value]` | 사용자 지정 데이터 |
| 환경 및 세션 데이터 | 사용자가 활동에 액세스하는 방법 및 시기에 대한 정보입니다. | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | 방문자 프로필 - 가장 최근 방문의 시작<br>방문자 프로필 -총방문 횟수<br>방문자 프로필 - 방문당 평균 시간<br>브라우저 - 시간대<br>브라우저 - 요일<br>브라우저 - 언어 설정<br>브라우저 - 유형<br>운영 체제 - 버전 |
| Geography | 방문자가 있는 위치에 대한 정보입니다. | `Geo - [geo attribute]` | 구/군/시<br>국가<br>지역/주<br>우편 번호<br>위도<br>경도<br>ISP 또는 모바일 통신사 |
| 장치 및 모바일 데이터 | 장치 및 모바일 전용 정보입니다. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | 모바일 장치 OS<br>모바일 화면 크기 |

다음 섹션에는 속성 이름, 설명 및 샘플 값을 비롯한 다양한 데이터 유형에 대한 자세한 정보가 들어 있습니다.

일부 값은 가장 가까운 정수 또는 시간으로 반올림됩니다.

## 환경 및 세션 데이터

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 브라우저 - 요일 | 방문자가 활동에 액세스한 요일. | 0 - 6.<br>(0는 일요일임) |
| 브라우저 - 하루 중 시간 | 방문자가 활동에 액세스한 시간입니다. | 0 ~ 23 |
| 브라우저 - 주 중 시간 | 방문자가 활동에 액세스한 시간입니다. | 0 - 168<br>(일요일 자정은 0) |
| 브라우저 - 언어 설정 | 활동에 액세스하는 데 사용된 방문자의 브라우저에 지정된 언어입니다. | englishgerman<br> |
| 브라우저 - 화면 높이 (px) | 활동에 액세스하기 위해 사용된 방문자의 브라우저 화면 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 브라우저 - 하루 중 시간 | 방문자가 활동에 액세스한 브라우저의 시간입니다. | 0, 6, 12, 18<br>(0는 밤, 6는 아침, 12는 오후, 18는 저녁) |
| 브라우저 - 표준 시간대 | 활동에 액세스하는 동안 방문자의 시간대가 표시됩니다. | 태평양 표준시<br>표준시 TIMEGMT<br> |
| 브라우저 - 유형 | 방문자가 활동에 액세스하는 동안 사용한 브라우저의 유형입니다. | Chromefirefoxinternet<br><br>Explorer 10<br>safariother<br> |
| 브라우저 - 평일/주말 | 방문자가 활동에 액세스할 때의 작업 상태 (주말, 근무 시간 또는 평일 무료 시간) | Saturday and Sunday is Weekendmonday<br>through Friday 0900 ~ 1800 is work timemonday<br>is work timemonday until 1800 until 0900 is weekday free time |
| 브라우저 - 창 높이 (px) | 활동에 액세스하기 위해 사용된 방문자의 창 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 브라우저 - 창 너비 (px) | 활동에 액세스하기 위해 사용된 방문자의 창 너비 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 장치 - 화면 높이 | 방문자가 활동에 액세스하는 데 사용한 장치의 화면 높이입니다. | 1, 2, 3 등 |
| 장치 - 화면 너비 | 활동에 액세스하기 위해 사용된 방문자의 화면 너비입니다. | 1, 2, 3 등 |
| 모바일 &gt; 픽셀 밀도 (ppi) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 픽셀 밀도입니다. | 1, 2, 3 등 |
| 운영 체제 | 운영 체제에서 활동에 액세스하는 데 사용되는 방문자의 장치입니다. | Mac oswindows<br>10<br>linuxsearch<br>Botunknown<br>OS |
| 운영 체제 - 버전 | 방문자가 활동에 액세스하는 데 사용한 운영 체제의 버전입니다. | Windows 10<br>Mac OS 10 |
| 트래픽 소스 - 참조 랜딩 페이지 URL | 사이트에 액세스할 때 방문자가 본 첫 번째 페이지입니다. | `https://www.adobe.com/experience-cloud.html` |

## 지리 정보

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 지역 - 구/군/시 | 방문자가 활동에 액세스한 도시. | San Francisco |
| 지역 - 국가 | 방문자가 활동에 액세스한 국가. | 독일 |
| 지역 - DMA | 방문자가 활동에 액세스한 DMA (Designated Marketing Area). | Charlottesville |
| 지역 - 위도 | 방문자가 활동에 액세스한 위도입니다. | 47.269<br>소수점 이하 3 자리로 반올림됨 (약 100 미터 정확도) |
| 지역 - 경도 | 방문자가 활동에 액세스한 경도입니다. | -122.269<br>소수점 이하 3 자리로 반올림됨 (약 100 미터 정확도) |
| 지역 - 주/지역 | 방문자가 활동에 액세스한 상태 또는 지역. | Utahnew<br>South Wales |
| 지역 - 우편번호 | 방문자가 활동에 액세스한 우편 번호. | 84004 |
| 모바일 - 통신사 | 활동에 액세스할 때 방문자가 사용한 이동통신사. | Vodafonet<br>-mobile |
| 네트워크 - 연결 속도 | 방문자가 활동에 액세스할 때의 네트워크 연결 속도입니다. | Broadbandcabledslmobilewirelesssatellite<br><br><br><br><br> |
| 네트워크 - 도메인 이름 | 방문자가 활동에 액세스한 네트워크 도메인의 이름. | `nnt.net` |
| 네트워크 - ISP | 방문자가 활동에 액세스한 네트워크입니다. | NNT Communications Corporation |

## 모바일 데이터

| Attribute name | 속성 설명 | 샘플 값 |
| --- | --- | --- |
| 모바일 - 장치 - 브랜드 | 방문자가 활동에 액세스하는 데 사용한 모바일 장치 상표입니다. | Apple |
| 모바일 - 장치 - 모델 이름 | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 모델 이름입니다. | iPhone XS |
| 모바일 - OS - OSX | 사용자가 OSX 장치를 사용하여 활동에 액세스했는지 여부를 지정합니다. | 0는 false 이고, 1는 true 입니다. |
| 모바일 - 화면 높이 (px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 높이 (픽셀 단위) 입니다. | 1, 2, 3 등 |
| 모바일 - 화면 너비 (px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 너비 (픽셀 단위) 입니다. | 1, 2, 3 등 |