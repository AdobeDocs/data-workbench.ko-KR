---
description: 리소스 모니터 벡터에는 메모리 예산 모니터 및 쿼리 수 모니터가 포함되어 있습니다.
title: 쿼리 큐 리소스 모니터
uuid: 6b516bed-7f9a-4821-869e-19e720f20313
exl-id: 6d445a4d-a415-41ce-9d45-1bdd0e726edd
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 2%

---

# 쿼리 큐 리소스 모니터{#query-queue-resource-monitors}

리소스 모니터 벡터에는 메모리 예산 모니터 및 쿼리 수 모니터가 포함되어 있습니다.

다음 표에서는 쿼리 큐에 사용되는 리소스 모니터 필드에 대해 설명합니다.

<table id="table_9991EED2647A460FACA2DC80D4973A8E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>메모리 예산 모니터 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>현재 사용자 그룹이 사용하는 쿼리 메모리를 모니터링합니다. 현재 사용량이 낮은 임계값과 높은 임계값 사이에 있는 경우, 사용자가 작업 영역을 닫은 결과 메모리 사용량이 낮은 임계값 아래로 돌아올 때까지 새 분치가 예약되지 않습니다. 예약된 번치를 확장할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>높은 임계값 </p> </td> 
   <td colname="col2"> <p>이중 </p> </td> 
   <td colname="col3"> <p>메모리 사용에 대한 높은 임계값(바이트)입니다. 메모리 사용이 이 값보다 크면 예약은 수행되지 않으며, 메모리 사용이 이 값 이하로 전환될 때까지 일정 기간 동안 가장 낮은 우선 순위의 예약된 부치가 한 번에 하나씩 예약되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>낮은 임계값 </p> </td> 
   <td colname="col2"> <p>이중 </p> </td> 
   <td colname="col3"> <p>메모리 사용에 대한 낮은 임계값(바이트)입니다. <span class="wintitle"> 메모리 예산 모니터</span> 값이 이 값 미만인 경우 새 번치를 예약할 수 있으며 예약된 번치를 늘릴 수 있습니다. 예를 들어 사용자가 작업 공간에 시각화를 추가하면 번치가 증가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>반응 시간 </p> </td> 
   <td colname="col2"> <p>이중 </p> </td> 
   <td colname="col3"> <p>메모리 사용 예상치를 부드럽게 하기 위한 시간 상수입니다. 보정 값을 사용하면 사용 스파이크에 대한 반응을 피할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>쿼리 수 모니터 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>현재 프로필에 대해 예약된 총 쿼리 수를 모니터링합니다. 이 리소스 모니터를 사용하면 총 쿼리 수가 낮은 임계값 필드의 값 아래에 남아 있는 경우 분치를 예약할 수 있습니다. 이 모니터는 전체 쿼리 수가 [높은 임계값] 필드의 값 아래로 유지되는 경우 현재 예약된 번치를 늘릴 수 있습니다. 또한 이 모니터는 우선 순위가 낮은 번치를 예약하거나 늘릴 수 있도록 낮은 우선 순위의 부치를 제거합니다. 하지만 이 설정은 [터치할 수 없는 우선 순위] 필드에 지정된 우선 순위보다 높은 우선 순위를 갖는 부치를 사전에 설정하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>높은 임계값 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>메모리 사용에 대한 높은 임계값(바이트)입니다. 메모리 사용이 이 값보다 크면 예약은 수행되지 않으며, 메모리 사용이 이 값 아래로 이동될 때까지 일정 기간 동안 가장 낮은 우선 순위의 예약된 부치가 한 번에 하나씩 예약되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>낮은 임계값 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>메모리 사용에 대한 낮은 임계값(바이트)입니다. <span class="wintitle"> 메모리 예산 모니터</span> 값이 이 값보다 낮으면 새 부치를 예약할 수 있으며 예약된 부치가 커질 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
