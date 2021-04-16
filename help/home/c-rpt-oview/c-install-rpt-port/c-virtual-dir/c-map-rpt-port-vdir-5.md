---
description: 보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 절차.
title: 보고서 포털을 가상 디렉터리에 매핑(IIS 5.0)
uuid: 9514c33e-c139-4cc2-97c2-8b241522c44d
exl-id: 20d8e9ea-c5b6-4a1b-9b15-557cc71ad5d9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 6%

---

# 보고서 포털을 가상 디렉터리에 매핑(IIS 5.0){#mapping-report-portal-to-a-virtual-directory-iis}

보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 절차.

1. [!DNL Report Portal]이(가) 설치된 컴퓨터에서 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]** 또는 **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]**&#x200B;을 사용하여 IIS 관리자를 시작합니다.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. **[!UICONTROL Default Web Site]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**&#x200B;를 선택합니다.

1. [!DNL Virtual Directory Wizard]이(가) 열리면 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

1. 다음 단계를 완료하여 [!DNL Report Portal]에 대한 루트 가상 디렉토리를 정의합니다.

   1. 별칭에 대한 메시지가 표시되면 [!DNL Report Portal] 이름을 입력한 다음 **[!UICONTROL Next]**&#x200B;을 클릭합니다. 예를 들어 &quot;Portal&quot;을 [!DNL Report Portal]의 이름으로 사용하려면 별칭 &quot;포털&quot;을 가상 디렉토리에 할당합니다. 완료되면 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

   1. 물리적 경로를 묻는 메시지가 표시되면 *&lt;**[!UICONTROL PortalName]*** **[!UICONTROL \PortalASP]** 디렉토리를 찾아 선택한 다음 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

      예: [!DNL C:\Inetpub\wwwroot\Portal\PortalASP]

   1. 권한을 묻는 메시지가 표시되면 다음 옵션이 활성화되어 있는지 확인합니다.

      * **[!UICONTROL Read]**
      * **[!UICONTROL Run scripts (such as ASP)]**
   1. **[!UICONTROL Next]**&#x200B;를 클릭한 다음 **[!UICONTROL Finish]**&#x200B;을 클릭합니다. 만든 가상 디렉토리가 다음 예와 같이 기본 웹 사이트 아래에 나타납니다.

   ![](assets/RptPort_scrn_VirDirManual.png)

1. 방금 만든 가상 디렉터리를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**&#x200B;를 선택합니다.

1. [!DNL Virtual Directory] 마법사를 사용하여 다음 각 실제 디렉토리에 대한 별칭을 만듭니다. 이렇게 하면 이러한 각 물리적 리소스에 대해 적절히 이름이 지정된 가상 디렉토리가 만들어집니다.

<table id="table_B2E04423C20F40CAA8EDA3FCBA210AA2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 별칭을 만듭니다... </th> 
   <th colname="col2" class="entry"> 이 물리적 리소스의 경우.. </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Core </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Core </p> <p>예:<span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Core</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CSS </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\CSS </p> <p>예:<span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\CSS</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTC </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\HTC </p> <p>예:<span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\HTC</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이미지 </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Images </p> <p>예:<span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Images</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p><span class="keyword"> 보고서 서버</span>에서 보고서 세트에 대한 출력을 저장하는 디렉토리의 물리적 위치입니다. 출력 폴더는 어디든지 찾을 수 있으며, 아무 이름을 지정할 수 있으며, 각 보고서 세트에 대한 하위 폴더를 포함할 수 있습니다. </p> <p>보고서 세트에 대해 <span class="filepath"> Report.cfg</span> 파일의 출력 루트 매개 변수에서 지정한 디렉터리여야 합니다. 자세한 내용은 <a href="../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d"> Report.cfg 파일 구성</a>을 참조하십시오. </p> <p>기본 위치는 \<i>PortalName</i>\PortalFiles\Output입니다. </p> <p>예:<span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Output</span> </p> <p>이 별칭에 대해 지정한 출력 디렉토리로 이동해야 하는 <i>PortalName</i>\PortalFiles\Output directory contains the <span class="filepath"> profiles.xml</span> 파일. </p> <p><span class="wintitle"> 경로</span> 특성이 올바르게 설정되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 완료되면 IIS에 6개의 새 가상 디렉터리가 표시되는지 확인하십시오. 디렉터리 구조에 아래와 같이 상위 폴더(포털과 동일한 이름)와 하위 폴더 5개가 있는지 확인합니다.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. 완료되면 [세션 구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)으로 이동하여 설치 과정을 계속합니다.
