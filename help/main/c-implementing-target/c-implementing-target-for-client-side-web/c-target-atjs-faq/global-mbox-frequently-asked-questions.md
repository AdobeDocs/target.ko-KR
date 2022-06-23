---
keywords: 문제 해결;자주 묻는 질문;FAQ;FAQ;글로벌;글로벌 mbox
description: Adobe에 대한 FAQ 및 답변 읽기 [!DNL Target] 글로벌 mbox입니다.
title: 글로벌 Mbox에 대해 Faq는 무엇입니까?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 64%

---

# 글로벌 mbox FAQ

글로벌 mbox에 대한 FAQ 목록

## 내 [!DNL Target] 계정이 여러 도메인에 걸쳐 설정되어 있습니까? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

계정에서는 하나의 글로벌 mbox만 지원됩니다.

활동에 URL 규칙을 추가하여 활동이 실행되는 위치를 제한할 수 있습니다. 자세한 내용은 [유사한 페이지에 동일한 경험 포함](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

를 사용하여 페이지에서 매개 변수를 전달할 수도 있습니다. [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/){target=_blank}를 선택하고 페이지의 &quot;URL 구성&quot; 섹션에서 해당 매개 변수를 선택합니다. [!UICONTROL 시각적 경험 작성기] (VEC) 또는 양식 기반 경험 작성기에서 매개 변수를 &quot;개선&quot;으로 추가하여

## 에 대한 수입 데이터를 전달하려면 어떻게 합니까? [!DNL Target] 글로벌 mbox를 사용할 수 있습니까? {#section_17AEA933BADA4D169CCEDF5833C41306}

target-global-mbox에 대한 수입 및 주문 정보를 수집하려면 &quot;mbox 매개 변수&quot;를 Target으로 보내야 합니다. 이 매개 변수는 Target에 추가 정보를 보내는 데 사용되는 이름/값 쌍입니다. Target은 수입 데이터를 채우기 위해 이 매개 변수(예약된 이름)를 자동으로 검색합니다.

`orderConfirmPage`의 경우 `orderTotal`, `orderId` 및 `productPurchasedId`를 전달해야 합니다. 

이러한 매개 변수는 를 통해 target-global-mbox로 전송해야 합니다 `targetPageParams()`. 자세한 내용은 [글로벌 Mbox에 매개 변수 전달](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/)을 참조하십시오.

또한 아래와 같이 주문 확인 페이지가 표시되었을 때 Target이 target-global-mbox에 대한 전환만 카운트하도록 전환 조각에 타깃팅을 추가할 수도 있습니다.

![](assets/revenue1.png)

위 그림의 사이트 페이지 섹션에는 현재 페이지, URL, 포함, orderconfirm이 포함되어 있습니다.

![](assets/revenue2.png)

위 그림의 선택 사항에는 다음 설정이 포함됩니다.

* **이 활동을 통해 무엇을 측정하고자 하십니까:**&#x200B;수입
* **보고를 위한 기본 보기:** RPV(방문객당 수입)
* **목표에 도달했음을 나타내기 위해 대상이 수행한 작업은 무엇입니까?** mbox 확인함, target-global-mbox
