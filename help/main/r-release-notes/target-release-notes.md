---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cd25bda52b7a1b916a73ca5e531a7134ba8cef4e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 43%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 일자: 2025년 4월 17일 금요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target Standard/Premium] 25.4.4(2025년 4월 17일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 활동에서 중복 옵션을 확인하는 방법을 사용자에게 안내하는 오류 메시지를 추가했습니다. (TGT-51927)
* 리디렉션 오퍼가 있는 페이지 또는 경험을 삭제할 때 `ClickTrack` 선택기가 제거되지 않았던 문제를 수정했습니다. (TGT-51952)
* 빈 `ClickTrack` 선택기를 허용하여 발생하는 문제를 해결했습니다. 이제 [!DNL Target]을(를) 사용하려면 선택기 필드가 비어 있지 않아야 합니다. (TGT-52107)
* 중복 이름이 있는 지표를 잘못 허용하는 문제가 수정되었습니다. 이제 지표에 고유한 이름이 필요합니다. (TGT-52201)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 오퍼 수준 타깃팅을 편집할 때 대상 정의가 표시되지 않던 문제를 수정했습니다. (TGT-52148)
* [!UICONTROL Editor] 권한이 있는 고객이 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-52227)
* 옵션이 변경되지 않은 상태로 유지되면 `OptionLocalIDs`이(가) 더 이상 잘못 증가하지 않습니다. (TGT-52139)
* 활동을 만들려고 할 때 &quot;잘못된 `optionLocalIds`&quot; 메시지가 표시되는 문제를 해결했습니다. (TGT-52154)
* 활동에 대해 정의된 `OptionLocalIDs`과(와) 경험을 정의하는 데 사용된  간의 불일치가 수정되었습니다. (TGT-52215)
* A/B 활동을 만들려고 할 때 유효성 검사 오류가 발생하는 문제를 해결했습니다. (TGT-51923)

## 타겟 권한 업데이트(2025년 4월 22일)

이 향후 업데이트는 [!DNL Target] 인스턴스 구성에 대한 조직의 제어를 강화하여 다양한 테스트 및 개인화 팀의 활동 전달에 영향을 줄 수 있는 우발적인 업데이트를 방지합니다.

2025년 4월 22일부터 [!DNL Target] 작업 영역의 역할에 관계없이 [!UICONTROL Product] 및 [!UICONTROL Solutions] 관리자만 [!UICONTROL Administration] 섹션의 설정을 업데이트할 수 있습니다. 이 권한이 없는 사용자는 [!UICONTROL Administration] 섹션에 대한 읽기 전용 액세스 권한을 갖게 됩니다.

자세한 내용은 [Target 관리](/help/main/administrating-target/start-target.md)를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
