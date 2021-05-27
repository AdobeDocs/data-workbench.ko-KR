---
description: Data Workbench 서버는 해당 소스로부터 데이터를 받으면 센서와 같은 데이터 소스를 인식합니다.
title: '"기준" 시간 이해'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
exl-id: 58ea5c6f-de6b-48d2-b573-f265857026da
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# &quot;기준&quot; 시간 이해{#understanding-as-of-time}

Data Workbench 서버는 해당 소스로부터 데이터를 받으면 센서와 같은 데이터 소스를 인식합니다.

기준 시간은 [!DNL data workbench server]에 알고 있는 모든 데이터 소스에 대한 데이터가 있음을 보증합니다.

데이터를 [!DNL data workbench server]에 전송하는 세 개의 [!DNL Sensors] 세트가 있다고 가정해 보겠습니다.WEB1, WEB2 및 WEB3 [!DNL data workbench server]이 이러한 [!DNL Sensors]에서 데이터를 수신하고 처리하면 이러한 각 소스에서 데이터를 자동으로 받게 됩니다. 기준 시간은 [!DNL data workbench server]이 세 개의 소스 모두로부터 데이터를 받은 마지막 시간을 나타냅니다.

사실상 [!DNL data workbench server]은 &quot;월 시간&quot;이라고 지칭되는 시간이나 벽면의 시계로부터 오는 시간이 아니라 시간으로 신경을 쓸 뿐입니다. [!DNL data workbench server]은 시간만 기준 시간으로 알고 있습니다. 이 기능은 부분 데이터만 있는 보고서를 시스템의 최종 사용자에게 보낼 수 없도록 하는 기준 시간에 따라 항상 보고서를 실행하도록 보장하므로 보고 목적으로 특히 중요합니다.

[!DNL data workbench server] 은 전송기에서 전송한 데이터를 사용하여 웹 사이트에서 수집된 실제 데이터인지 또는 [!DNL Sensors]에서 보낸 주기적 하트비트를 제공하는 데 사용됩니다. 이러한 하트비트는 다음 두 가지 용도로 사용됩니다.

1. [!DNL Sensor] 과 [!DNL data workbench server] 사이에 HTTP/1.1 영구 연결을 계속 열려면 다음을 수행하십시오.

1. 웹 사이트 트래픽이 수집되지 않고 [!DNL data workbench server]으로 전송되는 경우 기준 시간을 최신 상태로 유지하려면
