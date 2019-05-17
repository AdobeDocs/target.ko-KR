---
description: Target Standard는 컨텐츠 라이브러리에서 DAM(디지털 자산 관리)을 제공하기 위해 Adobe Scene7과 통합될 수 있습니다.
seo-description: Target Standard는 컨텐츠 라이브러리에서 DAM(디지털 자산 관리)을 제공하기 위해 Adobe Scene7과 통합될 수 있습니다.
seo-title: Scene7 설정
solution: Target
subtopic: 시작하기
title: Scene7 설정
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Scene7 설정{#scene-settings}

Target Standard는 컨텐츠 라이브러리에서 DAM(디지털 자산 관리)을 제공하기 위해 Adobe Scene7과 통합될 수 있습니다.

>[!NOTE]
>
>Target을 Scene7과 통합하여 업로드된 자산(활동의 일부)을 Adobe Experience Cloud 자산 폴더로 전달할 수 있습니다. 이렇게 통합한다고 해서 Target 활동에서 전달하기 위해 Scene7에 업로드된 모든 자산에 액세스할 수 있는 것은 아닙니다.

Scene7 계정이 있는 경우 Scene7 자격 증명을 제공할 수 있습니다. Scene7 계정이 없는 경우 Target 계정 전용 무료 Scene7 계정으로 이 기능을 구성할 수 있는 Adobe 담당자에게 문의하십시오. 이 계정은 Target용으로만 제한된 용도로 사용할 수 있습니다. 이 서비스는 이미지 대체 기능이 필요한 워크플로우의 고객이 사용할 수 있습니다.

이 설정이 구성되지 않은 경우, 활동 생성 워크플로우 내에서 이미지 오퍼 대체 옵션을 사용할 수 없습니다. 이 설정을 구성한 후에는 이미지 오퍼를 대체/변경하기 위한 옵션을 [VEC(시각적 경험 작성기) 및 양식 기반 경험 작성기](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) 둘 다에서 사용할 수 있습니다. 그런 다음, Target 활동에서 사용할 수 있도록 Adobe Experience Cloud에서 업로드한 이미지와 함께 이미지 오퍼를 활용할 수 있습니다.

활동 생성 중에 오퍼 또는 사용자 지정 코드에서 직접 공개 이미지 URL을 참조하려면 이미지를 사용자 고유의 웹 서버에 배포하고 코드에서 자체 URL을 사용해야 합니다. Experience Cloud에 업로드된 이미지의 게재된 URL을 획득한 후 직접 사용하거나, Adobe Target을 사용하여 타깃팅 워크플로우 외부에서 사용할 수 있는 방법은 없습니다. 이 기능이 계약에 따라 허용되지는 않습니다.

이미지의 스토리지 URL과 최종 Scene7 공개 URL은 다르며, 이러한 경우에는 전달이 작동하지 않으므로 이미지의 스토리지 링크를 사용하여 오퍼를 만들지 않아야 합니다. 도움말 설명서에 설명된 대로 이미지 오퍼 기능을 사용해야 합니다.

Scene7과 통합하려면 일부 Scene7 정보를 지정해야 합니다.

1. **[!UICONTROL 설정]** &gt; **[!UICONTROL Scene7 설정]**을 클릭합니다.
1. 다음 Scene7 계정 정보를 지정하십시오. 

   **Scene7 지역:** Scene7의 계정의 지역: 북미, 유럽 또는 아시아

   **Scene7 애드혹 폴더:** 대상 폴더 외부에 있고 Scene7에 수동으로 업로드되는 컨텐츠의 위치입니다.

   **Scene7 이메일 주소:** Scene7에 로그인하는 데 사용되는 이메일 주소입니다.

   **Scene7 암호:** Scene7에 로그인하는 데 사용되는 암호입니다.
1. **[!UICONTROL 제출을 클릭합니다]**.
