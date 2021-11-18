---
keywords: 고객 관계 관리;고객 레코드 서비스;crs;crm;mbox3rdpartyid;고객 속성;타깃팅;csv;crm;adobe experience cloud 사람
description: 에서 콘텐츠 타겟팅을 위해 CRM(고객 관계 관리) 데이터베이스의 엔터프라이즈 고객 데이터를 사용하는 방법을 알아봅니다. [!DNL Adobe Target].
title: 고객 속성은 무엇이며 어떻게 사용할 수 있습니까?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: a600559cd4aa6bf4335af4ef1143472183a998ff
workflow-type: tm+mt
source-wordcount: '1575'
ht-degree: 32%

---

# 고객 속성

의 콘텐츠 타깃팅을 위해 CRM(고객 관계 관리) 데이터베이스의 엔터프라이즈 고객 데이터를 사용하는 방법에 대한 정보입니다 [!DNL Adobe Target] 에서 고객 속성을 사용하여 [!DNL Adobe Enterprise Cloud People] 서비스.

여러 소스를 통해 수집되고 CRM 데이터베이스 내에 저장된 기업 고객 데이터는에서 사용할 수 있습니다. [!DNL Target] 고객에게 가장 관련 있는 컨텐츠를 전략적으로 전달하고, 특히 재방문 고객에 중점을 둡니다. 의 대상 및 고객 속성 [!DNL People] 서비스(이전의 프로필 및 대상)는 데이터 수집 및 분석과 실용적인 데이터와 통찰력을 만드는 테스트 및 최적화를 하나로 모읍니다.

## 고객 속성 개요 {#section_B4099971FA4B48598294C56EAE86B45A}

[고객 속성](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html) 에서 [!DNL People] 서비스는 [!DNL Adobe Experience Cloud] 및 는 고객 데이터를 [!DNL Experience Cloud] 플랫폼.

[!DNL Experience Cloud]로 온보딩되는 데이터는 모든 [!DNL Experience Cloud] 워크플로우에 사용할 수 있습니다. [!DNL Target] 은 속성을 기반으로 재방문 고객을 타깃팅하기 위해 이 데이터를 사용합니다. [!DNL Adobe Analytics]는 이러한 속성을 사용하며, 분석 및 세그멘테이션에 사용될 수 있습니다.

![crs 예](/help/c-target/c-visitor-profile/assets/crs.png)

고객 특성 및 [!DNL Target]:

* 을(를) 사용하기 전에 충족해야 하는 몇 가지 전제 조건 요구 사항이 있습니다 [!UICONTROL 고객 속성] 의 기능 [!DNL People] 서비스. 자세한 내용은 의 &quot;고객 속성을 업로드하기 위한 사전 요구 사항&quot;을 참조하십시오. [고객 속성](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) 에서 *Experience Cloud 서비스 및 관리 설명서*.
* 에 설명된 대로 파일 업로드와 관련된 제한 사항을 알아 두십시오 [고객 속성에 대한 데이터 파일 및 데이터 소스 정보](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en) 에서 *Experience Cloud 중앙 인터페이스 구성 요소 안내서*. 우수 사례:

   * 단일 대용량 파일 업로드(내) [지정된 제한](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en)). 단일 대용량 파일이 여러 개의 작은 파일보다 선호됩니다.
   * 업로드를 여러 파일로 분할해야 하는 경우 새 파일을 제출하기 전에 파일이 완전히 처리되었는지 확인하십시오. 배치에 있는 다음 파일을 제출하기 전에 배치에 있는 각 파일이 완전히 처리되었는지 확인합니다.

* [!DNL Adobe] CRM 데이터베이스의 고객 속성(방문자 프로필) 데이터 100%가 [!DNL Experience Cloud] 따라서 타깃팅에 사용할 수 있습니다. [!DNL Target]. 현재 디자인에서는 적은 비율의 데이터(큰 프로덕션 일괄 처리의 최대 0.1%)가 온보딩되지 않을 수 있습니다.
* 에서 가져온 고객 속성 데이터의 라이프타임 [!DNL Experience Cloud] to [!DNL Target] 은 기본적으로 14일인 방문자 프로필의 라이프타임에 따라 달라집니다. 자세한 내용은 [방문자 프로필 라이프타임](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* 만약 `vst.*` 매개 변수는 방문자를 식별하는 유일한 항목이며, 기존 &quot;인증됨&quot; 프로필은 `authState` 는 인증되지 않음(0)입니다. 프로필은 `authState` 가 AUTHENTICATED (1)로 변경되었습니다.

   예를 들어 `vst.myDataSource.id` 매개 변수는 방문자를 식별하는 데 사용됩니다. 여기서 `myDataSource` 는 데이터 소스 별칭임)이고 매개 변수를 사용하여 MCID 또는 타사 ID가 없습니다 `vst.myDataSource.authState=0` 고객 속성 가져오기를 통해 작성되었을 수 있는 프로필을 가져오지 않습니다. 인증된 프로필을 가져오려면 `vst.myDataSource.authState` 값은 1(AUTHENTICATED)이어야 합니다.

