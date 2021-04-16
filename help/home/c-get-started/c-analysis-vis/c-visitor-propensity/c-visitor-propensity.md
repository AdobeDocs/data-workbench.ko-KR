---
description: 성향 점수를 사용하면 성공적인 전환이나 지정된 이벤트 완료 가능성을 기반으로 고객을 정의할 수 있습니다. 프로세스를 실행하거나 캠페인을 감독하기 전에 노력의 잠재적 영향을 최대화할 수 있습니다.
title: 성향 점수
uuid: 4f7163f5-6fe4-4f87-9e27-71ec8b4717af
exl-id: 832a1e6c-8eeb-4dcc-97e8-9570e1a6eb4f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 24%

---

# 성향 점수{#propensity-scoring}

성향 점수를 사용하면 성공적인 전환이나 지정된 이벤트 완료 가능성을 기반으로 고객을 정의할 수 있습니다. 프로세스를 실행하거나 캠페인을 감독하기 전에 노력의 잠재적 영향을 최대화할 수 있습니다.

## 성향 점수의 가치 {#section-c51ece66effc42de9b754f0f46027c1b}

성향 점수를 통해 데이터 검색을 수행하여 데이터 전체에 존재하는 숨겨진 행동 또는 패턴을 식별할 수 있습니다. 특히, 성향 점수는 단순 세그멘테이션이나 필터링보다 더 집중되고 객관적인 수단을 사용하여 유사한 고객 클러스터를 식별하는 데 도움이 됩니다. 또한, 성향 점수를 통해 가치가 높은 고객의 행동을 식별할 수 있는 예측 능력을 갖출 수 있습니다.

가치가 높은 대상을 식별하게 되면 최대의 효과를 위해 해당 고객들과 참여할 수 있습니다. 예를 들어, 비즈니스-비즈니스 회사인 경우 리드를 점수로 평가하고 오프라인으로 전환할 가능성을 식별할 수 있는 판매 콜 리드가 있을 수 있습니다. 모든 리드는 비용 증가를 수반하므로 매출 전환 가능성이 가장 큰 잠재고객을 식별하는 인센티브를 만드는 것이 가장 효과적이며 리소스에 집중할 수 있는 가장 저비용의 방법입니다.

성향 점수를 통해 특정 점수의 예측이나 이벤트 발생 가능성을 높이는 요인을 식별할 수 있지만, 다음과 같은 특정 질문에도 적용할 수 있습니다. 고객이 전환될 것인가? 고객이 이메일 반응할 것인가? 고객이 재구매할 것인가? 성향 점수를 통해 이러한 질문에 답할 수 있으며 설정 및 평가할 수 있는 행동에 대한 의향을 가진 고객을 식별할 수 있습니다.

또한 필터를 사용하여 선택적인 **[!UICONTROL Training Filter]** 기능을 사용하여 점수를 매길 방문자의 하위 집합을 정의할 수 있습니다. 필터가 적용되지 않으면 모든 방문자가 점수 지정을 위해 타깃팅됩니다.

## 성향 점수 시각화 기능 {#section-28413bc7d33b42c59cecb427c1c5a3fa}

성향 점수 시각화를 열려면 **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]**&#x200B;를 클릭합니다.

![](assets/propensity_visualization_GO.png)

성향 점수 시각화에는 도구 모음에서 액세스할 수 있는 다음 기능이 포함됩니다.

| 도구 모음 기능 | 설명 |
|---|---|
| 이동 | 매개변수를 설정한 후 를 클릭하여 채점 프로세스를 실행합니다. |
| 재설정 | 시각화의 모든 설정을 지웁니다. |
| 로드 | 채점 모델을 변경 및/또는 다시 작성할 수 있도록 이전에 만든 ScoreDim을 로드합니다. |
| 저장 | 필요에 따라 액세스 및 열도록 성향 점수 시각화를 흐림 파일로 저장합니다. |
| 제출 | 서버측 처리를 위해 점수 지정 작업을 제출합니다. |
| 옵션 | 방문자 하위 집합을 제한하도록 교육 필터를 설정합니다. 기본 필터는 **[!UICONTROL Train on Everyone]**&#x200B;이지만 작업 영역을 선택하거나 **[!UICONTROL Filter Editor]**&#x200B;를 사용하여 필터를 작성하여 변경할 수 있습니다. |
| Target 설정 | 종속적 변수를 설정합니다. |
| 지표 | 지표를 독립 변수로 추가합니다. |
| 요소 | Dimension 테이블의 `<Ctrl>` + `<Alt>` 키를 사용하여 Dimension 요소를 드래그합니다. |

**참조 항목**:

* [게인 및 리프트 차트](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a)입니다. 이러한 보기는 전체 채점 모델 또는 [!DNL Add Visualization> Predictive Analytics > Scoring.]에서 열 수 있습니다.
* [모델 뷰어](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-d4fdf4b335c04b0ea07e70ab9a7ce9dd)입니다. 이러한 보기는 전체 채점 모델 또는 [!DNL Add Visualization> Predictive Analytics > Scoring.]에서 열 수 있습니다.
* [복잡한 필터 설명](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-complex-filter.md#concept-f9c55e54837f4b5995a00bc950ce5dff) 기능입니다.

## 성향 점수 시각화 사용 {#section-63ced03fa2eb44f2b8a98d61a6c88122}

* **하나 이상의 필터를 정의하여 점수를 매길 방문자 인구를 정의합니다**. 이 선택 사항 **[!UICONTROL Training Filter]**&#x200B;을 사용하면 선택한 기준을 기반으로 방문자를 타게팅할 수 있습니다. 교육 필터가 적용되지 않으면 모든 방문자가 점수 지정을 위해 타깃팅됩니다. 교육 필터가 설정되면 각 방문자에게 여전히 점수가 부여되지만 점수 지정 결과는 정의된 방문자 모집단에게 의미가 있습니다.
* **긍정적인 방문자** 식별 종속 변수를 정의하여 원하는 결과와 일치하는 긍정적인 방문자를 식별하는 타겟 필터를 지정합니다. 매출액 > $10만큼 간단하거나 보다 복잡한 필터를 만들 수 있습니다.
* **Target 필터는 교육 필터와 같을 수 없습니다**. 논리적으로 Target 필터는 교육 필터에 추가되어야 하므로 긍정적인 방문자 인구의 하위 세트가 점수를 받습니다.
* **관심 변수(독립 변수)를 성향 점수 알고리즘에 대한 입력으로 선택합니다**. 지표 또는 Dimension의 개별 요소가 될 수 있습니다. 성향 점수 지정은 [방문자 클러스터링](../../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d)에서와 마찬가지로 사전 처리를 시작합니다. 시스템은 이전에 설정한 교육 필터의 정의와 일치하는 일정 양의 샘플(있는 경우)을 캡처하기 시작합니다. 현재 샘플 크기는 최소 20,000과 최대 100,000으로 채점 인구의 10%로 설정되며 채점 인구의 크기에 구속됩니다.

* 점수 Dimension에는 Target 변수와 일치하는 방문자의 가능성을 결정하는 0%에서 100%까지의 요소가 있습니다.
