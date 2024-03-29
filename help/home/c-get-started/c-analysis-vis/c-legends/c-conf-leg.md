---
description: 신뢰도 범례는 표시되는 숫자가 우연으로 인한 가능성이고 데이터의 가능한 편차를 이해할 가능성을 결정하는 데 도움이 됩니다.
title: 신뢰도 범례
uuid: 2559ff7c-6060-4fee-b509-9ae0c3912016
exl-id: 9aab169a-98b8-4e71-b74d-28e385c5c424
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---

# 신뢰도 범례{#confidence-legends}

{{eol}}

신뢰도 범례는 표시되는 숫자가 우연으로 인한 가능성이고 데이터의 가능한 편차를 이해할 가능성을 결정하는 데 도움이 됩니다.

데이터를 샘플링하지 않더라도 특정 기간 또는 하위 집합에서 전체 신뢰도를 가진 다른 기간 또는 하위 집합으로 숫자를 추출할 수 없습니다. 신뢰 범례를 사용하면 숫자가 특정 범위 내에 포함될 가능성을 탐색할 수 있습니다.

실세계 데이터를 큰 실험이라고 생각하면 실제 세계에는 여전히 기회가 있습니다. 정확한 숫자로 작업해도 말이죠. 예를 들어, 한 화요일에 오전 8시에서 오후 12시 사이의 거래를 완료한 사람의 수를 알고 있다는 것은 정확한 동일한 숫자가 다음 화요일에 그렇게 된다는 것을 의미하지는 않습니다.

다음 신뢰 범례는 변환 지표에 대한 신뢰 세부 사항을 표시하는 반면 다음 표는 각 데이터 포인트가 의미하는 바에 대한 자세한 정보를 제공합니다.

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
   <td colname="col2"> <p>신뢰도 정보를 보려는 지표 이름 또는 지표 식입니다. 작업 공간에서 선택한 모든 항목이 범례에 반영됩니다. 이 예는 전환 지표에 대한 세부 정보를 표시합니다. </p> <p>표현식 입력을 위한 구문 규칙에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f"> 쿼리 언어 구문</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>측정된 값 </p> </td> 
   <td colname="col2"> <p>수집된 실제 데이터의 값입니다. 이 예에서 현재 선택 영역의 전환율은 2.3%입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표준 편차 </p> </td> 
   <td colname="col2"> <p>측정값의 표준 편차. 이 예에서 현재 선택 항목에 대한 전환율의 표준 편차는 0.1%입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>"true" 값 </p> </td> 
   <td colname="col2"> <p>측정값이 각 가능성에 대해 나열된 범위 내에 있을 가능성. 이 예에서 이 "실제 실험"이 반복해서 반복되면 측정된 값이 2.1%와 2.4% 사이임을 90% 확신할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>계산 결과를 분석할 때는 다음 주의 사항을 고려해야 합니다.
>* 그 숫자는 추정이다. 다른 데이터 세트로 동일한 계산을 반복하면 다른 결과가 표시됩니다. 이를 무작위 변형이라고 합니다.
>* 모든 지표에 맞지 않는 정상인의 추정에 따라 더 높은 확률을 추정하는 것이 다릅니다. 따라서, 99% 확률에 대한 값은 90% 확률에 대한 값보다 신뢰성이 떨어집니다.
>
>정확한 숫자가 더 필요하다면 통계 전문가에게 문의해야 합니다.

## 지표 또는 공식 변경 {#section-7f09ff84c3514f26b78d29294e1f03d9}

* 신뢰 범례에서 **[!UICONTROL Metric or Formula]** 필드를 작성하고 원하는 지표나 표현식을 입력합니다. 표현식 구문 규칙에 대해서는 [쿼리 언어 구문](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f).

## Microsoft Excel로 내보내기 {#section-f36e2db7273740b7af278f8a2b79d564}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349).
