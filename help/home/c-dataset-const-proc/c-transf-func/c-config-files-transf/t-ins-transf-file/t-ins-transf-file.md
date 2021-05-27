---
description: Data workbenchTransform.cfg 파일에는 로그 소스, 데이터 변환 및 내보내기를 정의하는 매개 변수가 포함되어 있습니다.
title: Transform.cfg 파일
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
exl-id: e84f2536-cb22-4c47-a7a8-270b3c37ece6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 2%

---

# Transform.cfg 파일{#the-transform-cfg-file}

Data workbenchTransform.cfg 파일에는 로그 소스, 데이터 변환 및 내보내기를 정의하는 매개 변수가 포함되어 있습니다.

정의하는 변환은 센서( [!DNL .vsl] 파일)에 의해 수집되거나 텍스트 파일, XML 파일 또는 ODBC 호환 데이터베이스에 포함된 원시 데이터를 조작하여 기존 필드에 출력하거나, 현재 데이터를 덮어쓰거나 새로 정의된 필드로 출력합니다.

변환 기능을 구성하려면 이벤트 데이터를 내보내려는 프로필의 데이터 세트 폴더 내에서 Data Workbench [!DNL Transform.cfg] 파일을 편집합니다. 일반적으로 이 프로필은 변환 기능에만 사용됩니다(즉, Data Workbench [!DNL Transform.cfg] 파일에 정의된 데이터 처리 이외의 다른 작업은 수행하지 않습니다). 상속된 프로필에 대해 [!DNL Log Processing Dataset Include] 파일에 지정된 처리 지침 외에 Data Workbench [!DNL Transform.cfg] 파일에 지정된 처리 지침이 적용됩니다.

