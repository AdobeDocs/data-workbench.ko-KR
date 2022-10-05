---
description: Transform Mode.cfg 구성 파일을 사용하면 데이터 처리를 데이터 집합에 일시 중지하거나, 오프라인 소스를 지정하거나, 변환 기능을 실행하는 Data Workbench 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.
title: Transform Mode.cfg 파일
uuid: 6e875d02-341a-414c-90e5-aa7fa910ab81
exl-id: 4faca063-3ca9-4c7c-9f04-ba2dfb647a77
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 3%

---

# Transform Mode.cfg 파일{#the-transform-mode-cfg-file}

{{eol}}

Transform Mode.cfg 구성 파일을 사용하면 데이터 처리를 데이터 집합에 일시 중지하거나, 오프라인 소스를 지정하거나, 변환 기능을 실행하는 Data Workbench 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.

변경 [!DNL Transform Mode.cfg] 소스 추가 또는 제거를 포함하여 파일이 데이터를 재처리하는 것은 아닙니다.

**데이터 집합 프로필에 대한 Transform Mode.cfg 파일을 편집하려면**

1. 데이터를 내보낼 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 디렉토리 내용을 표시합니다.
1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Transform Mode.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 다음 [!DNL Transform Mode.cfg] 창이 나타납니다.
1. 다음 표를 안내서로 사용하여 구성 파일에서 매개 변수를 편집합니다.

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
    <td colname="col2"> <p>오프라인 로그 소스의 마스크입니다. </p> <p> 오프라인 소스를 지정하려면 다음을 수행합니다. </p> 
    <ul id="ul_B93F945A697C4882ADE420438712B0B0"> 
     <li id="li_617C04FE9F1C4E998394F224CFEA21F3"> 마우스 오른쪽 단추 클릭 <span class="uicontrol"> 오프라인 소스</span> 을(를) 클릭합니다. <span class="uicontrol"> 새로 추가</span> &gt; <span class="uicontrol"> 소스</span>. </li> 
    <li id="li_B263A294D1F14D62BBAA5DBF3B388C38"> 새 소스의 매개 변수에 로그 시퀀스의 마스크를 입력합니다. 형식의 파일 이름이 있는 센서 로그 소스의 경우 <span class="filepath"> YYYMDD-SENDSORID.vsl</span>이면 마스크는 <i>SENSORID.SENSORID</i> 는 대/소문자를 구분합니다. 로그 파일 로그 소스의 경우 마스크는 <span class="wintitle"> 마스크 패턴</span> 자세한 내용은 <a href="../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> 로그 파일</a>). </li> 
    </ul> <p> 소스 추가 또는 제거 <span class="wintitle"> 오프라인 소스</span> 는 데이터 집합을 재처리하게 하지 않습니다. </p> <p> 기준 시간 측정은 프로필의 온라인 소스 처리를 위해 유지됩니다. 오프라인 소스가 다시 온라인 상태가 되면 해당 소스에 대해 들어오는 로그 파일의 처리가 다시 시작됩니다. </p> <p> <p>참고: 소스가 온라인 상태가 될 때마다 <span class="wintitle"> 오프라인 소스</span>. 그렇지 않으면 Data Workbench 서버가 소스를 온라인 소스로 처리하고 소스가 데이터를 전송하는 동안 기준 시간을 업데이트합니다. 소스가 다시 오프라인 상태가 되면 기준 시간 측정이 중지됩니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 일시 정지됨 </td> 
    <td colname="col2"> True 또는 False입니다. true인 경우 새 데이터가 데이터 세트에 처리되지 않습니다. 기본값은 false입니다. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 저장 간격(초) </td> 
    <td colname="col2"> <p>변환 기능을 실행 중인 Data Workbench 서버가 상태 파일을 저장하는 빈도입니다. 기본값은 3600입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
    </tr> 
    </tbody> 
   </table>

   편집 시 [!DNL Transform Mode.cfg] data workbench 창 내의 파일에서는 잘라내기(Ctrl+x ), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그)과 모두 선택(Ctrl+a )하는 등 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 또한 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])를 다른 이름으로 바꿉니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]data workbench에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Transform Mode.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > **[!UICONTROL profile name]**: 프로필 이름은 데이터를 내보내는 프로필의 이름입니다. 프로필의 동기화 후 데이터 재처리가 시작됩니다.

   내보낼 데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
