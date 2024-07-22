---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: 제안된 해결 방법과 함께 Adobe Target에서 [!UICONTROL Automated Personalization](AP) 활동을 사용하는 동안 발생할 수 있는 잠재적인 어려움에 대해 알아봅니다.
title: '[!UICONTROL Automated Personalization]개 활동 문제를 해결하려면 어떻게 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
source-git-commit: 2cb2c2b68f6487d1af41ecc7e73750afa1ad85f9
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 32%

---

# [!UICONTROL Automated Personalization] 문제 해결

활동은 경우에 따라 예상대로 수행되지 않을 수 있습니다. AP([!UICONTROL Automated Personalization])와 일부 제안된 해결 방법을 사용하는 동안 발생할 수 있는 몇 가지 잠재적인 어려움에 대해 설명합니다.

## [!UICONTROL Automated Personalization] 활동에서 모델을 만드는 데 시간이 너무 오래 걸립니다. {#section_20028B204DBB4D77A324BA193434AEE2}

+++세부 정보 보기

[!UICONTROL Automated Personalization] 활동에 있는 경험 수, 사이트에 대한 트래픽, 선택한 성공 지표 등 모델을 만드는 데 드는 예상 시간을 줄일 수 있는 몇 가지 활동 설정 변경 사항이 있습니다.

**해결 방법:** 활동 설정을 검토하여 모델을 만드는 속도를 개선하기 위해 변경할 사항이 있는지 확인하십시오.

* 성공 지표가 RPV로 설정된 경우 전환으로 변경할 수 있습니까? 전환 활동은 일반적으로 모델을 만드는 데 필요한 트래픽이 적습니다. 성공 지표를 RPV에서 전환으로 변경해도 활동 데이터가 손실되지 않습니다.
* 성공 지표가 활동 경험에서 판매 경로의 아래쪽에 있습니까? 활동 전환율이 낮으면 최소의 전환 횟수가 필요하므로 모델 작성에 필요한 트래픽 요구 수준이 늘어납니다.
* 활동에서 제외할 수 있는 오퍼나 경험이 있습니까? 활동에서 경험 수를 줄이면 모델을 만드는 시간이 빨라집니다.
* 이 활동이 더 성공할 수 있는 더 높은 트래픽 페이지가 있습니까? 활동 위치에 트래픽과 전환이 많을수록 모델이 더 빨리 구축됩니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동이 상승도를 생성하지 않았습니다. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++세부 정보 보기

[!UICONTROL Automated Personalization] 활동에서 상승도를 생성하는 데 필요한 몇 가지 요소가 있습니다.

* 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 오퍼는 최적화 목표에 영향을 주는 위치에 있어야 합니다.
* 상승도를 감지하려면 테스트에 충분한 트래픽 및 통계적 &quot;검정력&quot;이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

**솔루션:**&#x200B;가장 적합한 방법은 먼저 활동 경험을 구성하는 컨텐츠 및 위치가 간단한 개인화되지 않은 A/B 테스트를 사용하는 전반적인 응답률과 분명한 차이가 있는지 확인하는 것입니다. 반드시 미리 샘플 크기를 계산하십시오. 미리 샘플 크기를 계산하면 적당한 상승도를 볼 수 있는 충분한 전원이 있는지 확인하는 데 도움이 됩니다. 그런 다음 중지하거나 변경하지 않고 고정된 기간 동안 A/B 테스트를 실행할 수 있습니다. A/B 테스트 결과에 하나 이상의 경험에 대해 통계적으로 중요한 상승도가 표시되면 개인화된 활동이 성공할 가능성이 높습니다. Personalization은 경험의 전체 응답률에 차이가 없어도 작동할 수 있습니다. 일반적으로 이 문제는 통계적 유의성을 가지고 감지할 최적화 목표에 충분히 큰 영향을 주지 않는 오퍼 또는 위치에서 비롯됩니다.

+++

## 내 [!UICONTROL Automated Personalization] 활동 URL에 잘못된 페이지에 오퍼 콘텐츠가 표시됩니다. {#section_82A224406DBF4107B05204BEFBBE458C}

+++세부 정보 보기

[!UICONTROL Automated Personalization]에서 URL 및 템플릿 테스트 규칙이 [!DNL Target] 요청 항목 제약 조건(예: target-global-mbox)에 추가되어 한 번만 평가됩니다. 사용자가 활동 자격을 얻으면 Target 요청 수준 타깃팅 규칙이 재평가되지 않습니다. 그러나 타깃팅 대상이 위치 타깃팅 규칙에 추가됩니다.

**해결 방법:** 활동에 대한 입력 대상으로 필요한 템플릿 규칙을 추가합니다. 대상 평가는 각 요청/호출에 대해 발생합니다.

+++

## 전환 지표에 종속되는 어떤 지표도 전환되지 않습니다. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++세부 정보 보기

이는 예상되었습니다.

[!UICONTROL Automated Personalization] 활동에서 전환 지표(최적화 목표든 게시 목표든)가 전환되면 방문자가 경험에서 해제되고 활동이 다시 시작됩니다.

예를 들어 전환 지표(C1)와 추가적인 지표(A1)가 있는 활동이 있습니다. A1은 C1에 따라 다릅니다. 방문자가 처음으로 활동을 시작하고 A1 및 C1을 전환하기 위한 기준이 전환되지 않은 경우 지표 A1은 성공 지표 종속성으로 인해 전환되지 않습니다. 방문자가 C1을 변환한 다음 A1을 변환하는 경우 C1이 변환되면 방문자가 해제되므로 A1은 여전히 변환되지 않습니다.

+++

## 내 경험 URL이 예상대로 작동하지 않습니다. {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++세부 정보 보기

* 브라우저 캐시로 인해 새 탭에서 미리 보기를 볼 수 없는 경우 새로 고침을 두 번 또는 세 번 시도하십시오. 링크를 복사하여 새 브라우저나 새 세션에서 열 수도 있습니다.
* 컨텐츠를 변경하고 팀 동료와 새 링크를 공유한 경우 경험 URL 링크를 재생성하십시오.

+++
