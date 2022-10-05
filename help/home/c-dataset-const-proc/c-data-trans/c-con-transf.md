---
description: 변환을 구성할 때 적용되는 규칙을 보여주는 표
title: 변환 구성을 위한 규칙
uuid: 91dddca6-4c17-4107-b78b-0f8b8870ef8d
exl-id: c2552c52-c6d3-4c9f-8359-b5a58bf1a59f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# 변환 구성을 위한 규칙{#conventions-for-constructing-transformations}

{{eol}}

변환을 구성할 때 적용되는 규칙을 보여주는 표

<table id="table_BEB0F6C416D144B5A2DD3D1A21613B21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 규칙 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 순차적 실행 </td> 
   <td colname="col2"> <p>데이터 집합 구성 파일 내의 변형은 로그 항목에 순차적으로(즉, 구성 파일에 나열된 순서대로) 적용됩니다. 따라서 변형이 다른 변형에 대한 입력으로 사용되는 순서대로 나열되어야 합니다. 보다 구체적으로, 한 변환의 출력을 다른 변환에 대한 입력으로 사용하는 경우 데이터 집합 구성 파일에서 이전 변환보다 먼저 해당 이전 변환에 나열된 것이 중요합니다. 그렇지 않으면 Data Workbench 서버에서 오류를 생성합니다. </p> <p> 처리 단계는 여러 데이터 세트 내에 정의된 변형에 파일을 포함하는 순서를 지정하는 방법을 제공합니다. 모든 데이터 집합에 특정 처리 스테이지와 연결된 파일이 포함되어 있으면 입력 및 출력에 따라 변형이 정렬됩니다. 또한 여러 데이터 집합에 스테이지 출력 데이터 내의 파일이 변환의 결과로 동일한 필드에 포함되는 경우 Data Workbench 서버에서 오류가 발생합니다. </p> <p> 단계에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일</a>, <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md"> 변형 구성 파일</a>, 및 <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> 데이터 집합에 파일 포함</a>. </p> <p>A <span class="wintitle"> 변형 종속성 맵</span> 일련의 변형으로 필드를 수정하는 방법을 표시할 수 있습니다. 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md"> 데이터 집합 구성 도구</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 이름 </td> 
   <td colname="col2"> 대부분의 변형은 출력 필드를 지정합니다. 출력이 사용자 정의 확장 필드인 경우 이 필드의 이름은 "x-"로 시작해야 합니다. 출력 필드 이름에는 공백이나 특수 문자를 사용할 수 없습니다. 확장 필드의 이름은 가독성을 위해 "x-NewCampaignName" 또는 "x-New-Campaign-Name"과 같이 대/소문자를 혼용할 수 있지만, 소프트웨어에서 대소문자를 구분하지 않는 것으로 처리됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 필드 </td> 
   <td colname="col2"> <p>입력 필드는 이전 변환의 출력으로 인해 생성되는 베이스라인 필드 또는 사용자 생성 필드 중 하나를 의미합니다. 상수 문자열이 필요한 경우 기준선 또는 사용자가 생성한 필드 대신 따옴표로 묶인 문자열을 사용할 수 있습니다. </p> <p> Data Workbench 서버가 처리할 수 있는 일반적으로 정의된 데이터 필드 중 일부 목록은 다음을 참조하십시오 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md"> 이벤트 데이터 레코드 필드</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 간단한 문자열 및 문자열 벡터 </td> 
   <td colname="col2"> 모든 변형은 문자열 및/또는 문자열 벡터에서 작동합니다. 단순 문자열은 문자의 리터럴 시퀀스입니다. 문자열 벡터는 특정 순서로 0개 이상의 간단한 문자열을 포함합니다. </td> 
  </tr> 
 </tbody> 
</table>
