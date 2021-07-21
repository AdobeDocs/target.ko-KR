---
keywords: scene7;dynamic media classic;디지털 에셋 관리;에셋;dam;콘텐츠 라이브러리;이미지 교환
description: Adobe [!DNL Target] 를 Adobe Dynamic Media Classic(이전 Scene7)과 통합하여 콘텐츠 라이브러리에서 DAM(디지털 에셋 관리)을 제공하는 방법에 대해 알아봅니다.
title: Dynamic Media Classic(Scene7) 통합을 구성하는 방법은 무엇입니까?
feature: 관리 및 구성
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: ht
source-wordcount: '404'
ht-degree: 100%

---

# Dynamic Media Classic(이전 Scene7) 구성

[!DNL Adobe Target]를 [!DNL Adobe Dynamic Media Classic](이전 [!DNL Scene7])과 통합하여 [!UICONTROL 콘텐츠 라이브러리]에서 DAM(디지털 에셋 관리)을 제공할 수 있습니다.

>[!NOTE]
>
>[!DNL Target]를 [!DNL Dynamic Media Classic]와 통합하여 [!DNL Adobe Experience Cloud] 에셋 폴더에 업로드된 에셋을 (활동의 일부로) 전달할 수 있습니다. 이 통합은 [!DNL Target] 활동의 전달을 위해 [!DNL Dynamic Media Classic]에 업로드된 모든 에셋에 대한 액세스를 제공하지 않습니다.

이미 [!DNL Dynamic Media] 계정이 있는 경우 기존 자격 증명을 사용할 수 있습니다. 계정이 없는 경우 [!DNL Adobe] 담당자에게 추가 비용 없이 사용 제한 [!DNL Dynamic Media Classic] 계정을 요청할 수 있습니다. 이 계정은 [!DNL Target]에서 제한된 용도로만 사용할 수 있습니다. 이 서비스는 이미지 대체 기능이 필요한 워크플로의 고객이 사용할 수 있습니다.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

이 설정이 구성되지 않은 경우 활동 생성 워크플로 내에서 [!UICONTROL 이미지 대체 오퍼] 옵션을 사용할 수 없습니다. 이 설정이 구성되면 [시각적 경험 작성기(VEC) 및 양식 기반 경험 작성기](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) 모두에서 이미지 오퍼를 대체/변경하는 옵션을 사용할 수 있습니다. 그런 다음 [!DNL Target] 활동에 사용하기 위해 [!DNL Adobe Experience Cloud]에서 업로드된 이미지와 함께 이미지 오퍼를 활용할 수 있습니다.

활동 생성 중에 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 사용자 고유의 웹 서버에 배포하고 코드에서 자체 URL을 사용해야 합니다. [!DNL Target]을(를) 사용하여 직접 또는 대상 워크플로 외부에서 사용하기 위해 [!DNL Experience Cloud]에 업로드된 이미지의 게시된 URL을 가져올 수 없습니다. 이 기능이 계약에 따라 허용되지는 않습니다.

[!DNL Dynamic Media]의 이미지 저장 URL과 최종 게시 URL이 다르기 때문에 이미지 저장 링크를 사용하여 오퍼를 작성해서는 *안 됩니다*. 이러한 경우 전달이 작동하지 않습니다. 도움말 문서에 설명된 대로 이미지 오퍼 기능을 사용해야 합니다.

[!DNL Dynamic Media Classic]([!DNL Scene7])과 통합하려면 다음 정보를 지정해야 합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL Scene7 구성]**&#x200B;을 클릭합니다.

   ![Scene7 페이지](/help/administrating-target/assets/scene7.png)

1. 다음 [!DNL Dynamic Media Classic] 계정 정보를 지정합니다.

   **지역**[!DNL Dynamic Media]: 계정의 지역: 북미, 유럽 또는 아시아.

   **임시 폴더**: 대상 폴더 외부에 있고 수동으로 [!DNL Dynamic Media]에 업로드되는 콘텐츠의 위치입니다.

   **이메일 주소:** [!DNL Dynamic Media Classic]([!DNL Scene7])에 로그인할 때 사용되는 이메일 주소입니다.

   **암호:** [!DNL Dynamic Media Classic]([!DNL Scene7])에 로그인할 때 사용하는 암호입니다.

1. **[!UICONTROL 제출]**&#x200B;을 클릭합니다.
