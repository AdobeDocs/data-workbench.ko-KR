---
description: '시간 차원을 사용하면 입력 시간(1970년) 매개 변수에 대해 지정한 타임스탬프 필드를 기반으로 주기적 또는 절대 로컬 시간 차원 집합(예: 일, 요일, 시간, 예약 시간 등)을 생성할 수 있습니다.'
title: 시간 차원
uuid: b633cf4f-0db4-4378-9e59-43b6ad8f772d
exl-id: f9534b24-3a16-4220-bac2-bc541e121005
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# 시간 차원{#time-dimensions}

{{eol}}

시간 차원을 사용하면 입력 시간(1970년) 매개 변수에 대해 지정한 타임스탬프 필드를 기반으로 주기적 또는 절대 로컬 시간 차원 집합(예: 일, 요일, 시간, 예약 시간 등)을 생성할 수 있습니다.

시간 측정기준을 정의할 때 주 시작 요일 매개 변수를 지정하여 한 주의 시작으로 월요일 대신 다른 요일을 선택할 수도 있습니다. 차원에 다른 이름이 있는 한 데이터 세트에 두 개 이상의 시간 차원 세트를 정의할 수 있습니다.

시간 차원은 다음 매개 변수로 정의됩니다.

<table id="table_9734F6CD7ABA4661A2F9A5FB948A7282"> 
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
   <td colname="col2"> 선택 사항. 확장 차원에 대한 참고 사항 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2"> <p>다음 기간에 대해 차원 이름을 지정할 수 있습니다. </p> <p> 
     <ul id="ul_EB0837DD66BE4004A615A6029EEF4CD5"> 
      <li id="li_2E46E6DB004E443C8CC831DCEE743D60"> 일 </li> 
      <li id="li_F59A27779EBE4E2A84E0972EE8BCDFA7"> 요일 </li> 
      <li id="li_7D74CD547ED1449091EF7B2E0E8C46DE"> 시간 </li> 
      <li id="li_706AF9D385CB44C098DEBACA3BA2CD4B"> 시간 (일 기준) </li> 
      <li id="li_76FBF69B25954885A0192D308A155E41"> 월 </li> 
      <li id="li_3C16955BE5C54291A25E25CD31259661"> 주 </li> 
     </ul> </p> <p> 여기에 입력하는 이름은 차원 메뉴 및 Data Workbench의 시각화에 나타나는 이름입니다. 시간 차원의 이름을 비워 두면 데이터 세트에 차원이 만들어지지 않습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 차원이 Data Workbench 인터페이스에 표시되는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되는 경우 이 매개 변수를 true로 설정하여 Data Workbench 표시에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력시간(1970epoch) </td> 
   <td colname="col2"> <p>입력으로 사용할 타임스탬프 필드의 이름입니다. </p> <p> <p>참고: 필드의 값은 1970년 1월 1일 이후 시간(초)을 00으로 나타내야 합니다:00:01. 입력 시간이 유효한 시간(1970~2037)이 아닌 경우 변환 프로세스가 실패하고 Data Workbench 서버에서 오류가 발생합니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 가산 차원은 상위 차원일 수 있습니다. 웹 데이터의 경우 상위는 세션입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주 시작일 </td> 
   <td colname="col2"> <p>주 중 첫 날로 사용할 요일입니다. </p> <p> 이 매개 변수는 주 차원, 요일 차원 및 주 단위로 정의된 모든 보고 시간 차원에 영향을 줍니다. </p> </td> 
   <td colname="col3"> 월 </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 사용자 정의 입력 필드 x-time-1970을 기반으로 시간 차원 집합을 만듭니다. 시간 차원 세트의 이름은 &quot;세션 시간&quot;입니다. 각 차원의 상위는 세션 차원이므로 시간 차원의 각 요소는 세션이 시작된 시간에 해당합니다. 주 시작 일 매개 변수는 주 차원의 각 주가 월요일에 시작되도록 지정합니다.

![](assets/cfg_Transformation_Dim_TimeDim.png)
