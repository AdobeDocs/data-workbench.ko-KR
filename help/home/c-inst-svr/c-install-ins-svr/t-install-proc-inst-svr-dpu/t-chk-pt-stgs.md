---
description: 기본적으로 Insight Server는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.
solution: Insight
title: 포트 설정 확인
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 포트 설정 확인{#checking-the-port-settings}

기본적으로 Insight Server는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.

이러한 포트가 이미 설치된 컴퓨터의 다른 프로세스에 의해 할당된 [!DNL Insight Server]경우 다음 절차를 사용하여 [!DNL Insight Server’s] 포트 할당을 변경합니다.

**포트 할당을 변경하려면**

1. 설치한 디렉토리의 [!DNL Components] 폴더로 [!DNL Insight Server]이동합니다.

   예: [!DNL C:\Adobe\Server\Components]

1. 메모장과 같은 텍스트 편집기에서 파일을 [!DNL Communications.cfg] 엽니다.
1. 아래와 같이 포트 및 SSL 포트 항목을 찾습니다.

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

1. 사용할 포트가 아닌 [!DNL Insight Server] 경우 포트 할당을 변경한 다음 파일을 저장하고 닫습니다.
