---
description: Repeater에 사용할 Insight Server FSU를 설치하고 구성하는 지침입니다.
title: 반복을 위한 Insight Server FSU 구성
uuid: c2bae862-37d3-4841-b31b-59593c1e4316
exl-id: dacbabd5-f6f5-4201-8709-146075eae679
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 5%

---

# 반복을 위한 Insight Server FSU 구성{#configuring-an-insight-server-fsu-for-repeater}

Repeater에 사용할 Insight Server FSU를 설치하고 구성하는 지침입니다.

다음 작업을 순서대로 완료합니다. 각 단계 후에 [!DNL Insight Server] FSU를 반복 서버로 사용할 수 있도록 해야 하는 모든 예외 또는 변경 사항입니다.

1. [Insight Server 설치](../../../../home/c-inst-svr/c-install-ins-svr/c-install-ins-svr.md#concept-1c796b4ca427474f99ec6ba34d8254cd)에 설명된 대로 [!DNL Insight Server] 프로그램 파일을 설치합니다.

   이러한 파일을 설치하는 컴퓨터는 Repeater를 실행하는 데 사용되므로 설치 디렉토리에 [!DNL D:\Adobe\Repeater]와 같은 설명적인 이름을 지정하는 것이 좋습니다.

1. [디지털 인증서 다운로드 및 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)에 설명된 대로 [!DNL Insight Server] 디지털 인증서를 설치합니다.

   Adobe 라이센스 서버에 로그인한 후에는 지정된 반복 컴퓨터의 서버 일반 이름과 일치하는 인증서 이름을 찾아보십시오.

1. [포트 설정 확인](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64)에 설명된 대로 [!DNL Communications.cfg] 파일의 포트 설정을 확인합니다.

   동일한 시스템에서 실행되는 다른 프로세스에서 할당된 포트(포트 및 SSL 포트)를 사용하는 경우 포트 할당을 사용하지 않는 쌍으로 변경해야 합니다.

1. 필요한 경우 이 컴퓨터에 저장 및 수집될 [!DNL Sensor] 데이터의 로그 디렉터리를 변경하십시오. 자세한 내용은 [이벤트 데이터 공간 모니터링](../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440)을 참조하십시오.
1. [액세스 제어 파일 업데이트](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d)에 설명된 대로 [!DNL Insight]에서 [!DNL Insight Server]에 대한 관리 액세스를 허용하도록 [!DNL Access Control.cfg] 파일을 수정합니다.
1. [!DNL server.address] 파일을 수정하여 [서버의 네트워크 위치 정의](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)에 정의된 대로 서버의 네트워크 위치를 정의합니다.
1. Windows 메모리 사용 매개 변수를 설정합니다.
1. [Insight 서버를 Windows 서비스](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)로 등록에 설명된 대로 [!DNL Insight Server]을(를) Windows 서비스로 등록합니다.
