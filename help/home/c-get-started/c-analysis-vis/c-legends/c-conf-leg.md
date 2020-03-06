---
description: 신뢰 범례는 사용자가 보고 있는 숫자가 우연으로 인한 가능성을 확인하고 데이터의 가능한 편차를 이해하는 데 도움이 됩니다.
solution: Analytics
title: 신뢰도 범례
topic: Data workbench
uuid: 2559ff7c-6060-4fee-b509-9ae0c3912016
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 신뢰도 범례{#confidence-legends}

신뢰 범례는 사용자가 보고 있는 숫자가 우연으로 인한 가능성을 확인하고 데이터의 가능한 편차를 이해하는 데 도움이 됩니다.

데이터를 샘플링하지 않더라도 특정 기간이나 하위 집합에서 다른 기간이나 전체 신뢰도의 하위 집합으로 숫자를 추정할 수 없습니다. 신뢰 범례를 사용하면 숫자가 특정 범위 내에 있을 가능성을 탐색할 수 있습니다.

실세계 데이터를 큰 실험으로 본다면, 실제 세상은 여전히 기회를 가지고 있습니다. 정확한 숫자를 가지고 작업할 때도 말이죠. 예를 들어, 하나의 화요일에 오전 8시에서 오후 12시 사이의 거래를 완료한 사람의 수를 알고 있다는 것은 정확한 숫자가 다음 화요일에 그렇게 된다는 것을 의미하지는 않습니다.

다음 신뢰 범례는 전환 지표에 대한 신뢰 세부 사항을 표시하는 반면, 다음 표는 각 데이터 포인트의 의미에 대한 자세한 정보를 제공합니다.

![](assets/lgd_ConfidenceLegend.png)

<table id="table_387F22C7EF4E4DE9AD810D3D9204676F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>지표 또는 공식 </p> </td> 
   <td colname="col2"> <p>신뢰도 정보를 보려는 지표 이름 또는 지표 표현식. 작업 영역에서 선택한 모든 항목이 범례에 반영됩니다. 이 예에서는 전환 지표에 대한 세부 사항을 표시합니다. </p> <p>표현식 입력을 위한 구문 규칙에 대한 자세한 내용은 쿼리 언어 <a href="../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f"> 구문을 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>측정된 값 </p> </td> 
   <td colname="col2"> <p>수집된 실제 데이터의 값입니다. 이 예에서는 현재 선택 항목의 전환율이 2.3%입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표준 편차 </p> </td> 
   <td colname="col2"> <p>측정된 값의 표준 편차. 이 예에서는 현재 선택 항목에 대한 전환율의 표준 편차가 0.1%입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>"true" 값 </p> </td> 
   <td colname="col2"> <p>측정된 값이 각 가능성에 대해 나열된 범위 내에 포함될 가능성이 있습니다. 이 예에서, 이 "실제 실험"이 반복해서 반복되는 경우, 측정된 값이 2.1%에서 2.4% 사이인지 90% 확신할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>계산 결과를 분석할 때는 다음 사항을 고려해야 합니다.>
>* 그 수치는 추정이다. 다른 데이터 세트에 대해 동일한 계산을 반복하면 다른 결과를 얻을 수 있습니다. 이를 무작위 변이로 합니다.
>* 더 높은 확률에 대한 추정은 모든 지표에 대해 올바르지 않은 정상 상태에 대한 가정에 달려 있습니다. 따라서 99%의 확률에 대한 값은 90%의 확률에 대한 값보다 안정성이 낮습니다.
>
>
더 정확한 숫자가 필요하면 통계 전문가의 도움을 받아야 한다.

## 지표 또는 공식 변경 {#section-7f09ff84c3514f26b78d29294e1f03d9}

* 신뢰 범례에서 **[!UICONTROL Metric or Formula]** 필드를 클릭하고 원하는 지표나 표현식을 입력합니다. 표현식 구문 규칙에 대해서는 쿼리 [언어 구문을 참조하십시오](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f).

## Microsoft Excel로 내보내기 {#section-f36e2db7273740b7af278f8a2b79d564}

창 내보내기에 대한 자세한 내용은 창 [데이터 내보내기를 참조하십시오](../../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349).
