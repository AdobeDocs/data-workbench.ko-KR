---
description: 상속된 프로파일에 대한 로그 처리 데이터 세트 포함 파일에는 데이터 집합 구성의 로그 처리 단계와 연관된 매개 변수가 포함되어 있습니다.
title: 로그 처리 데이터 세트에 파일 포함
uuid: 8bf99c9a-f674-4a07-bb3e-de0d9efc9716
exl-id: 06d8046d-6bac-4ccd-bcef-06f7c9ec7619
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 3%

---

# 로그 처리 데이터 세트에 파일 포함{#log-processing-dataset-include-files}

{{eol}}

상속된 프로파일에 대한 로그 처리 데이터 세트 포함 파일에는 데이터 집합 구성의 로그 처리 단계와 연관된 매개 변수가 포함되어 있습니다.

의 첫 번째 줄 [!DNL Log Processing Dataset Include] 파일 정의 형식 [!DNL LogProcessingInclude] 디코더 그룹, 필드, 로그 항목 조건, 매개 변수, 재처리, 스테이지 및 변환 매개 변수를 지원합니다. 로그 처리를 위한 다른 모든 매개 변수는 [!DNL Log Processing.cfg] 데이터 집합 프로필의 데이터 집합 디렉터리에 있는 파일입니다. 이름을 [!DNL Log Processing Dataset Include] 원하는 모든 파일을 파일이지만 파일 확장명은 [!DNL .cfg]. 파일은 *상속된 프로필 이름*\Dataset\Log Processing 디렉터리입니다. 데이터 집합 구성의 로그 처리 단계 중에 파일이 재귀적으로 로드되므로 [!DNL Log Processing Dataset Include] 디렉토리 내의 임의의 레벨에 있는 파일(예: *상속된 프로필 이름*\Dataset\Log Processing\*folder name*\*include file name*.cfg)

>[!NOTE]
>
>사이트에 대한 많은 웹 특정 구성 매개 변수는 [!DNL Log Processing Dataset Include] 파일. 이러한 매개 변수에 대한 자세한 내용은 [웹 데이터에 대한 구성 설정](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

<table id="table_E2112652CCD443E889A529EEDC4ADF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 디코더 그룹 </td> 
   <td colname="col2"> <p>로그 파일 또는 XML 파일 로그 소스를 <span class="filepath"> Log Processing.cfg</span> 파일. 로그 파일 및 XML 로그 소스에서 데이터 필드를 추출하기 위해 정의하는 텍스트 파일 또는 XML 디코더입니다. </p> <p> <b>새 디코더 그룹을 추가하려면</b> 
     <ul id="ul_54087499003C48C8B0AD9660A2F46EA9"> 
      <li id="li_E361861E61D246DDB3964C97CC5187E9"> 마우스 오른쪽 단추 클릭 <span class="uicontrol"> 디코더 그룹</span> 을(를) 클릭합니다. <span class="uicontrol"> 새로 추가</span> &gt; <span class="uicontrol"> 텍스트 파일 디코더 그룹</span> 또는 <span class="uicontrol"> XMLDecoderGroup</span>. </li> 
      <li id="li_B2D61A0763AD4FEDB619BF9550EF4602"> 새 그룹의 이름 매개 변수에 원하는 디코더 그룹의 이름을 입력합니다. </li> 
     </ul> </p> <p> <p>참고: 에서 디코더 그룹을 지정하는 경우 <span class="filepath"> Log Processing.cfg</span> 데이터 세트 프로필의 파일에서는 이 이름이 여기에 입력한 이름과 정확히 일치해야 합니다. 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> 로그 파일</a>. </p> </p> <p> 각 그룹에 대해 정의할 수 있는 디코더에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> 텍스트 파일 디코더 그룹</a> 또는 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML 디코더 그룹</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필드 </td> 
   <td colname="col2"> <p>에 정의된 필드를 나열합니다 <span class="wintitle"> 로그 소스</span> 또는 <span class="wintitle"> 변형</span> 에서 <span class="wintitle"> 로그 처리 데이터 집합 구성</span> 파일에서 변형, 조건 또는 확장 차원에 사용됨 <span class="wintitle"> 변형 데이터 집합 구성</span> 여기에 파일을 나열해야 합니다. </p> <p> 아래 각 필드는 일부 필드에 나열해야 합니다 <span class="wintitle"> 로그 처리 데이터 집합에 포함</span> 파일: 
     <ul id="ul_D1BB18A80D874C0B9B54DA361698EB30"> 
      <li id="li_7E8B5B697BDA408DBE10D9A63AF295AC"> x-trackingid </li> 
      <li id="li_F5DEE90A596A4A1C86AF874653C4048C"> x-timestamp </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 항목 조건 </td> 
   <td colname="col2"> <p>선택 사항. 데이터 집합에 포함할 로그 항목이 고려되는 규칙을 정의합니다. 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 로그 항목 조건</a>. </p> <p> <p>참고: 데이터 집합에 포함하려면 로그 항목이 <span class="wintitle"> 로그 항목 조건</span> 에서 <span class="filepath"> Log Processing.cfg</span> 파일 및 <span class="wintitle"> 로그 처리 데이터 집합에 포함</span> 파일. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 매개 변수 </td> 
   <td colname="col2"> 선택 사항. 다른 구성 매개 변수에서 참조할 수 있는 변수입니다. 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 데이터 집합에 있는 매개 변수 정의 포함 파일</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재처리 </td> 
   <td colname="col2"> <p>선택 사항. 여기에 문자 또는 문자 조합을 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 Data Workbench 서버에 저장하면 데이터 재처리가 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 단계 </td> 
   <td colname="col2"> <p>선택 사항. 여기에 적용되는 처리 단계의 이름입니다 <span class="wintitle"> 로그 처리 데이터 집합에 포함</span> 파일. 처리 단계는 <span class="filepath"> Log Processing.cfg</span> 파일. </p> <p> <p>참고: Stage를 지정할 때 Stage의 이름은 Stage의 Stage 매개 변수에 나열된 이름과 정확히 일치해야 합니다 <span class="filepath"> Log Processing.cfg</span> 데이터 집합 프로필의 파일입니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 변형 </td> 
   <td colname="col2"> 선택 사항. 로그 처리 중에 적용해야 하는 데이터 변형을 정의합니다. 사용 가능한 변형 유형에 대한 자세한 내용은 <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 데이터 변환</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>의 매개 변수에 대한 설명 [!DNL Log Processing.cfg] 파일, [로그 처리 구성 파일](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

작업할 때마다 다음 사항을 염두에 두어야 합니다 [!DNL Log Processing Dataset Include] 파일:

* 이 파일에서 매개 변수를 변경하려면 모든 데이터를 재처리해야 합니다.
* 위에 설명된 매개 변수를 [!DNL Log Processing Dataset Include] 파일을 열고 메모장에서 편집하여 파일을 엽니다. 사용자가 만들고 저장하는 모든 변경 사항은 Data Workbench에서 파일을 다시 열면 나타납니다. 새 매개 변수를 추가할 때 Space 키(Tab 키 아님)를 사용하여 이전 제목 수준 오른쪽에 있는 두 개의(2) 공백을 들여씁니다.
