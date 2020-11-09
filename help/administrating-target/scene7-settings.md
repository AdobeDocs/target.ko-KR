---
description: Target Standard를 Adobe Dynamic Media Classic과 통합하여 콘텐츠 라이브러리에서 DAM(Digital Asset Management)을 제공할 수 있습니다.
title: Dynamic Media Classic 통합 구성 통합
feature: administration general
subtopic: Getting Started
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 4e2e894ee10d8a83907e0533630091442d1733fa
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 17%

---


# Scene7 구성 {#scene-settings}

Target can be integrated with [!DNL Adobe Dynamic Media Classic] to provide Digital Asset Management (DAM) in the Content Library.

>[!NOTE]
>
>Integrating [!DNL Target] with [!DNL Dynamic Media Classic] enables delivery of assets (as part of activities) uploaded to the [!DNL Adobe Experience Cloud] assets folder. This integration does not enable access to all assets uploaded in [!DNL Dynamic Media Classic] for delivery in [!DNL Target] activities.

If you already have a [!DNL Dynamic Media] account, you can supply your existing credentials. If you do not have an account, you can request a restricted-use [!DNL Dynamic Media Classic] account at no additional charge from your [!DNL Adobe] representative. This account can be used for purposes restricted for use in [!DNL Target] only. 이 서비스는 이미지 대체 기능이 필요한 워크플로우의 고객이 사용할 수 있습니다.

>[!NOTE]
>
>Adobe Target에 대한 제한된 사용 무료 [!DNL Dynamic Media Classic] 계정은 신규 고객 또는 신규 사용자에게 더 이상 지원되지 않습니다. 기존 로그인 자격 증명은 평소대로 작동합니다.

If this setting is not configured, the [!UICONTROL Swap Image offer] option within the activity creation workflow is not available. 이 설정이 구성되면 VEC( [Visual Experience Composer)와 양식 기반 Experience Composer 모두에서 이미지 오퍼를 교체/변경하는 옵션을 사용할 수 있습니다](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). You can then leverage image offers with images that have been uploaded from the [!DNL Adobe Experience Cloud] for use in [!DNL Target] activities.

활동 생성 중에 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 사용자 고유의 웹 서버에 배포하고 코드에서 자체 URL을 사용해야 합니다. There is no way to obtain the published URL of an image uploaded into the [!DNL Experience Cloud] to consume directly or outside of targeting workflows using [!DNL Target]. 이 기능이 계약에 따라 허용되지는 않습니다.

Note that the storage URL and the final publish URLs of images from [!DNL Dynamic Media] are different and one must *NOT* create offers using the storage link of images as delivery will not work in such cases. 도움말 설명서에 설명된 대로 이미지 오퍼 기능을 사용해야 합니다.

To integrate with [!DNL Dynamic Media Classic] ([!DNL Scene7]), you need to specify the following information.

1. 관리 **** > **[!UICONTROL Scene7 구성을 클릭합니다]**.

   ![Scene7 페이지](/help/administrating-target/assets/scene7.png)

1. Specify the following [!DNL Dynamic Media Classic] account information:

   **지역**[!DNL Dynamic Media]:  계정의 지역: 북미, 유럽 또는 아시아.

   **임시 폴더:** 대상 폴더 외부에 있고 수동으로 업로드되는 콘텐트의 위치입니다 [!DNL Dynamic Media].

   **이메일 주소:** ( [!DNL Dynamic Media Classic] )에 로그인하는 데 사용되는 이메일[!DNL Scene7]주소입니다.

   **암호:** ( [!DNL Dynamic Media Classic] )에 로그인하는 데 사용되는[!DNL Scene7]암호입니다.

1. **[!UICONTROL 제출을 클릭합니다]**.
