---
description: 변형을 구성할 때 적용되는 규칙을 보여주는 표.
solution: Analytics
title: 변형 구성을 위한 규칙
topic: Data workbench
uuid: 91dddca6-4c17-4107-b78b-0f8b8870ef8d
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변형 구성을 위한 규칙{#conventions-for-constructing-transformations}

변형을 구성할 때 적용되는 규칙을 보여주는 표.

<table id="table_BEB0F6C416D144B5A2DD3D1A21613B21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 컨벤션 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 순차적 실행 </td> 
   <td colname="col2"> <p>데이터 집합 구성 파일 내의 변환은 로그 항목에 순차적으로 적용됩니다(즉, 구성 파일에 나열되는 순서대로). 따라서 변형이 다른 변형에 대한 입력으로 사용되는 순서대로 나열되어야 합니다. 특히 한 변환의 출력을 다른 변환에 대한 입력으로 사용하는 경우 데이터 세트 구성 파일에서 이전 변환이 변환되기 전에 먼저 나열된 것이 중요합니다. 그렇지 않으면 데이터 워크벤치 서버에서 오류가 발생합니다. </p> <p> 처리 단계에서는 여러 데이터 세트 내에 정의된 변형 순서를 지정할 수 있습니다. 모든 데이터 세트에 특정 처리 단계에 연결된 파일이 포함되어 있으므로 입력 및 출력을 기반으로 변형이 순서가 지정됩니다. 또한 여러 데이터 세트에 변환 결과로 동일한 필드에 대한 스테이지 출력 데이터 내의 파일이 포함된 경우 데이터 워크벤치 서버에서 오류가 생성됩니다. </p> <p> 단계에 대한 자세한 내용은 로그 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 처리 구성 파일</a>, 변형 구성 파일 <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md"> 및</a>데이터 세트에 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 파일이</a>포함되어 있는 것을 참조하십시오. </p> <p>변형 <span class="wintitle"> 종속성 맵은</span> 일련의 변형으로 필드를 수정하는 방법을 표시할 수 있습니다. 데이터 <a href="../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md"> 집합 구성 도구를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 이름 </td> 
   <td colname="col2"> 대부분의 변형은 출력 필드를 지정합니다. 출력이 사용자 정의 확장 필드인 경우 이 필드의 이름은 "x-"로 시작해야 합니다. 출력 필드 이름에는 공백이나 특수 문자를 사용할 수 없습니다. 확장 필드의 이름은 "x-NewCampaignName" 또는 "x-New-Campaign-Name"과 같은 대/소문자를 혼합하여 작성할 수 있지만 소프트웨어에서 대/소문자를 구분하지 않는 것으로 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 필드 </td> 
   <td colname="col2"> <p>입력 필드는 이전 변환의 출력으로 인해 생성된 기준 필드 또는 사용자 생성 필드 중 하나를 나타냅니다. 상수 문자열이 필요한 경우 기준선 또는 사용자가 만든 필드 대신 인용 부호 문자열을 사용할 수 있습니다. </p> <p> 데이터 워크벤치 서버에서 처리할 수 있는 일반적으로 정의된 데이터 필드 중 일부 목록은 이벤트 데이터 레코드 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md"> 필드를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 간단한 문자열 및 문자열 벡터 </td> 
   <td colname="col2"> 모든 변형은 문자열 및/또는 문자열 벡터에서 작동합니다. 간단한 문자열은 문자 시퀀스입니다. 문자열 벡터에는 특정 순서로 0개 이상의 간단한 문자열이 포함됩니다. </td> 
  </tr> 
 </tbody> 
</table>

