---
description: Repeater와 함께 사용할 Insight Server FSU를 설치하고 구성하는 지침
solution: Insight
title: 반복용 Insight Server FSU 구성
uuid: c2bae862-37d3-4841-b31b-59593c1e4316
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 반복용 Insight Server FSU 구성{#configuring-an-insight-server-fsu-for-repeater}

Repeater와 함께 사용할 Insight Server FSU를 설치하고 구성하는 지침

다음 작업을 순서대로 완료합니다. FSU를 반복 서버로 사용할 수 있도록 [!DNL Insight Server] 해야 하는 모든 예외 또는 변경 사항은 각 단계 뒤에 명시됩니다.

1. Insight 서버 설치에 설명된 대로 [!DNL Insight Server] 프로그램 [파일을 설치합니다](../../../../home/c-inst-svr/c-install-ins-svr/c-install-ins-svr.md#concept-1c796b4ca427474f99ec6ba34d8254cd).

   이러한 파일을 설치하는 컴퓨터는 Repeater를 실행하는 데 사용되므로 설치 디렉토리에 설명 이름(예: [!DNL D:\Adobe\Repeater]예:

1. 디지털 인증서 다운로드 및 [!DNL Insight Server] 설치에 설명된 대로 [디지털 인증서를 설치합니다](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).

   Adobe License Server에 로그인한 후에는 지정된 반복기 컴퓨터의 서버 공통 이름과 일치하는 인증서 이름을 찾아야 합니다.

1. 포트 설정 확인 에 설명된 대로 [!DNL Communications.cfg] 파일의 [포트 설정을 확인합니다](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64).

   동일한 시스템에서 실행되는 다른 프로세스에서 할당된 포트(포트 및 SSL 포트)를 사용하는 경우 포트 할당을 사용하지 않는 쌍으로 변경해야 합니다.

1. 필요한 경우 수집 및 저장할 [!DNL Sensor] 데이터의 로그 디렉토리를 변경합니다. 자세한 내용은 이벤트 데이터 [공간 모니터링을 참조하십시오](../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440).
1. 액세스 제어 파일 업데이트에 설명된 [!DNL Access Control.cfg] 대로 파일을 수정하여 [!DNL Insight Server] 관리용 액세스 권한을 부여할 [!DNL Insight] 수 있습니다 [](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d).
1. 서버의 네트워크 위치 정의에 정의된 대로 [!DNL server.address] 파일을 수정하여 서버의 네트워크 [위치를 정의합니다](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).
1. Windows 메모리 사용률 매개 변수를 설정합니다.
1. Insight [!DNL Insight Server] Server를 Windows 서비스로 [등록에 설명된 대로 Windows 서비스로 등록합니다](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).
