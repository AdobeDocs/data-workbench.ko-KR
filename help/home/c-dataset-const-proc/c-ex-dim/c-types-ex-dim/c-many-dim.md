---
description: 다대다 차원은 상위 계산 가능한 차원과 다대다 관계를 가집니다.
solution: Analytics
title: 다대다 차원
topic: Data workbench
uuid: 42c909e8-1228-4210-9406-ffc0d92372fa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 다대다 차원{#many-to-many-dimensions}

다대다 차원은 상위 계산 가능한 차원과 다대다 관계를 가집니다.

다대다 차원을 상위 차원의 각 요소에 대한 값 세트의 표현으로 생각할 수 있습니다. 예를 들어 다대다 차원 검색 구문은 세션 수준 차원입니다(세션의 상위가 있음). 세션 차원의 각 세션과 연관된 검색 구문 집합을 나타냅니다. 단일 검색 구문은 세션 수에 관계없이 사용할 수 있으며 단일 세션에는 0개 이상의 검색 구문이 포함될 수 있습니다. 따라서 검색어 차원은 세션 차원과 다대다 관계를 가집니다.

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
   <td colname="col1">  이름  </td> 
   <td colname="col2"> 데이터 워크벤치에서 사용자에게 표시되는 차원의 설명 이름입니다. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 상위와 입력 필드 값 간의 관계를 만들어야 하는 조건. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 데이터 워크벤치 인터페이스에 차원이 나타나는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되는 경우 이 매개 변수를 true로 설정하여 데이터 워크벤치 디스플레이에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>상위 차원(상위)과 관련된 값. 이 필드가 문자열 벡터인 경우 벡터의 각 요소는 상위와 자체 관계를 가집니다. </p> <p> <p>참고: 상위 차원의 요소에 대한 모든 로그 항목에 대한 입력 값이 비어 있으면 다대다 차원의 요소는 상위 차원의 해당 요소와 관련되지 않습니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 계산 가능한 차원은 상위 차원일 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 다대다 차원의 정의를 보여 줍니다. &quot;선택한 제품&quot;이라는 이 다대다 차원은 세션 중에 방문자가 구매한 제품과 세션을 관련시킵니다. x-products 필드에는 값 벡터가 포함되어 있으며, 각각은 페이지 뷰와 연결되어 있고, 이 벡터는 세션과 연결됩니다.

![](assets/cfg_Transformation_Dim_ManytoMany.png)

이러한 변형을 만들어 선택한 제품 차원과 각 제품이 관련된 세션 수 간의 관계를 설명하는 데이터 워크벤치에서 시각화를 만들 수 있습니다.
