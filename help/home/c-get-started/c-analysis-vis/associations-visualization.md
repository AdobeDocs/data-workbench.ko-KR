---
description: 연결 테이블 시각화를 사용하면 Cramer의 V 알고리즘을 사용하여 지표, 차원 및 차원 요소와 지표를 연결할 수 있습니다.
title: 연결 테이블 시각화
uuid: 4563c336-3377-4929-8694-8c0d00866825
exl-id: 3fc2c025-d369-45ed-8c9e-eb4a0ac412b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# 연결 테이블 시각화{#association-table-visualization}

{{eol}}

연결 테이블 시각화를 사용하면 Cramer의 V 알고리즘을 사용하여 지표, 차원 및 차원 요소와 지표를 연결할 수 있습니다.

연결 테이블은 값을 Pearson에서 사용한 대로 상관 계수를 사용하는 대신 Cramer의 V 계산과 비교합니다 [상관 관계 매트릭스](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/correlation-analysis/c-correlation-analysis.html) 및 [상관 관계 코드](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/c-chord-visualization.html) 시각화(지표만 비교할 수 있고 연결 표와 [연결 코드](../../../home/c-get-started/c-analysis-vis/associations-chord.md#concept-51d0bda998474dd5946cc2a9b8393445) 지표, 차원 및 요소를 비교할 수 있습니다.)

## 연결 테이블 작성 {#section-87ed12ccc1af4196a1b6534e621c4cbb}

연결 테이블은 가산 차원이나 가산 가능한 차원에 대해 지표를 비교합니다. 표를 수정하여 색상 피킹을 통해 시각화 내의 연결을 강조 표시하거나 텍스트 맵, 열 맵 또는 두 가지 모두로 렌더링할 수 있습니다.

1. 연결 테이블을 엽니다.

   마우스 오른쪽 단추 클릭 [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Association Table].

   ![](assets/association_table.png)

1. 확장된 차원(클릭스루, 히트, 제품, 방문 또는 방문자 차원)을 선택합니다. 연결 테이블은 모서리에서 식별된 확장 차원과 행 및 열 모두에 배치된 관련 지표와 함께 열립니다.

   ![](assets/association_table1.png)

   연결 테이블은 Cramer의 V를 대칭적인 상관 관계로 사용하여 선택된 지표, 차원 및 요소 값이 연관 테이블의 열과 행 모두에 반영됩니다. 예를 들어, **제품** 확장 차원은 **[!UICONTROL Visits]** 지표는 테이블의 행과 열 모두에서 연결된 지표로, 비교 값이 동일하므로 완벽하지만 쓸모 없는 비교(1.00)가 됩니다.

1. 연결 테이블에 값을 더 추가합니다.

   열이나 행을 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **지표 추가** 또는 **Dimension 추가**. 지표와 차원을 **파인더** 패널. Dimension 요소를 열린 테이블에서 표 시각화로 드래그하여 놓을 수도 있습니다.

   ![](assets/association_table2.png)

   >[!NOTE]
   >
   >연결 테이블에 허용되는 행과 열은 10개로 제한됩니다.
