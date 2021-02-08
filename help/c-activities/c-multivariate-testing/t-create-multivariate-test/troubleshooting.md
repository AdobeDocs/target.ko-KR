---
keywords: 다변수 테스트;문제 해결;문제 해결;mvt
description: 제안 솔루션과 함께 Adobe Target에서 MVT(Multivariate Test) 활동을 사용할 때 발생할 수 있는 잠재적인 문제를 살펴볼 수 있습니다.
title: 다변량 테스트 문제를 어떻게 해결합니까?
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 42%

---


# 다변량 테스트 문제 해결

이 항목에는 [!DNL Adobe Target]에서 [!UICONTROL Multivariate](MVT) 테스트를 디자인할 때 발생할 수 있는 일부 문제를 해결하기 위한 제안이 있습니다.

* 활동을 편집할 때 [!DNL Analytics] 기반 지표를 사용했는데 보고서 세트가 로드되지 않는 경우(스피너가 표시), 지표를 [!DNL Target] 지표로 전환한 다음 다시 [!DNL Analytics] 기반 지표로 전환합니다. 이제 보고서 세트가 로드됩니다.
* 이미 실행 중인 테스트를 변경하면 테스트 및 해당 데이터를 재설정할 수 있습니다.

   [!DNL Target] 라이브 활동을 편집할 수 있습니다. 진행 중인 활동을 편집하면 테스트가 재설정될 수 있으므로 보고서에서 일부 변경 사항이 인식되지 않을 수 있습니다.

   기존 텍스트 또는 html 오퍼 편집 등과 같은 간단한 변경을 수행하는 것이 안전합니다.

   경험 이름 및 보고서를 재설정하는 특정 작업은 다음과 같습니다.

   * 새 위치 추가
   * 위치 삭제
   * 새 오퍼 추가 또는 기존 위치에서 오퍼 삭제

