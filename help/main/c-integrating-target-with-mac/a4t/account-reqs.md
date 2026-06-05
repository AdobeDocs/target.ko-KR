---
keywords: Analytics를 보고 소스로 사용;a4t;A4T;요구 사항
description: A4T(Analytics for [!DNL Target] 을(를) 사용하여  [!DNL Target] Adobe에서 Adobe Analytics 기반 활동을 만드는 데 필요한 사용자 계정 요구 사항을 구성하는 방법에 대해 알아봅니다.
title: A4T에 필요한 사용자 권한 요구 사항은 무엇입니까?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
TQID: https://experienceleague.adobe.com/SGNIoARqe3yN4WvKF4JPIp0t0JCMiSgj--zrjt-ZXJQ
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3aid: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 31%

---

# 사용자 권한 요구 사항

[!DNL Adobe Target] (A4T)에서 [!DNL Adobe Analytics] 기반 활동을 만들기 위한 사용자 계정 요구 사항에 대한 정보입니다.

[!DNL Analytics] 활동을 정의할 때 보고서 세트를 선택하려면 [!DNL Analytics] 사용자 계정과 [!DNL Target] 사용자 계정이 둘 다 필요합니다.

다음 섹션에 설명된 대로 사용자 계정을 구성해야 합니다.

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

[!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com)에서 다음 작업을 완료하십시오.

### 솔루션 계정을 Adobe ID에 연결합니다

[!DNL Analytics] 및 [!DNL Target] 사용자 계정이 Adobe ID에 연결되어 있어야 합니다.

자세한 내용은 [조직 및 계정 연결](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en)을 참조하세요.

### Experience Cloud 그룹 멤버십 구성

하나 이상의 [!DNL Experience Cloud] 그룹의 구성원으로서 [!DNL Analytics] 및 [!DNL Target]에 액세스할 수 있어야 합니다.

자세한 내용은 [Experience Cloud 사용자 및 제품 관리](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html)를 참조하십시오.

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

지정된 보고서 세트에서 A4T를 사용하려면 해당 보고서 세트에 대한 액세스 권한이 있어야 하며 [!DNL Web Services Access] 그룹에 대한 액세스 권한을 부여해야 합니다.

1. **[!UICONTROL Admin Console]**&#x200B;에서 [!DNL Analytics] 제품 프로필을 클릭한 다음 **[!UICONTROL 권한]** 탭을 클릭합니다.

   그러면 프로필에서 액세스할 수 있는 보고서 세트를 확인할 수 있습니다.

1. [!DNL Target]에서 액세스할 수 있는 보고서 세트가 속해 있는 제품 프로필에 나열된 보고서 세트 중 하나인지 확인하십시오.

   다음 그림은 모든 보고서 세트에 액세스할 수 있는 제품 프로필의 예입니다.

   ![Admin Console 권한 탭](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. [!UICONTROL 웹 서비스 액세스] 그룹에 대한 액세스를 구성하십시오.

   [!DNL Target]의 보고 소스로 [!DNL Analytics]을(를) 사용하려면 [!DNL Analytics]의 [!UICONTROL 웹 서비스 액세스] 그룹에 액세스해야 합니다.


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

추가적인 권한이 필요하지 않습니다.
