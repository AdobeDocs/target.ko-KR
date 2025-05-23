---
keywords: 다변량 테스트;mvt;mvt 계획;다변량 테스트 계획
description: 성공적인 테스트를 만들 수 있도록  [!DNL Adobe Target] 에서 [!UICONTROL Multivariate Test]을(를) 계획하는 방법을 알아봅니다.
title: '[!UICONTROL Multivariate Test]을(를) 계획하려면 어떻게 해야 합니까?'
feature: Multivariate Tests
exl-id: 130718d5-7bd9-4b1a-b81a-7a146f0ffd0d
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 64%

---

# [!UICONTROL Multivariate Test] 계획

성공적인 테스트를 만들려면 [!DNL Adobe Target]의 MVT([!UICONTROL Multivariate Tests]) 활동에 몇 가지 계획을 세워야 합니다.

MVT에는 유용한 결과를 얻기에 충분한 트래픽이 필요합니다. 테스트를 설정하기 전에, 노출 수 및 전환 수를 비롯하여 사이트에 일반적으로 수신되는 트래픽의 양을 알아야 합니다. 이 정보를 사용하면 사이트의 트래픽을 초과하는 요구 사항을 사용하여 테스트를 디자인할 가능성을 줄이는 데 도움이 됩니다.

요소는 서로 독립적입니다. 예를 들어 동일한 테스트에서 레이아웃과 콘텐츠를 테스트하지 마십시오.

테스트할 페이지의 HTML 코드를 검사합니다. 사이트의 HTML 요소에 DOM ID가 중복되지 않아야 합니다. ID가 중복되면 동일한 콘텐츠가 여러 위치에 전달될 수 있습니다.

유효한 결과를 생성할 가능성이 있는 페이지의 요소를 테스트하도록 계획합니다. 예를 들어 배너 또는 영웅 이미지는 바닥글을 변경하여 더 많은 전환이 발생될 수 있습니다. 영향력이 적은 요소를 테스트에 포함하면 페이지에서 더 중요한 요소를 테스트하는 데 필요한 트래픽과 시간만 늘어날뿐입니다.

마지막으로, 테스트를 만들기 전에 테스트할 콘텐츠를 만들어야 합니다. 각 오퍼의 콘텐츠 차이점을 파악하고 테스트에 사용할 이미지, 텍스트, HTML 오퍼를 만듭니다.

## 교육 비디오: 다변량 테스트 만들기(9:25) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에서는 안내가 있는 [!DNL Target] 3단계 워크플로우를 사용하여 다변량 테스트를 계획하고 만드는 방법을 보여 줍니다.

* 다변량 테스트 정의 및 디자인
* 다변량 테스트 만들기

>[!VIDEO](https://video.tv.adobe.com/v/30528?captions=kor)
