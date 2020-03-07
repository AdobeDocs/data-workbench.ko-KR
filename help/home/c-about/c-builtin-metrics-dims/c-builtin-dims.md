---
description: 데이터 워크벤치에는 내장 차원이 포함되어 있습니다.
solution: Analytics
title: 내장 차원
topic: Data workbench
uuid: 0aabbc52-266d-46c1-a4b3-dd575c0f2c72
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 내장 차원{#built-in-dimensions}

데이터 워크벤치에는 내장 차원이 포함되어 있습니다.

다음 표에는 데이터 워크벤치에 사용할 수 있는 내장 차원이 나열됩니다.

<table id="table_40796088B3484F98889859C59D525AD7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">  이름  </th> 
   <th colname="col2" class="entry"> 세부 사항 </th> 
   <th colname="col3" class="entry"> 레벨 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 없음 </td> 
   <td colname="col2"> 파생 </td> 
   <td colname="col3"> 해당 없음 </td> 
   <td colname="col4">모든 차원의 모든 요소와 관련된 단일 요소 ""가 있습니다. 없음으로 지표를 평가하는 것은 차원 없이 평가하는 것과 같습니다. <p>필터 <span class="filepath"> [None="]</span> 는 <span class="filepath"> [True]</span>와 같습니다. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 1(숨김) </td> 
   <td colname="col2"> 숫자 </td> 
   <td colname="col3"> 해당 없음 </td> 
   <td colname="col4">서수 값 <span class="filepath"> = 1이</span>있는 요소 "1"은 모든 차원의 모든 요소와 관련됩니다. One 차원은 일반적으로 다음 구문을 사용하여 카운트를 구성하는 데 사용됩니다. <p><span class="filepath"> sum(one,Countable_Dimension)</span></p></td> 
  </tr> 
 </tbody> 
</table>

