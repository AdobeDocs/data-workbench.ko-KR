---
description: 통계 설명선은 의미 있는 관계를 측정하여 대상 클러스터링 및 방문자 응답 점수 책정 시 고급 데이터 마이닝 기능에 대한 숨겨진 기회와 관심 변수를 식별합니다.
title: 통계 설명선
uuid: 04911ac4-bc3f-4813-800b-087d9668a782
exl-id: d4ed540e-f837-4db9-a81e-b8a30c15f270
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 22%

---

# 통계 설명선{#statistical-callouts}

{{eol}}

통계 설명선은 의미 있는 관계를 측정하여 대상 클러스터링 및 방문자 응답 점수 책정 시 고급 데이터 마이닝 기능에 대한 숨겨진 기회와 관심 변수를 식별합니다.

통계 콜아웃은 알고리즘을 확장하므로 계산 가능한 지표(방문 횟수, 주문 또는 다운로드)와 상관 관계가 있는 이진 변수(예/아니요, 0/1 또는 구매자/비구매자)와 같은 더 많은 유형의 데이터가 상호 작용할 수 있습니다.

통계 콜아웃을 추가하려면

1. 표에서 지표 헤더를 마우스 오른쪽 단추로 클릭합니다.
1. 선택 **[!UICONTROL Statistics]** 그런 다음 필요한 각 설정에 대한 확인 표시를 선택하거나 선택 취소합니다. 콜아웃 표시(Display Callout)의 모든 항목이 기본 설정으로 선택됩니다.

   ![](assets/statistical_callouts.png)

콜아웃은 데이터 세트 열에 팩터링된 통계적 값을 반환할 수 있습니다.

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
   <td colname="col2"><p> 차원의 모든 요소에 걸쳐 최소 지표 값을 식별합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 평균 </td>
   <td colname="col2"><p> 평균은 Dimension에 있는 요소의 지표 값에 대한 산술 평균으로서, 총계를 개수(합계/카운트)로 나눈 값입니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 표준 편차 </td>
   <td colname="col2"> 표준 편차는 예상 평균으로부터 얼마만큼의 차이가 있는지를 보여줍니다. 표준 편차가 작으면 데이터 포인트가 평균에 가까움을 의미합니다. 표준 편차가 크면 데이터 포인트가 넓은 값 범위에 퍼져 있음을 의미합니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 합계 </td>
   <td colname="col2"><p> 지표 값의 총 합계를 반환합니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> 분산 </td>
   <td colname="col2"><p> 해당 차원에 대해 지표에서 지표 값의 분산에 대한 측정입니다. 표준 편차의 제곱과 같습니다. </p></td>
  </tr>
 </tbody>
</table>
