---
description: 숫자 차원은 순차적인 숫자 요소로 구성되며 상위 계산 가능한 차원과 일대다 관계를 갖습니다.
solution: Analytics
title: 숫자 차원
topic: Data workbench
uuid: 19fab770-1535-41b2-bad1-811eba5f3575
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 숫자 차원{#numeric-dimensions}

숫자 차원은 순차적인 숫자 요소로 구성되며 상위 계산 가능한 차원과 일대다 관계를 갖습니다.

숫자 차원을 상위 차원 요소의 숫자 속성의 표현으로 생각할 수 있습니다. 예를 들어, 웹 데이터를 사용하여 작업하는 경우 세션 차원의 각 세션에 대한 매출액을 달러 단위로 정의하는 숫자 차원 세션 매출을 정의할 수 있습니다. 각 세션은 관련된 매출액을 한 번만 가지지만 여러 세션은 동일한 양의 관련 매출을 가질 수 있습니다. 따라서 세션 매출 차원은 세션 차원과 일대다 관계를 갖습니다.

숫자 차원은 종종 값을 합하거나, 조건의 발생 수를 계산하거나, 최소 또는 최대 값을 찾는 지표를 정의하는 데 사용됩니다. 예를 들어 &quot;매출액&quot;이라는 지표는 세션 매출 차원을 사용하여 정의할 수 있습니다.sum(Session_Revenue, Session). 이렇게 정의하면 매출액 지표가 선택한 세션의 총 매출 금액을 제공합니다.

숫자 차원은 다른 차원의 상위 차원이 될 수 없습니다.

숫자 차원은 다음 매개 변수로 정의됩니다.

<table id="table_15B849DD0BFC4D57AD6CF28898901324"> 
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
   <td colname="col2"> 데이터 워크벤치에서 나타나는 차원의 설명 이름입니다. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 클립 값 </td> 
   <td colname="col2"> 참 또는 거짓 [작업 후] 입력 값을 [최소]와 [최대] 값 사이에서 클리핑할지 여부를 지정합니다. [클립 값]이 true이면 값이 해당 범위로 잘립니다. [클립 값]이 false이면 상위 차원의 요소에 대해 값이 반환되지 않습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 입력 필드가 숫자 차원 생성에 기여하는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 고정 크기 </td> 
   <td colname="col2"> 참 또는 거짓 차원의 요소 수(기수)를 제어합니다. true이면 최소에서 최대까지 모든 요소가 차원에 포함됩니다. false이면 값이 추가되면 차원의 크기가 커집니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 데이터 워크벤치 인터페이스에 차원이 나타나는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되는 경우 이 매개 변수를 true로 설정하여 데이터 워크벤치 디스플레이에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <p>지정된 작업 또는 발생 횟수를 카운트할 입력 값과 함께 사용할 값입니다. </p> <p> 이 필드가 문자열 벡터인 경우 벡터의 각 요소에 대해 평가가 수행됩니다. 예를 들어 길이가 3인 벡터와 카운트 작업이 카운트에 3을 추가합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소 </td> 
   <td colname="col2"> 최종 차원 결과에 대한 하한. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최대 </td> 
   <td colname="col2"> 최종 차원 결과의 상한입니다. </td> 
   <td colname="col3"> 1e6 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오프셋 </td> 
   <td colname="col2"> 이 표의 비율을 참조하십시오. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>사용 가능한 작업은 다음과 같습니다. </p> <p> 
     <ul id="ul_E04733E5E8824A2BAAB90D9356078D99"> 
      <li id="li_CAEE9167D45540BEAC538345F250B509"> 카운트:차원의 조건을 충족하는 모든 로그 항목에 대한 <span class="wintitle"> 입력</span> 필드에 비어 있지 않은 값의 총 수가 사용됩니다. 입력 <span class="wintitle"> 필드가</span> 벡터 필드인 경우 각 로그 항목의 비어 있지 않은 값의 총 수가 계산됩니다. </li> 
      <li id="li_64A4D671E78642BD9A9334F8098450B9"> 비어 있지 않은 첫 번째 항목:비어 있지 않은 첫 번째 입력 값이 첫 번째 로그 항목에서 오는지에 관계없이 사용됩니다. [ <span class="wintitle"> 입력</span> ]이 벡터 필드인 경우 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 값이 숫자가 아닌 경우 값이 사용되지 않습니다. </li> 
      <li id="li_C967964729BD4A638FF78D8883CE513F"> 첫 번째 행:상위 차원 요소와 관련된 첫 번째 로그 항목의 값이 사용됩니다(입력이 비어 있는 경우에도). [ <span class="wintitle"> 입력</span> ]이 벡터 필드인 경우 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아닌 경우 또는 관련 로그 항목이 차원의 조건을 충족하지 않는 경우 값이 사용되지 않습니다. </li> 
      <li id="li_74171B17F480478B8547E1A361B22DA4"> 마지막 비어 있지 않음:마지막 로그 항목에서 오는지에 관계없이 비어 있지 않은 마지막 입력 값이 사용됩니다. [ <span class="wintitle"> 입력</span> ]이 벡터 필드인 경우 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 값이 숫자가 아닌 경우 값이 사용되지 않습니다. </li> 
      <li id="li_1253ECF507BD4BBF97CBB2FA12915045"> 마지막 행:상위 차원 요소와 관련된 마지막 로그 항목의 값이 사용됩니다(입력이 비어 있는 경우에도). [ <span class="wintitle"> 입력</span> ]이 벡터 필드인 경우 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아닌 경우 또는 관련 로그 항목이 차원의 조건을 충족하지 않는 경우 값이 사용되지 않습니다. </li> 
      <li id="li_20819E3944544F98853D6A02814F47B2"> 합계:차원의 조건을 충족하는 모든 로그 항목에 대한 <span class="wintitle"> 입력</span> 필드의 모든 숫자 값의 합계가 사용됩니다. 로그 항목이 없거나 숫자 값이 없는 경우 숫자 값 0이 사용됩니다. </li> 
      <li id="li_086C2E57604B4645A9203A984C6F9A04">최소 또는 최대:차원의 조건을 충족하는 모든 로그 항목에서 <span class="wintitle"> 입력</span> 필드에 있는 최소 또는 최대 숫자 값이 사용됩니다. 로그 항목이 없거나 숫자 값이 없는 경우 값이 사용되지 않습니다. </li> 
     </ul> </p> <p> <p>참고: 차원이 의도된 대로 정의되도록 작업을 지정해야 합니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 계산 가능한 차원은 상위 차원일 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비율 조정 </td> 
   <td colname="col2"> <p>차원의 서수 값을 산출하기 위해 공정 결과는 다음과 같이 변형됩니다. </p> <p> (크기 조절 * 입력) + 오프셋 </p> </td> 
   <td colname="col3"> 1.0 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>값을 [!DNL Operation] 반환하지 않거나 [!DNL Clip Values] false인 경우 값이 와 사이에 있지 않은 [!DNL Min] [!DNL Max]경우, 숫자 차원의 요소는 상위 차원의 요소와 관련되지 않습니다.

이 예에서는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 숫자 차원의 정의를 보여 줍니다. &quot;광고 보기 카운터&quot;라는 이 숫자 차원은 지정된 세션 동안 방문자가 광고를 본 횟수를 카운트합니다. 모든 광고 리소스는 cs-uri-query의 일부로 ad=가 있는 웹 서버에서 요청된다고 가정합니다. 이 예에서는 방문자에게 광고되는 횟수(COUNT)가 필드의 실제 값이 아닌 관심 값입니다.

![](assets/cfg_Transformation_Dim_Numeric.png)
