---
description: 병합 변환은 입력 필드(일반적으로 문자열 벡터)의 값을 가져와 지정된 구분 기호로 구분된 단일 문자열로 결합하고 결과 문자열을 지정된 출력 필드에 배치합니다.
solution: Analytics
title: 병합
topic: Data workbench
uuid: 9ca2ab22-d854-47b0-8189-f563c1e83d1c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 병합{#merge}

병합 변환은 입력 필드(일반적으로 문자열 벡터)의 값을 가져와 지정된 구분 기호로 구분된 단일 문자열로 결합하고 결과 문자열을 지정된 출력 필드에 배치합니다.

<table id="table_2458E008C9A14B31A774E6819D07E9BE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">  이름  </td> 
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> 선택 사항입니다. 변환에 대한 참고 사항. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본값 </td> 
   <td colname="col2"> 조건이 충족되고 입력 값을 사용할 수 없는 경우 사용할 기본값입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구분 기호 </td> 
   <td colname="col2"> <p>입력 문자열 벡터의 개별 요소를 단일 출력 문자열에서 구분하는 데 사용되는 문자열입니다. </p> <p> Ctrl 키를 누른 채로 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 삽입 <span class="wintitle"> 메뉴가</span> 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 출력 문자열을 형성하기 위해 결합된 문자열 값의 벡터입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 출력 문자열의 이름입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

이 예에서 문자열 입력 벡터에 구입용으로 선택한 제품 세트가 포함되어 있다고 가정합니다. 이러한 제품은 단일 출력 문자열로 삽입되며 &quot;::&quot;(콜론 2개)로 구분됩니다.

![](assets/cfg_TransformationType_Merge.png)

따라서 입력 필드 x-제품에 문자열 값 B57481, C46355 및 Z97123이 포함되어 있으면 결과 출력 문자열 x-show-products는 B57481::C46355::Z971이 됩니다. 23.