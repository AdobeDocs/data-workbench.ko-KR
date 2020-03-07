---
description: 연결 코드화 시각화를 사용하면 지표, 차원 및 요소 간의 비율과 연관성을 모두 표시할 수 있으므로 더 큰 코드를 보다 긴밀한 연관을 나타내는 표시로 표시할 수 있습니다.
title: 연결 코드 시각화
uuid: c656ffc8-e45a-44c0-a29b-cdc10dcbd1f2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 연결 코드 시각화{#association-chord-visualization}

연결 코드화 시각화를 사용하면 지표, 차원 및 요소 간의 비율과 연관성을 모두 표시할 수 있으므로 더 큰 코드를 보다 긴밀한 연관을 나타내는 표시로 표시할 수 있습니다.

연결 테이블은 상관 관계 매트릭스 및 상관 관계 코드 시각화에 사용된 상관 계수 대신 값을 [Cramer의 V](/help/home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md) 계산과 비교합니다( [이러한](/help/home/c-get-started/c-analysis-vis/associations-visualization.md) 값은 지표만 비교할 수 있고 연결 테이블 및 코드에서는 지표, 차원 및 요소를 비교할 수 있습니다). 또한 Associations Chord는 이전에 작성한 연결 테이블에 다른 뷰를 [제공합니다](../../../home/c-get-started/c-analysis-vis/associations-visualization.md#concept-9d937dda38174875b32095c6eaf22f2f).

**연결 코드 작성**

1. 작업 영역에서 시각화 > 예측 **분석 > 연결 코드를 마우스 오른쪽 단추로 클릭합니다**.

   목록에서 확장 차원을 선택할 수 있는 메뉴가 열립니다.

   ![](assets/association_chord1.png)

   선택하면 제목에 식별된 선택한 차원이 있는 빈 연결 테이블이 열립니다. ![](assets/association_chord2.png)

1. **지표, 차원 또는 차원 요소를**&#x200B;선택합니다.

   코드 시각화를 마우스 오른쪽 단추로 클릭하고 지표 추가 **또는 차원** 추가를 **선택합니다**. 메뉴에서 항목을 선택하여 코드에 추가합니다.

   지표와 차원을 클릭하고 **[!UICONTROL Finder]** 코드대로 드래그하여 지표와 차원을 **[!UICONTROL Ctrl-Alt]** 끌 수도 있습니다. 또한 열린 표에서 직접 코드표 시각화로 차원 요소를 드래그할 수 있습니다.

1. **연결할**&#x200B;추가 지표, 차원 및 요소를 선택합니다.

   두 개 이상의 값을 선택하면 차트가 자동으로 새로 고쳐지고 연결 데이터가 표시됩니다. 데이터 포인트를 연결하기 위해 필요에 따라 지표를 계속 추가합니다.

   ![](assets/association_chord.png)

   Chord 시각화에는 각 세그먼트의 영역으로 표현되는 전체 비율이 표시됩니다. 중요한 관계를 식별하고 조사할 필요에 따라 지표/차원/요소를 계속 추가합니다.

1. **Chord 시각화를**&#x200B;봅니다.

   시각화의 각 값 위로 마우스를 가져가면 관계를 볼 수 있습니다.

1. **설정 변경.** 코드 시각화를 마우스 오른쪽 단추로 클릭하여 메뉴를 열어 지표, 차원 또는 요소 표시 차원을 절대 숫자 또는 백분율로 변경하고, 선택한 지표나 모든 지표를 제거하고, 색상과 세부 사항을 편집하고, 값을 연결 테이블로 내보냅니다.

**연결 테이블에서 연결 코드를 만들려면**

1. 연결 테이블 **시각화를** 엽니다.
1. 마우스 오른쪽 버튼을 클릭하고 Export Chord **Visualization을 선택합니다**. 연결 테이블에서 선택한 값으로 연결 코드표(Association Chord) 다이어그램이 열립니다. ![](assets/association_table_to_chord.png)

>[!IMPORTANT]
>
>하나 이상의 지표를 포함하는 연결 코드표(연결 코드표)에서 연결 테이블을 내보내면 연결 테이블의 행/열에 요소가 중복됩니다. 중복된 요소를 방지하려면 연결 코드표에서 요소를 내보내지 않고 새 연결 테이블을 만들고 원하는 요소를 추가합니다.

