---
description: 밀도 맵 시각화는 요소를 사각형 맵 내의 음영처리된 사각형으로 표시합니다.
title: 밀도 맵
uuid: c13cecee-f322-4757-aa90-12039173ff9f
exl-id: da37d954-cadb-42a6-a44b-9b38c0354a5d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# 밀도 맵{#density-map}

{{eol}}

밀도 맵 시각화는 요소를 사각형 맵 내의 음영처리된 사각형으로 표시합니다.

사각형의 크기는 더 큰 값이 더 큰 영역의 사각형으로 표시되는 요소 값에 따라 달라집니다. 파이 차트와 유사하게 이 시각화를 사용하면 선택한 차원의 가장 큰 백분율을 구성하는 요소를 빠르게 확인할 수 있습니다.

![](assets/density_map_day_visits.png)

밀도 맵을 만들려면:

1. 새 작업 공간을 엽니다.

   새 작업 공간을 연 후 **추가** > **일시적으로 잠금 해제**.
1. 클릭 **[!UICONTROL Visualization]** > **[!UICONTROL Density Map]**.

1. 선택 **[!UICONTROL Dimension]** 메뉴 아래의 제품에서 사용할 수 있습니다.

   예를 들어, **[!UICONTROL Time]** > **[!UICONTROL Days]**.

   반면에 선택 **[!UICONTROL Time]** > **[!UICONTROL Hours]** 더 작은 값이 작은 사각형으로 표시되는 더 많은 요소를 제공할 수 있습니다.

   >[!NOTE]
   >
   >필요에 따라 여러 요소가 있는 차원을 선택할 수 있습니다. 현재 제한은 각 차원에 대해 가장 큰 요소의 200개입니다.

1. 차원 보기를 열어 변경할 수 있습니다 **[!UICONTROL Visualization]** > **[!UICONTROL Table]** 맵에 표시할 테이블에서 요소 간에 선택합니다.

   ![](assets/density_map_day_selections.png)

   맵은 테이블에서 선택한 항목에 응답합니다.

1. 작은 요소를 마우스로 가리키면 마우스 커서 근처에 나타나는 텍스트에 해당 이름과 값이 표시됩니다.
1. 마우스 오른쪽 단추를 클릭하고 선택하여 요소를 마스크합니다. **[!UICONTROL Mask]**&#x200B;를 선택한 다음 옵션을 선택합니다.

   ![](assets/density_map_day_mask.png)

   마스크된 노드를 모두 표시하려면 다음을 선택합니다 **[!UICONTROL Unhide All]**.

1. 마우스 오른쪽 단추를 클릭하고 선택하여 Spotlight 요소 **[!UICONTROL Spotlight]**&#x200B;를 선택한 다음 옵션을 선택합니다. Spotlight를 사용하면 범위에서 요소를 강조 표시하고 어둡게 할 수 있습니다.
1. 작업 공간에 색상 범례를 추가합니다. 색상 범례를 사용하여 맵에서 값을 식별할 수 있습니다.

   작업 공간에 색상 범례를 추가할 수 있으며 노드는 데이터의 추가 차원을 기반으로 색상을 변경합니다.
1. 맵 제목을 마우스 오른쪽 단추로 클릭하고 메뉴에서 선택하여 차원이나 지표를 변경합니다.

   ![](assets/density_map_change_dim.png)

1. 셀을 마우스 오른쪽 단추로 클릭하고 을 선택하여 콜아웃 추가 **[!UICONTROL Add Callout]**. 메뉴에서 다른 유형 또는 시각화 중에서 선택할 수 있습니다.

   ![](assets/density_map_callout.png)

1. 모든 시각화에서 제목 표시줄에서 마우스 오른쪽 단추를 클릭하여 기본 명령을 닫기, 저장, Microsoft Excel로 내보내기, 순서, 복사, 최소화 및 테두리 없이 시각화를 표시할 수 있습니다.

   ![](assets/density_map_export.png)

1. 밀도 맵을 사용하면 다른 시각화와 유사한 여러 요소를 선택하고 선택 취소할 수 있습니다.

* 요소를 선택하려면 마우스 왼쪽 단추를 클릭하십시오.
* 여러 요소를 선택하려면 Ctrl 키를 누른 채 클릭하십시오.
* 요소를 선택 취소하려면 Shift 키를 누른 상태로 클릭합니다.
* 선택한 요소 내에서 마우스 오른쪽 단추를 클릭하여 메뉴를 엽니다. 그런 다음 **[!UICONTROL Deselect]** 또는 **[!UICONTROL Deselect All]** 선택한 요소를 지우려면

## 추가 옵션 {#section-d77defb012424de4a7ced8e5c93115bc}

밀도 맵을 마우스 오른쪽 단추로 클릭하여 다음 옵션이 있는 메뉴를 엽니다.

<table id="table_3ADA85031C834792BFD041E186962A41"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 옵션 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에 설명선 </td> 
   <td colname="col2">요소를 추가로 식별하거나 설명하려면 시각화에서 설명선으로 텍스트나 그래픽을 추가합니다. <p>밀도 맵에서 선택한 요소를 기반으로 빈 지표 범례, 테이블, 선 그래프 또는 산포도 선택할 수도 있습니다. 그런 다음 필요에 따라 지표 및 차원을 이러한 빈 시각화에 추가할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마스크 </td> 
   <td colname="col2">마스킹 옵션을 사용하면 선택한 요소를 숨길 수 있습니다. 마우스 오른쪽 단추를 클릭하여 마스크 옵션을 표시합니다. <p><span class="uicontrol"> 이 요소 숨기기</span>- 선택한 단일 요소를 마스크하려면 이 옵션을 선택합니다. </p> <p><span class="uicontrol"> 선택 항목 숨기기</span>- 선택한 여러 요소를 마스크하려면 이 옵션을 선택합니다. </p> <p><span class="uicontrol"> 상위 표시</span>— 밀도 맵의 값을 기반으로 상위 100, 50, 25 또는 10개의 최상위 요소만 표시하려면 이 옵션을 선택합니다. </p> <p><span class="uicontrol"> 아래쪽 표시</span>- 밀도 맵의 값을 기준으로 하위 100, 50, 25 또는 10개의 상위 요소만 표시하려면 이 옵션을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 스포트라이트를 엽니다 </td> 
   <td colname="col2"> Spotlight를 사용하면 범위에서 요소를 강조 표시하고 어둡게 할 수 있습니다. 마우스 오른쪽 단추를 클릭하여 옵션 메뉴를 엽니다. <p><span class="uicontrol"> 상위 표시</span>— 밀도 맵의 값을 기반으로 상위 100, 50, 25 또는 10개의 최상위 요소만 강조 표시하려면 이 옵션을 선택합니다. </p> <p><span class="uicontrol"> 아래쪽 표시</span>- 밀도 맵의 값을 기반으로 하위 100, 50, 25 또는 10개의 상위 요소만 강조 표시하려면 이 옵션을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>선택 취소 </p> <p>전체 선택 취소 </p> </td> 
   <td colname="col2"> <p> 이 명령을 선택하여 현재 요소를 선택 취소하거나 선택한 모든 요소를 선택 취소합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
