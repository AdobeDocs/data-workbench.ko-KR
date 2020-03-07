---
description: 데이터 세트 프로필에 대한 Transformation.cfg 파일을 편집하는 절차.
solution: Analytics
title: 변형 구성 파일 편집
topic: Data workbench
uuid: 77b9e566-4a9a-4ea1-b5ab-63a4574c0fdb
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변형 구성 파일 편집{#editing-the-transformation-configuration-file}

데이터 세트 프로필에 대한 Transformation.cfg 파일을 편집하는 절차.

1. 데이터 집합 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 클릭하여 내용을 **[!UICONTROL Dataset]** 표시합니다.

   데이터 워크벤치 사용자 안내서를 [!DNL Profile Manager]참조하여 데이터 워크벤치를 *엽니다*.

   >[!NOTE]
   >
   >Transformation 하위 디렉터리가 데이터 집합 디렉터리 내에 있을 수 있습니다. 이 하위 디렉토리에는 하나 이상의 상속된 프로파일에 대해 생성된 [!DNL Transformation Dataset Include] 파일이 포함되어 있습니다. 파일에 대한 자세한 내용은 [!DNL Transformation Dataset Include] 데이터 세트 포함 [파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL Transformation.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**&#x200B;를 클릭합니다. 창이 [!DNL Transformation.cfg] 나타납니다.

   또한 에서 [!DNL Transformation.cfg] 파일을 열 수 [!DNL Transformation Dependency Map]있습니다. 자세한 [!DNL transformation dependency maps]내용은 데이터 집합 [구성 도구를 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. 다음 표를 참조하여 구성 파일의 매개 변수를 편집합니다.

   데이터 워크벤치 창에서 파일을 편집할 때 단축키(Ctrl+x), 복사(Ctrl+C), 붙여넣기(Ctrl+V), 실행 취소(Ctrl+Z), 다시 실행(Ctrl+Shift+Z), 섹션 선택(클릭+드래그), 모두 선택(Ctrl+a)을 사용하여 기본 편집 기능을 사용할 수 있습니다. [!DNL Transformation.cfg] 또한 단축키를 사용하여 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 파일에 붙여넣을 수 있습니다.

   >[!NOTE]
   >
   >상속된 프로필의 [!DNL Transformation Dataset Include] 파일에는 다음 표에 설명된 매개 변수의 하위 집합과 일부 추가 매개 변수가 포함되어 있습니다. 파일에 대한 자세한 내용은 [!DNL Transformation Dataset Include] 데이터 세트에 [파일 포함 참조](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)

   <table id="table_5E184F67CCEC4421B2BBD4261711A6FE"> 
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
      <ul id="ul_1EC55DA4936946C98E447E1476E8280F"> 
       <li id="li_F2D862833F4B451C965E1ED6C05DCE1B"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_EB7FFEB2E2C24EAFB8E4B14F2479DA3D"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 종료 시간으로 "2013년 7월 29일 00:00:00 EDT"를 지정하면 2013년 7월 28일(오후 11:59:59)의 데이터가 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> <p>참고: 종료 시간에 대한 값을 지정하면 종료 시간이라는 매개 변수가 설정되고 데이터 세트 생성의 변형 단계 전체에 적용됩니다. 매개 변수에 대한 자세한 내용은 데이터 세트에 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 포함 파일의 매개 변수 정의를 참조하십시오 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 확장 차원 </td> 
      <td colname="col2"> 선택 사항입니다. 하나 이상의 변형 데이터 세트 포함 <span class="wintitle"></span> 파일에서 확장 차원을 정의하는 것이 좋습니다. 자세한 내용은 변형 데이터 세트에 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 파일 포함을 참조하십시오 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 해시 임계값 </td> 
      <td colname="col2"> <p>선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 각 n개의 추적 ID 중 한 개만 데이터 세트에 진입하여 n의 배율로 데이터 세트에 있는 총 행 수를 줄입니다.100% 정확도가 필요한 데이터 세트를 만들려면(즉, 모든 행을 포함하려면) 해시 임계값을 1로 설정합니다. </p> <p> Log Processing.cfg와 Transformation.cfg <span class="filepath"> 파일 모두에 해시 임계값이 지정된 경우 </span> <span class="filepath"> </span> 해당 임계값은 순서대로 적용되지 않습니다.구성 파일에 설정된 최대 값 중 하나가 적용됩니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 로그 항목 조건 </td> 
      <td colname="col2"> 선택 사항입니다. 데이터 집합 프로필에 포함할 것으로 간주되는 로그 처리 결과 로그 항목을 정의합니다. 로그 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 항목 조건을 참조하십시오 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 새 방문자 조건 </td> 
      <td colname="col2"> 선택 사항입니다. 웹 데이터에 사용 데이터에 포함할 방문자가 고려되는 규칙을 정의합니다. 새 <span class="wintitle"> 방문자 조건은 데이터 세트에 사용할 방문자(시간별 순서)의 첫 번째 로그 항목을 </span> 정의합니다. 이 방문자의 후속 로그 항목은 이 조건을 충족하는지 여부에 관계없이 데이터 세트에 포함됩니다. 새 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-new-vstr-con.md#concept-1d0d8e26718447ad9d235e00b33a36f3"> 방문자 조건을 </a>참조하십시오. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 재처리 </td> 
      <td colname="col2"> <p>선택 사항입니다. 모든 문자 또는 문자 조합을 여기에 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 저장하면 데이터 변환이 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 재처리 및 <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재변형을 참조하십시오 </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 스키마 확인 </td> 
      <td colname="col2"> 참 또는 거짓 true이면 데이터 워크벤치 서버가 데이터 세트 손상 문제를 식별하고 데이터 워크벤치 서버의 추적 디렉토리에 로그 파일의 문제에 대한 정보를 기록합니다. 기본값은 true입니다. 이 매개 변수를 항상 true로 설정하는 것이 좋습니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 단계 </td> 
      <td colname="col2"> <p>선택 사항입니다. 변환 데이터 세트에 사용할 수 있는 처리 단계의 이름은 <span class="wintitle"> 파일을 </span> 포함합니다. 처리 단계에서는 변형 데이터 세트 포함 파일에 정의된 변형을 <span class="wintitle"> 순서를 지정할 수 </span> 있습니다. 이 매개 변수는 여러 변형 데이터 세트 포함 <span class="wintitle"> </span> 파일에서 하나 이상의 변형을 정의했으며 변형 중에 특정 지점에서 특정 변형을 수행하려는 경우 매우 유용합니다. </p> <p> 여기에서 단계를 나열하는 순서에 따라 변형 데이터 세트 포함 파일의 <span class="wintitle"> 변형을 </span> 실행하는 순서가 결정됩니다. <span class="wintitle"> 전처리 </span> 및 <span class="wintitle"> 후처리 과정은 기본으로 </span> 되어 있다.사전 <span class="wintitle"> 처리는 </span> 항상 첫 번째 단계이며 <span class="wintitle"> 사후 처리는 </span> 항상 마지막 단계입니다. 기본적으로 Default라는 스테이지가 <span class="wintitle"> 있습니다 </span>. </p> <p> <b>새 처리 단계를 추가하려면</b> </p> <p> 
      <ul id="ul_6AF2EF72CEE34FA88575C46FA333BDA1"> 
       <li id="li_80627E7A89CE4E57A4228C4F5496533F"> Transformation.cfg <span class="filepath"> 창에서 단계를 마우스 오른쪽 단추로 </span> 클릭하고 <span class="uicontrol"> Add </span> New <span class="uicontrol"> &gt; Stage Statement </span> <span class="uicontrol"> </span>를 클릭합니다. </li> 
       <li id="li_321BEDB1E95F4AA4B282EED32A4CA196"> 새 스테이지의 이름을 입력합니다. </li> 
      </ul> </p> <p> <b>기존 처리 단계를 삭제하려면</b> </p> <p> 
      <ul id="ul_2EFA5A40982A48919E9946BF1955110A"> 
       <li id="li_3B3829DA34FD4774B3F9F94074099794"> 삭제할 스테이지에 해당하는 번호를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>를 클릭합니다. </li> 
      </ul> </p> <p> <p>참고: 변형 데이터 세트에 스테이지를 지정할 <span class="wintitle"> 때 포함 </span> 파일을 지정하면 스테이지의 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. 데이터 세트에 파일이 포함된 방법에 대한 자세한 내용은 데이터 세트 포함 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 파일을 참조하십시오 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시작 시간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 데이터를 필터링하여 타임스탬프가 있는 로그 항목을 이 시간 또는 이후에 포함할 수 있습니다. Adobe에서는 당분간 다음 형식 중 하나를 사용할 것을 권장합니다. 
      <ul id="ul_6BC86CCB1FC447ACAC4045E08C8EF8F8"> 
       <li id="li_2151B3F7FAD54F38B6C33E25CDCACBBE"> 2013년 1월 1일 HH:MM:SS EDT </li> 
       <li id="li_CA1BB675C1244104915FB9ED96A3013D"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 2013년 7월 29일 00:00:00 EDT를 시작 시간으로 지정하면 2013년 7 <span class="wintitle"> 월 29일부터 12:00:00 AM EDT에서 시작되는 데이터가 </span> 포함됩니다. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> <p>참고: 시작 시간에 대한 값을 지정하면 시작 시간이라는 매개 변수가 설정되고 데이터 세트 생성의 변형 단계 전체에 적용됩니다. 매개 변수에 대한 자세한 내용은 데이터 세트에 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 포함 파일의 매개 변수 정의를 참조하십시오 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 변형 </td> 
      <td colname="col2"> 선택 사항입니다. 하나 이상의 Transformation Dataset Include <span class="wintitle"> </span> 파일에서 데이터 세트 구성의 변형 단계를 정의하는 것이 좋습니다. 자세한 내용은 변형 데이터 세트에 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 파일 포함을 참조하십시오 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시간대 </td> 
      <td colname="col2"> <p>데이터 집합 프로필의 표준 시간대입니다. 시간대는 시간 변환과 시간 차원 생성에 사용됩니다. 시간대를 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> 참조하십시오 </a>. </p> <p> <p>참고: Log Processing. <span class="filepath"> cfg </span> 파일에 정의되면 시간대 매개 변수는 시간 변환에만 사용됩니다. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Transformation.cfg]> *를 [!DNL User] **[!UICONTROL Save to]** **[!UICONTROL dataset profile name]** 클릭하여 로컬에서 변경한 내용을 적용합니다. 데이터 집합 프로필의 동기화 후 데이터 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

   데이터 재처리 또는 재변환에 대한 자세한 내용은 재처리 및 [재변형을 참조하십시오](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
