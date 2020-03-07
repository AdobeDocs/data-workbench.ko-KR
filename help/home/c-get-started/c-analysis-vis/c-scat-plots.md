---
description: '분산형 플롯은 x축과 y축이 서로 다른 지표를 나타내는 격자에 데이터 차원의 요소(예: 페이지 또는 도시)를 그래프로 표시합니다.'
solution: Analytics
title: 2D 분포도
topic: Data workbench
uuid: 73c23d22-3c3a-4535-b66b-0e3508bd904c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 2D 분포도{#d-scatter-plots}

분산형 플롯은 x축과 y축이 서로 다른 지표를 나타내는 격자에 데이터 차원의 요소(예: 페이지 또는 도시)를 그래프로 표시합니다.

분산형 플롯은 서로 다른 많은 항목의 관계를 두 개의 서로 다른 지표로 이해하려는 경우 유용합니다. 다음 예에서는 각 도시를 방문자 수와 각 유지율을 기준으로 보여 주는 산포도 분포입니다.

![](assets/vis_ScatterPlot_City.png)

산포도는 이상치를 빨리 볼 수 있도록 해줍니다. 예를 들어 Salt Lake City는 방문자당 평균 유지율보다 높습니다.

또한 데이터 일관성을 표시하는 데 산포도 사용할 수 있습니다. 다음 예에서는, 산포도 특정 길이의 세션이 있는 방문자 수를 보여줍니다.

![](assets/vis_ScatterPlot_SessionDuration.png)

산포도 내의 각 점의 크기는 반경 지표에 의해 결정됩니다. 기본 반경 지표는 각 Adobe 애플리케이션에 대해 다릅니다. 예를 들어 에서 [!DNL Site]반경 지표는 기본적으로 세션을 기반으로 합니다. 산포도 내의 점이 사용 가능한 지표를 나타내도록 반경 지표를 변경할 수 있습니다. 이를 위한 단계는 반경 [지표 변경을](../../../home/c-get-started/c-analysis-vis/c-scat-plots.md#section-fd80576d583c430cb469daf12e39aa2a) 참조하십시오. 점의 색상은 작업 공간 내에 열려 있는 색상 범례를 기반으로 합니다. 색상 범례에 대한 자세한 내용은 색상 범례를 [참조하십시오](../../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).

## 포인트 선택 {#section-4b4d45f39b884d54bb7407b3b2f4ea50}

**단일 점을 선택하려면**

* 점을 클릭합니다.

**선택 영역에 다른 점 또는 점 그룹을 추가하려면**

* Ctrl 키를 누른 채 점을 클릭하거나 Ctrl 키를 누른 채 여러 점을 드래그합니다.

**선택 항목에서 점 또는 점 그룹을 제거하려면**

* Shift 키를 누른 상태에서 점을 클릭하거나 Shift 키를 누른 채 여러 점을 드래그합니다.

## 차원 변경 {#section-796cd962ef3f476caa89d99083782ed1}

* 그래프 맨 위에 있는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Change Dimension]** > *&lt;**[!UICONTROL dimension name]**>*&#x200B;를 클릭합니다.

## 지표 변경 {#section-44b8be9215cd4039b1eeb98ae1b31445}

**산포도 x축 또는 y축에 표시되는 지표를 변경하려면**

* 변경할 지표의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Change Metric]** > *&lt;**[!UICONTROL metric name]**>*&#x200B;를 클릭합니다.

## 반경 지표 변경 {#section-fd80576d583c430cb469daf12e39aa2a}

**산포도 반경 지표 변경**

그래프 맨 위에 있는 차원의 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Change Radius Metric]** > *&lt;**[!UICONTROL metric name]**>*&#x200B;를 클릭합니다.

![](assets/mnu_ScatterPlot_Change.png)

