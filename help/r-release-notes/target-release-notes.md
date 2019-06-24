---
description: 이러한 릴리스 노트는 최신 또는 예정된 타겟 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트
seo-description: 이러한 릴리스 노트는 최신 또는 예정된 Adobe Target 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다
seo-title: Adobe Target 릴리스 노트 (베타 버전)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: bc44fd95263e7f2ad22e556a07468c9d7ed3ba8c

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트: 2019년 6월 25일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target Standard/Premium 19.6.1(2019년 6월 26일) {#tgt-19-6-1}

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 기능 / 개선 사항 | 설명 |
| --- | --- |
| 시각적 경험 작성기(VEC) | **새 VEC 메뉴 옵션**: vec에서 페이지 요소를 클릭하면 메뉴에 해당 요소 유형에 사용할 수 있는 옵션이 표시됩니다.<ul><li>You can now use the [!UICONTROL Styles &gt; Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**클릭 추적 개선** 사항: VEC 및 SPA (Single Page Application) VEC 내에서 클릭 추적을 구성하는 과정을 개선했습니다.<ul><li>클릭 추적에서 사용할 요소를 선택할 때 사용 가능한 모든 요소의 이름이 오른쪽의 수정 패널에 표시되므로 원하는 요소를 빠르고 손쉽게 선택할 수 있습니다.</li><li>The [!UICONTROL Goals &amp; Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. 이 숫자 위로 마우스를 가져가면 선택한 모든 요소의 이름이 표시됩니다. (TGT-33878)</li></ul>See [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md). |
| SPA VEC(Single Page App Visual Experience Composer) | **가이드 워크플로우**: 새로운 안내 워크플로우는 단일 페이지 앱에 대해 활동을 실행하고 실행하는 페이지 배달 규칙 설정을 구성하는 방법을 이해하는 데 도움이 됩니다. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**복제 수정** 사항: 이제 SPA VEC를 사용하여 수정 사항을 정의한 다음 단일 페이지 앱에서 다른 보기에 사용하기 위해 해당 수정 내용을 복제할 수 있습니다. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md). |
| 모바일 시각적 경험 작성기 | **다양한 앱 버전**: 이제 여러 버전의 모바일 앱용 활동을 제작할 수 있습니다. 따라서 버전이 유사하고 앱의 UI를 크게 변경할 필요가 없을 때 시간과 노력을 절약할 수 있습니다. (TGT-34231) |
| ![프리미엄 배지](/help/assets/premium.png) 자동 개인화 (AP) 및 자동 타깃팅 | **제어 기능**: AP 또는 자동 타겟 활동을 만드는 동안 컨트롤로 사용할 경험을 선택할 수 있습니다. 이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대한 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다. 현재 제어 옵션 (임의로 제공된 경험) 는 계속 사용할 수 있습니다. (TGT-32801 &amp; TGT-26572)<br>**Personalization Insights reports**: The marketer-friendly naming for attributes when a visitor sees a specific piece of content in a specific location provides more meaningful information. (TGT-33326 및 TGT-34957) |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
