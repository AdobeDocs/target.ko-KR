---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: 권장 사항을 사용자 지정하려면 CSV 파일을 업로드합니다.
title: 사용자 지정 기준 업로드
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 108bbe65732b7df20caf9df6b3e5b77e3c31c457
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 63%

---


# ![PREMIUM](/help/assets/premium.png) 사용자 지정 기준 업로드{#upload-custom-criteria}

권장 사항을 사용자 지정하려면 CSV 파일을 업로드합니다.

[!UICONTROL 새 기준 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. 여기서 만드는 기준은 자동으로 모든 [!DNL Recommendations] 활동에 사용 가능해집니다.
* VEC( [!DNL Recommendations] Visual Experience Composer [!UICONTROL )를 사용하여] 활동을 하는 경우, 사용자는 페이지에서 요소 선택 [!UICONTROL 후 즉시] 기준 [!UICONTROL 선택]으로 선택한 후 [!UICONTROL , Click]Creating Recommendations/ Town을 클릭한 다음 , RecommendationsInsert, Town 또는 Insert After Creating Recommendations으로 이동합니다. 그런 다음 사용 가능한 기준을 선택하거나 기준 **[!UICONTROL 만들기를 클릭할 수 있습니다]**. 새 기준을 만드는 경우 다른 [!DNL Recommendations] 활동과 함께 사용할 기준을 저장할 수 있습니다. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* [!DNL Recommendations] 활동을 편집하는 경우 페이지에서 [!UICONTROL 권장 사항 위치] 상자를 클릭하고 **[!UICONTROL 기준 변경]**&#x200B;을 선택합니다. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. 다른 [!DNL Recommendations] 활동과 함께 사용할 새 기준을 저장하는 선택 사항이 있습니다.

다음 단계에서는 첫 번째 방법을 사용하여 새 기준 [!UICONTROL 만들기] 화면에 액세스한다고 가정합니다.[ **[!UICONTROL Recommendations]** ] > [ **[!UICONTROL 기준]** 라이브러리] 화면

1. Recommendations **[!UICONTROL >]** 기준을 클릭합니다 ****.

1. 기준 **[!UICONTROL 만들기]** > 사용자 지정 기준 **[!UICONTROL 업로드를 클릭합니다]**.

1. Fill in the information in the [Basic Information](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. 데이터 소스 [섹션의 정보를](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) 입력합니다.

1. Fill in the information in the [Content](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) section.

1. (조건부) [컨텐츠 유사성](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) 섹션에 정보를 입력합니다.

1. (조건부) 포함 규칙 [섹션에 정보를](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) 입력합니다.

1. (조건부 속성 가중치 섹션의 정보를 [입력합니다](/help/c-recommendations/c-algorithms/create-new-algorithm.md#weighting) .

1. CSV **[!UICONTROL 업로드]** 섹션에서 **[!UICONTROL CSV]** 파일의위치를 선택합니다.

   ![CSV 섹션 업로드](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   CSV 파일을 성공적으로 업로드하려면 형식이 올바르게 지정되어야 합니다. **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭하여 올바른 형식의 CSV 파일을 가져옵니다.

   다음 두 가지 위치 옵션이 있습니다.

   * **FTP:** FTP 서버에서 CSV 파일을 업로드하려면 **[!UICONTROL FTP]**&#x200B;를 선택한 다음, 필요한 정보를 입력합니다. SSL을 사용하기 위한 옵션이 제공됩니다. 이 옵션은 FTPS 프로토콜을 사용하여 CSV 파일을 안전하게 전송합니다.
   * **URL:** URL에서 CSV 파일을 업로드하려면 **[!UICONTROL URL을]**&#x200B;선택한 다음 피드 URL을 입력합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >사용자 지정 기준 엔티티(행)에는 최대 1,000개의 권장 항목(열)이 포함될 수 있습니다.

사용자 지정 기준 업데이트는 기본적으로 &quot;누적&quot;입니다. CSV 업로드 파일에 지정된 새 키-값 쌍이 기존 키-값 쌍을 덮어씁니다. CSV 업로드에 지정된 키가 없는 기존 키-값 쌍은 계속 제공할 수 있으며, CSV 파일의 일부로 마지막으로 업로드한 뒤 31일 후에 만료됩니다.

Client Care에 문의하여 다음 CSV 업로드에 포함되지 않은 기존 결과를 삭제하도록 설정을 활성화합니다. 이 설정을 활성화하면 사용자 지정 CSV 피드 파일에 있는 키만 전달할 수 있습니다. 이 설정은 모든 사용자 지정 기준에 적용됩니다.

사용자 지정 기준 피드는 24시간마다 한 번씩 업데이트됩니다.

권장 사항 > 기준 페이지에서 각 기준 카드의 맨 아래에 있는 사용자 지정 기준 업로드의 업로드 및 동기화 상태를 확인할 수 있습니다. 사용자 지정 기준을 편집할 때 편집 대화 상자에서 상태를 볼 수도 있습니다.

오류가 없는 업로드에 대한 흐름은 예약됨 > 피드 파일 다운로드 >가져오기 > 성공입니다.

The following are possible error messages you might receive if [!DNL Target] encounters a problem with the upload:

| 오류 메시지 | 세부 사항 |
|--- |--- |
| 알 수 없는 오류 | 내부 기술 오류를 나타냅니다. |
| 구문 분석 오류 | 피드 파일 형식에 문제가 있을 수 있습니다. 파일 형식을 수정하고 알고리즘을 다시 저장하여 파일 다운로드 프로세스를 다시 시작합니다. |
| 서버를 찾을 수 없음 | 인터넷에 표시되는 IP 또는 호스트 이름을 제공하십시오. |
| 자격 증명 오류 | 서버의 활성 계정에 대한 유효한 사용자 및 암호를 제공합니다. |
| 디렉토리를 찾을 수 없음 | 서버에 존재하는 디렉토리를 지정합니다. |
| 파일을 찾을 수 없음 | 표시된 디렉토리의 서버에 있는 파일의 이름을 제공합니다. |

## 교육 비디오: 추천에서 기준 만들기(12:33) ![자습서 배지](/help/assets/tutorial.png)

이 비디오에는 다음 정보가 포함되어 있습니다(사용자 지정 기준 업로드에 대한 세부 사항은 11:43부터 시작).

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)