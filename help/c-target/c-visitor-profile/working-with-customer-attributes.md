---
keywords: customer relationship management;customer record service;crs;crm;mbox3rdpartyid;customer attributes;targeting;csv;crm;adobe experience cloud people
description: Adobe Experience Cloud 사람 핵심 서비스의 고객 특성을 사용하여 Adobe Target에서 컨텐츠 타깃팅을 위한 CRM(고객 관계 관리) 데이터베이스의 기업 고객 데이터를 사용하는 방법에 대한 정보입니다.
title: Adobe Target의 고객 속성
feature: visitor profiles
subtopic: Getting Started
topic: Standard
uuid: fc3c9a02-30d7-43df-838d-10ce1aa17f16
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 37%

---


# 고객 속성{#customer-attributes}을 참조하십시오.

Information about using enterprise customer data from Customer Relationship Management (CRM) databases for content targeting in [!DNL Adobe Target] by using customer attributes in the [!DNL Adobe Enterprise Cloud People] core service.

Enterprise customer data collected through multiple sources and stored inside CRM databases can be used in [!DNL Target] to strategically deliver the most relevant content to customers, specifically focusing on returning customers. Audiences and customer attributes in the [!DNL People] core service (formerly Profiles and Audiences) brings together data collection and analysis with testing and optimization, making data and insights actionable.

## Customer attributes overview {#section_B4099971FA4B48598294C56EAE86B45A}

[핵심 서비스의](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) 고객 속성 [!DNL People] 은 [!DNL Adobe Experience Cloud] 해당 서비스의 일부이며 [!DNL Experience Cloud] 기업에 고객 데이터를플랫폼으로 전달하는 도구를 제공합니다.

[!DNL Experience Cloud]로 온보딩되는 데이터는 모든 [!DNL Experience Cloud] 워크플로우에 사용할 수 있습니다. [!DNL Target] 이 데이터를 사용하여 특성을 기반으로 돌아온 고객을 타깃팅합니다. [!DNL Adobe Analytics]는 이러한 속성을 사용하며, 분석 및 세그멘테이션에 사용될 수 있습니다.

![crs 예](/help/c-target/c-visitor-profile/assets/crs.png)

Consider the following information as your work with customer attributes and [!DNL Target]:

