---
description: Log Processing Mode.cfg 구성 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 데이터 워크벤치 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.
solution: Analytics
title: 로그 처리 모드.cfg
topic: Data workbench
uuid: 1f1e5d8b-80e7-4423-bb03-56e706a1b7b4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 로그 처리 모드.cfg{#log-processing-mode-cfg}

Log Processing Mode.cfg 구성 파일을 사용하면 데이터 세트에 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, 데이터 워크벤치 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.

소스 추가 또는 제거를 포함하여 파일을 변경하더라도 데이터가 다시 처리되지는 않습니다. [!DNL Log Processing Mode.cfg]

**데이터 집합 프로필에 대한 로그 처리 Mode.cfg 파일을 편집하려면**

1. 데이터 집합 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 클릭하여 내용을 **[!UICONTROL Dataset]** 표시합니다.

   >[!NOTE]
   >
   >파일이 원하는 프로필의 디렉토리에 없는 [!DNL Log Processing Mode.cfg] 경우 데이터 워크벤치 서버 시스템의 기본 디렉토리에서 이 파일을 프로파일 디렉토리로 복사해야 합니다.

   열기 및 작업에 대한 자세한 내용은 데이터 워크벤치 [!DNL Profile Manager,] 사용 안내서를 *참조하십시오*.

1. 구성 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 구성 창이 나타납니다.
1. 다음 표를 참조하여 구성 파일의 매개 변수를 편집합니다.

   >[!NOTE]
   >
   >파일의 일부 매개 변수에는 [!DNL Log Processing Mode.cfg] 또는 [!DNL Fast Input] [!DNL Fast Merge]가 포함된 이름이 있습니다. [!DNL Fast Input]은 데이터 집합 구성의 로그 처리 단계를 나타내며 전체 데이터 집합 처리 시간의 약 절반을 담당합니다. [!DNL Fast Merge] 로그 처리가 앞에 있을 때만 데이터 집합 구성의 변환 단계를 나타냅니다. [!DNL Fast Merge] 는 [!DNL Transformation Dataset Configuration] 파일을 수정하는 작업으로 인해 재변환하는 동안 발생하지 않습니다. 예를 [!DNL Fast Input]들어 [!DNL Fast Merge] 데이터 세트 처리 시간의 약 절반을 담당하고 있습니다.

   <table id="table_1BF356E21C0E4119A277F40CEC5D7A21"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> 매개 변수 </th> 
      <th colname="col2" class="entry"> 설명 </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> 클라우드 바이트 </td> 
      <td colname="col2"> <p>데이터 변환 효율성에 영향을 주는 조정 매개 변수입니다. 기본값은 128000000입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 입력 결정 비율 </td> 
      <td colname="col2"> <p>시스템이 실시간으로 데이터를 처리하는 대신 빠른 입력 모드(및 이후 빠른 병합 <span class="wintitle"> )에</span> 들어가는 읽지 않은 로그 바이트에 대한 <span class="wintitle"> 비율을</span>지정하는 조정 매개 변수입니다. </p> <p> 기본값은 200입니다. 즉, 읽지 <span class="wintitle"> 않은</span> 로그 데이터가 전체 데이터의 1/200에 있을 때 시스템이 실시간 모드로 빠른 입력 모드로 전환됨을 의미합니다. 의사 결정 비율이 높을수록 시스템이 빠른 입력 <span class="wintitle"> 모드로</span> 더 쉽게 전환되고, 비율이 낮을수록 빠른 입력 모드로 들어갈 가능성이 <span class="wintitle"> 낮아집니다</span> . </p> <p> <p>참고:매개 변수를 0으로 설정하면 초기 처리에도 불구하고 시스템이 <span class="wintitle"> 빠른</span> 입력 모드로 들어갈 수 없습니다. 매개 변수를 1.1로 설정하면 시스템이 초기 처리 <span class="wintitle"> 중에 빠른</span> 입력을 입력할 수 있지만 후속 처리를 위해 입력할 수는 없습니다. Adobe에서는 0과 1.1 사이의 값을 사용하지 않는 것이 좋습니다.이 매개 변수 설정에 대한 자세한 내용은 Adobe에 문의하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 입력 FIFO 바이트 </td> 
      <td colname="col2"> <p>데이터 처리 중 메모리 사용량 및 시스템 성능을 균형 있게 조정하는 조정 매개 변수입니다. 기본값은 120000000입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 병합 버퍼 바이트 </td> 
      <td colname="col2"> <p>데이터 처리 중 메모리 사용량 및 시스템 성능을 균형 있게 조정하는 조정 매개 변수입니다. 기본값은 128000000입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 오프라인 소스 </td> 
      <td colname="col2"> <p>오프라인 로그 소스의 마스크입니다. </p> <p> <b> 오프라인 소스를 지정하려면</b> 
      <ul id="ul_569B90E9A85246F88906FA5444F8A93E"> 
       <li id="li_3EF182CEF4A44106B5267175EC62B9AB"> 오프라인 소스를 마우스 오른쪽 단추로 <span class="uicontrol"> 클릭한</span>다음 <span class="uicontrol"> 새로</span> 추가 &gt; 소스를 <span class="uicontrol"> 클릭합니다</span>. </li> 
       <li id="li_E8FBA212F4784B1A830745A90BB3AF90"> 새 소스의 매개 변수에 로그 시퀀스의 마스크를 입력합니다. 파일 이름이 YYYYMMDD-SENDORID.vsl인 센서 로그<i>소스의</i>경우 마스크는 <i>SENDORID.SENDORID이며</i> 대/소문자를 구분합니다. 로그 파일 로그 소스의 경우 마스크는 마스크 패턴에서 추출한 <span class="wintitle"> 문자열입니다</span>. See <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Log Files</a>. </li> 
      </ul> </p> <p> Offline Sources에서 소스를 추가하거나 제거해도 데이터 세트를 재처리할 수 없습니다. </p> <p> 시간 측정을 통해 프로파일의 온라인 소스를 처리할 수 있습니다. 오프라인 소스가 다시 온라인 상태가 되면 해당 소스에 대해 들어오는 로그 파일의 처리가 다시 시작됩니다. </p> <p> 소스가 온라인으로 돌아올 때마다 오프라인 소스에서 소스를 제거해야 합니다. 그렇지 않으면 데이터 워크벤치 서버가 소스를 온라인 소스로 취급하고 소스가 데이터를 전송하는 한 기준 시간을 업데이트합니다. 소스가 다시 오프라인 상태가 되면 기준 시간 측정을 중지합니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 일시 정지됨 </td> 
      <td colname="col2"> 참 또는 거짓 true이면 새 데이터가 데이터 세트로 처리되지 않습니다. 기본값은 false입니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 실시간 지연 </td> 
      <td colname="col2"> 데이터 워크벤치 서버가 데이터 세트에 대한 처리 간격 사이에 대기하는 시간(초)입니다. 이 값을 0으로 설정하면 시스템이 들어오는 데이터를 실시간으로 추적하려고 합니다. 기본값은 0(0)이지만 이 값을 늘려 CPU 로드를 줄일 수 있습니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 실시간 FIFO 바이트 </td> 
      <td colname="col2"> <p>데이터 세트로 처리 대기 중인 데이터를 저장하는 데 사용되는 메모리 크기(바이트)입니다. 실시간 지연에 대해 지정한 시간(초)을 기준으로 이 값을 변경해야 할 수 있습니다. 기본값은 16000000입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 저장 간격(초) </td> 
      <td colname="col2"> <p>데이터 워크벤치 서버가 상태 파일을 저장하는 빈도입니다. 기본값은 3600입니다. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   데이터 워크벤치 창에서 파일을 편집할 때 단축키(Ctrl+x), 복사(Ctrl+C), 붙여넣기(Ctrl+V), 실행 취소(Ctrl+Z), 다시 실행(Ctrl+Shift+Z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a)을 사용하여 기본 편집 기능을 사용할 수 있습니다. [!DNL Log Processing Mode.cfg] 또한 단축키를 사용하여 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 파일에 붙여넣을 수 있습니다.

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL User] > **[!UICONTROL Save to]** **[!UICONTROL datasetprofile name]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.
