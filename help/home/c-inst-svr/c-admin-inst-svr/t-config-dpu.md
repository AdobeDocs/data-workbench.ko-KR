---
description: DPU 구성 파일 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.
solution: Analytics
title: DPU.cfg 구성
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# DPU.cfg 구성{#configuring-dpu-cfg}

DPU 구성 파일 DPU.cfg는 Insight Server에 대한 다양한 성능 매개 변수를 지정합니다.

이러한 매개 변수를 설정하는 방법은 데이터 세트 크기 및 기타 여러 요인에 따라 다릅니다. 성능 조정에 대한 도움이 필요하면 Adobe 컨설팅 서비스에 문의하십시오.

**권장 빈도:** 필요한 경우에만

**DPU[!DNL Insight Server]성능 설정을 변경하려면**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Components]** 를 봅니다. 이 디렉터리 내에 [!DNL DPU.cfg] 파일이 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 [!DNL DPU.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL DPU.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Insight]**&#x200B;클릭합니다.
1. 창에서 구성 요소를 [!DNL DPU.cfg] 클릭하여 콘텐트를 봅니다.
1. 필요에 따라 성능 및 경로 설정을 변경합니다. 이 파일에서 사용할 수 있는 매개 변수의 목록은 DPU 성능 [설정을 참조하십시오](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1).

   >[!NOTE]
   >
   >이 파일의 매개 변수를 변경하기 전에 Adobe에 문의하십시오.

   ![](assets/cfg_DPU_egvalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 열 [!DNL Server Files Manager]에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 선택합니다&#x200B;**[!UICONTROL server name]***.

