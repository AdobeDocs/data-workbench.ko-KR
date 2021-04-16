---
description: Insight Server DPU를 설치하고 관리용으로 구성하기 위한 세부 지침
title: Insight Server DPU의 설치 절차
uuid: 4a04d333-3264-4c15-87fd-8fd201eb68fc
exl-id: 0bdfb598-d7eb-4e49-8d9b-4f362c3a62e8
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 8%

---

# Insight Server DPU의 설치 절차{#installation-procedures-for-an-insight-server-dpu}

Insight Server DPU를 설치하고 관리용으로 구성하기 위한 세부 지침

[!DNL Insight Server] DPU를 설치하고 구성하려면 다음 작업을 완료해야 합니다.

1. [!DNL Insight Server] 프로그램 파일을 설치합니다. [Insight 서버 프로그램 파일 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088)를 참조하십시오.
1. [!DNL Insight Server] 디지털 인증서를 다운로드하고 설치합니다. [디지털 인증서 다운로드 및 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)를 참조하십시오.
1. [!DNL Communications.cfg] 파일의 포트 설정을 확인합니다. [포트 설정 확인](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64)을 참조하십시오.
1. [!DNL Access Control.cfg] 파일을 수정하여 [!DNL Insight]의 [!DNL Insight Server]에 대한 관리 액세스를 허용합니다. [액세스 제어 파일 업데이트](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d)를 참조하십시오.
1. [!DNL server.address] 파일을 수정하여 서버의 네트워크 위치를 정의합니다. [서버의 네트워크 위치 정의](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)를 참조하십시오.
1. (선택 사항) 처리된 데이터가 저장되는 위치를 지정하려면 [!DNL Disk Files.cfg] 파일을 수정합니다. [데이터 세트 위치 구성(temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e)을 참조하십시오.
1. 프로필 및 조회 파일을 설치합니다. [프로필 및 조회 파일 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-install-prof-lkup-files.md#concept-1631895d09a14dc99316bf8cf166fdfc)를 참조하십시오.
1. Microsoft Windows 메모리 사용 매개 변수를 설정합니다.
1. [!DNL Insight Server]을(를) Windows 서비스로 등록합니다. [Insight Server를 Windows 서비스](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)로 등록을 참조하십시오.
