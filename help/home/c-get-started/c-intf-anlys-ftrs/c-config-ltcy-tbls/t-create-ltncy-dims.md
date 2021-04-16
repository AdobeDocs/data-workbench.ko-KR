---
description: '지연 차원은 세션 등의 상위 계산 가능한 차원과 시간 차원(예: 일)에서 구성됩니다.'
title: 지연 차원 만들기
uuid: 531d8bf6-a66f-4b02-9d81-05664fb9c988
exl-id: 38b470ef-9409-455b-b2b8-b0391f80b800
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 2%

---

# 지연 차원 만들기{#create-a-latency-dimension}

지연 차원은 세션 등의 상위 계산 가능한 차원과 시간 차원(예: 일)에서 구성됩니다.

Data Workbench에서 지연 테이블을 만들면 시각화 파일(.vw)에 지연 차원을 자동으로 추가합니다. 아래 단계를 수행하여 테이블의 지연 차원을 편집할 수 있습니다.

**지연 차원을 편집하려면**

1. 메모장과 같은 텍스트 편집기에서 만든 지연 표를 엽니다. Data Workbench 설치 디렉토리 내의 사용자 > `working profile name` > 작업 폴더에 있습니다.

   정의된 지연 차원은 다음 예제에 표시된 매개 변수를 포함합니다. 지연 차원의 정의에는 추가 매개 변수가 포함될 수 있습니다. [!DNL line entity = LatencyDim:]은 지연 차원 정의의 시작을 나타냅니다.

   ```
   entity = LatencyDim:
   Name = string: dimension name
   Level = ref: wdata/model/dim/level
   Clip = ref: wdata/model/dim/clip
   Time = ref: wdata/model/dim/time dimension
   Format = printf_format: 
   format = string: %+0.0f time string
   offset = double: offset
   Time Before = int: time before
   Time After = int: time after
   ```

1. 다음 표를 안내서로 사용하여 이름, 레벨, 클립, 시간, 형식, 이전 시간 또는 이후 시간 매개 변수의 값을 편집합니다.

   <table id="table_13DF30B8B7314F118D0ED5DF9EA70B9B"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> 이 매개 변수의 경우.. </th> 
      <th colname="col2" class="entry"> 이 정보 제공... </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>이름 </p> </td> 
      <td colname="col2"> <p>선택 사항입니다. 차원 레이블이나 요소를 마우스 오른쪽 단추로 클릭하면 컨텍스트 메뉴에 나타나는 지연 차원의 이름입니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>레벨 </p> </td> 
      <td colname="col2"> <p>지연 차원의 상위 차원인 계산 가능한 차원입니다. 이러한 예로는 세션, 방문자 및 페이지 보기가 있습니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>클립 </p> </td> 
      <td colname="col2"> <p>지연 차원 수준과 일대다 관계가 있는 계산 가능한 차원입니다. 지연은 이 차원의 경계를 넘어 계산되지 않습니다. 예를 들어 페이지 보기 수준 및 세션 클립을 지정하는 경우 이벤트와 동일한 세션 동안 발생한 페이지 보기에 대해 지연 시간이 계산됩니다. </p> <p>일대다(단순) 차원에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>시간 </p> </td> 
      <td colname="col2"> <p>지연 차원에 대한 경과 시간을 측정하는 데 사용되는 차원입니다. 이 차원은 일 또는 시간과 같은 시간 차원이거나 방문자, 세션 또는 페이지 보기와 같은 계산 가능한 차원일 수 있습니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> 형식 </td> 
      <td colname="col2"> <p>선택 사항입니다. Data Workbench에서 지연 시각화의 모양을 지정합니다. Format 매개 변수 내에서 다음 값을 편집할 수 있습니다. 
      <ul id="ul_ABF4C17BDE2E4F6C9CBDD933674DE861"> 
         <li id="li_5ED6A7267C81444983AF8507ADC6A5AB">시간 문자열. 지연 시각화에 표시되는 시간 단위(예: 일 또는 주). 시간 차원을 변경할 때는 시간 문자열을 변경해야 합니다. </li> 
         <li id="li_E3B517ECE1494221AAE90455CC0AAB42">오프셋. 이전 시간 값의 음수와 같은 정수입니다. 예를 들어 이전 시간이 7이면 오프셋이 -7이어야 합니다. </li> 
      </ul> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>이전 시간 </p> </td> 
      <td colname="col2"> <p>지연이 계산되는 이벤트가 계산되기 전의 최대 시간(시간 차원 단위로 표시됨) 이 값이 0으로 설정되거나 전혀 설정되지 않은 경우 지연은 전방 방향에만 계산됩니다. </p> <p>이 값을 변경할 경우 Format 매개 변수에서 오프셋 값을 변경해야 합니다.오프셋은 이전 시간 값의 음수입니다. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>이후 시간 </p> </td> 
      <td colname="col2"> <p>지연이 계산되는 이벤트 이후의 최대 시간(시간 차원 단위로 표시됨) </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. [!DNL .vw] 파일을 User\*working profile name*\Work 폴더에 저장합니다.

   기본 지연 차원에 대한 설정은 다음과 같습니다.

   ```
   entity = LatencyDim:
   Name = string: 
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Day
   Time Before = int: 7
   Time After = int: 7
   ```

   다음 대기 시간 차원에서는 각 세션 이벤트의 지연이 시간 단위로 계산되고 이전 시간은 0으로 설정됩니다. 따라서 지연은 정의된 이벤트 후 24시간 이내에 발생한 세션에만 계산됩니다.

   ```
   entity = LatencyDim:
   Name = string:
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Hour
   Time Before = int: 0
   Time After = int: 24
   ```
