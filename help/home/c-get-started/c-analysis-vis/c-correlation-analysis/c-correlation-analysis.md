---
description: 통계적 상관관계는 고급 데이터 마이닝을 통해 기회를 식별하기 위해 의미 있는 관계를 측정합니다.
title: 상관 관계 매트릭스
uuid: 7f6bdb65-dc31-4e27-9870-4c9402ee6031
exl-id: 79c23bb9-2b4b-4fe0-bfdb-52721fbbdf0c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# 상관 관계 매트릭스{#correlation-matrix}

{{eol}}

통계적 상관관계는 고급 데이터 마이닝을 통해 기회를 식별하기 위해 의미 있는 관계를 측정합니다.

를 사용하여 [퍼슨 상관 계수](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c)를 사용하면 상관 관계 매트릭스가 마케팅 캠페인에서 다음 단계를 더 잘 식별하거나, 사이트 디자인을 개선하거나, 추가적인 상관 관계를 위해 심층적인 고객 분석을 계속 진행하기 위해 관련 정보를 제공합니다.

## 상관 관계 매트릭스 작성 {#section-87ed12ccc1af4196a1b6534e621c4cbb}

상관 관계 매트릭스는 가산 차원이나 비가산 차원에 대해 지표를 비교합니다. 그런 다음 매트릭스를 수정하여 색상 피킹을 통해 시각화 내의 상관 관계를 강조 표시하거나 텍스트 맵, 열 맵 또는 두 가지 모두로 렌더링할 수 있습니다.

1. 상관 관계 매트릭스 를 엽니다.

   마우스 오른쪽 단추 클릭 [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Correlation Matrix]. 차원 테이블이 열립니다.

   ![](assets/correlation_matrix_2.png)

   다음과 같은 차원을 선택합니다 [!DNL Time] > [!DNL Day of the Week] 이 메뉴에서 상관 관계 테이블이 행렬의 모서리에서 식별된 차원과 행 및 열에 배치된 관련 지표로 열립니다. 요일 차원의 경우 **[!UICONTROL Visits]** 는 연결된 지표입니다.

   ![](assets/correlation_matrix_1.png)

   지표를 자신과 비교하기 때문에(완벽하지만 사용할 수 없는, 상관 관계를 반영함) 상관 관계는 1.000입니다.

1. 지표 중 하나를 변경합니다.

   마우스 오른쪽 단추를 클릭하고 을 선택합니다 **[!UICONTROL Change Metric]** 행 또는 열에서 지표를 변경하려면 다음을 수행합니다. 이렇게 하면 두 값 지표 간의 상관 관계가 설정됩니다.

   이 예제에서는 **[!UICONTROL Visits]** 열의 지표 **[!UICONTROL Internal Searches]**. 마우스 오른쪽 단추를 클릭하고 을 선택합니다 [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Internal Searches].

   ![](assets/correlation_matrix_change_metric.png)

1. 상관 관계 매트릭스에 지표를 더 추가합니다.

   지표 열 또는 행을 마우스 오른쪽 단추로 클릭합니다. 예를 들어 지표 메뉴에서 을 추가합니다. [!DNL Metric] > [!DNL Custom Events] > [!DNL Custom Event 1-10] > [!DNL Sign in Error].

   ![](assets/correlation_matrix_11.png)

   새 지표는 상관 관계 숫자가 있는 열에 나타납니다. 다음과 같은 다른 지표를 추가할 수 있습니다 **[!UICONTROL Email Signups]**&#x200B;를 입력하여 테이블을 생성합니다.

   ![](assets/correlation_matrix_6.png)

   또는 열에 있는 지표와 비교할 지표를 행에 추가합니다.

   ![](assets/correlation_matrix_add_metric.png)

