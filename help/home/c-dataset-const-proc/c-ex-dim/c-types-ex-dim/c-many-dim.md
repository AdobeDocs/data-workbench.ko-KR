---
description: 다대다 차원은 상위 계산 가능한 차원과 다대다 관계를 갖습니다.
title: 다대다 차원
uuid: 42c909e8-1228-4210-9406-ffc0d92372fa
exl-id: 02d1a21c-a5b4-4b58-8089-9b9c68a7b1d1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 3%

---

# 다대다 차원{#many-to-many-dimensions}

다대다 차원은 상위 계산 가능한 차원과 다대다 관계를 갖습니다.

다대다 차원을 상위 차원의 각 요소에 대한 값 집합의 표시로 생각할 수 있습니다. 예를 들어 다대다 차원 검색 구문은 세션 수준 차원(세션의 상위 차원)입니다. 세션 차원의 각 세션과 연관된 검색 구문 세트를 나타냅니다. 단일 검색 구문은 세션 수에 관계없이 사용할 수 있으며, 단일 세션은 0개 이상의 검색 구문을 포함할 수 있습니다. 따라서 검색 구문 차원은 세션 차원과 다대다 관계를 갖습니다.

다대다 차원은 다음 매개 변수로 정의됩니다.

<table id="table_A6D495008DFF4DD28A3ECD718D775E54"> 
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
   <td colname="col2"> Data Workbench에서 사용자에게 표시되는 차원의 수사적 이름입니다. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원에 대한 참고 사항 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 상위 및 입력 필드의 값 간의 관계를 만들어야 하는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 차원이 Data Workbench 인터페이스에 표시되는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되는 경우 이 매개 변수를 true로 설정하여 Data Workbench 표시에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>상위 차원(상위)과 관련된 값입니다. 이 필드가 문자열 벡터이면 벡터의 각 요소는 상위와 자체 관계를 갖습니다. </p> <p> <p>참고: 상위 차원의 요소에 대한 모든 로그 항목에 대한 입력 값이 비어 있으면 다대다 차원의 요소가 상위 차원의 해당 요소와 관련되지 않습니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 가산 차원은 상위 차원일 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 다대다 차원의 정의를 보여줍니다. &quot;선택된 제품&quot;이라는 다대다 차원은 해당 세션 중에 방문자가 구입한 제품에 대한 세션을 제공합니다. x-products 필드에는 값 벡터가 포함되어 있으며, 이 벡터는 각각 페이지 보기와 연결되어 있고, 결과적으로 페이지와 연결됩니다.

![](assets/cfg_Transformation_Dim_ManytoMany.png)

이러한 변형을 작성함으로써 선택한 제품 차원과 각 제품과 관련된 세션 수의 관계를 나타내는 시각화를 Data Workbench에서 만들 수 있습니다.
