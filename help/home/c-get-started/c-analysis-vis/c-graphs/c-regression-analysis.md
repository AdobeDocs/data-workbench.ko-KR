---
description: 이제 Data Workbench의 막대 그래프에는 여러 그래프에 걸쳐 여러 지표에 대한 회귀 비교가 포함됩니다.
title: 회귀 분석 그래프
uuid: 8512890e-f42b-4dce-826a-2b4bf2a215f4
exl-id: bfc76c4a-edd5-41fe-b875-c199ea3beab5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# 회귀 분석 그래프{#regression-analysis-graph}

{{eol}}

이제 Data Workbench의 막대 그래프에는 여러 그래프에 걸쳐 여러 지표에 대한 회귀 비교가 포함됩니다.

[막대 그래프](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/graphs/c-graphs.html) Data Workbench에서 한 그래프의 지표를 다른 그래프의 지표에 요약할 수 있습니다. 여러 개의 그래프가 있는 경우 지표(독립 변수)를 다른 지표(종속 변수로)를 평가하는 그래프와 비교할 수 있습니다. 이렇게 하면 한 종속 변수(먼저 설정된 지표)와 다른 일련의 변경 지표(설정된 종속 지표와의 회귀) 간의 관계의 강도를 결정할 수 있습니다.

그래프 시각화의 회귀 분석을 사용하면 분석가가 &quot;what-if&quot; 시나리오를 수행할 수 있습니다. 예를 들어 방문 수가 이 수준까지 증가하면 매출에 어떤 영향을 줍니까?

**회귀 분석 설정**

1. 회귀 비교를 위해 그래프를 종속 지표로 선택합니다.

   그래프를 마우스 오른쪽 버튼으로 클릭하고 을 선택합니다 **회귀의 기본 지표로 설정**.

   ![](assets/c_graph_regression_1.png)

1. 다른 지표 그래프를 독립 변수로 설정합니다.

   지표를 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **[!UICONTROL Regress with `<base metric name>`]** 추가 정보.

   ![](assets/c_graph_regression.png)

1. 그래프를 마우스 오른쪽 단추로 클릭하여 회귀 보기를 클릭하여 막대를 위아래로 이동합니다.

   특정 값에 대한 그래프를 마우스 오른쪽 단추로 클릭하면 증가 또는 하향 값을 기준으로 각 지표의 회귀 비율을 볼 수 있습니다.

   ![](assets/c_graph_regression_2.png)

   예를 들어, 내 페이지 보기 수가 86,041로 감소하면 다른 지표에는 다음 값이 있습니다. 12,183의 방문 및 12,028의 방문자 수.

   ![](assets/c_graph_regression_3.png)

   방문별 방문자 수 값이 26,141로 증가하면 다른 지표는 26,560의 방문 횟수이고 페이지 보기 수는 189,091입니다.
