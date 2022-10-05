---
description: Data Workbench 서버는 해당 소스로부터 데이터를 받으면 센서와 같은 데이터 소스를 인식합니다.
title: '"기준" 시간 이해'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
exl-id: 58ea5c6f-de6b-48d2-b573-f265857026da
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# &quot;기준&quot; 시간 이해{#understanding-as-of-time}

{{eol}}

Data Workbench 서버는 해당 소스로부터 데이터를 받으면 센서와 같은 데이터 소스를 인식합니다.

당시는 [!DNL data workbench server] 에는 알고 있는 모든 데이터 소스에 대한 데이터가 있습니다.

3세트 세트를 가지고 있다고 합시다 [!DNL Sensors] 데이터를 [!DNL data workbench server]: WEB1, WEB2 및 WEB3 로서의 [!DNL data workbench server] 이들로부터 데이터를 받고 처리합니다 [!DNL Sensors]은 이러한 각 소스의 데이터를 자동으로 예상하게 됩니다. 기준 시간은 [!DNL data workbench server] 이 세 소스 모두에서 데이터를 받았습니다.

실용적인 측면에서, [!DNL data workbench server] &quot;월 시간&quot;이라고 불리는 것, 혹은 벽에 있는 시계로부터의 시간이 아닌 시간의 시에만 신경 쓰지 않습니다. 다음 [!DNL data workbench server] 시간만 기준 시간으로 알고 있습니다. 이 기능은 부분 데이터만 있는 보고서를 시스템의 최종 사용자에게 보낼 수 없도록 하는 기준 시간에 따라 항상 보고서를 실행하도록 보장하므로 보고 목적으로 특히 중요합니다.

다음 [!DNL data workbench server] 는 전송기에서 전송한 데이터를 사용하여 웹 사이트에서 수집된 실제 데이터인지 또는 사용자가 전송한 주기적 하트비트를 제공합니다 [!DNL Sensors]. 이러한 하트비트는 다음 두 가지 용도로 사용됩니다.

1. HTTP/1.1 영구 연결을 [!DNL Sensor] 그리고 [!DNL data workbench server].

1. 웹 사이트 트래픽이 수집되어 로 전송되지 않는 경우 기준 시간을 최신 상태로 유지하려면 [!DNL data workbench server].