데이터 집합 포함 파일에 대한 자세한 내용은 [데이터 집합에 파일 포함](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오.

내보내려는 데이터가 Data Workbench 서버 클러스터에서 처리되는 경우 클러스터의 각 처리 서버(DPU)가 데이터를 처리하지만 첫 번째 DPU([!DNL profile.cfg] 파일의 처리 서버 #0)만 출력 데이터를 로컬 파일 시스템에 기록합니다.

**Data Workbench Transform.cfg 파일을 편집하려면**

1. 데이터를 내보낼 프로필에서 작업하는 동안 [!DNL Profile Manager] 을 열고 **[!UICONTROL Dataset]** 을 클릭하여 디렉토리의 내용을 표시합니다.
1. Data Workbench [!DNL Transform.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]** 를 클릭합니다. Data Workbench [!DNL Transform.cfg] 창이 나타납니다.
1. 아래 표를 안내서로 사용하여 구성 파일에서 매개 변수를 편집합니다.

<table id="table_91D9C4C1BE2E43158D9D06C6284EE3C7"> 
  <thead> 
    <tr> 
    <th colname="col1" class="entry"> 매개 변수 </th> 
    <th colname="col2" class="entry"> 설명 </th> 
    </tr> 
  </thead>
  <tbody> 
    <tr> 
    <td colname="col1"> 종료 시간 </td> 
    <td colname="col2"> <p>선택 사항입니다. 이번에는 타임스탬프가 포함되지만 포함하지 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. 
      <ul id="ul_C8C7F0F631594F7095CB83EF54E7CD0E"> 
       <li id="li_77AB6EEE8EEC4698AA886DE8BB0E2783"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_33806070F991476BB986906876CAF7F1"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어, 2013년 7월 29일 00:00:00 EDT를 <span class="wintitle"> 종료 시간 </span>으로 지정하면 2013년 7월 28일(11:59:59 PM EDT에서)의 데이터가 포함됩니다. </p> <p> 표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 시간대 약자 목록은 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a> 를 참조하십시오. </p> <p> 센서 및 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 수출자 </td> 
    <td colname="col2"> <p>내보내기의 하위 필드는 출력 데이터가 처리 및/또는 포맷되는 방식을 지정합니다. 로그 소스 집합에 대해 여러 내보내기를 정의할 수 있습니다. 각 내보내기 유형은 출력을 독립적으로 만듭니다. </p> <p> 다음과 같은 세 가지 유형의 내보내기가 있습니다. 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> 내보내기 구분 텍스트 파일 </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> 내보내기 유형에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> 내보내기 정의 </a>를 참조하십시오. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 해시 임계값 </td> 
    <td colname="col2"> 선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 내보내기를 위해 각 n개의 추적 ID 중 하나씩만 선택되므로 n개의 계수로 내보낸 총 행 수가 줄어듭니다.모든 행을 내보내려면 해시 임계값을 1로 설정합니다. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 항목 조건 </td> 
    <td colname="col2"> 선택 사항입니다. 내보낼 로그 항목이 고려되는 규칙을 정의합니다. <span class="wintitle"> 로그 항목 조건 </span>에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>을 참조하십시오. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 소스 </td> 
    <td colname="col2"> <p>데이터 소스. <span class="wintitle"> 로그 소스는  </span> .vsl  <span class="filepath">   </span> 파일, 로그 파일, XML 파일 또는 ODBC 호환 데이터베이스의 데이터일 수 있습니다. <span class="wintitle"> 로그 소스 </span>에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>을 참조하십시오. </p> <p> <span class="wintitle"> Transform </span> 에서는 모든 소스 데이터가 사전순으로 정렬된 입력 파일 내에서 시간 순서대로 와야 합니다. 이 요구 사항이 충족되지 않으면 계산 수가 잘못되고 출력 파일이 닫힌 후 추가 입력 데이터가 처리될 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 오프라인 모드 </td> 
    <td colname="col2"> <p>선택 사항입니다. True 또는 False. true인 경우 <span class="wintitle"> 변환 </span> 에서는 데이터 처리를 시작할 때 모든 입력 파일이 있다고 가정합니다. 입력 데이터를 모두 읽으면 <span class="wintitle"> 변환 </span> 에서는 추가 데이터가 수신될 때까지 기다리지 않고 모든 출력 파일을 닫습니다. 기본값은 false입니다. </p> <p> <p>참고: <span class="wintitle"> 오프라인 모드 </span>가 true로 설정된 경우 <span class="wintitle"> 변환 </span>은 처리가 시작되기 전에 모든 소스 데이터가 있어야 합니다. 출력 파일을 닫은 후 추가 데이터를 받으면 <span class="filepath"> VisualServer.log </span> 파일에 경고 메시지가 생성됩니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 재처리 </td> 
    <td colname="col2"> <p>선택 사항입니다. 여기에 문자 또는 문자 조합을 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 <span class="wintitle"> 변환 </span> 컴퓨터에 저장하면 데이터 재처리가 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형 </a> 을 참조하십시오. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 단계 </td> 
    <td colname="col2"> <p>선택 사항입니다. <span class="wintitle"> 로그 처리 데이터 집합에 사용할 수 있는 처리 단계의 이름에는 Data Workbench <span class="filepath"> Transform.cfg </span> 파일 외에 실행되는 </span> 파일이 포함됩니다. 처리 단계는 <span class="wintitle"> 로그 처리 데이터 집합에 정의된 변형에 </span> 파일을 정렬하는 방법을 제공합니다. 이 매개 변수는 여러 <span class="wintitle"> 로그 처리 데이터 집합 포함 </span> 파일 내에서 하나 이상의 변형을 정의했으며 내보내기 프로세스 중에 특정 지점에서 특정 변환을 수행하려는 경우에 매우 유용합니다. </p> <p> 여기에서 단계를 나열하는 순서는 데이터를 내보내는 동안 <span class="wintitle"> 로그 처리 데이터 집합에 포함된 </span> 파일의 변환이 실행되는 순서를 결정합니다. <span class="wintitle"> 사전 처리  </span> 및  <span class="wintitle"> 사후 처리 </span> 는 기본 제공 단계입니다. <span class="wintitle"> 사전 처리 </span> 는 항상 첫 번째 단계이며  <span class="wintitle"> 사후 처리 </span> 는 항상 마지막 단계입니다. 기본적으로 <span class="wintitle"> 기본값 </span> 이라는 이름의 스테이지가 있습니다. </p> <p> <b>새 처리 단계를 추가하려면</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> Data Workbench <span class="filepath"> Transform.cfg </span> 창에서 <span class="uicontrol"> 단계 </span>를 마우스 오른쪽 단추로 클릭한 다음 <span class="uicontrol"> 새로 추가 </span> &gt; <span class="uicontrol"> 단계 </span>를 클릭합니다. </li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> 새 스테이지의 이름을 입력합니다. </li> 
      </ul> <p> <b>기존 처리 단계를 삭제하려면</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> 삭제할 스테이지에 해당하는 숫자를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span></i>를 클릭합니다. </li> 
      </ul> <p> <p>참고: <span class="wintitle"> Log Processing Dataset Include </span> 파일에 스테이지를 지정하는 경우 스테이지의 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. 데이터 집합 포함 파일에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 데이터 집합 포함 파일 </a>을 참조하십시오. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 시작 시간 </td> 
    <td colname="col2"> <p>선택 사항입니다. 이 시간 또는 그 후 타임스탬프가 있는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> <p> 예를 들어, 시작 시간으로 2013년 7월 29일 00:00:00 EDT를 지정하면 2013년 7월 29일, 12:00:00 AEM EDT에서 시작되는 데이터가 포함됩니다. </p> <p> 표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 시간대 약자 목록은 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a> 를 참조하십시오. </p> <p> <p>참고: 센서 및 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 변형 </td> 
    <td colname="col2"> <p>선택 사항입니다. 데이터에 적용할 변형을 정의합니다. 사용 가능한 변형 유형에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 데이터 변환 </a> 을 참조하십시오. </p> <p> <p>참고: Data Workbench <span class="filepath"> Transform.cfg </span> 파일에 정의된 경우 다음 변형 유형이 작동하지 않습니다. </p> </p> 
      <ul id="ul_B091DFBD1C33471BBC01AEC7E92FC8CC"> 
       <li id="li_660EBECFC407488199CCCC886326806D"> AppendURI </li> 
       <li id="li_56BCEBE4A2D044AE87F5B747C6501817"> 교차 행 </li> 
       <li id="li_B23B4E81B37942DCA55FEC1A6239C5FA"> ODBCLookup </li> 
       <li id="li_EF0AFF13C40D4AB49EAB4EF1691F8FA4"> 세션 </li> 
      </ul> </td> 
    </tr> 
  </tbody> 
  </table>

>[!NOTE]
>
>출력 파일을 닫은 후 추가 데이터를 받으면( 이전 테이블의 [!DNL Log Sources] 및 [!DNL Offline Mode] 참조) [!DNL Transform]에서 추가 데이터가 있는 새 출력 파일을 만듭니다. 새 출력 파일의 이름은 확장 바로 앞에 괄호로 묶인 버전 번호가 추가된 원본 출력 파일의 이름에서 생성됩니다. 예를 들어 원래 출력 파일이 [!DNL 20070701-ABC.vsl]이면 이 파일의 후속 버전은 [!DNL 20070701-ABC(1).vsl], [!DNL 20070701-ABC(2).vsl] 등으로 이름이 지정됩니다. Data Workbench 서버에 대한 입력으로 버전이 지정된 파일을 사용하면 처리 오류가 발생할 수 있습니다.
>
>
>Adobe은 사전순으로 정렬된 입력 파일 내에서 모든 소스 데이터가 시간 순서대로 있는지 확인하고 [!DNL Offline Mode] 이 true로 설정된 경우 처리가 시작되기 전에 모든 소스 데이터가 존재하는지 확인하여 버전이 지정된 출력 파일을 생성하지 않도록 권장합니다. 자세한 내용은 이전 테이블의 [!DNL Log Sources] 및 [!DNL Offline Mode] 항목을 참조하십시오.

1. **[!UICONTROL Transformations]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Transformation type]** 를 클릭하여 변형을 추가합니다. 변환 필드를 완료합니다.

   변형 기능에 사용할 수 있는 변형에 대한 설명 및 예는 [데이터 변환](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)을 참조하십시오.

1. 창 맨 위에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save]** 를 클릭합니다.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열의 Data Workbench [!DNL Transform.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > **[!UICONTROL profile name]**&#x200B;를 클릭하십시오. 여기서 프로필 이름은 데이터를 내보내는 프로필의 이름입니다. 프로필의 동기화 후 데이터 재처리가 시작됩니다.

   >[!NOTE]
   >
   >내보낼 데이터를 재처리하는 방법에 대한 자세한 내용은 [재처리 및 재변형](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.
