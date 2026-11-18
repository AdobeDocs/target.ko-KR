---
keywords: Automated Personalization;ap;문제 해결;문제 해결;모델;상승도
description: 제안된 해결 방법과 함께 Adobe Target에서 [!UICONTROL Automated Personalization](AP) 활동을 사용하는 동안 발생할 수 있는 잠재적인 어려움에 대해 알아봅니다.
title: '[!UICONTROL Automated Personalization] 활동 문제를 해결하려면 어떻게 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
TQID: 'https://experienceleague.adobe.com/1Qevyq-TiutN1dEZnfC1DDmUgXoHIxtBl-3RMPq-m-0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 7%
---
# [!UICONTROL Automated Personalization] 문제 해결 {#ap-troubleshooting}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL Automated Personalization]** 활동과 관련된 일반적인 문제에 대한 해결 방법을 찾으십시오.

>[!ENDSHADEBOX]

활동이 항상 예상대로 수행되지 않습니다. 다음 목록을 사용하여 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 일반적인 문제의 원인을 식별하고 제안된 해결 방법을 적용하십시오.

## 모델 및 상승도 {#models-and-lift}

+++ [!UICONTROL Automated Personalization] 활동에서 모델을 만드는 데 시간이 너무 오래 걸립니다.

**[!UICONTROL Automated Personalization]** 활동의 경험 수, 사이트에 대한 트래픽, 선택한 성공 지표 등 몇 가지 활동 설정 선택 사항은 모델을 만들어야 하는 시간에 영향을 줍니다.

**해결 방법:** 활동 설정을 검토하고 모델을 만드는 속도를 향상시키는 변경 작업을 수행할 수 있는지 확인하십시오.

* 성공 지표가 RPV로 설정된 경우 전환으로 변경할 수 있습니까? 전환 활동은 일반적으로 모델을 만드는 데 필요한 트래픽이 적습니다. 성공 지표를 RPV에서 전환으로 변경해도 활동 데이터가 손실되지 않습니다.
* 성공 지표가 활동 경험에서 판매 경로의 아래쪽에 있습니까? 활동 전환율이 낮으면 최소 전환 수가 필요하므로 모델을 만드는 데 필요한 트래픽 요구 사항이 증가합니다.
* 활동에서 제외할 수 있는 오퍼 또는 경험이 있습니까? 활동에서 경험 수를 줄이면 모델을 만드는 시간이 빨라집니다.
* 이 활동이 더 성공할 수 있는 더 높은 트래픽 페이지가 있습니까? 활동 위치에 트래픽과 전환이 많을수록 모델이 더 빨리 구축됩니다.

+++

+++ 내 [!UICONTROL Automated Personalization] 활동이 상승도를 생성하지 않았습니다.

**[!UICONTROL Automated Personalization]** 활동에서 상승도를 생성하려면 몇 가지 요소가 필요합니다.

* 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 오퍼는 최적화 목표에 영향을 주는 위치에 있어야 합니다.
* 상승도를 감지하려면 테스트에 충분한 트래픽 및 통계적 &quot;검정력&quot;이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

**솔루션:** 가장 적합한 방법은 먼저 간단한 개인화되지 않은 A/B 테스트를 사용하여 활동 경험을 구성하는 콘텐츠 및 위치가 전체 응답률과 분명한 차이가 있는지 확인하는 것입니다. 미리 샘플 크기를 계산하여 적당한 상승도를 보기에 충분한 전원이 있는지 확인한 다음, 실행을 중단하거나 변경하지 않고 고정된 시간 동안 A/B 테스트를 실행합니다. A/B 테스트 결과가 하나 이상의 경험에 대해 통계적으로 중요한 상승도를 보이면 개인화된 활동이 성공할 가능성이 높습니다. Personalization은 경험의 전체 응답률에 차이가 없어도 작동할 수 있습니다. 일반적으로 이 문제는 통계적 유의성을 가지고 감지할 최적화 목표에 충분히 큰 영향을 주지 않는 오퍼 또는 위치에서 비롯됩니다.

+++

## 활동 설정 및 보고 {#setup-and-reporting}

+++ 내 [!UICONTROL Automated Personalization] 활동 URL에 잘못된 페이지에 오퍼 콘텐츠가 표시됩니다

**원인:** **[!UICONTROL Automated Personalization]**&#x200B;에서 URL 및 템플릿 테스트 규칙이 [!DNL Target] 요청 항목 제약 조건(예: target-global-mbox)에 추가되어 한 번만 평가됩니다. 방문자가 활동 자격을 얻으면 [!DNL Target] 요청 수준 타깃팅 규칙은 재평가되지 않지만 타깃팅 대상은 위치 타깃팅 규칙에 추가됩니다.

**해결 방법:** 필요한 템플릿 규칙을 활동의 입력 대상으로 추가합니다. 대상 평가는 각 요청(호출)에 대해 수행됩니다.

+++

+++ 전환 지표에 종속되는 어떤 지표도 전환되지 않습니다.

이 동작은 예상되었습니다.

**[!UICONTROL Automated Personalization]** 활동에서 전환 지표(최적화 목표든 게시 목표든)가 전환되면 방문자가 경험에서 해제되고 활동이 다시 시작됩니다.

예를 들어 활동에 전환 지표(C1)와 C1에 의존하는 추가 지표(A1)가 있습니다. 방문자가 처음 활동에 들어갔을 때 C1과 A1을 전환하지 않은 경우 성공 지표 종속성으로 인해 A1이 전환되지 않습니다. 방문자가 C1을 변환한 다음 A1을 변환하는 경우 C1이 변환될 때 방문자가 릴리스되므로 A1은 여전히 변환되지 않습니다.

+++

+++ 내 경험 URL이 예상대로 작동하지 않습니다.

**솔루션:** 다음 작업을 사용하십시오.

* 브라우저 캐시로 인해 새 탭에서 미리 보기를 볼 수 없는 경우 새로 고침을 두 번 또는 세 번 시도하십시오. 링크를 복사하여 새 브라우저나 새 세션에서 열 수도 있습니다.
* 콘텐츠를 변경한 경우 경험 URL 링크를 다시 생성하고 새 링크를 팀원과 공유하십시오.

+++
