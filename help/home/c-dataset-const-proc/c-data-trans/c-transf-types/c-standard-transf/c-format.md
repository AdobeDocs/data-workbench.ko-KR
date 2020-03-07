---
description: 형식 변환은 입력 세트를 가져와 지정된 구조와 일치하는 출력을 만듭니다.
solution: Analytics
title: 형식
topic: Data workbench
uuid: c596902e-21bc-4ce6-9ca4-7ca86dfc0a6c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 형식{#format}

형식 변환은 입력 세트를 가져와 지정된 구조와 일치하는 출력을 만듭니다.

변환은 단순 문자열 또는 문자열 벡터에서 작동하며 모든 입력 값이 변형될 때까지 각 입력 값에 주어진 형식을 적용하여 출력물을 생성합니다.

<table id="table_3953C993167248AA9A47964A51C4AB5D"> 
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
   <td colname="col1"> 형식 </td> 
   <td colname="col2"> <p>출력물이 표시되는 방식을 지정하는 데 사용되는 서식 문자열입니다. </p> <p> %1%이(가) 첫 번째 입력 벡터의 값을 참조하고, %2%은(는) 두 번째 입력 벡터의 값을 참조합니다. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>단순 문자열 또는 문자열 벡터가 포함된 필드. 문자열 벡터가 입력으로 사용되는 경우 출력도 Format 매개 변수의 적용에서 각 입력 값 세트에 <span class="wintitle"> 대한</span> 문자열 벡터가 됩니다. </p> <p> <p>참고: 입력 번호 매기는 0부터 시작되지만 형식 대체 값의 번호 매기는 %1%에서 시작됩니다. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 변환 결과를 포함하도록 만든 필드의 이름입니다. 입력 내용이 문자열 벡터인 경우 출력 문자열 벡터의 길이는 가장 긴 입력 벡터의 길이가 됩니다. 입력 문자열 벡터의 길이가 짧은 경우 출력 벡터의 길이에 도달할 때까지 형식 문자열에서 빈 문자열이 해당 위치에 사용됩니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 제품 카테고리를 나타내는 문자열 벡터와 구입한 각 제품의 수량을 나타내는 문자열 벡터로 구성된 두 개의 벡터가 동일한 길이의 단일 벡터로 변환됩니다.제품 %1%, 수량 %2%.

![](assets/cfg_TransformationType_Format.png)

입력 벡터에 (683, 918)의 제품 카테고리와 (10, 4)의 수량이 포함된 경우, 결과는 다음 두 문자열을 포함하는 하나의 최종 출력 벡터가 됩니다.(&quot;제품 683, 수량 10&quot;, &quot;제품 918, 수량 4&quot;).
