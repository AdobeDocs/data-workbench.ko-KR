---
description: Server Files Manager를 사용하면 구성 및 조회 파일을 포함하여 제품의 설치 디렉토리에 있는 모든 디렉토리와 파일에 대한 액세스를 제공하여 권한 있는 Data Workbench에서 Data Workbench 서버 컴퓨터를 원격으로 관리하고 관리할 수 있습니다.
title: 서버 파일 관리자
uuid: 62625b9d-587f-4a78-8328-2270869909f8
exl-id: 9ac7e95d-47e5-4862-a16e-bee0df1d3d15
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 1%

---

# 서버 파일 관리자{#server-files-manager}

Server Files Manager를 사용하면 구성 및 조회 파일을 포함하여 제품의 설치 디렉토리에 있는 모든 디렉토리와 파일에 대한 액세스를 제공하여 권한 있는 Data Workbench에서 Data Workbench 서버 컴퓨터를 원격으로 관리하고 관리할 수 있습니다.

[!DNL Admin] 메뉴를 사용하여 [!DNL Server Files Manager]에 액세스할 수 있을 뿐만 아니라, [!DNL Servers Manager]에서 Data Workbench 서버 컴퓨터의 노드를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Server Files]**&#x200B;를 클릭하면 됩니다.

![](assets/vis_FileManager.png)

