---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Adobe Target은 Adobe Dynamic Media Classic과 통합하여 콘텐츠 라이브러리에 디지털 자산 관리(DAM)를 제공할 수 있습니다.
title: Dynamic Media Classic 통합 구성 통합
feature: administration general
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 18%

---


# Scene7 구성 {#scene-settings}

[!DNL Target] 을 컨텐츠 라이브러리 [!DNL Adobe Dynamic Media Classic] 에서 디지털 자산 관리(DAM)를 제공하기 위해 [!UICONTROL 와 통합할 수 있습니다].

>[!NOTE]
>
>[!DNL Target]과 [!DNL Dynamic Media Classic]을(를) 통합하면 [!DNL Adobe Experience Cloud] 자산 폴더에 업로드된 자산(활동의 일부)을 전달할 수 있습니다. 이 통합은 [!DNL Dynamic Media Classic]에 업로드된 모든 자산에 대한 액세스를 [!DNL Target] 활동에 제공할 수 있도록 활성화하지 않습니다.

이미 [!DNL Dynamic Media] 계정이 있는 경우 기존 자격 증명을 제공할 수 있습니다. 계정이 없는 경우 [!DNL Adobe] 담당자의 추가 비용 없이 제한된 사용 [!DNL Dynamic Media Classic] 계정을 요청할 수 있습니다. 이 계정은 [!DNL Target]에서만 사용하도록 제한된 목적으로만 사용할 수 있습니다. 이 서비스는 이미지 대체 기능이 필요한 워크플로우의 고객이 사용할 수 있습니다.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

이 설정이 구성되지 않으면 활동 만들기 작업 과정 내에서 [!UICONTROL 이미지 교체 오퍼] 옵션을 사용할 수 없습니다. 이 설정이 구성되면 이미지 오퍼를 교체/변경하는 옵션을 [VEC(Visual Experience Composer)와 양식 기반 경험 작성기](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)에서 모두 사용할 수 있습니다. 그런 다음 [!DNL Adobe Experience Cloud]에서 업로드된 이미지가 있는 이미지 오퍼를 사용하여 [!DNL Target] 활동에 사용할 수 있습니다.

활동 생성 중에 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 사용자 고유의 웹 서버에 배포하고 코드에서 자체 URL을 사용해야 합니다. [!DNL Target]을(를) 사용하여 타깃팅 워크플로의 직접 또는 외부에서 사용하도록 [!DNL Experience Cloud]에 업로드된 이미지의 게시된 URL을 가져올 수 있는 방법은 없습니다. 이 기능이 계약에 따라 허용되지는 않습니다.

[!DNL Dynamic Media]의 저장소 URL과 이미지의 최종 게시 URL은 서로 다르며, *NOT*&#x200B;에서 이미지 저장소 링크를 사용하여 오퍼를 만들어야 하는 경우 배달이 작동하지 않습니다. 도움말 설명서에 설명된 대로 이미지 오퍼 기능을 사용해야 합니다.

[!DNL Dynamic Media Classic]([!DNL Scene7])과 통합하려면 다음 정보를 지정해야 합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL Scene7 구성]**&#x200B;을 클릭합니다.

   ![Scene7 페이지](/help/administrating-target/assets/scene7.png)

1. 다음 [!DNL Dynamic Media Classic] 계정 정보를 지정합니다.

   **지역**[!DNL Dynamic Media]:  계정의 지역: 북미, 유럽 또는 아시아.

   **임시 폴더:** 대상 폴더 외부에 있고 수동으로 업로드되는 컨텐츠의  [!DNL Dynamic Media]위치입니다.

   **이메일 주소:** 로그인하는 데 사용되는 이메일  [!DNL Dynamic Media Classic] ([!DNL Scene7])입니다.

   **암호:** 로그인하는 데 사용되는  [!DNL Dynamic Media Classic] ([!DNL Scene7]) 암호입니다.

1. **[!UICONTROL 제출을 클릭합니다]**.
