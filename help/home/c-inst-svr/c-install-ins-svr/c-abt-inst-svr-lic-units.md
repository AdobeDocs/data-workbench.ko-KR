---
description: Insight Server는 두 가지 라이센스 유형에서 사용할 수 있습니다.
title: Insight Server 라이선스 단위 정보
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
exl-id: 82d6fa29-d36e-480d-a975-f5a5e60a32d2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 7%

---

# Insight Server 라이선스 단위 정보{#about-insight-server-license-units}

{{eol}}

Insight Server는 두 가지 라이센스 유형에서 사용할 수 있습니다.

다음은 두 가지 라이센스 유형입니다.

* [DPU(데이터 처리 단위)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [파일 서버 유닛(FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## DPU(데이터 처리 단위) {#section-bf589e13cf5c43a58f8f85a457de6f65}

이러한 유형의 [!DNL Insight Server] Adobe 데이터 세트에서 데이터를 처리, 저장 및 제공할 수 있습니다. 선택적으로 데이터 집합이 구성되는 소스 데이터가 포함된 로그 파일을 저장하거나, [!DNL Insight Server] 파일 서버 유닛(FSU). DPU는 [!DNL Insight Server] 사용 [!DNL Insight] 및 [!DNL Report] 클라이언트는 직접 상호 작용합니다.

를 설치하는 경우 [!DNL Insight Server] DPU, [Insight Server DPU의 설치 절차](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc).

## 파일 서버 유닛(FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

이 유형의 서버는 하나 이상의 이벤트 데이터를 수신하고 저장하도록 구성되어 있습니다 [!DNL Sensor] 또는 이벤트 데이터 복제 인스턴스( [!DNL Repeater] 특수 사용 라이선스가 포함된 기능) 및 하나 이상의 데이터 스트림으로 데이터를 스트리밍할 수 있습니다 [!DNL Insight Server] Adobe 데이터 세트를 구성하기 위한 DPU(데이터 처리 유닛)입니다. DPU는 이벤트 데이터를 DPU로 전송하도록 최적화하는 프로토콜을 사용하여 FSU와 통신하며 일반 파일 서버에서 로그 파일을 유지 관리하는 것보다 훨씬 빠릅니다. 또한 FSU를 사용하면 로그 데이터를 저가의 스토리지 하드웨어에 저장할 수 있으므로 하드웨어 비용을 줄이고, 여러 가지 기능을 통해 관리 복잡성을 줄입니다 [!DNL Sensors] 단일 [!DNL Insight Server].

를 설치하는 경우 [!DNL Insight Server] FSU, 자세한 내용은 [Insight Server FSU의 설치 절차](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016).
