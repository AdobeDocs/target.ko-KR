---
keywords: 원격 오퍼;원격 오퍼 선택 표;캐시된 컨텐츠;다이내믹 컨텐츠;url 유형
description: Adobe [!DNL Target] 에서 원격 오퍼를 사용하여 외부 콘텐츠(CMS 또는 다른 시스템의 콘텐츠)를 호스팅하는 방법을 알아봅니다. 원격 오퍼를 사용할 수 있는 이유를 알아봅니다.
title: 원격 오퍼를 만드는 방법
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 29%

---

# 원격 오퍼 만들기

원격 오퍼를 사용하여 [!DNL Adobe Target] 이 참조하고 사용자의 웹 사이트에 전달하는 콘텐츠를 [!DNL Target] 외부에 호스팅합니다. 이 콘텐츠는 편의성이나 보안상의 이유로 콘텐츠 관리(CMS) 또는 다른 시스템에 있을 수 있습니다.

>[!NOTE]
>
>원격 오퍼는 [!UICONTROL Offers] > [!UICONTROL Code Offers] 페이지나 [Forms 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)에서 만들 수 있습니다. VEC(시각적 경험 작성기)에서는 원격 오퍼를 만들거나 적용할 수 없습니다. [!DNL Target] 요청 위치에 콘텐츠가 삽입되므로 이는 전역 [!DNL Target] 요청에 적합하지 않을 수 있습니다.
>
>[!DNL Target Classic]에 유사한 기능 [!UICONTROL Offer on Your Site] 및 [!UICONTROL Offer Outside Test&Target]이(가) 포함되었습니다.

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

* 오퍼가 [!DNL Target] 요청과 동일한 도메인에 있는 경우 [!UICONTROL Cached] 옵션을 사용하면 오퍼 위치를 설명하는 데 상대 URL을 사용할 수 있습니다.

  이 경우 스테이징 서버에서 프로덕션으로 활동을 이동할 때 URL을 수동으로 변경하지 않아도 자동으로 컨텐츠에 액세스할 수 있습니다.

