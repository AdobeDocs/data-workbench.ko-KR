---
description: 데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.
solution: Insight
title: '"기준" 시간 이해'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# &quot;기준&quot; 시간 이해{#understanding-as-of-time}

데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.

기준 시간은 사용자가 알고 있는 모든 데이터 소스에 대한 데이터를 [!DNL data workbench server] 가지고 있다는 보증입니다.

데이터를 Adobe에 [!DNL Sensors] 전송하는 세 가지 세트가 있다고 [!DNL data workbench server]가정해 봅시다.WEB1, WEB2 및 WEB3. Adobe [!DNL data workbench server] 는 이러한 데이터를 수신하고 처리하므로 [!DNL Sensors]이러한 각 소스에서 데이터를 자동으로 예상할 수 있습니다. 기준 시간은 이 세 소스 모두에서 데이터를 [!DNL data workbench server] 받은 마지막 시간을 나타냅니다.

실용적인 측면에서, &quot;담벼락 시간&quot;이라고 일컬어질 수 있는 것 혹은 벽에 있는 시계로부터의 시간이 아닌, 시간의 시기만 [!DNL data workbench server] 고려한다. 시간은 [!DNL data workbench server] 현재 시간으로만 알고 있습니다. 이것은 보고서가 항상 기준 시간을 기준으로 실행되므로 보고 목적으로 특히 중요합니다. 따라서 일부 데이터만 있는 보고서는 시스템의 최종 사용자에게 전송되지 않습니다.

전송기에서 전송한 데이터를 [!DNL data workbench server] 사용하여 기준 시간(웹 사이트에서 수집된 실제 데이터 또는 사용자가 전송한 주기적 하트비트)을 제공합니다 [!DNL Sensors]. 이러한 하트비트는 두 가지 목적을 지원합니다.

1. HTTP/1.1의 영구 연결을 [!DNL Sensor] 및 URL 간에 계속 [!DNL data workbench server]열려면

1. 웹 사이트 트래픽이 수집되어 해당 웹 사이트로 전송되지 않는 경우 기준 시간을 최신 상태로 유지하기 [!DNL data workbench server]위해

