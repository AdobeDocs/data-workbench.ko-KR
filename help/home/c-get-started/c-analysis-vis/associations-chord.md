---
description: 연결 Chord 시각화를 사용하면 지표, 차원 및 요소 간의 비율 및 연결을 모두 표시할 수 있으며 더 큰 코드를 더 강한 연관성을 나타내는 표시로 표시할 수 있습니다.
title: 연결 Chord 시각화
uuid: c656ffc8-e45a-44c0-a29b-cdc10dcbd1f2
exl-id: e71394ef-4895-4a3e-912d-d6f56ca8f001
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---

# 연결 Chord 시각화{#association-chord-visualization}

{{eol}}

연결 Chord 시각화를 사용하면 지표, 차원 및 요소 간의 비율 및 연결을 모두 표시할 수 있으며 더 큰 코드를 더 강한 연관성을 나타내는 표시로 표시할 수 있습니다.

연결 테이블은 Pearson에 사용된 대로 Correlation 계수를 사용하는 대신 값을 Cramer의 V 계산과 비교합니다 [상관 관계 매트릭스](/help/home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md) 및 [상관 관계 코드](/help/home/c-get-started/c-analysis-vis/associations-visualization.md) 시각화(지표만 비교할 수 있고, 연결 테이블 및 코드는 지표, 차원 및 요소를 비교할 수 있습니다.) 연결 코드도 이전에 빌드한 항목에 다른 보기를 제공합니다 [연결 테이블](../../../home/c-get-started/c-analysis-vis/associations-visualization.md#concept-9d937dda38174875b32095c6eaf22f2f).

**연결 코드를 만들려면**

1. 작업 공간에서 마우스 오른쪽 단추 클릭 **시각화 > Predictive Analytics > 연결 코드**.

   목록에서 확장된 차원을 선택할 수 있는 메뉴가 열립니다.

   ![](assets/association_chord1.png)

   선택하면 제목에서 식별된 선택한 Dimension과 함께 빈 연결 테이블이 열립니다. ![](assets/association_chord2.png)

1. **지표, 차원 또는 차원 요소를 선택합니다**.

   Chord 시각화를 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **지표 추가** 또는 **Dimension 추가**. 메뉴에서 항목을 선택하여 코드에 추가합니다.

   지표와 차원을 **[!UICONTROL Finder]** 를 클릭합니다. **[!UICONTROL Ctrl-Alt]** 지표와 차원을 코드로 끌어서 놓습니다. 또는 차원 요소를 열린 테이블에서 코드 시각화로 직접 드래그합니다.

1. **연결할 추가 지표, 차원 및 요소를 선택합니다**.

   둘 이상의 값을 선택한 후 차트가 자동으로 새로 고침되고 연결 데이터 표시를 시작합니다. 데이터 포인트를 연결하는 데 필요에 따라 지표를 계속 추가합니다.

   ![](assets/association_chord.png)

   Chord 시각화는 각 세그먼트의 영역으로 표시된 전체 비율의 비율을 표시합니다. 중요한 관계를 식별하고 조사하는 데 필요한 지표/차원/요소를 계속 추가합니다.

1. **Chord 시각화 보기**.

   시각화의 각 값 위로 마우스를 가져가면 관계를 볼 수 있습니다.

1. **설정 변경.** 코드 시각화를 마우스 오른쪽 단추로 클릭하여 메뉴를 열고 지표, 차원 또는 요소를 절대 번호 또는 백분율로 표시하고, 선택한 지표나 모든 지표를 제거하고, 색상 및 세부 사항을 편집하고, 값을 연결 테이블로 내보냅니다.

**연결 테이블에서 연결 코드를 작성하려면 다음을 수행하십시오.**

1. 열기 **연결 테이블** 시각화.
1. 마우스 오른쪽 단추를 클릭하고 을 선택합니다 **Chord 시각화 내보내기**. 연결 테이블에서 선택한 값으로 연결 코드 다이어그램이 열립니다. ![](assets/association_table_to_chord.png)

>[!IMPORTANT]
>
>하나 이상의 지표가 포함된 연결 코드 다이어그램에서 연결 테이블을 내보내면 연결 테이블의 행/열에 요소가 중복됩니다. 중복 요소를 방지하려면 연결 코드 다이어그램에서 요소를 내보내는 대신 새 연결 테이블을 만들고 원하는 요소를 추가합니다.
