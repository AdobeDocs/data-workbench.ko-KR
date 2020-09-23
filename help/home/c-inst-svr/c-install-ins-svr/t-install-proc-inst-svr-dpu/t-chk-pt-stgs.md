---
description: 기본적으로 Insight 서버는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.
solution: Analytics
title: 포트 설정 확인
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---


# 포트 설정 확인{#checking-the-port-settings}

기본적으로 Insight 서버는 포트 80(HTTP용) 및 443(HTTPS용)에서 수신합니다.

이러한 포트가 이미 설치되어 있는 컴퓨터의 다른 프로세스에 의해 할당된 경우 다음 절차 [!DNL Insight Server]를 사용하여 [!DNL Insight Server’s] 포트 할당을 변경합니다.

**포트 할당을 변경하려면**

1. 설치한 디렉토리 [!DNL Components] 의 폴더로 이동합니다 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\Components]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Communications.cfg] 파일을 엽니다.
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

1. 사용할 포트가 아닌 경우 포트 할당 [!DNL Insight Server] 을 변경한 다음 파일을 저장하고 닫습니다.
