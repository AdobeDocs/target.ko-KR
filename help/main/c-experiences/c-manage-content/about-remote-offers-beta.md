---
keywords: 원격 오퍼;캐시된 컨텐츠;다이내믹 컨텐츠;url 유형
description: 에서 원격 오퍼를 사용하는 방법 알아보기 [!DNL Target] 외부 콘텐츠(CMS 또는 기타 시스템의 콘텐츠)를 호스팅하려면 다음 작업을 수행하십시오.
title: 원격 오퍼를 만드는 방법
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip=" [!DNL Adobe Target]의 Beta 기능"
hide: true
hidefromtoc: true
source-git-commit: bd7e6cc206f0d38ee6672c37d836e40b8831da1c
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 21%

---

# 원격 오퍼 만들기

원격 오퍼를 사용하여 [!DNL Adobe Target] 이 참조하고 사용자의 웹 사이트에 전달하는 콘텐츠를 [!DNL Target] 외부에 호스팅합니다. 이 콘텐츠는 편의성이나 보안상의 이유로 CMS(콘텐츠 관리) 또는 다른 시스템에 있을 수 있습니다.

>[!NOTE]
>
>이 문서에는 다음 업데이트 정보가 포함되어 있습니다. [!DNL Target] 현재 베타 프로그램의 일부인 사용자 인터페이스입니다. 다음 [!DNL Adobe Target] 팀은 종종 테스트 및 피드백 목적으로 일부 고객을 위해 새로운 기능을 활성화합니다. 테스트 기간이 완료되면 향후 모든 고객에 대해 이러한 기능이 활성화됩니다 [!DNL Target Standard/Premium] 릴리스 및 릴리스 정보에 발표됨.

원격 오퍼를 만들 수 있는 위치: [!UICONTROL Offers] > [!UICONTROL Code Offers] 페이지 또는 [Forms 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md). 에서 원격 오퍼를 만들거나 적용할 수 없습니다. [!UICONTROL Visual Experience Composer] (VEC). 내용물이 [!DNL Target] 요청 위치이므로 이러한 위치는 전역에는 적합하지 않을 수 있습니다 [!DNL Target] 요청.

원격 오퍼의 예는 다음과 같습니다.

* 크로스셀의 여러 버전
* 동적 장바구니 메시지
* 양식
* 계산기
* 이자율 업데이트
* 전자 메일
* 키오스크
* 음성 도우미

## 원격 오퍼 사용 우수 사례 {#section_7718512D08E14121B6F6B8C38134F4BC}

활동에서 원격 오퍼를 사용하는 우수 사례:

* 오퍼가 과 동일한 도메인에 있는 경우 [!DNL Target] 요청, 사용 [!UICONTROL Cached] 옵션을 사용하면 오퍼 위치를 설명할 때 상대 URL을 사용할 수 있습니다.

  즉, 활동을 스테이징 서버에서 프로덕션으로 이동할 때 URL을 수동으로 변경하지 않고도 콘텐츠에 자동으로 액세스할 수 있습니다.

