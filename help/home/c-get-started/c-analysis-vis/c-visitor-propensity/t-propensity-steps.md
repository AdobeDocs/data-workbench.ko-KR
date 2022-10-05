---
description: 다음 단계에 따라 성향 점수 시각화를 사용하십시오.
title: 성향 점수 설정
uuid: afc9aada-3bf9-4ce6-8c43-a955771065b4
exl-id: e16a7062-636e-44a9-a07d-343d48bf1b4c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 2%

---

# 성향 점수 설정{#setting-up-propensity-scoring}

{{eol}}

다음 단계에 따라 성향 점수 시각화를 사용하십시오.

1. 새 작업 공간을 열고 **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]**.

   ![](assets/propensity_visualization.png)

1. 설정 **[!UICONTROL Target]** (종속 변수)

   다음을 선택하여 종속 변수를 설정합니다.

* **Dimension 요소**: 작업 공간에서 마우스 오른쪽 단추를 클릭하고 을 선택합니다. **[!UICONTROL Table]**. 그런 다음 Dimension 요소를 종속 변수로 선택합니다.

   또는

* **[!UICONTROL Filter Editor]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 클릭 **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Filter Editor]** 필터 편집기 시각화를 열려면 다음을 수행하십시오.

   ![](assets/propensity_visualization_filter_editor.png)

   Dimension 요소 또는 필터를 종속 변수로 선택한 후 **[!UICONTROL Set Target]**&#x200B;를 입력하여 종속 변수를 설명합니다. 그런 다음 **[!UICONTROL OK]** Target을 설정하려면 필터 상자가 강조 표시되어 있는지 확인합니다.

   ![](assets/propensity_visualization_setTarget.png)

   타겟에 지정하는 이름은 왼쪽 창에 나타나는 종속 변수입니다.
1. 독립 변수를 추가합니다.

   지표 또는 Dimension 요소를 사용하여 독립 변수를 추가합니다.

   ![](assets/propensity_visualization_metrics.png)

* **지표**. 성향 점수 도구 모음에서 **[!UICONTROL Metrics]** 메뉴 아래의 제품에서 사용할 수 있습니다.

* **Dimension 요소**: 작업 공간에서 마우스 오른쪽 단추를 클릭하고 을 선택합니다. **[!UICONTROL Table]**. 하나 이상의 Dimension 요소를 선택하고 아래의 왼쪽 열로 드래그합니다 **[!UICONTROL Independent Variables]** 또는 **[!UICONTROL Element]** 상자를 사용하여 `<Ctrl>` + `<Alt>` 키.

1. 설정 **[!UICONTROL Training Filter]**. 클릭 시 점수를 매길 방문자 세트를 정의할 수 있습니다 **[!UICONTROL Options]** > **[!UICONTROL Set Training Filter]** 성향 점수 도구 모음에서 를 클릭합니다. 이렇게 하면 점수를 매길 방문자만 사용하여 작성된 데이터 하위 세트가 제공됩니다. 예를 들어, 지난 달에 방문한 방문자, 호주에 거주하는 방문자 또는 특정 제품을 본 방문자 수.

   기본 필터는 다음과 같습니다 **[!UICONTROL Train on Everyone]**&#x200B;를 활성화하면 변경할 수 있습니다 **[!UICONTROL Dimension Elements]** 테이블 또는 **[!UICONTROL Filter Editor]**.

   Dimension 요소를 선택하거나 필터를 빌드하고 활성화된 상태에서 를 클릭한 다음 **옵션** > **교육 필터 설정**&#x200B;을 클릭하고 필터를 설명하는 이름을 입력한 다음 를 클릭합니다 **[!UICONTROL OK]**.
1. 입력을 모두 확인했으면 **[!UICONTROL Go]**.

   ![](assets/propensity_visualization_GO.png)

   점수 프로세스는 데이터를 여러 번 전달하여 시작됩니다. 그러면 결과가 퍼센트 라인 위에 막대 차트로 표시됩니다.
1. 성향 점수를 저장합니다.

   6.1부터 이제 성향 점수 저장 을 사용할 때 선택 사항이 제공됩니다.

* 차원
* Dimension 및 지표

   저장한 파일 두 개(차원 및 정의된 지표 모두)로 끝납니다.

   >[!NOTE]
   >
   >처리할 성향 점수를 제출하면 차원만 얻습니다.

   파생된 지표는 연결된 평균 점수 지표입니다.
1. 정확성을 확인합니다.

   시스템이 표시됩니다 **[!UICONTROL Model Complete]** 프로세스가 완료되면 점수 모델을 생성합니다.

   마우스 오른쪽 단추 클릭 **[!UICONTROL Model Complete]** 시스템에서 정의한 점수 모델의 정확도를 확인합니다. 0%에서 100% 사이의 값을 통해 방문자가 **[!UICONTROL Target]** 변수를 채우는 방법을 설명합니다.

   혼동 매트릭스는 실제 양수(AP), 실제 음수(AN), 예상 양수(PP) 및 예측된 음수(PN)의 조합으로 4개의 카운트를 제공합니다. 이 수치들은 우리가 진짜 답을 알고 있는 20% 보류된 테스트 데이터에 결과 점수 모델을 적용하여 얻습니다. 점수가 50%보다 큰 경우 양성 사례(정의된 이벤트와 일치)로 예측됩니다.

   ![](assets/propensity_lift_gain_1.png)

<table id="table_154BDD6D294C4ED1B8C15EC33B74B199"> 
 <tbody> 
  <tr> 
   <td colname="col1"><b> 정확도</b> </td> 
   <td colname="col2"> 모든 예측에 대한 올바른 예측을 식별하여 모델이 얼마나 정확한지 나타냅니다. <p>(TP + TN)/(TP + FP + TN + FN) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> 회수</b> </td> 
   <td colname="col2"> 점수 모델을 다시 식별하는 기능을 식별합니다. <p><b>TP / (TP + FN)</b> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> 정밀도</b> </td> 
   <td colname="col2">불일치 수준을 식별합니다. <p>TP / (TP + FP) </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 열기 [상승도 또는 이득 차트](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a)또는 [모델 뷰어](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-9f2593a8218140b7bd132a4c74e159f9).

   을(를) 마우스 오른쪽 단추로 클릭합니다. **모델 완료** 시각화 및 선택 **[!UICONTROL Lift Chart]**, **[!UICONTROL Gain Chart]**, 또는 **[!UICONTROL Model Viewer.]**