* `mbox3rdPartyID`에서 더하기 기호(+)와 슬래시(/)는 보낼 수 없습니다.

## 사용자 서비스에서 고객 속성에 액세스

1. 에서 [!DNL Adobe Experience Cloud]를 클릭하고 메뉴 아이콘( ![메뉴 아이콘](/help/c-target/c-visitor-profile/assets/menu-icon.png) )를 클릭한 다음 **[!UICONTROL 사람]**.

   ![사람](/help/c-target/c-visitor-profile/assets/people.png)

1. 을(를) 클릭합니다. **[!UICONTROL 고객 속성]** 탭.

   ![고객 속성 탭](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## 에 대한 고객 속성 워크플로우 [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

아래 그림과 같이 다음 단계를 완료하여 [!DNL Target]에서 CRM 데이터를 사용하십시오.

![crm 워크플로우](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

다음 각 작업을 완료하기 위한 자세한 지침은 [고객 속성 소스를 만들고 데이터 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html) 에서 *Experience Cloud 서비스 및 관리 설명서*.

1. 데이터 파일 만들기.

   CRM의 고객 데이터를 CSV 형식으로 내보내 .csv 파일을 만듭니다. 또는 업로드하기 위해 zip 또는 gzip 파일을 생성할 수 있습니다. CSV 파일의 첫 번째 행이 헤더이고 모든 행(고객 데이터)에 동일한 수의 항목이 있는지 확인합니다.

   다음 그림은 샘플 엔터프라이즈 고객 데이터 파일을 보여줍니다.

   ![crs 샘플](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   다음 그림은 샘플 엔터프라이즈 고객 .csv 파일을 보여줍니다.

   ![csv 샘플](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. 속성 소스를 만들고 데이터 파일 업로드.

   데이터 소스 및 별칭 ID에 대해 이름과 설명을 지정합니다. 별칭 Id는 의 고객 속성 코드에 사용할 고유 ID입니다. `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >데이터 소스 이름 및 속성 이름은 점을 포함할 수 없습니다.

   데이터 파일은 업로드 요구 사항 파일을 준수해야 하며 100MB를 초과할 수 없습니다. 파일이 너무 크거나 반복적으로 업로드해야 하는 데이터가 있는 경우 대신 파일을 FTP로 전송할 수 있습니다.

   * **HTTPS:** .csv 데이터 파일을 드래그 앤 드롭하거나 을 클릭할 수 있습니다 **[!UICONTROL 찾아보기]** 를 업로드합니다.
   * **FTP:** 다음 FTP 링크를 클릭합니다. [ftp를 통해 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). 첫 번째 단계는 Adobe 제공 FTP 서버에 대한 암호를 제공하는 것입니다. 암호를 지정한 다음 **[!UICONTROL 완료]**.

   이제 CSV/ZIP/GZIP 파일을 FTP 서버로 전송하십시오. 이 파일이 성공적으로 전송되면 동일한 이름 및 `.fin` 확장. 이 빈 파일을 서버로 전송합니다. 이는 전송 종료 및 [!DNL Experience Cloud] 데이터 파일 처리를 시작합니다.

1. 스키마 유효성 검사.

   유효성 검사 프로세스를 사용하여 표시 이름 및 설명을 업로드된 속성(문자열, 정수, 숫자 등)에 매핑할 수 있습니다. 각 속성을 올바른 데이터 유형, 표시 이름 및 설명으로 매핑합니다.

   클릭 **[!UICONTROL 저장]** 스키마 유효성 검사가 완료된 후. 파일 업로드 시간은 크기에 따라 다릅니다.

   ![스키마 유효성 검사](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![스키마 업로드](/help/c-target/c-visitor-profile/assets/upload1.png)

1. 가입 구성 및 속성 소스 활성화.

   **[!UICONTROL 구독 추가]**&#x200B;를 클릭하고 이러한 속성을 구독할 솔루션을 선택합니다. [구독 구성](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) 간 데이터 흐름을 설정합니다. [!DNL Experience Cloud] 및 솔루션을 제공합니다. 속성 소스를 활성화하면 데이터가 구독 중인 솔루션으로 유입될 수 있습니다. 업로드한 고객 레코드는 웹 사이트 또는 애플리케이션에서 들어오는 ID 신호와 대조됩니다.

   ![솔루션 구성](/help/c-target/c-visitor-profile/assets/solution.png)

   ![활성화](/help/c-target/c-visitor-profile/assets/activate.png)

   이 단계를 수행하는 동안 다음 제한 사항에 유의하십시오.

   * HTTP 메서드를 사용하는 각 업로드의 최대 파일 크기는 100MB입니다.
   * FTP 메서드를 사용하는 각 업로드의 최대 파일 크기는 4GB입니다.
   * 가입이 허용되는 속성 수는 [!DNL Target Standard]의 경우 5개이고 [!DNL Target Premium]의 경우 200개입니다.

## 에서 고객 특성 사용 [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

다음과 같은 방법으로 [!DNL Target]에서 고객 속성을 사용할 수 있습니다.

### 타깃팅 대상자 만들기

[!DNL Target]에서는 대상을 만들 때 방문자 프로필 섹션에서 고객 속성을 선택할 수 있습니다.  모든 고객 속성에는 목록에 &lt; data_source_name > 접두사가 있습니다. 필요에 따라 이러한 특성을 다른 데이터 특성과 결합하여 대상을 구성합니다.

![Target 대상](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### 토큰을 사용하여 프로필 스크립트 만들기

`crs.get('<Datasource Name>.<Attribute name>')` 형식을 사용하여 프로필 스크립트에서 고객 속성을 참조할 수 있습니다.

이 프로필 스크립트는 현재 방문자에 속하는 속성을 제공하기 위해 오퍼에서 직접 사용할 수 있습니다.

### 성공적인 구현 및 사용을 위해 웹 사이트에서 mbox3rdPartyID 사용

패스 `mbox3rdPartyId` 를 내부 글로벌 mbox에 대한 매개 변수로 `targetPageParams()` 메서드를 사용합니다. 다음 값 `mbox3rdPartyId` 는 CSV 데이터 파일에 있는 고객 ID로 설정해야 합니다.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Experience Cloud ID 서비스 사용

Experience Cloud ID 서비스를 사용하는 경우 타깃팅에서 고객 속성을 사용하려면 고객 ID 및 인증 상태를 설정해야 합니다. 자세한 내용은 [고객 ID 및 인증 상태](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) 에서 *Experience Cloud ID 서비스 도움말*.

[!DNL Target]에서 고객 속성을 사용하는 방법에 대한 자세한 내용은 다음 리소스를 참조하십시오.

* [고객 속성 소스를 만들고 데이터 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) 에서 *Experience Cloud 서비스 및 관리 설명서*

## 고객에게 자주 발생하는 문제 {#section_BE0F70E563F64294B17087DE2BC1E74C}

고객 속성 및 [!DNL Target].

>[!NOTE]
>
>문제 1과 2는 이 지역에서 약 60%의 문제를 유발합니다. 문제 3은 약 30%의 문제를 유발합니다. 문제 4는 약 5%의 문제를 유발합니다. 나머지 5%는 기타 문제로 인해 발생합니다.

### 문제 1: 프로필이 너무 커서 고객 특성이 제거됩니다

사용자 프로필의 특정 필드에 대해 문자 제한이 없지만 프로필이 64K보다 커지면 다시 64K보다 작아질 때까지 가장 오래된 속성을 제거하여 잘립니다.

### 문제 2: 의 대상 라이브러리에 속성이 나열되지 않음 [!DNL Target]며칠 후에도

일반적으로 파이프라인 연결 문제입니다. 해결 방법으로 고객 속성 팀에 피드를 다시 게시하라고 요청합니다.

### 문제 3: 게재가 속성을 기반으로 작동하지 않음

프로필이 아직 에지에서 업데이트되지 않았습니다. 해결 방법으로 고객 속성 팀에 피드를 다시 게시하라고 요청합니다.

### 문제 4: 구현 문제

다음 구현 문제에 유의하십시오.

* 방문자 ID가 올바르게 전달되지 않았습니다. ID가 전달되었습니다 `mboxMCGVID` 대신 `setCustomerId`.
* 방문자 ID가 올바르게 전달되었지만 AUTHENTICATION 상태가 인증됨으로 설정되지 않았습니다.
* `mbox3rdPartyId`가 올바르게 전달되지 않았습니다.

### 문제 5: `mboxUpdate` 가 제대로 수행되지 않았습니다.

`mboxUpdate`  가 `mbox3rdPartyId`.

### 문제 6: 고객 속성을 [!DNL Target]

Target에서 고객 속성 데이터를 찾을 수 없는 경우 마지막 가져오기 내에서 가져오기가 발생했는지 확인하십시오 *x* 일 위치 *x* Target [방문자 프로필 라이프타임](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) 값(기본적으로 14일).

## 교육 비디오: 고객 속성을 사용하여 오프라인 데이터 업로드 ![튜토리얼 배지](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

이 비디오에서는 오프라인 CRM, 도움말 데스크, POS 및 기타 마케팅 데이터를 [!DNL Experience Cloud People] 서비스를 제공하고 알려진 ID를 사용하여 방문자와 연결합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
