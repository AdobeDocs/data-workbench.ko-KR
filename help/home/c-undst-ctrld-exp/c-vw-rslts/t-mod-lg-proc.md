---
description: 확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 x-experiment 필드를 추가해야 합니다.
solution: Analytics
title: Log Processing.cfg 수정
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
exl-id: 23c7873f-8ffd-422f-896b-d6c7e16aabbd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---

# Log Processing.cfg 수정{#modifying-log-processing-cfg}

{{eol}}

확장 차원을 만드는 데 사용되는 Log Processing.cfg 파일에 x-experiment 필드를 추가해야 합니다.

자세한 내용은 [Transformation.cfg 수정](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6).

**Log Processing.cfg를 수정하려면**

1. in [!DNL Insight]를 열고 [!DNL Profile Manager] 작업 공간 내에서 마우스 오른쪽 단추 클릭 및 **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]**&#x200B;또는 의 [!DNL Admin] 탭.
1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Dataset]** 콘텐츠를 표시합니다.
1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Log Processing.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. 다음 [!DNL Log Processing.cfg] 창이 나타납니다.
1. 클릭 **[!UICONTROL Fields]** 콘텐츠를 표시합니다.
1. 현재 목록에서 마지막 필드를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Field]**.
1. 다음 예와 같이 새로 만든 필드에 x-experiment를 입력합니다.

   ![단계 정보](assets/logprocessing.png)

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Log Processing.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* 로컬에서 만든 변경 사항을 작업 프로필에 저장하려면

   >[!NOTE]
   >
   >데이터 세트가 즉시 재처리를 시작합니다.

   로그 처리 및 필드에 대한 자세한 내용은 *데이터 집합 구성 안내서*.
