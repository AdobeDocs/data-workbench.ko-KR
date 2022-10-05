---
description: 보고서 서버를 등록하고 실행하는 단계입니다.
title: 보고서 서버를 Windows 서비스로 등록
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
exl-id: 46ea5dd4-7041-451e-91e5-f927873fc7d7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 3%

---

# 보고서 서버를 Windows 서비스로 등록{#registering-report-server-as-a-windows-service}

{{eol}}

보고서 서버를 등록하고 실행하는 단계입니다.

이 절차를 수행하기 전에 [!DNL Report Server] 서비스가 실행됩니다. 생성된 보고서가 저장된 위치에 액세스할 수 있는 적절한 권한이 이 계정에 있는지 확인합니다(즉, [!DNL Local System Account]).

시작하려면 아래 절차를 따르십시오 [!DNL Report Server]. 시작할 때 [!DNL Report Server] 처음으로 자동으로 Windows 서비스로 등록됩니다.

시작할 때 [!DNL Report Server] 처음으로 디지털 인증서를 등록하기 위해 Adobe 라이센스 서버에 자동으로 연결됩니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

1. Windows에서 설치한 디렉토리로 이동합니다 [!DNL Report Server].

   예: D:\Adobe\Report

1. 두 번 클릭 **[!UICONTROL ReportServer.exe]**.
1. 이를 확인하려면 [!DNL Report Server] 올바르게 실행되고 있는 경우 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.
1. 서비스 목록에서 [!DNL Report Server] 시작 상태이고 시작 유형이 자동인지 확인합니다.
1. 다음을 수행하여 다음 사용자 계정을 지정합니다. [!DNL Report Server] 실행됨:

   1. 두 번 클릭 **[!UICONTROL Report Server]** 열다 [!DNL Properties] 창을 엽니다.

   1. 을(를) 선택합니다 **[!UICONTROL Log On]** 탭.
   1. 을(를) 선택합니다 **[!UICONTROL This account]** 라디오 단추입니다.
   1. 계정 이름을 입력하거나 찾아봅니다. 이 계정에는 생성된 보고서가 저장된 위치에 액세스할 수 있는 권한이 있어야 합니다.

      >[!NOTE]
      >
      >If [!DNL Report Server] 보고서를 Microsoft Excel로 배포( [!DNL .xls] 또는 [!DNL .xlsx]) 파일에서, 계정에 Microsoft Excel을 실행할 수 있는 권한도 있는지 확인하십시오.

   1. 계정의 암호를 입력하고 확인합니다.
   1. 클릭 **[!UICONTROL OK]**.

1. 마우스 오른쪽 단추를 클릭합니다. [!DNL Report Server] 서비스를 선택하고 **[!UICONTROL Restart]** 지정한 계정에서 서비스를 다시 시작하려면 다음을 수행하십시오.
1. 다음을 확인하려면 [!DNL Report Server] 시작하는 동안 오류가 발생하면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 왼쪽 창에서 [!DNL Event Viewer] 창에서 응용 프로그램 로그를 선택합니다.
   1. 오른쪽 창에서 [!DNL Source] 열.
   1. Adobe에서 오류가 발견되면 오류를 두 번 클릭하여 [!DNL Event Properties] 창을 엽니다. 이 창에서는 오류에 대한 자세한 정보를 제공합니다.

      >[!NOTE]
      >
      >다음 이후 [!DNL Report Server] 서비스가 시작되고, 파일이 [!DNL ReportServer.log] 보고서 서버에서 만들어집니다. [!DNL Trace] 디렉토리. 이 파일은 [!DNL Report Server].

설치를 완료했습니다. [!DNL Report Server]. [!DNL Report Server] 는 지속적으로 실행되도록 설계되었습니다. 시스템을 다시 시작하면 [!DNL Report Server] 자동으로 다시 시작됩니다. 시작하고 중지해야 하는 경우 [!DNL Report Server] 수동으로 이렇게 하려면 [!DNL Services] Windows의 제어판
