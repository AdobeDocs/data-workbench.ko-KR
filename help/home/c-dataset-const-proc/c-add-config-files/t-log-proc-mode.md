---
description: 구성 파일 Log Processing Mode.cfg를 사용하면 데이터 집합에 대한 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, Data Workbench 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.
title: Log Processing Mode.cfg
uuid: 1f1e5d8b-80e7-4423-bb03-56e706a1b7b4
exl-id: e252b815-e691-490d-9ac9-88bb1fd2c64d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 3%

---

# Log Processing Mode.cfg{#log-processing-mode-cfg}

{{eol}}

구성 파일 Log Processing Mode.cfg를 사용하면 데이터 집합에 대한 데이터 처리를 일시 중지하거나, 오프라인 소스를 지정하거나, Data Workbench 서버가 상태 파일을 저장하는 빈도를 지정할 수 있습니다.

변경 [!DNL Log Processing Mode.cfg] 소스 추가 또는 제거를 포함하여 파일이 데이터를 재처리하는 것은 아닙니다.

**데이터 집합 프로필에 대한 Log Processing Mode.cfg 파일을 편집하려면**

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 콘텐츠를 표시합니다.

   >[!NOTE]
   >
   >만약 [!DNL Log Processing Mode.cfg] 파일이 원하는 프로파일에 대한 디렉토리에 없습니다. data workbench 서버 컴퓨터의 기본 디렉토리에서 프로필 디렉토리에 이 파일을 복사해야 합니다.

   열기 및 작업에 대한 자세한 내용은 [!DNL Profile Manager,] 참조 *Data Workbench 사용 안내서*.

