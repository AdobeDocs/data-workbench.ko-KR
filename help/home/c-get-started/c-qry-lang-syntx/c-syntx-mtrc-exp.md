---
description: 지표 편집기를 사용하여 지표를 편집하고 프로필의 지표 디렉토리에 저장할 수 있습니다.
solution: Analytics
title: 지표 표현식 구문
topic: Data workbench
uuid: 801e265d-d7e4-4f0f-9698-d0b50dd00995
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 지표 표현식 구문{#syntax-for-metric-expressions}

지표 편집기를 사용하여 지표를 편집하고 프로필의 지표 디렉토리에 저장할 수 있습니다.

자세한 내용은 파생된 지표 [만들기 및 편집을 참조하십시오](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40). 지표 표현식을 워크시트에 사용할 수도 있습니다. 자세한 내용은 워크시트를 [참조하십시오](../../../home/c-get-started/c-analysis-vis/c-wksts/c-wksts.md#concept-45b50aafc4d84709841f14aee8022581). 다음 구문은 지표 표현식을 정의하는 데 사용됩니다.

참고:

1. 밑줄 친 단어는 문자 그대로 표현식 텍스트에 입력해야 합니다.
1. {TEXT} 양식입니까? 은 선택적 텍스트를 나타냅니다.
1. {TEXT}* 형식은 0회 이상 발생할 수 있는 텍스트를 나타냅니다.
1. 양식 {A| B| C|...}은 A, B 또는 C와 같은 지정된 옵션 중 하나로 구성된 텍스트를 나타냅니다..
1. 양식 [A,B)은 A부터 B까지 숫자 범위를 나타냅니다.

<table id="table_A6CA9C9F396448209398AA2A369E63FA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>식별자 </p> </td> 
   <td colname="col2"> <p>식별자는 명명된 지표를 참조합니다. 법적 식별자를 제어하는 규칙에 대해서는 식별자에 <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> 대한 구문을 참조하십시오 </a>. </p> <p>예:매출 = Total_Price </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(지표) </p> </td> 
   <td colname="col2"> <p>(지표)의 결과는 지표의 결과와 동일합니다. 괄호는 표현식에서 작업 순서를 지정합니다. </p> <p>예:평균 = (A + B) / 2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A + B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 합계. </p> <p>예:값 = 매출 + 비용 절감 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A - B </p> </td> 
   <td colname="col2"> <p>지표 A와 지표 B의 결과 차이. </p> <p>예:이익 = 수익 - 원가 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A * B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 제품. </p> <p>예:달러 = 센트 * 0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A/B </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 비율. </p> <p>예:Revenue_per_Session = 매출 / 세션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A^ B </p> </td> 
   <td colname="col2"> <p>지표 A의 결과가 지표 B의 결과의 거듭제곱 값으로 상승했습니다. </p> <p>예:영역 = 너비^2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>신뢰도(지표) </p> </td> 
   <td colname="col2"> <p>지표의 표준 편차의 예상 이것은 자크링이라고 알려진 샘플링 기법을 사용하여 계산됩니다. </p> <p>이 지표는 메모리를 많이 사용하므로 큰 테이블에서 사용해서는 안 됩니다. </p> <p>이 구문을 사용하려면 적절한 속성이 있는 자칼 차원("자칼")이 있어야 합니다. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오. </p> <p>예:confidence(Average_Score) </p> <p> <p>참고: 신뢰도(지표) 및 신뢰도(지표,jacknife)를 비롯한 신뢰도 지표 유형은 Adobe의 제어 실험 기능을 사용할 때 특히 유용합니다. 제어된 실험 중에 지표가 12%에서 16%로 이동한 경우 임의 변동으로 인해 점프할 가능성을 계산하는 신뢰 콜아웃을 사용할 수 있습니다. 이는 제한된 증거로부터 잘못된 결론을 도출하는 것을 피할 수 있고, 반대로 미심쩍은 변화가 실제로 존재한다는 확신을 줄 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>신뢰도(지표, 자칼) </p> </td> 
   <td colname="col2"> <p>지표의 표준 편차의 예상 이것은 자크링이라고 알려진 샘플링 기법을 사용하여 계산됩니다. 이 구문을 사용하면 "잭나이프" 이외의 다른 이름으로 하는 자칼 차원을 사용하여 지표의 신뢰도를 결정할 수 있습니다. </p> <p>이 지표는 메모리를 많이 사용하므로 큰 테이블에서 사용해서는 안 됩니다. </p> <p>이 구문을 사용하려면 적절한 속성이 있는 자칼 차원("자칼" 이외의 것)이 있어야 합니다. 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오. </p> <p>예:신뢰도(Average_Score,SubSamples) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eval(CellReference) </p> </td> 
   <td colname="col2"> <p>참조하는 셀의 컨텐츠를 지표 표현식으로 처리합니다. 이 구문은 워크시트 시각화에서만 사용할 수 있습니다. </p> <p>예:eval(B1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그(B, X) </p> </td> 
   <td colname="col2"> <p>수학 로그 함수:지표 X는 매개 변수이고 지표 B는 기준입니다. </p> <p>예:dB = 20*log(진폭,10) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지표[필터] </p> </td> 
   <td colname="col2"> <p>"필터가 있는 지표":주어진 필터에 의해 필터링된 새 지표. </p> <p>예:Jan_Sessions = Sessions[ Month="Jan" ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>차원별 지표 </p> </td> 
   <td colname="col2"> <p>차원의 "수준"에서 평가된 지표. (M by X)[F](필터 "F"로 평가된 지표 "M by X"의 결과)는 M[F by X]의 결과입니다("F by X" 필터로 평가된 지표 "M"의 결과). </p> <p>예:AB_Visitors = </p> <p>(세션별 방문자 수)[페이지="A" 및 페이지="B"] = </p> <p>세션별 방문자[(페이지="A" 및 페이지="B") = </p> <p>동일한 세션에서 페이지 A와 페이지 B를 방문한 방문자 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수 </p> </td> 
   <td colname="col2"> <p>값이 고정된 지표. </p> <p>예:Pi = 3.1415 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(지표) </p> </td> 
   <td colname="col2"> <p>지표가 평가되는 차원을 무시합니다. 지표는 해당 차원의 모든 요소에 대해 동일한 값을 가집니다. </p> <p>예:Pct_of_Visitors = 방문자 수/총(방문자 수) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>all(지표) </p> </td> 
   <td colname="col2"> <p>지표에 적용되는 필터를 무시합니다. 지표는 선택 및 기타 필터의 영향을 받지 않습니다. </p> <p>예:Benchmark_Sessions = all( 세션 ) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(all(지표) </p> </td> 
   <td colname="col2"> <p>모든 필터 및 크기를 무시합니다. 적용된 필터 또는 차원에 관계없이 해당 프로필 전체에 동일한 값이 있습니다. </p> <p>예:Dataset_Visitors = total(all(방문자) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(One,Countable_Dimension) </p> </td> 
   <td colname="col2"> <p>방문자 또는 세션과 같은 계산 가능한 차원의 수를 제공하는 지표. </p> <p>예:방문자 = sum(One,Visitor) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(Numeric_Dimension, Countable_Dimension) </p> </td> 
   <td colname="col2"> <p>계산 가능한 차원 위에 숫자 차원의 합계를 제공하는 지표. 숫자 차원 요소의 서수 값(서식이 지정된 값과 반대)이 사용되므로 비율 인수를 결과에 적용해야 하는 경우가 많습니다. </p> <p>예:값 = sum(Session_Value, Session)*0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>min(A, B) </p> </td> 
   <td colname="col2"> <p>지표 A와 지표 B의 더 적은 결과. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>max(A, B) </p> </td> 
   <td colname="col2"> <p>지표 A 및 지표 B의 결과 중 더 큽니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>format(A, B) </p> </td> 
   <td colname="col2"> <p>지표 B의 서식 기능을 사용한다는 점을 제외하고 지표 A와 동일한 지표. </p> </td> 
  </tr> 
 </tbody> 
</table>

