---
title: 보고
description: Customer Journey Analytics을 사용하여 플래그에서 기능 플래그 보고를 보는 방법에 대해 알아봅니다.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# 보고 {#reporting}

플래그는 **Customer Journey Analytics(CJA)**&#x200B;을 통해 보고를 전달합니다. 콘솔 내 결과 또는 보고서 탭이 없습니다. 대신 각 기능 플래그 또는 기능 그룹의 **보고서** 버튼을 누르면 해당 항목에 대한 범위가 지정된 CJA 대시보드가 열립니다.

## 사전 요구 사항 {#prerequisites}

보고서를 보려면 다음을 확인하십시오.

1. 응용 프로그램에 대한 보고가 설정되어 있습니다. [Customer Journey Analytics을 사용하여 보고 설정](#setup)을 참조하십시오.
1. 기능 플래그 또는 기능 그룹이 활성화되었으며 데이터가 누적되었습니다.

## 보고서 보기 {#view-report}

기능 플래그 또는 기능 그룹에 대한 보고서를 열려면 다음을 수행합니다.

1. 콘솔에서 기능 플래그 또는 기능 그룹으로 이동합니다.
1. **보고서**&#x200B;를 선택하십시오.

범위가 지정된 Customer Journey Analytics 대시보드가 열리고 해당 플래그 또는 기능 그룹에 대한 데이터가 표시됩니다. 대시보드에는 다음이 포함됩니다.

* **참가자** — 기능에 적합한 총 사용자 수(변형 + 컨트롤 그룹 결합)
* **컨트롤 그룹** — 컨트롤 그룹에 할당된 사용자 수(기본 환경을 받은 사용자)
* **변형 분류** — 각 변형 및 컨트롤 그룹에 등록된 누적 사용자 수
* **일별 등록** — 시간에 따른 각 변형 및 컨트롤 그룹의 등록을 보여 주는 일별 차트

## Customer Journey Analytics을 사용하여 보고 설정 {#setup}

보고에는 Flags 애플리케이션에 연결된 Customer Journey Analytics 데이터 세트가 필요합니다. 플래그지원팀 또는 Adobe 담당자에게 문의하여 애플리케이션에 대한 보고를 사용하도록 설정합니다.

>[!NOTE]
>
>기능 요청에서 전달된 ID는 프로필에 연결할 필요가 없습니다. 평가는 런타임에 수행되며 이벤트는 Customer Journey Analytics으로 전송됩니다.

## 참조: {#see-also}

* [첫 번째 기능 플래그 만들기](create-your-first-feature-flag.md)
* [기능 플래그를 사용하여 A/B 테스트](a-b-testing.md)
* [기능 그룹 만들기](create-a-feature-group.md)

<!-- -->
