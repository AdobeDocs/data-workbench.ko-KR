---
description: 이제 데이터 워크벤치의 막대 그래프에는 여러 그래프에 걸쳐 여러 지표에 대한 회귀 비교가 포함됩니다.
title: 회귀 분석 그래프
uuid: 8512890e-f42b-4dce-826a-2b4bf2a215f4
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Regression Analysis Graph{#regression-analysis-graph}

이제 데이터 워크벤치의 막대 그래프에는 여러 그래프에 걸쳐 여러 지표에 대한 회귀 비교가 포함됩니다.

[데이터 워크벤치의 막대 그래프를](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/graphs/c-graphs.html) 사용하면 한 그래프의 지표를 다른 그래프에 있는 지표에 등록할 수 있습니다. 여러 그래프가 있는 경우 지표를 독립 변수로 비교하고 다른 지표(종속 변수)를 평가하는 그래프와 비교할 수 있습니다. 이렇게 하면 한 종속 변수(먼저 설정된 지표)와 일련의 다른 변경 지표(설정된 종속 지표로 회귀) 간의 관계 강도를 확인할 수 있습니다.

애널리스트는 그래프 시각화에 대한 회귀 분석을 통해 &quot;what-if&quot; 시나리오를 수행할 수 있습니다. 예를 들어 방문 수가 이 수준으로 증가하면 이러한 증가가 매출에 어떤 영향을 미칩니까?

**회귀 분석 설정**

1. 회귀 비교를 위해 종속 지표로 그래프를 선택합니다.

   그래프를 마우스 오른쪽 버튼으로 클릭하고 회귀를 **위한 기본 지표로 설정을 선택합니다**.

   ![](assets/c_graph_regression_1.png)

1. 다른 지표 그래프를 독립 변수로 설정합니다.

   지표를 마우스 오른쪽 단추로 클릭하고 다른 지표에 **[!UICONTROL Regress with `<base metric name>`]** 대해 선택합니다.

   ![](assets/c_graph_regression.png)

1. 그래프를 마우스 오른쪽 버튼으로 클릭하여 막대를 위아래로 이동시켜 회귀 상황을 볼 수 있습니다.

   특정 값에 대한 그래프를 마우스 오른쪽 단추로 클릭하면 위쪽 또는 아래쪽 값에 대해 각 지표의 회귀 비율을 볼 수 있습니다.

   ![](assets/c_graph_regression_2.png)

   예를 들어 페이지 보기 횟수가 86,041로 감소하면 다른 지표에는 다음 값이 있게 됩니다.12,183의 방문 횟수와 12,028의 방문자.

   ![](assets/c_graph_regression_3.png)

   방문별 방문자 수 값이 26,141로 증가하면 다른 지표는 26,560의 방문 횟수가 되고 페이지 보기는 189,091이 됩니다.

