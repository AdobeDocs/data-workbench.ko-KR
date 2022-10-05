---
description: 트래픽 프로필에는 방문자 트래픽을 식별하기 위한 다음 지표가 포함되어 있습니다.
title: 트래픽 프로필 지표
uuid: 7dfa18ef-d2cd-44ae-8c56-a0630a9d5cf2
exl-id: 38f191e5-5b30-4fe0-a680-bcb33fe52eca
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 2%

---

# 트래픽 프로필 지표{#traffic-profile-metrics}

{{eol}}

트래픽 프로필에는 방문자 트래픽을 식별하기 위한 다음 지표가 포함되어 있습니다.

<table id="table_D981FB9F8B734E3C845A9628548565F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 지표 </th> 
   <th colname="col2" class="entry"> 지표 공식 및 수준 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 항목 </td> 
   <td colname="col2">공식: <span class="filepath"> Page_Views[no shift(None,Page_View, Session,-1)]</span><p>수준: 페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트에 입력된 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 비율 </td> 
   <td colname="col2">공식: <span class="filepath"> 종료/Page_Views </span><p>수준: 페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션의 백분율입니다. 종료 비율 지표는 페이지 차원에서만 평가할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 </td> 
   <td colname="col2">공식:<span class="filepath"> Page_Views[no shift(None,Page_View, Session,1)] </span><p>수준: 페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LVCI90 </td> 
   <td colname="col2">공식: <span class="filepath"> (원시(방문자) - ((원시(방문자) + .69)^0.5 * 1.281551 - 1.2269))*(방문자 수/원시(방문자))</span><p>수준: 방문자 </p></td> 
   <td colname="col3"> Insight가 보고한 가능한 가장 낮은 방문자 수의 측정입니다. 수학적으로 90% 확률이 있는 가장 낮은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 기간 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> sum (exact_page_duration, page_view)*0.1/Page_Views[any Exact_Page_Duration]</span></p> <p>수준: 페이지 보기 </p> </td> 
   <td colname="col3"> 특정 페이지 또는 페이지 그룹에서 보낸 평균 시간(MM:SS) 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션당 페이지 보기 수 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> Page_Views/ (Page_View별 세션) </span></p> <p>수준: Session </p> </td> 
   <td colname="col3"> 페이지 보기 수가 있는 각 세션의 평균 페이지 보기 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 조회수 </td> 
   <td colname="col2">공식: <span class="filepath"> sum(One, Page_View)</span><p>수준: 페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기 수. 페이지 보기는 정의된 페이지에 대한 요청입니다. 이미지 및 기타 유형의 필터링된 컨텐츠에 대한 액세스는 계산되지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 수 </td> 
   <td colname="col2">공식: <span class="filepath"> Page_Views/total(Page_Views) </span><p>수준: 페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기 횟수 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 pct </td> 
   <td colname="col2">공식: <span class="filepath"> 세션/총(세션)</span><p>수준: Session </p></td> 
   <td colname="col3"> 세션의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 수 </td> 
   <td colname="col2">공식: <span class="filepath"> 방문자 수/합계(방문자 수) </span><p>수준: 방문자 </p></td> 
   <td colname="col3"> 방문자의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct 참조 방문자 </td> 
   <td colname="col2"> <p>공식: Referring_Visitors/Visitor </p> <p>수준: 방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조 세션 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 세션[레퍼러&lt;&gt; '없음' 및 레퍼러&lt;&gt;'책갈피']</span></p> <p>수준: Session </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조된 방문자 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> Visitor[Visitor_ Referrer&lt;&gt;'None' 및 Visitor_Referrer&lt;&gt;'book marks']</span></p> <p>수준: 방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유지 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 세션[shift(없음,세션,방문자,1) = ""] / 세션</span></p> <p>수준: Session </p> </td> 
   <td colname="col3"> 마지막 세션 방문자가 아닌 세션의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 기간 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> (sum (Exact_Page_Duration, Session)*.1/Sessions)[Session_Duration &lt;= '01:00:00']</span></p> <p>수준: Session </p> </td> 
   <td colname="col3">방문자가 한 세션에서 보내는 평균 시간(MM:SS)입니다. <p><p>참고: 이 지표는 <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Segment_Export" format="http" scope="external"> 세그먼트 내보내기</a> 기능. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기별 세션 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> Page_View별 세션</span></p> <p> 수준: Session </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> sum(One, Session)</span></p> <p>수준: Session </p> </td> 
   <td colname="col3"> 방문자 세션 수입니다. 세션은 웹 사이트 방문자 한 명에 대한 활동 기간입니다. 각 방문자에 대한 개별 세션은 쿠키, 시간 초과 및 기타 추론을 사용하여 식별됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SCI80 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 신뢰도(세션) * 1.281551 / 세션</span></p> <p>수준: 방문자 </p> </td> 
   <td colname="col3"> Data Workbench에서 보고한 세션 지표의 신뢰도 측정입니다. 수학적으로, 실제 응답이 80%가 될 범위를 지정하는 +/- 백분율입니다. SCI80 퍼센트를 두 배로 늘리면 99%의 실제 답을 얻을 수 있는 범위가 될 것입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UVCI90 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> (((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) + 원시(방문자))*( 방문자 수/원시(방문자)))</span></p> <p>수준: 방문자 </p> </td> 
   <td colname="col3"> Insight가 보고한 가능한 가장 높은 방문자 수에 대한 측정입니다. 수학적으로 90% 가능성이 있는 가장 높은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VCI80 </td> 
   <td colname="col2">공식: <span class="filepath"> ((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) / 원시(방문자)</span><p>수준: 방문자 </p></td> 
   <td colname="col3"> Insight에서 보고한 방문자 지표의 신뢰도 측정입니다. 수학적으로, 실제 응답이 80%가 될 범위를 지정하는 +/- 백분율입니다. 경험상, VCI80%를 두 배로 늘리면 실제 응답이 99%가 될 범위를 제공할 것입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기별 방문자 수 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> Page_View별 방문자 수</span></p> <p>수준: 페이지 보기 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션별 방문자 수 </td> 
   <td colname="col2"> <p>공식: <span class="filepath"> 세션별 방문자 수 </span></p> <p>수준: Session </p> </td> 
   <td colname="col3"> 세션을 가진 방문자의 수입니다. </td> 
  </tr> 
 </tbody> 
</table>
