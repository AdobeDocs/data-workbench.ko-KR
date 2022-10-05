---
description: DPU 구성 파일인 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.
title: DPU.cfg 구성
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
exl-id: 55e4ea7f-fee3-4af7-9cbc-d121e79e6ab2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# DPU.cfg 구성{#configuring-dpu-cfg}

{{eol}}

DPU 구성 파일인 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.

이러한 매개 변수를 설정하는 방법은 데이터 세트 크기와 기타 여러 요인에 따라 다릅니다. 성능 조정에 대한 도움이 필요하면 Adobe 컨설팅 서비스에 문의하십시오.

**권장 빈도:** 필요한 경우에만

**변경하려면 [!DNL Insight Server] DPU 성능 설정**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL DPU.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL DPU.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL DPU.cfg].
1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. 에서 [!DNL DPU.cfg] 창에서 구성 요소를 클릭하여 해당 컨텐츠를 확인합니다.
1. 필요에 따라 성능 및 경로 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수 목록에 대해서는 [DPU 성능 설정](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1).

   >[!NOTE]
   >
   >이 파일의 매개 변수를 변경하기 전에 Adobe에 문의하십시오.

   ![](assets/cfg_DPU_egvalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
