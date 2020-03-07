---
description: 보고서 포털을 가상 디렉터리(IIS 6.0)에 매핑하는 단계입니다.
solution: Analytics
title: 가상 디렉터리에 보고서 포털 매핑(IIS 6.0)
topic: Data workbench
uuid: e09d23d7-09de-4180-8260-60527f47aa98
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 가상 디렉터리에 보고서 포털 매핑(IIS 6.0){#mapping-report-portal-to-a-virtual-directory-iis}

보고서 포털을 가상 디렉터리(IIS 6.0)에 매핑하는 단계입니다.

IIS 6.0 [!DNL Report Portal] 의 가상 디렉터리에 대한 매핑에는 세 가지 별도의 작업이 포함됩니다.

1. [구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-eaf1c58935074cfa840dac33e1286520)
1. [구성 파일을 IIS로 가져오기](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-9d61f6bfa93846dcb96973fec5573b19)
1. [IIS에서 ASP(Active Server Pages) 사용](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-a7725ec2afc64ffc854c5bd8c5c31802)

세 가지 작업을 모두 완료해야 합니다.

## To Edit the Configuration File {#section-eaf1c58935074cfa840dac33e1286520}

1. 설치되어 [!DNL Report Portal] 있는 컴퓨터에서 메모장과 같은 텍스트 편집기에서 \*PortalName*\ReportPortalSetup.xml을 엽니다.

1. 편집기의 찾기 및 바꾸기 기능을 사용하여 문자열 &quot;VSVirtualPortalName&quot;을 포털의 이름으로 전체적으로 바꿉니다(모두 바꾸기). 예를 들어 &quot;VisualReportPortal&quot;을 사용자의 이름으로 사용하려면 &quot;VSVirtualPortalName&quot;을 검색하여 &quot;VisualReportPortal&quot;으로 바꿉니다. [!DNL Report Portal]
1. 이 파일에서 다음 요소를 찾습니다.

   ```
   <IIsWebVirtualDir Location= "/LM/W3SVC/1/Root/PortalName/Output" AccessFlags="AccessRead | AccessScript” AppFriendlyName="Output" . . . >
   ```

1. 이 요소의 속성을 보고서 세트에 대한 출력을 저장하는 디렉토리의 물리적 위치로 [!DNL Path] [!DNL Report Server] 설정합니다.

   출력 폴더는 어느 위치에서나 찾을 수 있으며, 아무 곳이든 이름을 지정할 수 있으며, 각 보고서 세트에 대한 하위 폴더를 포함합니다.

   >[!NOTE]
   >
   >이 디렉토리는 보고서 세트에 대한 파일의 출력 루트 매개 변수에서 지정하는 디렉토리와 같아야 합니다. [!DNL Report.cfg] 자세한 내용은 Report.cfg [파일 구성을 참조하십시오](../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d).

   다음 코드 샘플에서는 보고서를 저장할 때 [!DNL Path] 속성을 설정하는 방법을 보여 줍니다 [!DNL E:\VSReport\ReportOutput].

   ```
   < . . . 
   AppIsolated="2" 
       AppRoot="/LM/W3SVC/1/Root/PortalName/OutputFolder" 
       DirBrowseFlags="DirBrowseShowDate | DirBrowseShowTime |...  
       Path="E:\VSReport\ReportOutput"
   ```

   >[!NOTE]
   >
   >속성이 올바르게 설정되어야 합니다 [!DNL Path] .

1. 요소의 기본값을 변경한 [!DNL Path] 경우 [!DNL Output] \PortalName \PortalFiles\Output folder to the output directory that you specified in Step 4폴더에서 [!DNL profiles.xml] 파일을 *이동합니다*. 위의 예에서 [!DNL profiles.xml] 로 [!DNL E:\VSReport\ReportOutput]이동합니다.

1. 모든 다른 [!DNL Path] 요소의 [!DNL IIsWebVirtualDir] 속성을 올바른 위치에 매핑하고 각 인스턴스를 올바른 [!DNL C:\Inetpub\wwwroot] 경로로 대체하여 확인합니다.

1. 파일을 저장합니다. 원본 파일을 보존하려면 새 이름을 사용하여 구성 파일을 저장할 수 있습니다.

## 구성 파일을 IIS로 가져오려면 {#section-9d61f6bfa93846dcb96973fec5573b19}

1. 설치되어 [!DNL Report Portal] 있는 컴퓨터에서 **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Systems (IIS) Manager]**&#x200B;를 사용하여 IIS 관리자를 시작합니다.

1. 선택 **[!UICONTROL (local computer)]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Default Web Site]** > **[!UICONTROL New]** **[!UICONTROL Virtual Directory]** (파일에서)을 선택합니다.

1. 파일을 **[!UICONTROL ReportPortalSetup.xml]** 선택하고 을 클릭합니다 **[!UICONTROL Read File]**.

1. 다음 예와 [!DNL Report Portal] 같이 6개의 가상 디렉토리가 사용자에게 나열되어 있는지 확인합니다.

   ![](assets/rptPort_dia_VirDirs.png)

   6개의 가상 디렉토리가 표시되지 않거나 오류 메시지가 표시되는 경우 구성 파일을 클릭하여 오류를 **[!UICONTROL Cancel]** 검사합니다.

1. 목록에서 첫 번째 가상 디렉터리(나머지 다섯 개의 상위 디렉터리)를 선택하고 을 클릭합니다 **[!UICONTROL OK]**. IIS는 매핑을 가져오고 가상 디렉터리를 기본 웹 사이트에 추가합니다.

   다음 예와 같이 결과 디렉토리 구조에 상위 폴더(포털과 동일한 이름)와 하위 디렉토리 5개가 있는지 확인합니다.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. 각 가상 디렉터리를 클릭하여 IIS가 나타내는 실제 디렉터리를 찾을 수 있도록 합니다. IIS에 오류가 표시되면 가상 디렉터리 이름을 마우스 오른쪽 단추로 클릭하고 [!DNL Local Path] 필드가 올바른 실제 디렉터리를 가리키는지 확인합니다.

## IIS에서 ASP(Active Server Pages)를 활성화하려면 {#section-a7725ec2afc64ffc854c5bd8c5c31802}

사용하려면 IIS에서 ASP를 [!DNL Report Portal]활성화해야 합니다. 기본적으로 IIS 6.0이 설치되면 ASP가 비활성화됩니다. 다음 절차를 사용하여 IIS에서 ASP가 활성화되어 있는지 확인합니다.

1. IIS 관리자 창에서 **[!UICONTROL (local computer)]** > **[!UICONTROL Web Service Extensions]**&#x200B;을 선택합니다.
1. 확장이 [!DNL Active Server Pages] 로 설정되어 있는지 확인합니다 [!DNL Allowed].

   ![](assets/report_aspenable.png)

1. [상태]가 [금지됨]인 경우 을 선택하고 **[!UICONTROL Active Server Pages]** 클릭합니다 **[!UICONTROL Allow]**.
1. IIS 관리자를 닫습니다.

