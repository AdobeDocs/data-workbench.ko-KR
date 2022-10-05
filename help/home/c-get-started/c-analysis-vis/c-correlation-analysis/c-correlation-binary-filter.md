---
description: 상관 관계 매트릭스의 이진 필터를 사용하면 상관 관계가 있는 지표 중 하나 또는 둘 다에 대한 값을 제한하여 비교에 더 잘 집중할 수 있습니다.
title: 상관 관계 매트릭스의 이진 필터
uuid: 61c3ca37-cfa2-49dc-87de-4e9a44647eca
exl-id: e693fc72-5697-4c47-a498-e0d4d875c688
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 5%

---

# 상관 관계 매트릭스의 이진 필터{#binary-filter-in-the-correlation-matrix}

{{eol}}

상관 관계 매트릭스의 이진 필터를 사용하면 상관 관계가 있는 지표 중 하나 또는 둘 다에 대한 값을 제한하여 비교에 더 잘 집중할 수 있습니다.

상관 관계 매트릭스에서 이진 필터를 설정하려면 다음을 수행하십시오.

1. 상관 관계 매트릭스에서 지표 이름을 마우스 오른쪽 단추로 클릭합니다.
1. 선택 **지표 세부 사항 편집**.

   ![](assets/correlation_matrix_binary_filter.png)

   다음 **[!UICONTROL Edit Correlation Metric Details]** 창이 열립니다.

   ![](assets/correlation_matrix_metric_details.png)

1. 이진 필터를 설정합니다.

   먼저 **[!UICONTROL Inactive]** 설정 필터를 로 설정하도록 전환합니다. **[!UICONTROL Active]** 그리고 **비교** 및 **값** 필드.

   그런 다음 **[!UICONTROL Comparison]** 연산자를 설정하고 **[!UICONTROL Value]** 을 눌러 선택한 지표에 대한 필터를 설정합니다.

>[!IMPORTANT]
>
>Data Workbench 6.2용 이진 필터가 새로운 기능으로 업데이트되어 이전 버전에서 빌드된 이진 필터로 상관 관계 매트릭스를 다시 빌드해야 합니다.

## Dimension 요소 추가 {#section-f19f4e0368ca488e92d1e28bcc24417c}

차원 요소를 추가하여 지표를 제한할 수도 있습니다. 지표에는 연결된 요소가 하나만 있을 수 있습니다.

![](assets/correlation_matrix_element.png)

작업 공간에서 마우스 오른쪽 단추를 클릭하고 을 선택합니다. **표**. 요소를 사용하여 차원을 열고 로 드래그합니다. **[!UICONTROL Element]** 상관 관계 지표 세부 정보 편집 창에서 설정하거나 상관 관계 매트릭스에서 지표를 놓습니다.
