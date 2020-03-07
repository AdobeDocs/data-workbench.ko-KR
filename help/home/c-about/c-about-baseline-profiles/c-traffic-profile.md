---
description: 트래픽 프로필에는 방문자 트래픽을 식별하는 다음 지표가 포함되어 있습니다.
solution: Analytics
title: 트래픽 프로필 지표
topic: Data workbench
uuid: 7dfa18ef-d2cd-44ae-8c56-a0630a9d5cf2
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 트래픽 프로필 지표{#traffic-profile-metrics}

트래픽 프로필에는 방문자 트래픽을 식별하는 다음 지표가 포함되어 있습니다.

<table id="table_D981FB9F8B734E3C845A9628548565F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 지표 </th> 
   <th colname="col2" class="entry"> 지표 공식 및 레벨 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 항목 </td> 
   <td colname="col2">공식:Page_ <span class="filepath"> Views[no shift(None,Page_View, Session,-1)]</span><p>수준:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트에 들어온 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 비율 </td> 
   <td colname="col2">공식:Exits/ <span class="filepath"> Page_Views </span><p>수준:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션의 비율입니다. 종료 비율 지표는 페이지 차원에서만 평가할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 </td> 
   <td colname="col2">공식:<span class="filepath"> Page_Views[no shift(None,Page_View, Session,1)] </span><p>수준:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LVCI90 </td> 
   <td colname="col2">공식: <span class="filepath"> (원시(방문자) - ((원시(방문자) + .69)^0.5 * 1.281551 - 1.2269)))*(방문자 수/원시(방문자)))</span><p>수준:방문자 </p></td> 
   <td colname="col3"> Insight가 보고한 가능한 가장 낮은 방문자 수의 측정값입니다. 수학적으로, 90% 확률을 가진 가장 낮은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 기간 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 합계(exact_page_duration, page_view)*0.1/Page_Views[any Exact_Page_Duration]</span></p> <p>수준:페이지 보기 </p> </td> 
   <td colname="col3"> 특정 페이지 또는 페이지 그룹에서 보낸 평균 시간(MM:SS)입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션당 페이지 보기 횟수 </td> 
   <td colname="col2"> <p>공식:Page_ <span class="filepath"> Views/(Page_View별 세션) </span></p> <p>수준:세션 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 각 세션의 평균 페이지 보기 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 수 </td> 
   <td colname="col2">공식: <span class="filepath"> 합계(One, Page_View)</span><p>수준:페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기 수입니다. 페이지 보기는 정의된 페이지에 대한 요청입니다(이미지 및 기타 유형의 필터링된 컨텐츠에 대한 액세스는 카운트되지 않음). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 횟수 </td> 
   <td colname="col2">공식:Page_ <span class="filepath"> Views/total(Page_Views) </span><p>수준:페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct of Sessions </td> 
   <td colname="col2">공식:세션 <span class="filepath"> 수/총 수(세션)</span><p>수준:세션 </p></td> 
   <td colname="col3"> 세션의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 수 </td> 
   <td colname="col2">공식:방문자 수/총 수(방문자 수) <span class="filepath"></span><p>수준:방문자 </p></td> 
   <td colname="col3"> 방문자의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 직송 참조 방문자 </td> 
   <td colname="col2"> <p>공식:Referred_Visitors/Visitors </p> <p>수준:방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조 세션 </td> 
   <td colname="col2"> <p>공식:세션 <span class="filepath"> [레퍼러&lt;&gt; '없음' 및 레퍼러&lt;&gt;'책갈피']</span></p> <p>수준:세션 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조된 방문자 </td> 
   <td colname="col2"> <p>공식:방문자[ <span class="filepath"> 방문자_ 레퍼러&lt;&gt;'없음' 및 Visitor_Referrer&lt;&gt;'책갈피']</span></p> <p>수준:방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유지 </td> 
   <td colname="col2"> <p>공식:세션 <span class="filepath"> [shift(None,Ses,Session,Visitor,1) = ""] / 세션</span></p> <p>수준:세션 </p> </td> 
   <td colname="col3"> 방문자가 마지막 세션이 아닌 세션의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 기간 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> (sum (Exact_Page_Duration, Session)*.1/Sessions)[Session_ Duration &lt;= '01:00:00']</span></p> <p>수준:세션 </p> </td> 
   <td colname="col3">방문자가 세션에서 보내는 평균 시간(MM:SS). <p><p>참고:세그먼트 내보내기 기능과 함께 이 지표를 사용할 <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Segment_Export" format="http" scope="external"> 수</a> 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기별 세션 </td> 
   <td colname="col2"> <p>공식:Page_ <span class="filepath"> View별 세션</span></p> <p> 수준:세션 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 합계(하나, 세션)</span></p> <p>수준:세션 </p> </td> 
   <td colname="col3"> 방문자 세션 수. 세션은 웹 사이트의 한 방문자에 대한 활동 기간입니다. 각 방문자에 대한 개별 세션은 쿠키, 시간 초과 및 기타 추론을 사용하여 식별됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SCI80 </td> 
   <td colname="col2"> <p>공식:신뢰도(세션) * 1.281551 / 세션 <span class="filepath"></span></p> <p>수준:방문자 </p> </td> 
   <td colname="col3"> 데이터 워크벤치에서 보고한 세션 지표의 신뢰도 측정 수학적으로, 실제 대답이 80%가 될 범위를 지정하는 +/- 백분율입니다. SCI80 퍼센트를 두 배로 늘리면 99%의 실제 답이 나올 수 있는 범위를 갖게 됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UVCI90 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> ((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) + 원시(방문자))*( 방문자 수/원시(방문자 수)))</span></p> <p>수준:방문자 </p> </td> 
   <td colname="col3"> Insight가 보고한 가능한 최대 방문자 수 측정값입니다. 수학적으로 90% 확률을 가진 가장 높은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VCI80 </td> 
   <td colname="col2">공식: <span class="filepath"> ((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) / 원시(방문자)</span><p>수준:방문자 </p></td> 
   <td colname="col3"> Insight가 보고한 방문자 지표의 신뢰도 측정 수학적으로, 실제 대답이 80%가 될 범위를 지정하는 +/- 백분율입니다. 경험상 VCI80%의 두 배치는 99%의 실제 응답 범위를 제공합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기별 방문자 수 </td> 
   <td colname="col2"> <p>공식:페이지별 <span class="filepath"> 방문자 수_보기</span></p> <p>수준:페이지 보기 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션별 방문자 수 </td> 
   <td colname="col2"> <p>공식:세션별 <span class="filepath"> 방문자 수 </span></p> <p>수준:세션 </p> </td> 
   <td colname="col3"> 세션이 있는 방문자 수입니다. </td> 
  </tr> 
 </tbody> 
</table>

