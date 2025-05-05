---
keywords: 환경 데이터;세션 데이터;지역 데이터;지리적 데이터;장치 데이터;모바일 데이터;속성;프로필 속성;개인화 알고리즘;머신 러닝 알고리즘;머신 러닝 알고리즘
description: ' [!DNL Adobe Target] 수집 및 사용하여 머신 러닝 알고리즘을 작성하는 데이터를 알아봅니다.'
title: 머신 러닝 알고리즘을 구축하기 위해 수집되는 데이터는 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: fe6a7addd3854c430798fc339741c9ae6a4efc7d
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 51%

---

# [!DNL Target] 머신 러닝 알고리즘에서 사용하는 데이터

[!DNL Adobe Target]은(는) 다양한 데이터를 자동으로 수집하고 사용하여 [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Auto-Target]&#x200B;(AT) 활동에서 개인화 알고리즘을 만듭니다. 방문자가 [!UICONTROL Automated Personalization] 또는 [!UICONTROL Auto-Target] 활동을 시작하면 정보의 스냅숏이 일련의 &quot;교육 레코드&quot;(개인화 알고리즘이 학습하는 방문자 데이터)에 전달됩니다.

[!DNL Target] 개인화 알고리즘에 대한 자세한 내용은 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)을 참조하세요.

## 기본 [!DNL Target] 특성 범주

