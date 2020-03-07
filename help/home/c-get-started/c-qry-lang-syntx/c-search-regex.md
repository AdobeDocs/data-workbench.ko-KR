---
description: 데이터 워크벤치는 검색 및 정렬 작업에 정규 표현식(regex)을 사용합니다.
solution: Analytics
title: 정규 표현식
topic: Data workbench
uuid: dc8c1e88-4d95-4011-8a38-70fae0c5cf6d
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Regular expressions{#regular-expressions}

데이터 워크벤치는 검색 및 정렬 작업에 정규 표현식(regex)을 사용합니다.

필드 내에서 일반적인 표현식을 사용하여 &quot;re:&quot; 문 다음에 검색을 수행할 수 있습니다. 예를 들면 다음과 같습니다. **[!UICONTROL Search]**

```
<b>re: *.s</b>
```

<table id="table_BA125AB039794EE382B33003BE4E0AFB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 메타문자 </th> 
   <th colname="col2" class="entry"> description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>. (점) </p> </td> 
   <td colname="col2"> <p>예를 들어 단일 문자와 일치합니다.re: <span class="filepath"> x.z는 "xyz" 또는 "xxz"와 </span> 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>* (별) </p> </td> 
   <td colname="col2"> <p>하나 이상의 문자와 일치합니다(예:re: <span class="filepath"> Z* </span> 는 "ZZZ"와 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? (와일드카드) </p> </td> 
   <td colname="col2"> <p>이전 식의 0 또는 1과 일치하여 최소값 일치를 적용합니다(예:xy?z <span class="filepath"> </span> 는 "xy" 및 "xyz"와 일치합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

추가적인 일반 표현식을 사용하여 보다 복잡한 검색 문자열을 만들 수도 있습니다. 정규 표현식은 쿼리 엔티티 패널을 포함한 모든 데이터 워크벤치 검색 필드에서 사용됩니다.

자세한 내용은 [일반 표현식을](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-dataset-constr.html#Regular_Expressions)참조하십시오.
