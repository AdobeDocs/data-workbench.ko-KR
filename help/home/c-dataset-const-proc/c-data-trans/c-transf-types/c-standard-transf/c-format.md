---
description: 형식 변환은 입력 집합을 사용하여 지정된 구조와 일치하는 출력을 만들기 위해 형식을 지정합니다.
title: 형식
uuid: c596902e-21bc-4ce6-9ca4-7ca86dfc0a6c
exl-id: 842b502e-cd16-45b3-ada8-6f2d899f1d54
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 3%

---

# 형식{#format}

형식 변환은 입력 집합을 사용하여 지정된 구조와 일치하는 출력을 만들기 위해 형식을 지정합니다.

변환은 단순 문자열 또는 문자열 벡터 중 하나에서 작동하며 모든 입력 값이 변형될 때까지 지정된 형식을 각 입력 값에 적용하여 출력을 생성합니다.

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
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
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
   <td colname="col2"> <p>출력이 표시되는 방식을 지정하는 데 사용되는 형식 문자열입니다. </p> <p> %1%이(가) 첫 번째 입력 벡터의 값을 참조하고 %2%은(는) 두 번째 입력 벡터의 값을 참조합니다. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>단순 문자열 또는 문자열 벡터를 포함하는 필드. 문자열 벡터를 입력으로 사용하는 경우 출력은 <span class="wintitle"> Format</span> 매개 변수를 각 입력 값 세트에 적용하여 생성되는 문자열 벡터이기도 합니다. </p> <p> <p>참고: 입력 번호 매기는 0부터 시작되지만 형식 대체 값의 번호 매기는 %1%에서 시작됩니다. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 변형 결과를 포함하도록 만든 필드의 이름입니다. 입력이 문자열 벡터이면 출력 문자열 벡터의 길이는 가장 긴 입력 벡터의 길이가 됩니다. 입력 문자열 벡터 중 일부가 길이가 짧은 경우 출력 벡터의 길이에 도달할 때까지 빈 문자열이 형식 문자열에서 해당 위치에 사용됩니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 제품 카테고리를 나타내는 문자열 벡터 1개와 각 제품의 구매 수량을 나타내는 해당 문자열 벡터가 다음 두 개의 벡터로 변형되며, 이 벡터는 다음과 같이 형식을 취합니다.제품 %1%, 수량 %2%.

![](assets/cfg_TransformationType_Format.png)

입력 벡터에 (683, 918) 및 수량 (10, 4)의 제품 카테고리가 포함된 경우 결과는 다음 두 문자열을 포함하는 하나의 최종 출력 벡터가 됩니다.(&quot;제품 683, 수량 10&quot;, &quot;제품 918, 수량 4&quot;)