1. 구성 파일 이름 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 구성 창이 나타납니다.
1. 다음 표를 안내서로 사용하여 구성 파일에서 매개 변수를 편집합니다.

   >[!NOTE]
   >
   >의 일부 매개 변수 [!DNL Log Processing Mode.cfg] 파일에는 가 들어 있는 이름이 있습니다. [!DNL Fast Input] 또는 [!DNL Fast Merge]. [!DNL Fast Input]는 데이터 집합 구성의 로그 처리 단계를 나타내며 총 데이터 집합 처리 시간의 약 절반을 담당합니다. [!DNL Fast Merge] 는 로그 처리 앞에 와야 데이터 집합 구성의 변환 단계를 나타냅니다. [!DNL Fast Merge] 재변형 중에 수정 결과가 발생하지 않습니다 [!DNL Transformation Dataset Configuration] 파일. 좋아요 [!DNL Fast Input], [!DNL Fast Merge] 또한 는 데이터 세트 처리 시간의 약 절반을 담당합니다.

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
      <td colname="col2"> <p>데이터 변환 효율에 영향을 주는 조정 매개 변수입니다. 기본값은 128000000입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 입력 의사 결정 비율 </td> 
      <td colname="col2"> <p>시스템이 입력하는 읽지 않은 로그 바이트와 총 바이트 비율을 지정하는 조정 매개 변수 <span class="wintitle"> 빠른 입력</span> 모드(및 그 후) <span class="wintitle"> 빠른 병합</span>) 내의 아무 곳에나 삽입할 수 있습니다. </p> <p> 기본값은 200이며, 이것은 시스템이 입력하는 것을 의미합니다 <span class="wintitle"> 빠른 입력</span> 읽지 않은 로그 데이터가 전체 데이터의 1/200에 있는 실시간 모드에서 모드입니다. 의사 결정 비율이 높을수록 시스템이 진입합니다 <span class="wintitle"> 빠른 입력</span> 모드를 보다 쉽게 사용할 수 있는 반면, 낮은 비율을 사용하면 진입 가능성이 줄어듭니다 <span class="wintitle"> 빠른 입력</span> 모드. </p> <p> <p>참고: 매개 변수를 0으로 설정하면 시스템이 <span class="wintitle"> 빠른 입력</span> 초기 처리에도 불구하고 모드 로 전환합니다. 매개 변수를 1.1로 설정하면 시스템이 다음을 입력할 수 있습니다 <span class="wintitle"> 빠른 입력</span> 초기 처리 중이지만 후속 처리가 아닙니다. Adobe은 0에서 1.1 사이의 값을 사용하지 않는 것이 좋습니다. 이 매개 변수 설정에 대한 자세한 내용은 Adobe에게 문의하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 입력 FIFO 바이트 </td> 
      <td colname="col2"> <p>데이터 처리 중 메모리 사용 및 시스템 성능 균형을 조정하는 조정 매개 변수입니다. 기본값은 120000000입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 빠른 병합 버퍼 바이트 </td> 
      <td colname="col2"> <p>데이터 처리 중 메모리 사용 및 시스템 성능 균형을 조정하는 조정 매개 변수입니다. 기본값은 128000000입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 오프라인 소스 </td> 
      <td colname="col2"> <p>오프라인 로그 소스의 마스크입니다. </p> <p> <b> 오프라인 소스를 지정하려면</b> 
      <ul id="ul_569B90E9A85246F88906FA5444F8A93E"> 
       <li id="li_3EF182CEF4A44106B5267175EC62B9AB"> 마우스 오른쪽 단추 클릭 <span class="uicontrol"> 오프라인 소스</span>를 클릭한 다음 <span class="uicontrol"> 새로 추가</span> &gt; <span class="uicontrol"> 소스</span>. </li> 
       <li id="li_E8FBA212F4784B1A830745A90BB3AF90"> 새 소스의 매개 변수에 로그 시퀀스의 마스크를 입력합니다. 파일 이름이 YYYYMMDD 인 센서 로그 소스의 경우<i>SENSORID</i>.vsl, 마스크는 <i>SENSORID.SENSORID</i> 는 대/소문자를 구분합니다. 로그 파일 로그 소스의 경우 마스크는 <span class="wintitle"> 마스크 패턴</span>. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> 로그 파일</a>. </li> 
      </ul> </p> <p> 오프라인 소스에서 소스를 추가하거나 제거해도 데이터 세트가 재처리되지는 않습니다. </p> <p> 기준 시간 측정은 프로필의 온라인 소스 처리를 위해 유지됩니다. 오프라인 소스가 다시 온라인 상태가 되면 해당 소스에 대해 들어오는 로그 파일의 처리가 다시 시작됩니다. </p> <p> 소스가 다시 온라인으로 돌아올 때마다 오프라인 소스에서 이를 제거해야 합니다. 그렇지 않으면 Data Workbench 서버가 소스를 온라인 소스로 처리하고 소스가 데이터를 전송하는 동안 기준 시간을 업데이트합니다. 소스가 다시 오프라인 상태가 되면 기준 시간 측정이 중지됩니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 일시 정지됨 </td> 
      <td colname="col2"> True 또는 False입니다. true인 경우 새 데이터가 데이터 세트에 처리되지 않습니다. 기본값은 false입니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 실시간 지연 </td> 
      <td colname="col2"> Data Workbench 서버가 데이터 집합에 대한 처리 간격 사이에 대기하는 시간(초)입니다. 이 값을 0으로 설정하면 시스템에서 들어오는 데이터를 실시간으로 추적하려고 합니다. 기본값은 0(0)이지만, 이 값을 늘려 CPU 로드를 줄일 수 있습니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 실시간 FIFO 바이트 </td> 
      <td colname="col2"> <p>데이터 집합에 처리되기를 기다리는 데이터를 저장하는 데 사용되는 메모리 크기(바이트)입니다. 실시간 지연에 대해 지정하는 초 수를 기반으로 이 값을 변경해야 할 수 있습니다. 기본값은 16000000입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 저장 간격(초) </td> 
      <td colname="col2"> <p>Data Workbench 서버가 상태 파일을 저장하는 빈도입니다. 기본값은 3600입니다. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하면 안 됩니다. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   편집 시 [!DNL Log Processing Mode.cfg] data workbench 창 내의 파일에서는 잘라내기(Ctrl+x ), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그)과 모두 선택(Ctrl+a )하는 등 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 또한 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])를 다른 이름으로 바꿉니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > **[!UICONTROL datasetprofile name]**.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.
