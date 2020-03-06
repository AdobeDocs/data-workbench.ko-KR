---
description: 분할 변환은 문자열을 지정된 구분 기호를 기준으로 하위 문자열의 벡터로 분할합니다.
solution: Analytics
title: 분할
topic: Data workbench
uuid: 116e8465-8fb1-41eb-9a28-412cee54ab87
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Split{#split}

분할 변환은 문자열을 지정된 구분 기호를 기준으로 하위 문자열의 벡터로 분할합니다.

[!DNL Split] 은 단일 URI 쿼리 이름 값과 연결된 값 컬렉션에서 개별 값을 추출하는 데 특히 유용합니다.

<table id="table_C97DA4E45DA844FAB8D61AABA22FF809"> 
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
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> 선택 사항입니다. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구분 기호 </td> 
   <td colname="col2"> <p>입력 문자열을 하위 문자열로 구분하는 데 사용되는 문자열입니다. 길이는 단일 문자여야 합니다. </p> <p> Ctrl 키를 누른 채로 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 삽입 메뉴가 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 출력 문자열 벡터를 만들기 위해 값을 분할하는 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 출력 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

구매 성공과 연관된 확인 페이지에 액세스할 때 고객이 구매한 제품이 cs-uri-query 값의 일부로 나열되는 웹 사이트를 고려해 보십시오. 다음은 이러한 문자열의 예입니다.

* /checkout/confirmed.asp?prod_selected=B57481,C46355,Z97123

cs-uri-stem 필드는 로그 항목에서 요청할 페이지가 확인 페이지인지 여부를 확인하는 데 사용됩니다. 고객이 구입한 제품의 코드는 cs-uri-query에서 prod_selected 이름의 쉼표로 구분된 값으로 나열됩니다. 변환은 [!DNL Split] cs-uri-stem 값이 조건에 지정된 값과 일치하는 경우 제품 코드를 쉼표로 구분하여 이 정보를 추출하는 데 사용할 수 [!DNL String Match] 있습니다. 문자열 [일치를 참조하십시오](../../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-f8d132085c6b4500bfbe4515b848142f). 다음 변환은 이 문제의 해결 방법을 자세히 설명합니다.

![](assets/cfg_TransformationType_Split.png)

여기서 출력 필드는 x-products로, 구매한 제품을 구매가 이루어진 세션에 매핑하는 원하는 확장 차원을 만드는 데 사용됩니다.
