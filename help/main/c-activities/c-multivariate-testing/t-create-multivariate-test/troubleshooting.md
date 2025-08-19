---
keywords: 다변량 테스트;문제 해결;문제 해결;mvt
description: 제안된 해결 방법과 함께 [!UICONTROL Multivariate Test]에서  [!DNL Adobe Target](MVT) 활동을 사용하는 동안 발생할 수 있는 잠재적인 어려움에 대해 알아봅니다.
title: '[!UICONTROL Multivariate Test] 문제를 해결하려면 어떻게 합니까?'
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 22%

---

# [!UICONTROL Multivariate Test]개 활동 문제 해결

이 문서에는 [!UICONTROL Multivariate Test]에서 [!DNL Adobe Target]&#x200B;(MVT)을(를) 디자인할 때 발생할 수 있는 몇 가지 문제를 해결하기 위한 제안 사항이 포함되어 있습니다.

* 활동을 편집할 때 [!DNL Analytics] 기반 지표를 사용했지만 보고서 세트가 로드되지 않는 경우(회전식 표시) 지표를 [!DNL Target] 지표로 전환한 다음 [!DNL Analytics] 기반 지표로 다시 전환하십시오. 이제 보고서 세트가 로드됩니다.
* 이미 실행 중인 테스트를 변경하면 테스트와 해당 데이터를 재설정할 수 있습니다.

  [!DNL Target]을(를) 사용하면 라이브 활동을 편집할 수 있습니다. 진행 중인 활동을 편집하면 테스트가 재설정될 수 있으므로 보고서가 일부 변경 사항을 인식하지 못할 수 있습니다.

  기존 텍스트 또는 html 오퍼 편집 등과 같은 간단한 변경을 수행하는 것이 안전합니다.

  경험 이름 및 보고서를 재설정하는 특정 작업은 다음과 같습니다.

   * 새 위치 추가
   * 위치 삭제
   * 새 오퍼 추가 또는 기존 위치에서 오퍼 삭제
