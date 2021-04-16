---
description: Dimension 표현식은 단독으로 사용되지 않지만, 지표나 필터 표현식에서 차원이 호출되는 모든 곳에서 사용할 수 있습니다.
title: 차원 표현식의 구문
uuid: c437cc52-4eb3-4202-a0b4-e23889f9c8a2
exl-id: 58609e31-8ad8-418b-9a9f-40462d6443f7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1855'
ht-degree: 0%

---

# 차원 표현식의 구문{#syntax-for-dimension-expressions}

Dimension 표현식은 단독으로 사용되지 않지만, 지표나 필터 표현식에서 차원이 호출되는 모든 곳에서 사용할 수 있습니다.

1. 밑줄 친 단어는 문자 그대로 표현식 텍스트에 입력해야 합니다.
1. `{TEXT}?` 형식은 선택적 텍스트를 나타냅니다.
1. `{TEXT}*` 형식은 0회 이상 발생할 수 있는 텍스트를 나타냅니다.
1. `{A | B | C |...}` 형식은 A 또는 B 또는 C... 같은 주어진 옵션 중 하나로 구성되는 텍스트를 나타냅니다..
1. `[A,B)` 형식은 A부터 B까지는 포함되지 않지만 A까지의 숫자 범위를 나타냅니다.

