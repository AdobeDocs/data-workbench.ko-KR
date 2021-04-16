---
description: 트래픽 프로필에는 방문자 트래픽을 식별하는 다음 지표가 포함되어 있습니다.
title: 트래픽 프로필 지표
uuid: 7dfa18ef-d2cd-44ae-8c56-a0630a9d5cf2
exl-id: 38f191e5-5b30-4fe0-a680-bcb33fe52eca
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---

# 트래픽 프로필 지표{#traffic-profile-metrics}

트래픽 프로필에는 방문자 트래픽을 식별하는 다음 지표가 포함되어 있습니다.

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
   <td colname="col2">공식:<span class="filepath"> Page_Views[no shift(None,Page_View, Session,-1)]</span><p>레벨:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 입력한 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 비율 </td> 
   <td colname="col2">공식:<span class="filepath"> 종료/Page_Views </span><p>레벨:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션의 백분율입니다. 종료 비율 지표는 페이지 차원을 통해서만 평가할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 종료 </td> 
   <td colname="col2">공식:<span class="filepath"> Page_Views[no shift(None,Page_View, Session,1)] </span><p>레벨:페이지 보기 </p></td> 
   <td colname="col3"> 각 페이지에서 사이트를 종료한 세션 수입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LVCI90 </td> 
   <td colname="col2">공식:<span class="filepath"> (원시(방문자 수) - ((원시(방문자 수) + .69)^0.5 * 1.281551 - 1.2269))*(방문자 수/원시(방문자))</span><p>레벨:방문자 </p></td> 
   <td colname="col3"> Insight가 보고한 가능한 가장 낮은 방문자 수의 측정값입니다. 수학적으로 90% 확률을 가진 가장 낮은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 기간 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 합계(exact_page_duration, page_view)*0.1/Page_Views[Exact_Page_Duration]</span></p> <p>레벨:페이지 보기 </p> </td> 
   <td colname="col3"> 특정 페이지 또는 페이지 그룹에서 보낸 평균 시간(MM:SS)입니다. 이 지표는 페이지 차원에서만 평가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션당 페이지 보기 횟수 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> Page_Views/(Page_View별 세션) </span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 각 세션의 평균 페이지 보기 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 수 </td> 
   <td colname="col2">공식:<span class="filepath"> sum(One, Page_View)</span><p>레벨:페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기 횟수. 페이지 보기는 정의된 페이지에 대한 요청입니다(이미지 및 기타 유형의 필터링된 컨텐츠에 대한 액세스는 카운트되지 않음). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지 보기 횟수 </td> 
   <td colname="col2">공식:<span class="filepath"> Page_Views/total(Page_Views) </span><p>레벨:페이지 보기 </p></td> 
   <td colname="col3"> 페이지 보기의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 사진 </td> 
   <td colname="col2">공식:<span class="filepath"> 세션/총(세션)</span><p>레벨:세션 </p></td> 
   <td colname="col3"> 세션의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 수 </td> 
   <td colname="col2">공식:<span class="filepath"> 방문자 수/총(방문자 수) </span><p>레벨:방문자 </p></td> 
   <td colname="col3"> 방문자 비율. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 직책 방문자 </td> 
   <td colname="col2"> <p>공식:Referred_Visitors/Visitors </p> <p>레벨:방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자의 비율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조된 세션 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 세션[레퍼러&lt;&gt; '없음' 및 레퍼러&lt;&gt;'책갈피']</span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 참조된 방문자 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 방문자[Visitor_Referrer&lt;&gt;'None' 및 Visitor_Referrer&lt;&gt;'book marks']</span></p> <p>레벨:방문자 </p> </td> 
   <td colname="col3"> 다른 사이트에서 이 사이트를 참조한 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유지 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 세션[shift(None,Ses, Version,Visitor,1) = ""] / 세션</span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3"> 방문자가 마지막 세션이 아닌 세션의 백분율입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 기간 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> (sum (Exact_Page_Duration, Session)*.1/Sessions)[Session_Duration &lt;= '01:00:00']</span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3">방문자가 세션에서 보내는 평균 시간(MM:SS). <p><p>참고:이 지표는 <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Segment_Export" format="http" scope="external"> 세그먼트 내보내기</a> 기능과 함께 사용할 수 있습니다. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지별 세션 보기 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> Page_View</span>별 세션</p> <p> 레벨:세션 </p> </td> 
   <td colname="col3"> 페이지 보기가 있는 세션 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> sum(하나, 세션)</span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3"> 방문자 세션 수입니다. 세션은 웹 사이트의 한 방문자에 대한 활동 기간입니다. 각 방문자에 대한 개별 세션은 쿠키, 시간 초과 및 기타 추론을 사용하여 식별됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SCI80 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 신뢰(세션) * 1.281551 / 세션</span></p> <p>레벨:방문자 </p> </td> 
   <td colname="col3"> 데이터 워크벤치가 보고한 세션 지표의 신뢰도 측정값입니다. 수학적으로, 실제 대답이 80%가 될 범위를 지정하는 +/- 백분율입니다. SCI80%를 두 배로 증가시키는 것은 99%의 실제 대답이 될 수 있는 범위를 제공할 것이다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UVCI90 </td> 
   <td colname="col2"> <p>공식:<span class="filepath">((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) + 원시(방문자))*( 방문자 수/원시(방문자 수))</span></p> <p>레벨:방문자 </p> </td> 
   <td colname="col3"> Insight가 보고한 가능한 최대 방문자 수 측정값입니다. 수학적으로 90% 확률을 가진 가장 높은 방문자 수를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VCI80 </td> 
   <td colname="col2">공식:<span class="filepath"> ((원시(방문자) + .68)^0.5 * 1.281551 + 1.2269) / 원시(방문자)</span><p>레벨:방문자 </p></td> 
   <td colname="col3"> Insight가 보고한 방문자 지표의 신뢰도 측정값입니다. 수학적으로, 실제 대답이 80%가 될 범위를 지정하는 +/- 백분율입니다. 경험상 VCI80%를 두 배로 증가시키면 실제 답변이 99%가 될 수 있는 범위가 생깁니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 페이지별 방문자 수 보기 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> Page_View</span>별 방문자</p> <p>레벨:페이지 보기 </p> </td> 
   <td colname="col3"> 페이지 보기가 있었던 방문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세션별 방문자 수 </td> 
   <td colname="col2"> <p>공식:<span class="filepath"> 세션별 방문자 </span></p> <p>레벨:세션 </p> </td> 
   <td colname="col3"> 세션이 있는 방문자 수입니다. </td> 
  </tr> 
 </tbody> 
</table>
