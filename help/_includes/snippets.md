---
source-git-commit: 87c0d2aa67d54dcbc2963be63d2d7ad9c02b6aa9
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 5%
---
# 스니펫

## Target Premium 기능 {#premium-note}

>[!NOTE]
>
>이 기능은 [Target Premium](/help/main/c-intro/intro.md#premium)라이선스의 일부로 제공됩니다. 이 기능은 [!DNL Target Standard]에서 사용할 수 없습니다.

## Target 권한 업데이트 {#permissions-update}

>[!IMPORTANT]
>
>[!UICONTROL 제품 관리자] 및 [!UICONTROL 시스템 관리자] 권한이 있는 [!DNL Target] 사용자는 [!DNL Target]의 역할에 관계없이 [!UICONTROL 관리] 페이지에서 모든 설정을 편집할 수 있습니다. 이러한 권한이 없는 사용자는 이러한 설정에 대해 읽기 전용 액세스 권한을 갖습니다.

## Target UI가 업데이트됨 {#updated-ui}

>[!NOTE]
>
>2025년에 새로 도입된 [!DNL Target]에서는 업데이트된 UI와 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)를 도입했습니다. 자세한 내용을 보려면 다음 링크를 클릭하십시오.
>
>* [[!DNL Target Standard/Premium] 25.2.1(2025년 2월 17일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): [!UICONTROL 활동], [!UICONTROL 권장 사항] 및 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
>
>* [[!DNL Target Standard/Premium] 25.1.1(2025년 1월 9일) 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): [!UICONTROL 오퍼 라이브러리]에 대한 [!DNL Target]의 주요 UI 변경 사항에 대한 요약을 제공합니다.
>
>* [UI 이해 [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): [!DNL Target]에 익숙해지는 데 도움이 되는 간단한 개요를 제공하고 자세한 정보와 단계별 지침을 제공하는 링크를 제공합니다.
>
>* [[!UICONTROL 시각적 경험 작성기] 변경 사항](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): [!DNL Adobe Target Standard/Premium] 25.2.1 릴리스(2015년 2월 17일)에서는 업데이트된 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)를 도입했습니다. 이 문서에서는 VEC의 기존 버전과 업데이트된 버전의 차이점에 대해 설명합니다.
>
>* [[!UICONTROL 시각적 경험 작성기] 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): 이 문서에서는 업데이트된 VEC UI 및 해당 옵션에 대해 설명합니다.
>
>* [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md): 이 FAQ는 탐색 변경, 기능 위치 및 임시 UI 버전 전환 중단 등 새 [!DNL Target] UI 및 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)에 대한 일반적인 질문을 해결합니다. 마케터, 개발자 또는 관리자이든, 이 FAQ는 원활하게 전환하고 업데이트된 UI를 최대한 활용하는 데 도움이 됩니다.

## 활동 이름 규칙 {#activity-name-rules}

활동 이름은 `=`, `+`, `-` 또는 `@`(으)로 시작할 수 없습니다. 활동 이름에는 문자 시퀀스 `;=`, `;+`, `;-`, `;@`, `,=`, `,+`, `,-`, `,@`, `["` 또는 `"]`도 포함될 수 없습니다.

## 타깃팅 단계에서 대상 선택 {#audience-selection-steps}

1. 대상을 변경하려면 오른쪽 프레임에서 **[!UICONTROL 바꾸기]** 아이콘(![바꾸기 아이콘](/help/main/assets/icons/Retweet.svg))을 클릭하십시오.

1. **[!UICONTROL 대상 추가]** 대화 상자에서 [원하는 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)한 다음 **[!UICONTROL 대상 할당]**&#x200B;을 클릭합니다.

   여러 대상을 결합하는 대상을 만들려면 **[!UICONTROL 대상 결합]**&#x200B;을 클릭합니다. 자세한 내용은 [여러 대상 결합](/help/main/c-target/combining-multiple-audiences.md)을 참조하십시오.

   [!UICONTROL 대상 라이브러리]에 없는 새 대상을 만들려면 **[!UICONTROL 대상 만들기]**&#x200B;를 클릭하십시오. [대상자 만들기 워크플로](/help/main/c-target/c-audiences/audiences.md)에서 다음 옵션 중 하나를 선택하십시오.

   * **[!UICONTROL 대상 라이브러리]**: [!UICONTROL 대상 라이브러리]에 저장되고 다른 활동에서 다시 사용할 수 있는 온디맨드 대상을 만듭니다.
   * **[!UICONTROL 이 활동만]**: [!UICONTROL 대상 라이브러리]에 저장되지 않고 현재 활동에서만 사용할 수 있는 [활동별 대상을 만듭니다](/help/main/c-target/creating-activity-only-audience.md).

1. 오른쪽 프레임에서 **[!UICONTROL 방문자 비율]**&#x200B;을 클릭한 다음 활동을 시작할 자격 있는 방문자의 비율을 선택합니다.