* 테스트가 서버에서 동적으로 생성된 데이터와 관련된 경우 [!UICONTROL Dynamic] 옵션이 올바른 선택일 수 있습니다.
* 기존 원격 오퍼 콘텐츠의 모양만 테스트하려면 [!UICONTROL Visual Experience Composer] 컨텐츠 관리 시스템에서 반환되는 컨텐츠의 모양과 느낌을 변경합니다.
* 사용 [원격 오퍼 선택 표](#reference_B23BEDD29DDD47709A7651AFD27E776B) (아래)를 참조하십시오. 의문 사항이 있는 경우 계정 담당자에게 문의하십시오.

## 에서 원격 오퍼 만들기 [!UICONTROL Code Offers] 페이지

1. 클릭 **[!UICONTROL Offers]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Code Offers]** 탭.

   ![오퍼 > 코드 오퍼](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. 클릭 **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

   ![원격 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui_new.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 나와 다른 사용자가에서 오퍼를 빠르게 찾을 수 있습니다. [!UICONTROL Assets] 라이브러리입니다.

1. (조건부) [Target Premium 계정](/help/main/c-intro/intro.md#premium)를 클릭하고 원하는 을 선택합니다 [작업 영역](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. 리디렉션 URL 유형을 지정합니다.

   다음을 참조하십시오 [리디렉션 URL 유형: 캐시됨 또는 동적](#url-type) 자세한 내용은 아래를 참조하십시오.

1. 원격 오퍼에 대한 절대 원격 URL을 지정합니다.

1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

## 를 사용하여 원격 오퍼 만들기 [!UICONTROL Form-Based Experience Composer]

1. 을 사용하여 활동을 만드는 동안 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)을(를) 클릭하고 표시할 위치를 선택합니다 **[!UICONTROL Content]** 섹션.

   ![양식 기반 경험 작성기의 콘텐츠 섹션](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. 다음을 클릭합니다. **[!UICONTROL Default Content]** 드롭다운 목록을 클릭한 다음 **[!UICONTROL Change Remote Offer]**.

   ![원격 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. 클릭 **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![원격 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 나와 다른 사용자가에서 오퍼를 빠르게 찾을 수 있습니다. [!UICONTROL Assets] 라이브러리입니다.

1. 리디렉션 URL 유형을 지정합니다.

   다음을 참조하십시오 [리디렉션 URL 유형: 캐시됨 또는 동적](#url-type) 자세한 내용은 아래를 참조하십시오.

1. 원격 오퍼에 대한 원격 URL을 지정하십시오.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 리디렉션 URL 유형: 캐시됨 또는 동적 {#url-type}

다음 정보는 두 옵션 간의 차이점을 이해하는 데 도움이 됩니다.

### 캐시된 URL

캐시된 원격 오퍼의 콘텐츠는에서 제공됩니다. [!DNL Target].

두 시간마다, [!DNL Target] 원격 URL에서 컨텐츠를 가져온 다음 내부에 컨텐츠를 저장합니다. [!DNL Target]. 방문자가 원격 오퍼를 포함하는 경험이 있는 사이트를 로드할 때 [!DNL Target] 은 오퍼를 제공합니다.

누군가 로그인했으므로 캐시된 원격 오퍼는 향상된 보안을 제공합니다. [!DNL Target] 콘텐츠를 변경할 수 없습니다. 콘텐츠를 변경하려면 누군가가 로그 또는 다른 시스템에서 콘텐츠를 변경해야 합니다.

캐시된 원격 오퍼에 대한 절대 또는 상대 URL을 지정할 수 있습니다.

### 동적 URL

다이내믹 원격 오퍼는 이 아니라 콘텐츠 관리 시스템이나 다른 시스템에서 제공됩니다 [!DNL Target].

컨텐츠를 주기적으로 캐시한 다음 로 전달하는 것을 원치 않을 수도 있습니다. [!DNL Target] 방문자가 원격 오퍼를 포함하는 경험이 있는 사이트를 로드할 때마다. 대신 컨텐츠를 호스팅하는 시스템을 호출하고 반환된 오퍼가 각 사용자에 대해 동적이거나 서로 다를 수 있도록 특정 정보를 전달할 수 있습니다. 예를 들어, 사용자가 다이내믹 원격 오퍼가 있는 경험이 포함된 신용 카드 웹 사이트에 로그인하는 경우, 사용자 계정 정보를 얻기 위해 URL에 매개 변수를 전달할 수 있습니다. 그러면 웹 사이트에서는 계좌 잔고와 같은 사용자별 정보를 제공할 수 있습니다.

다음을 클릭할 수 있습니다. **[!UICONTROL Add Parameter]** 하나 이상을 추가하려면 [!DNL Target] 요청 또는 요청 매개 변수.

## 활동에서 원격 오퍼 사용

다음을 사용하여 원격 오퍼를 적용해야 합니다. [!UICONTROL Form-Based Experience Composer]. 현재 다음을 사용하여 원격 오퍼를 적용할 수 없습니다. [!UICONTROL Visual Experience Composer] (VEC).

다음 [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] 는에서 사용할 경험을 만드는 데 유용한 시각적이지 않은 경험 및 오퍼 만들기 인터페이스입니다 [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Recommendations] 다음과 같은 경우 활동 [!UICONTROL Visual Experience Composer] 는 사용할 수 없거나 실용적이지 않습니다. 예를 들어 [!UICONTROL Form-Based Experience Composer] 원격 오퍼를 사용하는 경험을 만듭니다.

1. 에서 활동 만들기 또는 편집 [!UICONTROL Form-Based Experience Composer].

   다음을 참조하십시오 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 자세한 단계별 지침은 을 참조하십시오.

1. 원하는 위치를 지정하고 필요에 따라 대상 세분화를 추가합니다.

1. 에서 드롭다운 목록을 클릭합니다. **[!UICONTROL Content]** 섹션을 클릭한 다음 **[!UICONTROL Change Remote Offer]**.

   ![원격 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. 에서 원하는 원격 오퍼를 선택합니다. [!UICONTROL Select Remote Offer] 대화 상자를 클릭한 다음 **[!UICONTROL Done]**.

1. 활동 구성을 완료합니다.

## 다이내믹 원격 오퍼 작동 방식 {#concept_CC2A969420B34364A9FA78C1CE251818}

다이내믹 원격 오퍼에서는 다이내믹 페이지 기술을 사용하여 값을 오퍼에 전달합니다.

페이지를 렌더링한 후 오퍼가 실행됩니다. 보이지 않는 iFrame은 데이터를 수집하여 프레임에서 복사하고 페이지에 를 삽입하여 전달된 값을 로드합니다.

![remote_offer_howitworks_2 이미지](assets/remote_offer_howitworks_2.jpeg)

1. 방문자의 브라우저가 서버에서 페이지를 요청합니다.

2. 브라우저는 mbox를 포함하여 페이지를 렌더링합니다.

3. `mboxCreate` 호출에는 다이내믹 콘텐츠를 렌더링하는 데 필요한 매개 변수가 포함되어 있습니다.

4. [!DNL Target] 는 다이내믹 콘텐츠의 위치 및 해당 매개 변수와 함께 URL을 반환합니다. mbox 영역에 iFrame을 설정합니다.

5. 브라우저가 URL을 요청하고 페이지에서 렌더링합니다.

## 원격 오퍼 선택 표 {#reference_B23BEDD29DDD47709A7651AFD27E776B}

원격 오퍼 선택 표는 선택할 원격 오퍼의 유형을 결정하는 데 도움이 됩니다. [!UICONTROL Cached] 또는 [!UICONTROL Dynamic].

| 기능 | 캐시됨 | 동적 |
|--- |--- |--- |
| 방문자가 요청할 때마다 업데이트 | 아니오 | 예 |
| 컨텐츠 업데이트 | 2시간마다 캐시됨 | 각 요청 시 즉시 업데이트됨 |
| 로드 시간 | 고속 | 요청 처리로 인해 더 느림 |
| 페이지에서 JavaScript를 볼 수 있음 | 예 | 아니요, 하지만 URL을 통해 전달할 수 있음 |
| 오퍼에 JavaScript가 포함될 수 있음 | 예 | 예 |
| 오퍼 URL | 절대 또는 상대 | 상대 |
| 요청 컴퓨터 | Adobe 서버 | 방문자 쿠키가 저장되어 있는 방문자 컴퓨터 |

## 교육 비디오: 양식 기반 작성기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오는 의 데모를 제공합니다. [!UICONTROL Form-Based Experience Composer]원격 오퍼를 만드는 데 사용할 수 있습니다.

* 를 사용하여 활동 만들기 [!UICONTROL Form-Based Experience Composer]
* 사용 시점 이해 [!UICONTROL Form-Based Experience Composer] 및 [!UICONTROL Visual Experience Composer]
* 개선을 통해 위치 타깃팅

>[!VIDEO](https://video.tv.adobe.com/v/17390)