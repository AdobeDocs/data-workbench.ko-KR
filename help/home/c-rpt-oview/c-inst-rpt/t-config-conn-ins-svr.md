---
description: 보고서 및 경고를 생성하려면 먼저 보고서 서버가 Insight 서버의 주소를 지정하고 보고할 프로파일을 식별하도록 구성해야 합니다.
title: Insight Server에 연결 구성
uuid: 2018b67e-90a6-41d7-b628-4b463869df6e
exl-id: a398a665-fe09-448a-977c-b0f9de4add09
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---

# Insight Server에 연결 구성{#configuring-the-connection-to-the-insight-server}

보고서 및 경고를 생성하려면 먼저 보고서 서버가 Insight 서버의 주소를 지정하고 보고할 프로파일을 식별하도록 구성해야 합니다.

>[!NOTE]
>
>아래에 설명된 대로 보고서 서버를 구성할 때까지 보고서 서버를 성공적으로 실행할 수 없습니다. 프로그램과 함께 설치되는 구성되지 않은 파일로 보고서 서버를 실행하려고 하면 보고서 서버에서 오류 스트림을 생성합니다.

**보고서 서버를 구성하려면**

1. Windows 탐색기에서 보고서 서버를 설치한 디렉토리로 이동합니다.
1. 메모장에서 [!DNL ReportServer.cfg] 파일을 열고 원하는 대로 파일을 수정합니다.

   다음 샘플 [!DNL Report Server.cfg]에는 기본적으로 [!DNL Report Server.cfg] 파일에 포함된 매개 변수만 포함되어 있습니다(필요한 매개 변수 설정이 강조 표시됨). 프록시 서버를 통해 Adobe 라이센스 서버에 문의하는 경우 라이센스 벡터와 해당 매개 변수를 추가해야 합니다. 자세한 설명은 [보고서 서버.cfg 매개 변수](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-svr-param.md#concept-53359b328fd140d593c3f2fc0031be06)를 참조하십시오.

   ```
   Fonts = vector: 0 items
   Gamma = float: 1.6
   Network Location = string: NetworkLocationName
   Servers = vector: 1 items
     0 = serverInfo:
       Address = string: ServerIPAddress
       Name = string: 
       Port = int: 443
       Proxy Address = string:
       Proxy Password = string:
       Proxy Port = int: 8080
       Proxy User Name = string:
       SSL Client Certificate = string: ReportCertFileName.pem
       SSL Server Common Name = string: ServerCommonName
       Use SSL = bool: true
   Result Memory Limit (KB) = double: 100000
   Maximum Slice Size = int: 30
   Use OpenGL Hardware Rendering = bool: true
   Reporting = :
     Profiles = vector: 1 items
       0 = ReportProfile:
         Server = string: ServerCommonName
         Profile = string: ProfileName
     Update Interval (minutes) = int: 10
     Completion Message Interval (seconds) = int: 600
     Status interval (seconds) = int: 600
     SMTP Server for Errors = string: SMTPServerHostName
     SMTP Server for Errors Username = string: SMTPServerUsername
     SMTP Server for Errors Password = string: SMTPServerPassword
     SMTP Server for Errors Send From = string: SenderAddress
     SMTP Server for Errors Send To = string: RecipientAddresses
   ```

1. 파일을 저장하고 닫습니다.
