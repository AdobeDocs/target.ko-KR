---
keywords: 사용자 지정 기준 만들기;알고리즘;기준;권장 사항 기준;csv;ftp;sftp;csv 업로드
description: CSV 파일을 업로드하여 Adobe [!DNL Target] 권장 사항에서 권장 사항을 사용자 지정하는 방법을 알아봅니다.
title: 사용자 지정 기준 업로드
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
TQID: 'https://experienceleague.adobe.com/8gSKOQxHGB5TPe6vdhjgy5sAFxN8O7dodITo7wgrR50'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 14%
---
# 사용자 지정 기준 업로드 {#upload-custom-criteria}

>[!BEGINSHADEBOX]

**이 페이지에서:** 권장 사항의 CSV 파일을 업로드하여 [!DNL Adobe Target Recommendations]에서 사용자 지정 기준을 만드는 방법을 알아봅니다.

>[!ENDSHADEBOX]

사용자 지정 기준에서는 [!DNL Target]에 업로드된 권장 사항의 CSV 파일을 사용합니다. 이렇게 하면 [!DNL Target] 외부에서 계산된 권장 사항을 [!DNL Recommendations] 활동에서 전달할 수 있습니다. 사용자 지정 기준이 작동하는 방식에 대한 자세한 내용은 [Target의 권장 사항 알고리즘에 숨겨진 과학](/help/main/c-recommendations/c-algorithms/recommendations-algorithms.md)을 참조하십시오.

사용자 지정 기준은 **[!UICONTROL 새 기준 만들기]** 화면에서 만들어집니다. 이 화면에 액세스하는 방법은 [새 기준 만들기 화면에 액세스](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#access-create-criteria)를 참조하십시오. 다음 단계는 **[!UICONTROL 권장 사항]** > **[!UICONTROL 기준]** 라이브러리 화면에서 시작됩니다.

1. **[!UICONTROL 권장 사항]** > **[!UICONTROL 기준]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 만들기]**&#x200B;를 클릭합니다.

   ![기준 만들기 메뉴가 열려 있는 기준 페이지에 기준 만들기 및 기준 시퀀스 만들기 표시](../assets/criteria_create_1.png)

1. [기본 정보](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) 섹션에 정보를 입력하십시오.

1. **[!UICONTROL 알고리즘 유형 선택]** 드롭다운 목록에서 **[!UICONTROL 사용자 지정 기준]**&#x200B;을 선택합니다. **[!UICONTROL 알고리즘]** 드롭다운 목록에서 **[!UICONTROL 사용자 지정 알고리즘]**&#x200B;을 선택합니다.

   ![알고리즘 유형으로 사용자 지정 기준이 있고 알고리즘으로 사용자 지정 알고리즘이 있는 권장 사항 알고리즘 섹션](../assets/criteria_create_9.png)

1. (조건부) [백업 콘텐츠](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) 및 [포함 규칙](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) 섹션에 정보를 입력합니다.

1. **[!UICONTROL CSV 업로드]** 섹션에서 CSV 파일의 **[!UICONTROL 위치]**&#x200B;를 선택합니다.

   CSV 파일을 성공적으로 업로드하려면 형식이 올바르게 지정되어야 합니다. 올바른 형식의 CSV 파일을 가져오려면 **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭합니다.

   다음 위치 옵션을 사용할 수 있습니다.

   * **FTP**: FTP 서버에서 CSV 파일을 업로드하려면 **[!UICONTROL FTP]**&#x200B;을 선택한 다음 필요한 정보를 입력하십시오. SSL을 사용할 수 있으며, FTPS 프로토콜을 사용하여 CSV 파일을 안전하게 전송합니다.

   * **SFTP**: SFTP 서버에서 CSV 파일을 업로드하려면 **[!UICONTROL SFTP]**&#x200B;을(를) 선택한 다음 호스트 이름 또는 IP 주소, 포트(기본값 22), 사용자 이름, 암호 및/또는 SSH 개인 키, 디렉터리 및 파일 이름을 입력하십시오. 자세한 내용은 [지원되는 SFTP 서버 설정](/help/main/c-recommendations/c-products/feeds.md#steps)을 참조하세요.

     SFTP는 사용자 지정 기준 CSV 형식을 변경하지 않습니다. `# Key,Recommendation_1,...` 형식을 사용합니다. 다른 피드 유형 형식의 CSV 파일로 인해 가져오기가 실패합니다.

   * **URL**: URL에서 CSV 파일을 업로드하려면 **[!UICONTROL URL]**&#x200B;을 선택한 다음 피드 URL을 입력하십시오.

     ![위치 옵션 FTP, SFTP 및 URL이 강조 표시되고 SFTP가 선택된 CSV 업로드 섹션](../assets/criteria_create_10.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

## 고려 사항

* 사용자 지정 기준 엔티티(행)에는 최대 1,000개의 권장 항목(열)이 포함될 수 있습니다.

* 사용자 지정 기준 업데이트는 기본적으로 &quot;누적&quot;입니다. CSV 업로드 파일의 새 키-값 쌍이 기존 키-값 쌍을 덮어씁니다. CSV 업로드에 키가 없는 기존 키-값 쌍은 계속 전달할 수 있으며 CSV 파일의 일부로 마지막으로 업로드한 후 31일 후에 만료됩니다.

  다음 CSV 업로드에 포함되지 않은 기존 결과를 삭제하려면 Client Care에 문의하여 해당 설정을 활성화하십시오. 이 설정을 활성화하면 사용자 지정 CSV 피드 파일에 있는 키만 게재할 수 있습니다. 이 설정은 모든 사용자 지정 기준에 적용됩니다.

* 사용자 지정 기준 피드는 24시간마다 한 번씩 업데이트됩니다.

  각 사용자 지정 기준 업로드의 업로드 및 동기화 상태가 **[!UICONTROL 권장 사항]** > **[!UICONTROL 기준]** 페이지에 표시됩니다. 사용자 지정 기준을 편집하면 **[!UICONTROL 편집]** 대화 상자에도 상태가 표시됩니다.

* 오류 없는 업로드의 흐름은 **[!UICONTROL 예약됨]** > **[!UICONTROL 피드 파일 다운로드]** > **[!UICONTROL 가져오기]** > **[!UICONTROL 성공]**&#x200B;입니다.

* [!DNL Target]에서 업로드에 문제가 발생하면 다음 오류 메시지가 나타날 수 있습니다.

  | 오류 메시지 | 세부 사항 |
  |--- |--- |
  | 알 수 없는 오류 | 내부 기술 오류를 나타냅니다. |
  | 구문 분석 오류 | 피드 파일 형식에 문제가 있을 수 있습니다. 파일 형식을 수정하고 알고리즘을 다시 저장하여 파일 다운로드 프로세스를 다시 시작합니다. |
  | 서버를 찾을 수 없음 | 인터넷에 표시되는 IP 또는 호스트 이름을 입력합니다. |
  | 자격 증명 오류 | 서버의 활성 계정에 대한 유효한 사용자 및 암호를 제공합니다. |
  | 디렉토리를 찾을 수 없음 | 서버에 존재하는 디렉토리를 지정합니다. |
  | 파일을 찾을 수 없음 | 지정한 디렉터리의 서버에 있는 파일의 이름을 입력하십시오. |
