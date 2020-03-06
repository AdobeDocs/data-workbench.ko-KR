---
description: 상속된 프로필에 대한 로그 처리 데이터 세트 포함 파일에는 데이터 집합 구성의 로그 처리 단계와 연결된 매개 변수가 포함되어 있습니다.
solution: Analytics
title: 로그 처리 데이터 세트에 파일 포함
topic: Data workbench
uuid: 8bf99c9a-f674-4a07-bb3e-de0d9efc9716
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 로그 처리 데이터 세트에 파일 포함{#log-processing-dataset-include-files}

상속된 프로필에 대한 로그 처리 데이터 세트 포함 파일에는 데이터 집합 구성의 로그 처리 단계와 연결된 매개 변수가 포함되어 있습니다.

파일의 첫 번째 줄은 디코더 그룹, 필드, 로그 항목 조건, 매개 변수, 재처리, 스테이지 및 변형 매개 변수를 지원하는 유형을 정의합니다. [!DNL Log Processing Dataset Include] [!DNL LogProcessingInclude] 로그 처리를 위한 다른 모든 매개 변수는 데이터 집합 프로필의 데이터 집합 디렉터리에 있는 [!DNL Log Processing.cfg] 파일에 정의해야 합니다. 파일 이름은 원하는 대로 지정할 수 있지만 파일 확장자는 [!DNL Log Processing Dataset Include] 이어야 합니다 [!DNL .cfg]. 파일은 *상속된 프로필 이름*\Dataset\Log Processing directory 내에 저장해야 합니다. 데이터 세트 생성의 로그 처리 단계 동안 파일이 반복적으로 로드되므로 디렉토리 내의 모든 수준에 [!DNL Log Processing Dataset Include] 파일을 저장할 수 있습니다(예: *상속된 프로파일 이름*\Dataset\Log Processing\*folder name*\*include file name*.cfg).

>[!NOTE]
>
>사이트에 대한 많은 웹 특정 구성 매개 변수가 [!DNL Log Processing Dataset Include] 파일에 정의되어 있습니다. 이러한 매개 변수에 대한 자세한 내용은 웹 [데이터에 대한 구성 설정을 참조하십시오](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

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
   <td colname="col2"> <p>Log Processing.cfg 파일에서 로그 파일 또는 XML 파일 로그 소스를 정의한 <span class="filepath"> 경우</span> 필요합니다. 로그 파일 및 XML 로그 소스에서 데이터 필드를 추출하기 위해 정의하는 텍스트 파일 또는 XML 디코더 </p> <p> <b>새 디코더 그룹을 추가하려면</b> 
     <ul id="ul_54087499003C48C8B0AD9660A2F46EA9"> 
      <li id="li_E361861E61D246DDB3964C97CC5187E9"> [디코더 그룹]을 마우스 오른쪽 단추로 <span class="uicontrol"> 클릭하고 [새로</span> 추가 <span class="uicontrol"> ] &gt; [</span> TextFileGroup <span class="uicontrol"> ] 또는 [XMLDecoderGroup</span> 디코더]를 <span class="uicontrol"></span>클릭합니다. </li> 
      <li id="li_B2D61A0763AD4FEDB619BF9550EF4602"> 새 그룹의 이름 매개 변수에 디코더 그룹의 원하는 이름을 입력합니다. </li> 
     </ul> </p> <p> <p>참고: 데이터 집합 프로필의 Log Processing.cfg <span class="filepath"> 파일에서</span> 디코더 그룹을 지정할 때 이 이름은 여기에 입력한 이름과 정확히 일치해야 합니다. 자세한 내용은 로그 파일을 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> 참조하십시오</a>. </p> </p> <p> 각 그룹에 대해 정의할 수 있는 디코더에 대한 자세한 내용은 텍스트 파일 디코더 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> 그룹</a> 또는 XML 디코더 그룹을 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필드 </td> 
   <td colname="col2"> <p>로그 소스 또는 <span class="wintitle"> 로그</span> 처리 <span class="wintitle"> 데이터 세트</span> 구성 <span class="wintitle"> 파일의 변형이나 변형에</span> 정의되어 있지만 변환 데이터 세트 구성 <span class="wintitle"> 파일의 변형, 조건, 확장 차원에 사용되는 필드를 나열해야</span> 합니다. </p> <p> 아래의 각 필드는 일부 로그 처리 데이터 세트 포함 <span class="wintitle"> 파일에 나열되어야</span> 합니다. 
     <ul id="ul_D1BB18A80D874C0B9B54DA361698EB30"> 
      <li id="li_7E8B5B697BDA408DBE10D9A63AF295AC"> x-trackingid </li> 
      <li id="li_F5DEE90A596A4A1C86AF874653C4048C"> x-timestamp </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 항목 조건 </td> 
   <td colname="col2"> <p>선택 사항입니다. 데이터 세트에 포함할 로그 항목이 고려되는 규칙을 정의합니다. 로그 <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> 항목 조건을 참조하십시오</a>. </p> <p> <p>참고: 데이터 세트에 포함하려면 로그 항목이 Log <span class="wintitle"> Processing.cfg</span> 파일과 모든 <span class="filepath"> Log Processing</span> Dataset Include <span class="wintitle"> 파일의 로그 항목 조건을</span> 충족해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 매개 변수 </td> 
   <td colname="col2"> 선택 사항입니다. 다른 구성 매개 변수에서 참조할 수 있는 변수입니다. 자세한 내용은 데이터 세트에 <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 포함 파일의 매개 변수 정의를 참조하십시오</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재처리 </td> 
   <td colname="col2"> <p>선택 사항입니다. 모든 문자 또는 문자 조합을 여기에 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 데이터 워크벤치 서버에 저장하면 데이터 재처리가 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 재처리 및 <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재변형을 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 스테이지 </td> 
   <td colname="col2"> <p>선택 사항입니다. 이 로그 처리 데이터 집합 포함 <span class="wintitle"> 파일에 적용되는 처리 단계의</span> 이름입니다. 처리 단계는 Log Processing.cfg 파일의 Stage 매개 <span class="filepath"> 변수에</span> 정의됩니다. </p> <p> <p>참고: 스테이지를 지정할 때 스테이지의 이름은 데이터 세트 프로필의 Log Processing.cfg 파일에 있는 Stage 매개 변수에 나열된 <span class="filepath"> 이름과</span> 정확히 일치해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 변형 </td> 
   <td colname="col2"> 선택 사항입니다. 로그 처리 중에 적용해야 하는 데이터 변형을 정의합니다. 사용 가능한 변환 유형에 대한 자세한 내용은 데이터 변형을 <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 참조하십시오</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>파일의 매개 변수에 대한 설명은 [!DNL Log Processing.cfg] 로그 처리 구성 [파일을 참조하십시오](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

파일을 사용하여 작업할 때마다 다음 사항을 고려해야 합니다. [!DNL Log Processing Dataset Include]

* 이 파일의 매개 변수를 변경하려면 모든 데이터를 다시 처리해야 합니다.
* 메모장에서 파일을 열고 편집하여 위에 설명된 매개 변수를 [!DNL Log Processing Dataset Include] 파일에 추가할 수 있습니다. 데이터 워크벤치에서 파일을 다시 열면 변경 사항이 모두 나타납니다. 새 매개 변수를 추가할 때 Tab 키가 아닌 Space 키를 사용하여 이전 제목 수준 오른쪽에 두 개의 공백을 들여씁니다.

