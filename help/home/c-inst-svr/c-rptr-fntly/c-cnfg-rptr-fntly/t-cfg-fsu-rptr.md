---
description: 반복에서 사용할 Insight Server FSU를 설치 및 구성하는 지침
title: 반복을 위한 Insight Server FSU 구성
uuid: c2bae862-37d3-4841-b31b-59593c1e4316
exl-id: dacbabd5-f6f5-4201-8709-146075eae679
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 5%

---

# 반복을 위한 Insight Server FSU 구성{#configuring-an-insight-server-fsu-for-repeater}

{{eol}}

반복에서 사용할 Insight Server FSU를 설치 및 구성하는 지침

다음 작업을 순서대로 완료합니다. 다음을 수행하도록 해야 하는 모든 예외 또는 변경 사항 [!DNL Insight Server] FSU는 각 단계 후에 반복 서버로 사용할 수 있습니다.

1. 설치 [!DNL Insight Server] 에 설명된 프로그램 파일 [Insight Server 설치](../../../../home/c-inst-svr/c-install-ins-svr/c-install-ins-svr.md#concept-1c796b4ca427474f99ec6ba34d8254cd).

   이러한 파일을 설치하는 시스템은 Repeater를 실행하는 데 사용되므로 설치 디렉토리에 다음과 같은 설명 이름을 지정하는 것이 좋습니다 [!DNL D:\Adobe\Repeater].

1. 설치 [!DNL Insight Server] 에 설명된 대로 디지털 인증서 [디지털 인증서 다운로드 및 설치](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).

   Adobe 라이선스 서버에 로그인한 후에는 지정된 반복 시스템의 서버 일반 이름과 일치하는 인증서 이름을 찾아야 합니다.

1. 에서 포트 설정을 확인합니다. [!DNL Communications.cfg] 에 설명된 대로 [포트 설정 확인](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64).

   할당된 포트(포트 및 SSL 포트)를 동일한 컴퓨터에서 실행 중인 다른 프로세스에서 사용하는 경우 포트 할당을 사용하지 않는 쌍으로 변경해야 합니다.

1. 필요한 경우 의 로그 디렉토리를 변경합니다. [!DNL Sensor] 이 컴퓨터에 수집하고 저장할 데이터입니다. 자세한 내용은 [이벤트 데이터 공간 모니터링](../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440).
1. 수정 [!DNL Access Control.cfg] 파일에 대한 관리자 액세스 허용 [!DNL Insight Server] 변환 전: [!DNL Insight] 에 설명된 대로 [액세스 제어 파일 업데이트](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d).
1. 수정 [!DNL server.address] 파일에 정의된 대로 서버의 네트워크 위치를 정의하는 파일 [서버의 네트워크 위치 정의](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).
1. Windows 메모리 사용률 매개 변수를 설정합니다.
1. 등록 [!DNL Insight Server] 에 설명된 대로 [Insight Server를 Windows 서비스로 등록](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).
