---
description: Insight Server DPU를 설치하고 관리용으로 구성하기 위한 세부 지침입니다.
title: Insight Server DPU의 설치 절차
uuid: 4a04d333-3264-4c15-87fd-8fd201eb68fc
exl-id: 0bdfb598-d7eb-4e49-8d9b-4f362c3a62e8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 8%

---

# Insight Server DPU의 설치 절차{#installation-procedures-for-an-insight-server-dpu}

{{eol}}

Insight Server DPU를 설치하고 관리용으로 구성하기 위한 세부 지침입니다.

를 설치하고 구성하려면 [!DNL Insight Server] DPU에서 다음 작업을 순서대로 완료해야 합니다.

1. 설치 [!DNL Insight Server] 프로그램 파일. 자세한 내용은 [Insight Server 프로그램 파일 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088).
1. 를 다운로드하여 설치합니다. [!DNL Insight Server] 디지털 인증서. 자세한 내용은 [디지털 인증서 다운로드 및 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. 에서 포트 설정을 확인합니다. [!DNL Communications.cfg] 파일. 자세한 내용은 [포트 설정 확인](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64).
1. 수정 [!DNL Access Control.cfg] 파일에 대한 관리자 액세스 허용 [!DNL Insight Server] 변환 전: [!DNL Insight]. 자세한 내용은 [액세스 제어 파일 업데이트](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d).
1. 수정 [!DNL server.address] 파일을 사용하여 서버의 네트워크 위치를 정의합니다. 자세한 내용은 [서버의 네트워크 위치 정의](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).
1. (선택 사항) [!DNL Disk Files.cfg] 파일을 사용하여 처리된 데이터가 저장되는 위치를 지정합니다. 자세한 내용은 [데이터 집합 위치 구성(temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).
1. 프로필 및 조회 파일을 설치합니다. 자세한 내용은 [프로필 및 조회 파일 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-install-prof-lkup-files.md#concept-1631895d09a14dc99316bf8cf166fdfc).
1. Microsoft Windows 메모리 사용률 매개 변수를 설정합니다.
1. 등록 [!DNL Insight Server] Windows 서비스로 사용할 수 있습니다. 자세한 내용은 [Insight Server를 Windows 서비스로 등록](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).
