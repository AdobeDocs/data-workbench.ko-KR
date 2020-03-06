---
description: 서버 파일 관리자를 사용하면 구성 및 조회 파일을 포함하여, 제품의 설치 디렉토리에 있는 모든 디렉토리 및 파일에 대한 액세스를 제공하여 인증된 데이터 워크벤치에서 데이터 워크벤치 서버 컴퓨터를 원격으로 관리하고 관리할 수 있습니다.
solution: Analytics
title: 서버 파일 관리자
topic: Data workbench
uuid: 62625b9d-587f-4a78-8328-2270869909f8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 서버 파일 관리자{#server-files-manager}

서버 파일 관리자를 사용하면 구성 및 조회 파일을 포함하여, 제품의 설치 디렉토리에 있는 모든 디렉토리 및 파일에 대한 액세스를 제공하여 인증된 데이터 워크벤치에서 데이터 워크벤치 서버 컴퓨터를 원격으로 관리하고 관리할 수 있습니다.

메뉴를 [!DNL Server Files Manager] 사용할 수도 [!DNL Admin] 있고, 에서 Data Workbench 서버 컴퓨터의 노드를 마우스 오른쪽 단추로 클릭한 [!DNL Servers Manager] 다음 을 클릭하여 액세스할 수도 **[!UICONTROL Server Files]**&#x200B;있습니다.

![](assets/vis_FileManager.png)

>[!NOTE]
>
>선택한 디렉토리를 표시하는 새 서버 파일 관리자를 만들 수 있습니다. 새 [서버 파일 관리자 만들기를 참조하십시오](../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-svr-files-mgrs.md#concept-6e8f63273109443699a8f61b1a2ea816).

목록 파일 및 폴더 이름의 왼쪽 열입니다. [!DNL Server Files Manager] 가운데 및 오른쪽 열의 확인 표시는 파일 구조에서 이러한 디렉토리와 파일이 있는 위치를 나타냅니다.

파일이 제품의 설치 디렉토리에 있으면 *서버 이름* (예: 데이터 워크벤치 서버) 열에 확인 표시가 나타납니다. 파일이 Data Workbench 설치 디렉토리 *\Temp 디렉토리에 있는 Data* Workbench 사용자의 컴퓨터에 있을 경우 이 [!DNL Temp] 열에는 확인 표시가 나타납니다. 확인 표시 색상은 다른 위치에 있는 파일이 동시에 수정되었는지 여부를 나타냅니다.

* 서버 이름 열의 빨간색 확인 표시는 폴더 또는 파일이 데이터 워크벤치 서버 컴퓨터에 있음을 나타냅니다.
* 열의 빨간색 확인 표시는 [!DNL Temp] 파일 또는 폴더의 로컬 사본이 데이터 워크벤치 서버 컴퓨터의 파일 또는 폴더와 동일한 수정일 및 시간을 갖는다는 것을 나타냅니다.
* 열의 흰색 확인 표시는 데이터 워크벤치 설치 디렉토리 [!DNL Temp] \Temp 디렉토리의 파일 또는 폴더에 **&#x200B;데이터 워크벤치 서버 컴퓨터의 파일 또는 폴더와 다른 수정 날짜 및 시간이 있음을 나타냅니다.

다음 그래픽은 빨간색 및 흰색 체크 표시가 [!DNL Server Files Manager] 있는 것을 보여줍니다.

![](assets/vis_FileManager_RedWhiteChecks.png)

**To manage directory and files using the[!DNL Server Files Manager]**

Data Workbench 서버 컴퓨터의 디렉토리 및 파일을 조작하는 [!DNL Server Files Manager] 데 를 사용할 수 있습니다.

다음 표에는 를 사용하여 완료할 수 있는 작업이 나와 [!DNL Server Files Manager]있습니다.

<table id="table_D217AE5A878542EC8B604812A61819C3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>디렉토리 내의 파일 보기 </p> </td> 
   <td colname="col2"> <p>디렉토리 이름을 클릭하여 내용을 봅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리의 컨텐츠를 숨기려면 </p> </td> 
   <td colname="col2"> <p>디렉토리 이름을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리에 대한 세부 정보를 보려면 </p> </td> 
   <td colname="col2"> <p>서버 이름이나 임시 열에서 디렉토리 옆에 있는 셀을 마우스 오른쪽 단추로 <span class="wintitle"> 클릭합니다</span> . 다음 정보가 표시됩니다. </p> 
    <ul id="ul_2DA5C8D0E95F4BCC8F7E25D05F00EB02"> 
     <li id="li_3FDECC14D62543B183C3509C338DF432">경로. 디렉토리의 경로입니다. </li> 
     <li id="li_9CF3989FD9E2427995F070E043FAD02C">디렉토리. 디렉토리 이름입니다. </li> 
     <li id="li_68AAA11907404D0BBF407ECD7CA2E467">From. 디렉토리 원격 또는 임시 위치입니다. </li> 
     <li id="li_CB4AEEC89E424868B758465EC0B701B5">날짜(임시 열만). 로컬 사본에 대한 마지막 개정일 또는 작성 일자. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일에 대한 세부 사항 보기 </p> </td> 
   <td colname="col2"> <p>서버 이름이나 임시 열에서 파일 옆에 있는 확인 표시를 마우스 오른쪽 단추로 <span class="wintitle"> 클릭합니다</span> . 다음 정보가 표시됩니다. </p> <p> 
     <ul id="ul_C4E6CB86D1774D739B5ECF48AF8DB628"> 
      <li id="li_7A6D39CF8C064FDDAB87F8D4E50FA832">경로. 파일의 경로입니다. </li> 
      <li id="li_9C735B6F0A2541F1992B845359C3685A">파일. 파일의 이름입니다. </li> 
      <li id="li_3EB903E4F4C44A6093732C588F0125EF">From. 디렉토리 원격 또는 임시 위치입니다. </li> 
      <li id="li_C1FED4F98F854D5892DBAD9F9E1D47B8">날짜. 파일의 마지막 개정일 </li> 
      <li id="li_7477C727C62F4406BB2026063E41F2AE">크기. 파일의 크기입니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로컬 컴퓨터에 디렉토리를 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>이 디렉토리의 <i>서버 이름</i> 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 [디렉토리 로컬로 만들기] <span class="uicontrol"> 를 클릭합니다</span>. 디렉토리에 대한 확인 표시가 임시 열에 <span class="wintitle"> 표시됩니다</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로컬 컴퓨터에 파일을 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>이 파일의 <i>서버 이름</i> 열에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [로컬로 만들기]를 <span class="uicontrol"> 클릭합니다</span>. 파일의 확인 표시가 임시 열에 <span class="wintitle"> 나타납니다</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로컬 컴퓨터에 로그 파일의 마지막 부분을 다운로드하려면 </p> </td> 
   <td colname="col2"> <p>전체 로그 파일을 다운로드할 필요가 없도록 하려면(특히 오류 메시지가 파일의 끝에 근접했다는 것을 알고 있는 경우) 해당 파일의 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 테일을</span>클릭한 다음 다운로드할 부분의 크기를 선택합니다. 파일의 확인 표시가 임시 열에 <span class="wintitle"> 나타납니다</span> . 로컬 파일에는 파일 끝부터 시작하여 지정한 데이터의 양만 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리를 열려면 </p> </td> 
   <td colname="col2"> <p>[임시] 열에서 디렉토리에 대한 확인 표시를 마우스 오른쪽 단추로 <span class="wintitle"> 클릭하고</span> [열기] <span class="uicontrol"> &gt;</span> <span class="uicontrol"> 폴더를</span>클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일을 열려면 </p> </td> 
   <td colname="col2"> <p>임시 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="wintitle"></span> 열기를 <span class="uicontrol"> 클릭한 다음</span>데이터 워크벤치 <span class="uicontrol"> (메모장</span>) <span class="uicontrol"> 또는 폴더인 메모장에서 데이터 워크벤치</span><span class="uicontrol"></span>(Data Workbench)를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리의 로컬 복사본을 데이터 워크벤치 서버에 저장 </p> </td> 
   <td colname="col2"> <p>임시 열의 디렉토리에 대한 확인 표시를 마우스 오른쪽 단추로 <span class="wintitle"></span> 클릭하고 <span class="uicontrol"> 디렉터리</span> 저장을 <i>클릭하여<span class="uicontrol"> &gt;&lt;프로필 이름</span>&gt;</i>을클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일의 로컬 복사본을 데이터 워크벤치 서버에 저장 </p> </td> 
   <td colname="col2"> <p>임시 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 <span class="wintitle"> 클릭하고</span> 저장 <span class="uicontrol"> 위치</span> &gt; 프로필 이름 <i>&gt;을<span class="uicontrol"></span></i>클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디렉토리 또는 파일의 로컬 복사본 제거 </p> </td> 
   <td colname="col2"> <p>[임시] 열에서 디렉토리 또는 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="wintitle"> [제거</span> ]를 <span class="uicontrol"> 클릭합니다</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Microsoft Outlook에서 파일을 전자 메일 첨부 파일로 복사하여 붙여넣기 </p> </td> 
   <td colname="col2"> <p>임시 열에서 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 <span class="wintitle"> 복사를</span> 클릭합니다 <span class="uicontrol"></span>. 이메일 본문에 있는 Ctrl+v를 눌러 파일을 첨부합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

