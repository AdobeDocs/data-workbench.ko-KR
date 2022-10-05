---
description: 기본적으로 Insight Server는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.
title: 포트 설정 확인
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
exl-id: 924860e3-5afa-4c0f-bb7a-d38d5c1355b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# 포트 설정 확인{#checking-the-port-settings}

{{eol}}

기본적으로 Insight Server는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.

이러한 포트가 이미 설치된 시스템의 다른 프로세스에 의해 할당된 경우 [!DNL Insight Server]를 변경하려면 다음 절차를 따르십시오 [!DNL Insight Server’s] 포트 할당

**포트 할당을 변경하려면**

1. 로 이동합니다 [!DNL Components] 설치한 디렉토리의 폴더 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\Components]

1. 를 엽니다. [!DNL Communications.cfg] 메모장과 같은 텍스트 편집기에 있는 파일입니다.
1. 다음과 같이 포트 및 SSL 포트 항목을 찾습니다.

   ```
   component = CommServer: 
     Access Control File = Path: Access Control\\Access Control.cfg
     Access Log Directory = string: P:\\Audit\\
     IP Interface = string: 
     Port = int: 80
     SSL Port = int: 443
     Servers = vector: 17 items
       0 = InitServer: 
         Client Type = string: Sensor
         URI = string: /SensorInit.vsp
     . . .
   ```

1. 원하는 포트가 아닌 경우 [!DNL Insight Server] 사용하려면 포트 할당을 변경한 다음 파일을 저장하고 닫습니다.
