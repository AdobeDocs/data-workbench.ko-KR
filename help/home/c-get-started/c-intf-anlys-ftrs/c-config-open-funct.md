---
description: 열기 기능을 사용하면 텍스트 편집기 또는 웹 브라우저와 같은 외부 애플리케이션에서 문서 또는 URI와 같은 항목을 열 수 있습니다.
solution: Analytics
title: 개방형 기능 구성
topic: Data workbench
uuid: dfa79a2b-e9ff-4e62-b15b-ae7911adeafd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 개방형 기능 구성{#configure-open-functionality}

열기 기능을 사용하면 텍스트 편집기 또는 웹 브라우저와 같은 외부 애플리케이션에서 문서 또는 URI와 같은 항목을 열 수 있습니다.

현재 열기 기능은 [!DNL Site] 응용 프로그램에서만 구성되며 URI를 여는 경우에만 구성됩니다. 이 섹션에서는 에 대한 Open URI 기능을 구성하는 방법에 대한 정보를 제공합니다 [!DNL Site]. 다른 응용 프로그램에 대해 열기 기능을 구성하거나 다른 항목을 여는 방법에 대한 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오.

에서 페이지 오버레이나 표에서 URI를 마우스 오른쪽 단추로 [!DNL Site]클릭하여 형식이 지정된 응용 프로그램의 URI를 표시할 수 있습니다. 예를 들어 URI 테이블 시각화에서 URI를 클릭하여 웹 브라우저에 웹 페이지를 표시할 수 있습니다.

시각화에서 URI를 열려면 먼저 URI 차원의 [!DNL Open URI.cfg] 파일을 편집하여 데이터 워크벤치가 URI를 여는 데 사용하는 위치 및 이름 지정 규칙을 식별해야 합니다. URI를 기본 형식(예: HTML)으로 보려면 데이터 워크벤치에서 참조된 위치 및 해당 항목을 여는 데 필요한 응용 프로그램에 대한 액세스 권한이 있어야 합니다. 예를 들어, 웹 페이지를 보려면 데이터 워크벤치가 인터넷에 액세스해야 하며 웹 브라우저가 설치되어 있어야 합니다.

**열린 URI.vw를 편집하려면**

1. In the [!DNL Profile Manager], click **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.
1. URI 폴더에서 [!DNL Open URI.vw]파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 파일이 [!DNL .cfg] 파일이면 를 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** 파일이 [!DNL .vw] 파일이면 를 클릭합니다.
1. 을 **[!UICONTROL Command]**&#x200B;클릭한 다음 **[!UICONTROL Parameters]** 파일의 내용을 봅니다.
1. 필요에 따라 [!DNL Site] 매개 변수와 템플릿 매개 변수를 수정합니다.

<table id="table_CDB316DB271F476AB9F9B557B86AFD25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우... </th> 
   <th colname="col2" class="entry"> 이 정보 제공... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>사이트 </p> </td> 
   <td colname="col2"> <p>열려는 URI의 위치입니다. </p> <p>예:mysite.com </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>템플릿 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치가 URI를 찾아 여는 데 사용해야 하는 매개 변수입니다. </p> <p>예:http://%Site%%URI% <span class="filepath"></span> </p> <p>예제에 표시된 기본 템플릿은 데이터 워크벤치에 웹 브라우저를 열고 사이트 매개 변수에 정의된 위치를 찾은 <span class="wintitle"> 다음</span> 열려는 URI 차원 요소를 찾습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 파일을 저장합니다.
1. 작업 프로필의 모든 사용자가 이 변경 사항을 사용할 수 있도록 하려면 [!DNL .vw] 열에서 해당 [!DNL User] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > **[!UICONTROL working profile name]**&#x200B;을 클릭합니다.

