---
description: 차원 표현식은 단독으로 사용되지는 않지만 지표나 필터 표현식에서 차원이 호출되는 모든 곳에서 사용할 수 있습니다.
solution: Analytics
title: 차원 표현식의 구문
topic: Data workbench
uuid: c437cc52-4eb3-4202-a0b4-e23889f9c8a2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 차원 표현식의 구문{#syntax-for-dimension-expressions}

차원 표현식은 단독으로 사용되지는 않지만 지표나 필터 표현식에서 차원이 호출되는 모든 곳에서 사용할 수 있습니다.

1. 밑줄 친 단어는 문자 그대로 표현식 텍스트에 입력해야 합니다.
1. {TEXT} 양식입니까? 은 선택적 텍스트를 나타냅니다.
1. {TEXT}* 형식은 0회 이상 발생할 수 있는 텍스트를 나타냅니다.
1. 양식 {A| B| C|...}은 A, B 또는 C와 같은 지정된 옵션 중 하나로 구성된 텍스트를 나타냅니다..
1. 양식 [A,B)은 A부터 B까지 숫자 범위를 나타냅니다.

<table id="table_2D9AE1E2397843C284E838330370A1EE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>식별자는 명명된 차원을 참조합니다. 법적 식별자를 제어하는 규칙에 대해서는 식별자에 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> 대한 구문을 참조하십시오 </a>. </p> <p>예:Sessions[ Session_Number = "1" ] 은 세션 번호가 "1"인 세션의 수입니다. 세션 번호는 식별자가 참조하는 명명된 차원입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(차원) </p> </td> 
   <td colname="col2"> <p>(차원)의 결과는 차원의 결과와 동일합니다. 괄호는 표현식에서 작업 순서를 지정합니다. </p> <p>예:Sessions[(페이지) = "/home" ] 은 페이지 "/home"을 방문하는 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수준별 흐림 </p> </td> 
   <td colname="col2"> <p>치수 치수(Dim) 및 치수 레벨(Dimension Level)을 통해 다른 차원과 관련된 요소를 갖는 차원을 정의합니다. </p> <p>특히, 새 차원의 요소는 dim의 동일한 요소와 동일한 레벨 요소와 관련되며, 해당 레벨의 요소와 관련된 다른 차원의 요소와 관련됩니다. </p> <p>예:Sessions[(방문자별 페이지)="/home"]은 페이지 "/home"을 방문한 방문자 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>shift(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>치수(Dim) 치수와 동일한 요소를 갖는 치수를 정의합니다. 차원의 두 번째 요소는 레벨의 e+Nth 요소와 관련된 Dim의 요소와 새 차원의 동일한 요소와 관련이 있습니다. 단, 차원의 두 번째 및 e+Nth 요소는 차원 그룹의 동일한 요소와 관련됩니다. </p> <p>예:Page_Views[ shift(Page, Page_View, Session, 1)="/home" ] 는 동일한 세션에서 본 다음 페이지가 "/home"인 페이지 보기 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>next(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>shift(Dim,Level,Group,N)와 유사하지만 차원에 빈 값이 있으면 건너뜁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>segment(Level {,String-&gt;Filter}*) </p> </td> 
   <td colname="col2"> <p> 필터 목록을 기반으로 수준의 요소를 분류하는 차원을 정의합니다. 새 차원의 요소는 인수로 지정된 문자열입니다. 수준의 각 요소는 필터가 수준 요소를 허용하는 세그먼트 차원의 첫 번째 요소와 관련됩니다. 세그먼트 시각화와 유사합니다. </p> <p>예:segment(방문자, "일회성 방문자" -&gt; Visitor_Sessions = 1, "매우 단골 방문자" -&gt; Visitor_Sessions &gt; 10, "Everyone Else" -&gt; True)는 방문자를 세 그룹으로 분류하는 차원을 만듭니다. 1회 방문자는 한 세션만 있는 방문자이고, 매우 충성스러운 방문자는 10개 이상의 세션 및 기타 모든 그룹으로 구분됩니다. 방문자의 값은 "Everyone Else"입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bucket(Level, Metric, Count, Format {, Start {, Size}? }?) </p> </td> 
   <td colname="col2"> <p>요소가 숫자 범위(예: [0-9], [10-19],..)인 차원을 정의합니다. 레벨 요소는 해당 레벨 요소에 대한 지표 값을 포함하는 버킷 딤의 요소와 관련됩니다. 형식은 지표 요소의 형식을 지정하는 데 사용되는 printf 형식 문자열입니다. </p> <p>예:Page_Duration_Minutes가 각 페이지에서 보낸 시간(분)을 나타내는 페이지 보기 수준 차원인 경우 bucket(Session, sum(Page_Duration_Minutes, Page_View), 100, "%0.0f minutes", 0, 5)은 각 세션에서 소요된 시간(분)을 나타내는 세션 수준 차원입니다.요소는 5분 간격 {[0-5), [5-10),...,[495-500)}. </p> <p>Start는 첫 번째 간격의 시작 값입니다(기본값:0) 및 크기는 간격의 크기입니다(기본값:1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prefix(Level {,ElementName-&gt;(Prefix{,Prefix}* )}* ) </p> </td> 
   <td colname="col2"> <p>주어진 ElementName 문자열이며 해당 Prefix 문자열 세트와 연결된 요소가 있는 차원을 정의합니다. [레벨]의 요소는 지정된 레벨 요소의 이름으로 일치하는 가장 긴 접두사와 연결된 접두사 dim의 요소와 관련됩니다. 특수 문자 '$'로 끝나는 접두사는 정확히 일치해야 합니다. </p> <p>예를 들어 접두사(URI, "Products" -&gt; ("/products/"), "Services" -&gt; ("/services/", "/products/service/"), "Warranties" -&gt; ("/products/warranty.html$", "/services/warranty.html$", "Everything Else" -&gt; ("/")는 URI를 나열된 네 개의 카테고리로 분류하는 차원을 만듭니다. 다양한 페이지에 미치는 영향은 다음과 같습니다. </p> <p>/products/warranty.html은 /products/warranty.html$ 접두사와 정확히 일치하므로 보증에 포함됩니다. </p> <p>/products/cars/specialcar.html이 /products/ 접두사와 일치하고 더 이상 접두사가 없으므로 Products로 이동합니다. </p> <p>/products/service/something.html은 /products/ 접두사보다 긴 /products/service/ 접두사와 일치하기 때문에 서비스로 이동합니다. </p> <p>/companyinfo/aboutus.html이 일치하는 유일한 접두사는 "/"이므로 "Everything Else" 카테고리로 이동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지연(Level, Clip, Dim, Filter, MaxBefore, MaxAfter, FormatString) </p> </td> 
   <td colname="col2"> <p>지연 <a href="../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/t-create-ltncy-dims.md#task-6d46ea8c89a047318d9c71bf105ef64a"> 차원 생성을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cartesian_product(구분 문자 {,Dim}*) </p> </td> 
   <td colname="col2"> <p>주어진 차원 요소의 모든 조합("카티시안 제품")을 포함하는 차원을 정의합니다. 각 요소의 이름은 입력 차원에 있는 해당 요소의 연결로 지정된 구분 문자로 구분됩니다. </p> <p>예를 들어 차원 D1에 {"a", "b"} 요소가 있고 차원 D2에 {"x", "y"} 요소가 있는 경우, 카티시안 product("-", D1, D2)에는 {"a-x", "a-y", "b-x", "b-y"} 요소가 있습니다. </p> <p>내부적으로 각 입력 차원은 요소의 수가 다음으로 높은 2의 거듭제곱 같이 처리됩니다. 이로 인해 카티시안 제품에 더미 요소가 있습니다. 데이터 워크벤치 API를 사용할 때 출력 형식에 따라 이러한 요소가 생략되거나 "#nnn"으로 표시될 수 있습니다. 여기서 nnn은 요소의 서수입니다(그리고 클라이언트는 무시해야 함). </p> <p>예를 들어 위의 예에서 D2에 세 개의 요소 {"x", "y", "z"}가 있는 경우, 4개의 요소가 있는 것처럼 취급되고, 카티시안 제품은 {"a-x", "a-y", "a-z", "#3", "b-x", "b-y", "b-z", "#7"} 요소가 있습니다. </p> <p>차원을 지정하지 않으면 "없음" 차원과 같은 요소가 "#0"인 차원이 생성됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nearly_countable(Dim) </p> </td> 
   <td colname="col2"> <p>이미 기존 차원을 참조합니다.스키마에서 가장 가까운 계산 가능한 Dim 상위 항목. 예를 들어 가장 가까운 countable(URI)은 Page_View와 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>normalized(Dim,Count) </p> </td> 
   <td colname="col2"> <p>최대 카운트 요소와 함께 비정상 치수 Dim에서 정규화된 치수를 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>last_n(Dim, TimeMetric, FormatString, Count, Offset, TrimToData {, WeekStart}?) </p> </td> 
   <td colname="col2"> <p>요소가 시간(예: 일, 주 또는 년)을 나타내는 차원 Dim의 요소 하위 집합을 갖는 차원을 정의합니다. </p> <p>하위 세트는 지정된 시간 주위의 범위이며, 상수 지표 TimeMetric의 값입니다. 이 값은 1970년 1월 1일 자정 이후 초 단위의 시간 값으로 해석됩니다. 범위에는 카운트 요소가 있으며, 그 중 마지막은 주어진 FormatString 문자열로 지표 값의 서식을 지정한 결과 이름인 주어진 Dim 요소 뒤에 있는 오프셋 요소입니다. FormatString은 표준 C 라이브러리 함수 스트플라이트와 동일한 % 이스케이프를 사용합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 모든 요소가 제거됩니다(흐림 시작 전). false이면 항상 카운트에 의해 지정된 요소의 정확한 수가 있게 됩니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>선택 사항인 WeekStart는 { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" } 중 하나여야 합니다. TimeMetric을 해당 요일의 가장 최근 항목으로 뒤로 이동하여 수정합니다. </p> <p>예:주에 { "10/03/10", "10/10/10", ..., "12/12/10" } 요소가 있고 기본 제공 기준 지표의 값은 1292348109입니다(12월 14일 중간의 시간 표시). 2010), 그 다음 마지막 n(주, As_Of, "%m/%d/%y", 4, 0, false, "Sun")은 요소 { "12/12/12/10", "12/19/10", "12/23/3" 0/10" }. </p> <p>예 2:주 차원에 {"12/19/10", "12/26/10", ..., "01/30/11"} 요소만 있고 기준 지표가 위와 같은 경우 마지막 n(주, As_Of, "%m/%d/%y", 4, 0, true, "Sun")은 {"12/19/10", "12/23/10", "12/30/10"} 요소가 있는 차원을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_previous_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>Dim 요소의 하위 세트가 있는 차원을 정의합니다. 요소의 하위 세트는 일을 나타냅니다. 하위 세트는 지정된 시간 주위의 범위이며, 상수 지표 TimeMetric의 값입니다. 이 값은 1970년 1월 1일 자정 이후 초 단위의 시간 값으로 해석됩니다. 범위에는 지정된 시간 이전 개월 동안 각 날짜에 해당하는 요소가 포함됩니다. includeThisMonth가 true인 경우 범위에 지정된 시간이 들어 있는 매일이 포함됩니다. </p> <p>FormatString은 표준 C 라이브러리 함수 스트림에서와 같이 "%"를 사용하여 치수 요소의 서식을 지정합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 모든 요소가 제거됩니다(흐림 시작 전). false이면 항상 카운트에 의해 지정된 요소의 정확한 수가 있게 됩니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:Day에 { "01/01/10", "01/02/10", ..., "12/31/10" } 요소가 있고 기본 제공 As Of 지표의 값은 1292348109입니다(12월 14일 중간의 시간 표시). 2010), 그 다음 이전 달의 날(일, As_Of, "%m/%d/%y", 2, false, false)에는 { "10/01/10", "10/02/10", ..., "11/30/10" } 요소가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_current_month(Dim, TimeMetric, FormatString, allMonth, trimToData) </p> </td> 
   <td colname="col2"> <p>요소는 시간 지표에 의해 지정된 시간과 같은 월의 일에만 해당한다는 점을 제외하고 이전 월의 일수와 유사합니다. allMonth가 참이면 해당 월의 각 날에 대한 요소가 있습니다.그렇지 않은 경우, 해당 월의 첫 번째 달에서 지정된 시간이 들어 있는 날까지의 날만 차원의 일부가 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_future_months(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>요소는 시간 지표에 의해 지정된 시간을 포함하는 월을 포함하는 달이 아닌 그 후의 개월 수에 해당한다는 점을 제외하고 이전 월의 일과 유사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hours_of_day(Dim, Metric, TimeFormatString, nDaysForward, TrimData) </p> </td> 
   <td colname="col2"> <p>요소가 시간을 나타내는 dim 요소의 하위 세트가 있는 차원을 정의합니다. 하위 세트는 지정된 시간 주위의 범위이며, 상수 지표 TimeMetric의 값입니다. 이 값은 1970년 1월 1일 자정 이후 초 단위의 시간 값으로 해석됩니다. 범위에는 TimeMetric에 의해 지정된 시간이 포함된 일 이후 일 중 각 시간에 해당하는 요소가 포함됩니다. </p> <p>FormatString은 표준 C 라이브러리 함수 스트림에서와 같이 "%"를 사용하여 치수 요소의 서식을 지정합니다. 형식 문자열은 항상 전달된 시간의 시작 부분에 자정을 나타내는 문자열을 출력해야 합니다. </p> <p>trimToData가 true이면 결과 치수의 시작 부분에 있는 모든 요소가 제거됩니다(흐림 시작 전). false이면 항상 카운트에 의해 지정된 요소의 정확한 수가 있게 됩니다. 결과 치수의 끝에 실제로 딤에 없는 요소가 항상 있을 수 있습니다. </p> <p>예:[시간]에 { "01/01/100:00", "01/01/10 01:00", ..., "12/31/10 23:00" } 요소가 있고 기본 제공 [기준] 지표의 값은 129234 2010년 12월 14일 중간의 시간 표시)와 시간(시간(시간, As_Of, "%x00:00", 0, false)에 요소 { "12/12/100:00", "12/12/12/10 1:00", ..., "12/12/10 23:00" }. </p> </td> 
  </tr> 
 </tbody> 
</table>