* There are some prerequisite requirements that you must meet before you can use the [!UICONTROL Customer attributes] feature in the [!DNL People] core service. For more information, see &quot;Prerequisites for uploading Customer Attributes&quot; in [Customer attributes](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in the *Experience Cloud and Core Services Product documentation*.

   >[!NOTE]
   >
   >[!DNL at.js] (모든 버전) 또는 [!DNL mbox.js] 버전 58 이상이 필요합니다.

* [!DNL Adobe] 은 CRM 데이터베이스의 고객 속성(방문자 프로필) 데이터의 100%가 컨텐츠에 [!DNL Experience Cloud] 업로드되므로 타깃팅에 사용할 수 있음을 보장하지 않습니다 [!DNL Target]. 현재 설계에서는 적은 양의 데이터(대규모 프로덕션 배치의 최대 0.1%까지)가 온보딩되지 않을 가능성이 있습니다.
* The lifetime of customer attributes data imported from the [!DNL Experience Cloud] to [!DNL Target] depends on the lifetime of the visitor profile, which is 14 days by default. 자세한 내용은 [방문자 프로필 라이프타임을 참조하십시오](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* If the `vst.*` parameters are the only thing identifying the visitor, the existing &quot;authenticated&quot; profile will not be fetched as long as `authState` is UNAUTHENTICATED (0). The profile will come into play only if `authState` is changed to AUTHENTICATED (1).

   For example, if the `vst.myDataSource.id` parameter is used to identify the visitor (where `myDataSource` is the data source alias) and there is no MCID or third-party ID, using the parameter `vst.myDataSource.authState=0` won&#39;t fetch the profile that might have been created through a Customer Attributes import. If the desired behavior is to fetch the authenticated profile, the `vst.myDataSource.authState` must have the value of 1 (AUTHENTICATED).

* `mbox3rdPartyID`에서 더하기 기호(+)와 슬래시(/)는 보낼 수 없습니다.

## 사람 핵심 서비스의 고객 속성 액세스

1. 메뉴 아이콘( [!DNL Adobe Experience Cloud]메뉴 아이콘 ![)을 클릭한 다음](/help/c-target/c-visitor-profile/assets/menu-icon.png) 사람을 클릭합니다 ****.

   ![사람](/help/c-target/c-visitor-profile/assets/people.png)

1. 고객 속성 **[!UICONTROL 탭을]** 클릭합니다.

   ![고객 속성 탭](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Customer attribute workflow for Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

아래 그림과 같이 다음 단계를 완료하여 [!DNL Target]에서 CRM 데이터를 사용하십시오.

![crm 워크플로우](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Detailed instructions for completing each of the following tasks can be found in [Create a customer attribute source and upload the data file](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html) in the *Experience Cloud and Core Services Product Documentation*.

1. 데이터 파일 만들기.

   CRM의 고객 데이터를 CSV 형식으로 내보내 .csv 파일을 만듭니다. 또는 업로드하기 위해 zip 또는 gzip 파일을 생성할 수 있습니다. CSV 파일의 첫 번째 행이 헤더이고 모든 행(고객 데이터)의 항목 수가 동일한지 확인합니다.

   다음 그림은 샘플 기업 고객 데이터 파일을 보여줍니다.

   ![crs 샘플](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   다음 그림에서는 샘플 기업 고객 .csv 파일을 보여 줍니다.

   ![csv 샘플](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. 속성 소스를 만들고 데이터 파일 업로드.

   데이터 소스 및 별칭 ID에 대해 이름과 설명을 지정합니다. The alias Id is a unique ID to be used in your Customer Attribute code in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >데이터 소스 이름 및 속성 이름은 점을 포함할 수 없습니다.

   데이터 파일은 업로드 요구 사항을 준수해야 하며 100MB를 초과할 수 없습니다. 파일이 너무 크거나 반복적으로 업로드해야 하는 데이터가 있는 경우 대신 FTP를 통해 파일을 업로드할 수 있습니다.

   * **HTTPS:** .csv 데이터 파일을 드래그 앤 드롭하거나 **[!UICONTROL 찾아보기를]** 클릭하여 파일 시스템에서 업로드할 수 있습니다.
   * **FTP:** FTP 링크를 클릭하여 FTP를 통해 [파일을 업로드합니다](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). 첫 번째 단계는 Adobe 제공 FTP 서버에 대한 암호를 제공하는 것입니다. Specify the password, then click **[!UICONTROL Done]**.

   이제 CSV/ZIP/GZIP 파일을 FTP 서버로 전송하십시오. 이 파일 전송이 성공한 후 동일한 이름과 .fin 확장명을 가진 새 파일을 만듭니다. 이 빈 파일을 서버로 전송합니다. This indicates a End Of Transfer and the [!DNL Experience Cloud] starts to process the data file.

1. 스키마 유효성 검사.

   유효성 검사 프로세스를 사용하여 표시 이름 및 설명을 업로드된 속성(문자열, 정수, 숫자 등)에 매핑할 수 있습니다. 각 속성을 올바른 데이터 유형, 표시 이름 및 설명으로 매핑합니다.

   Click **[!UICONTROL Save]** after the schema validation is complete. 파일 업로드 시간은 크기에 따라 다릅니다.

   ![스키마 유효성 검사](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![스키마 업로드](/help/c-target/c-visitor-profile/assets/upload1.png)

1. 가입 구성 및 속성 소스 활성화.

   **[!UICONTROL 구독 추가]**&#x200B;를 클릭하고 이러한 속성을 구독할 솔루션을 선택합니다. [가입을 구성하면](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/subscription.html) 솔루션 간의 데이터 흐름을 [!DNL Experience Cloud] 설정할 수 있습니다. 속성 소스를 활성화하면 데이터가 구독 중인 솔루션으로 유입될 수 있습니다. 업로드한 고객 레코드는 웹 사이트 또는 애플리케이션에서 들어오는 ID 신호와 대조됩니다.

   ![솔루션 구성](/help/c-target/c-visitor-profile/assets/solution.png)

   ![활성화](/help/c-target/c-visitor-profile/assets/activate.png)

   이 단계를 수행하는 동안 다음 제한 사항에 유의하십시오.

   * HTTP 메서드를 사용하는 각 업로드의 최대 파일 크기는 100MB입니다.
   * FTP 메서드를 사용하는 각 업로드의 최대 파일 크기는 4GB입니다.
   * 가입이 허용되는 속성 수는 [!DNL Target Standard]의 경우 5개이고 [!DNL Target Premium]의 경우 200개입니다.

##  Target에서 고객 속성 사용 {#section_107E3A0F0EC7478E82E6DBD17B30B756}

다음과 같은 방법으로 [!DNL Target]에서 고객 속성을 사용할 수 있습니다.

### 타깃팅 대상자 만들기

[!DNL Target]에서는 대상을 만들 때 방문자 프로필 섹션에서 고객 속성을 선택할 수 있습니다.  모든 고객 속성에는 목록에 &lt; data_source_name > 접두사가 있습니다. 필요에 따라 이러한 특성을 다른 데이터 특성과 결합하여 대상을 구성합니다.

![Target 대상](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### 토큰을 사용하여 프로필 스크립트 만들기

`crs.get('<Datasource Name>.<Attribute name>')` 형식을 사용하여 프로필 스크립트에서 고객 속성을 참조할 수 있습니다.

이 프로필 스크립트는 현재 방문자에 속하는 속성을 제공하기 위해 오퍼에서 직접 사용할 수 있습니다.

### 성공적인 구현 및 사용을 위해 웹 사이트에서 mbox3rdPartyID 사용

Pass `mbox3rdPartyId` as a parameter to the global mbox inside the `targetPageParams()` method. The value of `mbox3rdPartyId` should be set to the customer ID that was present in the CSV data file.

```
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Experience Cloud ID 서비스 사용

Experience Cloud ID 서비스를 사용하는 경우 타깃팅에서 고객 속성을 사용하도록 고객 ID 및 인증 상태를 설정해야 합니다. For more information, see [Customer IDs and Authentication State](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) in the *Experience Cloud Identity Service Help*.

[!DNL Target]에서 고객 속성을 사용하는 방법에 대한 자세한 내용은 다음 리소스를 참조하십시오.

* [고객 속성 소스를 만들고](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html) Experience Cloud 제품 문서에서 데이터 파일 *업로드*
*  *디지털 마케팅 블로그*&#x200B;의 [Customer Attributes: The More You Know, The Better You Connect(고객 속성: 더 많이 알수록 더 쉬워지는 연결)](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/)

## Issues frequently encountered by customers {#section_BE0F70E563F64294B17087DE2BC1E74C}

You might encounter the following issues when working with customer attributes and [!DNL Target].

>[!NOTE]
>
>문제 1과 2는 이 지역의 약 60%의 문제를 야기합니다. 문제 3은 약 30%의 문제를 야기합니다. 문제 4는 약 5%의 문제를 야기합니다. 나머지 5%는 기타 문제로 인해 발생합니다.

### 문제 1:프로필이 너무 커서 고객 속성이 제거됩니다

사용자 프로필의 특정 필드에 대해 문자 제한이 없지만 프로필이 64K보다 커지면 다시 64K보다 작아질 때까지 가장 오래된 속성을 제거하여 잘립니다.

### Issue 2: Attributes not listing in the Audience Library in [!DNL Target], even after several days

일반적으로 파이프라인 연결 문제입니다. 해결 방법으로 고객 속성 팀에 피드를 다시 게시하라고 요청합니다.

### 문제 3:특성에 따라 배달이 작동하지 않음

프로필이 아직 에지에서 업데이트되지 않았습니다. 해결 방법으로 고객 속성 팀에 피드를 다시 게시하라고 요청합니다.

### 문제 4:구현 문제

다음 구현 문제에 유의하십시오.

* 방문자 ID가 올바르게 전달되지 않았습니다. The ID was passed in `mboxMCGVID` instead of `setCustomerId`.
* 방문자 ID가 올바르게 전달되었지만 AUTHENTICATION 상태가 인증됨으로 설정되지 않았습니다.
* `mbox3rdPartyId`가 올바르게 전달되지 않았습니다.

### 문제 5: `mboxUpdate` 제대로 수행되지 않음

`mboxUpdate`  이(가) `mbox3rdPartyId`

### Issue 6: Customer attributes are not being imported into [!DNL Target]

If you cannot find Customer Attributes data in Target, ensure that the import occurred within the last *x* days where *x* is the Target [Visitor Profile Lifetime](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) value (14 days by default).

## Training video: Upload Offline Data using Customer Attributes ![Tutorial badge](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

This video shows you how to import offline CRM, help desk, point-of-sale, and other marketing data into the [!DNL Experience Cloud People] service and associate it with visitors using their known IDs.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
