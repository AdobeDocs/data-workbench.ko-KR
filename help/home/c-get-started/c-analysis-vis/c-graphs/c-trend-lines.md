---
description: 트렌드 라인을 사용하면 그래프를 오버레이하여 데이터를 비교 및 해석할 수 있습니다.
title: 꺾은 선형
uuid: b1d81973-2181-4507-a0a5-adf5eeb9f926
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# 꺾은 선형{#trend-lines}

트렌드 라인을 사용하면 그래프를 오버레이하여 데이터를 비교 및 해석할 수 있습니다.

산포도 [시각화처럼](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/c-scat-plots.html) 이제 선형, 지수, 전력 또는 다항식 선을 기반으로 변화율을 표시하도록 그래프 시각화에 트렌드 라인을 설정할 수 있습니다. 트렌드 라인 기능을 사용하면 일반적으로 시간 차원에 걸쳐 그래프에 트렌드 라인을 오버레이할 수 있습니다.

예를 들어 이 그래프 비교에서는 방문 수가 트렌드를 높이고 있지만 주문 수가 트렌드를 보여주고 있습니다.

![](assets/trend_line.png)

트렌드 라인을 추가하려면

1. 그래프를 열고 왼쪽 상단 모서리에서 지표 이름을 마우스 오른쪽 단추로 클릭합니다.
1. 을 **[!UICONTROL Trend Lines]** 클릭하고 옵션에서 선택합니다.

   ![](assets/trend_line_graph.png)

   그래프 위에 단순 선형, 지수 **,**&#x200B;전력 **,**&#x200B;다항식 **중**&#x200B;하나로 표시할 꺾은 **선을 선택할 수**&#x200B;있습니다. 다항식으로 다항식 회귀 꺾은 꺾은 꺾은 선형을 만듭니다. 단순 선형은 회귀선을 따라 변경 비율로 트렌드 라인을 만듭니다. 지수에서는 y = b*exp( a*x ) 및 Power as y = b*x로 트렌드 라인을 계산합니다`<sup>a</sup>`.

   트렌드는 그래프에서 계산되고 렌더링되며 트렌드 방정식의 세부 정보를 표시하는 콜아웃이 열립니다.

   ![](assets/trend_line_detail.png)

