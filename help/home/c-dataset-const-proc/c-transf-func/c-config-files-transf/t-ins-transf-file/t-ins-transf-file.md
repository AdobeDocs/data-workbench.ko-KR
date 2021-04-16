---
description: 데이터 워크벤치Transform.cfg 파일에는 로그 소스, 데이터 변환 및 내보내기 작업을 정의하는 매개 변수가 들어 있습니다.
title: Transform.cfg 파일
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
exl-id: e84f2536-cb22-4c47-a7a8-270b3c37ece6
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 2%

---

# Transform.cfg 파일{#the-transform-cfg-file}

데이터 워크벤치Transform.cfg 파일에는 로그 소스, 데이터 변환 및 내보내기 작업을 정의하는 매개 변수가 들어 있습니다.

사용자가 정의하는 변형은 센서( [!DNL .vsl] 파일)로 수집되거나 텍스트 파일, XML 파일 또는 ODBC 호환 데이터베이스에 포함되어 기존 필드로 출력하거나, 현재 데이터를 덮어쓰거나, 새로 정의된 필드로 출력합니다.

변형 기능을 구성하려면 이벤트 데이터를 내보내려는 프로필의 데이터 세트 폴더 내에 있는 데이터 워크벤치 [!DNL Transform.cfg] 파일을 편집합니다. 일반적으로 이 프로필은 변환 기능에 대한 전용 프로파일입니다. 즉, 데이터 워크벤치 [!DNL Transform.cfg] 파일에 정의된 것 이외의 다른 데이터 처리를 수행하지 않습니다. 상속된 프로파일에 대해 [!DNL Log Processing Dataset Include] 파일에 지정된 모든 처리 지침이 데이터 워크벤치 [!DNL Transform.cfg] 파일에 지정된 처리 지침 외에 적용됩니다.

