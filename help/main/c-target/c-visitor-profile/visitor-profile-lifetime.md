---
keywords: 개요 및 참조
description: 방문자 프로필이  [!DNL Adobe Target]에 만료되는 시기에 대해 자세히 알아보세요.
title: 방문자 프로필 라이프타임이란 무엇이며 연장할 수 있습니까?
feature: Audiences
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
TQID: https://experienceleague.adobe.com/yMfacKgQthOmpfhFiuO-jGGPWZh5VrliOSi0TQ-uis0
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 62%

---

# 방문자 프로필 라이프타임

기본적으로 [!DNL Adobe Target]의 방문자 프로필은 해당 방문자가 14일 동안 활동하지 않으면 만료됩니다. 이 프로필 라이프타임은 연장할 수 있습니다.

[추가적인 비용 없이 프로필 라이프타임을 연장하려면 Client Care나 Adobe 컨설턴트](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에게 문의하십시오. 라이프타임은 90일 이내로 설정할 수 있습니다.

프로필이 기본값 이상으로 확장된 경우 새 [!DNL Platform Web SDK] 파일 또는 at.js 파일을 다운로드할 필요가 없습니다.

기존 프로필에 대한 만료 날짜는 재설정되지 않습니다. 15일 동안 이전 방문자가 다시 방문하지 않는다면 이 프로필은 만료됩니다. 원래의 2주 프로필이 만료되기 전에 이전 방문자가 재방문하는 경우 프로필은 연장된 라이프타임으로 재설정됩니다. 모든 새 방문자 프로필은 연장된 프로필 라이프타임으로 설정됩니다.
