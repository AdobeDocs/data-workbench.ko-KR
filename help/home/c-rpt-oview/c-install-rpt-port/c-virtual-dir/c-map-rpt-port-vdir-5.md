---
description: 보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 단계입니다.
title: 보고서 포털을 가상 디렉터리에 매핑(IIS 5.0)
uuid: 9514c33e-c139-4cc2-97c2-8b241522c44d
exl-id: 20d8e9ea-c5b6-4a1b-9b15-557cc71ad5d9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 6%

---

# 보고서 포털을 가상 디렉터리에 매핑(IIS 5.0){#mapping-report-portal-to-a-virtual-directory-iis}

{{eol}}

보고서 포털을 가상 디렉터리(IIS 5.0)에 매핑하는 단계입니다.

1. 머신에서 [!DNL Report Portal] 이 설치되어 있으면 다음 중 하나를 사용하여 IIS 관리자를 시작합니다 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]** 또는 **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]**.

1. 선택 **[!UICONTROL Local Machine]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Default Web Site]** 을(를) 선택합니다. **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. 이 [!DNL Virtual Directory Wizard] 열기 **[!UICONTROL Next]**.

1. 다음 단계를 완료하여 루트 가상 디렉토리를 정의합니다. [!DNL Report Portal]:

   1. 별칭을 묻는 메시지가 나타나면 [!DNL Report Portal]를 클릭한 다음 **[!UICONTROL Next]**. 예를 들어 의 이름으로 &quot;Portal&quot;을 사용하려는 경우 [!DNL Report Portal]를 눌러 &quot;Portal&quot; 별칭을 가상 디렉토리에 할당합니다. 완료되면 **[!UICONTROL Next]**&#x200B;를 클릭합니다.

   1. 물리적 경로를 묻는 메시지가 표시되면 을(를) 찾아 선택합니다 *&lt;**[!UICONTROL PortalName]**>* **[!UICONTROL \PortalASP]** 디렉토리 **[!UICONTROL Next]**.

      예: [!DNL C:\Inetpub\wwwroot\Portal\PortalASP]

   1. 권한을 묻는 메시지가 표시되면 다음 옵션이 활성화되어 있는지 확인합니다.

      * **[!UICONTROL Read]**
      * **[!UICONTROL Run scripts (such as ASP)]**
   1. **[!UICONTROL Next]**&#x200B;를 클릭한 다음 **[!UICONTROL Finish]**&#x200B;을 클릭합니다. 생성한 가상 디렉터리가 다음 예와 같이 기본 웹 사이트 아래에 나타납니다.

   ![](assets/RptPort_scrn_VirDirManual.png)

1. 방금 생성한 가상 디렉터리를 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. 를 사용하십시오 [!DNL Virtual Directory] 다음 각 물리적 디렉토리에 대해 별칭을 생성합니다. 이렇게 하면 이러한 각 물리적 리소스에 대해 적절히 이름이 지정된 가상 디렉토리가 생성됩니다.

<table id="table_B2E04423C20F40CAA8EDA3FCBA210AA2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 별칭을 만듭니다 . . . </th> 
   <th colname="col2" class="entry"> 이 물리적 리소스에 대해 입니다. . . </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 코어 </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\Portal파일\코어 </p> <p>예: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Core</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CSS </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\Portal파일\CSS </p> <p>예: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\CSS</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTC </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\Portal파일\HTC </p> <p>예: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\HTC</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이미지 </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\Portal파일\이미지 </p> <p>예: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Images</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>디렉터리가 있는 실제 위치 <span class="keyword"> 보고서 서버</span> 보고서 세트의 출력을 저장합니다. 출력 폴더는 모든 위치에 있을 수 있으며, 모든 이름을 지정할 수 있으며, 각 보고서 세트의 하위 폴더를 포함합니다. </p> <p>이 디렉터리는 의 출력 루트 매개 변수에서 지정하는 디렉터리와 같아야 합니다 <span class="filepath"> Report.cfg</span> 보고서 세트에 대한 파일입니다. 자세한 내용은 <a href="../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d"> Report.cfg 파일 구성</a>. </p> <p>기본 위치는 \ 입니다<i>PortalName</i>\Portal파일\출력. </p> <p>예: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Output</span> </p> <p>다음 <i>PortalName</i>\PortalFiles\Output 디렉터리에 <span class="filepath"> profiles.xml</span> 파일. 이 별칭에 대해 지정한 출력 디렉토리로 이동해야 합니다. </p> <p>중요한 것은 <span class="wintitle"> 경로</span> 속성이 제대로 설정되어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 완료되면 IIS에 6개의 새 가상 디렉터리가 표시되는지 확인합니다. 디렉토리 구조에 아래와 같이 상위 폴더(포털과 동일한 이름)와 하위 폴더 5개가 있는지 확인합니다.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. 완료되면 로 이동합니다. [세션 구성 파일 편집](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7) 설치 프로세스를 계속 진행합니다.
