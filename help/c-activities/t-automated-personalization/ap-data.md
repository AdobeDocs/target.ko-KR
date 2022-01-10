---
keywords: 환경 데이터;세션 데이터;지역 데이터;지역 데이터;지역 데이터;장치 데이터;모바일 데이터;속성;프로필 속성;개인화 알고리즘;기계 학습 알고리즘
description: 데이터 Adobe 알아보기 [!DNL Target] 을(를) 수집 및 사용하여 [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] (AT) 활동.
title: 기계 학습 알고리즘을 생성하기 위해 수집되는 데이터는 무엇입니까?
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: d191274f18098edeba1f6f87c75d9ca20ba0c412
workflow-type: tm+mt
source-wordcount: '2085'
ht-degree: 48%

---

# ![PREMIUM](/help/assets/premium.png) 에서 사용하는 데이터 [!DNL Target] 기계 학습 알고리즘

[!DNL Adobe Target] 에서는 자동으로 다양한 데이터를 수집하고 사용하여 개인화 알고리즘을 [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] (AT) 활동. 방문자가 AP 또는 AT 활동을 시작하면 정보의 스냅숏이 일련의 &quot;교육 레코드&quot;(개인화 알고리즘이 학습할 방문자 데이터)에 전달됩니다.

에 대해 자세히 알아보려면 [!DNL Target] 개인화 알고리즘 을 참조하십시오. [Random Forest 알고리즘](/help/c-activities/t-automated-personalization/algo-random-forest.md).

## 기본값 [!DNL Adobe Target] 속성 카테고리

