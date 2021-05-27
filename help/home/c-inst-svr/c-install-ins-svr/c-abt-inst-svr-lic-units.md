---
description: Insight Server는 두 가지 라이센스 유형에서 사용할 수 있습니다.
title: Insight Server 라이선스 단위 정보
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
exl-id: 82d6fa29-d36e-480d-a975-f5a5e60a32d2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 7%

---

# Insight Server 라이선스 단위 정보{#about-insight-server-license-units}

Insight Server는 두 가지 라이센스 유형에서 사용할 수 있습니다.

다음은 두 가지 라이센스 유형입니다.

* [DPU(데이터 처리 단위)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [파일 서버 유닛(FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## DPU(데이터 처리 단위) {#section-bf589e13cf5c43a58f8f85a457de6f65}

이 유형의 [!DNL Insight Server]은(는) Adobe 데이터 세트에서 데이터를 처리, 저장 및 제공할 수 있습니다. 선택적으로 데이터 집합이 구성되는 소스 데이터가 포함된 로그 파일을 저장하거나 [!DNL Insight Server] FSU(파일 서버 유닛)에서 해당 데이터를 수신할 수 있습니다. DPU는 [!DNL Insight] 및 [!DNL Report] 클라이언트가 직접 상호 작용하는 [!DNL Insight Server] 유형입니다.

[!DNL Insight Server] DPU를 설치하는 경우 Insight Server DPU](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc)에 대한 설치 절차 를 참조하십시오.[

## 파일 서버 유닛(FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

이 유형의 서버는 하나 이상의 [!DNL Sensor] 또는 이벤트 데이터 복제 인스턴스( 특수 사용 라이선스가 제공된 [!DNL Repeater] 기능)에서 이벤트 데이터를 받고 저장하고, Adobe 데이터 세트를 구성하기 위한 하나 이상의 [!DNL Insight Server] 데이터 처리 단위(DPU)로 데이터를 스트리밍하도록 구성되어 있습니다. DPU는 이벤트 데이터를 DPU로 전송하도록 최적화하는 프로토콜을 사용하여 FSU와 통신하며 일반 파일 서버에서 로그 파일을 유지 관리하는 것보다 훨씬 빠릅니다. 또한 FSU를 사용하면 로그 데이터가 저가의 스토리지 하드웨어에 저장되도록 함으로써 하드웨어 비용을 줄이고 여러 [!DNL Sensors]이 하나의 [!DNL Insight Server]을 가리키도록 함으로써 관리 복잡성을 줄입니다.

[!DNL Insight Server] FSU를 설치하는 경우 [Insight Server FSU](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016)에 대한 설치 절차 를 참조하십시오.
