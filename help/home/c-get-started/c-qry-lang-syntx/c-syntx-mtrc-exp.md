---
description: 지표는 지표 편집기를 사용하여 편집하고 프로필의 지표 디렉토리에 저장할 수 있습니다.
title: 지표 표현식 구문
uuid: 801e265d-d7e4-4f0f-9698-d0b50dd00995
exl-id: 27d86fea-6500-4608-aadb-f39058fd3a6e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 1%

---

# 지표 표현식 구문{#syntax-for-metric-expressions}

{{eol}}

지표는 지표 편집기를 사용하여 편집하고 프로필의 지표 디렉토리에 저장할 수 있습니다.

자세한 내용은 [파생 지표 만들기 및 편집](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40). 지표 표현식은 워크시트에서 사용할 수도 있습니다. 자세한 내용은 [워크시트](../../../home/c-get-started/c-analysis-vis/c-wksts/c-wksts.md#concept-45b50aafc4d84709841f14aee8022581). 다음 구문은 지표 표현식을 정의하는 데 사용됩니다.

참고:

1. 밑줄 친 단어는 문자 그대로 식 텍스트에 입력해야 합니다.
1. 양식 `{TEXT}?` 선택적 텍스트를 나타냅니다.
1. 양식 `{TEXT}*` 0회 이상 발생할 수 있는 텍스트를 나타냅니다.
1. 양식 `{A | B | C |...}` A 또는 B 또는 C... 등 지정된 옵션 중 하나로 구성된 텍스트를 나타냅니다..
1. 양식 `[A,B)` 는 A부터 B까지 범위의 숫자를 나타냅니다.

<table id="table_A6CA9C9F396448209398AA2A369E63FA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>식별자는 명명된 지표를 참조합니다. 법적 식별자를 관리하는 규칙에 대해서는 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> 식별자용 구문 </a>. </p> <p>예: 매출 = Total_Price </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(지표) </p> </td> 
   <td colname="col2"> <p>(지표) 결과는 지표 결과와 동일합니다. 괄호는 표현식에서 작업 순서를 지정합니다. </p> <p>예: 평균 = (A + B) / 2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A + B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 합계. </p> <p>예: 값 = 수익 + 비용 절감 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A - B </p> </td> 
   <td colname="col2"> <p>지표 A와 지표 B의 결과 차이. </p> <p>예: 이익 = 수익 - 원가 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A * B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 제품입니다. </p> <p>예: 달러 = 센트 * 0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A/B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 비율입니다. </p> <p>예: Revenue_per_Session = Revenue / Sessions </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A^ B </p> </td> 
   <td colname="col2"> <p>지표 A의 결과가 지표 B의 결과 기능으로 향상되었습니다. </p> <p>예: 영역 = 너비^2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>신뢰도(지표) </p> </td> 
   <td colname="col2"> <p>지표의 표준 편차의 예상. 이것은 잭킹이라고 알려진 샘플링 기법을 사용하여 계산됩니다. </p> <p>이 지표는 메모리가 많이 사용되므로 큰 표에서 사용하지 않아야 합니다. </p> <p>이 구문을 사용하려면 적절한 속성을 갖는 자칼 차원("jackknife"라고 함)이 있어야 합니다. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오. </p> <p>예: confidence(Average_Score) </p> <p> <p>참고: 신뢰도(지표) 및 신뢰도(지표,jacknife)를 포함한 신뢰도 지표 유형은 특히 Adobe의 통제 실험 기능을 사용할 때 유용합니다. 통제된 실험 중에 지표가 12%에서 16%로 급증한 경우 신뢰 콜아웃을 사용하여 점프가 임의 변형으로 인한 확률을 계산할 수 있습니다. 이것은 제한된 증거로부터 잘못된 결론을 도출하는 것을 피하는데 도움이 될 수 있고, 반대로, 의심스러운 변화가 실제로 현실적이라는 것을 보증합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>신뢰도(지표, 자칼) </p> </td> 
   <td colname="col2"> <p>지표의 표준 편차의 예상. 이것은 잭킹이라고 알려진 샘플링 기법을 사용하여 계산됩니다. 이 구문을 사용하면 "jackknife" 이외의 다른 이름으로 명명된 jackknife 차원을 사용하여 지표의 신뢰도를 결정할 수 있습니다. </p> <p>이 지표는 메모리가 많이 사용되므로 큰 표에서 사용하지 않아야 합니다. </p> <p>이 구문을 사용하려면 적절한 속성을 갖는 자칼 차원("jackknife" 이외의 이름)이 있어야 합니다. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오. </p> <p>예: confidence(Average_Score,SubSamples) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eval(CellReference) </p> </td> 
   <td colname="col2"> <p>참조하는 셀의 컨텐츠를 지표 식으로 처리합니다. 이 구문은 워크시트 시각화에서만 사용할 수 있습니다. </p> <p>예: eval(B1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그(B, X) </p> </td> 
   <td colname="col2"> <p>수학 로그 함수: 지표 X는 매개 변수이며 지표 B는 기본입니다. </p> <p>예: dB = 20*log(진폭,10) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지표[필터] </p> </td> 
   <td colname="col2"> <p>"필터가 있는 지표": 주어진 필터로 필터링된 새 지표. </p> <p>예: Jan_Sessions = Sessions[ Month="Jan" ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimension별 지표 </p> </td> 
   <td colname="col2"> <p>차원의 "수준"에서 평가된 지표입니다. (M by X)[F] (필터 "F"로 평가된 지표 "M by X"의 결과)는 M[F by X]의 결과입니다(결과 "M"이 필터 "F by X"로 평가됨). </p> <p>예: AB_Visitors = </p> <p>(세션별 방문자)[Page="A" and Page="B"] = </p> <p>Session[(Page="A" 및 Page="B") 방문자 수] = </p> <p>동일한 세션에서 페이지 A와 페이지 B를 방문한 방문자의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>number </p> </td> 
   <td colname="col2"> <p>값이 고정된 지표. </p> <p>예: Pi = 3.1415 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(지표) </p> </td> 
   <td colname="col2"> <p>지표가 평가되는 차원을 무시합니다. 지표는 해당 차원의 모든 요소에 대해 동일한 값을 갖습니다. </p> <p>예: Pct_of_Visitors = 방문자 수/총 방문자 수(방문자 수) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모두(지표) </p> </td> 
   <td colname="col2"> <p>지표에 적용되는 필터를 무시합니다. 지표는 선택 및 기타 필터의 영향을 받지 않습니다. </p> <p>예: 벤치마크_Sessions = all( 세션 ) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(all(지표) </p> </td> 
   <td colname="col2"> <p>모든 필터 및 차원을 무시합니다. 적용된 필터 또는 차원에 관계없이 주어진 프로필 전체에서 동일한 값을 갖습니다. </p> <p>예: Dataset_Visitors = total(all(방문자) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(One,Countable_Dimension) </p> </td> 
   <td colname="col2"> <p>방문자 또는 세션과 같이 계산할 수 있는 차원의 수를 제공하는 지표입니다. </p> <p>예: 방문자 = sum(One,Visitor) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(숫자_ Dimension, Countable_ Dimension) </p> </td> 
   <td colname="col2"> <p>가산 차원에 숫자 차원의 합계를 제공하는 지표. 숫자 차원 요소의 서수 값(형식이 지정된 값과 반대됨)이 사용되므로 결과에 배율 인수를 적용해야 하는 경우가 많습니다. </p> <p>예: 값 = sum(Session_Value, Session)*0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>min(A, B) </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 더 적은 결과. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>max(A, B) </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 중 큰 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>format(A, B) </p> </td> 
   <td colname="col2"> <p>지표 B의 서식 기능을 사용한다는 점을 제외하면 지표 A와 동일한 지표입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
