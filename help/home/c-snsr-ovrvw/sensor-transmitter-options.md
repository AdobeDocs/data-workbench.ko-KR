---
description: UNIX 및 Windows용 센서 송신기 시작 명령에 대한 정보입니다.
title: 센서 송신기 명령줄 옵션
uuid: 8d077d76-a709-494e-a176-07ca3e761662
exl-id: f4b27859-8fab-42cd-bad0-b32f87764668
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 6%

---

# 센서 송신기 명령줄 옵션{#sensor-transmitter-command-line-options}

{{eol}}

UNIX 및 Windows용 센서 송신기 시작 명령에 대한 정보입니다.

## UNIX용 Start-up 명령 {#section-e8e7a6e62971499ba5f633d896590949}

UNIX 시스템에서 센서 송신기를 시작하려면 다음 명령을 사용합니다.

```
txlogd -f configFileName
```

여기서 configFileName은 송신기 구성 파일의 정규화된 이름(txlogd.conf)입니다.

기본적으로 송신기는 백그라운드 프로세스(데몬)로 실행되고 syslog에 운영 메시지를 기록합니다.

다음은 txlogd용 명령줄 스위치의 전체 목록입니다.

| 스위치 | 설명 |
|---|---|
| -f | 구성 파일의 정규화된 이름(txlogd.conf)을 지정합니다. 이 스위치를 지정하지 않으면 송신기가 현재 디렉토리에서 txlogd.conf를 찾습니다. |
| -n | 백그라운드 프로세스가 아닌 대화형 모드로 전송기를 시작합니다. |
| -i | 인터랙티브 모드로 전송기를 시작하고 디버그 출력을 stdout으로 보냅니다. |
| -d | 송신기를 백그라운드 프로세스로 시작하고 디버그 출력을 현재 디렉토리의 txlogd-debug.log로 보냅니다. |
| -c | 전송기를 시작하고 디스크 큐 파일이 없는 경우 디스크 큐 파일을 만듭니다. 디스크 큐가 이미 있으면 이 매개 변수는 무시됩니다. |
| -x | 송신기를 시작하고 디스크 큐에서 마지막 패킷을 전송한 후 종료하도록 합니다. 새 큐 파일 만들기와 같은 관리 작업을 준비하기 위해 큐를 드레인하려면 이 옵션을 사용할 수 있습니다. |

## Windows용 시작 명령 {#section-aaafbb68559a45c7a40abe6a4c80ccc0}

Sensor를 시작하고 Windows 시스템에서 서비스로 등록하려면 다음 명령을 사용합니다.

```
txlog /regserver
```
