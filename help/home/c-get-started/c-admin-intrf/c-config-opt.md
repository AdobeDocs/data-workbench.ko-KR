---
description: 구성 옵션을 사용하면 다양한 서버에 대한 연결을 제어하는 Insight.cfg 파일이 열립니다.
title: 구성 옵션
uuid: 1edfcf03-b278-4d81-942c-c9024378e13c
exl-id: bb694d3c-64f7-4a74-b774-4d5145250e6d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# 구성 옵션{#configuration-option}

{{eol}}

구성 옵션을 사용하면 다양한 서버에 대한 연결을 제어하는 Insight.cfg 파일이 열립니다.

![](assets/cfg_Workstation.png)

**Insight.cfg 파일을 편집하려면**

1. 에서 [!DNL Insight.cfg] 창에서 원하는 대로 매개 변수를 수정합니다. 의 매개 변수에 대한 자세한 설명 [!DNL Insight.cfg] 파일, [인사이트 구성 매개 변수](../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b).
1. 구성 설정을 저장하려면 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL Insight.cfg (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save as Insight.cfg]**.

**새 서버를 추가하려면**

1. 에서 [!DNL Insight.cfg] 창, 마우스 오른쪽 단추 클릭 **[!UICONTROL Servers]** 을(를) 클릭합니다. **[!UICONTROL Add new child]** > **[!UICONTROL Server]**.

   ![](assets/cfg_Workstation_AddServer.png)

1. 서버 매개 변수를 완료하거나 수정하여 원하는 서버에 액세스할 수 있는 Data Workbench을 제공합니다. 의 매개 변수에 대한 자세한 설명 [!DNL Insight.cfg] 파일, [인사이트 구성 매개 변수](../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b).
1. 연결을 구성할 각 서버에 대해 1단계와 2단계를 반복합니다.
1. 구성 설정을 저장하려면 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL Insight.cfg (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save as Insight.cfg]**.

Data Workbench은 지정한 설정을 사용하여 서버에 연결을 시도합니다. 연결이 설정되면 [!DNL Servers Manager] 아래와 같이 표시됩니다. Data Workbench이 서버에 연결할 수 없는 경우 빨간색 노드가 나타납니다.

![](assets/vis_SysStat_RedGreenDots.png)
