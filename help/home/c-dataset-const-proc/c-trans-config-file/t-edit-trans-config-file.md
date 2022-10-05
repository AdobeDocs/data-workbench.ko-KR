---
description: 데이터 집합 프로필에 대한 Transformation.cfg 파일을 편집하는 단계입니다.
title: 변형 구성 파일 편집
uuid: 77b9e566-4a9a-4ea1-b5ab-63a4574c0fdb
exl-id: 3fab17a4-d356-4548-b977-f5d409870753
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 2%

---

# 변형 구성 파일 편집{#editing-the-transformation-configuration-file}

{{eol}}

데이터 집합 프로필에 대한 Transformation.cfg 파일을 편집하는 단계입니다.

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 을(를) 클릭합니다. **[!UICONTROL Dataset]** 콘텐츠를 표시합니다.

   열기 및 작업에 대한 자세한 내용은 [!DNL Profile Manager]를 참조하고 *Data Workbench 사용 안내서*.

   >[!NOTE]
   >
   >Transformation 하위 디렉터리가 데이터 집합 디렉터리 내에 있을 수 있습니다. 이 하위 디렉토리는 다음과 같습니다. [!DNL Transformation Dataset Include] 상속된 하나 이상의 프로필에 대해 생성된 파일입니다. 에 대한 자세한 정보 [!DNL Transformation Dataset Include] 파일, [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Transformation.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**. 다음 [!DNL Transformation.cfg] 창이 나타납니다.

   또한 [!DNL Transformation.cfg] 파일에서 [!DNL Transformation Dependency Map]. 에 대한 자세한 정보 [!DNL transformation dependency maps]를 참조하십시오. [데이터 집합 구성 도구](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. 다음 표를 안내서로 사용하여 구성 파일에서 매개 변수를 편집합니다.

   편집 시 [!DNL Transformation.cfg] data workbench 창 내의 파일에서는 잘라내기(Ctrl+x ), 복사(Ctrl+c), 붙여넣기(Ctrl+v), 실행 취소(Ctrl+z), 다시 실행(Ctrl+Shift+z), 섹션 선택(클릭+드래그)과 모두 선택(Ctrl+a )하는 등 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 또한 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])를 다른 이름으로 바꿉니다.

   >[!NOTE]
   >
   >A [!DNL Transformation Dataset Include] 상속된 프로파일에 대한 파일에는 다음 표에 설명된 매개 변수의 하위 집합과 일부 추가 매개 변수가 포함되어 있습니다. 에 대한 자세한 정보 [!DNL Transformation Dataset Include] 파일, [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)

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
      <td colname="col2"> <p>선택 사항. 이번에는 타임스탬프가 포함되지만 포함하지 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. 
      <ul id="ul_1EC55DA4936946C98E447E1476E8280F"> 
       <li id="li_F2D862833F4B451C965E1ED6C05DCE1B"> 2013년 1월 1일 HH:MM:SS 편집 </li> 
       <li id="li_EB7FFEB2E2C24EAFB8E4B14F2479DA3D"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 "2013년 7월 29일 00을 지정하는 경우:00:종료 시간으로 00 EDT"가 포함된 데이터는 2013년 7월 28일까지, 11시:59:동부 표준시 </p> <p> 표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 표준 시간대 약자 목록은 다음을 참조하십시오 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a>. </p> <p> <p>참고: 종료 시간에 대한 값을 지정하는 경우 End Time이라는 매개 변수가 설정되고 데이터 집합 구성의 변환 단계 전체에 적용됩니다. 매개 변수에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 데이터 집합에 있는 매개 변수 정의 포함 파일 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 확장된 차원 </td> 
      <td colname="col2"> 선택 사항. Adobe은 하나 이상의 확장 차원을 정의하는 것을 권장합니다 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 변형 데이터 집합에 파일 포함 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 해시 임계값 </td> 
      <td colname="col2"> <p>선택 사항. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 각 n개의 추적 ID 중 한 개만 데이터 세트에 입력되므로 데이터 세트에 있는 총 행 수를 n의 계수로 줄일 수 있습니다. 100% 정확도가 필요한 데이터 세트를 만들려면(즉, 모든 행을 포함하도록) 해시 임계값을 1로 설정합니다. </p> <p> 해시 임계값이 <span class="filepath"> Log Processing.cfg </span> 및 <span class="filepath"> Transformation.cfg </span> 파일, 순서대로 적용되지 않습니다. 두 구성 파일에 설정된 최대 값 수가 적용됩니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 로그 항목 조건 </td> 
      <td colname="col2"> 선택 사항. 로그 처리에서 출력되는 로그 항목이 데이터 집합 프로필에 포함되도록 간주되는 규칙을 정의합니다. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 로그 항목 조건 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 새 방문자 조건 </td> 
      <td colname="col2"> 선택 사항. 웹 데이터에 사용. 데이터에 포함할 방문자를 고려할 규칙을 정의합니다. 다음 <span class="wintitle"> 새 방문자 조건 </span> 데이터 집합에 사용할 방문자(시간별로 순서 지정)의 첫 번째 로그 항목을 정의합니다. 이 방문자의 모든 후속 로그 항목은 이 조건을 충족하는지 여부에 관계없이 데이터 세트에 포함됩니다. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-new-vstr-con.md#concept-1d0d8e26718447ad9d235e00b33a36f3"> 새 방문자 조건 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 재처리 </td> 
      <td colname="col2"> <p>선택 사항. 여기에 문자 또는 문자 조합을 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 저장하면 데이터 재변환이 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형 </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 스키마 확인 </td> 
      <td colname="col2"> True 또는 False입니다. true인 경우 Data Workbench 서버는 데이터 집합 손상 문제를 식별하고 Data Workbench 서버의 Trace 디렉토리에 있는 로그 파일의 문제에 대한 정보를 기록합니다. 기본값은 true입니다. Adobe은 이 매개 변수를 항상 true로 설정하는 것을 권장합니다. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 단계 </td> 
      <td colname="col2"> <p>선택 사항. 에서 사용할 수 있는 처리 단계의 이름 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일. 처리 단계는 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일. 이 매개 변수는 여러 변형에서 하나 이상의 변형을 정의한 경우에 매우 유용합니다 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일 및 변형 중에 특정 지점에서 특정 변형을 수행할 수 있습니다. </p> <p> 여기에서 단계를 나열하는 순서대로 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일을 변환하는 동안 실행됩니다. <span class="wintitle"> 사전 처리 </span> 및 <span class="wintitle"> 사후 처리 </span> 기본 제공 단계입니다. <span class="wintitle"> 사전 처리 </span> 항상 첫 번째 단계이고 <span class="wintitle"> 사후 처리 </span> 는 항상 마지막 단계입니다. 기본적으로 라는 스테이지가 있습니다 <span class="wintitle"> 기본값 </span>. </p> <p> <b>새 처리 단계를 추가하려면</b> </p> <p> 
      <ul id="ul_6AF2EF72CEE34FA88575C46FA333BDA1"> 
       <li id="li_80627E7A89CE4E57A4228C4F5496533F"> 에서 <span class="filepath"> Transformation.cfg </span> 창, 마우스 오른쪽 단추 클릭 <span class="uicontrol"> 단계 </span> 을(를) 클릭합니다. <span class="uicontrol"> 새로 추가 </span> &gt; <span class="uicontrol"> 단계 </span>. </li> 
       <li id="li_321BEDB1E95F4AA4B282EED32A4CA196"> 새 스테이지의 이름을 입력합니다. </li> 
      </ul> </p> <p> <b>기존 처리 단계를 삭제하려면</b> </p> <p> 
      <ul id="ul_2EFA5A40982A48919E9946BF1955110A"> 
       <li id="li_3B3829DA34FD4774B3F9F94074099794"> 삭제할 스테이지에 해당하는 숫자를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>. </li> 
      </ul> </p> <p> <p>참고: 스테이지를 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 스테이지 이름이 여기에 입력한 이름과 정확히 일치해야 하는 파일입니다. 데이터 집합 포함 파일에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 데이터 집합에 파일 포함 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시작 시간 </td> 
      <td colname="col2"> <p>선택 사항. 이 시간 또는 그 후 타임스탬프가 있는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. 
      <ul id="ul_6BC86CCB1FC447ACAC4045E08C8EF8F8"> 
       <li id="li_2151B3F7FAD54F38B6C33E25CDCACBBE"> 2013년 1월 1일 HH:MM:SS 편집 </li> 
       <li id="li_CA1BB675C1244104915FB9ED96A3013D"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 2013년 7월 29일 00을 지정하는 경우:00:00 EDT를 <span class="wintitle"> 시작 시간 </span> 에는 2013년 7월 29일, 12일에 시작된 데이터가 포함되어 있습니다:00:오전 시간 </p> <p> 표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 표준 시간대 약자 목록은 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a>. </p> <p> <p>참고: 시작 시간에 대한 값을 지정하는 경우 시작 시간이라는 매개 변수가 설정되고 데이터 집합 구성의 변환 단계 전체에 적용됩니다. 매개 변수에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 데이터 집합에 있는 매개 변수 정의 포함 파일 </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 변형 </td> 
      <td colname="col2"> 선택 사항. Adobe은 하나 이상의 데이터 집합 구성의 변형 단계에 대한 변형을 정의할 것을 권장합니다 <span class="wintitle"> 변형 데이터 집합에 포함 </span> 파일. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> 변형 데이터 집합에 파일 포함 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시간대 </td> 
      <td colname="col2"> <p>데이터 집합 프로필의 시간대입니다. 시간대는 시간 전환과 시간 차원 생성에 사용됩니다. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> 시간대 </a>. </p> <p> <p>참고: 에서 정의된 경우 <span class="filepath"> Log Processing.cfg </span> 파일에서 시간대 매개 변수는 시간 변환에만 사용됩니다. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Transformation.cfg]에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > * **[!UICONTROL dataset profile name]** 로컬에서 변경한 내용을 적용하려면 데이터 세트 프로필을 동기화한 후 데이터 재변환이 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.

   데이터 재처리 또는 재변형에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
