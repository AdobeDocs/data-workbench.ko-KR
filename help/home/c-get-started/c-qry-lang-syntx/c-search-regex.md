---
description: Data Workbench는 검색 및 정렬 작업에 정규 표현식(regex)을 사용합니다.
title: 정규 표현식
uuid: dc8c1e88-4d95-4011-8a38-70fae0c5cf6d
exl-id: bb1be6d8-3b7a-47e4-bb29-4a65de99666b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# 정규 표현식{#regular-expressions}

Data Workbench는 검색 및 정렬 작업에 정규 표현식(regex)을 사용합니다.

**[!UICONTROL Search]** 필드 내에서 일반적인 표현식을 사용하여 &quot;re:&quot; 문 다음에 오는 검색을 수행할 수 있습니다.

```
<b>re: *.s</b>
```

<table id="table_BA125AB039794EE382B33003BE4E0AFB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 메타문자 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>. (점) </p> </td> 
   <td colname="col2"> <p>단일 문자와 일치하는 예:<span class="filepath"> re:x.z </span>은 "xyz" 또는 "xxz"와 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>* (별) </p> </td> 
   <td colname="col2"> <p>하나 이상의 문자와 일치(예:<span class="filepath"> re:Z* </span>이 "ZZZ"와 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? (와일드카드) </p> </td> 
   <td colname="col2"> <p>최소 일치를 강제 적용하기 위해 이전 표현식의 0 또는 1과 일치합니다. 예:<span class="filepath"> xy?z </span>은 "xy" 및 "xyz"와 일치합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

추가적인 일반적인 정규 표현식을 사용하여 더 복잡한 검색 문자열을 만들 수도 있습니다. 정규 표현식은 쿼리 엔티티 패널을 포함하여 모든 Data Workbench 검색 필드에서 사용됩니다.

[정규 표현식](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-dataset-constr.html#Regular_Expressions)에서 심층적인 정보를 참조하십시오.
