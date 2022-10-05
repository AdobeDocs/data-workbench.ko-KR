---
description: Data Workbench에는 기본 제공 차원이 포함되어 있습니다.
title: 내장 차원
uuid: 0aabbc52-266d-46c1-a4b3-dd575c0f2c72
exl-id: c08a487d-60b8-4db7-8776-7ae1b9f1f27c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 14%

---

# 내장 차원{#built-in-dimensions}

{{eol}}

Data Workbench에는 기본 제공 차원이 포함되어 있습니다.

다음 표에는 Data Workbench에 사용할 수 있는 기본 제공 차원이 나열되어 있습니다.

<table id="table_40796088B3484F98889859C59D525AD7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 세부 사항 </th> 
   <th colname="col3" class="entry"> 레벨 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 없음 </td> 
   <td colname="col2"> 파생 </td> 
   <td colname="col3"> 해당 사항 없음 </td> 
   <td colname="col4">모든 차원의 모든 요소와 관련된 단일 요소 ""가 있습니다. 없음을 통해 지표를 평가하는 것은 차원을 기준으로 평가하는 것과 같습니다. <p>다음 <span class="filepath"> 필터 [None=""]</span> 은 <span class="filepath"> [True]</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 하나(숨김) </td> 
   <td colname="col2"> 숫자 </td> 
   <td colname="col3"> 해당 사항 없음 </td> 
   <td colname="col4">서수 값도 있는 요소 "1" <span class="filepath"> = 1</span>는 모든 차원의 모든 요소에 해당됩니다. 한 차원은 일반적으로 다음 구문을 사용하여 카운트를 구성하는 데 사용됩니다. <p><span class="filepath"> sum(one,Countable_Dimension)</span></p></td> 
  </tr> 
 </tbody> 
</table>
