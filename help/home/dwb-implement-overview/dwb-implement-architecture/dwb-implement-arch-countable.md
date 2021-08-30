---
description: 스키마를 디자인 및 구현하기 위한 DWB(Dataworkbench)의 계산 테이블에 대한 설명입니다.
title: 스키마 디자인 계산 가능한 구조
uuid: 2530980d-1c6b-4a96-b9c1-431fc75678bb
exl-id: 4f2a2f8a-7b42-42bb-8ba1-2675ffe6b2c2
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 3%

---

# 스키마 디자인 계산 가능한 구조{#schema-design-countable-structures}

스키마를 디자인 및 구현하기 위한 DWB(Dataworkbench)의 계산 테이블에 대한 설명입니다.

## Data Workbench의 계산 가능 이해 {#section-6e6b8d1c17634d669e62c91a80a0bc62}

가장 높은 수준에서 가산 차원입니다. 가산 차원은 두 가지 주요 기능을 제공합니다. 먼저 계산하려는 요소의 차원입니다. 다시 말해, 카운터 테이블은 다음과 같은 질문에 대답합니다.

* 홈 페이지를 방문한 방문자는 몇 명입니까?

* Google.com에서 방문한 방문자는 몇 명입니까?

`<discoiqbr>`가산 차원은 일반적으로 차원의 모든 요소의 카운트 또는 합계를 반환하는 합계 지표를 만드는 데 사용됩니다. 예약 예약 또는 제품 주문과 같은 인스턴스를 카운트할 가산 차원을 정의할 수 있습니다. 예를 들어, 요소를 계산할 수 있는 계산 가능한 차원 주문(온라인 스토어의 주문에 해당하는 로그 항목)을 정의할 수 있습니다. 시각화 내에 주문 수를 표시하려면 차원을 통해 평가되거나 필터가 적용되는 주문 합계 지표를 정의합니다.

계산 가능한 측정기준은 다른 측정기준의 상위 또는 다른 계산 가능한 측정기준의 하위에 있을 수 있습니다.

루트 가산 차원이 데이터의 추적 ID와 연결할 필요가 없지만 데이터 세트의 루트 가산 차원을 구성하여 추적 ID 필드(x-trackingid)를 키로 사용하는 것이 좋습니다. 따라서 루트 카운테이블의 각 요소는 x-trackingid의 고유한 값과 연결되며 각 요소에 대한 모든 데이터가 함께 그룹화됩니다.

가산 차원은 다음 매개 변수로 정의됩니다.

<table id="table_5E00B72CFDD645368ADCC25AB9B5E53D"> 
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
   <td colname="col2"> Data Workbench에서 사용자에게 표시되는 차원의 수사적 이름입니다. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>댓글 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 확장 차원에 대한 참고 사항

    &lt;/p> &lt;/td>
