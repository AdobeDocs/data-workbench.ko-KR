---
description: 데이터 집합 프로필에 대한 Log Processing.cfg 파일을 편집하는 단계입니다.
title: 로그 처리 구성 파일 편집
uuid: 2ffae53a-ef2f-4933-821d-13f29dcdb68d
exl-id: 294063ef-6771-4310-8198-df57fab1e2b4
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 2%

---

# 로그 처리 구성 파일 편집{#editing-the-log-processing-configuration-file}

데이터 집합 프로필에 대한 Log Processing.cfg 파일을 편집하는 단계입니다.

1. 데이터 집합 프로필에서 작업하는 동안 [!DNL Profile Manager] 을 열고 **[!UICONTROL Dataset]** 를 클릭하여 해당 콘텐츠를 표시합니다.

   [!DNL Profile Manager] 열기 및 작업에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

   >[!NOTE]
   >
   >로그 처리 하위 디렉터리가 데이터 집합 디렉터리에 있을 수 있습니다. 이 하위 디렉토리에는 하나 이상의 상속된 프로파일에 대해 생성된 [!DNL Log Processing Dataset Include] 파일이 있습니다. [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오.

1. [!DNL Log Processing.cfg] 옆의 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]** 를 클릭합니다. [!DNL Log Processing.cfg] 창이 나타납니다.

   [!DNL Transformation Dependency Map]에서 [!DNL Log Processing.cfg] 파일을 열 수도 있습니다. 변형 종속성 맵에 대한 자세한 내용은 [데이터 집합 구성 도구](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5)를 참조하십시오.

