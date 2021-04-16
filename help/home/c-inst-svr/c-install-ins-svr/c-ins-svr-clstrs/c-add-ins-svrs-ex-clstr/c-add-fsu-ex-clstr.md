---
description: 추가 파일 서버에 소스 데이터를 저장하거나 마스터 Insight Server에 대한 백업을 설정하려면 기존 클러스터에 Insight Server FSU를 추가할 수 있습니다.
title: 기존 클러스터에 Insight Server FSU 추가
uuid: 57d6ef52-eef9-4425-943a-331e4c9c4207
exl-id: b3b08016-42ad-4972-a8b7-ee714493fa52
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# 기존 클러스터에 Insight Server FSU 추가{#adding-an-insight-server-fsu-to-an-existing-cluster}

추가 파일 서버에 소스 데이터를 저장하거나 마스터 Insight Server에 대한 백업을 설정하려면 기존 클러스터에 Insight Server FSU를 추가할 수 있습니다.

기존 클러스터에 [!DNL Insight Server] FSU를 추가하려면 다음 절차를 수행해야 합니다.

1. [서버의 구성 기본 파일 업데이트](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-b5f21f2edb35493da4475de2cdeefca1)
1. [새 Insight Server FSU 설치](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-dddad299dd8642aa91cbe19a395ef3f4)
1. [새 Insight Server FSU 구성](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-c39334c5bd754d5b98d41ad094333108)

## 서버 {#section-b5f21f2edb35493da4475de2cdeefca1}에서 기본 구성 파일 업데이트

[!DNL Insight]에서 마스터 [!DNL Insight Server](일반적으로 [!DNL Insight Server] FSU)에 대해 [!DNL Server Files Manager]을 열고 클러스터에 추가할 각 FSU에 대해 다음을 수행합니다.

1. [처리 인사이트 서버를 주소 파일](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d)에 추가하는 방법에 설명된 대로 마스터 [!DNL Insight Server]에서 주소 파일을 편집하여 새 FSU의 이름과 주소를 포함합니다. 클러스터의 현재 [!DNL Insight Servers]이(가) 나열되는 그룹에 새 FSU의 이름과 주소를 추가합니다.

1. [클러스터](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b)에 대한 액세스 제어 파일 업데이트에 설명된 대로 마스터 [!DNL Insight Server]에서 액세스 제어 파일을 편집하여 새 FSU의 IP 주소를 포함합니다.

## 새 Insight 서버 FSU {#section-dddad299dd8642aa91cbe19a395ef3f4} 설치

1. 현재 FSU에서 [!DNL Insight Server] 설치 디렉토리의 zip 파일을 만들고 새 FSU에 파일을 복사합니다.
1. [!DNL Insight Server] 소프트웨어를 배치할 위치에 파일의 압축을 해제합니다.
1. [디지털 인증서 다운로드 및 설치](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)에 설명된 대로 새 FSU에 대한 디지털 인증서를 다운로드하여 설치합니다.
1. 새 FSU에 Windows 메모리 사용 매개 변수를 설정합니다.
1. [서버의 네트워크 위치 정의](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)에 설명된 대로 FSU의 이름을 반영하도록 [!DNL .address] 파일의 이름을 변경합니다.

1. 새 FSU의 드라이브 구조가 기본 FSU의 드라이브 구조와 다른 경우 [!DNL Disk Files.cfg] 파일을 편집해야 합니다.

   1. 새 FSU에서 [!DNL Disk Files.cfg] 파일을 엽니다.
   1. [데이터 집합 데이터 공간 모니터링](../../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-dtst-data-spc.md#task-6223fa2c718845678824a0a96df96a03)에 설명된 대로 기본 FSU의 드라이브와 일치하도록 설정을 업데이트합니다.
   1. 파일을 로컬과 서버에 저장합니다.

1. [Insight Server를 Windows 서비스](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)로 등록에 설명된 대로 새 FSU 컴퓨터의 [!DNL Insight Server]을(를) Windows 서비스로 등록합니다.

1. 클러스터에 추가하는 각 추가 FSU에 대해 1~6단계를 반복합니다.

## 새 Insight 서버 FSU 구성 {#section-c39334c5bd754d5b98d41ad094333108}

다음 절차에서는 특정 구성 작업에 대한 지침을 제공합니다. 새 FSU 구현에 적합한 지침을 따릅니다.

**소스 데이터 저장소에 대한 FSU를 구성하려면**

새 FSU가 클러스터에서 실행 중인 데이터 세트에 대한 추가 소스 데이터를 저장하는 경우 *데이터 세트 구성 안내서*&#x200B;의 로그 처리 구성 파일 장에 있는 [!DNL Insight Server] 파일 서버 단위 구성에 설명된 대로 파일 서버 구성 프로세스를 완료해야 합니다.

**새 FSU를 만들려면 마스터 FSU에 대한 백업을  [!DNL Insight Server] 수행하십시오**

새 FSU를 마스터 [!DNL Insight Server](클러스터의 FSU로 제공)에 대한 백업으로 만들려면 새(백업) FSU에서 마스터 FSU와 동기화되도록 동기화 파일을 수정해야 합니다.

1. 백업 [!DNL Insight Server] FSU에서 [!DNL Server Files Manager] 폴더를 [!DNL Components for Processing Servers] 폴더에 있는 [!DNL Synchronize.cfg] 파일을 [!DNL Components] 폴더에 복사합니다.

1. [!DNL Insight]에서 [!DNL Synchronize.cfg] 파일([!DNL Components] 폴더)을 엽니다.

1. Components 디렉토리의 위치를 지정하는 SynchronizeDir을 찾습니다. 디렉터리 아래에 여러 개의 동기화 디렉터리가 있을 수 있으므로 원하는 서버를 찾기 위해 여러 디렉터리(서버 번호 클릭)에 대한 콘텐트를 볼 수 있습니다.
1. 아래 예와 같이 SynchronizeDir 항목을 편집하고 두 번째 SynchronizeDir 항목을 추가합니다.

   ![](assets/cfg_cluster_SynchronizeDirEditComponents.png)

1. 클러스터의 DPU의 [!DNL Synchronize.cfg] 파일과 혼동하지 않도록 수정한 파일을 [!DNL FSU_Synchronize.cfg]과 같은 새 이름으로 저장합니다.

1. 이름을 바꾼 파일의 로컬 복사본을 서버에 저장하려면 [!DNL Server Files Manager]을 사용합니다. 백업 FSU는 마스터 [!DNL Insight Server] FSU에서 식별된 디렉토리에 있는 파일을 다운로드하고 변경 시 마스터 [!DNL Insight Server] FSU에서 업데이트된 파일의 복사본을 동적으로 검색합니다.