<td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>조건 </p> </td> 
   <td colname="col2"> <p>입력 필드가 계산 가능한 차원 생성에 기여하는 조건입니다. 지정하면 조건이 차원에 표시되는 로그 항목 세트와 데이터 세트 스키마의 모든 하위 항목을 제한합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 차원이 Data Workbench 인터페이스에 표시되는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되는 경우 이 매개 변수를 true로 설정하여 Data Workbench 표시에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 </td> 
   <td colname="col2"> <p>선택 사항입니다. 키로 사용할 필드의 이름입니다. 이 매개 변수를 정의하면 계산 가능한 차원의 상위 요소와 키로 지정된 필드의 고유 값을 조합할 때마다 계산 가능한 차원의 요소가 존재합니다. </p> <p>가산 차원의 각 요소는 연속적인 로그 항목 세트와 관련시키는 데 필요합니다. 따라서 로그 항목이 키로 정렬되지 않으면 키 필드가 변경될 때마다 계산 가능한 차원의 요소가 만들어집니다. 이러한 상황을 방지하기 위해 Adobe은 시간 순서대로 인접한 고유한 키를 사용하는 것을 권장합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> <p> 상위 차원의 이름입니다. 가산 차원은 상위 차원일 수 있습니다. 차원을 데이터 집합 스키마에서 최상위 차원으로 만들려면 매개 변수를 "root"로 설정합니다. 정의된 차원은 데이터 집합에 대한 루트 가산 차원이 됩니다. 예를 들어 사이트를 사용하여 작업하는 경우 방문자 차원은 데이터 세트에 대해 계산할 수 있는 루트 차원입니다. </p> <p>참고: 루트 가산 차원이 데이터의 추적 ID와 연결할 필요가 없지만 데이터 세트의 루트 가산 차원을 구성하여 추적 ID 필드(x-trackingid)를 해당 키로 사용하는 것이 좋습니다. 따라서 루트 카운테이블의 각 요소는 x-trackingid의 고유한 값과 연결되며 각 요소에 대한 모든 데이터가 함께 그룹화됩니다. 데이터 세트를 다르게 구성하려면 Adobe에 문의하십시오. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제는 웹 사이트 트래픽에서 수집된 이벤트 데이터를 사용하여 가산 차원의 정의를 보여줍니다. 가산 차원은 주어진 세션 내의 웹 캠페인 이벤트를 계산합니다. 모든 이메일 캠페인 리소스는 cs-uri-query의 일부로 &quot;email=&quot;가 포함된 웹 서버에서 요청된다고 가정합니다. 이 예에서 방문자가 주어진 세션 동안 이메일 캠페인에 응답하는 횟수는 cs-uri-query(email) 필드의 실제 값이 아니라 관심사입니다.

![](assets/dwb_impl_arch_1.png)

counttable의 두 번째 주요 기능은 데이터 집합 스키마 구조의 중추를 구성하는 것입니다. 데이터 스키마와 기타 모든 차원은 아래에 그룹화되고 계산 가능한 차원에 속하도록 구성되어 있습니다. 다시 말해, 차원을 &quot;카테고리&quot;로 간주하면 카운테이블이 이러한 &quot;카테고리&quot;를 그룹으로 구성하는 방법입니다.
차원을 가산 차원 아래에 그룹화할 때 가산 차원의 &quot;수준&quot;에 있다고 합니다. 예를 들어 아래 그림에서 &#39;이메일 주소&#39;가 방문자 수준에 있고 &quot;브라우저&quot;가 방문 수준에 있음을 알 수 있습니다. &quot;상위&quot; 및 &quot;하위&quot;는 계산 가능한 차원과 그 아래에 그룹화된 차원 간의 관계를 의미합니다. 예를 들어 방문자는 이메일 주소의 &quot;상위&quot;입니다. 반대로 이메일 주소는 방문자의 &quot;하위&quot;입니다. ![](assets/dwb_impl_arch_2.png) ![](assets/dwb_impl_arch_3.png)

## Data Workbench에서 계산 가능 만들기 {#section-491f3e8e4fbc429e95d6c97f012a208e}

Dataworkbench에서 계산 가능한 을 만들려면 다음 단계를 수행하십시오.

1. 프로필 관리자 열기
1. 변형 폴더에서 구성 파일을 만들어 워크스테이션에서 엽니다.
1. 확장 Dimension 아래에서 마우스 오른쪽 단추를 클릭하고 아래와 같이 새로 추가 -> 계산 가능 을 선택합니다. ![](assets/dwb_impl_arch_4.png)

1. 새 계산 가능한 이름을 입력합니다. 아래 예에서는 고객 계산 가능 이 정의됩니다. 최상위 계산 가능한 경우 상위 쓰기 루트에서 ![](assets/dwb_impl_arch_5.png)

   Countable이 최상위 레벨 1이 아닌 경우 상위 필드에 상위 계산 가능한 이름을 지정합니다. 아래 예에서는 참여 계산 이 생성되고 이 계산 가능한 상위는 고객입니다. ![](assets/dwb_impl_arch_5.png)

스키마 디자인, 계산 가능한 구조 및 오프라인 데이터 피드 구성을 위한 Data Workbench 아키텍처에 대한 자세한 내용은 [데이터 세트 스키마 인터페이스](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/c-dtst-sch-intrf.html)를 참조하십시오.
