---
description: 단순 차원은 상위 가산 차원과 일대다 관계를 갖습니다.
title: 단순 차원
uuid: 3bca2354-02c4-4739-a7da-acccdb0efdfd
exl-id: 2acad750-7c48-40f1-8130-ab056ac8bf0d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 1%

---

# 단순 차원{#simple-dimensions}

단순 차원은 상위 가산 차원과 일대다 관계를 갖습니다.

단순 차원은 항상 가산 차원의 하위 차원입니다. 단순 차원을 상위 차원에 있는 요소의 속성 표현으로 생각할 수 있습니다. 예를 들어, 웹 데이터를 사용하여 작업하는 경우 방문자의 상위 차원이 있는 간단한 차원인 방문자 레퍼러 차원을 정의할 수 있습니다. 방문자 차원의 각 방문자에 대한 첫 번째 HTTP 레퍼러를 나타냅니다. 방문자 차원의 각 방문자에는 방문자 레퍼러가 하나만 있지만 많은 방문자에게 동일한 방문자 레퍼러가 있을 수 있습니다. 따라서 방문자 레퍼러 차원은 방문자 차원과 일대다 관계를 갖습니다.

단순 차원은 다음 매개 변수로 정의됩니다.

<table id="table_E6F729DFA226459DBFC1776CE8CB81F8"> 
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
   <td colname="col2"> Data Workbench에 표시되는 차원의 수사적 이름입니다. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
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
   <td colname="col2"> 상위 차원(상위)과 관련된 값 필드입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 로드 </td> 
   <td colname="col2"> <p>선택 사항입니다. 관계에 사용할 수 있는 값 파일입니다. 다음 중 하나가 적용되는 경우 로드 파일을 사용합니다. </p> <p> 
     <ul id="ul_056C4A8E46AA479397DC63173C035D5C"> 
      <li id="li_C26EB5A4AB3C4BEB8EB3A217A5A2377E"> 값에는 Data Workbench 표시에 유지할 특정 정렬 순서가 있습니다. 예를 들어 요소(연도 분기)가 항상 시간 순서대로 표시되는 분기 차원을 만들 수 있습니다. </li> 
      <li id="li_5D4DF56BC6124D038A7260131B1F3DB3"> 데이터에서 찾을 수 없지만 Data Workbench 디스플레이에 표시되어야 하는 값에 대한 자리 표시자를 만들려고 합니다. </li> 
     </ul> </p> <p> 파일에 없는 값이 발견되면 Data Workbench에서 볼 때 값의 끝에 추가됩니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>사용 가능한 작업은 다음과 같습니다. </p> <p> 
     <ul id="ul_88AE4279413C42609D8B53EC64B5E913"> 
      <li id="li_DD9623D006844BC28B2AAA8E12AA04E1"> 첫 번째 비어 있지 않음:첫 번째 로그 항목에서 오는지에 관계없이 첫 번째 비공백 입력 값이 사용됩니다. 입력(Input)이 벡터 필드인 경우 관련 로그 항목의 벡터에 있는 첫 번째 행이 사용됩니다. </li> 
      <li id="li_0FBE7F0B7B9744D994ECEDAA08F0045C"> 첫 번째 행:입력이 비어 있어도 상위 차원 요소와 관련된 첫 번째 로그 항목의 값이 사용됩니다. 입력(Input)이 벡터 필드인 경우 관련 로그 항목의 벡터에 있는 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아니거나 관련 로그 항목이 차원의 조건을 충족하지 않는 경우 값이 사용되지 않습니다. </li> 
      <li id="li_C17190BC699D4A099DC5326C07D1044D"> 마지막 비공백:마지막 로그 항목에서 오는지에 관계없이 마지막으로 비공백 입력 값이 사용됩니다. 입력(Input)이 벡터 필드인 경우 관련 로그 항목의 벡터에 있는 첫 번째 행이 사용됩니다. </li> 
      <li id="li_00BAE86F12004C098F6A455908DB7062"> 마지막 행:입력이 비어 있어도 상위 차원 요소와 관련된 마지막 로그 항목의 값이 사용됩니다. 입력(Input)이 벡터 필드인 경우 관련 로그 항목의 벡터에 있는 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아니거나 관련 로그 항목이 차원의 조건을 충족하지 않는 경우 값이 사용되지 않습니다. </li> 
     </ul> </p> <p> <p>참고: 특정 로그 항목에 대한 값 또는 빈 값을 산출하지 않은 경우 상위 차원의 해당 요소는 단순 차원의 "없음" 요소와 관련됩니다. </p> </p> <p> 차원이 의도한 대로 정의되도록 작업을 지정해야 합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 가산 차원은 상위 차원일 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제는 웹 사이트 트래픽 및 로드 파일에서 수집한 이벤트 데이터를 사용하여 단순 차원의 정의를 보여줍니다.

사이트 방문자가 좋아하는 Girl Scout 쿠키에 대한 설문 조사의 예를 생각해 보십시오. 웹 페이지는 이 투표를 캡처하여 이름-값 쌍 즐겨찾기로 사용하여 웹 서버에 반환합니다. 방문자당 한 표만 계산되지만, 방문자가 마음을 변경하고 원할 경우 다시 투표할 수 있습니다. 이는 일대다 관계입니다.한 방문자는 많은 표를 사용할 수 있지만 각 표는 한 명의 방문자만 연결됩니다. 따라서 차원의 상위 항목은 방문자 수(방문자당 한 표만) 및 작업은 LAST ROW입니다(마음을 변경하고 다시 투표할 수 있음).

투표를 받는 쿠키 유형이 Data Workbench 표시에 나타나도록 모든 유형의 쿠키에 대한 자리 표시자가 있어야 합니다. 이러한 이유로, 선택할 수 있는 쿠키 유형 목록이 포함된 로드 파일이 정의되었습니다. 이 파일의 내용은 [!DNL cookietypes.txt] 파일에 저장되며 다음과 같습니다.

동물 보물

캐러멜

레몬 페이스트리 크림

땅콩 버터 패티

단빵

얇은 분

최종 차원은 다음과 같이 정의됩니다.

![](assets/cfg_Transformation_Dim_Simple.png)
