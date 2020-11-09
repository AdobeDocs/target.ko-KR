---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;can't create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: 활동이 사이트에 나타나지 않는 경우 이 문제 해결 제안은 해결 방법을 찾는 데 도움이 될 것입니다.
title: 활동 문제 해결
feature: activities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 81%

---


# 활동 문제 해결{#troubleshoot-activities}

활동이 사이트에 나타나지 않는 경우 이 문제 해결 제안은 해결 방법을 찾는 데 도움이 될 것입니다.

>[!NOTE]
>
>다음 문제 해결 정보 외에 추가적인 문제 해결 주제, FAQ 및 [!DNL Adobe Target]에 있는 활동 및 기능의 문제 해결에 대한 기타 유용한 정보가 필요하면 연관 링크를 제공하는 [Target 문제 해결](/help/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839)을 참조하십시오.

다음 섹션은 추천 해결 방법에서 발생할 수 있는 문제를 포함합니다.

## Target UI를 사용하여 활동을 만들었지만 API를 통해 업데이트할 수 없습니다.

Target UI를 사용하여 만든 활동은 Target UI를 통해 업데이트해야 합니다. API를 통해 생성된 활동은 API를 통해 업데이트해야 합니다. 예를 들어, API를 사용하여 원래 활동을 만든 다음 나중에 Target UI를 통해 활동을 편집하는 경우 일부 변경 사항이 업데이트되지 않습니다. 모든 변경 사항은 백엔드에 저장되며 다른 API 호출을 수행하여 업데이트할 수 있습니다.

원래 활동을 만드는 데 사용한 동일한 방법(UI 또는 API)을 사용하여 활동을 업데이트하는 것이 좋습니다.

## 기본 컨텐츠가 표시됩니다.

활동이 완료되었고 활성화되었는지 확인하십시오.

## 활동이 라이브 상태가 아닙니다.

**유효성 검사:** 개요 탭으로 이동하여 테스트가 비활성 상태나 초안으로 표시되어 있는지 확인하십시오.

**옵션:**

* 테스트를 활성화합니다.
* 미리 보기 링크를 사용하여 비활성 테스트를 표시합니다.

## 대상 타깃팅 조건을 충족하지 않습니다.

**유효성 검사:**&#x200B;개요 페이지의 타깃팅 조건을 검토합니다.

**옵션:**

* 자격을 제공하고 다시 시도합니다.
* 미리 보기 링크를 사용하여 타깃팅 조건을 우회합니다.

## 페이지가 페이지 타깃팅 조건에 적합하지 않습니다.

**유효성 검사:**&#x200B;개요 페이지에서 페이지가 타깃팅 조건을 벗어나는지 판별하십시오.

**옵션:**

* 시각적 경험 작성기로 이동하여 URL\> 고급\> 현재 페이지를 클릭합니다.

## 새 경험이 아니라 이전 경험이 표시됩니다.

**유효성 검사:** 아래 선택 사항 중 하나를 사용하여 경험을 다시 살펴보십시오.

**옵션:**

* 캐시와 쿠키를 지운 다음, 다시 시도하십시오.

* 다른 브라우저를 사용해 보십시오.
* 비공개/시크릿 모드를 사용하십시오.

## 최근 Target에 추가되었지만 활동을 만들 수 없습니다.

**유효성 검사:** 활동 만들기를 클릭하십시오. 이 선택 사항을 사용할 수 없다면, 활동을 만들기에 충분한 권한이 없을 가능성이 큽니다.

**옵션:**

Target에서 사용자로 추가된 후 활동을 만들려면 승인자 역할이 있어야 합니다.

* 승인자가 되려면 계정 관리자에게 문의하십시오.
* If you are the Admin, give yourself the Approver role from **[!UICONTROL Administration]** > **[!UICONTROL Users]** in Target.

   [자신에게 승인자 역할 지정](/help/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7)을 참조하십시오.

## 활동 설정 후 페이지의 구조가 변경되었습니다.

**유효성 검사:** 기존 활동에 대한 시각적 경험 작성기로 이동하십시오. 선택기(또는 구조)가 변경되었음을 나타내는 경고 메시지를 찾으십시오.

**옵션:**

* 활동을 다시 빌드합니다.

페이지 수정이 Target의 표시 기능에 미치는 영향에 대한 자세한 내용은 [페이지 수정 시나리오](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB)를 참조하십시오.

## 페이지 구조는 페이지 로드 중에 수정됩니다(실행 시).

**유효성 검사:** 개발자에게 문의하십시오.

**참고:** Target이 활동 변경 사항을 적용해야 하는 위치를 인식하기 위해서는 동일한 클래스가 있는 요소들을 동적으로 삽입하거나 같은 수준의 클래스를 동적으로 수정하지 마십시오.

**옵션:**

* 테스트할 각 요소를 고유하게 식별하도록 페이지 코드를 업데이트합니다( ID 사용).
* 위에서 설명한 대로 클래스 또는 동일한 수준의 요소들을 동적으로 수정하지 마십시오.

페이지 수정이 Target의 표시 기능에 미치는 영향에 대한 자세한 내용은 [페이지 수정 시나리오](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB)를 참조하십시오.

## Mbox.js가 헤드 및 본문에서 모든 후속 코드를 표시하고 있습니다.

**유효성 검사:** 소스를 보고 `</body>` 태그를 닫기 전에 mbox.js 파일 다음에 선언이 오는지 판별하십시오.

**옵션:**

* mbox.js를 페이지의 `<head>` 섹션 내부에 마지막 항목으로 배치합니다.
* 본문 내의 최상위 수준 요소에서 고유한 div ID를 사용합니다.

## 다른 활동이 동일한 페이지에서 실행 중입니다.

**유효성 검사:** 충돌 탭을 사용하여 다른 작업이 실행 중인지 확인하십시오.

**참고:** 충돌 탭은 템플릿 테스트 모듈에서 작동하지 않습니다.

**옵션:**

* 이 활동의 우선순위를 높입니다.
* 다른 활동의 우선순위를 낮춥니다.
* 다른 활동을 비활성화합니다.

## 프로필 스크립트를 삭제하면 오류 메시지가 표시됩니다.

**유효성 검사:** Target Standard/Premium에서 프로필 스크립트를 삭제하면 &quot;프로필 스크립트 삭제 실패&quot;라는 오류 메시지가 표시됩니다.

**옵션:**

다음 중 하나를 수행하십시오.

* 다시 삭제합니다. 성공 메시지가 나타납니다.
* Target Standard/Premium 가져오기가 실행될 때까지 약 10분 동안 기다립니다. 가져오기에서 프로필 스크립트 목록을 업데이트합니다.

## Some ajax [!DNL Target] calls are not working.

**참고:**[!DNL Target] 이름은 동일하지만 매개 변수가 다른 여러 개의 ajax 호출의 경우 동일한 페이지에서 작동하지 않습니다. 첫 번째 호출만 수행됩니다.

## You activated an activity using the Target API, but the activity shows a status of [!UICONTROL Inactive] in the Target UI.

Target API를 사용하여 UI 외부에서의 활동 활성화와 같은 특정 작업을 수행하면 업데이트가 UI로 전파되는 데 최대 10분이 걸릴 수 있습니다.