---
description: 통계적 설명에서는 의미 있는 관계를 측정하여 고객 클러스터링 및 방문자 응답 점수부여의 고급 데이터 마이닝 기능에 대한 숨겨진 기회와 관심 변수를 식별합니다.
solution: Analytics
title: 통계 콜아웃
topic: Data workbench
uuid: 04911ac4-bc3f-4813-800b-087d9668a782
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 통계 콜아웃{#statistical-callouts}

통계적 설명에서는 의미 있는 관계를 측정하여 고객 클러스터링 및 방문자 응답 점수부여의 고급 데이터 마이닝 기능에 대한 숨겨진 기회와 관심 변수를 식별합니다.

통계 설명서는 계산 가능한 지표(방문, 주문 또는 다운로드)와 상관 관계가 있는 이진 변수(예/아니요, 0/1 또는 구매자/비구매자)와 같은 더 많은 유형의 데이터를 상호 연관시킬 수 있도록 알고리즘을 확장합니다.

통계 설명선을 추가하려면:

1. 표에서 지표 머리글을 마우스 오른쪽 단추로 클릭합니다.
1. 필요한 각 설정에 대한 확인 표시를 **[!UICONTROL Statistics]** 선택한 다음 선택하거나 취소합니다. 콜아웃 표시에서 모두 기본 설정으로 선택됩니다.

   ![](assets/statistical_callouts.png)

콜아웃은 데이터 집합 열에 포함된 통계 값을 반환할 수 있습니다.

<table id="table_B2A4F9D5938D4756A81ACF6F4D77E63D">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 계산 </th>
   <th colname="col2" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> 계수 </td>
   <td colname="col2"><p>데이터 세트에 있는 행 수를 반환합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 최대값 </td>
   <td colname="col2"><p> 차원의 모든 요소에서 최대 지표 값을 식별합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 최소값 </td>
   <td colname="col2"><p> 차원의 모든 요소에서 최소 지표 값을 식별합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 평균 </td>
   <td colname="col2"><p> 평균은 차원에 있는 요소의 지표 값에 대한 산술 평균으로서, 총 합계를 카운트(합계/카운트)로 나눈 값입니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 표준 편차 </td>
   <td colname="col2"> 표준 편차는 예상 평균으로부터 얼마만큼의 차이가 있는지를 보여줍니다. 표준 편차가 작으면 데이터 포인트가 평균에 가까움을 의미합니다. 표준 편차가 크면 데이터 포인트가 넓은 값 범위에 퍼져 있음을 의미합니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 합계 </td>
   <td colname="col2"><p> 지표 값의 합계를 반환합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 변화 </td>
   <td colname="col2"><p> 해당 차원에 대한 지표에서 지표 값의 분산을 의미합니다. 표준 편차의 제곱과 같습니다. </p></td>
  </tr>
 </tbody>
</table>