데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 [데이터 세트에 파일 포함](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오.

내보내려는 데이터가 데이터 워크벤치 서버 클러스터에 의해 처리되는 경우 클러스터의 각 DPU(처리 서버)가 데이터를 처리하지만 첫 번째 DPU(처리 서버 #0 in the [!DNL profile.cfg] file)만 출력 데이터를 로컬 파일 시스템에 기록합니다.

**데이터 워크벤치 Transform.cfg 파일을 편집하려면**

1. 데이터를 내보낼 프로필에서 작업하는 동안 [!DNL Profile Manager]을 열고 **[!UICONTROL Dataset]**&#x200B;을 클릭하여 디렉토리의 내용을 표시합니다.
1. 데이터 워크벤치 [!DNL Transform.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 데이터 워크벤치 [!DNL Transform.cfg] 창이 나타납니다.
1. 아래 표를 참조하여 구성 파일의 매개 변수를 편집합니다.

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
    <td colname="col2"> <p>선택 사항입니다. 이번에는 타임스탬프가 포함되지만 포함되지는 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용할 것을 권장합니다. 
      <ul id="ul_C8C7F0F631594F7095CB83EF54E7CD0E"> 
       <li id="li_77AB6EEE8EEC4698AA886DE8BB0E2783"> 2013년 1월 1일 HH:MM:SS 편집 </li> 
       <li id="li_33806070F991476BB986906876CAF7F1"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 2013년 7월 29일 00:00:00 EDT를 <span class="wintitle"> 종료 시간 </span>으로 지정하는 경우 2013년 7월 28일(11:59:59 PM EDT에서)까지의 데이터가 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약어 목록은 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a>를 참조하십시오. </p> <p> 센서와 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 수출업체 </td> 
    <td colname="col2"> <p>내보내기 프로그램의 하위 필드는 출력 데이터의 처리 방법 및/또는 형식을 지정합니다. 로그 소스 집합에 대해 여러 내보내기 프로그램을 정의할 수 있습니다. 각 내보내기 유형은 출력을 독립적으로 만듭니다. </p> <p> 다음과 같은 세 가지 유형의 수출자가 있습니다. 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> Export구분된 텍스트 파일 </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> 내보내기 유형에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> 수출자 정의 </a>를 참조하십시오. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 해시 임계값 </td> 
    <td colname="col2"> 선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 인수. 숫자 n으로 설정하면 내보내기를 위해 각 n개 추적 ID 중 하나만 선택되므로 n의 계수로 내보낸 총 행 수가 줄어듭니다.모든 행을 내보내려면 해시 임계값을 1로 설정합니다. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 항목 조건 </td> 
    <td colname="col2"> 선택 사항입니다. 내보낼 로그 항목이 고려되는 규칙을 정의합니다. <span class="wintitle"> 로그 항목 조건 </span>에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>을 참조하십시오. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 소스 </td> 
    <td colname="col2"> <p>데이터 소스. <span class="wintitle"> 로그 소스는  </span> .vsl  <span class="filepath">   </span> 파일, 로그 파일, XML 파일 또는 ODBC 호환 데이터베이스의 데이터일 수 있습니다. <span class="wintitle"> 로그 소스 </span>에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>을 참조하십시오. </p> <p> <span class="wintitle"> 모든 소스 데이터가 사전순으로 정렬된 입력 파일 내에서 시간순으로 순서대로  </span> 검색되어야 합니다. 이 요구 사항이 만족스럽지 않으면 계산 결과가 잘못되고 출력 파일을 닫은 후에 추가 입력 데이터가 처리될 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 오프라인 모드 </td> 
    <td colname="col2"> <p>선택 사항입니다. True 또는 False. true인 경우 <span class="wintitle"> Transform </span>에서는 데이터 처리를 시작할 때 입력 파일이 모두 있다고 가정합니다. 입력 데이터를 모두 읽으면 <span class="wintitle"> Transform </span> 추가 데이터가 수신될 때까지 기다리지 않고 모든 출력 파일을 닫습니다. 기본값은 false입니다. </p> <p> <p>참고: <span class="wintitle"> 오프라인 모드 </span>이 true로 설정된 경우 <span class="wintitle"> 변환 </span>은(는) 처리를 시작하기 전에 모든 소스 데이터가 있어야 합니다. 출력 파일을 닫은 후 추가 데이터를 받는 경우 <span class="filepath"> VisualServer.log </span> 파일에 경고 메시지가 생성됩니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 재처리 </td> 
    <td colname="col2"> <p>선택 사항입니다. 모든 문자 또는 문자 조합을 여기에 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 <span class="wintitle"> 변환 </span> 컴퓨터에 저장하면 데이터 재처리가 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형 </a>을 참조하십시오. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 단계 </td> 
    <td colname="col2"> <p>선택 사항입니다. <span class="wintitle"> 로그 처리 데이터 세트에 사용할 수 있는 처리 단계 이름에는 데이터 워크벤치 <span class="filepath"> Transform.cfg </span> 파일 외에 실행되는 </span> 파일이 포함됩니다. 처리 단계는 <span class="wintitle"> 로그 처리 데이터 세트 포함 </span> 파일에 정의된 변형을 순서를 지정하는 방법을 제공합니다. 이 매개 변수는 여러 <span class="wintitle"> 로그 처리 데이터 집합 포함 </span> 파일 내에서 하나 이상의 변형을 정의했으며 내보내기 프로세스 중에 특정 지점에서 특정 변형을 수행하려는 경우 매우 유용합니다. </p> <p> 여기에 단계를 나열하는 순서는 데이터를 내보내는 동안 <span class="wintitle"> 로그 처리 데이터 세트 포함 </span> 파일의 변형이 실행되는 순서를 결정합니다. <span class="wintitle"> 사전 처리  </span> 및  <span class="wintitle"> 사후 처리 </span> 는 기본 단계에 포함됩니다. <span class="wintitle"> 사전 처리 </span> 는 항상 첫 번째 단계이며  <span class="wintitle"> 사후 처리 </span> 는 항상 마지막 단계입니다. 기본적으로 <span class="wintitle"> 기본값 </span>이라는 이름의 스테이지가 있습니다. </p> <p> <b>새 처리 단계를 추가하려면</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> 데이터 워크벤치 <span class="filepath"> Transform.cfg </span> 창에서 <span class="uicontrol"> 단계 </span>을 마우스 오른쪽 단추로 클릭한 다음 <span class="uicontrol"> 새로 추가 </span> &gt; <span class="uicontrol"> 스테이지 </span>를 클릭합니다. </li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> 새 스테이지의 이름을 입력합니다. </li> 
      </ul> <p> <b>기존 처리 단계를 삭제하려면</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> 삭제할 스테이지에 해당하는 번호를 마우스 오른쪽 버튼으로 클릭하고 <span class="uicontrol"> </span><i> 제거&lt; <span class="uicontrol"> #stage_number </span></i>를 클릭합니다. </li> 
      </ul> <p> <p>참고: <span class="wintitle"> 로그 처리 데이터 세트 </span> 파일에서 스테이지를 지정하는 경우 스테이지의 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. 데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 데이터 세트에 파일 </a>을(를) 참조하십시오. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 시작 시간 </td> 
    <td colname="col2"> <p>선택 사항입니다. 데이터를 필터링하여 타임스탬프가 있는 로그 항목을 이 시간 또는 그 후에 포함할 수 있습니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용할 것을 권장합니다. </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 2013년 1월 1일 HH:MM:SS 편집 </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> <p> 예를 들어 2013년 7월 29일 00:00:00 EDT를 시작 시간으로 지정하면 2013년 7월 29일부터 시작되는 데이터(12:00:00 AM EDT)가 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약어 목록은 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a>를 참조하십시오. </p> <p> <p>참고: 센서와 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 변형 </td> 
    <td colname="col2"> <p>선택 사항입니다. 데이터에 적용할 변형을 정의합니다. 사용 가능한 변형 유형에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 데이터 변형 </a>을 참조하십시오. </p> <p> <p>참고: 데이터 워크벤치 <span class="filepath"> Transform.cfg </span> 파일에 정의된 경우 다음 변형 유형이 작동하지 않습니다. </p> </p> 
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
>출력 파일이 닫힌 후 추가 데이터가 수신되는 경우(위 표의 [!DNL Log Sources] 및 [!DNL Offline Mode] 참조), [!DNL Transform]는 추가 데이터가 있는 새 출력 파일을 만듭니다. 새 출력 파일의 이름은 확장자 바로 앞에 괄호 안의 버전 번호가 추가되어 원본 출력 파일의 이름에서 생성됩니다. 예를 들어 원본 출력 파일이 [!DNL 20070701-ABC.vsl]인 경우 이 파일의 후속 버전은 [!DNL 20070701-ABC(1).vsl], [!DNL 20070701-ABC(2).vsl] 등으로 지정됩니다. 버전 관리 파일을 데이터 워크벤치 서버에 입력으로 사용하면 처리 오류가 발생할 수 있습니다.
>
>
>Adobe에서는 사전 정렬된 입력 파일 내에서 모든 소스 데이터가 시간 순서대로 순서대로 나열되고 [!DNL Offline Mode]이 true로 설정된 경우 처리가 시작되기 전에 모든 소스 데이터가 존재하도록 하여 버전을 매긴 출력 파일을 만들지 않는 것이 좋습니다. 자세한 내용은 위 표의 [!DNL Log Sources] 및 [!DNL Offline Mode] 항목을 참조하십시오.

1. **[!UICONTROL Transformations]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Transformation type]**&#x200B;를 클릭하여 변형을 추가합니다. 변형 필드를 완료합니다.

   변형 기능에 사용할 수 있는 변형에 대한 설명 및 예는 [데이터 변환](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)을 참조하십시오.

1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]에서 [!DNL User] 열에서 데이터 워크벤치 [!DNL Transform.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > **[!UICONTROL profile name]**&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터를 내보내는 프로필의 이름입니다. 프로필 동기화 후 데이터 재처리가 시작됩니다.

   >[!NOTE]
   >
   >내보낼 데이터를 재처리하는 방법에 대한 자세한 내용은 [재처리 및 재변형](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.
