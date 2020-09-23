---
description: 데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.
solution: Analytics
title: '"기준" 시간 이해'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# &quot;기준&quot; 시간 이해{#understanding-as-of-time}

데이터 워크벤치 서버는 해당 소스에서 데이터를 받으면 센서와 같은 데이터 소스를 인식하게 됩니다.

표준은 사용자가 알고 있는 모든 데이터 소스에 대한 데이터가 [!DNL data workbench server] 있음을 보장하는 것입니다.

데이터를 A로 전송하는 세 가지 세트 [!DNL Sensors] 가 있다고 가정해 봅시다 [!DNL data workbench server].WEB1, WEB2 및 WEB3 이 [!DNL data workbench server] 에서 데이터를 수신하고 처리하면 [!DNL Sensors]이러한 각 소스에서 데이터가 자동으로 기대됩니다. 기준 시간은 이러한 세 소스 모두에서 데이터를 [!DNL data workbench server] 받은 마지막 시간을 나타냅니다.

현실적으로 보면, &quot;벽 시간&quot; 또는 벽 위의 시계로부터 오는 시간이 아닌, 단지 시간의 시에만 관심이 있다. [!DNL data workbench server] 시간 [!DNL data workbench server] 은 시간대로만 안다. 이것은 보고서가 항상 기준 시간을 기반으로 실행되도록 보장하므로 보고 목적으로 특히 중요하며, 이것은 부분적인 데이터만 있는 보고서를 시스템의 최종 사용자에게 보낼 수 없도록 합니다.

이 [!DNL data workbench server] 는 전송기에서 전송한 데이터를 사용하여 기준 시간(웹 사이트에서 수집된 실제 데이터 또는 사용자가 전송한 주기적 하트비트)을 제공합니다 [!DNL Sensors]. 이러한 하트비트는 두 가지 목적을 지원합니다.

1. HTTP/1.1 영구 연결을 [!DNL Sensor] and에서 계속 열려면 [!DNL data workbench server]필요합니다.

1. 웹 사이트 트래픽이 수집되어 해당 웹 사이트로 전송되지 않는 경우 기준 시간을 최신 상태로 유지하기 위해 [!DNL data workbench server].

