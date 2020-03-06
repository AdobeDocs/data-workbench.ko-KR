---
description: 처리 범례는 특정 서버의 데이터 처리 및 변환에 대한 자세한 정보를 제공하므로 재처리 및 재변형되는 데이터의 진행 상태를 추적할 수 있습니다.
solution: Analytics
title: 처리 범례
topic: Data workbench
uuid: 6c082c8f-fbb3-4e48-a249-2a13345fda86
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 처리 범례{#processing-legend}

처리 범례는 특정 서버의 데이터 처리 및 변환에 대한 자세한 정보를 제공하므로 재처리 및 재변형되는 데이터의 진행 상태를 추적할 수 있습니다.

![](assets/vis_ProcessingLegend.png)

다음 표에는 를 사용하여 완료할 수 있는 작업이 나와 [!DNL Processing Legend]있습니다.

<table id="table_6149250C44B14C44A3CB1CEF68B280C6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>모든 데이터의 전체 크기를 보려면 </p> </td> 
   <td colname="col2"> <p>[총 로그 항목 수] <span class="wintitle"> 및 [로그</span> 바이트 <span class="wintitle"> 합계] 필드의 값을</span> 검토합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>필터링이 작동하는지 확인하려면 </p> </td> 
   <td colname="col2"> <p>필터링된 총 로그 항목 <span class="wintitle"> 필드의 값을</span> 검토합니다. 값이 0이면 필터링이 작동하지 않고 구성을 확인하여 문제를 해결해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 진행 상태를 확인하려면 </p> </td> 
   <td colname="col2"> <p>로그 처리 진행 <span class="wintitle"> 필드에서 값을</span> 검토합니다. 이 백분율은 재처리가 얼마나 완료되었는지를 나타냅니다. </p> <p>다시 처리하여 데이터 세트를 수정할 때 전체 디코딩된 로그 항목 수와 필터링된 <span class="wintitle"> 총 로그 항목</span> 수를 <span class="wintitle"> 확인할 수 있습니다</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변환 진행 상태를 확인하려면 </p> </td> 
   <td colname="col2"> <p>변환 진행(Transformation Progress) <span class="wintitle"> 필드에서 값을</span> 검토합니다. 이 백분율은 변환이 완료된 양을 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

