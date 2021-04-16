---
description: 계산 가능한 차원의 요소는 시스템에서 계산할 수 있습니다.
title: 가산 차원
uuid: 3312f5eb-69b9-43af-b32a-5c40e3050b29
exl-id: c607c15d-de85-4daf-af76-79b460f51b38
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 4%

---

# 가산 차원{#countable-dimensions}

계산 가능한 차원의 요소는 시스템에서 계산할 수 있습니다.

계산 가능한 차원은 일반적으로 차원의 모든 요소의 개수 또는 합계를 반환하는 합계 지표를 만드는 데 사용됩니다. 예약 예약 예약 또는 제품 주문과 같은 인스턴스를 카운트하기 위해 계산 가능한 차원을 정의할 수 있습니다. 예를 들어 요소(온라인 스토어의 주문에 해당하는 로그 항목)를 계산할 수 있는 계산 가능한 차원 주문을 정의할 수 있습니다. 시각화 내에서 주문 수를 표시하려는 경우, 차원 위에 평가되거나 적용된 필터가 있는 주문 수 지표를 정의합니다.

계산 가능한 측정기준은 다른 측정기준의 상위 또는 다른 계산 가능한 측정기준의 하위에 있을 수 있습니다.

>[!NOTE]
>
>어떤 것의 계수만 제공하는 차원이 필요한 경우 COUNT 연산이 있는 숫자 차원을 사용해야 합니다. [숫자 Dimension](../../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed)을(를) 참조하십시오.

계산 가능한 차원은 다음 매개 변수로 정의됩니다.

<table id="table_9F3F093F5B074EA68CA4DCE731161F6C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 데이터 워크벤치에 있는 사용자에게 나타나는 차원의 설명형 이름. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 입력 필드가 계산 가능한 차원 생성에 기여하는 조건. 지정된 경우 조건이 데이터 세트 스키마의 모든 하위 차원 및 차원에 표시되는 로그 항목 집합을 제한합니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 데이터 워크벤치 인터페이스에 차원이 나타나는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되도록 설정된 경우 이 매개 변수를 true로 설정하여 데이터 워크벤치 디스플레이에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 </td> 
   <td colname="col2"> <p>선택 사항입니다. 키로 사용할 필드의 이름입니다. 이 매개변수를 정의할 경우 계산 가능한 차원 상위의 요소 조합과 키로 지정된 필드의 고유한 값을 조합할 때마다 계산 가능한 차원의 요소가 존재합니다. </p> <p> 계산 가능한 차원의 각 요소는 연속된 로그 항목 세트와 관련지을 필요가 있습니다. 따라서 로그 항목이 키로 순서가 지정되지 않은 경우 키 필드가 변경될 때마다 계산 가능한 차원의 요소가 생성됩니다. 이러한 상황을 방지하려면 시간 순서대로 인접한 고유한 키를 사용하는 것이 좋습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> <p>상위 차원의 이름입니다. 모든 계산 가능한 차원은 상위 차원일 수 있습니다. 데이터 세트 스키마에서 차원을 최상위 차원으로 만들려면 매개 변수를 "root"로 설정합니다. 정의된 차원은 데이터 세트에 대한 루트 계산 가능한 차원이 됩니다. 예를 들어 사이트에서 작업하는 경우 방문자 차원은 데이터 세트에 대한 루트 계산 가능한 차원입니다. </p> <p> <p>참고: 루트 계산 가능한 차원이 데이터의 추적 ID와 연결되어 있지 않아도 되지만 Adobe에서는 추적 ID 필드(x-trackingid)를 키로 사용하도록 데이터 세트의 루트 계산 가능한 차원을 구성하는 것이 좋습니다. 따라서 루트 계산 가능한 각 요소는 x-trackingid의 고유한 값과 연결되고 각 요소에 대한 모든 데이터가 함께 그룹화됩니다. 데이터 세트를 다르게 구성하려면 Adobe에 문의하십시오. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 계산 가능한 차원의 정의를 보여 줍니다. 계산 가능한 차원은 주어진 세션 내의 웹 캠페인 이벤트를 카운트합니다. 모든 이메일 캠페인 리소스가 cs-uri-query의 일부로 &quot;email=&quot;가 포함된 웹 서버에서 요청된다는 가정입니다. 이 예제에서 방문자가 지정된 세션 동안 이메일 캠페인에 응답한 횟수는 cs-uri-query(email) 필드의 실제 값이 아니라 관심 있는 횟수입니다.

![](assets/cfg_Transformation_Dim_Countable.png)

이 예는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 셀 수 없는 차원의 정의도 표시하지만 정의된 키 매개 변수가 있습니다. 세션 계산 가능 차원은 x-session-key 필드를 키로 사용합니다. x-session-key 필드는 [!DNL Sessionize] 변환의 출력이며 각 세션에 대한 고유 값을 갖습니다. 방문자 차원(상위)과 x-session-key 필드의 모든 고유한 요소 조합은 세션 차원의 요소입니다.

![](assets/cfg_Transformation_Dim_Countable2.png)
