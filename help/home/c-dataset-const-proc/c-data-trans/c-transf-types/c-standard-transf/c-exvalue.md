---
description: 웹 데이터를 사용하여 작업하는 경우 ExtractValue 변환을 사용하여 웹 사이트 데이터의 쿼리 문자열, 쿠키 또는 유사한 인코딩 필드에서 값을 추출할 수 있습니다.
title: 정확한 값
uuid: 305827a2-04e6-421f-82cb-923d62b02e70
exl-id: 5bafe64f-081a-49ec-997e-68e8f6915a71
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 3%

---

# 정확한 값{#extractvalue}

웹 데이터를 사용하여 작업하는 경우 ExtractValue 변환을 사용하여 웹 사이트 데이터의 쿼리 문자열, 쿠키 또는 유사한 인코딩 필드에서 값을 추출할 수 있습니다.

추출할 값에 해당하는 이름은 각 로그 항목마다 다를 수 있습니다.

<table id="table_D16A39BE035043628A4D6F7452952304"> 
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
   <td colname="col1"> 입력 이름 </td> 
   <td colname="col2"> <p>입력 쿼리에서 추출할 필드의 이름입니다. </p> <p> <p>참고: 입력 이름이 벡터인 경우(즉, 여러 이름이 있음) 하나의 값만 추출됩니다. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 쿼리 </td> 
   <td colname="col2"> 값을 추출할 인코딩된 매핑(쿼리 문자열, 쿠키 등)입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 값 </td> 
   <td colname="col2"> 추출된 디코딩된 값을 캡처하는 데 사용되는 필드의 이름입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

검색 구문을 추출하려면 전체 구문을 추출하고 원하는 경우 [!DNL Tokenize] 변형을 사용하여 구문을 검색 용어로 분할할 수 있습니다. [!DNL Tokenize] 변환에 대한 자세한 내용은 [토큰화](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-tokenize.md#concept-f460aa5df3a7476e971af29cf5d9b32c)를 참조하십시오.

이 예에서는 cs(referrer-query)에서 x-v-search-querynames 필드의 값을 추출하고 x-search-phrase 필드에 저장하기 위해 [!DNL ExtractValue] 변환을 구성합니다.

![](assets/cfg_TransformationType_ExtractValue.png)
