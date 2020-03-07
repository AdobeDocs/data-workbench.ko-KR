---
description: 보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 단계입니다.
solution: Analytics
title: 가상 디렉터리에 보고서 포털 매핑(IIS 5.0)
topic: Data workbench
uuid: 9514c33e-c139-4cc2-97c2-8b241522c44d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 가상 디렉터리에 보고서 포털 매핑(IIS 5.0){#mapping-report-portal-to-a-virtual-directory-iis}

보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 단계입니다.

1. 시스템이 설치되어 [!DNL Report Portal] 있는 경우, > > > **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]** 있는 위치에서 IIS 관리자를 사용하여 **[!UICONTROL Start]** **[!UICONTROL Administrative Tools]** **[!UICONTROL Internet Information Services]**&#x200B;시작합니다.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Default Web Site]** > **[!UICONTROL New]** **[!UICONTROL Virtual Directory]**&#x200B;을 선택합니다.

1. 이 [!DNL Virtual Directory Wizard] 열리면 을 클릭합니다 **[!UICONTROL Next]**.

1. 다음 단계에 따라 루트 가상 디렉토리를 [!DNL Report Portal]정의합니다.

   1. 별칭을 묻는 메시지가 나타나면 해당 이름을 [!DNL Report Portal]입력한 다음 을 클릭합니다 **[!UICONTROL Next]**. 예를 들어, &quot;Portal&quot;을 사용자의 이름으로 사용하려면 [!DNL Report Portal]가상 디렉토리에 &quot;Portal&quot;이라는 별칭을 지정합니다. 완료되면 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

   1. 물리적 경로를 묻는 메시지가 나타나면 *&lt;**[!UICONTROL PortalName]**>* 디렉토리를 찾아 선택한 다음 을 **[!UICONTROL \PortalASP]** **[!UICONTROL Next]**&#x200B;클릭합니다.

      예: [!DNL C:\Inetpub\wwwroot\Portal\PortalASP]

   1. 권한을 묻는 메시지가 표시되면 다음 옵션이 활성화되어 있는지 확인합니다.

      * **[!UICONTROL Read]**
      * **[!UICONTROL Run scripts (such as ASP)]**
   1. Click **[!UICONTROL Next]**, then click **[!UICONTROL Finish]**. 만든 가상 디렉터리가 다음 예와 같이 기본 웹 사이트 아래에 나타납니다.
   ![](assets/RptPort_scrn_VirDirManual.png)

1. 방금 만든 가상 디렉토리를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**&#x200B;를 선택합니다.

1. 마법사를 사용하여 [!DNL Virtual Directory] 다음 각 물리적 디렉토리에 대한 별칭을 만듭니다. 이렇게 하면 이러한 물리적 리소스 각각에 대해 적절히 이름이 지정된 가상 디렉토리가 생성됩니다.

<table id="table_B2E04423C20F40CAA8EDA3FCBA210AA2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 별칭을 만듭니다... </th> 
   <th colname="col2" class="entry"> 이 물리적 리소스의 경우.. </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 코어 </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Core </p> <p>예:C:\Inetpub\wwwroot\Portal\PortalFiles\Core <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CSS </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\CSS </p> <p>예:C:\Inetpub\wwwroot\Portal\PortalFiles\CSS <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTC </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\HTC </p> <p>예:C:\Inetpub\wwwroot\Portal\PortalFiles\HTC <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이미지 </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Images </p> <p>예:C:\Inetpub\wwwroot\Portal\PortalFiles\Images <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>보고서 서버가 보고서 세트에 대한 <span class="keyword"> 출력을</span> 저장하는 디렉토리의 물리적 위치입니다. 출력 폴더는 어느 위치에서나 찾을 수 있으며, 아무 곳이든 이름을 지정할 수 있으며, 각 보고서 세트에 대한 하위 폴더를 포함합니다. </p> <p>이 디렉토리는 보고서 세트에 대해 Report.cfg 파일의 출력 루트 매개 변수에서 지정한 <span class="filepath"> 디렉토리와</span> 같아야 합니다. 자세한 내용은 Report.cfg <a href="../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d"> 파일 구성을 참조하십시오</a>. </p> <p>기본 위치는 \PortalName<i>\PortalFiles\Output</i>입니다. </p> <p>예:C:\Inetpub\wwwroot\Portal\PortalFiles\Output <span class="filepath"></span> </p> <p>PortalName <i></i>\PortalFiles\Output directory contains the <span class="filepath"> profiles.xml</span> 파일을 이 별칭에 대해 지정한 출력 디렉토리로 이동해야 합니다. </p> <p>Path 속성이 <span class="wintitle"> 제대로</span> 설정되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 완료되면 IIS에 6개의 새 가상 디렉터리가 표시되는지 확인합니다. 디렉토리 구조에 아래와 같이 상위 폴더(포털과 동일한 이름)와 하위 폴더 5개가 있는지 확인하십시오.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. 완료되면 세션 구성 [파일](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7) 편집으로 이동하여 설치 프로세스를 계속합니다.

