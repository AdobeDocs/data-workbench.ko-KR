---
description: 연결 테이블 시각화를 사용하면 Cramer의 V 알고리즘을 사용하여 지표를 지표, 차원 및 차원 요소와 연결할 수 있습니다.
title: 연결 테이블 시각화
uuid: 4563c336-3377-4929-8694-8c0d00866825
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# 연결 테이블 시각화{#association-table-visualization}

연결 테이블 시각화를 사용하면 Cramer의 V 알고리즘을 사용하여 지표를 지표, 차원 및 차원 요소와 연결할 수 있습니다.

연관 테이블은 상관 관계 매트릭스 및 상관 관계 코드 시각화에 사용된 상관 계수 대신 값을 [Cramer의](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/correlation-analysis/c-correlation-analysis.html) V 계산과 비교합니다( [지표만 비교할 수](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/c-chord-visualization.html) 있고 연결 테이블 및 연결 코드에서는 지표, 차원 및 요소를 [비교할 수](../../../home/c-get-started/c-analysis-vis/associations-chord.md#concept-51d0bda998474dd5946cc2a9b8393445) 있는 반면이러한 수는비교할 수 있습니다).

## 연결 테이블 만들기 {#section-87ed12ccc1af4196a1b6534e621c4cbb}

연결 테이블은 계산 가능 차원이나 비계산 차원 위에 지표를 비교합니다. 표를 수정하여 색상 선택을 통해 시각화 내의 연결을 강조 표시하거나 텍스트 맵, 히트 맵 또는 둘 다로 렌더링할 수 있습니다.

1. 연결 테이블을 엽니다.

   마우스 오른쪽 단추를 클릭하여 [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Association Table]을 클릭합니다.

   ![](assets/association_table.png)

1. 확장 차원(클릭스루, 히트, 제품, 방문 또는 방문자 차원)을 선택합니다. 연결 테이블은 모서리에서 식별된 확장 차원과 행 및 열 모두에 연결된 지표로 열립니다.

   ![](assets/association_table1.png)

   연결 테이블은 Cramer의 V를 대칭 상관 관계로 사용하므로 선택된 지표, 차원 및 요소 값이 연관 테이블의 열과 행에 모두 반영됩니다. 예를 들어 제품 **확장** 차원을 선택하면 표의 행과 열 모두에서 **[!UICONTROL Visits]** 지표가 연결되어 비교(1.00)되므로 완벽하지만 쓸모없는 비교(1.00)가 됩니다.

1. 연결 테이블에 값을 더 추가합니다.

   열 또는 행을 마우스 오른쪽 단추로 클릭하고 지표 추가 **또는 차원** 추가를 **선택합니다**. 파인더 패널에서 지표와 차원을 드래그할 수도 **있습니다** . 또한 차원 요소를 열린 테이블에서 테이블 시각화로 드래그하여 놓을 수 있습니다.

   ![](assets/association_table2.png)

   >[!NOTE]
   >
   >연결 테이블에 허용되는 행 및 열은 10개로 제한됩니다.

