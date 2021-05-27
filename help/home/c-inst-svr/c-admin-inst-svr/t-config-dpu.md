---
description: DPU 구성 파일인 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.
title: DPU.cfg 구성
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
exl-id: 55e4ea7f-fee3-4af7-9cbc-d121e79e6ab2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# DPU.cfg 구성{#configuring-dpu-cfg}

DPU 구성 파일인 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.

이러한 매개 변수를 설정하는 방법은 데이터 세트 크기와 기타 여러 요인에 따라 다릅니다. 성능 조정에 대한 도움이 필요하면 Adobe 컨설팅 서비스에 문의하십시오.

**권장 빈도:**  필요한 경우에만

**DPU  [!DNL Insight Server] 성능 설정을 변경하려면**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.
1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL DPU.cfg] 파일이 이 디렉터리 내에 있습니다.
1. [!DNL DPU.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다. [!DNL DPU.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.
1. [!DNL DPU.cfg] 창에서 구성 요소를 클릭하여 해당 내용을 확인합니다.
1. 필요에 따라 성능 및 경로 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수 목록은 [DPU 성능 설정](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1)을 참조하십시오.

   >[!NOTE]
   >
   >이 파일의 매개 변수를 변경하기 전에 Adobe에 문의하십시오.

   ![](assets/cfg_DPU_egvalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.
