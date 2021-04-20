---
keywords: 구현;구현;설정;사용자 특성
description: 고객 특성을 활용하여 데이터를 Target으로 가져올 수 있습니다.
title: 고객 속성을 사용하여 데이터를 Target으로 가져오려면 어떻게 해야 합니까?
feature: Implementation
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 51%

---

# 고객 속성

고객 속성을 사용하여 FTP를 통해 방문자 프로필 데이터를 [!DNL Adobe Experience Cloud]에 업로드할 수 있습니다. 업로드되면 [!DNL Adobe Analytics] 및 [!DNL Adobe Target]의 데이터를 사용합니다.

Target Standard 고객은 5개의 속성을 적용할 수 있으며, Target Premium 고객은 200개의 속성을 적용할 수 있습니다.

## 형식

Experience Cloud ID(ECIDs) 및 속성 이름/값 쌍이 있는 .csv 파일은 FTP를 통해 업로드되거나 Experience Cloud UI에서 수동으로 업로드됩니다.

## 활용 사례 예

CRM 또는 기타 내부 시스템은 Target 및 Analytics를 포함하여 Adobe의 Experience Cloud와 공유하려는 중요 정보를 저장합니다.

## 방법의 이점

고객 데이터를 업로드하면 Target에 방문자가 아직 표시되지 않은 경우에도 Target에서 해당 방문자에 대한 프로필 항목이 만들어집니다.

동일한 데이터를 Target 및 Analytics에서 자동으로 사용할 수 있습니다.

FTP는 API보다 간단한 구현 방법일 수 있습니다.

## 주의 사항

Target Standard 고객은 5개의 속성을 적용할 수 있으며, Target Premium 고객은 200개의 속성을 적용할 수 있습니다

페이지에서가 아니라 고객 속성을 통해서만 값을 업데이트할 수 있습니다.

Experience Cloud ID(ECID) 구현이 필요합니다.

## 코드 예제

자세한 내용은 [고객 속성 소스를 만들고 데이터 파일](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html)에 업로드하십시오.

### 관련 정보에 대한 링크

[고객 속성 소스를 만들고 데이터 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
