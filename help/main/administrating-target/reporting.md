---
keywords: 보고서;보고서;보고;experience cloud 솔루션;시간대;시간대;통화;IP 제외;매출액에서 예상되는 향상도;매출;매출액에서 상승도;세분화된 우선순위;세분화된 우선순위
description: 사용 [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics] 보고 소스로 기본 시간대 및 통화 형식을 지정하고, 보고에서 제외할 IP 주소를 추가하는 등의 작업을 수행할 수 있습니다.
title: 에서 보고를 구성하는 방법 [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: ea9513c4310d13e1e7899aa7e228b4d7ecdf0748
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 22%

---

# 에서 보고 구성 [!DNL Target]

에서 사용할 일반 설정 구성 [!DNL Adobe Target] 전체에 적용되는 보고 [!DNL Target] 계정입니다.

에 액세스하려면 [!UICONTROL Reporting] 구성 페이지에서 **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

이 페이지에서 다음 설정을 지정할 수 있습니다.

* 보고에 사용할 Adobe Experience Cloud 솔루션
* 보고에 사용할 시간대
* 보고에 사용할 통화
* 보고에서 제외할 IP 주소
* 보고에 매출액에서 예상되는 향상도를 표시할지 여부
* 세분화된 우선순위를 활성화할지 여부

>[!NOTE]
>
>제외할 시간대, 통화 및 IP 주소는 을 사용하는 활동에 적용됩니다 [!DNL Target] 보고. 이 설정은 를 사용하는 활동에는 적용되지 않습니다. [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) 또는 [!DNL Customer Journey Analytics] 를 보고 소스로 사용합니다.

![보고 페이지](/help/main/administrating-target/assets/reporting.png)

## Reporting Cloud 솔루션 {#solution}

결과 및 보고서에 사용되는 데이터를 결정하는 옵션을 설정합니다.

활동의 보고 소스를 선택하십시오. [!DNL Target], [!DNL Adobe Analytics], 또는 [!DNL Adobe Customer Journey Analytics]. 활동을 만드는 동안 안내가 있는 3가지 부분 워크플로의 일부로 활동당 보고 소스를 선택하도록 선택할 수도 있습니다.

보고 소스를 선택하는 경우 다음 정보를 고려하십시오.

* **[!DNL Adobe Target]**: 보고 소스가 다음으로 설정된 경우 **[!DNL Target]** 여기서는 를 사용하는 활동을 만들거나 활성화할 수 없습니다. [!DNL Analytics] 또는 [!DNL Customer Journey Analytics] 를 보고 소스로 사용합니다. 보고 소스를 다음으로 변경해야 합니다. **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Analytics]**: 보고 소스가 다음으로 설정된 경우 **[!DNL Analytics]** 여기서는 를 사용하는 활동을 만들거나 활성화할 수 없습니다. [!DNL Target] 또는 [!DNL Customer Journey Analytics] 를 보고 소스로 사용합니다. 보고 소스를 다음으로 변경해야 합니다. **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Customer Journey Analytics]**: 보고 소스가 다음으로 설정된 경우 **[!DNL Customer Journey Analytics]** 여기서는 를 사용하는 활동을 만들거나 활성화할 수 없습니다. [!DNL Target] 또는 [!DNL Analytics] 를 보고 소스로 사용합니다. 보고 소스를 다음으로 변경해야 합니다. **[!UICONTROL Select per activity]**.
* **활동당 선택**: 보고 소스가 다음으로 설정된 경우 **[!UICONTROL Select per activity]** 여기에서 선택한 보고 소스에서 지원하는 활동을 만들고 활성화할 수 있습니다.

보고 소스를 결정할 때는 다음 정보를 고려하십시오.

* **[!DNL Analytics]**: 를 사용하는 지원되는 활동의 매트릭스입니다. [!DNL Analytics] 보고 소스(A4T)로서 [지원되는 활동 유형](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) 위치: *Adobe Target용 보고 소스로서의 Adobe Analytics (A4t)*.

  [!UICONTROL Automated Personalization] (AP) 활동 작성 및 활성화는 선택한 보고 소스와 관계없이 허용됩니다. [!UICONTROL Automated Personalization] 선택할 때는 활동이 지원되지 않습니다. [Adobe Target용 보고 소스로서의 Adobe Analytics (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

  다음을 지정하는 경우에도 [!DNL Analytics] 를 보고 소스로 사용할 때에는 [!DNL Target] 의 보고 소스로 사용됩니다. [!DNL Automated Personalization] 활동.

* **[!DNL Customer Journey Analytics]**: 를 사용하는 지원되는 활동의 매트릭스입니다. [!DNL Target] 보고 위치 [!DNL Customer Journey Analytics], 참조 [지원되는 활동 유형](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) 위치: *[!DNL Target]보고 위치[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate], 및 [!UICONTROL Auto-Target] 활동 생성 및 활성화는 선택한 보고 소스와 관계없이 허용됩니다. 선택할 때는 이러한 활동이 지원되지 않습니다. [보고 소스로서의 Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

  다음을 지정하는 경우에도 [!DNL Customer Journey Analytics] 를 보고 소스로 사용할 때에는 [!DNL Target] 의 보고 소스로 사용됩니다. [!DNL Automated Personalization] 활동.

  을 지정하는 경우 [!DNL Customer Journey Analytics] 를 의 보고 소스로 사용 [!UICONTROL Auto-Allocate] 또는 [!UICONTROL Auto-Target] 활동, [!DNL Target] 또는 [!DNL Analytics] 를 보고 소스로 사용할 수 있습니다.

## 보고를 위한 시간대

보고에 사용할 시간대를 지정합니다.

## 보고 통화

보고에 사용할 통화를 지정합니다.

## 제외할 IP [!DNL Target] 보고 데이터

보고 데이터에서 제외할 IP 주소를 지정합니다. 예를 들어 내부 회사 주소를 제외하는 것은 보고 데이터가 웹 사이트에서의 고객 상호 작용을 반영하도록 하는 좋은 방법입니다.

새 라인에 각 IP 주소를 입력합니다.

## 매출액에서 예상되는 상승도 표시

목표에 대한 통화 값을 입력하는 경우 매출액에서 예상되는 상승도를 표시하도록 선택할 수 있습니다. [!DNL Target]은 모든 사용자가 우승을 경험하는 경우 이루게 되는 매출 상승도를 예측할 수 있습니다. 예상되는 상승도 기능은 기본적으로 비활성화됩니다.

전용 [!DNL Experience Cloud] 관리자 사용자는 이 기능을 활성화하거나 비활성화할 수 있습니다. 예상되는 상승도가 비활성화되면 해당 필드가 인터페이스에 표시되지 않습니다. 이 기능을 비활성화해도 예상치에 사용되는 데이터를 비롯한 어떤 데이터도 손실되지 않습니다. 예상치는 기능의 활성화 여부와 관계없이 수집되는 데이터를 기준으로 합니다.

자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

## 세밀하게 제어된 우선순위 사용

우선순위 범위에 대해 0~999의 숫자 항목을 사용할 수 있습니다.

설정에 따라 우선순위의 UI 및 옵션이 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다.

대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.
