---
description: 통계 상관 관계는 고급 데이터 마이닝을 통해 의미 있는 관계를 측정함으로써 기회를 식별합니다.
solution: Analytics
title: 상관 관계 매트릭스
topic: Data workbench
uuid: 7f6bdb65-dc31-4e27-9870-4c9402ee6031
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 상관 관계 매트릭스{#correlation-matrix}

통계 상관 관계는 고급 데이터 마이닝을 통해 의미 있는 관계를 측정함으로써 기회를 식별합니다.

Pearsons 상관 [계수를](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c)사용하면 상관 관계 매트릭스가 마케팅 캠페인의 다음 단계를 더 잘 식별하거나 사이트 디자인을 개선하거나 추가적인 상관 관계를 위해 심도 있는 고객 분석을 계속하기 위해 관련 정보를 제공합니다.

## 상관 관계 매트릭스 작성 {#section-87ed12ccc1af4196a1b6534e621c4cbb}

상관 관계 매트릭스는 계산 가능한 차원과 계산 가능한 차원과 지표를 비교합니다. 그런 다음 매트릭스를 수정하여 색상 선택을 통해 시각화 내의 상관 관계를 강조 표시하거나 텍스트 맵, 열 맵 또는 둘 다로 렌더링할 수 있습니다.

1. 상관 관계 지표를 엽니다.

   마우스 오른쪽 단추를 클릭하여 [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Correlation Matrix]을 클릭합니다. 차원 테이블이 열립니다.

   ![](assets/correlation_matrix_2.png)

   이 메뉴에서 [!DNL Time] > [!DNL Day of the Week] 등과 같은 차원을 선택합니다. 상관 관계 테이블은 행렬의 모서리에서 식별된 차원과 행 및 열에 배치된 관련 지표로 열립니다. 요일 차원의 경우 관련 지표가 **[!UICONTROL Visits]** 됩니다.

   ![](assets/correlation_matrix_1.png)

   지표를 자신과 비교하기 때문에 상관관계는 1.000입니다(완벽하지만 사용할 수 없는 상관 관계).

1. 지표 중 하나를 변경합니다.

   마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Change Metric]** 선택하여 행이나 열에서 지표를 변경합니다. 이렇게 하면 값의 두 지표 간의 상관 관계가 설정됩니다.

   이 예에서는 열의 **[!UICONTROL Visits]** 지표를 다음으로 변경합니다 **[!UICONTROL Internal Searches]**. 마우스 오른쪽 단추를 클릭하고 [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Internal Searches]을 선택합니다.

   ![](assets/correlation_matrix_change_metric.png)

1. 상관 관계 매트릭스에 지표를 더 추가합니다.

   지표 열 또는 행을 마우스 오른쪽 단추로 클릭합니다. 예를 들어 지표 메뉴에서 > [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Sign in Error]을 추가합니다.

   ![](assets/correlation_matrix_11.png)

   새 지표는 상관 관계 번호가 있는 열에 나타납니다. 표 작성과 같은 다른 지표를 추가할 **[!UICONTROL Email Signups]**&#x200B;수 있습니다.

   ![](assets/correlation_matrix_6.png)

   또는 열에 있는 지표와 비교할 지표를 행에 추가합니다.

   ![](assets/correlation_matrix_add_metric.png)

1. (선택 사항) 차원 요소를 추가하여 지표를 제한합니다.

   작업 영역을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Table]**&#x200B;선택합니다. 열린 차원 테이블에서 Ctrl + Alt를 누르고 요소를 열 또는 행의 지표 위로 드래그합니다. 요소는 대괄호로 표시된 지표 옆에 나타납니다.

   예를 들어, **[!UICONTROL Visits]** 지표의 경우 **[!UICONTROL Country]** 를 **[!UICONTROL New Zealand]**&#x200B;선택하여 제한할 수 있습니다.

   ![](assets/correlation_matrix_dim_element.png)

   차원 요소를 선택하면 선택한 차원 요소를 기준으로 모든 지표의 상관 관계가 변경됩니다. 차원 창이 닫히면 &quot;뉴질랜드&quot;에 대한 방문 지표만 제한됩니다.

   >[!NOTE]
   >
   >차원 제약 조건으로 지표를 변경하는 경우(마우스 오른쪽 단추 클릭 및 선택 **[!UICONTROL Change Metric]**) 지표를 제한하는 차원 요소가 손실됩니다. 차원 요소를 다시 추가해야 합니다.

