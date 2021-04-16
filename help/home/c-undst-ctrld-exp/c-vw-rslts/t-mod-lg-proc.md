---
description: x-expertion 필드를 확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 추가해야 합니다.
solution: Analytics,Analytics
title: Log Processing.cfg 수정
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
exl-id: 23c7873f-8ffd-422f-896b-d6c7e16aabbd
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---

# Log Processing.cfg 수정{#modifying-log-processing-cfg}

x-expertion 필드를 확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 추가해야 합니다.

[Modifying Transformation.cfg](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6)를 참조하십시오.

**로그 처리.cfg를 수정하려면**

1. [!DNL Insight]에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 [!DNL Profile Manager] > **[!UICONTROL Profile Manager]**&#x200B;을 클릭하거나 [!DNL Admin] 탭에서 프로필 관리 작업 영역을 열어 **[!UICONTROL Admin]** 파일을 엽니다.
1. [!DNL Profile Manager]에서 **[!UICONTROL Dataset]**&#x200B;을 클릭하여 내용을 표시합니다.
1. [!DNL Log Processing.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. [!DNL Log Processing.cfg] 창이 나타납니다.
1. 내용을 표시하려면 **[!UICONTROL Fields]**&#x200B;을 클릭합니다.
1. 현재 목록에서 마지막 필드를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Field]**&#x200B;을 클릭합니다.
1. 다음 예와 같이 새로 만든 필드에 x-expertion을 입력합니다.

   ![단계 정보](assets/logprocessing.png)

1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL Log Processing.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭하여 작업 프로필에 로컬로 변경한 내용을 저장합니다.

   >[!NOTE]
   >
   >데이터 세트에 즉시 재처리가 시작됩니다.

   로그 처리 및 필드에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