다음 표에서는 [!DNL Target] 또는 다른 [!DNL Adobe] 솔루션의 구성 없이 기본적으로 [!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동에서 수집된 데이터를 보여 줍니다. 표에는 [Personalization 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)에서 이러한 특성을 표시하는 데 사용되는 명명 규칙도 포함되어 있습니다. 언제든지 입력 데이터 세트를 늘릴 수 있습니다. 추가 데이터를 업로드하는 방법에 대한 자세한 내용은 [개인화 알고리즘을 위한 데이터 업로드](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)를 참조하십시오. [!DNL Target] 

| 데이터 범주 | 시스템 접두사 | 설명 | [!UICONTROL Insights]개 보고서에 이름 표시 |
| --- | --- | --- | --- |
| 환경 매개 변수 | 환경 | 운영 체제, 브라우저 및 요일/요일을 포함한 사용자 환경에 대한 정보입니다. | 브라우저 - [특성 이름]<br>운영 체제 - [값] |
| Geography | 지역 | IP 조회를 통해 얻은 사용자 지역 정보. | 지역 - [지역 특성] |
| 모바일 디바이스 | 군중 | 사용자의 모바일 장치에 대한 정보입니다. | 장치 - [장치 특성]<br>모바일 - [모바일 특성] |
| [!DNL Target]개의 보고 세그먼트 | SEG | [!DNL Target] 보고에 구성된 보고 세그먼트입니다. | 보고 세그먼트 -[세그먼트 이름] |
| 세션 동작 | SES | 본 페이지 수와 같은 사용자 동작에 대한 정보입니다. | 방문자 프로필 - [특성 이름] |

## 사용자 지정 [!DNL Target] 특성 범주

다음 표는 [!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동에서 수집한 고객 제공 데이터를 보여 줍니다. 이 데이터는 제공한 경우에만 수집됩니다. 특정 속성 이름과 샘플 값은 시스템 구성에 따라 다릅니다.

| 데이터 범주 | 시스템 접두사 | 설명 | [!UICONTROL Insights]개 보고서에 이름 표시 |
| --- | --- | --- | --- |
| 페이지 매개 변수 | 상자 | [!DNL Target] 호출에서 전달된 사용자 지정 페이지 매개 변수(&quot;mbox 매개 변수&quot;)입니다. | 사용자 지정 - Mbox 매개 변수 - [매개 변수 이름] |
| [!DNL Target] 프로필 | PRO | 사용자 지정 프로필 특성은 API 또는 페이지 매개 변수 및 [!DNL Target] 프로필 스크립트를 통해 [!DNL Target] 프로필에 직접 업로드됩니다. | 사용자 지정 - 방문자 프로필 - [특성 이름] |
| 고객 속성 | CRS | [[!DNL Adobe Experience Cloud Customer Attributes Service]](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=ko){target=_blank}을(를) 통해 [!DNL Target] 프로필에 업로드된 고객 특성입니다. | 사용자 지정 - 방문자 프로필 - [특성 이름] |
| URL 매개 변수 | URL | 현재 표시된 페이지의 URL 및 모든 URL 매개 변수. | 사용자 지정 - URL 매개 변수 - [URL 매개 변수] |
| 참조 URL | 참조 | 참조 URL 및 참조 URL에 대한 모든 URL 매개 변수 | 사용자 지정 - [참조 URL 매개 변수] - [매개 변수 값] |
| [!DNL Adobe Experience Cloud]개의 공유 대상 | AAM | 다른 [!DNL Adobe Experience Cloud] 솔루션(예: [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=ko){target=_blank}을 통해 [!DNL Adobe Audience Manager] 및 [!DNL Adobe Analytics])의 [!DNL Target]과(와) 모든 대상을 공유했습니다. | 사용자 지정 - Experience Cloud 대상 - [대상 이름] |
| 대상 [!DNL Adobe Experience Platform Real-time CDP]개 | UPS | [!UICONTROL Destinations]을(를) 통해 [!DNL Target]과(와) 공유되는 Platform Real-time CDP 대상자입니다. |  |


## [!DNL Target] 머신 러닝 알고리즘에서 기능 차단

[!DNL Target] 기계 학습 알고리즘에서 기능을 차단하여 [!UICONTROL Automated Personalization] 또는 [!UICONTROL Auto-Target] 모델 또는 활동에서 사용할 수 없습니다.

자세한 내용은 *[!DNL Adobe Target]개발자 안내서*&#x200B;의 [모델 API(차단 목록에 추가) 개요](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html?lang=ko){target=_blank}를 참조하십시오.

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
| 모바일 - 픽셀 밀도(ppi) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 픽셀 밀도입니다. | 1, 2, 3 등등. | MOB_targeting.mobile.displayPpi |
| 모바일 - OS - OS X([!DNL Android], [!DNL Windows] 등) | 사용자가 OSX(또는 [!DNL Android], [!DNL Windows] 등) 장치를 사용하여 활동에 액세스했는지 여부를 지정합니다. | 0이면 False이고, 1이면 True입니다. | MOB_targeting.mobile.os[OS]<br>예: MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| 모바일 - 화면 높이(px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 높이(픽셀 단위)입니다. | 1, 2, 3 등등. | MOB_targeting.mobile.displayHeight |
| 모바일 - 화면 너비(px) | 방문자가 활동에 액세스하는 데 사용한 모바일 장치의 화면 너비(픽셀 단위)입니다. | 1, 2, 3 등등. | MOB_targeting.mobile.displayWidth |

## 환경 데이터 {#env}

| Attribute name | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | -- |
| 브라우저 - 요일 | 방문자가 활동에 액세스한 요일입니다. | 0 - 6.<br>(0: 일요일) | ENV_DayOfWeek |
| 브라우저 - 시간 | 방문자가 활동에 액세스한 시간입니다. | 0 - 23<br>(0: 자정) | ENV_UserHour |
| 브라우저 - 요일 시간 | 방문자가 활동에 액세스한 요일 시간입니다. | 0 - 168<br>(0: 일요일 자정) | ENV_WeekHour |
| 브라우저 - 언어 설정 | 방문자가 활동에 액세스하는 데 사용한 브라우저에 지정된 언어입니다. | 영어<br>독일어 | ENV_Language |
| 브라우저 - 시간 | 방문자가 활동에 액세스한 브라우저의 시간입니다. | 0, 6, 12, 18<br>(0: 밤, 6: 아침,<br>12: 오후, 18: 저녁) | ENV_LocalTimePeriod |
| 브라우저 - 표준 시간대 | 방문자가 활동에 액세스한 시간대입니다. | 태평양 표준시<br>동부 표준시<br>GMT | ENV_BrowserTimezoneOffsetMinutes |
| 브라우저 - 유형 | 방문자가 활동에 액세스하는 동안 사용한 브라우저의 유형입니다.  | [!DNL Chrome]<br>[!DNL Firefox]<br>[!DNL Internet Explorer]<br>[!DNL Safari]<br>기타 | ENV_Browser |
| 브라우저 - 평일/주말 | 방문자가 활동에 액세스할 때의 작업 상태입니다(주말, 근무 시간 또는 평일 자유 시간). | 토요일과 일요일: 주말<br>월요일~금요일 0900 - 1800 근무시간<br>1800 이후 월요일-금요일 0900까지 평일 자유 시간 | ENV_UserHourType |
| 브라우저 - 창 높이(px) | 방문자가 활동에 액세스하는 데 사용한 브라우저의 창 높이(픽셀 단위)입니다. | 1, 2, 3 등, | ENV_BrowserHeight |
| 브라우저 - 창 너비(px) | 방문자가 활동에 액세스하는 데 사용한 브라우저의 창 너비(픽셀 단위)입니다. | 1, 2, 3 등, | ENV_BrowserWidth |
| 장치 - 화면 높이(px) | 방문자가 활동에 액세스하는 데 사용한 장치의 화면 높이입니다. | 1, 2, 3 등, | ENV_ScreenHeight |
| 장치 - 화면 너비(px) | 방문자가 활동에 액세스하는 데 사용한 장치의 화면 너비입니다. | 1, 2, 3 등, | ENV_ScreenWidth |
| 운영 체제 | 방문자의 장치에서 활동에 액세스하는 데 사용한 운영 체제입니다. | [!DNL Mac OS]<br>[!DNL Windows]<br>[!DNL Linux]<br>검색 보트<br>알 수 없는 OS | ENV_OperatingSystem |
| 운영 체제 - 버전 | 방문자가 활동에 액세스하는 데 사용한 운영 체제의 버전입니다. | [!DNL Windows] 10<br>[!DNL Mac OS] 10 | ENV_OperatingSystemVersion |
| 트래픽 소스 - 랜딩 페이지 URL 참조 | 사이트에 액세스할 때 방문자가 본 첫 페이지입니다. | `https://www.adobe.com/ecloud.html` | ENV_Referrer |

## 지역 데이터 {#geo}

| Attribute name | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | --- |
| 지역 - 도시 | 방문자가 활동에 액세스한 도시입니다. | San Francisco | 지역_도시 |
| 지역 - 국가 | 방문자가 활동에 액세스한 국가입니다. | 독일 | Geo_Country |
| 지역 - DMA | 방문자가 활동에 액세스한 DMA(Designated Marketing Area)입니다. | 샬러츠빌 | Geo_DMA |
| 지역 - 위도 | 방문자가 활동에 액세스한 위도입니다. | 47.269<br>소수점 이하 세 자리로 반올림됨(약 100m 정확도) | GEO_Latitude |
| 지역 - 경도 | 방문자가 활동에 액세스한 경도입니다. | -122.269<br>소수점 이하 세 자리로 반올림됨(약 100m 정확도) | GEO_Longitude |
| 지역 - 주/지역 | 방문자가 활동에 액세스한 주 또는 지역입니다. | 유타<br>뉴사우스웨일스 | GEO_State<br>GEO_Region |
| 지역 - 우편 번호 | 방문자가 활동에 액세스한 우편 번호입니다. | 84004 | GEO_ZipCode |
| 모바일 - 통신사 | 방문자가 활동에 액세스할 때 사용한 이동통신사입니다. | [!DNL Vodafone]<br>[!DNL T-Mobile] | GEO_mobileCarrier |
| 네트워크 - 연결 속도 | 방문자가 활동에 액세스했을 때의 장치의 네트워크 연결 속도입니다. | 광대역<br>케이블<br>DSL<br>모바일<br>무선<br>위성 | GEO_ConnectionSpeed |
| 네트워크 - 도메인 이름 | 방문자가 활동에 액세스한 네트워크 도메인의 이름입니다. | `nnt.net` | GEO_DomainName |
| 네트워크 - ISP | 방문자가 활동에 액세스한 네트워크입니다. | nnt communications corporation | GEO_IspName |

## 세션 데이터 {#session}

| Attribute name | 속성 설명 | 샘플값 | 시스템 이름 |
| --- | --- | --- | --- |
| 방문자 프로필 - 활동 라이프타임 주문 가격 | 특정 활동에 대한 모든 방문/세션의 모든 주문 가격의 합계를 지정합니다. | 이중 | SES_CUMULATIVE_ORDER_VALUE |
| 방문자 프로필 - 활동 라이프타임 사이트에서 보낸 시간 | 현재 세션을 제외하고 방문자가 사이트에서 보낸 총 시간을 지정하고, 세션이 만료되면 업데이트됩니다. | 더블, 밀리초 | SES_TOTAL_TIME |
| 방문자 프로필 - 활동 중 방문당 평균 페이지 보기 횟수 | 현재 세션을 제외하고 세션당 평균 페이지 보기 횟수를 지정합니다. | 이중 | SES_REQUESTS_PER_SESSION |
| 방문자 프로필 - 방문당 평균 시간 | 방문/세션당 보낸 평균 시간을 지정합니다. 여기에 현재 세션은 포함되지 않습니다. | 더블, 밀리초 | SES_TIME_PER_SESSION |
| 방문자 프로필 - 첫 번째 방문 | 사용자가 [!DNL Target]과(와) 상호 작용한 첫 번째 방문 시간을 지정합니다. | 더블, 밀리초 | SES_PROFILE_CREATION_TIME |
| 방문자 프로필 - 마지막 방문 이후의 시간 | 이 특정 활동에 대한 마지막 방문 이후의 시간을 지정합니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_HOURS_SINCE_LAST_VISIT |
| 방문자 프로필 - 위치/콘텐츠의 노출 횟수 | 특정 활동의 특정 위치/콘텐츠 조합에 대한 노출 횟수를 지정합니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| 방문자 프로필 - 마지막 [!DNL Target] 상호 작용 | [!DNL Target]과(와)의 마지막 상호 작용 시간을 지정합니다. [!DNL Target]의 현재 구현이 각 요청에서 프로필을 업데이트하므로 모든 [!DNL Target] 요청마다 상호 작용이 발생합니다. | 더블, 밀리초 | SES_PROFILE_UPDATE_TIME |
| 방문자 프로필 - 활동 전에 본 페이지 수 | 방문자가 활동에 들어갈 때까지 현재 방문/세션을 포함하여 총 페이지 보기 횟수(노출 횟수)를 지정합니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_TOTAL_PAGE_VIEWS |
| 방문자 프로필 - 현재 방문의 페이지 보기 | 방문자가 활동에 들어갈 때까지 현재 방문/세션에 페이지 보기 횟수를 지정합니다. 정확하게 말하면 노출 횟수입니다. 이러한 노출 횟수는 실제 페이지 보기 횟수가 아니라, 요청이 [!DNL Target]에 도달한 횟수입니다. [!DNL Target]은(는) 시간 초과 또는 사용자가 콘텐츠를 받지 못하거나 보지 못한 다른 이유를 구별할 수 없습니다. | 더블(정수 양수만) | SES_SESSION_POSITION |
| 방문자 프로필 - 현재 방문 시작 | [!DNL Target]과(와)의 현재 방문/세션이 시작된 시간을 지정합니다. 활동을 입력하지 않고 [!DNL Target]&#x200B;(으)로 방문을 시작할 수 있습니다. [!DNL Target] 요청에 대한 호출만 필요합니다. 방문자가 활동을 입력하고 스냅샷을 가져올 때까지 시간이 걸릴 수 있습니다. | 더블, 밀리초 | SES_SESSION_START |
| 방문자 프로필 - 최근 방문 시작일 | [!DNL Target]과(와)의 마지막 방문/세션이 시작된 시간을 지정합니다. 이 속성은 세션이 만료되면 업데이트됩니다.<br>방문자의 첫 번째 세션인 경우 `LAST_SESSION_START = 0.`이(가) 됩니다. | 더블, 밀리초 | SES_LAST_SESSION_START |
| 방문자 프로필 - 처음 활동을 시작할 때 가장 최근 방문한 이후 시간 | 이전 세션과 사용자가 활동을 시작하고 스냅숏이 수행되는 시간 사이의 기간을 지정합니다. | 더블, 밀리초 | SES_RECENCY |
| 방문자 프로필 - 활동 입력 전 방문 시간 | [!DNL Target]과의 마지막 상호 작용과 현재 방문이 시작된 시간의 차이를 지정합니다. 이 속성은 사용자가 활동을 시작하고 스냅숏이 수행될 때까지 방문/세션 기간으로 간주될 수 있습니다.<br>세션 시작 시간과 마지막 업데이트 시간이 동일한 [!DNL Target] 호출에 의해 트리거되면 음수 값이 발생합니다. 음수 값은 0로 간주해야 합니다. | 더블, 밀리초 | SES_SESSION_TIME |
| 방문자 프로필 - 총 방문 횟수 | 총 방문/세션 수를 지정합니다. 현재 방문/세션은 포함하지 않습니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_TOTAL_SESSIONS |
| 방문자 프로필 - 활동에 대한 총 방문 횟수 | 특정 활동에 대한 방문 횟수를 지정합니다. 이전 방문이 없는 경우 0을 반환합니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_PREVIOUS_VISIT_COUNT |
| 방문자 프로필 - 전환이 있는 활동에 대한 총 방문 횟수 | 방문 중에 전환이 하나 이상 있었던 경우 특정 활동에 대한 방문/세션 횟수를 지정합니다. | 이중 | SES_CUMULATIVE_SUCCESS |
| 방문자 프로필 - 전환이 없는 활동에 대한 방문 횟수 | 전환이 없는 특정 활동에 대한 방문/세션 횟수입니다. 이 값은 전환 후 0으로 재설정되거나, 전환이 발생하지 않는 경우 -1로 재설정됩니다. | 더블(정수 양수만) 1, 2, 3 등. | SES_SUCCESS_RECENCY |
