---
description: 세그먼트 내보내기 파일에 대한 사용자 정의 열 내보내기 헤더를 만들어 내보낸 세그먼트에 대해 쉽게 이해할 수 있는 설명을 추가합니다. 이 내보내기 기능을 사용하면 TSV 및 CSV 파일로 출력할 수도 있습니다.
title: 사용자 지정 헤더로 세그먼트 내보내기
uuid: 186e7868-13b2-42e1-b83f-5a752ee9b407
translation-type: tm+mt
source-git-commit: 8f5c69541bdd97aefbad3840f75f06846615f222
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 4%

---


# 사용자 지정 헤더로 세그먼트 내보내기{#segment-export-with-custom-headers}

세그먼트 내보내기 파일에 대한 사용자 정의 열 내보내기 헤더를 만들어 내보낸 세그먼트에 대해 쉽게 이해할 수 있는 설명을 추가합니다. 이 내보내기 기능을 사용하면 TSV 및 CSV 파일로 출력할 수도 있습니다.

헤더를 사용하여 내보내거나 CSV 및 TSV 형식으로 내보내는 기능을 포함하여, 새 기능이 세그먼트 내보내기에 추가되었습니다.

내보내기 파일의 열 헤더를 만들 수 있습니다.

## 새 세그먼트 내보내기 만들기 {#section-cffff55855f8467ea468b71393ab7676}

1. 작업 영역을 열고 > **[!UICONTROL Tools]** 를 마우스 오른쪽 단추로 클릭합니다 **[!UICONTROL Detail Table]**.

1. 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Add Level > Extended]** > 항목 선택을 선택합니다.
1. 제목을 마우스 오른쪽 단추로 클릭하고 메뉴에서 차원 **[!UICONTROL Add Attribute.]** 선택을 선택합니다.

1. 제목을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Metric.]** 메뉴에서 지표 선택을 선택합니다.

1. 제목을 마우스 오른쪽 단추로 클릭하고 선택합니다 **[!UICONTROL New Segment Export]**.

   ![](assets/segment_export_headers.png)

   **[!UICONTROL New Segment Export with Header]** 열 이름을 지표의 이름으로 자동으로 채웁니다. **[!UICONTROL New Segment Export]** 사용자 지정 이름을 설정해야 합니다. ![](assets/segment_export_with_headers.png)

   >[!NOTE]
   >
   >열 이름 필드는 비워 둘 수 없으며 헤더가 없습니다.

1. 세그먼트를 마우스 오른쪽 단추로 클릭하고 이름을 지정한 다음 을 클릭합니다 **[!UICONTROL Save Export File]**.

   내보내기 창이 열립니다.

1. 내보내기 이름을 마우스 오른쪽 단추로 클릭하고 다른 이름으로 **저장을 클릭합니다`<export filename>`**.

   ![](assets/segment_export_headers_7.png)

1. Right-click [!DNL Admin] > [!DNL Profile Manager] > [!DNL Expand Export]. 방금 만든 내보내기 파일을 찾아 기존 프로필에 저장합니다.

   ![](assets/segment_export_headers_8.png)

