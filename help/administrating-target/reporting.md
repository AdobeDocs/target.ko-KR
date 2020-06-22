---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: 일반 설정, 모바일 뷰포트 구성 및 CSS 선택기를 지정하여 Adobe Target VEC(Visual Experience Composer)를 구성합니다.
title: Adobe Target에서 보고 구성
topic: Standard
translation-type: tm+mt
source-git-commit: 0736f6f777f9f3d64706541bf5ef8265615e9082
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 30%

---


# Target에서 보고 구성

전체 계정에 적용되는 보고에 사용할 [!DNL Adobe Target] 일반 설정을 [!DNL Target] 구성합니다.

>[!NOTE]
>
>이 항목의 정보는 Target Standard/Premium 20.6.1 릴리스(2020년 7월)에 나오는 UI 변경 사항에 대해 살짝 돋보이게 하기 위해 업데이트되었습니다. 이 항목에 제시된 대부분의 정보는 현재 UI에 적용됩니다. 그러나 옵션이 약간 다를 수 있습니다.

보고 [!UICONTROL 구성] 페이지에 액세스하려면 **[!UICONTROL 관리]** > 보고 **[!UICONTROL 를]클릭합니다.**

이 페이지에서 다음 설정을 지정할 수 있습니다.

* 보고에 사용할 Adobe Experience Cloud 솔루션
* 보고에 사용할 표준 시간대
* 보고에 사용할 통화
* 보고에서 제외할 IP 주소
* 보고에서 예상 매출 증가를 표시할지 여부
* 세부적으로 분류된 우선 순위를 사용할지 여부

>[!NOTE]
>
>제외할 표준 시간대, 통화 및 IP 주소는 [!DNL Target] 보고를 사용하는 활동에 적용됩니다. 이러한 설정은 보고 소스(/help/c-integrating-target-with-mac/a4t/a4t.md)으로 Target(A4T)에 [Analytics을] 사용하는 활동에는 적용되지 않습니다.

![보고 페이지](/help/administrating-target/assets/reporting.png)

## Reporting Cloud 솔루션

결과 및 보고서에 사용되는 데이터를 결정하는 옵션을 설정합니다.

Select the reporting source for your activities, either [!DNL Target] or [!DNL Adobe Analytics]. 또한 활동별로 보고 소스를 선택하도록 지정할 수 있습니다.

보고 소스를 선택하는 경우 다음 정보를 고려하십시오.

* 보고 소스가 여기에서 **[!DNL Target]**&#x200B;으로 설정된 경우 [!DNL Analytics]를 보고 소스로 사용하는 활동을 활성화할 수 없습니다. You must change the reporting source to [!DNL Target] in your activity or change the reporting source to **[!UICONTROL Select per activity]** in **[!UICONTROL Administration]>[!UICONTROL Reporting]**.
* If the reporting source is set to **[!DNL Analytics]** here, you are not allowed to activate an activity that uses [!DNL Target] as the reporting source (the reporting source is specified as **[!UICONTROL Target per activity])**. You must change the reporting source to[!DNL Analytics]in your activity or change the reporting engine to**[!UICONTROL Select per activity ]**in**[!UICONTROL Administration]>[!UICONTROL Reporting ]**.
* If the reporting source is set to **[!UICONTROL Select per activity]** here, you can create, activate, and deactivate activities that are supported by the selected reporting source. For a matrix of supported activities, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.
* [!UICONTROL AP(Automated Personalization] ) 활동 생성, 활성화 및 비활성화를 선택한 보고 소스에 관계없이 사용할 수 있습니다. Automated Personalization activities are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Even if you specify [!DNL Analytics] as your reporting source, [!DNL Target] is used as the reporting source for Automated Personalization activities. For more information, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.

## 보고 표준 시간대

보고에 사용할 시간대를 지정합니다.

## 보고를 위한 통화

보고에 사용할 통화를 지정합니다.

## Target 보고 데이터에서 제외할 IP

보고 데이터에서 제외할 IP 주소를 지정합니다. 예를 들어, 내부 회사 주소를 제외하는 것은 보고 데이터가 웹 사이트의 고객 상호 작용을 반영하도록 하는 좋은 방법입니다.

새 줄에 각 IP 주소를 입력합니다.

## 매출액에서 예상되는 상승도 표시

목표에 대한 통화 값을 입력할 경우 예상 수익 향상도를 표시하도록 선택할 수 있습니다. [!DNL Target]은 모든 사용자가 우승을 경험하는 경우 이루게 되는 매출 상승도를 예측할 수 있습니다. 예상되는 상승도 기능은 기본적으로 비활성화됩니다.

Only [!DNL Experience Cloud] Admin users can enable or disable this feature. 예상되는 상승도가 비활성화되면 해당 필드가 인터페이스에 표시되지 않습니다. 이 기능을 비활성화해도 예상치에 사용되는 데이터를 비롯한 어떤 데이터도 손실되지 않습니다. 예상치는 기능의 활성화 여부와 관계없이 수집되는 데이터를 기준으로 합니다.

자세한 내용은 [매출 상승도 평가](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

## 세밀하게 제어된 우선순위 사용

우선순위 범위에 대해 0~999의 숫자 항목을 사용할 수 있습니다.

설정에 따라 우선순위의 UI 및 옵션이 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다.

대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.
