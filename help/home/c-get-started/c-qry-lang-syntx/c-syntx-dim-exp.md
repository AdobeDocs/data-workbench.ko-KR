---
description: Dimension 표현식은 단독으로 사용되지 않지만, 지표가 호출되거나 필터 표현식에서 사용될 수 있습니다.
title: 차원 표현식의 구문
uuid: c437cc52-4eb3-4202-a0b4-e23889f9c8a2
exl-id: 58609e31-8ad8-418b-9a9f-40462d6443f7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1855'
ht-degree: 0%

---

# 차원 표현식의 구문{#syntax-for-dimension-expressions}

Dimension 표현식은 단독으로 사용되지 않지만, 지표가 호출되거나 필터 표현식에서 사용될 수 있습니다.

1. 밑줄 친 단어는 문자 그대로 식 텍스트에 입력해야 합니다.
1. `{TEXT}?` 형식은 선택적 텍스트를 나타냅니다.
1. `{TEXT}*` 양식은 0회 이상 발생할 수 있는 텍스트를 나타냅니다.
1. `{A | B | C |...}` 양식은 A 또는 B 또는 C... 등 지정된 옵션 중 하나로 구성된 텍스트를 나타냅니다..
1. `[A,B)` 양식은 A부터 B까지 숫자의 범위를 나타냅니다.

