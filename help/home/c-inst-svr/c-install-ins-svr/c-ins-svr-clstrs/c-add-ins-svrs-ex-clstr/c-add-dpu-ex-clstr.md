---
description: 일반적으로 처리하려는 데이터의 양이 클러스터의 현재 구성 용량을 초과하는 경우 Insight Server DPU를 기존 클러스터에 추가하려고 합니다.
solution: Insight
title: 기존 클러스터에 Insight Server DPU 추가
uuid: 1977a90e-bd51-4838-9498-f7692891109f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 기존 클러스터에 Insight Server DPU 추가{#adding-an-insight-server-dpu-to-an-existing-cluster}

일반적으로 처리하려는 데이터의 양이 클러스터의 현재 구성 용량을 초과하는 경우 Insight Server DPU를 기존 클러스터에 추가하려고 합니다.

## 마스터 서버에서 구성 파일 업데이트 {#section-7c9a23754a994d73b722d53f999f0e82}

에서 마스터 [!DNL Insight](일반적으로 FSU) [!DNL Server Files Manager] [!DNL Insight Server] [!DNL Insight Server] 를 열고 클러스터에 추가할 각 DPU에 대해 다음을 수행합니다.

1. 처리 인사이트 서버를 주소 파일에 추가에 설명된 대로, 마스터에서 주소 파일을 [!DNL Insight Server] 편집하여 새 [DPU의 이름과 주소를 포함합니다](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d). 클러스터의 현재 상태가 [!DNL Insight Servers] 나열된 그룹에 새 DPU의 이름과 주소를 추가합니다.

1. 클러스터의 액세스 제어 파일 업데이트에 설명된 [!DNL Insight Server] 대로 새 DPU의 IP 주소를 [포함하려면 마스터에서 액세스 제어 파일을 편집합니다](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b).

## 새 Insight Server DPU 설치 {#section-8ce9a5957db24f94b3a3250caaccc7ba}

이 작업은 Windows 32비트에만 적용됩니다.

1. 클러스터의 현재 DPU 중 하나에서 새 DPU로 다음 디렉토리를 복사합니다.

   * [!DNL Insight Server] 설치 디렉토리/bin/
   * [!DNL Insight Server] 설치 디렉토리/인증서/
   * [!DNL Insight Server] 설치 디렉토리/구성 요소/

1. 디지털 인증서 다운로드 및 설치에 설명된 대로 새 DPU의 [디지털 인증서를 다운로드하여 설치합니다](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. 새 DPU에서 Windows 메모리 사용률 매개 변수를 설정합니다.
1. Insight [!DNL Insight Server] Server를 Windows 서비스로 [등록에 설명된 대로 새 DPU 컴퓨터에서 Windows 서비스로 등록합니다](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

1. 추적 로그를 확인하여 DPU가 마스터와 동기화되고 있는지 확인합니다 [!DNL Insight Server].
1. 클러스터에 추가하는 각 추가 DPU에 대해 1~6단계를 반복합니다.

## 데이터 집합 프로필의 처리 서버에 새 Insight 서버 DPU 추가 {#section-cdc6c3913b9f4010b5e17cc7ec85e849}

새 DPU가 클러스터의 다른 DPU와 동일한 데이터 세트를 처리하는 경우 Profile.cfg에서 처리 서버 지정에 설명된 [!DNL profile.cfg] 대로 새 DPU의 [!DNL Insight Server] 일반 이름을 마스터의 파일에 추가합니다 [](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9).