다음 표는 [!UICONTROL Automated Personalization] 및 [!UICONTROL 자동 Target] 활동은 기본적으로 [!DNL Target] 또는 기타 [!DNL Adobe] 솔루션뿐만 아니라, [개인화 통찰력 보고서](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). 언제든지 입력 데이터 세트를 늘릴 수 있습니다. 추가 데이터를 업로드하는 방법에 대한 자세한 내용은 [에 대한 데이터 업로드 [!DNL Target] 개인화 알고리즘](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| 데이터 카테고리 | 시스템 접두사 | 설명 | 이름 표시 위치 [!UICONTROL Insights] 보고서 |
| --- | --- | --- | --- |
| 환경 매개 변수 | 환경 | 운영 체제, 브라우저 및 요일/시간 등 사용자의 환경에 대한 정보입니다. | 브라우저 - [속성 이름]<br>운영 체제 - [값] |
| Geography | 지역 | IP 조회를 통해 가져온 사용자의 지역에 대한 정보입니다. | 지역 - [지리적 특성] |
| 모바일 장치 | MOB | 사용자의 모바일 장치에 대한 정보입니다. | 장치 - [장치 속성]<br>모바일 - [모바일 속성] |
| 보고 세그먼트 Target | SEG | 에 구성된 보고 세그먼트 [!DNL Target] 보고. | 보고 세그먼트 -[세그먼트 이름] |
| 세션 동작 | SES | 본 페이지 수와 같은 사용자 행동에 대한 정보입니다. | 방문자 프로필 - [속성 이름] |

## 사용자 지정 Adobe Target 속성 카테고리

다음 테이블은에서 수집한 고객 제공 데이터를 보여줍니다. [!UICONTROL Automated Personalization] 및 [!UICONTROL 자동 Target] 활동. 이 데이터는 제공하는 경우에만 수집됩니다. 특정 속성 이름 및 샘플 값은 시스템 구성에 따라 다릅니다.

| 데이터 카테고리 | 시스템 접두사 | 설명 | 이름 표시 위치 [!UICONTROL Insights] 보고서 |
| --- | --- | --- | --- |
| 페이지 매개 변수 | 상자 | 호출에 전달된 사용자 지정 페이지 매개 변수(&quot;mbox 매개 변수&quot;) [!DNL Target]. | 사용자 지정 - Mbox 매개 변수 - [매개 변수 이름] |
| [!DNL Target] 프로필 | PRO | 에 직접 업로드된 사용자 지정 프로필 속성 [!DNL Target] API 또는 페이지 매개 변수 및 [!DNL Target] 프로필 스크립트. | 사용자 지정 - 방문자 프로필 - [속성 이름] |
| 고객 속성 | CRS | 에 업로드된 고객 속성 [!DNL Target] 를 통해 [Adobe Experience Cloud 고객 특성 서비스](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html){target=_blank}. | 사용자 지정 - 방문자 프로필 - [속성 이름] |
| URL 매개 변수 | URL | 현재 표시된 페이지의 URL 및 모든 URL 매개 변수. | 사용자 지정 - URL 매개 변수 - [URL 매개 변수] |
| 참조 URL | REF | 참조 URL에 대한 URL 및 모든 URL 매개 변수 참조. | 사용자 지정 - [참조 URL 매개 변수] - [매개 변수 값] |
| Adobe Experience Cloud 공유 대상 | AAM | 공유된 모든 대상 [!DNL Target] 다른 [!DNL Adobe Experience Cloud] 솔루션(예: [!DNL Adobe Audience Manager] 및 [!DNL Adobe Analytics]를 통해 [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html){target=_blank}). | 사용자 지정 - Experience Cloud 대상 - [대상 이름] |
| Adobe Experience Platform RTCDP 대상 | UPS | 와 공유되는 AEP RTCDP 대상 [!DNL Target] 대상 을 참조하십시오.<br>이 기능은 아직 [!DNL Target] 하지만 앞으로 실행될 것입니다. |  |

## 기능 차단 [!DNL Target] 기계 학습 알고리즘

기능은 [!DNL Target] 기계 학습 알고리즘으로 어떠한 경우에도 사용되지 않음 [!UICONTROL 자동 Target] 또는 [!UICONTROL Automated Personalization] 모델 또는 활동.

피쳐 카테고리를 차단하려면 [!DNL Target] 기계 학습 알고리즘, 연락처 [고객 지원 Adobe](/help/cmp-resources-and-contact-information.md#section_CC8B206F58D6495C9372D5C0D4055CF6) 및 위에서 제공한 시스템 접두사를 사용하여 차단한 기능 범주를 지정합니다.

하나 이상의 특정 기능을 [!DNL Target] 기계 학습 알고리즘, 연락처 [고객 지원 Adobe](/help/cmp-resources-and-contact-information.md#section_CC8B206F58D6495C9372D5C0D4055CF6) 및 제공된 아래 시스템 이름을 사용하여 차단을 수행할 특정 기능 이름을 지정합니다. 다음 섹션에는 속성 이름, 설명 및 샘플값을 포함하여 다양한 데이터 유형에 대한 자세한 정보가 들어 있습니다.

## 장치 및 모바일 데이터 {#device-mobile}

| Attribute name | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | --- |
| 모바일 - 장치 - 브랜드 | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 브랜드입니다. | Apple | MOB_targeting.mobile.vendor |
| 모바일 - 장치 - eReader | 장치가 eReader인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.ereader |
| 모바일 - 장치 - 게임 콘솔 | 장치가 게임 콘솔인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.gamesConsole |
| 모바일 - 장치 - 미디어 플레이어 | 장치가 미디어 플레이어인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.mediaPlayer |
| 모바일 - 장치 - 휴대폰 | 장치가 휴대폰인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.mobilePhone |
| 모바일 - 장치 - 모델 이름 | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 모델 이름입니다. | iPhone XS | MOB_targeting.mobile.model |
| 장치 - 셋톱 박스 | 장치가 셋톱 박스인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.setTopBox |
| 모바일 - 장치 - 태블릿 | 장치가 태블릿인지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.tablet |
| 모바일 - 픽셀 밀도(ppi) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 픽셀 밀도입니다. | 1, 2, 3 등 | MOB_targeting.mobile.displayPpi |
| 모바일 - OS - OSX(Android, Windows 등) | 사용자가 OSX(또는 Android, Windows 등) 장치를 사용하여 활동에 액세스했는지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.os[OS]<br>예를 들어, MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux가 있습니다. |
| 모바일 - 화면 높이(px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 높이(픽셀 단위)입니다. | 1, 2, 3 등 | MOB_targeting.mobile.displayHeight |
| 모바일 - 화면 너비(px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 너비(픽셀 단위)입니다. | 1, 2, 3 등 | MOB_targeting.mobile.displayWidth |

## 환경 데이터 {#env}

|특성 이름|특성 설명|샘플 값|시스템 이름| | — | — | — | — | |브라우저 - 요일|방문자가 활동에 액세스한 요일입니다.|0~6.<br>(0: 일요일)|ENV_DayOfWeek| |브라우저 - 시간|방문자가 활동에 액세스한 시간입니다.|0~23<br>(0: 자정)|ENV_UserHour| |브라우저 - 요일 시간|방문자가 활동에 액세스한 요일 시간입니다.|0~168<br>(일요일 자정은 0)|ENV_WeekHour| |브라우저 - 언어 설정|방문자가 활동에 액세스하는 데 사용한 브라우저에 지정된 언어입니다.|영어<br>독일어|ENV_Language| |브라우저 - 시간|방문자가 활동에 액세스한 브라우저의 시간입니다.|0, 6, 12, 18<br>(0: 밤, 6: 아침<br>12는 오후(18은 저녁)|ENV_LocalTimePeriod| |브라우저 - 시간대|방문자가 활동에 액세스하는 동안 시간대입니다.|태평양 표준시<br>동부 표준시<br>GMT|ENV_BrowserTimezoneOffsetMinutes| |브라우저 - 유형|방문자가 활동에 액세스하는 동안 사용한 브라우저의 유형입니다.|Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>기타|ENV_Browser| |브라우저 - 평일/주말|방문자가 활동에 액세스했을 때의 작업 상태입니다(주말, 근무 시간 또는 평일 자유 시간).|토요일과 일요일은 주말<br>월요일~금요일 근무 시간: 0900~1800<br>1800부터 0900까지 월요일-금요일 자유 시간|ENV_UserHourType| |브라우저 - 창 높이(px)|방문자가 활동에 액세스하는 데 사용한 브라우저의 창 높이(픽셀 단위)입니다.|1, 2, 3 등|ENV_BrowserHeight| |브라우저 - 창 너비(px)|방문자가 활동에 액세스하는 데 사용한 브라우저의 창 너비(픽셀 단위)입니다.|1, 2, 3 등|ENV_BrowserWidth| |장치 - 화면 높이(px)|방문자가 활동에 액세스하는 데 사용한 장치의 화면 높이입니다.|1, 2, 3 등|ENV_ScreenHeight| |장치 - 화면 너비(px)|방문자가 활동에 액세스하는 데 사용한 장치의 화면 너비입니다.|1, 2, 3 등|ENV_ScreenWidth| |운영 체제|방문자가 활동에 액세스하는 데 사용한 장치의 운영 체제입니다.|Mac OS<br>Windows<br>Linux<br>검색 보트<br>알 수 없는 OS|ENV_OperatingSystem| |운영 체제 - 버전|방문자가 활동에 액세스하는 데 사용한 운영 체제의 버전입니다.|Windows 10<br>Mac OS 10|ENV_OperatingSystemVersion| |트래픽 소스 - 랜딩 페이지 URL 참조|사이트에 액세스할 때 방문자가 본 첫 페이지입니다.|`https://www.adobe.com/ecloud.html`|ENV_Referrer|

## 지역 데이터 {#geo}

| 속성 이름 | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | --- |
| 지역 - 도시 | 방문자가 활동에 액세스한 도시입니다. | San Francisco | Geo_City |
| 지역 - 국가 | 방문자가 활동에 액세스한 국가입니다. | 독일 | Geo_County |
| 지역 - DMA | 방문자가 활동에 액세스한 DMA(Designated Marketing Area)입니다. | 샬러츠빌 | Geo_DMA |
| 지역 - 위도 | 방문자가 활동에 액세스한 위도입니다. | 47.269<br>소수점 이하 세 자리로 반올림됨(약 100m 정확도) | GEO_Latitude |
| 지역 - 경도 | 방문자가 활동에 액세스한 경도입니다. | -122.269<br>소수점 이하 세 자리로 반올림됨(약 100m 정확도) | GEO_Longitude |
| 지역 - 주/지역 | 방문자가 활동에 액세스한 주 또는 지역입니다. | 유타<br>뉴사우스웨일스 | GEO_State<br>GEO_Region |
| 지역 - 우편 번호 | 방문자가 활동에 액세스한 우편 번호입니다. | 84004 | GEO_ZipCode |
| 모바일 - 통신사 | 방문자가 활동에 액세스할 때 사용한 이동통신사입니다. | Vodafone<br>T-Mobile | GEO_mobileCarrier |
| 네트워크 - 연결 속도 | 방문자가 활동에 액세스했을 때의 장치의 네트워크 연결 속도입니다. | 광대역<br>케이블<br>DSL<br>모바일<br>무선<br>위성 | GEO_ConnectionSpeed |
| 네트워크 - 도메인 이름 | 방문자가 활동에 액세스한 네트워크 도메인의 이름입니다. | `nnt.net` | GEO_DomainName |
| 네트워크 - ISP | 방문자가 활동에 액세스한 네트워크입니다. | nnt communications corporation | GEO_IspName |

## 세션 데이터 {#session}

| 속성 이름 | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | --- |
| 방문자 프로필 - 활동 라이프타임 주문 가격 | 특정 활동에 대한 모든 방문/세션의 모든 주문 가격의 합계를 지정합니다. | 이중 | SES_CUMULATIVE_ORDER_VALUE |
| 방문자 프로필 - 활동 라이프타임 사이트에서 보낸 시간 | 현재 세션을 제외하고 방문자가 사이트에서 보낸 총 시간을 지정하고, 세션이 만료되면 업데이트됩니다. | 더블, 밀리초 | SES_TOTAL_TIME |
| 방문자 프로필 - 활동 중 방문당 평균 페이지 보기 횟수 | 현재 세션을 제외하고 세션당 평균 페이지 보기 횟수를 지정합니다. | 이중 | SES_REQUESTS_PER_SESSION |
| 방문자 프로필 - 방문당 평균 시간 | 방문/세션당 보낸 평균 시간을 지정합니다. 여기에 현재 세션은 포함되지 않습니다. | 더블, 밀리초 | SES_TIME_PER_SESSION |
| 방문자 프로필 - 첫 번째 방문 | 사용자가 상호 작용한 첫 번째 방문 시간을 지정합니다 [!DNL Target]. | 더블, 밀리초 | SES_PROFILE_CREATION_TIME |
| 방문자 프로필 - 마지막 방문 이후의 시간 | 이 특정 활동에 대한 마지막 방문 이후의 시간을 지정합니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_HOURS_SINCE_LAST_VISIT |
| 방문자 프로필 - 위치/콘텐츠의 노출 횟수 | 특정 활동의 특정 위치/콘텐츠 조합에 대한 노출 횟수를 지정합니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| 방문자 프로필 - 마지막 [!DNL Target] 상호 작용 | 마지막으로 상호 작용한 시간을 지정합니다 [!DNL Target]. 상호 작용은 [!DNL Target] 의 현재 구현으로 인해 요청 [!DNL Target] 각 요청 시 프로필을 업데이트합니다. | 더블, 밀리초 | SES_PROFILE_UPDATE_TIME |
| 방문자 프로필 - 활동 전에 본 페이지 수 | 현재 방문/세션을 포함하여 방문자가 활동에 들어갈 때까지의 총 페이지 보기 횟수(노출 횟수)를 지정합니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_TOTAL_PAGE_VIEWS |
| 방문자 프로필 - 현재 방문의 페이지 보기 | 방문자가 활동에 들어갈 때까지 현재 방문/세션에 페이지 보기 횟수를 지정합니다. 정확하게 말하면 노출 횟수입니다. 이러한 노출 횟수는 실제 페이지 보기 횟수가 아니라, 요청이 Target에 도달한 횟수입니다. Target은 사용자가 콘텐츠를 받지 못하거나 보지 않은 다른 이유 또는 시간 초과를 구별하지 못합니다. | 더블(정수 양수만) | SES_SESSION_POSITION |
| 방문자 프로필 - 현재 방문 시작 | Target에서 현재 방문/세션이 시작된 시간을 지정합니다. Target에서 방문은 활동을 입력하지 않고 시작할 수 있습니다. 필요한 것은 [!DNL Target] 요청. 방문자가 활동을 입력하고 스냅샷을 가져올 때까지 시간이 걸릴 수 있습니다. | 더블, 밀리초 | SES_SESSION_START |
| 방문자 프로필 - 최근 방문 시작일 | 마지막 방문/세션이 [!DNL Target] 시작됨. 이 속성은 세션이 만료되면 업데이트됩니다.<br>방문자의 첫 번째 세션인 경우 `LAST_SESSION_START = 0.`이 됩니다. | 더블, 밀리초 | SES_LAST_SESSION_START |
| 방문자 프로필 - 처음 활동을 시작할 때 가장 최근 방문한 이후 시간 | 이전 세션과 사용자가 활동을 시작하고 스냅숏이 수행되는 시간 사이의 기간을 지정합니다. | 더블, 밀리초 | SES_RECENCY |
| 방문자 프로필 - 활동 입력 전 방문 시간 | 마지막 상호 작용 사이의 차이를 지정합니다 [!DNL Target] 그리고 현재 방문이 시작된 경우입니다. 이 속성은 사용자가 활동을 시작하고 스냅숏이 수행될 때까지 방문/세션 기간으로 간주될 수 있습니다.<br>[!DNL Target]세션 시작 시간과 마지막 업데이트 시간이 동일한 호출에 의해 트리거되면 음수 값이 발생합니다. 음수 값은 0로 간주해야 합니다. | 더블, 밀리초 | SES_SESSION_TIME |
| 방문자 프로필 - 총 방문 횟수 | 총 방문/세션 수를 지정합니다. 현재 방문/세션은 포함하지 않습니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_TOTAL_SESSIONS |
| 방문자 프로필 - 활동에 대한 총 방문 횟수 | 특정 활동에 대한 방문 횟수를 지정합니다. 이전 방문이 없는 경우 0을 반환합니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_PREVIOUS_VISIT_COUNT |
| 방문자 프로필 - 전환이 있는 활동에 대한 총 방문 횟수 | 방문 중에 전환이 하나 이상 있었던 경우 특정 활동에 대한 방문/세션 횟수를 지정합니다. | 이중 | SES_CUMULATIVE_SUCUMULATIVE |
| 방문자 프로필 - 전환이 없는 활동에 대한 방문 횟수 | 전환이 없는 특정 활동에 대한 방문/세션 횟수입니다. 이 값은 전환 후 0으로 재설정되거나, 전환이 발생하지 않는 경우 -1로 재설정됩니다. | 더블(정수 양수만) 1, 2, 3 등 | SES_SUCCESS_RECENCY |
