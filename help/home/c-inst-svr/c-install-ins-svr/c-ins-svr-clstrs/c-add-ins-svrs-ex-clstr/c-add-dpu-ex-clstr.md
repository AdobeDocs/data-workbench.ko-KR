---
description: 일반적으로 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 클러스터의 현재 구성 용량을 초과하는 경우 기존 클러스터에 Insight Server DPU를 추가하려고 합니다.
title: 기존 클러스터에 Insight Server DPU 추가
uuid: 1977a90e-bd51-4838-9498-f7692891109f
exl-id: 9cac2795-626b-4fe3-8a7c-f36c9f1dc68f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---

# 기존 클러스터에 Insight Server DPU 추가{#adding-an-insight-server-dpu-to-an-existing-cluster}

{{eol}}

일반적으로 Insight 및 Report 사용자가 처리하고 액세스할 수 있는 데이터 양이 클러스터의 현재 구성 용량을 초과하는 경우 기존 클러스터에 Insight Server DPU를 추가하려고 합니다.

## 기본 서버에서 구성 파일 업데이트 {#section-7c9a23754a994d73b722d53f999f0e82}

in [!DNL Insight]를 열고 [!DNL Server Files Manager] 마스터 [!DNL Insight Server] (일반적으로 [!DNL Insight Server] FSU) 및에 추가할 각 DPU에 대해 다음을 수행합니다.

1. 마스터에서 주소 파일 편집 [!DNL Insight Server] 에 설명된 대로 새 DPU의 이름과 주소를 포함하려면 [주소 파일에 처리 Insight Server 추가](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d). 클러스터의 현재 그룹에 새 DPU의 이름과 주소를 추가합니다 [!DNL Insight Servers] 나열됩니다.

1. 마스터에서 액세스 제어 파일 편집 [!DNL Insight Server] 에 설명된 대로 새 DPU의 IP 주소를 포함하려면 [클러스터의 액세스 제어 파일 업데이트](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b).

## 새 Insight Server DPU 설치 {#section-8ce9a5957db24f94b3a3250caaccc7ba}

이 작업은 Windows 32비트에만 적용됩니다.

1. 클러스터의 현재 DPU 중 하나에서 다음 디렉토리를 새 DPU로 복사합니다.

   * [!DNL Insight Server] 설치 디렉토리/bin/
   * [!DNL Insight Server] 설치 디렉토리/인증서/
   * [!DNL Insight Server] 설치 디렉토리/구성 요소/

1. 에 설명된 대로 새 DPU용 디지털 인증서를 다운로드하여 설치합니다. [디지털 인증서 다운로드 및 설치](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. 새 DPU에서 Windows 메모리 사용률 매개 변수를 설정합니다.
1. 등록 [!DNL Insight Server] 에 설명된 대로 새 DPU 시스템에서 Windows 서비스로 사용할 수 있습니다. [Insight Server를 Windows 서비스로 등록](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

1. 추적 로그를 확인하여 DPU가 마스터와 동기화되는지 확인합니다 [!DNL Insight Server].
1. 클러스터에 추가할 각 추가 DPU에 대해 1~6단계를 반복합니다.

## 데이터 집합 프로필의 처리 서버에 새 Insight Server DPU 추가 {#section-cdc6c3913b9f4010b5e17cc7ec85e849}

새 DPU가 클러스터의 다른 DPU와 동일한 데이터 세트를 처리하는 경우 새 DPU의 일반 이름을 [!DNL profile.cfg] 마스터의 파일 [!DNL Insight Server] 에 설명된 대로 [Profile.cfg에서 처리 서버 지정](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9).
