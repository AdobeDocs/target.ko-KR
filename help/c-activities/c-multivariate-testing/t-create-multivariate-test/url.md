---
description: 활동 URL는 MVT (다변수 테스트) 에서 사용되는 페이지를 결정하며, Target에서 테스트를 설계할 때 열립니다.
keywords: 타겟 지정
seo-description: 활동 URL는 MVT (다변수 테스트) 에서 사용되는 페이지를 결정하며, Adobe Target에서 테스트를 설계할 때 열립니다.
seo-title: 활동 URL
solution: Target
title: 활동 URL
uuid: ddc7330c-199a-4e38-b3d4-6786e3997783
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 활동 URL{#activity-url}

The activity URL determines the page that is used in the [!UICONTROL Multivariate Test] (MVT), and that opens when the test is designed in [!DNL Adobe Target].

When prompted during [activity creation](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specify the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서, [!DNL `https://www.adobe.com`]과 [!DNL `http://www.adobe.com`]은 모두 같습니다.

[!UICONTROL 기본적으로, Visual Experience Composer] (VEC) 는 [계정 기본 설정에 지정된 페이지를 엽니다](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

To display a different page after the VEC opens, click the **[!UICONTROL Configure]** icon, then select **[!UICONTROL Page Delivery]**, then specify the URL.

![페이지 배달 대화 상자](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL 템플릿 규칙 추가]를 클릭합니다.**

추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

* URL
* 도메인
* 경로
* 해시(#) 조각
* 쿼리
* 매개 변수

추가 규칙은 AND 또는 OR을 사용하여 활동 URL에 결합할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

완료되면 **[!UICONTROL 저장]을 클릭합니다.**

>[!NOTE]
>
>Target Standard JavaScript 코드가 포함되지 않은 사이트 URL을 입력하면 페이지 요소를 선택할 수 없습니다.

기본적으로 vec는 회전 배너와 같이 JavaScript가 포함된 요소의 변경을 허용하지 않습니다. **[!UICONTROL 시각적 경험 작성기]에서 이러한 요소를 변경하려면**[!UICONTROL JavaScript를 사용하여 렌더링]을 끄면 됩니다.

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.