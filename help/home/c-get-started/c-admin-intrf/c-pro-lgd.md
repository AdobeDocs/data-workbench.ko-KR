---
description: 처리 범례는 특정 서버의 데이터 처리 및 변환에 대한 자세한 정보를 제공하여 재처리 및 재변환되는 데이터의 진행 상황을 추적할 수 있습니다.
title: 처리 범례
uuid: 6c082c8f-fbb3-4e48-a249-2a13345fda86
exl-id: a83ce514-c92b-4cf8-a3cc-bff4e2ba63f1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---

# 처리 범례{#processing-legend}

처리 범례는 특정 서버의 데이터 처리 및 변환에 대한 자세한 정보를 제공하여 재처리 및 재변환되는 데이터의 진행 상황을 추적할 수 있습니다.

![](assets/vis_ProcessingLegend.png)

다음 표에는 [!DNL Processing Legend] 을 사용하여 완료할 수 있는 작업이 나와 있습니다.

<table id="table_6149250C44B14C44A3CB1CEF68B280C6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>모든 데이터의 총 크기를 보려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Total Log Entries</span> 및 <span class="wintitle"> Log Bytes Total</span> 필드의 값을 검토합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필터링이 작동하는지 확인하려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Total Filtered Log Entries</span> 필드의 값을 검토합니다. 값이 0이면 필터링이 작동하지 않으므로 구성을 확인하여 문제를 해결해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 진행 상황을 확인하려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> 로그 처리 진행률</span> 필드에서 값을 검토합니다. 이 백분율은 재처리가 완료되는 양을 나타냅니다. </p> <p>데이터 세트를 재처리하여 세분화할 때 <span class="wintitle"> 복호화된 총 로그 항목</span> 수와 <span class="wintitle"> 필터링된 총 로그 항목 수</span>를 비교해 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변환 진행 상태를 확인하려면 </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> 변환 진행률</span> 필드에서 값을 검토합니다. 이 백분율은 전체 변환 양을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
