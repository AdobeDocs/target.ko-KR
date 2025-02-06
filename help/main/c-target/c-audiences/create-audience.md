---
keywords: 대상자;대상자 규칙;대상자 만들기;대상자 생성
description: 사용자 지정된 대상을 만들고 활동에 사용할 수 있도록  [!DNL Adobe Target] [!UICONTROL Audiences] 라이브러리에 저장하는 방법에 대해 알아봅니다.
title: 대상을 만들려면 어떻게 합니까?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: 19d2b14f137fe4dbf95e9f9f9b84f80b93d1e281
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 48%

---

# [!DNL Target]에서 대상 작성

사용자 지정된 대상을 만들고 활동에서 사용할 수 있도록 [!DNL Adobe Target] [!UICONTROL Audiences] 라이브러리에 저장합니다. 기존 대상을 복사한 다음 편집하여 유사한 대상을 만들고 여러 대상을 결합할 수도 있습니다.

## 대상자 개요

대상자는 [!DNL Target] 활동에서 포함되거나 제외되는 사용자를 결정하는 규칙으로 정의됩니다. 대상 정의에는 여러 규칙이 포함될 수 있으며 각 규칙에는 여러 매개 변수가 포함될 수 있습니다. 복잡한 대상 정의는 부울 연산자 AND 및 OR로 규칙과 매개 변수를 결합하여 활동 참여자로 카운트되는 사이트 방문자를 보다 자세히 제어할 수 있습니다.

규칙이나 매개 변수를 AND와 결합하면 잠재적 대상 구성원은 참여자로 포함할 *모두*&#x200B;에 정의된 조건을 충족해야 합니다. 예를 들어, OS 규칙 AND 브라우저 규칙을 정의하는 경우 정의된 OS *와* 정의된 브라우저 둘 다를 사용하는 방문자만 활동에 포함됩니다.

규칙 또는 매개 변수를 OR로 결합하면 잠재적인 모든 대상 멤버가 참여자로 포함되기 위해 정의된 조건 하나만 만족하면 됩니다. 예를 들어, OR로 연결된 여러 개의 모바일 규칙을 정의하는 경우 정의된 기준을 *하나라도* 충족하는 방문자가 활동에 포함됩니다.

두 부울 연산자를 혼합하여 복합 규칙을 만들 수 있지만 동일한 규칙 수준의 연산자가 일치해야 합니다. 사용자 인터페이스는 올바른 연산자를 자동으로 적용합니다.

예를 들어, 다음 규칙은 [!DNL Windows] 컴퓨터에서 [!DNL Chrome] *또는* [!DNL Firefox]을(를) 사용하는 방문자를 타깃팅합니다.

![대상자 만들기](assets/audience_create.png)

>[!NOTE]
>
>모든 잠재적 대상자 구성원을 제외하는 규칙을 작성하지 않도록 주의하십시오. 예를 들어 [!DNL Chrome] *및* [!DNL Firefox]을(를) 동시에 사용하여 다른 사용자가 페이지를 방문할 수는 없습니다.

## 대상자 만들기

1. 상단 메뉴 모음에서 **[!UICONTROL Audiences]**&#x200B;을(를) 클릭합니다.

   ![audiences_list 이미지](assets/audiences_list.png)

1. [!UICONTROL Audiences] 목록에서 **[!UICONTROL Create Audience]**&#x200B;을(를) 클릭합니다.

   또는

   기존 대상을 복사하려면 [!UICONTROL Audiences] 목록에서 복사할 대상에 대해 **[!UICONTROL More Actions]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallListVert.svg))을 클릭한 다음 **[!UICONTROL Duplicate]**&#x200B;을(를) 클릭합니다. 그러면 대상자를 편집하여 유사한 대상자를 만들 수 있습니다.

1. 고유한 설명 대상 이름과 설명(선택 사항)을 입력합니다.

   대상 이름은 다음 문자로 시작할 수 없습니다.

   `=  +  -  !  @`

   대상 이름에는 다음 문자 시퀀스를 사용할 수 없습니다.

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. 왼쪽의 **[!UICONTROL Attributes]** 목록에서 원하는 특성을 대상 빌더 창으로 끌어다 놓습니다.

   ![특성 드래그 앤 드롭](assets/drag-attribute.png)

   각 규칙 유형에는 고유한 매개 변수가 있습니다. 각 대상 규칙 유형을 구성하는 방법에 대한 자세한 내용은 [대상 범주](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D)를 참조하십시오.

1. 규칙 매개 변수를 정의합니다.

   예를 들어 다음 대상은 [!DNL Macintosh] 운영 체제를 사용하는 유타 지역 방문자를 타깃팅합니다.

   ![유타/Macintosh 대상](assets/adience-builder.png)

1. (조건부) 원하는 속성을 계속 추가하고 정의합니다.

   다른 컨테이너를 만들려면 **[!UICONTROL Add container]**&#x200B;을(를) 클릭하거나 다른 특성을 Audience Builder 창으로 끌어다 놓습니다. 그런 다음 드롭다운 목록을 사용하여 연산자(AND 또는 OR)를 조정할 수 있습니다.

1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

   새로 만든 대상이 몇 초 동안 처리가 지연된 후에 목록에 표시됩니다. 대상이 목록에 즉시 표시되지 않는 경우 대상을 검색하거나 목록을 새로 고치십시오.

## 교육 비디오: 대상 만들기 ![개요 배지](/help/main/assets/overview.png)

이 비디오에는 대상을 만드는 방법에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
