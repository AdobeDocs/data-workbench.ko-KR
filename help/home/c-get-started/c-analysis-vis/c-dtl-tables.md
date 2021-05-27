---
description: 세부 사항 테이블을 사용하면 다른 시각화에서 선택한 사항에 의해 정의된 데이터 하위 집합에 대한 추가 정보를 볼 수 있습니다.
title: 세부 사항 테이블
uuid: 2becff5e-c78d-4ac7-8cda-814ad0193efd
exl-id: d7f0b768-f341-41e8-904b-ec98a25f7aa9
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 3%

---

# 세부 사항 테이블{#detail-table}

세부 사항 테이블을 사용하면 다른 시각화에서 선택한 사항에 의해 정의된 데이터 하위 집합에 대한 추가 정보를 볼 수 있습니다.

표시되는 추가 정보는 사용 가능한 모든 데이터의 샘플링입니다.

![](assets/vis_details.png)

다음 표에서는 세부 사항 테이블의 요소를 설명합니다.

<table id="table_C88C7F7F5AEA4820B908923E45CC0A62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col02" class="entry"> 색상 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>레벨 </p> </td> 
   <td colname="col02"> <p>분홍색 </p> </td> 
   <td colname="col2"> <p>세부 속성 및 지표 정보를 보려는 가산 차원입니다. 레벨 앞에 사용 가능한 요소 수 중 표시되는 요소 수가 표시됩니다. 예를 들어 6/444은 가능한 444에서 6개의 요소가 표시되고 있음을 나타냅니다. 위의 예에서 수준 방문자 는 제공된 모든 세부 사항이 방문자를 기반으로 함을 나타냅니다. 수준 페이지 보기 수는 제공된 모든 세부 사항이 페이지 보기를 기반으로 함을 나타냅니다. 서로 다른 계산 가능한 상위가 있는 데이터를 분석하려는 경우 여러 수준을 동시에 보는 것이 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>특성 </p> </td> 
   <td colname="col02"> <p>녹색 </p> </td> 
   <td colname="col2"> <p>도시-방문자 등 수준에서 일대다 또는 일대일 차원입니다. 각 행은 선택한 레벨의 각 요소와 관련된 요소를 표시합니다. 위의 예에서 도메인 및 도시 속성은 각 샘플 방문자에 대한 도메인과 시를 나열합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지표 </p> </td> 
   <td colname="col02"> <p>파란색 </p> </td> 
   <td colname="col2"> <p>선택한 수준에 대한 지표 세부 사항입니다. 위의 예에서 수준 이 방문자로 설정되어 있으면 페이지 보기 수 지표에는 개별 방문자에 대한 페이지 보기 수가 표시되고 페이지 보기 수 수준에서는 각 페이지 보기에 대한 세부 사항이 제공됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

웹 사이트 데이터로 작업하고 특정 도시 및 특정 도메인에서 방문자가 특정 기간 동안 방문한 페이지를 확인하려고 합니다.

먼저 관심이 있는 기간을 표시하는 시각화를 만든 다음 해당 기간을 선택해야 합니다. 이제 세부 사항 테이블을 추가하여 데이터 집합에 있는 방문자 샘플 수에 대해 원하는 세부 정보를 볼 수 있습니다.

위에 설명된 세부 정보를 보려면 다음 단계를 완료해야 합니다.

1. 세부 사항 테이블 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Level]** > **[!UICONTROL Visitor]** 를 클릭합니다.
1. 세부 사항 테이블 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Level]** > **[!UICONTROL Page View]** 를 클릭합니다.
1. **[!UICONTROL Visitors]** 수준 제목을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL Domain]** 를 클릭합니다.
1. 방문자 수준 제목 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL City]** 를 클릭합니다.
1. 방문자 수준 제목 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Metric]** > **[!UICONTROL Page Views]** 를 클릭합니다.
1. 페이지 보기 횟수 수준 머리글 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Attribute]** > **[!UICONTROL Page]** > **[!UICONTROL Page]** 를 클릭합니다.

다음 샘플 작업 공간은 지정한 기간 동안 6명의 사이트 방문자를 임의 샘플링하기 위한 관련 세부 정보를 보여줍니다.

![](assets/client-tab1.png)

## 수준 {#section-f948d3361fd84906ac4d9ebce520bfd0} 추가

* 세부 사항 테이블 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Level]** > *&lt;**[!UICONTROL dimension name]*** 를 클릭합니다.

![](assets/mnu_DetailsTable_AddLevel.png)

## 수준 {#section-a8c820e0b656451e98e5ea75373edefc} 제거

* 기존 수준 제목을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Remove Level]** > *&lt;**[!UICONTROL dimension name]*** 를 클릭합니다.

![](assets/mnu_DetailsTable_Level.png)

## 속성 및 지표 추가 {#section-cdda2df3c9a448d5b9770686c8b8efb3}

* 속성이나 지표 제목을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Attribute]** > *&lt;**[!UICONTROL attribute name]*** 또는 **[!UICONTROL Add Metric]** > *&lt;**[!UICONTROL metric name]***&#x200B;을 클릭합니다.

![](assets/mnu_DetailsTable.png)

## 속성 및 지표 제거 {#section-4002ac957a2846678f9940270987d651}

* 제거할 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Remove Attribute]** > *&lt;**[!UICONTROL attribute name]*** 또는 **[!UICONTROL Remove Metric]** > *&lt;**[!UICONTROL metric name]***&#x200B;을 클릭합니다.

![](assets/mnu_DetailsTable.png)

## Microsoft Excel로 내보내기 {#section-a9eaba63c88a4598836a34669ba8cac1}

창 내보내기에 대한 자세한 내용은 [창 데이터 내보내기](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)를 참조하십시오.
