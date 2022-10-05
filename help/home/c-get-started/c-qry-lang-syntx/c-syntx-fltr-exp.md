---
description: 필터는 데이터 집합에 있는 데이터의 하위 집합을 정의하는 표현식입니다.
title: 필터 표현식 구문
uuid: faeb6847-3295-48ab-9d1c-db00f57647ba
exl-id: 515c1645-69c8-4990-a913-d2d505c6fe51
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 1%

---

# 필터 표현식 구문{#syntax-for-filter-expressions}

{{eol}}

필터는 데이터 집합에 있는 데이터의 하위 집합을 정의하는 표현식입니다.

필터는 차원 간의 관계에 따라 각 차원의 각 요소를 허용하거나 거부합니다.

필터는 [!DNL Filter Editor]. 자세한 내용은 [필터 편집기](../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).

다음 표에서 각 구문 설명에는 해당 필터를 사용하는 지표 표현식의 예가 포함됩니다. 예: 세션[True] 는 &quot;참&quot; 필터를 사용하여 정의된 지표입니다. 세션[True] 지표는 True 필터가 세션 차원의 모든 요소를 허용하므로 세션 지표와 동일합니다.

<table id="table_5D66E6C11B384460BAAA7A6130214594"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>True </p> </td> 
   <td colname="col2"> <p>상수 필터입니다. 모든 차원의 모든 요소를 허용합니다 </p> <p>예: 세션[ True ] 은 세션과 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False </p> </td> 
   <td colname="col2"> <p>상수 필터입니다. 모든 차원의 모든 요소를 거부합니다. </p> <p>예: 세션[ False ] 은 항상 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필터링하지 않음 </p> </td> 
   <td colname="col2"> <p>필터가 거부하도록 요소를 허용합니다. </p> <p>예: Sessions[ not Page="A" ] 는 페이지 A를 방문하지 않은 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA 및 FilterB </p> </td> 
   <td colname="col2"> <p>FilterA 및 FilterB가 허용하는 요소를 허용합니다. </p> <p>예: Sessions[ Page="A" and Page="B" ] 는 페이지 A와 페이지 B를 모두 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA 또는 FilterB </p> </td> 
   <td colname="col2"> <p>FilterA 또는 FilterB가 허용하는 요소를 허용합니다. </p> <p>예: Sessions[ Page="A" 또는 Page="B" ] 는 페이지 A, 페이지 B 또는 둘 다를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>딤순으로 필터링 </p> </td> 
   <td colname="col2"> <p>필터에 허용되는 차원 Dim의 요소 집합을 허용합니다. </p> <p>예: Sessions[ Page="/home" by Visitor ] 는 "/home" 페이지를 본 방문자에 속하는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>프로필에 다른 방식으로 정의된 참조 필터. </p> <p>예: Sessions[ Broken_Session_Filter ] 는 중단된 세션 필터에 의해 허용되는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim = "Value" </p> </td> 
   <td colname="col2"> <p>차원의 지정된 요소 Dim을 허용합니다. </p> <p>예: Sessions[ Page="A" ] 는 페이지 A를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;&gt; "Value" </p> <p>흐림!= “값” </p> </td> 
   <td colname="col2"> <p>차원의 다른 모든 요소 Dim을 허용합니다. </p> <p>예: Sessions[ Page&lt;&gt;"A" ] 는 A 이외의 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim = #Ordinal </td> 
   <td colname="col2"> <p>주어진 서수 값으로 차원 Dim의 요소를 허용합니다. </p> <p>예: Sessions[ Month=#0 ] 는 데이터 집합의 첫 번째 달에 있는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>치수 &lt;&gt; #Ordinal </p> <p>흐림!= #서수 </p> </td> 
   <td colname="col2"> <p>차원의 다른 모든 요소 Dim을 허용합니다. </p> <p>예: Sessions[ Session_Value &lt;&gt; #0 ] 는 세션 값이 0이 아닌 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim 일치 "Expr" </p> </td> 
   <td colname="col2"> <p>주어진 정규 표현식과 일치하는 차원 요소를 적용합니다. Dim은 비정상 차원이거나 계산 가능한 차원이어야 합니다. </p> <p>예: 세션[ URI가 ".*/product/.*" ] 는 제품 디렉토리의 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim 노트가 "Expr"과 일치합니다. </p> </td> 
   <td colname="col2"> <p>주어진 정규 표현식과 일치하지 않는 Dim 차원의 요소를 허용합니다. Dim은 비정상 차원이거나 계산 가능한 차원이어야 합니다. </p> <p>예: 세션[ URI가 ""과 일치하지 않습니다.*\.jsp" ] 는 JSP 페이지가 아닌 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>치수 &lt; "값" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 작은 서수 값을 갖는 차원 Dim의 요소를 허용합니다. "값"이 차원의 요소가 아니면 차원의 현재 요소보다 큰 것으로 간주됩니다. </p> <p>예: Sessions[ Month &lt; "Jul '04" ] 는 2004년 7월 이전에 발생한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &gt; "Value" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 큰 서수 값을 갖는 차원 Dim의 요소를 허용합니다. "값"이 차원의 요소가 아니면 차원의 현재 요소보다 큰 것으로 간주됩니다. </p> <p>예: Sessions[ Month &gt; "Jul '04" ] 는 2004년 7월 이후에 발생한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>치수 &lt;= "값" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 작거나 같은 서수 값이 있는 Dim 차원의 요소를 허용합니다. "값"이 차원의 요소가 아니면 차원의 현재 요소보다 큰 것으로 간주됩니다. </p> <p>예: Sessions[ Session_Number &lt;= "2" ] 는 방문자의 첫 번째 또는 두 번째 세션이었던 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim &gt;= "Value" </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 크거나 같은 서수 값이 있는 Dim 차원의 요소를 허용합니다. "값"이 차원의 요소가 아니면 차원의 현재 요소보다 큰 것으로 간주됩니다. </p> <p>예: Sessions[ Session_Number &gt;= "5" ] 는 방문자에 대한 다섯 번째 이상의 세션이었던 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모든 치수 </p> </td> 
   <td colname="col2"> <p>차원의 모든 요소 Dim을 허용합니다. </p> <p>예: Sessions[ any Page_View ] 는 하나 이상의 페이지 보기가 있는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>치수 없음 </p> </td> 
   <td colname="col2"> <p>Dim이 거부되는 요소를 허용합니다. </p> <p>예: Sessions[ no Page_View ] 는 페이지 보기가 없는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(필터) </p> </td> 
   <td colname="col2"> <p>필터와 동일함; 필터 표현식의 일부를 그룹화하는 데 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