1. 다음 표를 안내서로 사용하여 구성 파일에서 매개 변수를 편집합니다.

   Data Workbench 창 내에서 [!DNL Log Processing.cfg] 파일을 편집할 때 잘라내기( Ctrl+x ), 복사( Ctrl+c), 붙여넣기( Ctrl+v ), 실행 취소( Ctrl+z ), 다시 실행( Ctrl+Shift+z ), 섹션 선택(클릭+드래그), 모두 선택( Ctrl+a )을 비롯한 기본적인 편집 기능에 바로 가기 키를 사용할 수 있습니다. 바로 가기를 사용하여 한 구성 파일( [!DNL .cfg])의 텍스트를 다른 구성 파일로 복사하고 붙여넣을 수도 있습니다.

   >[!NOTE]
   >
   >상속된 프로필에 대한 [!DNL Log Processing Dataset Include] 파일에는 다음 표에 설명된 매개 변수의 하위 집합과 일부 추가 매개 변수가 포함되어 있습니다. [데이터 집합에 파일 포함](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)을 참조하십시오.

   <table id="table_BC7D3635C94049A9B608463AC1DBFA69">
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> 매개 변수 </th> 
      <th colname="col2" class="entry"> 설명 </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> 로그 소스 </td> 
      <td colname="col2"> 데이터 소스. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 로그 소스 </a>를 참조하십시오. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 종료 시간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 최대 타임스탬프가 있지만 이 시간을 포함하지 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. </p> 
      <ul id="ul_42613B1D2F3A4A6C9563BC9B54BE895E"> 
      <li id="li_BC6E5FC5CA204D89936845BE05DFE6E6">2013년 1월 1일 HH:MM:SS EDT </li> 
      <li id="li_18FE1B0417AF4207B02497664F47D23F">2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> <p>예를 들어 2013년 7월 29일 00:00:00 EDT를 종료 시간으로 지정하는 경우 2013년 7월 28일까지 오후 11:59:59 EDT에서 데이터가 포함됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터 </a>를 참조하십시오. </p> <p>표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 시간대 약자 목록은 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a> 를 참조하십시오. </p> <p> <p>참고: <span class="wintitle"> 센서 </span>, 로그 파일 및 XML 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. 이러한 소스 유형에 대해 설명하는 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 로그 소스 </a> 섹션을 참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 필드 </td> 
      <td colname="col2"> 선택 사항입니다. Adobe은 하나 이상의 <span class="wintitle"> 로그 처리 데이터 집합에 </span> 파일을 포함하는 <span class="wintitle"> 필드를 정의하는 것이 좋습니다. </span> <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> 로그 처리 데이터 집합에 파일 </a> 포함 을 참조하십시오. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 그룹 최대 키 바이트 </td> 
      <td colname="col2"> <p>서버가 단일 추적 ID에 대해 처리할 수 있는 최대 이벤트 데이터 양입니다. 이 제한을 초과하는 데이터는 데이터 집합 구성 프로세스에서 필터링됩니다. 키 분할이 활성 상태일 때는 2e6로 설정하고 키 분할이 활성 상태가 아닐 때는 1e6로 설정해야 합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 키 분할 </a> 을 참조하십시오. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 해시 임계값 </td> 
      <td colname="col2"> <p>선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 각 n개의 추적 ID 중 한 개만 데이터 세트에 입력되므로 데이터 세트에 있는 총 행 수를 n의 계수로 줄일 수 있습니다. </p> <p>100% 정확도가 필요한 데이터 세트를 만들려면(즉, 모든 행을 포함하도록) 해시 임계값을 1로 설정합니다. </p> <p>값: </p> <span class="filepath"> 해시 임계값 = 1  </span> (모든 행을 포함하는 데이터의 100%) <p> <span class="filepath"> 해시 임계값 = 2  </span> (데이터의 1/2, 행의 절반을 포함합니다.) </p> <p> <span class="filepath"> 해시 임계값 = 3  </span>(데이터의 1/3, 세 행 중 하나를 포함하지만 쿼리 완료에서는 34%로 반올림됨) </p> <p> <span class="filepath"> 해시 임계값 = 4  </span>(데이터의 1/4분, 4개 행 중 1개 포함) </p> <p> </p> <p> <p>참고: <span class="filepath"> 해시 임계값 사용 = 8 </span>을 사용하면 데이터의 1/8번째(12.5%)가 제공됩니다. 그러나 이 값에 대해 반올림된 <span class="uicontrol"> 쿼리 완료 </span> 값은 13%로 반올림됩니다. 추가적인 예로는 <span class="filepath"> 해시 임계값 = 6 </span>이 있으며, 이 경우 쿼리 해상도는 17%입니다. <span class="filepath"> 해시 임계값 = 13 </span>은 8% 쿼리 해상도를 만듭니다. </p> </p> <p><span class="wintitle"> 해시 임계값 </span>이 <span class="filepath"> Log Processing.cfg </span> 및 <span class="filepath"> Transformation.cfg </span> 파일 모두에 지정되어 있으면 순서대로 적용되지 않습니다.두 구성 파일에 설정된 최대 값이 적용됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터 </a>를 참조하십시오. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 로그 항목 조건 </td> 
      <td colname="col2"> 선택 사항입니다. 데이터 집합에 포함할 로그 항목이 고려되는 규칙을 정의합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 로그 항목 조건 </a>을 참조하십시오. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 재처리 </td> 
      <td colname="col2"> <p>선택 사항입니다. 여기에 문자 또는 문자 조합을 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 Data Workbench 서버 시스템에 저장하면 데이터 재처리가 시작됩니다. </p> <p><a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형 </a>을 참조하십시오. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 키 버킷 공간 분할 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성화되면 해당 값은 6e6이어야 합니다. <a href="/help/home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#key-split"> 키 분할 </a> 을 참조하십시오. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 분할 키 바이트 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성 상태일 때는 1e6, 키 분할이 활성 상태가 아닐 때는 0이어야 합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 키 분할 </a> 을 참조하십시오. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 분할 키 공간 비율 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성화되면 해당 값은 10이어야 합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 키 분할 </a> 을 참조하십시오. </p> <p> <p>참고: 컨설팅 Adobe 없이 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 단계 </td> 
      <td colname="col2"> <p>선택 사항입니다. <span class="wintitle"> 로그 처리 데이터 집합에 사용할 수 있는 처리 단계의 이름에 </span> 파일이 포함됩니다. 처리 단계는 <span class="wintitle"> 로그 처리 데이터 집합에 정의된 변형에 </span> 파일을 정렬하는 방법을 제공합니다. 이 매개 변수는 여러 <span class="wintitle"> 로그 처리 데이터 집합 포함 </span> 파일 내에서 하나 이상의 변형을 정의했으며 로그 처리 중에 특정 지점에서 특정 변환을 수행하려는 경우에 매우 유용합니다. </p> <p>여기에서 단계를 나열하는 순서는 로그 처리 중 <span class="wintitle"> 로그 처리 데이터 집합에 포함된 </span> 파일의 변환이 실행되는 순서를 결정합니다. 사전 처리 및 사후 처리는 기본 단계입니다. 사전 처리는 항상 첫 번째 단계이며, 사후 처리는 항상 마지막 단계입니다. 기본적으로 Default라는 스테이지가 있습니다. </p> <p> <b>새 처리 단계를 추가하려면</b> 
      <ul id="ul_3A49BEAD1C134344999FED379B8CE7A3"> 
         <li id="li_AFC9B2529EC64642AFF98E9D5BA88C71"><span class="filepath"> Log Processing.cfg </span> 창에서 <span class="uicontrol"> 단계 </span>를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 새로 추가 </span> &gt; <span class="uicontrol"> 단계 </span>를 클릭합니다. </li> 
         <li id="li_5731B836658D4E1DB721C57C6275369A">새 스테이지의 이름을 입력합니다. </li> 
      </ul> </p> <p> <b>기존 처리 단계를 삭제하려면</b> 
      <ul id="ul_BBF4F710A5624C578F1F2A38FE18E9AD"> 
         <li id="li_CF6982C752DE41FFA97759C30CDE6AA0">삭제할 스테이지에 해당하는 숫자를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span></i>를 클릭합니다. </li> 
      </ul> </p> <p> <p>참고: <span class="wintitle"> 로그 처리 데이터 집합에 </span> 파일을 포함하는 <span class="wintitle"> 단계 </span>를 지정하는 경우 스테이지의 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 데이터 집합에 파일 </a> 포함 을 참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시작 시간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 이 시간 또는 그 후 타임스탬프가 있는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe은 해당 시간에 다음 형식 중 하나를 사용하는 것이 좋습니다. </p> <p> 
      <ul id="ul_0774889E22C24A6592809D289D1CBEC5"> 
         <li id="li_CE23541D8B584EA1AC432C5098564E46"> 2013년 1월 1일 HH:MM:SS EDT </li> 
         <li id="li_2EB0CF60CF12444BB744E52E9C919152"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 시작 시간으로 "2013년 7월 29일 00:00:00 EDT"를 지정하는 경우 2013년 7월 29일, 12:00:00 AEM EDT에서 시작하는 데이터가 포함됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터 </a>를 참조하십시오. </p> <p> 표준 시간대를 지정해야 합니다. 지정하지 않으면 시간대가 GMT로 기본값이 설정되지 않습니다. Data Workbench 서버에서 지원하는 시간대 약자 목록은 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드 </a> 를 참조하십시오. </p> <p> <p>참고: <span class="wintitle"> 센서 </span>, 로그 파일 및 XML 소스에 대한 시작/종료 시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. 이러한 소스 유형에 대해 설명하는 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 로그 소스 </a> 섹션을 참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시간대 </td> 
      <td colname="col2"> <p>선택 사항입니다. 로그 처리 중 시간 전환(예: x-local-timestring 필드로 표시되는 변환)에 사용되는 Data Workbench 서버의 시간대입니다. </p> <p> <p>참고: 데이터 집합 구성의 로그 처리 단계 동안 변환된 시간 필드에 액세스하려면 시간대를 지정해야 합니다. 그렇지 않으면 Data Workbench 서버가 이벤트 로그에 오류를 기록합니다. </p> </p> <p><a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> 시간대 </a>를 참조하십시오. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 변형 </td> 
      <td colname="col2"> 선택 사항입니다. Adobe은 하나 이상의 <span class="wintitle"> 로그 처리 데이터 집합에 </span> 파일을 포함하는 로그 처리에 대한 변환을 정의할 것을 권장합니다. <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> 로그 처리 데이터 집합에 파일 </a> 포함 을 참조하십시오. </td> 
   </tr> 
   </tbody> 
   </table>

1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.
1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL Log Processing.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]***&#x200B;를 클릭하여 로컬에서 변경한 내용을 적용합니다. 데이터 세트 프로필을 동기화한 후 데이터 재처리가 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공하는 내부 프로필에 저장하지 마십시오.

   데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)을 참조하십시오.
