---
description: 보고서 서버를 등록 및 실행하는 절차.
title: 보고서 서버를 Windows 서비스로 등록
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
exl-id: 46ea5dd4-7041-451e-91e5-f927873fc7d7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 3%

---

# 보고서 서버를 Windows 서비스로 등록{#registering-report-server-as-a-windows-service}

보고서 서버를 등록 및 실행하는 절차.

이 절차를 수행하기 전에 [!DNL Report Server] 서비스를 실행할 Windows 계정을 식별합니다. 생성된 보고서가 저장되는 위치(즉, [!DNL Local System Account] 사용 안 함)에 액세스할 수 있는 적절한 권한이 이 계정에 있는지 확인하십시오.

[!DNL Report Server]을(를) 시작하려면 아래 절차를 사용하십시오. 처음으로 [!DNL Report Server]을(를) 시작하면 Windows 서비스로 자동으로 등록됩니다.

처음으로 [!DNL Report Server]을(를) 시작하면 Adobe 라이센스 서버에 자동으로 연결하여 디지털 인증서를 등록합니다. 등록 프로세스를 성공적으로 완료하려면 다음 단계를 실행할 때 컴퓨터가 인터넷에 연결되어 있어야 합니다.

1. Windows에서 [!DNL Report Server]을(를) 설치한 디렉토리로 이동합니다.

   예:D:\Adobe\Report

1. **[!UICONTROL ReportServer.exe]**&#x200B;을(를) 두 번 클릭합니다.
1. [!DNL Report Server]이(가) 올바르게 실행되고 있는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 다를 수 있습니다.
1. 서비스 목록에서 [!DNL Report Server] 항목을 찾아 상태가 시작이고 시작 유형이 자동인지 확인합니다.
1. [!DNL Report Server]이(가) 실행될 사용자 계정을 지정하려면 다음을 수행합니다.

   1. **[!UICONTROL Report Server]**&#x200B;을 두 번 클릭하여 [!DNL Properties] 창을 엽니다.

   1. **[!UICONTROL Log On]** 탭을 선택합니다.
   1. **[!UICONTROL This account]** 라디오 단추를 선택합니다.
   1. 계정 이름을 입력하거나 찾아봅니다. 생성된 보고서가 저장되는 위치에 액세스할 수 있는 권한이 이 계정에 있어야 합니다.

      >[!NOTE]
      >
      >[!DNL Report Server]이(가) 보고서를 Microsoft Excel( [!DNL .xls] 또는 [!DNL .xlsx]) 파일로 배포하는 경우 계정에 Microsoft Excel을 실행할 수 있는 권한도 있는지 확인하십시오.

   1. 계정의 암호를 입력하고 확인합니다.
   1. 클릭 **[!UICONTROL OK]**.

1. [!DNL Report Server] 서비스를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Restart]**&#x200B;을 선택하여 지정한 계정에서 서비스를 다시 시작합니다.
1. 시작 중에 [!DNL Report Server]에 오류가 있는지 확인하려면 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**&#x200B;를 클릭합니다. 이 명령 시퀀스는 사용 중인 Windows 버전에 따라 다를 수 있습니다.

   1. [!DNL Event Viewer] 창의 왼쪽 창에서 애플리케이션 로그를 선택합니다.
   1. 오른쪽 창에서 [!DNL Source] 열에서 Adobe이 있는 이벤트를 찾습니다.
   1. Adobe에서 오류가 발견되면 오류를 두 번 클릭하여 [!DNL Event Properties] 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

      >[!NOTE]
      >
      >[!DNL Report Server] 서비스가 시작되면 보고서 서버 [!DNL Trace] 디렉터리에 [!DNL ReportServer.log] 파일이 만들어집니다. 이 파일은 [!DNL Report Server] 관련 문제를 해결하는 데에도 유용합니다.

[!DNL Report Server] 설치를 완료했습니다. [!DNL Report Server] 는 지속적으로 실행되도록 설계되었습니다. 컴퓨터를 다시 시작하면 [!DNL Report Server]이(가) 자동으로 다시 시작됩니다. [!DNL Report Server]을(를) 수동으로 시작 및 중지해야 하는 경우 Windows의 [!DNL Services] 제어판을 사용하여 시작할 수 있습니다.
