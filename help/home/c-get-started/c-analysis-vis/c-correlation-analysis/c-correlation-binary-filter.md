---
description: 상관 관계 매트릭스의 이진 필터를 사용하면 상관 관계가 있는 지표 중 하나 또는 둘 다에 대한 값을 제한하여 비교에 더 집중할 수 있습니다.
solution: Analytics
title: 상관 관계 매트릭스의 이진 필터
topic: Data workbench
uuid: 61c3ca37-cfa2-49dc-87de-4e9a44647eca
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 상관 관계 매트릭스의 이진 필터{#binary-filter-in-the-correlation-matrix}

상관 관계 매트릭스의 이진 필터를 사용하면 상관 관계가 있는 지표 중 하나 또는 둘 다에 대한 값을 제한하여 비교에 더 집중할 수 있습니다.

상관 관계 행렬에 이진 필터를 설정하려면

1. 상관 관계 매트릭스에서 지표 이름을 마우스 오른쪽 단추로 클릭합니다.
1. 지표 **세부 사항 편집을 선택합니다**.

   ![](assets/correlation_matrix_binary_filter.png)

   창문이 **[!UICONTROL Edit Correlation Metric Details]** 열립니다.

   ![](assets/correlation_matrix_metric_details.png)

1. 이진 필터를 설정합니다.

   먼저 **[!UICONTROL Inactive]** 설정을 클릭합니다. 필터를 로 설정하고 비교 및 값 **[!UICONTROL Active]** 필드를 표시하도록 **전환됩니다** **** .

   그런 다음 **[!UICONTROL Comparison]** 연산자를 선택하고 선택한 지표에 대한 필터를 **[!UICONTROL Value]** 설정하도록 설정합니다.

>[!IMPORTANT]
>
>데이터 워크벤치 6.2용 이진 필터가 새로운 기능으로 업데이트되어 이전 버전에 내장된 이진 필터로 상관 관계 행렬을 다시 빌드해야 합니다.

## 차원 요소 추가 {#section-f19f4e0368ca488e92d1e28bcc24417c}

차원 요소를 추가하여 지표를 제한할 수도 있습니다. 지표에는 연결된 요소가 하나만 있을 수 있습니다.

![](assets/correlation_matrix_element.png)

작업 영역을 마우스 오른쪽 단추로 클릭하고 표를 **선택합니다**. 해당 요소가 있는 차원을 열고 상관 관계 지표 세부 사항 편집 창의 **[!UICONTROL Element]** 설정으로 드래그하거나 상관 관계 매트릭스의 지표를 놓습니다.
