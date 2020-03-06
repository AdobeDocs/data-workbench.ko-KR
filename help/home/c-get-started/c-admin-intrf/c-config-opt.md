---
description: '[구성] 옵션을 사용하면 다양한 서버와의 연결을 제어하는 Insight.cfg 파일이 열립니다.'
solution: Analytics
title: 구성 옵션
topic: Data workbench
uuid: 1edfcf03-b278-4d81-942c-c9024378e13c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 구성 옵션{#configuration-option}

[구성] 옵션을 사용하면 다양한 서버와의 연결을 제어하는 Insight.cfg 파일이 열립니다.

![](assets/cfg_Workstation.png)

**Insight.cfg 파일을 편집하려면**

1. 창에서 원하는 대로 매개변수를 [!DNL Insight.cfg] 수정합니다. 파일에 있는 매개 변수에 대한 자세한 설명은 인사이트 구성 [!DNL Insight.cfg] 매개 변수를 참조하십시오 [](../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b).
1. 구성 설정을 저장하려면 창 **[!UICONTROL Insight.cfg (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save as Insight.cfg]**.

**새 서버를 추가하려면**

1. 창에서 [!DNL Insight.cfg] 마우스 오른쪽 단추를 **[!UICONTROL Servers]** 클릭하고 **[!UICONTROL Add new child]** > **[!UICONTROL Server]**&#x200B;를 클릭합니다.

   ![](assets/cfg_Workstation_AddServer.png)

1. 서버 매개변수를 완료하거나 수정하여 데이터 워크벤치에 원하는 서버에 대한 액세스를 제공합니다. 파일에 있는 매개 변수에 대한 자세한 설명은 인사이트 구성 [!DNL Insight.cfg] 매개 변수를 참조하십시오 [](../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b).
1. 연결을 구성할 각 서버에 대해 1단계 및 2단계를 반복합니다.
1. 구성 설정을 저장하려면 창 **[!UICONTROL Insight.cfg (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save as Insight.cfg]**.

데이터 워크벤치에서는 지정한 설정을 사용하여 서버에 연결을 시도합니다. 연결이 설정되면 아래와 [!DNL Servers Manager] 같이 녹색 노드가 나타납니다. 데이터 워크벤치가 서버에 연결할 수 없는 경우 빨간색 노드가 나타납니다.

![](assets/vis_SysStat_RedGreenDots.png)

