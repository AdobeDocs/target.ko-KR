---
description: Target 구현에 사용자를 추가하고, 작업 공간, 사용자 그룹 및 속성을 만들고, at_property 매개 변수를 포함하도록 Target 구현을 업데이트하고, 역할 및 권한을 지정하는 데 필요한 작업에 대한 정보입니다.
keywords: 사용자 추가;프로젝트;사용자 그룹;속성;작업 공간;속성 관리;속성;at_property;역할;권한
seo-description: 사용자를 Adobe Target 구현에 추가하는 데 필요한 작업에 대한 정보 작업 영역, 사용자 그룹 및 속성을 만듭니다. at_ property 매개 변수를 포함하도록 Target 구현을 업데이트합니다. 역할 및 권한을 지정합니다.
seo-title: Enterprise 권한 구성
solution: Target
subtopic: 시작하기
title: Enterprise 권한 구성
title-outputclass: premium
topic: Premium
uuid: 2f44ecd5-5c43-49c3-b1c3-58d28531c859
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) 엔터프라이즈 권한 구성{#configure-enterprise-permissions}

Target 구현에 사용자를 추가하고, 작업 공간, 사용자 그룹 및 속성을 만들고, at_property 매개 변수를 포함하도록 Target 구현을 업데이트하고, 역할 및 권한을 지정하는 데 필요한 작업에 대한 정보입니다.

>[!NOTE]
>
>속성 및 권한 기능은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.

다음 표에는 속성을 만들고 사용자 역할 및 권한을 지정하기 위해 수행해야 하는 작업이 나와 있습니다. 각 작업에 대한 자세한 내용은 아래 섹션을 참조하십시오.

| 작업 | 수행 위치 |
|--- |--- |
| 1. 사용자 추가(선택 사항) | [!DNL Adobe Admin Console for Enterprise] |
| 2. 작업 공간(제품 프로필) 만들기 | [!DNL Adobe Admin Console for Enterprise] |
| 3. 사용자 그룹 만들기(선택 사항) | [!DNL Adobe Admin Console for Enterprise] |
| 4. 속성 만들기 | [!DNL Target] UI |
| 5: `at_property` 매개 변수를 포함하도록 구현 업데이트 | [!DNL Target] UI, at.js 함수, [!DNL Adobe Launch] 또는 [!DNL Dynamic Tag Management] |
| 6: 역할 및 권한 지정 | [!DNL Adobe Admin Console for Enterprise] |

Enterprise용 Adobe Admin Console에서 수행되는 작업의 경우, 다음 단계에 따라 콘솔에 액세스하십시오.

1. 아직 로그인하지 않은 경우 [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)로 이동하고 Adobe ID를 사용하여 로그인합니다.

   또는

   이미 Experience Cloud에 로그인한 경우 [https://www.marketing.adobe.com](https://www.marketing.adobe.com/)로 이동한 다음 위쪽 탐색 모음에서 [!UICONTROL 앱] 아이콘을 클릭하고 오른쪽의 **[!UICONTROL [관리]** ] &gt; [관리 콘솔 **[!UICONTROL 시작] 를 클릭합니다]**.

1. (조건부) 두 개 이상의 조직을 위한 [!DNL Admin Console for Enterprise]에 액세스할 수 있는 경우 오른쪽 모서리나 맨 위 탐색 막대의 사용자 아바타를 클릭한 다음, 원하는 조직을 선택하십시오.

## 1단계. 사용자 추가(선택 사항) {#section_A92AF0F921B743FEB9E9033433BD816A}

새 [!UICONTROL 속성] 기능을 사용하기 시작할 때 [!DNL Adobe Admin Console for Enterprise]에서 모든 사용자 관리를 수행해야 합니다. 그러나 [!DNL Target]의 모든 기존 사용자는 [!DNL Target]에서 [!DNL Admin Console for Enterprise]로 마이그레이션됩니다.

1. [Admin Console에서](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE) 페이지 상단에 있는 **[!UICONTROL 사용자]** 탭 &gt; **사용자]를 클릭하여 새로운 사용자를 생성하거나 기존 사용자를 편집합니다.[!UICONTROL **
1. *Enterprise 사용 안내서*의 [Experience Cloud에서 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/users.html)에 있는 지침을 따릅니다.

## 2단계. 작업 공간(제품 프로필) 만들기{#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

작업 공간(제품 프로필)을 사용하여 조직에서는 특정 사용자 세트를 특정 속성 세트에 할당할 수 있습니다. 여러 가지 방식에서 작업 공간은 [!DNL Analytics]의 보고서 세트와 비슷합니다.

조직은 Admin Console 내에서 새 작업 공간을 만들고, Target 속성을 이러한 작업 공간에 지정하고, &quot;기본 작업 공간&quot; 구성에서 이러한 새로운 액세스 제한 작업 공간으로 사용자를 이동하여 Enterprise 권한 기능을 활용할 수 있습니다.

고객은 이러한 작업 공간을 사용하여 지역, 사업부, 사이트 섹션별로 또는 선택한 다른 방법을 통해 여러 다른 팀에 대한 액세스를 구분할 수 있습니다.

사용자는 여러 작업 공간에 속할 수 있으며, 각 작업 공간에서 서로 다른 역할을 가질 수도 있습니다.

1. Admin Console에서 **[!UICONTROL ]제품**을 클릭한 다음, 원하는 제품의 이름을 선택합니다.

   ![작업 공간](/help/administrating-target/c-user-management/c-user-management/assets/workspace.png)

1. 원하는 작업 공간(제품 프로필) 만들기:

   * **기본 액세스:**기존의 모든 활동은 &quot;기본 액세스&quot;라는 단일 프로젝트로 병합됩니다. 이는 고객에게 영향을 주지 않습니다. 모든 사용자 역할 및 기능은 이 변경 이전과 정확히 동일하게 유지됩니다.

      AEM([!DNL Adobe Experience Manager]), [!DNL Adobe Mobile Services] 및 [!DNL Target Classic]을 통해 만든 모든 활동도 &quot;기본 액세스&quot; 작업 공간에 포함됩니다. 현재, 프로젝트를 &quot;기본 액세스&quot;에서 다른 프로젝트로 이동할 수 없습니다.

   * **새 작업 공간(제품 프로필):**다음을 수행하여 새 권한 기능을 활용할 수 있습니다.

      * [!DNL Admin Console for Enterprise]에서 새 작업 공간 만들기
      * 작업 공간에 Target 속성 지정
   이러한 작업 공간을 사용하여 지역, 사업부, 사이트 섹션별로 또는 선택한 다른 방법을 통해 여러 다른 팀에 대한 액세스를 구분할 수 있습니다. 사용자는 여러 작업 공간에 속할 수 있으며, 각 작업 공간에서 서로 다른 역할을 가질 수 있습니다.

1. *Enterprise 사용 안내서*에 포함된 [제품 구성 만들기 및 관리](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html)의 지침에 따르십시오.

>[!NOTE]
>작업 공간 구성에 대한 자세한 내용은 아래 교육 비디오를 참조하십시오.

### 작업 영역 ID 얻기 {workspace-id}

Target API에서 [엔터프라이즈 권한을 활용하려면 작업 공간 ID를 전달해야](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)합니다.

1. [Adobe Admin Console](https://adminconsole.adobe.com)에서 [!UICONTROL 제품] 탭을 클릭한 다음 왼쪽 메뉴에서 제품을 클릭하여 PLC (작업 영역) 목록을 표시합니다.
1. 원하는 PLC (작업 영역) 를 클릭한 다음 아래에서 보듯이 URL에서 &quot;profiles&quot; ID를 찾습니다.

![Workspaceid](/help/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## 3단계. 사용자 그룹 만들기(선택 사항) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

개발자, 분석가, 마케터, 경영진 등과 같은 사용자 그룹을 만든 다음 여러 Adobe 제품 및 작업 공간에서 권한을 지정할 수 있습니다. 새 팀 구성원에게 다른 Adobe 제품에 대한 모든 적절한 권한을 지정하면 특정 사용자 그룹에 팀 구성원을 쉽게 추가할 수 있습니다.

1. Admin Console에서 **[!UICONTROL 사용자]** 탭 &gt; **사용자 그룹]을 클릭하여 새로운 사용자 그룹을 생성하거나 기존 그룹을 편집합니다.[!UICONTROL **
1. *Enterprise 사용 안내서*에 포함된 [제품 구성의 사용자 및 그룹 관리](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html)의 지침을 따르십시오.

## 4단계. 속성 만들기 {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

속성은 특정 이름/값 쌍을 Target 호출(mbox, API 등)의 매개 변수로 추가하면 활성화됩니다. 

속성은 특정 채널(웹, 모바일, 이메일 및 API/기타)에 속합니다.

**팁**: 속성 생성 방법에 대한 자세한 내용은 아래 교육 비디오를 참조하십시오.

1. [!DNL Target]에서 **[!UICONTROL 설정]** &gt; **[!UICONTROL 속성]**을 클릭하여 [!UICONTROL 속성] 목록을 표시합니다.
1. **속성 만들기**를 클릭합니다.

   ![새 속성 대화 상자](/help/administrating-target/c-user-management/property-channel/assets/new_property1.png)

   다음 필드를 채웁니다.

   * **채널:**속성에 대해 원하는 채널, 즉 웹, 모바일 앱, 이메일 또는 기타/API(예: 셋톱 박스 또는 PlayStation 콘솔)를 지정합니다.
   * **이름(필수):** 속성에 대해 수사적 이름을 지정합니다.
   * **설명:** 속성에 대한 선택적 설명을 지정합니다.

1. **[!UICONTROL 코드 생성]**을 클릭하여 [5: at_property 매개 변수를 포함하도록 구현 업데이트](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8)의 단계를 수행하면서 사용할 코드를 생성합니다.
1. 클립보드에 코드를 복사합니다.
1. 완료되면 **[!UICONTROL 저장]을 클릭합니다.**

>[!NOTE]
>속성 생성에 대한 자세한 내용은 아래 교육 비디오를 참조하십시오.

## 5단계: at_property 매개 변수를 포함하도록 구현 업데이트 {#section_9B17A59807A94712BE642942442EBBC8}

[!DNL Target] 사용자 권한 기능을 사용하려면 Target에 연결하는 모든 호출(mbox, api 등)에 `at_property` 매개 변수를 추가해야 합니다.

**`at_property`매개 변수 코드를 획득하려면:**

1. (조건부) [4. 속성 만들기](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD)의 단계를 수행하면서 생성하고 클립보드에 저장한 구현 코드를 사용하고 2단계를 계속 진행합니다.

   또는

   [!DNL Target]에서 **[!UICONTROL 설정]** &gt; **[!UICONTROL 속성]**을 클릭하여 [!UICONTROL 속성] 목록을 표시합니다.

   1. [!UICONTROL 최근 업데이트] 열에 마우스 포인터를 가져가 원하는 속성을 표시하고 [!UICONTROL 코드] 아이콘을 클릭합니다.

      ![속성 호버 코드](/help/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. 강조 표시된 구현 코드를 마우스 오른쪽 단추로 클릭하여 클립보드에 복사합니다.

      ![속성 코드](/help/administrating-target/c-user-management/property-channel/assets/code_property_2_new.png)

1. Target 구현을 이전 단계에서 얻은 구현 코드로 업데이트합니다.

   [!DNL Target] 구현을 업데이트하는 방법에는 여러 가지가 있습니다. 예를 들어, 웹 페이지에는 다음 방법을 사용할 수 있습니다.

   * **[!DNL Dynamic Tag Management]의 &quot;글로벌 매개 변수&quot;를 통해(Adobe 활성화):**

      ![](assets/property_token_2.png)

      자세한 내용은 *다이내믹 태그 관리 제품 설명서*의 [글로벌 매개 변수 - Adobe Target](https://marketing.adobe.com/resources/help/en_US/dtm/target_global_params.html)을 참조하십시오.

   * **targetPageParams() 함수를 통해:** at.js 또는 mbox.js 참조 위에서 <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> 태그에 다음 코드를 배치하십시오.

      ![](assets/property_token_1.png)

      at.js를 사용하여 이 작업을 수행하는 방법에 대한 자세한 내용은 [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md)를 참조하십시오.

   * **mboxCreate() 함수를 통해:**

      ![](assets/property_token_3.png)

      at.js를 사용하여 이 작업을 수행하는 방법에 대한 자세한 내용은 [Targetpageparams ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) 및 [mboxcreate (mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md).

## 6단계: 역할 및 권한 지정 {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Admin Console에서 **[!UICONTROL ]제품**을 클릭한 다음, 원하는 제품의 이름을 선택합니다.

   ![작업 공간](/help/administrating-target/c-user-management/c-user-management/assets/workspace.png)

   >[!NOTE]
   >
   >속성 및 권한 기능은 [!DNL Target Standard/Premium]에만 적용됩니다. [!DNL Target Classic]에서는 이 기능을 사용할 수 없습니다.

1. 원하는 프로필의 이름을 클릭합니다.
1. **[!UICONTROL 사용자를 클릭합니다]**.

   [!UICONTROL 사용자 구성] 탭에는 해당 작업 공간의 모든 사용자가 표시됩니다.

   ![사용자 구성](/help/administrating-target/c-user-management/property-channel/assets/configuration_users_new.png)

1. [!UICONTROL 제품 역할] 열의 각 사용자에 대한 드롭다운 목록을 사용하여 원하는 권한 역할(승인자, 편집자 또는 관찰자)을 선택합니다.

   | 역할 | 설명 |
   |--- |--- |
   | 관찰자 | 활동을 볼 수 있지만 만들거나 편집할 수는 없습니다. |
   | 편집자 | 활동이 라이브 상태가 되기 전에 활동을 만들고 편집할 수 있지만 활동 시작을 승인할 수는 없습니다. |
   | 승인자 | 활동을 만들고, 편집하고 활성화하거나 중지할 수 있습니다. |

   자세한 내용은 *Enterprise 사용 안내서*의 [Admin Console에서 제공 권한 및 역할 관리](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html)를 참조하십시오.

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### Target 작업 공간 구성 방법(6:55)

이 비디오에서는 작업 공간을 만드는 방법을 설명합니다.

* Adobe Target 인터페이스에서 Adobe Admin Console에 액세스(3가지 방법)
* Adobe Admin Console에서 작업 공간 구성

   * 작업 공간에 사용자 추가
   * 작업 공간에 속성 추가

* 기본 작업 공간 이해

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Adobe Target에서 속성을 만드는 방법(3:05)

* [!DNL Adobe Target] 인터페이스에서 속성을 만드는 방법
* 속성 구현에 포함할 속성 토큰을 생성하는 방법
* 다음 세 가지 구현 방법을 숙지하십시오.

   * 웹
   * 모바일 앱
   * 이메일, 셋톱 박스 또는 API 호출

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
