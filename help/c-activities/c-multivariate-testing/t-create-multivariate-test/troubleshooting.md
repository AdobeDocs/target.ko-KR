---
keywords: Mobile Web Experience Editor
description: 이 항목에서는 Adobe Target에서 MVT 테스트를 디자인할 때 발생할 수 있는 일부 문제를 해결하기 위한 제안을 제공합니다.
title: 다변량 테스트 문제 해결
feature: mvt
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 77%

---


# 다변량 테스트 문제 해결{#troubleshoot-multivariate-tests}

이 항목에서는 Adobe Target에서 MVT 테스트를 디자인할 때 발생할 수 있는 일부 문제를 해결하기 위한 제안을 제공합니다.

* 활동을 편집할 때 Analytics 기반 지표를 사용하며 보고서 세트가 로드되지 않는 경우(회전기 표시) 해당 지표를 Target 지표로 전환한 다음, 다시 Analytics 기반 지표로 전환하십시오. 이제 보고서 세트가 로드됩니다.
* 이미 실행 중인 테스트를 변경하는 경우 테스트 및 해당 데이터를 재설정할 수 있습니다.

   Target에서는 라이브 활동을 편집할 수 있습니다. 진행 중인 활동을 편집하면 테스트가 재설정될 수 있으므로 보고서에서 일부 변경 사항이 인식되지 않을 수 있습니다.

   기존 텍스트 또는 html 오퍼 편집 등과 같은 간단한 변경을 수행하는 것이 안전합니다.

   경험 이름 및 보고서를 재설정하는 특정 작업은 다음과 같습니다.

   * 새 위치 추가
   * 위치 삭제
   * 새 오퍼 추가 또는 기존 위치에서 오퍼 삭제

