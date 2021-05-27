---
description: 보고서 포털을 가상 디렉터리(IIS 6.0)에 매핑하는 단계입니다.
title: 보고서 포털을 가상 디렉터리에 매핑(IIS 6.0)
uuid: e09d23d7-09de-4180-8260-60527f47aa98
exl-id: 39335705-7391-49af-a63d-c0fe4ca3f8f0
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 3%

---

# 보고서 포털을 가상 디렉터리에 매핑(IIS 6.0){#mapping-report-portal-to-a-virtual-directory-iis}

보고서 포털을 가상 디렉터리(IIS 6.0)에 매핑하는 단계입니다.

[!DNL Report Portal]을 IIS 6.0의 가상 디렉터리에 매핑하려면 다음 세 가지 별도의 작업이 필요합니다.

1. [구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-eaf1c58935074cfa840dac33e1286520)
1. [구성 파일을 IIS로 가져오기](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-9d61f6bfa93846dcb96973fec5573b19)
1. [IIS에서 ASP(Active Server Pages) 사용](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-a7725ec2afc64ffc854c5bd8c5c31802)

세 가지 작업을 모두 완료해야 합니다.

## 구성 파일 {#section-eaf1c58935074cfa840dac33e1286520}을 편집하려면

1. [!DNL Report Portal]이 설치된 컴퓨터에서 메모장과 같은 텍스트 편집기에서 \*PortalName*\ReportPortalSetup.xml을 엽니다.

1. 편집기의 찾기 및 바꾸기 기능을 사용하여 문자열 &quot;VSVirtualPortalName&quot;을 포털의 이름으로 전체적으로 바꾸기(모두 바꾸기)합니다. 예를 들어 &quot;VisualReportPortal&quot;을 [!DNL Report Portal]의 이름으로 사용하려면 &quot;VSVirtualPortalName&quot;을 검색하고 &quot;VisualReportPortal&quot;로 바꿉니다.
1. 이 파일에서 다음 요소를 찾습니다.

   ```
   <IIsWebVirtualDir Location= "/LM/W3SVC/1/Root/PortalName/Output" AccessFlags="AccessRead | AccessScript” AppFriendlyName="Output" . . . >
   ```

1. 이 요소의 [!DNL Path] 속성을 [!DNL Report Server] 이 보고서 세트의 출력을 저장하는 디렉토리의 실제 위치로 설정합니다.

   출력 폴더는 모든 위치에 있을 수 있으며, 모든 이름을 지정할 수 있으며, 각 보고서 세트의 하위 폴더를 포함합니다.

   >[!NOTE]
   >
   >보고서 세트에 대한 [!DNL Report.cfg] 파일의 출력 루트 매개 변수에서 지정하는 디렉토리와 같아야 합니다. 자세한 내용은 [Report.cfg 파일 구성](../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d)을 참조하십시오.

   다음 코드 샘플은 보고서가 [!DNL E:\VSReport\ReportOutput]에 저장된 경우 [!DNL Path] 속성을 설정하는 방법을 보여 줍니다.

   ```
   < . . . 
   AppIsolated="2" 
       AppRoot="/LM/W3SVC/1/Root/PortalName/OutputFolder" 
       DirBrowseFlags="DirBrowseShowDate | DirBrowseShowTime |...  
       Path="E:\VSReport\ReportOutput"
   ```

   >[!NOTE]
   >
   >[!DNL Path] 특성이 올바르게 설정되어야 합니다.

1. [!DNL Output] 요소의 기본 [!DNL Path]을 변경한 경우 *\PortalName*\PortalFiles\Output folder to the output directory that you specified in Step 4에서 [!DNL profiles.xml] 파일을 이동합니다. 위의 예에서는 [!DNL profiles.xml] 을 [!DNL E:\VSReport\ReportOutput](으)로 이동합니다.

1. 다른 모든 [!DNL IIsWebVirtualDir] 요소에 대한 [!DNL Path] 속성이 [!DNL C:\Inetpub\wwwroot] 의 모든 인스턴스를 검색하여 올바른 경로로 대체하여 올바른 위치에 매핑되어 있는지 확인합니다.

1. 파일을 저장합니다. 원본 파일을 유지하려면 새 이름을 사용하여 구성 파일을 저장할 수 있습니다.

## 구성 파일을 IIS {#section-9d61f6bfa93846dcb96973fec5573b19}에 가져오려면

1. [!DNL Report Portal]이 설치된 컴퓨터에서 **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Systems (IIS) Manager]**&#x200B;을 사용하여 IIS 관리자를 시작합니다.

1. 선택 **[!UICONTROL (local computer)]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. **[!UICONTROL Default Web Site]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]** (파일에서)를 선택합니다.

1. **[!UICONTROL ReportPortalSetup.xml]** 파일을 선택하고 **[!UICONTROL Read File]** 를 클릭합니다.

1. 다음 예와 같이 6개의 가상 디렉터리가 [!DNL Report Portal]에 나열되는지 확인합니다.

   ![](assets/rptPort_dia_VirDirs.png)

   6개의 가상 디렉터리가 표시되지 않거나 오류 메시지가 표시되면 **[!UICONTROL Cancel]** 을 클릭하고 구성 파일에서 오류가 있는지 검사합니다.

1. 목록에서 첫 번째 가상 디렉터리(다른 5개의 상위 디렉터리)를 선택하고 **[!UICONTROL OK]**&#x200B;을 클릭합니다. IIS는 매핑을 가져오고 가상 디렉터리를 기본 웹 사이트에 추가합니다.

   다음 예제와 같이 결과 디렉토리 구조에 하나의 상위 폴더(포털과 동일한 이름)와 5개의 하위 디렉토리가 있는지 확인합니다.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. 각 가상 디렉터리를 클릭하여 IIS가 나타내는 실제 디렉터리를 찾을 수 있는지 확인합니다. IIS에 오류가 표시되면 가상 디렉터리 이름을 마우스 오른쪽 단추로 클릭하고 [!DNL Local Path] 필드가 올바른 실제 디렉터리를 가리키는지 확인합니다.

## IIS {#section-a7725ec2afc64ffc854c5bd8c5c31802}에서 활성 서버 페이지(ASP)를 활성화하려면

[!DNL Report Portal]을 사용하려면 IIS에서 ASP를 사용하도록 설정해야 합니다. 기본적으로 IIS 6.0이 설치되면 ASP가 비활성화됩니다. 다음 절차를 사용하여 IIS에서 ASP가 활성화되어 있는지 확인합니다.

1. IIS 관리자 창에서 **[!UICONTROL (local computer)]** > **[!UICONTROL Web Service Extensions]**&#x200B;을 선택합니다.
1. [!DNL Active Server Pages] 확장이 [!DNL Allowed] 로 설정되어 있는지 확인합니다.

   ![](assets/report_aspenable.png)

1. 상태가 금지된 경우 **[!UICONTROL Active Server Pages]** 을 선택하고 **[!UICONTROL Allow]** 를 클릭합니다.
1. IIS 관리자를 닫습니다.
