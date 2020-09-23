---
description: Insight Server DPU를 설치하고 관리용으로 구성하기 위한 자세한 지침
solution: Analytics
title: Insight Server DPU의 설치 절차
uuid: 4a04d333-3264-4c15-87fd-8fd201eb68fc
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 8%

---


# Insight Server DPU의 설치 절차{#installation-procedures-for-an-insight-server-dpu}

Insight Server DPU를 설치하고 관리용으로 구성하기 위한 자세한 지침

DPU를 설치하고 구성하려면 [!DNL Insight Server] 다음 작업을 완료해야 합니다.

1. 프로그램 파일을 [!DNL Insight Server] 설치합니다. See [Installing the Insight Server Program Files](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088).
1. Download and install the [!DNL Insight Server] digital certificate. See [Downloading and Installing the Digital Certificates](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. 파일의 포트 설정을 [!DNL Communications.cfg] 확인합니다. See [Checking the Port Settings](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64).
1. 관리 [!DNL Access Control.cfg] 액세스 권한을 허용하도록 파일 [!DNL Insight Server] 을 [!DNL Insight]수정합니다. See [Updating the Access Control File](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d).
1. 서버의 네트워크 위치를 정의하려면 [!DNL server.address] 파일을 수정합니다. See [Defining the Server&#39;s Network Location](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).
1. (선택 사항) 처리된 데이터가 저장되는 위치를 지정하려면 [!DNL Disk Files.cfg] 파일을 수정합니다. See [Configuring the Location of the Dataset (temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).
1. 프로필 및 조회 파일을 설치합니다. See [Installing Profiles and Lookup Files](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-install-prof-lkup-files.md#concept-1631895d09a14dc99316bf8cf166fdfc).
1. Microsoft Windows 메모리 사용률 매개 변수를 설정합니다.
1. Windows 서비스 [!DNL Insight Server] 로 등록하십시오. See [Registering Insight Server as a Windows Service](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).
