---
description: 데이터 workbenchTransform.cfg 파일에는 로그 소스, 데이터 변형 및 내보내기 기능을 정의하는 매개 변수가 포함되어 있습니다.
solution: Analytics
title: Transform.cfg 파일
topic: Data workbench
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Transform.cfg 파일{#the-transform-cfg-file}

데이터 workbenchTransform.cfg 파일에는 로그 소스, 데이터 변형 및 내보내기 기능을 정의하는 매개 변수가 포함되어 있습니다.

정의한 변형은 센서가 수집하거나 텍스트 파일( [!DNL .vsl] 파일), XML 파일 또는 ODBC 호환 데이터베이스에 포함된 원시 데이터를 조작하여 기존 필드로 출력하거나, 현재 데이터를 덮어쓰거나, 새로 정의된 필드로 출력합니다.

변형 기능을 구성하려면 이벤트 데이터를 내보내려는 프로필의 데이터 세트 폴더 내에서 데이터 워크벤치 [!DNL Transform.cfg] 파일을 편집합니다. 일반적으로 이 프로파일은 변환 기능에 사용됩니다(즉, 데이터 워크벤치 [!DNL Transform.cfg] 파일에 정의된 것 이외의 다른 데이터 처리를 수행하지 않습니다). 상속된 프로파일에 대해 파일에 지정된 처리 지침은 데이터 워크벤치 [!DNL Log Processing Dataset Include] [!DNL Transform.cfg] 파일에 지정된 처리 지침 외에 적용됩니다.

데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 데이터 세트 [포함 파일을 참조하십시오](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

내보내려는 데이터가 데이터 워크벤치 서버 클러스터에 의해 처리되는 경우 클러스터의 각 처리 서버(DPU)가 데이터를 처리하지만 첫 번째 DPU( [!DNL profile.cfg] 파일의 처리 서버 #0)만 로컬 파일 시스템에 출력 데이터를 기록합니다.

**데이터 워크벤치 Transform.cfg 파일을 편집하려면**

1. 데이터를 내보낼 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 을 클릭하여 디렉토리의 컨텐츠를 **[!UICONTROL Dataset]** 표시합니다.
1. 데이터 워크벤치 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭한 [!DNL Transform.cfg]다음 을 클릭합니다 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
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
    <td colname="col2"> <p>선택 사항입니다. 타임스탬프가 포함되지만 포함되지는 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe에서는 당분간 다음 형식 중 하나를 사용할 것을 권장합니다. 
      <ul id="ul_C8C7F0F631594F7095CB83EF54E7CD0E"> 
       <li id="li_77AB6EEE8EEC4698AA886DE8BB0E2783"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_33806070F991476BB986906876CAF7F1"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 종료 시간으로 2013년 7월 29일 00:00:00 EDT를 지정하면 2013년 7월 28 <span class="wintitle"> 일 오후 11:59:59 PM EDT에 데이터가 </span> 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> 센서와 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 수출업자 </td> 
    <td colname="col2"> <p>내보내기 프로그램의 하위 필드는 출력 데이터의 처리 방법 및/또는 형식을 지정합니다. 로그 소스 세트에 대해 여러 내보내기 프로그램을 정의할 수 있습니다. 각 내보내기 유형은 독립적으로 출력을 만듭니다. </p> <p> 다음 세 가지 유형의 수출업체가 있습니다. 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> ExportDeletedTextFile </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> 내보내기 유형에 대한 자세한 내용은 수출자 정의를 <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> 참조하십시오 </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 해시 임계값 </td> 
    <td colname="col2"> 선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 내보내기를 위해 각 n개 추적 ID 중 하나만 선택되므로 n의 계수로 내보낸 총 행 수가 줄어듭니다.모든 행을 내보내려면 해시 임계값을 1로 설정합니다. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 항목 조건 </td> 
    <td colname="col2"> 선택 사항입니다. 내보내기를 위해 로그 항목이 고려되는 규칙을 정의합니다. 로그 항목 조건에 대한 <span class="wintitle"> 자세한 </span>내용은 로그 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 처리 구성 파일을 </a>참조하십시오. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 로그 소스 </td> 
    <td colname="col2"> <p>데이터 소스 <span class="wintitle"> 로그 소스는 </span> .vsl <span class="filepath"> 파일, 로그 파일, XML 파일 또는 ODBC 호환 데이터베이스의 데이터일 </span> 수 있습니다. 로그 소스에 대한 자세한 내용은 <span class="wintitle"> 로그 처리 구성 </span>파일을 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 참조하십시오 </a>. </p> <p> <span class="wintitle"> Transform </span> 에서는 모든 소스 데이터가 사전순으로 정렬된 입력 파일 내에서 시간순으로 정렬되어야 합니다. 이 요구 사항이 충족되지 않으면 계산 기준 값이 잘못되고 출력 파일이 닫힌 후 추가 입력 데이터가 처리될 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 오프라인 모드 </td> 
    <td colname="col2"> <p>선택 사항입니다. 참 또는 거짓 true인 경우 <span class="wintitle"> Transform은 데이터 처리를 시작할 때 모든 입력 파일이 있다고 </span> 가정합니다. 모든 입력 데이터를 읽으면 <span class="wintitle"> Transform은 추가 데이터가 수신될 때까지 기다리지 않고 모든 출력 파일을 </span> 닫습니다. 기본값은 false입니다. </p> <p> <p>참고: [ <span class="wintitle"> 오프라인 모드] </span> 가 true로 설정된 경우 <span class="wintitle"> 처리가 시작되기 전에 모든 소스 데이터가 존재해야 </span> 합니다. 출력 파일을 닫은 후 추가 데이터를 <span class="filepath"> 받으면 VisualServer.log </span> 파일에 경고 메시지가 생성됩니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 재처리 </td> 
    <td colname="col2"> <p>선택 사항입니다. 모든 문자 또는 문자 조합을 여기에 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 변형 <span class="wintitle"> 시스템으로 저장하면 데이터 재처리가 </span> 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 재처리 및 <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재변형을 참조하십시오 </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 단계 </td> 
    <td colname="col2"> <p>선택 사항입니다. 로그 처리 데이터 세트에 사용할 수 있는 처리 단계의 이름에는 <span class="wintitle"> 데이터 워크벤치 Transform.cfg </span> 파일 외에 실행되는 <span class="filepath"> 파일이 </span> 포함됩니다. 처리 단계에서는 로그 처리 데이터 세트 포함 파일에 정의된 변형을 <span class="wintitle"> 순서를 </span> 지정합니다. 이 매개 변수는 여러 로그 처리 데이터 집합 포함 <span class="wintitle"> </span> 파일에서 하나 이상의 변형을 정의했으며 내보내기 프로세스 동안 특정 지점에서 특정 변형을 수행하려는 경우 매우 유용합니다. </p> <p> 여기에서 단계를 나열하는 순서는 데이터를 내보내는 동안 로그 처리 데이터 집합 포함 <span class="wintitle"> 파일의 </span> 변형을 실행하는 순서를 결정합니다. <span class="wintitle"> 전처리 </span> 및 <span class="wintitle"> 후처리 과정은 기본으로 </span> 되어 있다.사전 <span class="wintitle"> 처리는 </span> 항상 첫 번째 단계이며 <span class="wintitle"> 사후 처리는 </span> 항상 마지막 단계입니다. 기본적으로 Default라는 스테이지가 <span class="wintitle"> 있습니다 </span>. </p> <p> <b>새 처리 단계를 추가하려면</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> 데이터 워크벤치 <span class="filepath"> Transform.cfg </span> 창에서 단계를 마우스 오른쪽 단추로 <span class="uicontrol"> 클릭한 다음 </span>새로 추가 <span class="uicontrol"> &gt; </span> 스테이지 <span class="uicontrol"> </span>를 클릭합니다. </li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> 새 스테이지의 이름을 입력합니다. </li> 
      </ul> <p> <b>기존 처리 단계를 삭제하려면</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> 삭제할 스테이지에 해당하는 번호를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>를 클릭합니다. </li> 
      </ul> <p> <p>참고: 로그 처리 데이터 집합 포함 <span class="wintitle"> 파일에서 스테이지를 지정할 </span> 때 스테이지의 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. 데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 데이터 세트 포함 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 파일을 참조하십시오 </a>. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 시작 시간 </td> 
    <td colname="col2"> <p>선택 사항입니다. 데이터를 필터링하여 타임스탬프가 있는 로그 항목을 이 시간 또는 이후에 포함할 수 있습니다. Adobe에서는 당분간 다음 형식 중 하나를 사용할 것을 권장합니다. </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> <p> 예를 들어 시작 시간으로 2013년 7월 29일 00:00:00 EDT를 지정하면 2013년 7월 29일부터 오전 12:00:00까지 데이터가 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> <p>참고: 센서와 로그 파일 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> 변형 </td> 
    <td colname="col2"> <p>선택 사항입니다. 데이터에 적용할 변형을 정의합니다. 사용 가능한 변형 유형에 대한 자세한 내용은 데이터 변형을 <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 참조하십시오 </a>. </p> <p> <p>참고: 데이터 워크벤치 Transform.cfg 파일에 정의된 경우 다음 변형 유형이 <span class="filepath"> 작동하지 않습니다 </span> . </p> </p> 
      <ul id="ul_B091DFBD1C33471BBC01AEC7E92FC8CC"> 
       <li id="li_660EBECFC407488199CCCC886326806D"> AppendURI </li> 
       <li id="li_56BCEBE4A2D044AE87F5B747C6501817"> CrossRows </li> 
       <li id="li_B23B4E81B37942DCA55FEC1A6239C5FA"> ODBCLookup </li> 
       <li id="li_EF0AFF13C40D4AB49EAB4EF1691F8FA4"> 세션화 </li> 
      </ul> </td> 
    </tr> 
  </tbody> 
  </table>

>[!NOTE]
>
>출력 파일을 닫은 후 추가 데이터를 받으면( [!DNL Log Sources] 및 [!DNL Offline Mode] 위 표 참조) 추가 데이터가 있는 새 출력 파일을 [!DNL Transform] 만듭니다. 새 출력 파일의 이름은 확장자 바로 전에 괄호로 묶은 버전 번호를 추가하여 원본 출력 파일의 이름에서 생성됩니다. 예를 들어 원본 출력 파일이 있는 경우 [!DNL 20070701-ABC.vsl]이 파일의 후속 버전 [!DNL 20070701-ABC(1).vsl]이름 [!DNL 20070701-ABC(2).vsl]등이 지정됩니다. 데이터 워크벤치 서버에 대한 입력으로 버전을 사용한 경우 처리 오류가 발생할 수 있습니다.
>
>
>Adobe에서는 사전에 정렬된 입력 파일 내에서 모든 소스 데이터가 시간 순서대로 순서대로 순서대로 처리되도록 하여 버전을 매긴 출력 파일을 만들지 않고, [!DNL Offline Mode] 이 값이 true로 설정된 경우 처리가 시작되기 전에 모든 소스 데이터가 존재하도록 할 것을 권장합니다. 자세한 내용은 위 표의 [!DNL Log Sources] 및 [!DNL Offline Mode] 항목을 참조하십시오.

1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Transformations]** > **[!UICONTROL Add new]** 를 클릭하여 변형을 **[!UICONTROL Transformation type]**&#x200B;추가합니다. 변형 필드를 완료합니다.

   변형 [기능에](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) 사용할 수 있는 변형에 대한 설명과 예는 데이터 변형을 참조하십시오.

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 단추를 클릭한 다음 을 클릭합니다 **[!UICONTROL Save]**.
1. 로컬에서 변경한 내용을 적용하려면 [!DNL Profile Manager]열에서 데이터 워크벤치에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Transform.cfg] > [!DNL User] **[!UICONTROL Save to]** **[!UICONTROL profile name]**&#x200B;를 클릭합니다. 여기서 프로필 이름은 데이터를 내보내는 프로필의 이름입니다. 프로필 동기화 후 데이터 재처리가 시작됩니다.

   >[!NOTE]
   >
   >내보내기를 위해 데이터를 재처리하는 방법에 대한 자세한 내용은 재처리 및 [재변형을 참조하십시오](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