<table id="table_2D9AE1E2397843C284E838330370A1EE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>식별자는 명명된 차원을 참조합니다. 법적 식별자를 제어하는 규칙에 대해서는 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> 식별자 구문 </a>을 참조하십시오. </p> <p>예:Sessions[ Session_Number = "1" ] 은 세션 번호가 "1"인 세션의 수입니다. 세션 번호는 식별자가 참조하는 명명된 차원입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(차원) </p> </td> 
   <td colname="col2"> <p>(Dimension) 결과는 Dimension의 결과와 동일합니다. 괄호는 표현식에서 작업 순서를 지정합니다. </p> <p>예:Sessions[(페이지) = "/home" ] 은 "/home" 페이지를 방문하는 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레벨별 흐림 </p> </td> 
   <td colname="col2"> <p>치수 치수(Dim) 측정값과 요소가 같지만 치수 레벨을 통해 다른 차원과 관련된 치수를 정의합니다. </p> <p>특히, 새 차원의 요소는 Dim의 동일한 요소와 동일한 레벨 요소와 관련되며 해당 레벨 요소와 관련된 다른 차원의 요소와 관련됩니다. </p> <p>예:Sessions[(방문자별 페이지)="/home" ] 은 "/home" 페이지를 방문한 방문자의 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>shift(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>치수 치수(Dim)와 동일한 요소를 갖는 치수를 정의합니다. 레벨 9와 e+Nth 요소가 차원 그룹의 동일한 요소와 관련될 경우, 차원 레벨의 1 및 e+Nth 요소와 관련된 e+Nth 요소와 새 차원의 동일한 요소와 관련됩니다. </p> <p>예:Page_Views[ shift(Page, Page_View, Session, 1)="/home" ] 는 동일한 세션에서 본 다음 페이지가 "/home"인 페이지 보기 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>next(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>shift(Dim,Level,Group,N)과 유사하지만 치수에 빈 값이 있는 경우에는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>segment(level {,String-&gt;Filter}*) </p> </td> 
   <td colname="col2"> <p> 필터 목록을 기반으로 수준의 요소를 분류하는 차원을 정의합니다. 새 차원의 요소는 인수로 제공되는 문자열입니다. 수준의 각 요소는 필터가 수준의 요소를 허용하는 세그먼트 차원의 1차 요소와 관련됩니다. 세그먼트 시각화와 유사합니다. </p> <p>예:segment(방문자, "1회 방문자" -&gt; Visitor_Sessions = 1, "매우 충성스러운 방문자" -&gt; Visitor_Sessions &gt; 10, "Everyone Else" -&gt; True)는 방문자를 3개의 그룹으로 분류하는 차원을 만듭니다. 1회 방문자는 한 세션만, 매우 충성스러운 방문자는 10개 이상의 세션 및 다른 모든 방문자입니다 방문자의 값은 "다른 모든 사람"입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bucket(Level, Metric, Count, Format {, Start {, Size}? }?) </p> </td> 
   <td colname="col2"> <p>요소가 숫자 범위(예: [0-9], [10-19],..)인 차원을 정의합니다. 레벨 요소는 해당 레벨 요소에 대한 지표 값이 범위에 포함된 버킷 딤의 요소와 관련됩니다. 형식은 지표 요소의 형식을 지정하는 데 사용되는 printf 형식 문자열입니다. </p> <p>예:Page_Duration_Minutes가 각 페이지에서 보낸 시간(분)을 나타내는 페이지 보기 수준 차원일 경우 버킷(Session, sum(Page_Duration_Minutes, Page_View), 100, "%0.0f minutes", 0, 5)은 각 세션에서 사용된 시간 수를 나타내는 세션 수준 차원입니다.해당 요소는 <code>{[0-5), [5-10),...,[495-500)}</code>의 5분 간격입니다. </p> <p>시작 값은 첫 번째 간격의 시작 값입니다(기본값:0) 및 크기는 간격의 크기입니다(기본값:1). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prefix(Level {,ElementName-&gt;(Prefix{,Prefix}* )}* ) </p> </td> 
   <td colname="col2"> <p>주어진 ElementName 문자열이며 해당 Prefix 문자열 세트와 연결된 요소를 갖는 차원을 정의합니다. 레벨 요소는 지정된 레벨 요소의 이름에 대응되는 가장 긴 접두어와 연관된 접두사 dim 요소와 관련됩니다. 특수 문자 '$'으로 끝나는 접두사는 정확하게 일치해야 합니다. </p> <p>예를 들어 접두사(URI, "제품" -&gt; ("/products/"), "서비스" -&gt; ("/services/", "/products/service/"), "Warranties" -&gt; ("/products/warranty.html$", "/services/warranty.html$", "모든 것" -&gt; ("/"))는 URI를 나열된 4개의 카테고리로 분류하는 차원을 만듭니다. 다양한 페이지에 미치는 효과는 다음과 같습니다. </p> <p>/products/warranty.html이(가) 정확히 /products/warranty.html$ 접두사와 일치하기 때문에 보증으로 이동합니다. </p> <p>/products/cars/specialcar.html은 /products/ 접두사와 일치하고 더 이상 접두어가 없으므로 제품에 포함됩니다. </p> <p>/products/service/something.html은 /products/접두어보다 긴 /products/service/ 접두사와 일치하기 때문에 서비스로 이동합니다. </p> <p>/companyinfo/aboutus.html이 일치하는 유일한 접두어는 "/"이므로 "Everything Else" 범주로 이동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지연(레벨, 클립, 흐림, 필터, MaxBefore, MaxAfter, FormatString) </p> </td> 
   <td colname="col2"> <p><a href="../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/t-create-ltncy-dims.md#task-6d46ea8c89a047318d9c71bf105ef64a"> 지연 Dimension 만들기 </a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cartesian_product(구분 문자 {,Dim}*) </p> </td> 
   <td colname="col2"> <p>주어진 차원 요소의 모든 조합("직교 제품")을 갖는 차원을 정의합니다. 각 요소의 이름은 입력 차원에 있는 해당 요소의 연결로 지정된 구분 문자 문자열로 구분되어 만들어집니다. </p> <p>예를 들어 차원 D1에 요소 {"a", "b"}가 있고 차원 D2에 요소 {"x", "y"}가 있는 경우, 카르티시안 product("-", D1, D2)에는 {"a-x", "a-y", "b-x", "b-y"} 요소가 있습니다. </p> <p>내부적으로 각 입력 치수는 요소의 수가 다음으로 높은 2의 거듭제곱인 것처럼 처리됩니다. 이 결과는 카티시안 제품에 어떤 더미 요소가 있는 것입니다. Data Workbench API를 사용할 때 출력 형식에 따라 이러한 요소가 생략되거나 "#nnn"으로 표시될 수 있습니다. 여기서 nnn은 요소의 서수입니다(클라이언트에서 무시해야 함). </p> <p>예를 들어 위의 예에서 D2에 3개의 요소 {"x", "y", "z"}가 있으면 4개의 요소가 있는 것처럼 취급되고, 직사 제품은 {"a-x", "a-y", "a-z", "#3", "b-x", "b-y", "b-z", "#7"} 요소가 있습니다. </p> <p>차원을 지정하지 않으면 "#0"라는 요소가 한 차원이 되며 이 차원은 없음 차원에 해당합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nearest_countable(Dim) </p> </td> 
   <td colname="col2"> <p>이미 기존 차원을 참조합니다.스키마에서 가장 가까운 계산 가능한 Dim 상위 항목. 예를 들어 가장 가까운 계산 가능(URI)은 Page_View와 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>normalized(Dim,Count) </p> </td> 
   <td colname="col2"> <p>최대 카운트 요소와 함께 비정상 치수 딤에서 정규화된 치수를 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>last_n(Dim, TimeMetric, FormatString, Count, Offset, TrimToData {, WeekStart}?) </p> </td> 
   <td colname="col2"> <p>요소가 시간(예: 일, 주 또는 연도)을 나타내는 차원 Dim의 요소 하위 세트가 있는 차원을 정의합니다. </p> <p>하위 집합은 지정된 시간의 범위(1970년 1월 1일 자정 이후 시간 값(초)으로 해석되는 상수 지표 TimeMetric의 값입니다. 범위에는 카운트 요소가 있으며, 그 마지막은 지정된 FormatString 문자열을 사용하여 지표의 값을 서식을 지정한 결과 이름이 지정된 Dim 요소 뒤에 있는 오프셋 요소입니다. FormatString은 표준 C 라이브러리 함수 스트플라이트와 동일한 % 이스케이프를 사용합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 [흐림]을 시작하기 전에 모든 요소가 제거됩니다. false이면 항상 개수로 지정된 요소의 정확한 수가 있습니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>선택 사항인 WeekStart는 { "Sun", "Mon", "Tue", "Weed", "Thu", "Fri", "Sat" } 중 하나여야 합니다. 이 값은 해당 요일의 가장 최근 항목으로 뒤로 이동하여 TimeMetric을 수정합니다. </p> <p>예:주에 요소 { "10/03/10", "10/10/10", ..., "12/12/10" }가 있고 내장 기준 지표에 값 1292348109(2010년 12월 14일 중간 시간을 표시)이 있는 경우, 마지막 n(주, As_Of, "%m/%d/%y", 4, 0, false, "Sun")이 차원을 정의합니다. 를 사용할 수 있습니다. </p> <p>예 2:Week 차원에 {"12/19/10", "12/26/10", ..., "01/30/11"} 요소만 있고 As Of 지표가 위와 같은 경우, 마지막 n(주, As_Of, "%m/%d/%y", 4, 0, true, "Sun")은 {"12/19/10", "12/23/10", "12/30/10"} 요소가 있는 차원을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_previous_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>요소가 날짜를 나타내는 흐림 요소의 하위 세트가 있는 차원을 정의합니다. 하위 집합은 지정된 시간의 범위(1970년 1월 1일 자정 이후 시간 값(초)으로 해석되는 상수 지표 TimeMetric의 값입니다. 범위에는 지정된 시간 이전 월의 각 달에 해당하는 요소가 포함됩니다. includeThisMonth가 true인 경우 해당 범위의 각 날이 지정된 시간을 포함하고 있습니다. </p> <p>FormatString은 표준 C 라이브러리 함수 스트림에서와 같이 "%"를 이스케이프하여 흐림 요소의 서식을 지정합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 [흐림]을 시작하기 전에 모든 요소가 제거됩니다. false이면 항상 개수로 지정된 요소의 정확한 수가 있습니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:Day에 { "01/01/10", "01/02/10", ..., "12/31/10" } 요소가 있고 내장된 기준 지표에 1292348109(2010년 12월 14일 중간 시간을 표시) 값이 있는 경우 이전 개월(일, As_Of, "%m/%d/%y", 2, false, false)의 요소 { "10/01/10 ", "10/02/10", .., "11/30/10" }. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_current_month(Dim, TimeMetric, FormatString, allMonth, trimToData) </p> </td> 
   <td colname="col2"> <p>요소는 시간 지표에 의해 지정된 시간과 같은 달의 일수에만 해당된다는 점을 제외하고 이전 월의 일과 유사합니다. allMonth가 true이면 해당 월의 각 날에 대한 요소가 있습니다.그렇지 않은 경우 해당 월의 첫 번째 달부터 지정된 시간이 포함된 날까지의 날만 차원의 일부가 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_future_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>해당 요소가 시간 지표에 의해 지정된 시간을 포함하는 달을 포함하는 달이 아닌, 그 이후의 일 수에 해당한다는 점을 제외하고 이전 월의 일과 유사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hours_of_day(Dim, Metric, TimeFormatString, nDaysForward, TrimData) </p> </td> 
   <td colname="col2"> <p>요소가 시간을 나타내는 흐림 요소의 하위 세트가 있는 차원을 정의합니다. 하위 집합은 지정된 시간의 범위(1970년 1월 1일 자정 이후 시간 값(초)으로 해석되는 상수 지표 TimeMetric의 값입니다. 범위에는 TimeMetric에 의해 지정된 시간이 포함된 날의 다음 날 nDaysForward의 각 시간에 해당하는 요소가 포함됩니다. </p> <p>FormatString은 표준 C 라이브러리 함수 스트림에서와 같이 "%"를 이스케이프하여 흐림 요소의 서식을 지정합니다. 형식 문자열은 항상 전달된 시간의 시작 부분에 자정을 나타내는 문자열을 출력해야 합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 [흐림]을 시작하기 전에 모든 요소가 제거됩니다. false이면 항상 개수로 지정된 요소의 정확한 수가 있습니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:[시간]에 { "01/01/10 00:00", "01/01/10 01:00", .., "12/31/10 23:00" } 요소가 있고 내장 [기준] 지표에 1292348109(2010년 12월 14일 중간 시간) 시간(시간, As_Of, "%의 x 00:00", 0, false)에는 { "12/12/10 00:00", "12/12/10 001:00", ..., "12/12/10 23:00" } 요소가 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
