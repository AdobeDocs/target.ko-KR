---
description: Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
seo-description: Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 "교육 레코드"(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.
seo-title: Target의 개인화 알고리즘에 대한 데이터 수집
solution: Target
title: Target의 개인화 알고리즘에 대한 데이터 수집
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Target의 개인화 알고리즘을 위한 데이터 수집{#data-collection-for-the-target-personalization-algorithms}

Target은 자동으로 다양한 데이터를 수집하고 사용하여 자동화된 개인화(AP) 및 자동 타겟(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 AP나 AT 활동을 시작하면 정보의 스냅숏이 일련의 &quot;교육 레코드&quot;(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.

Target 개인화 알고리즘에 대한 자세한 내용은 [Random Forest 알고리즘](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA)을 참조하십시오.

다음 표는 마케터가 작업을 수행하지 않고도 기본적으로 자동화된 개인화를 통해 수집된 데이터와, [개인화 통찰력 보고서](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)에서 이러한 속성을 표시하는 데 사용된 이름 지정 규칙을 보여 줍니다. 언제든지 입력 데이터 세트를 늘릴 수 있습니다. 추가 데이터를 업로드하는 방법에 대한 자세한 내용은 [Target의 개인화 알고리즘을 위한 데이터 업로드](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)를 참조하십시오.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 | 예제 속성 |
|--- |--- |--- |--- |
| URL 매개 변수 | Target에서는 URL 매개 변수를 추출할 URL을 검사합니다. | `Custom - URL Parameter - [URL Parameter]` | 사용자 지정 데이터 |
| URL 매개 변수 참조 | 일반적으로 참조 URL은 mbox 호출을 시작한 특정 페이지를 참조하는 URL입니다.<br>이 변수는 사이트의 사용자 활동뿐만 아니라 사이트의 기술 구현에 의해서도 영향을 받을 수 있습니다. | `Custom - [Referring URL Parameter] - [Parameter value]` | 사용자 지정 데이터 |
| 환경 및 세션 데이터 | 사용자가 활동에 액세스하는 방법 및 시기에 대한 정보입니다. | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | 방문자 프로필 - 가장 최근 방문의 시작<br>방문자 프로필 -총방문 횟수<br>방문자 프로필 - 방문당 평균 시간<br>브라우저 - 시간대<br>브라우저 - 요일<br>브라우저 - 언어 설정<br>브라우저 - 유형<br>운영 체제 - 버전 |
| Geography | 방문자가 있는 위치에 대한 정보입니다. | `Geo - [geo attribute]` | 구/군/시<br>국가<br>지역/주<br>우편 번호<br>위도<br>경도<br>ISP 또는 모바일 통신사 |
| 장치 및 모바일 데이터 | 장치 및 모바일 전용 정보입니다. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | 모바일 장치 OS<br>모바일 화면 크기 |

