---
keywords: 다변량 테스트;문제 해결;mvt
description: Adobe Target에서 MVT(다변량 테스트) 활동을 제안되는 솔루션과 함께 사용하여 발생할 수 있는 잠재적인 어려움에 대해 탐색합니다.
title: 다변량 테스트 문제는 어떻게 해결합니까?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 42%

---

# 다변량 테스트 문제 해결

이 주제에는 디자인 시 발생할 수 있는 몇 가지 문제를 해결하기 위한 제안 사항이 포함되어 있습니다 [!UICONTROL 다변량] 의 (MVT) 테스트 [!DNL Adobe Target].

* 활동을 편집할 때 [!DNL Analytics]-기반 지표와 보고서 세트가 로드되지 않음(spinner display) 지표를 [!DNL Target] 지표를 만든 다음 [!DNL Analytics]기반 지표. 이제 보고서 세트가 로드됩니다.
* 이미 실행 중인 테스트를 변경하면 테스트 및 해당 데이터를 재설정할 수 있습니다.

   [!DNL Target] 라이브 활동을 편집할 수 있습니다. 진행 중인 활동을 편집하면 테스트가 재설정될 수 있으므로 보고서에서 일부 변경 사항이 인식되지 않을 수 있습니다.

   기존 텍스트 또는 html 오퍼 편집 등과 같은 간단한 변경을 수행하는 것이 안전합니다.

   경험 이름 및 보고서를 재설정하는 특정 작업은 다음과 같습니다.

   * 새 위치 추가
   * 위치 삭제
   * 새 오퍼 추가 또는 기존 위치에서 오퍼 삭제
