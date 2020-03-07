---
description: Transform Mode.cfg 구성 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 변환 기능을 실행하는 데이터 워크벤치 서버에서 상태 파일을 저장하는 빈도를 지정할 수 있습니다.
solution: Analytics
title: Transform Mode.cfg 파일
topic: Data workbench
uuid: 6e875d02-341a-414c-90e5-aa7fa910ab81
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Transform Mode.cfg 파일{#the-transform-mode-cfg-file}

Transform Mode.cfg 구성 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 변환 기능을 실행하는 데이터 워크벤치 서버에서 상태 파일을 저장하는 빈도를 지정할 수 있습니다.

소스 추가 또는 제거를 포함하여 파일을 변경하더라도 데이터가 다시 처리되지는 않습니다. [!DNL Transform Mode.cfg]

**데이터 세트 프로필에 대한 Transform Mode.cfg 파일을 편집하려면**

1. 데이터를 내보내려는 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 을 클릭하여 디렉토리의 컨텐츠를 **[!UICONTROL Dataset]** 표시합니다.
1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL Transform Mode.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 창이 [!DNL Transform Mode.cfg] 나타납니다.
1. 다음 표를 참조하여 구성 파일의 매개 변수를 편집합니다.

   <table id="table_9FC00BD54FD8439DA17AEF61AC2ACD50"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> 매개 변수 </th> 
    <th colname="col2" class="entry"> 설명 </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> 오프라인 소스 </td> 
    <td colname="col2"> <p>오프라인 로그 소스의 마스크입니다. </p> <p> 오프라인 소스를 지정하려면 </p> 
    <ul id="ul_B93F945A697C4882ADE420438712B0B0"> 
     <li id="li_617C04FE9F1C4E998394F224CFEA21F3"> 오프라인 소스를 마우스 오른쪽 단추로 <span class="uicontrol"> 클릭하고</span> 새로 <span class="uicontrol"> 추가</span> &gt; 소스를 <span class="uicontrol"> 클릭합니다</span>. </li> 
    <li id="li_B263A294D1F14D62BBAA5DBF3B388C38"> 새 소스의 매개 변수에 로그 시퀀스의 마스크를 입력합니다. 파일 이름이 YYYYMMDD-SENDORID.vsl인 센서 로그 소스의 경우 <span class="filepath"> 마스크는</span>SENDORID.SENDORID <i></i> 대/소문자를 구분합니다. 로그 파일 로그 소스의 경우 마스크는 마스크 패턴에서 추출한 <span class="wintitle"> 문자열입니다</span> (로그 파일 <a href="../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> 참조</a>). </li> 
    </ul> <p> Offline Sources에서 소스를 추가하거나 제거해도 <span class="wintitle"> 데이터</span> 세트에 대한 재처리가 되지 않습니다. </p> <p> 시간 측정을 통해 프로파일의 온라인 소스를 처리할 수 있습니다. 오프라인 소스가 다시 온라인 상태가 되면 해당 소스에 대해 들어오는 로그 파일의 처리가 다시 시작됩니다. </p> <p> <p>참고:소스가 온라인으로 돌아올 때마다 오프라인 소스에서 소스를 제거해야 <span class="wintitle"> 합니다</span>. 이렇게 하지 않으면 데이터 워크벤치 서버는 소스를 온라인 소스로 취급하고 소스가 데이터를 전송하는 한 기준 시간을 업데이트합니다. 소스가 다시 오프라인 상태가 되면 기준 시간 측정을 중지합니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 일시 정지됨 </td> 
    <td colname="col2"> 참 또는 거짓 true이면 새 데이터가 데이터 세트로 처리되지 않습니다. 기본값은 false입니다. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 저장 간격(초) </td> 
    <td colname="col2"> <p>변환 기능이 실행 중인 데이터 워크벤치 서버가 상태 파일을 저장하는 빈도입니다. 기본값은 3600입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
    </tr> 
    </tbody> 
   </table>

   데이터 워크벤치 창에서 파일을 편집할 때 단축키(Ctrl+x), 복사(Ctrl+C), 붙여넣기(Ctrl+V), 실행 취소(Ctrl+Z), 다시 실행(Ctrl+Shift+Z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a)을 사용하여 기본 편집 기능을 사용할 수 있습니다. [!DNL Transform Mode.cfg] 또한 단축키를 사용하여 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 파일에 붙여넣을 수 있습니다.

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]열에서 데이터 워크벤치의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Transform Mode.cfg] > [!DNL User] **[!UICONTROL Save to]** **[!UICONTROL profile name]**&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터를 내보내는 프로필의 이름입니다. 프로필 동기화 후 데이터 재처리가 시작됩니다.

   내보내기를 위해 데이터를 재처리하는 방법에 대한 자세한 내용은 재처리 및 [재변형을 참조하십시오](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
