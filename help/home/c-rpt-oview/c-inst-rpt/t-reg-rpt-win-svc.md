---
description: 보고서 서버를 등록하고 실행하는 절차.
solution: Analytics
title: 보고서 서버를 Windows 서비스로 등록
topic: Data workbench
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 서버를 Windows 서비스로 등록{#registering-report-server-as-a-windows-service}

보고서 서버를 등록하고 실행하는 절차.

이 절차를 수행하기 전에 서비스를 실행할 Windows 계정을 [!DNL Report Server] 식별합니다. 생성된 보고서가 저장되는 위치(즉, 를 사용하지 않음)에 액세스할 수 있는 적절한 권한이 이 계정에 있는지 [!DNL Local System Account]확인하십시오.

아래 절차를 사용하여 [!DNL Report Server]시작하십시오. 처음 시작할 [!DNL Report Server] 때 Windows 서비스로 자동으로 등록됩니다.

처음 시작할 [!DNL Report Server] 때 Adobe License Server에 자동으로 연결하여 디지털 인증서를 등록합니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

1. Windows에서 설치한 디렉토리로 이동합니다 [!DNL Report Server].

   예:D:\Adobe\Report

1. Double-click **[!UICONTROL ReportServer.exe]**.
1. 올바르게 실행되고 [!DNL Report Server] 있는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.
1. 서비스 목록에서 에 대한 항목을 찾아 [!DNL Report Server] 상태가 시작이고 시작 유형이 자동인지 확인합니다.
1. 다음을 수행하여 [!DNL Report Server] 실행할 사용자 계정을 지정합니다.

   1. 두 번 **[!UICONTROL Report Server]** 클릭하여 [!DNL Properties] 창을 엽니다.

   1. 탭을 **[!UICONTROL Log On]** 선택합니다.
   1. 라디오 단추를 **[!UICONTROL This account]** 선택합니다.
   1. 계정 이름을 입력하거나 찾습니다. 이 계정에는 생성된 보고서가 저장되는 위치에 액세스할 수 있는 권한이 있어야 합니다.

      >[!NOTE]
      >
      >보고서를 Microsoft Excel( [!DNL Report Server] 또는 [!DNL .xls] [!DNL .xlsx]) 파일로 배포하는 경우 계정에 Microsoft Excel 실행 권한도 있는지 확인하십시오.

   1. 계정의 암호를 입력하고 확인합니다.
   1. 클릭 **[!UICONTROL OK]**.

1. 서비스를 마우스 오른쪽 단추로 클릭하고 [!DNL Report Server] 지정한 계정 아래에서 서비스를 **[!UICONTROL Restart]** 다시 시작하려면 선택합니다.
1. 시작 중에 오류가 [!DNL Report Server] 발생했는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 창의 왼쪽 창에서 애플리케이션 로그를 [!DNL Event Viewer] 선택합니다.
   1. 오른쪽 창에서 [!DNL Source] 열에서 Adobe가 있는 이벤트를 찾습니다.
   1. Adobe에서 오류가 발견되면 오류를 두 번 클릭하여 [!DNL Event Properties] 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

      >[!NOTE]
      >
      >서비스가 [!DNL Report Server] 시작되면 보고서 서버 [!DNL ReportServer.log] [!DNL Trace] 디렉토리에 파일이 만들어집니다. 이 파일은 관련 문제를 해결하는 데에도 유용합니다 [!DNL Report Server].

설치를 완료했습니다 [!DNL Report Server]. [!DNL Report Server] 가 계속 실행되도록 설계되었습니다. 시스템을 다시 시작하면 자동으로 [!DNL Report Server] 다시 시작됩니다. 수동으로 시작 및 중지해야 하는 경우 Windows의 [!DNL Report Server] [!DNL Services] 제어판을 사용하여 시작할 수 있습니다.
