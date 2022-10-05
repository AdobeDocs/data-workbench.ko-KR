---
description: 트렌드 라인을 사용하면 그래프를 오버레이하여 데이터를 비교하고 해석할 수 있습니다.
title: 꺾은 선형
uuid: b1d81973-2181-4507-a0a5-adf5eeb9f926
exl-id: 3e7e9218-49b2-4877-a4bd-318b838089e8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# 꺾은 선형{#trend-lines}

{{eol}}

트렌드 라인을 사용하면 그래프를 오버레이하여 데이터를 비교하고 해석할 수 있습니다.

좋아요 [산포도](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/c-scat-plots.html) 시각화를 통해 이제 그래프 시각화에 트렌드 라인을 설정하여 선형, 지수, 전력 또는 다항식 선에 따른 변경 비율을 표시할 수 있습니다. 트렌드 라인 기능을 사용하면 그래프에 트렌드 라인을 오버레이할 수 있으며, 가장 일반적으로 시간 차원에 걸쳐 있습니다.

예를 들어 이 그래프 비교를 통해 방문 수가 트렌드를 표시하지만 주문 수가 트렌드를 표시하고 있음을 알 수 있습니다.

![](assets/trend_line.png)

꺾은 선형을 추가하려면

1. 그래프를 열고 왼쪽 상단 모서리에서 지표 이름을 마우스 오른쪽 단추로 클릭합니다.
1. 클릭 **[!UICONTROL Trend Lines]** 옵션을 선택합니다.

   ![](assets/trend_line_graph.png)

   그래프에 표시할 꺾은 선형을 다음과 같이 선택할 수 있습니다 **단순 선형**, **지수**, **전원**, 또는 **다항식**. 다항식이 다항식 회귀 트렌드 라인을 만듭니다. 단순 선형 은 회귀 라인을 따라 변경 비율로 트렌드 라인을 만듭니다. 지수는 꺾은 선형을 y = b로 계산합니다.&#42;exp( a&#42;x ) 및 Power as y = b&#42;x`<sup>a</sup>`.

   트렌드가 계산되어 그래프에 렌더링되고 트렌드 방정식의 세부 정보를 표시하는 콜아웃이 열립니다.

   ![](assets/trend_line_detail.png)
