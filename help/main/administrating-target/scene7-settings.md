---
keywords: scene7;dynamic media classic;디지털 에셋 관리;에셋;dam;콘텐츠 라이브러리;이미지 교환
description: Adobe Target을 Adobe Dynamic Media Classic(Scene7)에 연결하면 작성자가 활동에서 이미지 오퍼를 사용하고 Experience Cloud 에셋의 이미지를 교환할 수 있습니다.
landing-page-description: VEC 및 양식 기반 경험 작성기에서 이미지 오퍼, 콘텐츠 라이브러리 DAM 워크플로우 및 이미지 교체 작업을 활성화하도록 관리에서 Scene7 구성을 구성합니다.
short-description: VEC 및 양식 기반 경험 작성기에서 이미지 오퍼, 콘텐츠 라이브러리 DAM 워크플로우 및 이미지 교체 작업을 활성화하도록 관리에서 Scene7 구성을 구성합니다.
title: Dynamic Media Classic(Scene7) 통합을 구성하는 방법은 무엇입니까?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: 'https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 553aa8fb523a62f72f0e2be7d7fd1b4eb663da6b
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 5%
---
# Dynamic Media Classic 구성(Scene7)

**[!UICONTROL 관리]**&#x200B;의 **[!UICONTROL Scene7 구성]** 탭을 사용하여 [!DNL Adobe Target]을(를) [!DNL Adobe Dynamic Media Classic]&#x200B;(이전의 [!DNL Scene7])에 연결합니다. 통합은 DAM(디지털 자산 관리)을 [!UICONTROL 콘텐츠 라이브러리]로 가져오고 활동에서 이미지 대체 워크플로우를 가능하게 합니다.

이 탭이 다른 관리 작업에 어떻게 맞는지 알아보려면 [Target을 어떻게 관리합니까?](/help/main/administrating-target/administrating-target.md)를 참조하십시오. 인터페이스에서 **[!UICONTROL 관리]**&#x200B;를 찾으려면 [UI 이해 [!DNL Target] 를 참조하십시오](/help/main/c-intro/understand-the-target-ui.md).

**개요**

1. [통합을 통해 얻을 수 있는 기능](#what-it-enables): 이미지 오퍼, 이미지 교체 및 적합한 에셋.
1. [계정 및 자격 증명](#account-and-credentials): 기존 [!DNL Dynamic Media] 계정 및 지원되는 계정 유형입니다.
1. [사용 지침](#usage-guidelines): URL, 배달 및 지원되지 않는 항목.
1. [Target에서 Scene7 구성](#configure-scene7): 로그인 및 지역 설정.

{{permissions-update}}

## 통합으로 얻을 수 있는 이점 {#what-it-enables}

**[!UICONTROL Scene7 구성]**&#x200B;이 설정되면 작성자는 [!DNL Target] 활동의 [!DNL Adobe Experience Cloud] 자산 폴더에 업로드된 이미지를 사용할 수 있습니다. **[!UICONTROL 이미지 대체 오퍼]** 옵션이 [시각적 경험 작성기 및 양식 기반 경험 작성기](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)를 포함하여 활동 워크플로에 표시됩니다. VEC의 교체 동작은 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을 참조하십시오.

이 설정이 구성되지 않은 경우 **[!UICONTROL 이미지 교체 오퍼]**&#x200B;를 활동을 만드는 동안 사용할 수 없습니다.

통합은 Experience Cloud 에셋 폴더의 활동에 속하는 에셋을 제공합니다. [!DNL Target] 활동에서 사용할 [!DNL Dynamic Media Classic]의 모든 자산을 **노출하지**&#x200B;않습니다.

구성 후 [!UICONTROL 오퍼] 라이브러리에서 이미지 오퍼를 관리합니다. [콘텐츠 관리](/help/main/c-experiences/c-manage-content/manage-content.md)를 참조하세요.

## 계정 및 자격 증명 {#account-and-credentials}

이미 [!DNL Dynamic Media] 계정이 있는 경우 **[!UICONTROL Scene7 구성]** 페이지에 해당 자격 증명을 입력하십시오.

Adobe은 더 이상 신규 [!DNL Target] 고객 또는 신규 사용자에 대해 사용 제한, 무료 [!DNL Dynamic Media Classic] 계정을 프로비저닝하지 않습니다. 조직에 이 통합을 위한 로그인 자격 증명이 이미 있는 경우 계속 작동합니다. 계정 관련 질문은 [!DNL Adobe] 담당자에게 문의하십시오.

## 사용 지침 {#usage-guidelines}

이 통합으로 이미지를 사용할 때는 다음 제한 사항을 염두에 두십시오.

* **저장소 URL이 아닌 이미지 오퍼** [!DNL Dynamic Media] 저장소 URL과 게시된 게재 URL이 다릅니다. 스토리지 링크에서 오퍼를 작성하지 마십시오. 게재가 실패합니다. 대신 [이미지 오퍼](/help/main/c-experiences/c-manage-content/manage-content.md) 및 이미지 교체 워크플로우를 사용하십시오.
* 사용자 지정 코드의 **공개 URL입니다.** 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 자체 웹 서버에 호스팅하고 해당 URL을 사용합니다. [!DNL Target] 타겟팅 워크플로 외부에서 사용하기 위해 Experience Cloud 업로드 이미지에 대해 게시된 URL을 가져올 수 없습니다. 해당 사용은 계약에 따라 허용되지 않습니다.
* **적격 에셋.** Experience Cloud 에셋 폴더(및 이 통합에서 지원하는 워크플로)에 업로드된 에셋만 범위에 있으며 전체 [!DNL Dynamic Media Classic] 카탈로그는 포함되지 않습니다.

## Target에서 Scene7 구성 {#configure-scene7}

[!DNL Dynamic Media Classic]&#x200B;([!DNL Scene7])에 연결하려면 다음 단계를 사용하십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL Scene7 구성]**&#x200B;을 클릭합니다.
1. [!DNL Dynamic Media Classic] 계정 정보 입력:

   | 필드 | 설명 |
   | --- | --- |
   | **지역** | [!DNL Dynamic Media] 계정의 지역: 북미, 유럽 또는 아시아. |
   | **임시 폴더** | [!DNL Dynamic Media]에 수동으로 업로드하는 대상 폴더 외부의 콘텐츠 위치입니다. |
   | **전자 메일 주소** | [!DNL Dynamic Media Classic]&#x200B;([!DNL Scene7])에 로그인하는 데 사용되는 전자 메일 주소입니다. |
   | **암호** | [!DNL Dynamic Media Classic]&#x200B;([!DNL Scene7])에 로그인하는 데 사용되는 암호입니다. |

   ![Scene7 구성 필드](/help/main/administrating-target/assets/scene7-1.png)

1. **[!UICONTROL 제출]**&#x200B;을 클릭합니다.
