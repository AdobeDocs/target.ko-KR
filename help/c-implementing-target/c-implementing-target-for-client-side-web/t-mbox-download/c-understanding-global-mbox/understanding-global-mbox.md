---
keywords: 글로벌 mbox;at.js 구현
description: ' [!DNL Target] 구현에서 각 웹 페이지의 맨 위에서 수행된 단일 서버 호출을 참조하는 데 사용되는 이름인 Adobe Target의 글로벌 mbox에 대해 알아봅니다.'
title: 글로벌 mbox란?
feature: at.js
role: Developer
exl-id: 84d15feb-f5df-4879-ae35-a7f455c1b20f
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 82%

---

# 글로벌 mbox 이해

[!DNL Adobe Target] 구현에서 각 웹 페이지의 맨 위에서 수행된 단일 서버 호출을 참조하는 데 사용되는 이름인 글로벌 mbox에 대한 정보입니다.

기본적으로 글로벌 mbox에는 `target-global-mbox`라는 이름이 지정됩니다. 필요한 경우 이 이름을 해당 계정용으로 바꿀 수 있습니다.

일반 mbox(비글로벌 mbox)와 글로벌 mbox 사이에는 다음과 같이 몇 가지 차이점이 있습니다.

| 일반 mbox | 글로벌 mbox |
|--- |--- |
| 일반 mbox는 일반적으로 컨텐츠를 `<DIV>` 태그로 둘러싸고 있습니다. | 글로벌 mbox는 &quot;비어 있는&quot; 상태이며 컨텐츠를 둘러싸지 않습니다. |
| 한 활동의 컨텐츠만 일반 mbox에서 전달할 수 있습니다. | 여러 활동의 컨텐츠를 글로벌 mbox에 대한 하나의 응답으로 전달할 수 있습니다. |

여러 활동이 글로벌 mbox 또는 여러 일반 mbox를 통해 전달되는 경우 [!DNL Target]에서는 [활동이 웹 페이지에 전달되는 우선순위를 결정](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F)합니다.

추가적인 페이지 수준 데이터를 [!DNL Target] 함수를 사용하여 글로벌 mbox와 함께 `targetPageParams`에 전송할 수 있습니다. 이것은 mbox 매개 변수 기능과 비슷합니다. 자세한 내용은 [글로벌 Mbox에 매개 변수 전달](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5)을 참조하십시오.