1. 이진 [필터를](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-binary-filter.md#concept-24e1daff43c540f69019f236976da31c) 만들어 지표를 추가로 제한합니다. 테이블에서 지표를 마우스 오른쪽 단추로 클릭하고 메뉴에서 이진 필터를 선택합니다.

## 상관 관계 계획 및 분석 목표 {#section-cc322da60b7e417ba29e72b0afeb6f79}

다음은 상관 관계 매트릭스 구축을 위한 일반적인 목표입니다.

**지정된 차원에**&#x200B;대해 두 지표 간의 관계를 식별합니다. 이 예에서는 지표 방문, 이메일 등록 및 로그인 오류가 내부 검색, 로그인 및 설문 조사 표시 지표 이벤트와 비교하여 핵심 차원 요일을 중심으로 매트릭스가 구축되었습니다.

**가설을 개발하여 분석에**&#x200B;집중할 수 있습니다. 상관 관계 분석을 실행한 후 다음 단계는 지표의 종속성 및 상관 관계를 찾는 것입니다. 예를 들어, 내부 검색이 이메일 등록에 영향을 미친다는 것을 이해하면 해당 관계를 예측하고 마케팅 캠페인 또는 웹 사이트 탐색 디자인을 수정하는 경로를 제공합니다.

**고급 데이터 마이닝 알고리즘을**&#x200B;포함할 지표를 식별합니다. 대부분의 경우 주요 지표는 여러 상관 관계에 영향을 주는 것으로 보여지기 때문에 식별됩니다. 이제 이러한 주요 지표를 가져와 추가 데이터 마이닝 분석에 적용하여 보다 심층적인 통찰력을 얻을 수 있습니다.

## 상관 관계 매트릭스 기능 정보 {#section-ef3626c665ea468a9ecdad624b4132f5}

**테이블 내의 차원 요소를 필터링하고 선택하면 값과**&#x200B;비슷한 값이 비교됩니다. 예를 들어 요일 차원을 사용한 다음 요일 차원 테이블에서 특정 요일을 클릭하는 것과 같이 핵심 차원의 요소를 클릭하면 사용 가능한 상관 관계가 없는 100%에서 일치할 1대 1이 렌더링됩니다. 루트 차원이 요일이므로 요일 차원 테이블 내에서 선택한 모든 항목은 매트릭스를 1대1 상관 관계로 변경합니다.

![](assets/correlation_matrix_10.png)

그러나 1-1 상관 관계(모든 요소로 단일 선택 시)는 해당 날짜에만 적용됩니다. 여러 항목을 선택하는 경우 반드시 1-1 상관 관계로 유지되지 않으며, 주 중 1일 또는 1일 이상을 선택하더라도 항상 100% 일치 항목은 없습니다.

**통계 상관 관계는 Adobe Analytics 제품의 내역 참조인**&#x200B;상관 관계 데이터 모델과 같지 않습니다. 데이터 워크벤치의 통계적 상관 관계는 Pearson Correlation 모델을 [기반으로](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c)합니다.

**산포도 내 상관 관계**&#x200B;표시 산포도의 제목을 마우스 오른쪽 단추로 클릭하고 [!DNL Display Correlation] 메뉴에서 [!DNL Visualization] 선택합니다. 상관 관계 값은 산포도 오른쪽 위 섹션에 표시됩니다.

>[!NOTE]
>
>애플리케이션에서 Pearsons 상관 관계 계산을 실행할 수 없는 경우 산포도 및 Pearsons 매트릭스에 &quot;계산 오류&quot;가 표시됩니다. 일반적으로 데이터가 불충분하기 때문에 방정식을 0으로 분할하려고 할 수 있습니다.