>[!NOTE]
>
>선택한 디렉터리를 표시하는 새 서버 파일 관리자를 만들 수 있습니다. [새 서버 파일 관리자 만들기](../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-svr-files-mgrs.md#concept-6e8f63273109443699a8f61b1a2ea816)를 참조하십시오.

[!DNL Server Files Manager] 의 왼쪽 열에는 파일 및 폴더 이름이 나열됩니다. 가운데 열과 오른쪽 열의 확인 표시는 파일 구조에서 이러한 디렉토리와 파일이 있는 위치를 나타냅니다.

파일이 제품의 설치 디렉토리에 있는 경우 *서버 이름*(예: Data Workbench 서버) 열에는 확인 표시가 포함됩니다. 파일이 *Data Workbench 설치 디렉터리*\Temp 디렉터리에 있는 Data Workbench 사용자의 컴퓨터에 있으면 [!DNL Temp] 열에는 확인 표시가 포함됩니다. 확인 표시의 색상은 다른 위치에 있는 파일이 동시에 수정되었는지 여부를 나타냅니다.

* 서버 이름 열의 빨간색 확인 표시는 폴더 또는 파일이 Data Workbench 서버 컴퓨터에 있음을 나타냅니다.
* [!DNL Temp] 열에 빨간색 확인 표시가 있으면 파일이나 폴더의 로컬 복사본이 Data Workbench 서버 컴퓨터의 파일 또는 폴더와 동일한 수정 날짜 및 시간을 갖는다는 것을 나타냅니다.
* [!DNL Temp] 열에 있는 흰색 확인 표시는 *Data Workbench 설치 디렉토리*\Temp 디렉터리에 있는 파일 또는 폴더의 수정 날짜 및 시간이 Data Workbench 서버 컴퓨터의 파일 또는 폴더와 다르다는 것을 나타냅니다.

다음 그래픽에는 [!DNL Server Files Manager]에 빨간색 및 흰색 체크 표시가 모두 표시됩니다.

![](assets/vis_FileManager_RedWhiteChecks.png)

**를 사용하여 디렉터리 및 파일을 관리하려면[!DNL Server Files Manager]**

[!DNL Server Files Manager]을 사용하여 Data Workbench 서버 컴퓨터의 디렉터리와 파일을 조작할 수 있습니다.

다음 표에는 [!DNL Server Files Manager] 을 사용하여 완료할 수 있는 작업이 나와 있습니다.

<table id="table_D217AE5A878542EC8B604812A61819C3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>디렉토리 내의 파일을 보려면 </p> </td> 
   <td colname="col2"> <p>해당 내용을 보려면 디렉토리 이름을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리의 내용을 숨기려면 </p> </td> 
   <td colname="col2"> <p>디렉토리 이름을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리에 대한 세부 정보를 보려면 </p> </td> 
   <td colname="col2"> <p>서버 이름 또는 <span class="wintitle"> Temp</span> 열에서 디렉토리 옆에 있는 셀을 마우스 오른쪽 버튼으로 클릭합니다. 다음 정보가 표시됩니다. </p> 
    <ul id="ul_2DA5C8D0E95F4BCC8F7E25D05F00EB02"> 
     <li id="li_3FDECC14D62543B183C3509C338DF432">경로. 디렉토리의 경로입니다. </li> 
     <li id="li_9CF3989FD9E2427995F070E043FAD02C">디렉터리. 디렉토리 이름입니다. </li> 
     <li id="li_68AAA11907404D0BBF407ECD7CA2E467">From. 디렉터리 위치(원격 또는 임시)입니다. </li> 
     <li id="li_CB4AEEC89E424868B758465EC0B701B5">날짜(임시 열만). 로컬 복사본에 대한 마지막 수정 생성일 또는 날짜입니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일에 대한 세부 사항을 보려면 </p> </td> 
   <td colname="col2"> <p>서버 이름 또는 <span class="wintitle"> Temp</span> 열에서 파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. 다음 정보가 표시됩니다. </p> <p> 
     <ul id="ul_C4E6CB86D1774D739B5ECF48AF8DB628"> 
      <li id="li_7A6D39CF8C064FDDAB87F8D4E50FA832">경로. 파일의 경로입니다. </li> 
      <li id="li_9C735B6F0A2541F1992B845359C3685A">파일. 파일 이름입니다. </li> 
      <li id="li_3EB903E4F4C44A6093732C588F0125EF">From. 디렉터리 위치(원격 또는 임시)입니다. </li> 
      <li id="li_C1FED4F98F854D5892DBAD9F9E1D47B8">날짜. 파일의 마지막 수정 날짜입니다. </li> 
      <li id="li_7477C727C62F4406BB2026063E41F2AE">크기. 파일 크기입니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로컬 컴퓨터에 디렉터리를 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>이 디렉토리에 대한 <i>서버 이름</i> 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> Make Directory Local</span>을 클릭합니다. 디렉터리에 대한 확인 표시가 <span class="wintitle"> Temp</span> 열에 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로컬 컴퓨터에 파일을 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>이 파일에 대한 <i>서버 이름</i> 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 로컬 만들기</span>를 클릭합니다. 파일에 대한 확인 표시가 <span class="wintitle"> Temp</span> 열에 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 파일의 마지막 부분을 로컬 컴퓨터에 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>전체 로그 파일을 다운로드하지 않으려면(특히 오류 메시지가 파일 끝에 가깝다는 사실을 알 때), 파일의 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 테일</span> 을 클릭한 다음 다운로드할 부분의 크기를 선택하십시오. 파일에 대한 확인 표시가 <span class="wintitle"> Temp</span> 열에 나타납니다. 로컬 파일에는 파일 끝부터 지정한 데이터 양만 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리를 열려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 디렉토리에 대한 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 <span class="uicontrol"> Open</span> &gt; <span class="uicontrol"> 폴더</span>를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일을 열려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> Open</span>을 클릭한 다음 메모장</span>의 <span class="uicontrol"> Data Workbench</span>, <span class="uicontrol"> 폴더</span>를 클릭합니다.<span class="uicontrol"> </span></span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉터리 로컬 복사본을 Data Workbench 서버에 저장 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 디렉토리에 대한 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 <span class="uicontrol"> Save Directory to</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span></i>을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일의 로컬 복사본을 Data Workbench 서버에 저장 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> Save to</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span></i>을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉터리 또는 파일의 로컬 복사본 제거 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 디렉터리 또는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거</span> 를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Microsoft Outlook에서 전자 메일 첨부 파일로 파일 복사 및 붙여넣기 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Temp</span> 열에서 파일에 대한 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 <span class="uicontrol"> Copy</span> 를 클릭합니다. 전자 메일 본문에서 Ctrl+v를 눌러 파일을 첨부합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
