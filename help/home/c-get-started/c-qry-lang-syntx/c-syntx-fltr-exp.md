---
description: 필터는 데이터 세트에 있는 데이터의 하위 집합을 정의하는 표현식입니다.
title: 필터 표현식 구문
uuid: faeb6847-3295-48ab-9d1c-db00f57647ba
exl-id: 515c1645-69c8-4990-a913-d2d505c6fe51
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 1%

---

# 필터 표현식 구문{#syntax-for-filter-expressions}

필터는 데이터 세트에 있는 데이터의 하위 집합을 정의하는 표현식입니다.

필터는 차원 사이의 관계에 따라 각 차원의 각 요소를 허용하거나 거부합니다.

필터는 [!DNL Filter Editor]을 사용하여 편집할 수 있습니다. [필터 편집기](../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3)를 참조하십시오.

다음 표에서 각 구문 설명에 해당 필터를 사용하는 지표 표현식의 예가 포함됩니다. 예를 들어 세션[True]은 &quot;True&quot; 필터를 사용하여 정의된 지표입니다. 세션[True] 지표는 True 필터가 세션 차원의 모든 요소를 수용하므로 세션 지표와 동일합니다.

<table id="table_5D66E6C11B384460BAAA7A6130214594"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>True </p> </td> 
   <td colname="col2"> <p>상수 필터입니다. 모든 차원의 모든 요소 허용 </p> <p>예:세션[ True ] 은 세션과 동일합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False </p> </td> 
   <td colname="col2"> <p>상수 필터입니다. 모든 차원의 모든 요소를 거부합니다. </p> <p>예:세션[ False ] 은 항상 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필터가 아님 </p> </td> 
   <td colname="col2"> <p>필터가 거부하는 요소를 허용합니다. </p> <p>예:Sessions[ not Page="A" ] 은 페이지 A를 방문하지 않은 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA 및 FilterB </p> </td> 
   <td colname="col2"> <p>FilterA 및 FilterB가 허용하는 요소를 허용합니다. </p> <p>예:Sessions[ Page="A" and Page="B" ] 는 페이지 A와 페이지 B를 모두 방문한 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA 또는 FilterB </p> </td> 
   <td colname="col2"> <p>FilterA 또는 FilterB가 허용하는 요소를 허용합니다. </p> <p>예:Sessions[ Page="A" 또는 Page="B" ] 는 페이지 A, 페이지 B 또는 둘 다를 방문한 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐리게 필터링 </p> </td> 
   <td colname="col2"> <p>필터에서 허용하는 차원 Dim의 요소 집합을 허용합니다. </p> <p>예:Sessions[ Page="/home" by Visitor]은 페이지 "/home"을(를) 본 방문자에 속하는 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>프로필에 별도로 정의된 참조 필터입니다. </p> <p>예:Sessions[ Broken_Session_Filter ] 는 끊어진 세션 필터로 허용된 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim = "Value" </p> </td> 
   <td colname="col2"> <p>차원의 주어진 요소를 Dim에 적용합니다. </p> <p>예:Sessions[ Page="A" ] 은 페이지 A를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 &lt;&gt; "값" </p> <p>흐림!= “값” </p> </td> 
   <td colname="col2"> <p>차원의 다른 모든 요소 Dim을 적용합니다. </p> <p>예:Sessions[ Page&lt;&gt;"A" ] 는 A 이외의 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 흐림 = #Ordinal </td> 
   <td colname="col2"> <p>주어진 서수 값으로 치수 요소를 적용합니다. </p> <p>예:Sessions[ Month=#0 ] 은 데이터 세트의 첫 번째 달에 있는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 &lt;&gt; #Ordinal </p> <p>흐림!= #서수 </p> </td> 
   <td colname="col2"> <p>차원의 다른 모든 요소 Dim을 적용합니다. </p> <p>예:Sessions[ Session_Value &lt;&gt; #0 ] 은 세션 값이 0이 아닌 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 일치 "내보내기" </p> </td> 
   <td colname="col2"> <p>주어진 정규 표현식과 일치하는 치수 요소를 적용합니다. Dim은 비정상 치수나 계산 가능한 치수가 아니어야 합니다. </p> <p>예:세션[ URI가 ""과(와) 일치합니다.*/product/.*" ] 는 제품 디렉토리의 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 노트가 "내보내기"와 일치 </p> </td> 
   <td colname="col2"> <p>주어진 정규 표현식과 일치하지 않는 치수 요소를 적용합니다. Dim은 비정상 치수나 계산 가능한 치수가 아니어야 합니다. </p> <p>예:세션[ URI가 ""과(와) 일치하지 않습니다.*\.jsp" ] 는 JSP 페이지가 아닌 페이지를 방문한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 &lt; "Value" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 적은 서수 값을 사용하여 차원 Dim의 요소를 적용합니다. "값"이 차원의 요소가 아닌 경우 차원의 현재 요소보다 크다고 가정합니다. </p> <p>예:Sessions[ Month &lt; "Jul '04" ] 는 2004년 7월 이전에 발생한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 &gt; "값" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 큰 서수 값을 사용하여 차원 Dim의 요소를 적용합니다. "값"이 차원의 요소가 아닌 경우 차원의 현재 요소보다 크다고 가정합니다. </p> <p>예:Sessions[ Month &gt; "Jul '04" ] 은 2004년 7월 이후 발생한 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 &lt;= "값" </p> </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 작거나 같은 서수 값을 갖는 차원 Dim 요소를 적용합니다. "값"이 차원의 요소가 아닌 경우 차원의 현재 요소보다 크다고 가정합니다. </p> <p>예:Sessions[ Session_Number &lt;= "2" ] 는 방문자의 첫 번째 또는 두 번째 세션이었던 세션의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 흐림 &gt;= "값" </td> 
   <td colname="col2"> <p>"Value" 요소의 서수 값보다 크거나 같은 서수 값을 갖는 차원 Dim의 요소를 적용합니다. "값"이 차원의 요소가 아닌 경우 차원의 현재 요소보다 크다고 가정합니다. </p> <p>예:Sessions[ Session_Number &gt;= "5" ] 는 방문자에 대한 5번째 이상의 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>임의 흐림 </p> </td> 
   <td colname="col2"> <p>차원의 모든 요소 Dim을 허용합니다. </p> <p>예:Sessions[ any Page_View ] 는 페이지 보기가 하나 이상 있는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐림 없음 </p> </td> 
   <td colname="col2"> <p>모든 Dim이 거부하는 요소를 허용합니다. </p> <p>예:Sessions[ no Page_View ] 는 페이지 보기가 없는 세션 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(필터) </p> </td> 
   <td colname="col2"> <p>FILTER와 동일;필터 표현식의 일부를 그룹화하는 데 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
