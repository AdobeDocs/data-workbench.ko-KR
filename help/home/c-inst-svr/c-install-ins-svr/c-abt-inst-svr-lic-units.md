---
description: Insight Server는 두 가지 라이선스 유형에서 사용할 수 있습니다.
solution: Insight
title: Insight 서버 라이센스 단위 정보
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Insight 서버 라이센스 단위 정보{#about-insight-server-license-units}

Insight Server는 두 가지 라이선스 유형에서 사용할 수 있습니다.

다음은 두 가지 라이센스 유형입니다.

* [DPU(데이터 처리 단위)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [FSU(File Server Unit)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## DPU(데이터 처리 단위) {#section-bf589e13cf5c43a58f8f85a457de6f65}

이러한 유형의 [!DNL Insight Server] 데이터를 처리, 저장 및 제공할 수 있습니다. 선택적으로 데이터 세트가 생성된 소스 데이터가 포함된 로그 파일을 저장하거나 FSU(File Server Unit)에서 해당 데이터를 수신할 수 [!DNL Insight Server] 있습니다. DPU는 [!DNL Insight Server] 클라이언트와 직접 상호 작용하는 [!DNL Insight] 유형입니다 [!DNL Report] .

DPU를 설치하는 [!DNL Insight Server] 경우 Insight Server [DPU의 설치 절차를 참조하십시오](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc).

## FSU(File Server Unit) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

이 유형의 서버는 하나 이상의 [!DNL Sensor] 또는 이벤트 데이터 복제 인스턴스(특별 사용 라이선스와 함께 제공되는 [!DNL Repeater] 기능)에서 이벤트 데이터를 수신하여 저장하고 Adobe 데이터 세트를 구성하기 위해 데이터를 하나 이상의 DPU( [!DNL Insight Server] 데이터 처리 단위)로 스트리밍하도록 구성되어 있습니다. DPU는 이벤트 데이터를 DPU로 전송하도록 최적화하는 프로토콜을 사용하여 FSU와 통신하며 일반 파일 서버에서 로그 파일을 유지하는 것보다 훨씬 빠릅니다. 또한 FSU를 사용하면 로그 데이터를 저비용 스토리지 하드웨어에 저장할 수 있으므로 하드웨어 비용을 절감하고 여러 사용자가 한 [!DNL Sensors] 가지를 가리킬 수 있도록 함으로써 관리 복잡성을 줄일 수 [!DNL Insight Server]있습니다.

FSU를 설치하는 [!DNL Insight Server] 경우 Insight Server [FSU에 대한 설치 절차를 참조하십시오](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016).
