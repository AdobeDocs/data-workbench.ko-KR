---
description: 형식 변환은 주어진 구조와 일치하는 출력을 만들기 위해 입력 및 형식 집합을 사용합니다.
title: 형식
uuid: c596902e-21bc-4ce6-9ca4-7ca86dfc0a6c
exl-id: 842b502e-cd16-45b3-ada8-6f2d899f1d54
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 3%

---

# 형식{#format}

형식 변환은 주어진 구조와 일치하는 출력을 만들기 위해 입력 및 형식 집합을 사용합니다.

변형은 간단한 문자열 또는 문자열 벡터에서 작동하며 입력 값이 모두 변형될 때까지 각 입력 값에 주어진 형식을 적용하여 출력물을 생성합니다.

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
   <td colname="col2"> 변환의 설명형 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 변형에 대한 참고 사항 </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 형식 </td> 
   <td colname="col2"> <p>출력이 어떻게 표시되는지 지정하는 데 사용되는 형식 문자열입니다. </p> <p> %1%이(가) 첫 번째 입력 벡터의 값을 참조하고, %2%은(는) 두 번째 입력 벡터의 값을 참조합니다. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>단순 문자열 또는 문자열 벡터가 포함된 필드. 문자열 벡터가 입력으로 되어 있는 경우 출력도 <span class="wintitle"> Format</span> 매개 변수를 각 입력 값 집합에 적용하는 결과로 생성되는 문자열 벡터가 됩니다. </p> <p> <p>참고: 입력 번호 매기기를 0부터 시작하지만 형식 대체 값의 번호 매기기를 %1%에서 시작합니다. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 변환 결과를 포함하도록 만든 필드의 이름입니다. 입력이 문자열 벡터이면 출력 문자열 벡터의 길이가 가장 긴 입력 벡터의 길이가 됩니다. 입력 문자열 벡터의 길이가 짧은 경우 출력 벡터의 길이에 도달할 때까지 형식 문자열의 위치에 빈 문자열이 사용됩니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 제품 카테고리를 나타내는 문자열 벡터와 각 제품의 구매를 나타내는 해당 문자열 벡터의 2개의 벡터가 동일한 길이의 단일 벡터로 변환됩니다.제품 %1%, 수량 %2%.

![](assets/cfg_TransformationType_Format.png)

입력 벡터에 (683, 918)의 제품 카테고리와 (10, 4) 분량이 포함되어 있으면 다음 두 문자열을 포함하는 하나의 최종 출력 벡터가 됩니다.(&quot;제품 683, 수량 10&quot;, &quot;제품 918, 수량 4&quot;)
