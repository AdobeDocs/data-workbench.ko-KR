---
description: 데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.
title: '"기준" 시간 이해'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
exl-id: 58ea5c6f-de6b-48d2-b573-f265857026da
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# &quot;기준&quot; 시간 이해{#understanding-as-of-time}

데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.

기준 시간은 [!DNL data workbench server]에 알고 있는 모든 데이터 소스에 대한 데이터가 있음을 보장하는 것입니다.

데이터를 [!DNL data workbench server]으로 전송하는 세 개의 [!DNL Sensors] 세트가 있다고 가정해 봅시다.WEB1, WEB2 및 WEB3. [!DNL data workbench server]은 이러한 [!DNL Sensors]의 데이터를 수신하고 처리하므로 이러한 각 소스에서 데이터를 자동으로 예상하게 됩니다. 기준 시간은 [!DNL data workbench server]이(가) 이러한 3개의 소스 모두에서 데이터를 받은 마지막 시간을 나타냅니다.

실용적인 측면에서, [!DNL data workbench server]은 시간의 준수에 대해서만 관심을 가지며 &quot;벽 시간&quot;이라고 언급될 수 있는 것, 또는 벽 위의 시계로부터의 시간이 아닙니다. [!DNL data workbench server]은 시간 기준 시간으로만 알고 있습니다. 이 기능은 일부 데이터만 있는 보고서를 시스템의 최종 사용자에게 보낼 수 없도록 보장하는 기준 시간을 기반으로 항상 보고서를 실행할 수 있도록 보장하므로 보고 목적으로 특히 중요합니다.

[!DNL data workbench server]은 전송기에서 보낸 데이터를 사용하여 시간 기준(웹 사이트에서 수집한 실제 데이터 또는 [!DNL Sensors]에서 보낸 주기적 하트비트)을 제공합니다. 이러한 하트비트는 두 가지 목적을 지원합니다.

1. HTTP/1.1 영구 연결을 [!DNL Sensor]과 [!DNL data workbench server] 사이에 계속 열려면

1. 웹 사이트 트래픽을 수집하여 [!DNL data workbench server]으로 전송하지 않는 경우 기준 시간을 최신 상태로 유지하기 위해