1. (선택 사항) 차원 요소를 추가하여 지표를 제한합니다.

   작업 공간에서 마우스 오른쪽 단추를 클릭하고 을 선택합니다. **[!UICONTROL Table]**. 열려 있는 차원 테이블에서 Ctrl + Alt를 누르고 요소를 열 또는 행의 지표 위로 드래그합니다. 요소는 대괄호로 묶인 지표 옆에 표시됩니다.

   예를 들어 **[!UICONTROL Visits]** 지표를 선택할 수 있으므로 **[!UICONTROL Country]** 로서의 **[!UICONTROL New Zealand]**.

   ![](assets/correlation_matrix_dim_element.png)

   차원 요소를 선택하면 선택한 차원 요소를 기반으로 모든 지표의 상관 관계가 변경됩니다. 차원 창이 닫히면 &quot;뉴질랜드&quot;에 대한 방문 지표만 제한됩니다.

   >[!NOTE]
   >
   >차원 제한으로 지표를 변경하는 경우(마우스 오른쪽 단추를 클릭하고 선택) **[!UICONTROL Change Metric]**)이면 지표를 제한하는 차원 요소가 손실됩니다. 차원 요소를 다시 추가해야 합니다.

1. 만들기 [이진 필터](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-binary-filter.md#concept-24e1daff43c540f69019f236976da31c) 추가 제한. 테이블에서 지표를 마우스 오른쪽 단추로 클릭하고 메뉴에서 이진 필터 를 선택합니다.

## 상관 관계 계획 및 분석 목표 {#section-cc322da60b7e417ba29e72b0afeb6f79}

다음은 상관 관계 매트릭스 구축에 대한 일반적인 목표입니다.

**지정된 차원에 대해 두 지표 간의 관계를 식별합니다**. 이 예에서는 내부 검색, 로그인 및 설문 조사 표시된 지표 이벤트와 비교하여 방문, 이메일 등록 및 로그인 오류 지표와 함께 코어 차원, 요일 을 기준으로 매트릭스가 빌드되었습니다.

**가설 개발을 통해 집중 분석**. 상관 관계 분석을 실행한 후 다음 단계는 지표의 종속성 및 상관 관계를 찾는 것입니다. 예를 들어 내부 검색이 이메일 등록에 영향을 미친다는 것을 이해하면 해당 관계를 예측하고 마케팅 캠페인이나 웹 사이트 탐색 디자인을 수정할 수 있습니다.

**고급 데이터 마이닝 알고리즘을 포함할 지표 식별**. 대부분의 경우 주요 지표는 여러 상관 관계에 영향을 주는 것으로 표시되므로 식별됩니다. 이제 이러한 주요 지표를 가져와 추가 데이터 마이닝 분석에 적용하여 더 깊이 이해할 수 있습니다.

## 상관 관계 매트릭스 기능 정보 {#section-ef3626c665ea468a9ecdad624b4132f5}

**테이블 내의 차원 요소 필터링 및 선택은 값과 같은 값을 비교합니다**. 예를 들어 요일 차원을 사용한 다음 해당 핵심 차원의 요소(예: 요일 차원 테이블 내에서 특정 일 클릭)를 클릭하면 사용 가능한 상관 관계를 제공하지 않는 일치율 100%가 표시됩니다. 루트 차원이 요일이므로 요일 차원 테이블 내에서 선택한 모든 항목은 매트릭스를 일대일 상관 관계로 변경합니다.

![](assets/correlation_matrix_10.png)

하지만 1-1 상관 관계(모든 요소로 단일 선택을 하는 경우)는 해당 특정 날짜에만 적용됩니다. 여러 항목을 선택할 경우 반드시 1~1 상관관계가 유지되지 않으며, 1일 또는 1일 이상을 선택해도 항상 100% 일치를 산출하지는 않습니다.

**통계 상관 관계는 상관 관계가 있는 데이터 모델과 같지 않습니다**: Adobe Analytics 제품의 내역 참조. Data Workbench의 통계적 상관 관계는 [Pearson 상관 관계 모델](../../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-pearsons.md#concept-5996cb8c89fd4df5b47b7318e7a1d29c).

**산포도에 상관 관계 표시**. 산포도의 제목을 마우스 오른쪽 단추로 클릭하고 [!DNL Display Correlation] 에서 [!DNL Visualization] 메뉴 아래의 제품에서 사용할 수 있습니다. 상관 관계 값이 산포도의 오른쪽 위 섹션에 표시됩니다.

>[!NOTE]
>
>응용 프로그램에서 Pearsons 상관 관계 계산을 실행할 수 없는 경우 산포도 및 Pearsons 매트릭스에 &quot;계산 오류&quot;가 표시됩니다. 이는 일반적으로 데이터가 부족하기 때문에 방정식이 0으로 분할되도록 할 수 있습니다.
