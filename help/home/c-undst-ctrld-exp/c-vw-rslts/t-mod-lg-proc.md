---
description: 확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 x-experiment 필드를 추가해야 합니다.
solution: Analytics,Analytics
title: Log Processing.cfg 수정
topic: Data workbench
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---


# Log Processing.cfg 수정{#modifying-log-processing-cfg}

확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 x-experiment 필드를 추가해야 합니다.

Transformation.cfg [수정을 참조하십시오](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6).

**Log Processing.cfg를 수정하려면**

1. 에서 작업 공간 내 [!DNL Insight]를 마우스 오른쪽 단추로 클릭하고 [!DNL Profile Manager] > **[!UICONTROL Admin]** 을 클릭하거나 **[!UICONTROL Profile Manager]**[!DNL Admin] 탭에서 프로필 관리 작업 영역을 열어 해당 작업 공간을 엽니다.
1. 에서 [!DNL Profile Manager]을 클릭하여 내용 **[!UICONTROL Dataset]** 을 표시합니다.
1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Log Processing.cfg] 을 클릭합니다 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 열에 [!DNL User] 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > 를 클릭합니다 **[!UICONTROL in Insight]**. 창이 [!DNL Log Processing.cfg] 나타납니다.
1. 아이콘을 **[!UICONTROL Fields]** 클릭하여 내용을 표시합니다.
1. 현재 목록에서 마지막 필드를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > 를 클릭합니다 **[!UICONTROL Field]**.
1. 다음 예제와 같이 새로 만든 필드에 x-experiment를 입력합니다.

   ![단계 정보](assets/logprocessing.png)

1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 에서 열 [!DNL Profile Manager]의 확인 표시 [!DNL Log Processing.cfg] 를 마우스 오른쪽 단추로 클릭한 다음 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL profile name]**를 클릭하여* 로컬에서 작업 프로필에 변경 내용을 저장합니다.

   >[!NOTE]
   >
   >데이터 세트에 즉시 재처리가 시작됩니다.

   로그 처리 및 필드에 대한 자세한 내용은 데이터 세트 *구성 안내서를 참조하십시오*.

