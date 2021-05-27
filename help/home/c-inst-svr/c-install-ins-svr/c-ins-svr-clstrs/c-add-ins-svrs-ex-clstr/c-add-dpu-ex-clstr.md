---
description: 일반적으로 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 클러스터의 현재 구성 용량을 초과하는 경우 기존 클러스터에 Insight Server DPU를 추가하려고 합니다.
title: 기존 클러스터에 Insight Server DPU 추가
uuid: 1977a90e-bd51-4838-9498-f7692891109f
exl-id: 9cac2795-626b-4fe3-8a7c-f36c9f1dc68f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---

# 기존 클러스터에 Insight Server DPU 추가{#adding-an-insight-server-dpu-to-an-existing-cluster}

일반적으로 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 클러스터의 현재 구성 용량을 초과하는 경우 기존 클러스터에 Insight Server DPU를 추가하려고 합니다.

## 기본 서버 {#section-7c9a23754a994d73b722d53f999f0e82}에서 구성 파일 업데이트

[!DNL Insight]에서 마스터 [!DNL Insight Server](일반적으로 [!DNL Insight Server] FSU)에 대해 [!DNL Server Files Manager] 을 열고 클러스터에 추가할 각 DPU에 대해 다음을 수행합니다.

1. [처리 Insight Server를 주소 파일](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d)에 설명된 대로 새 DPU의 이름과 주소를 포함하려면 마스터 [!DNL Insight Server]에서 주소 파일을 편집합니다. 클러스터의 현재 [!DNL Insight Servers]이(가) 나열된 그룹에 새 DPU의 이름과 주소를 추가합니다.

1. [클러스터에 대한 액세스 제어 파일 업데이트](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b)에 설명된 대로 새 DPU의 IP 주소를 포함하도록 마스터 [!DNL Insight Server]에서 액세스 제어 파일을 편집합니다.

## 새 Insight Server DPU {#section-8ce9a5957db24f94b3a3250caaccc7ba} 설치

이 작업은 Windows 32비트에만 적용됩니다.

1. 클러스터의 현재 DPU 중 하나에서 다음 디렉토리를 새 DPU로 복사합니다.

   * [!DNL Insight Server] 설치 디렉토리/bin/
   * [!DNL Insight Server] 설치 디렉토리/인증서/
   * [!DNL Insight Server] 설치 디렉토리/구성 요소/

1. [디지털 인증서 다운로드 및 설치](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)에 설명된 대로 새 DPU용 디지털 인증서를 다운로드하여 설치합니다.
1. 새 DPU에서 Windows 메모리 사용률 매개 변수를 설정합니다.
1. [Insight Server를 Windows 서비스](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)로 등록에 설명된 대로 새 DPU 시스템에서 [!DNL Insight Server]을(를) Windows 서비스로 등록합니다.

1. 추적 로그를 확인하여 DPU가 마스터 [!DNL Insight Server]과(와) 동기화 중인지 확인합니다.
1. 클러스터에 추가할 각 추가 DPU에 대해 1~6단계를 반복합니다.

## 데이터 집합 프로필의 처리 서버에 새 Insight Server DPU 추가 {#section-cdc6c3913b9f4010b5e17cc7ec85e849}

새 DPU가 클러스터의 다른 DPU와 동일한 데이터 집합을 처리하는 경우 [Profile.cfg에서 처리 서버 지정에 설명된 대로 새 DPU의 공통 이름을 마스터 [!DNL Insight Server]의 [!DNL profile.cfg] 파일에 추가합니다.](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