* 테스트에 서버에서 동적으로 생성된 데이터가 포함된 경우 [!UICONTROL Dynamic] 옵션이 올바른 선택일 수 있습니다.
* 기존 원격 오퍼 콘텐츠의 모양만 테스트하려는 경우에는 [!UICONTROL Visual Experience Composer]을(를) 사용하여 콘텐츠 관리 시스템에서 반환되는 콘텐츠의 모양과 느낌을 변경하십시오.
* 특정 사례에 가장 적합한 오퍼를 선택하려면 [원격 오퍼 선택 표](#reference_B23BEDD29DDD47709A7651AFD27E776B)(아래)를 사용하십시오. 의문 사항이 있는 경우 계정 담당자에게 문의하십시오.

## 코드 오퍼 페이지에서 원격 오퍼 만들기

1. **[!UICONTROL Offers]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Code Offers]** 탭을 선택합니다.

   ![오퍼 > 코드 오퍼](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**&#x200B;을(를) 클릭합니다.

   ![원격 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 [!UICONTROL Assets] 라이브러리에서 오퍼를 빠르게 찾을 수 있습니다.

1. 리디렉션 URL 유형을 지정합니다.

   자세한 내용은 아래의 [리디렉션 URL 유형: 캐시됨 또는 동적](#url-type)을 참조하십시오.

1. 원격 오퍼에 대한 원격 URL을 지정하십시오.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 양식 기반 경험 작성기를 사용하여 원격 오퍼 만들기

1. [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 활동을 만드는 동안 **[!UICONTROL Content]** 섹션을 표시할 위치를 선택하십시오.

   양식 기반 경험 작성기의 ![콘텐츠 섹션](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. **[!UICONTROL Default Content]** 드롭다운 목록을 클릭한 다음 **[!UICONTROL Change Remote Offer]**&#x200B;을(를) 클릭합니다.

   ![원격 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**&#x200B;을(를) 클릭합니다.

   ![원격 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 [!UICONTROL Assets] 라이브러리에서 오퍼를 빠르게 찾을 수 있습니다.

1. 리디렉션 URL 유형을 지정합니다.

   자세한 내용은 아래의 [리디렉션 URL 유형: 캐시됨 또는 동적](#url-type)을 참조하십시오.

1. 원격 오퍼에 대한 원격 URL을 지정하십시오.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

## 리디렉션 URL 유형: 캐시됨 또는 동적 {#url-type}

다음 정보는 두 옵션 간의 차이점을 이해하는 데 도움이 됩니다.

### 캐시된 URL

캐시된 원격 오퍼에 대한 콘텐츠가 [!DNL Target]에서 제공됩니다.

[!DNL Target]은(는) 두 시간마다 원격 URL에서 콘텐츠를 가져온 다음 [!DNL Target] 내부에 콘텐츠를 저장합니다. 방문자가 원격 오퍼를 포함하는 경험이 있는 사이트를 로드하면 [!DNL Target]이(가) 오퍼를 제공합니다.

[!DNL Target]에 로그인한 사용자는 콘텐츠를 변경할 수 없으므로 캐시된 원격 오퍼는 향상된 보안을 제공합니다. 컨텐츠를 변경하기 위해서는 누군가가 컨텐츠 관리 시스템이나 다른 시스템에 로그인하여 컨텐츠를 변경해야 합니다.

캐시된 원격 오퍼에 대한 절대 또는 상대 URL을 지정할 수 있습니다.

### 동적 URL

동적 원격 오퍼는 [!DNL Target]이(가) 아닌 콘텐츠 관리 또는 다른 시스템에서 제공됩니다.

방문자가 원격 오퍼를 포함하는 경험이 있는 사이트를 로드할 때마다 [!DNL Target]에서 컨텐츠를 주기적으로 캐시한 다음 전달하는 것을 원치 않을 수 있습니다. 대신 컨텐츠를 호스팅하는 시스템을 호출하고 반환된 오퍼가 각 사용자에 대해 동적이거나 서로 다를 수 있도록 특정 정보를 전달할 수 있습니다. 예를 들어, 사용자가 다이내믹 원격 오퍼가 있는 경험이 포함된 신용 카드 웹 사이트에 로그인하는 경우, 사용자 계정 정보를 얻기 위해 URL에 매개 변수를 전달할 수 있습니다. 그러면 웹 사이트에서는 계좌 잔고와 같은 사용자별 정보를 제공할 수 있습니다.

**[!UICONTROL Add Parameter]**&#x200B;을(를) 클릭하여 하나 이상의 [!DNL Target] 요청 또는 요청 매개 변수를 추가할 수 있습니다.

## 활동에서 원격 오퍼 사용

[!UICONTROL Form-Based Experience Composer]을(를) 사용하여 원격 오퍼를 적용해야 합니다. 현재 VEC를 사용하여 원격 오퍼를 적용할 수 없습니다.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer]은(는) 시각적 경험 작성기가 사용이 불가능하거나 실용적이지 않을 때 [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Recommendations] 활동에 사용할 경험을 만드는 데 유용한 시각적이지 않은 경험 및 오퍼 만들기 인터페이스입니다. 예를 들어 [!UICONTROL Form-Based Experience Composer]을(를) 사용하여 원격 오퍼를 사용하는 경험을 만들 수 있습니다.

1. [!UICONTROL Form-Based Experience Composer]에서 활동을 만들거나 편집합니다.

   자세한 단계별 지침은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

1. 원하는 위치를 지정하고 필요에 따라 대상 세분화를 추가합니다.

1. **[!UICONTROL Content]** 섹션에서 드롭다운 목록을 클릭한 다음 **[!UICONTROL Change Remote Offer]**&#x200B;을(를) 클릭합니다.

   ![원격 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. [!UICONTROL Select Remote Offer] 대화 상자에서 원하는 원격 오퍼를 선택한 다음 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. 활동 구성을 완료합니다.

## 다이내믹 원격 오퍼 작동 방식 {#concept_CC2A969420B34364A9FA78C1CE251818}

다이내믹 원격 오퍼에서는 다이내믹 페이지 기술을 사용하여 값을 오퍼에 전달합니다.

페이지를 렌더링한 후 오퍼가 실행됩니다. 보이지 않는 iframe은 데이터를 수집하여 프레임에서 복사하고 페이지에 를 삽입하여 전달된 값을 로드합니다.

![remote_offer_howitworks_2 이미지](assets/remote_offer_howitworks_2.jpeg)

## 원격 오퍼 선택 표 {#reference_B23BEDD29DDD47709A7651AFD27E776B}

원격 오퍼 선택 표는 선택할 원격 오퍼의 유형([!UICONTROL Cached] 또는 [!UICONTROL Dynamic])을 결정하는 데 도움이 됩니다.

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

이 비디오는 원격 오퍼를 만드는 데 사용할 수 있는 양식 기반 작성기 데모를 제공합니다.

* 양식 기반 경험 작성기를 사용하여 활동 만들기
* 언제 양식 기반 경험 작성기를 사용하고 언제 시각적 경험 작성기를 사용할지 이해
* 개선을 통해 위치 타깃팅

>[!VIDEO](https://video.tv.adobe.com/v/17390)
