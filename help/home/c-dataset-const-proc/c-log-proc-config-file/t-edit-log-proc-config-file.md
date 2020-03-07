---
description: 데이터 집합 프로필에 대한 Log Processing.cfg 파일을 편집하는 절차.
solution: Analytics
title: 로그 처리 구성 파일 편집
topic: Data workbench
uuid: 2ffae53a-ef2f-4933-821d-13f29dcdb68d
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 로그 처리 구성 파일 편집{#editing-the-log-processing-configuration-file}

데이터 집합 프로필에 대한 Log Processing.cfg 파일을 편집하는 절차.

1. 데이터 집합 프로필에서 작업하는 동안 을 [!DNL Profile Manager] 열고 클릭하여 내용을 **[!UICONTROL Dataset]** 표시합니다.

   데이터 워크벤치 사용자 안내서를 [!DNL Profile Manager]참조하여 데이터 워크벤치를 *엽니다*.

   >[!NOTE]
   >
   >로그 처리 하위 디렉터리가 데이터 집합 디렉터리 내에 있을 수 있습니다. 이 하위 디렉토리에는 하나 이상의 상속된 프로파일에 대해 생성된 [!DNL Log Processing Dataset Include] 파일이 포함되어 있습니다. 데이터 [세트 포함 파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL Log Processing.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**&#x200B;를 클릭합니다. 창이 [!DNL Log Processing.cfg] 나타납니다.

   또한 에서 [!DNL Log Processing.cfg] 파일을 열 수 [!DNL Transformation Dependency Map]있습니다. 변환 종속성 맵에 대한 자세한 내용은 데이터 집합 [구성 도구를 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. 다음 표를 참조하여 구성 파일의 매개 변수를 편집합니다.

   데이터 워크벤치 창에서 [!DNL Log Processing.cfg] 파일을 편집할 때 바로 가기 키를 사용하여 잘라내기( Ctrl+x), 복사( Ctrl+c), 붙여넣기( Ctrl+v ), 실행 취소( Ctrl+z ), 다시 실행( Ctrl+Shift+z ), 섹션 선택(클릭+드래그), 모두 선택( Ctrl+a )을 비롯한 기본 편집 기능을 사용할 수 있습니다. 또한 단축키를 사용하여 한 구성 파일( [!DNL .cfg])의 텍스트를 복사하여 다른 구성 파일에 붙여넣을 수 있습니다.

   >[!NOTE]
   >
   >상속된 프로필의 [!DNL Log Processing Dataset Include] 파일에는 다음 표에 설명된 매개 변수의 하위 집합과 일부 추가 매개 변수가 포함되어 있습니다. 데이터 [세트 포함 파일을 참조하십시오](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

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
      <td colname="col2"> 데이터 소스 로그 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 소스를 참조하십시오 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 종료 시간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 타임스탬프가 있지만 이 시간이 포함되지 않는 로그 항목을 포함하도록 데이터를 필터링합니다. Adobe에서는 당분간 다음 형식 중 하나를 사용할 것을 권장합니다. </p> 
      <ul id="ul_42613B1D2F3A4A6C9563BC9B54BE895E"> 
      <li id="li_BC6E5FC5CA204D89936845BE05DFE6E6">2013년 1월 1일 HH:MM:SS EDT </li> 
      <li id="li_18FE1B0417AF4207B02497664F47D23F">2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> <p>예를 들어 종료 시간으로 2013년 7월 29일 00:00:00 EDT를 지정하면 2013년 7월 28일 오후 11:59:59에 데이터가 포함됩니다. 데이터 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 필터를 참조하십시오 </a>. </p> <p>시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> <p>참고: 센서, 로그 파일 및 XML 소스에 대한 <span class="wintitle"> 시작/종료 </span>시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. 이러한 소스 유형에 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 대해 </a> 설명하는 로그 소스 섹션을 참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 필드 </td> 
      <td colname="col2"> 선택 사항입니다. 하나 이상의 <span class="wintitle"> 로그 처리 데이터 세트 포함 </span> <span class="wintitle"> </span> 파일에서 필드를 정의하는 것이 좋습니다. 로그 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> 처리 데이터 세트 포함 파일을 </a>참조하십시오. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 그룹 최대 키 바이트 </td> 
      <td colname="col2"> <p>서버가 단일 추적 ID에 대해 처리할 수 있는 최대 이벤트 데이터 양입니다. 이 제한을 초과하는 데이터는 데이터 집합 구성 프로세스에서 필터링됩니다. 키 분할이 활성 상태인 경우 이 값을 2e6로 설정하고 키 분할이 활성화되지 않은 경우 1e6로 설정해야 합니다. 키 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 분할을 참조하십시오 </a>. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 해시 임계값 </td> 
      <td colname="col2"> <p>선택 사항입니다. 행의 임의 하위 샘플링을 위한 샘플링 요소입니다. 숫자 n으로 설정하면 각 n개의 추적 ID 중 한 개만 데이터 세트에 진입하여 n의 배율로 데이터 세트에 있는 총 행 수를 줄입니다. </p> <p>100% 정확도가 필요한 데이터 세트를 만들려면(즉, 모든 행을 포함하려면) 해시 임계값을 1로 설정합니다. </p> <p>값: </p> <span class="filepath"> 해시 임계값 = 1 </span> (모든 행을 포함한 데이터의 100%) <p> <span class="filepath"> 해시 임계값 = 2 </span> (데이터의 1/2, 행의 절반 포함) </p> <p> <span class="filepath"> 해시 임계값 = 3 </span>(데이터의 1/3, 3개 행 중 하나 포함, 쿼리 완료에서 34%로 반올림됨) </p> <p> <span class="filepath"> 해시 임계값 = 4 </span>(데이터의 1/4분의 1, 4개 행 중 1개 포함) </p> <p> </p> <p> <p>참고: 해시 임계값 <span class="filepath"> 사용 = 8 </span> 은 데이터의 1/8을 제공하며, 이것은 12.5%입니다. 그러나 <span class="uicontrol"> 이 값에 대한 질의 완료 </span> 값은 13%로 반올림됩니다. 추가 예에는 17%의 쿼리 <span class="filepath"> 해상도를 </span> 가져오는 해시 임계값 = 6이 포함됩니다. 해시 <span class="filepath"> 임계값 = 13으로 </span>인해 쿼리 해상도가 8%입니다. </p> </p> <p>해시 <span class="wintitle"> 임계값이 Log Processing.cfg </span> 및 Transformation.cfg <span class="filepath"> 파일에 모두 지정된 경우 </span> <span class="filepath"> </span> 순서에 적용되지 않습니다.구성 파일의 최대 값 세트가 적용됩니다. 데이터 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 필터를 참조하십시오 </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 로그 항목 조건 </td> 
      <td colname="col2"> 선택 사항입니다. 데이터 세트에 포함할 로그 항목이 고려되는 규칙을 정의합니다. 로그 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 항목 조건을 참조하십시오 </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 재처리 </td> 
      <td colname="col2"> <p>선택 사항입니다. 모든 문자 또는 문자 조합을 여기에 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 데이터 워크벤치 서버 시스템으로 저장하면 데이터 재처리가 시작됩니다. </p> <p>재처리 <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 및 재변형을 참조하십시오 </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 키 버킷 공간 분할 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성화되면 값은 6e6이어야 합니다. 키 <a href="/help/home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#key-split"> 분할을 참조하십시오 </a>. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 키 바이트 분할 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성 상태인 경우 1e6이고 키 분할이 활성화되지 않은 경우 0이어야 합니다. 키 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 분할을 참조하십시오 </a>. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 분할 키 공간 비율 </td> 
      <td colname="col2"> <p>키 분할에 관련된 매개 변수입니다. 키 분할이 활성화되면 값은 10이어야 합니다. 키 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> 분할을 참조하십시오 </a>. </p> <p> <p>참고: Adobe에 문의하지 않고 이 값을 변경하지 마십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 단계 </td> 
      <td colname="col2"> <p>선택 사항입니다. 로그 처리 데이터 세트에 사용할 수 있는 처리 단계의 이름은 <span class="wintitle"> 파일을 </span> 포함합니다. 처리 단계에서는 로그 처리 데이터 세트 포함 파일에 정의된 변형을 <span class="wintitle"> 순서를 </span> 지정합니다. 이 매개 변수는 여러 로그 처리 데이터 집합 포함 <span class="wintitle"> 파일에서 하나 이상의 변형을 정의했으며 </span> 로그 처리 중 특정 지점에서 특정 변형을 수행하려는 경우 매우 유용합니다. </p> <p>여기에서 단계를 나열하는 순서는 로그 처리 데이터 세트 포함 <span class="wintitle"> 파일의 변형이 </span> 실행되는 순서를 결정합니다. 사전 처리 및 사후 처리는 기본 단계입니다. 사전 처리는 항상 첫 번째 단계이며 사후 처리는 항상 마지막 단계입니다. 기본적으로 Default라는 스테이지가 있습니다. </p> <p> <b>새 처리 단계를 추가하려면</b> 
      <ul id="ul_3A49BEAD1C134344999FED379B8CE7A3"> 
         <li id="li_AFC9B2529EC64642AFF98E9D5BA88C71">Log <span class="filepath"> Processing.cfg </span> 창에서 단계를 마우스 오른쪽 단추로 클릭하고 [새 단계 추가] <span class="uicontrol"> &gt; </span> [새 <span class="uicontrol"> 단계 </span> <span class="uicontrol"> </span>]를 클릭합니다. </li> 
         <li id="li_5731B836658D4E1DB721C57C6275369A">새 스테이지의 이름을 입력합니다. </li> 
      </ul> </p> <p> <b>기존 처리 단계를 삭제하려면</b> 
      <ul id="ul_BBF4F710A5624C578F1F2A38FE18E9AD"> 
         <li id="li_CF6982C752DE41FFA97759C30CDE6AA0">삭제할 스테이지에 해당하는 번호를 마우스 오른쪽 단추로 클릭하고 <span class="uicontrol"> 제거 </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>를 클릭합니다. </li> 
      </ul> </p> <p> <p>참고: 로그 처리 <span class="wintitle"> 데이터 세트 포함 </span> 파일에서 스테이지를 지정할 <span class="wintitle"> </span> 때 스테이지의 이름은 여기에 입력한 이름과 정확히 일치해야 합니다. 데이터 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 세트에 파일 포함을 </a>참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시작 시간 </td> 
      <td colname="col2"> <p>선택 사항입니다. 데이터를 필터링하여 타임스탬프가 있는 로그 항목을 이 시간 또는 이후에 포함할 수 있습니다. Adobe에서는 당분간 다음 형식 중 하나를 사용할 것을 권장합니다. </p> <p> 
      <ul id="ul_0774889E22C24A6592809D289D1CBEC5"> 
         <li id="li_CE23541D8B584EA1AC432C5098564E46"> 2013년 1월 1일 HH:MM:SS EDT </li> 
         <li id="li_2EB0CF60CF12444BB744E52E9C919152"> 2013년 1월 1일 HH:MM:SS GMT </li> 
      </ul> </p> <p> 예를 들어 시작 시간으로 "July 29 2013 00:00:00 EDT"를 지정하면 2013년 7월 29일부터 12:00:00 AM EDT에서 시작되는 데이터가 포함됩니다. 데이터 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 필터를 참조하십시오 </a>. </p> <p> 시간대를 지정해야 합니다. 지정하지 않으면 표준 시간대가 GMT로 기본값이 설정되지 않습니다. 데이터 워크벤치 서버에서 지원하는 표준 시간대 약자 목록은 시간대 <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 코드를 참조하십시오 </a>. </p> <p> <p>참고: 센서, 로그 파일 및 XML 소스에 대한 <span class="wintitle"> 시작/종료 </span>시간 사용 매개 변수는 이 매개 변수와 관련되어 있습니다. 이러한 소스 유형에 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> 대해 </a> 설명하는 로그 소스 섹션을 참조하십시오. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 시간대 </td> 
      <td colname="col2"> <p>선택 사항입니다. 로그 처리 중 시간 변환에 사용되는 데이터 워크벤치 서버의 표준 시간대(예: x-local-timestring 필드로 표시되는 전환)입니다. </p> <p> <p>참고: 데이터 집합 구성의 로그 처리 단계 중 변환된 시간 필드에 액세스하려면 시간대를 지정해야 합니다. 그렇지 않으면 데이터 워크벤치 서버가 이벤트 로그에 오류를 기록합니다. </p> </p> <p>시간대를 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> 참조하십시오 </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 변형 </td> 
      <td colname="col2"> 선택 사항입니다. 하나 이상의 로그 처리 데이터 세트 포함 <span class="wintitle"> </span> 파일에서 로그 처리를 위한 변형을 정의하는 것이 좋습니다. 로그 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> 처리 데이터 세트 포함 파일을 </a>참조하십시오. </td> 
   </tr> 
   </tbody> 
   </table>

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Log Processing.cfg]> [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭하여 로컬에서 변경한 내용을 적용합니다&#x200B;**[!UICONTROL dataset profile name]*** . 데이터 집합 프로필의 동기화 후 데이터 재처리가 시작됩니다.

   >[!NOTE]
   >
   >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필에 저장하지 마십시오.

   데이터 재처리에 대한 자세한 내용은 재처리 및 [재변형을 참조하십시오](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
