---
description: Adobe Target은 at.js나 mbox.js JavaScript 라이브러리를 사용하여 웹 페이지와 통합됩니다.
keywords: 타깃팅;쿠키;퍼스트 파티;자사 쿠키
seo-description: Adobe Target은 at.js나 mbox.js JavaScript 라이브러리를 사용하여 웹 페이지와 통합됩니다.
seo-title: 타깃팅이 작동하는 방법
solution: Target
title: 타깃팅이 작동하는 방법
uuid: 8b5a36c0-555d-42c5-8b24-c08d07440a53
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 타깃팅이 작동하는 방법{#how-targeting-works}

Adobe Target은 at.js나 mbox.js JavaScript 라이브러리를 사용하여 웹 페이지와 통합됩니다.

[!DNL Target Classic]에서는 타깃팅된 컨텐츠를 표시하거나 데이터를 수집하려는 페이지에서 각 영역 주위에 mbox를 사용했습니다. [!DNL Target Standard]에서는 이러한 mbox가 필요하지 않습니다. 대신, 각 페이지에서 참조되는 하나의 [JavaScript 라이브러리](../c-implementing-target/c-considerations-before-you-implement-target/target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB)만 있으면 최적화 활동을 실행할 수 있습니다.

방문자가 Target이 활성화된 페이지를 요청할 때마다, [!DNL Target]에서는 다음 프로세스를 사용하여 오퍼를 제공합니다.

1. 고객이 서버에서 페이지를 요청하고 브라우저에 표시합니다.
1. 퍼스트 파티 쿠키는 고객의 브라우저에서 고유 방문자 ID를 설정하도록 설정됩니다.

   마스터 마케팅 프로필을 사용하는 경우 [!DNL Experience Cloud visitor ID]도 설정됩니다.

1. 페이지는 [!DNL Target] 파일이나 페이지의 mbox를 통해 [!DNL target.js]을 호출합니다.
1. [!DNL Target]은 방문자와 연결된 프로필을 참조합니다.
1. [!DNL Target]은 해당 프로필과 연결된 프로필 스크립트를 실행합니다.
1. [!DNL Target]은 응답을 계산합니다.
1. 활동이나 캠페인의 규칙에 따라 컨텐츠가 표시됩니다.

기본적인 A/B 테스트에서 표시되는 오퍼는 무작위로 선택됩니다. 이러한 트래픽 무작위 분할의 결과, 초기 트래픽을 많이 사용한 후에야 비율이 안정됩니다. 예를 들어 두 개의 경험이 있는 활동이 있는 경우 시작 경험이 무작위로 선택됩니다. 트래픽이 거의 없다면 방문자 비율이 하나의 경험으로 기울어질 수 있습니다. 트래픽이 증가함에 따라 이러한 비율은 더 비슷해지게 됩니다.