<table id="table_2D9AE1E2397843C284E838330370A1EE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>식별자는 명명된 차원을 참조합니다. 법적 식별자를 관리하는 규칙에 대해서는 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> 식별자 구문 </a>을 참조하십시오. </p> <p>예:Sessions[ Session_Number = "1" ] 는 세션 번호가 "1"인 세션의 수입니다. 세션 번호는 식별자에서 참조하는 명명된 차원입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(차원) </p> </td> 
   <td colname="col2"> <p>(Dimension) 결과는 Dimension 결과와 동일합니다. 괄호는 표현식에서 작업 순서를 지정합니다. </p> <p>예:Sessions[(Page) = "/home" ] 은 "/home" 페이지를 방문하는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수준별 치수 </p> </td> 
   <td colname="col2"> <p>치수(Dim)와 요소가 동일하지만 치수 레벨을 통해 다른 차원과 관련된 치수를 정의합니다. </p> <p>특히, 새 차원의 요소는 치수(Dim)의 동일한 요소와 동일한 레벨의 요소에 관련되며, 이러한 레벨의 요소와 관련된 다른 차원의 요소와 관련됩니다. </p> <p>예:Sessions[(Page by Visitor)="/home" ] 은 "/home" 페이지를 방문한 방문자의 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>shift(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>치수(Dim)와 동일한 요소를 갖는 치수를 정의합니다. 치수 레벨의 1 요소는 레벨(e+Nth) 요소와 관련된 Dim의 요소와 동일한 새 차원의 요소에 관한 것으로서, 레벨 1 및 e+Nth 요소가 차원 그룹의 동일한 요소와 관련되도록 하는 경우, e+Nth 요소가 Level의 e+Nth 요소에 의해 관련된다. </p> <p>예:Page_Views[ shift(Page, Page_View, Session, 1)="/home" ] 는 동일한 세션에서 본 다음 페이지가 "/home"인 페이지 보기 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>next(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>차원에 빈 값이 있는 경우 해당 값을 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>segment(수준 {,String-&gt;필터}*) </p> </td> 
   <td colname="col2"> <p> 필터 목록을 기반으로 레벨의 요소를 분류하는 차원을 정의합니다. 새 차원의 요소는 인수로 제공되는 문자열입니다. 수준의 각 요소는 필터가 수준 요소를 허용하는 세그먼트 차원의 첫 번째 요소에 관한 것입니다. 이는 세그먼트 시각화와 유사합니다. </p> <p>예:세그먼트(방문자, "1회 방문자" -&gt; Visitor_Sessions = 1, "매우 충성스런 방문자" -&gt; Visitor_Sessions &gt; 10, "Everyone Else" -&gt; True)는 방문자를 세 개의 그룹으로 분류하는 차원을 만듭니다. 1회 방문자는 한 개의 세션만 있는 방문자이고, 매우 충성스런 방문자는 10개 이상의 세션을 가진 방문자이고, 다른 모든 방문자는 "Everyone Else" 값을 갖습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bucket(Level, Metric, Count, Format {, Start {, Size}? }?) </p> </td> 
   <td colname="col2"> <p>요소가 숫자 범위(예: [0-9], [10-19],..)인 차원을 정의합니다. 수준 요소는 범위에 해당 수준 요소에 대한 지표 값이 포함된 버킷 딤의 요소와 관련이 있습니다. 형식은 지표 요소의 형식을 지정하는 데 사용되는 인쇄 형식 문자열입니다. </p> <p>예:Page_Duration_Minutes가 각 페이지에서 보낸 분 수를 나타내는 페이지 보기 수준 차원일 경우 bucket(Session, sum(Page_Duration_Minutes, Page_View), 100, "%0.0f minutes", 0, 5)은 각 세션에서 보낸 분 수를 나타내는 세션 수준 차원입니다.이 요소의 요소는 <code>{[0-5), [5-10),...,[495-500)}</code> 5분 간격입니다. </p> <p>Start는 첫 번째 간격의 시작 값입니다(기본값:0)과 Size는 간격의 크기입니다(기본값:1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prefix(Level {,ElementName-&gt;(Prefix{,Prefix}* )}* </p> </td> 
   <td colname="col2"> <p>요소가 지정된 ElementName 문자열이며 해당 Prefix 문자열 세트와 연결된 차원을 정의합니다. 레벨의 요소는 지정된 레벨의 요소 이름에 일치하는 가장 긴 접두어와 연결된 접두사 dim의 요소와 관련됩니다. 특수 문자 '$'로 끝나는 접두사는 정확히 일치해야 합니다. </p> <p>예를 들어 접두어(URI, "Products" -&gt; ("/products/"), "Services" -&gt; ("/services/", "/products/service/"), "Warranties" -&gt; ("/products/warranty.html$", "/services/warranty.html$", "Everything Else" -&gt; ("/")는 URI를 나열된 네 가지 카테고리로 분류하는 차원을 생성합니다. 다양한 페이지에 미치는 영향은 다음과 같습니다. </p> <p>/products/warranty.html 은 /products/warranty.html$ 접두사와 정확히 일치하므로 Warranty에 적용됩니다. </p> <p>/products/cars/specialcar.html 은 /products/ 접두사와 일치하고 더 이상 접두사가 없으므로 Products로 이동합니다 </p> <p>/products/service/something.html 은 /products/prefix보다 긴 /products/service/ 접두사와 일치하므로 Services로 이동합니다. </p> <p>/companyinfo/aboutus.html은 "/"와 일치하는 유일한 접두사이므로 "Everything Else" 카테고리로 이동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지연(Level, Clip, Dim, Filter, MaxBefore, MaxAfter, FormatString) </p> </td> 
   <td colname="col2"> <p><a href="../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/t-create-ltncy-dims.md#task-6d46ea8c89a047318d9c71bf105ef64a"> 지연 Dimension 만들기 </a> 를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cartesian_product(구분 기호 {,Dim}*) </p> </td> 
   <td colname="col2"> <p>제공된 차원 요소의 모든 조합("카티시안 제품")인 차원을 정의합니다. 각 요소의 이름은 입력 차원에서 해당 요소를 연결된 후 지정된 구분 문자 문자열로 구분됩니다. </p> <p>예를 들어 차원 D1에 {"a", "b"} 요소가 있고 차원 D2에 {"x", "y"} 요소가 있는 경우, 카르티시안 product("-", D1, D2)에는 {"a-x", "a-y", "b-x", "b-y"} 요소가 있습니다. </p> <p>내부적으로, 각 입력 차원은 요소 수가 다음으로 높은 2의 힘인 것처럼 처리됩니다. 이것은 몇 가지 더미 요소를 갖는 카티시안 제품을 만듭니다. Data Workbench API를 사용할 때 출력 형식에 따라 이러한 요소가 생략되거나 "#nnn"으로 표시될 수 있습니다. 여기서 nnn은 요소의 서수입니다(클라이언트가 무시해야 함). </p> <p>예를 들어 위의 예에서 D2에 세 개의 요소 {"x", "y", "z"}가 있는 경우, 이는 네 개의 요소가 있는 것처럼 처리되며, 카르티시안 제품은 {"a-x", "a-y", "a-z", "#3", "b-x", "b-y", "b-z", "#7"} 요소가 있습니다. </p> <p>차원이 제공되지 않으면 그 결과는 없음 차원에 해당하는 "#0" 요소가 하나 있는 차원입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nearest_countable(Dim) </p> </td> 
   <td colname="col2"> <p>이미 존재하는 차원을 참조합니다.스키마에서 가장 가까운 계산 가능한 Dim 상위 항목. 예를 들어 가장 가까운 URI(Countable)는 Page_View와 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>normalized(Dim,Count) </p> </td> 
   <td colname="col2"> <p>최대 개수 요소로 비정상 차원(Dim)에서 정규화된 차원을 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>last_n(Dim, TimeMetric, FormatString, Count, Offset, TrimToData {, WeekStart}?) </p> </td> 
   <td colname="col2"> <p>요소가 시간 슬라이스(예: 일, 주 또는 연도)를 나타내는 차원 Dim의 요소 하위 세트가 있는 차원을 정의합니다. </p> <p>하위 집합은 지정된 시간의 범위, 1970년 1월 1일 자정 이후 시간 값으로 해석되는 상수 지표 TimeMetric의 값입니다. 범위에 Count 요소가 있으며 그 중 마지막은 주어진 Dim 요소 뒤에 Offset 요소이며 그 이름은 주어진 FormatString 문자열로 지표 값을 서식을 지정한 결과입니다. FormatString은 표준 C 라이브러리 함수 문자열 시간과 동일한 % 이스케이프를 사용합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분의 요소가 제거되고 치수(Dim)가 시작되기 전입니다. false이면 항상 Count로 지정된 정확한 개수의 요소가 있습니다. 결과 차원의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>선택적인 WeekStart는 { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" } 중 하나여야 합니다. 이 수정 지표는 해당 요일의 가장 최근 발생 항목으로 뒤로 이동하여 TimeMetric을 수정합니다. </p> <p>예:주에 { "10/03/10", "10/10/10", ..., "12/12/10" } 요소가 있고 기본 제공 기준 지표에 1292348109(2010년 12월 14일 중반의 시간을 나타남)이 있는 경우 마지막 n(주, As_Of, "%m/%y", 4, 0, false, "Sun")이 { "12/12/10", "12/19/10", "12/23/10", "12/30/10" } 요소가 있는 차원을 정의합니다. </p> <p>예제 2:주 차원에 {"12/19/10", "12/26/10", ..., "01/30/11"} 요소만 있고 기준 지표가 위와 같은 경우, 마지막 n(주, As_Of, "%m/%d/%y", 4, 0, true, "Sun")은 {"12/19/10", "12/23/10", "12/30/10"} 요소가 있는 차원을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_previous_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>요소가 일을 나타내는 치수(Dim) 요소의 하위 세트가 있는 차원을 정의합니다. 하위 집합은 지정된 시간의 범위, 1970년 1월 1일 자정 이후 시간 값으로 해석되는 상수 지표 TimeMetric의 값입니다. 범위에는 지정된 시간 이전 달의 각 일에 해당하는 요소가 포함됩니다. includeThisMonth가 true인 경우 해당 범위는 지정된 시간이 포함된 월의 각 날도 포함합니다. </p> <p>FormatString은 표준 C 라이브러리 함수 문자열 시간처럼 "%"를 사용하여 Dim 요소의 형식을 지정합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분의 요소가 제거되고 치수(Dim)가 시작되기 전입니다. false이면 항상 Count로 지정된 정확한 개수의 요소가 있습니다. 결과 차원의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:Day에 { "01/01/10", "01/02/10",.., "12/31/10" } 요소가 있고 기본 제공 기준 지표에 1292348109 값(2010년 12월 14일 중간에 시간을 나타남)이 있는 경우 이전 월의 일(일, As_Of, "%m/%d/%y", 2, false, false)에는 { "10/01/10", "10/02/10", ..., "11/30/10" }이 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_current_month(Dim, TimeMetric, FormatString, allMonth, trimToData) </p> </td> 
   <td colname="col2"> <p>요소는 TimeMetric에서 지정한 시간과 같은 달의 일 수에만 해당된다는 점을 제외하면 이전 달의 일 수와 유사합니다. allMonth 가 true일 경우 해당 월의 각 날에 대한 요소가 있습니다.그렇지 않으면 해당 월의 첫 번째 달부터 지정된 시간이 포함된 날까지의 날짜만 차원의 일부가 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_future_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>요소가 TimeMetric에 의해 지정된 시간이 포함된 월을 포함하는 이전 달이 아닌 다음 달 이후의 일에 해당한다는 점을 제외하고, 이전 달의 일 수와 유사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hours_of_day(Dim, Metric, TimeFormatString, nDaysForward, TrimData) </p> </td> 
   <td colname="col2"> <p>요소가 시간을 나타내는 치수(Dim) 요소의 하위 세트가 있는 차원을 정의합니다. 하위 집합은 지정된 시간의 범위, 1970년 1월 1일 자정 이후 시간 값으로 해석되는 상수 지표 TimeMetric의 값입니다. 이 범위에는 TimeMetric에서 지정한 시간을 포함하는 날짜 이후 nDaysForward의 각 시간에 해당하는 요소가 포함됩니다. </p> <p>FormatString은 표준 C 라이브러리 함수 문자열 시간처럼 "%"를 사용하여 Dim 요소의 형식을 지정합니다. 형식 문자열은 항상 전달된 시간 시작 시 자정을 나타내는 문자열을 출력해야 합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분의 요소가 제거되고 치수(Dim)가 시작되기 전입니다. false이면 항상 Count로 지정된 정확한 개수의 요소가 있습니다. 결과 차원의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:Hour에 { "01/01/10 00:00", "01/01/10 01:00", ..., "12/31/10 23:00" } 요소가 있고 기본 제공 As Of 지표에 1292348109 값(2010년 12월 14일 중순 시간 표시)이 있는 경우 시간(시간, As_Of, "%x00:00", 0, false)에는 { "12/12/10 00:00", "12/12/100:000", ":000", "200", "2000", "212/12/10. " } </p> </td> 
  </tr> 
 </tbody> 
</table>
